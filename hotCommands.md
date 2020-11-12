> `hostname`

> `id` && `id -I`

> `hostnamectl`

>For remote server login using the `ssh: ssh user@server-name`

>`vmstat` : Linux `vmstat` command used to display statistics of virtual memory, kernerl threads, disks, system processes, I/O blocks, interrupts, CPU activity and much more. By default vmstat command is not available under Linux systems you need to install a package called sysstat that includes a vmstat program. 

>`lsof` command used in many Linux/Unix like system that is used to display list of all the open files and the processes. The open files included are disk files, network sockets, pipes, devices and processes. One of the main reason for using this command is when a disk cannot be unmounted and displays the error that files are being used or opened. With this commmand you can easily identify which files are in use. The most common format for this command is.

>`tcpdump` one of the most widely used command-line network packet analyzer or packets sniffer program that is used capture or filter TCP/IP packets that received or transferred on a specific interface over a network. It also provides a option to save captured packages in a file for later analysis. tcpdump is almost available in all major Linux distributions.

>To find number of files/directories <br>`find directory-path_directory-name -type f | wc -l`

>## File Redirections<br>
>* `ls foobar > stdouterr.txt`<br>
this script will execute ls command for foobar and if foobar exists `bash` will write on `stdout` if it does not exists will write on `stderr`
>* for redirections we use `>` for stdout i.e succes<br>
`2>` for stderr i.e failure and `&>` for stdout or stderr any of them.

> ### `tar` command details <br>
> `tar -cvf destination_file source_file`<br>
>* c – Creates a new .tar archive file.
>* v – Verbosely show the .tar file progress.
>* f – File name type of the archive file.
>* z – gzip archive file
>* j – To create highly compressed tar file (`bz2`) (slow as compared to `gzip`)<br>
>`tar -xvf file_to_be_unzipped.tar`
>* x – To unzip<br>
>`tar -xvf zippedFile.tar -C directory_in_which_file_to_be_unzipped`<br>
> ## If you want to untar in a different directory then use option as `-C`<br>
>* t - will list the content of .tar file<br>
>* To extract a single file called cleanfiles.sh from cleanfiles.sh.tar use the following command. <br>
>`tar -xvf cleanfiles.sh.tar cleanfiles.sh` or `tar --extract --file=cleanfiles.sh.tar cleanfiles.sh`

