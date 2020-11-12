> ## What does the init process do?
    The program init is the process with process ID 1. It is responsible for initializing the system in the required way. init is started directly by the kernel and resists signal 9, which normally kills processes. All other programs are either started directly by init or by one of its child processes.

     init is centrally configured in the /etc/inittab file where the runlevels are defined (see Section 13.2.1, “Runlevels”). The file also specifies which services and daemons are available in each of the runlevels. Depending on the entries in /etc/inittab, several scripts are run by init. For reasons of clarity, these scripts, called init scripts, all reside in the directory /etc/init.d (see Section 13.2.2, “Init Scripts”).

    The entire process of starting the system and shutting it down is maintained by init. From this point of view, the kernel can be considered a background process whose task is to maintain all other processes and adjust CPU time and hardware access according to requests from other programs.

> ## Runlevels
    In Linux, runlevels define how the system is started and what services are available in the running system. After booting, the system starts as defined in `/etc/inittab` in the line initdefault. Usually this is 3 or 5. See Table 13.1, “Available Runlevels”. As an alternative, the runlevel can be specified at boot time (at the boot prompt, for instance). Any parameters that are not directly evaluated by the kernel itself are passed to init. 
> ### To change runlevels while the system is running, enter telinit and the corresponding number as an argument. Only the system administrator is allowed to do this. The following list summarizes the most important commands in the runlevel area.

* telinit 1 or shutdown now
    `The system changes to single user mode. This mode is used for system maintenance and administration tasks. `

* telinit 3
    `All essential programs and services (including network) are started and regular users are allowed to log in and work with the system without a graphical environment. `

* telinit 5
    `The graphical environment is enabled. Usually a display manager like XDM, GDM, or KDM is started. If autologin is enabled, the local user is logged in to the preselected window manager (GNOME or KDE or any other window manager). `

* telinit 0 or shutdown -h now
    `The system halts.`

* telinit 6 or shutdown -r now
    `The system halts then reboots.`