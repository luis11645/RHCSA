# 10.1 Access the Remote Command Line with SSH #

* StrictHostKeyChecking parameter is set to yes fail at the first try if the publickey is not matching
* StrictHostKeyChecking parameter is set to no the ssh add the key in `~./known_hosts` file
* We can verify the SSH fingerprint with the command ssh-keygen -lf <path-to-publickey>

# Configure SSH Key-Based Authentication #

* To configure ssh-agent we have to first execute `eval $(ssh-agent)` and then execute `ssh-add` command and enter the passphrase.
