[Safe fun substitute](../_attach/Docs/pdf/Safe_fun.pdf)

#### POSIX

下表中所列的均为异步信号安全函数，来自POSIX标准。应用程序可以在信号处理程序中调用这些异步安全函数。
```
_Exit()
fexecve()
posix_trace_event()
sigprocmask()
_exit()
fork()
pselect()
sigqueue()
abort()
fstat()
pthread_kill()
sigset()
accept()
fstatat()
pthread_self()
sigsuspend()
access()
fsync()
pthread_sigmask()
sleep()
aio_error()
ftruncate()
raise()
sockatmark()
aio_return()
futimens()
read()
socket()
aio_suspend()
getegid()
readlink()
socketpair()
alarm()
geteuid()
readlinkat()
stat()
bind()
getgid()
recv()
symlink()
cfgetispeed()
getgroups()
recvfrom()
symlinkat()
cfgetospeed()
getpeername()
recvmsg()
tcdrain()
cfsetispeed()
getpgrp()
rename()
tcflow()
cfsetospeed()
getpid()
renameat()
tcflush()
chdir()
getppid()
rmdir()
tcgetattr()
chmod()
getsockname()
select()
tcgetpgrp()
chown()
getsockopt()
sem_post()
tcsendbreak()
clock_gettime()
getuid()
send()
tcsetattr()
close()
kill()
sendmsg()
tcsetpgrp()
connect()
link()
sendto()
time()
creat()
linkat()
setgid()
timer_getoverrun()
dup()
listen()
setpgid()
timer_gettime()
dup2()
lseek()
setsid()
timer_settime()
execl()
lstat()
setsockopt()
times()
execle()
mkdir()
setuid()
umask()
execv()
mkdirat()
shutdown()
uname()
execve()
mkfifo()
sigaction()
unlink()
faccessat()
mkfifoat()
sigaddset()
unlinkat()
fchdir()
mknod()
sigdelset()
utime()
fchmod()
mknodat()
sigemptyset()
utimensat()
fchmodat()
open()
sigfillset()
utimes()
fchown()
openat()
sigismember()
wait()
fchownat()
pause()
signal()
waitpid()
fcntl()
pipe()
sigpause()
write()
fdatasync()
poll()
sigpending()
```

#### OpenBSD

OpenBSD singal()手册列出了少量异步安全函数，但是这些函数其它平台下可能不是安全的。这些函数包括：snprintf()， vsnprintf()和syslog_r()函数（只有当syslog_data结构体初始化为本地变量的情况下才可以）。
