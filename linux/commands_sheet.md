#### How to identify kernel version of the currently running system
`uname -a`  Gives you every detail i.e System Information (Hostname, Kernel, OS, Architecture, Release etc)

`uname -v`  Kernel Version

`uname -r`  Kernel Release

#### How to identify current IP Address (i.e IPV6 or ETH0)
##### Legacy Way 
`ifconfig` Bunch of all available devices (Ethernet, IPV4, IPV6 etc)

##### New Way
`ip addr show` show all interface devices detail

`ip addr show eth0` show info regarding interface eth0

#### Available free space
`df -ah`  Give all filesystem info

#### How do you manage service (start/stop/reload service)
##### Legacy Way
`service udev status`
##### New Way
`systemctl status udev`

#### How would u check the given size of the directory
`du -sh code`  -> 375M code (Code is directory)

#### How would u check for open ports
`sudo netstat  -tulpn`

`t = tcp`

`u = udp`

#### How to check Linux process information (CPU usage, memory, user information, etc.)?
`sudo ps aux | grep nginx`

Nginx Process Information, Another way

`top` with too much information (descend order % cpu)

`htop` another alternate

A common and convenient way of using ps to obtain much more complete information about the processes currently on the system is to use the following:

ps -aux | less

The `-a` option tells ps to list the processes of all users on the system rather than just those of the current user, with the exception of group leaders and processes not associated with a terminal. A group leader is the first member of a group of related processes.

The `-u` option tells ps to provide detailed information about each process. The `-x` option adds to the list processes that have no controlling terminal, such as daemons, which are programs that are launched during booting (i.e., computer startup) and run unobtrusively in the background until they are activated by a particular event or condition.

As the list of processes can be quite long and occupy more than a single screen, the output of ps -aux can be piped (i.e., transferred) to the `less` command, which lets it be viewed one screenful at a time. The output can be advanced one screen forward by pressing the SPACE bar and one screen backward by pressing the b key

Reference `http://www.linfo.org/ps.html`

#### Show which programs are listening on TCP and UDP ports
`netstat -plunt`

#### how would you mount a new volume
`mount {absolute_path_to_the_volume}`

`mount  /dev/sda2 /mnt`

check existing mounts, do without any arguments.
`mount`

#### Man pages, How would you find information about unknown commands
`man <command>`

`man ps`
