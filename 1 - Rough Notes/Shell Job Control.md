2024-09-18 12:01
Status:
Tags:
___
# Shell Job Control

The job control is an ability offer by Unix to stop and restart executing commands.
A command or program could be executed in:
- Background: in this case we are talking about [[Job Processes]].
- Foreground: program that is running in bash.

When you are running a command like this:

```bash
$ /usr/bin/firefox & [1] 1748
[1] 1748
```
We receive the job id and the pid of the process in background.
```ps
$ jobs
[1]+  Stopped                 sleep 60
```
- 1 is the id of the job
- + The plus sign indicated the current, default job (last suspended or sent to the background). The previous job is flagged as (`-`)
- Stopped: status of the job
- Sleep 60 The command or job itself.

___
## References
[[LPIC-1 Exam 101.pdf#page=]]