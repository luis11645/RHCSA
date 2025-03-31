# Tune System Performance #

# 5.1 #

Defalt profiles are stored in /usr/lib/tuned and custom profiles are stored in /etc/tuned, /etc/tuned always have priority over /usr/lib/tuned.

`tuned-adm list`
`tuned-adm profile`
`tuned-adm profile_info`
`tuned-adm recommend`

`renice -n <nice-value> -p <PID> ` change the nice value of runnung process
`nice -n <nice-value> <command> ` start a process with a assigned nice value

