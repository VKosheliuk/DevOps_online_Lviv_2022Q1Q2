1. How many states could has a process in Linux

    <ul>There are five Linux process states</ul>
    <ul>They are as follows: running & runnable, interruptable_sleep, uninterruptable_sleep, stopped, and zombie.</ul>

2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current process.

<ul><i>systemd─┬─ModemManager───2*[{ModemManager}]</i></ul>
           <ul><i>├─NetworkManager───2*[{NetworkManager}]</i></ul>
           <ul><i> ├─accounts-daemon───2*[{accounts-daemon}]</i></ul>
          <ul><i> ├─acpid</i></ul>
         <ul><i> ├─avahi-daemon───avahi-daemon</i></ul>
          <ul><i> ├─colord───2*[{colord}]</i></ul>
           <ul><i>├─cron</i></ul>
          <ul><i> ├─cups-browsed───2*[{cups-browsed}]</i></ul>
          <ul><i>├─cupsd───dbus</i></ul>
         <ul><i> ├─dbus-daemon</i></ul>
         <ul><i> ├─fprintd───4*[{fprintd}]</i></ul>


3.What is a proc file system?

  <ul>Proc file system (procfs) is virtual file system created on fly when system boots and is dissolved at time of system shut down</ul>

4. Print information about the processor (its type, supported technologies, etc.).

  <ul><i>$ less /proc/cpuinfo</i></ul>

    <ul>processor       : 0</ul>
    <ul>vendor_id       : GenuineIntel</ul>
    <ul>cpu family      : 6</ul>
    <ul>model           : 62</ul>
    <ul>model name      : Intel(R) Xeon(R) CPU E5-2650 v2 @ 2.60GHz</ul>
    <ul>stepping        : 4</ul>
    <ul>microcode       : 0xffffffff</ul>
    <ul>cpu MHz         : 2593.750</ul>
    <ul>cache size      : 20480 KB</ul>
    <ul>physical id     : 0</ul>
    <ul>siblings        : 1</ul>
    <ul>core id         : 0</ul>
    <ul>cpu cores       : 1</ul>
    <ul>apicid          : 0</ul>
    <ul>initial apicid  : 0</ul>
    <ul>fpu             : yes</ul>
    <ul>fpu_exception   : yes</ul>
    <ul>cpuid level     : 13</ul>
    <ul>wp              : yes</ul>
    <ul>flags           : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_freq pni ssse3 cx16 pcid sse4_1 sse4_2 hypervisor lahf_lm pti fsgsbase md_clear flush_l1d arch_capabilities</ul>
    <ul>bugs            : cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs itlb_multihit</ul>
    <ul>bogomips        : 5187.50</ul>
    <ul>clflush size    : 64</ul>
    <ul>cache_alignment : 64</ul>
    <ul>address sizes   : 46 bits physical, 48 bits virtual</i></ul>
    <ul>power management:</ul>

5. Use the ps command to get information about the process. The information should be as follows: the owner of the process, the arguments with which the process was launched for execution, the group owner of this process, etc.

dell@dell:~$ ps
    PID TTY          TIME CMD
   2199 pts/0    00:00:00 bash
   2239 pts/0    00:00:00 less
   2278 pts/0    00:00:00 ps

6. How to define kernel processes and user processes?

User-space processes have its own virtual address space.
Kernel processes or threads do not have their own address space, they operate within kernel address space only. And they may be started before the kernel has started any user process (e.g. init).

7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. What condition are they in, or can they be arriving in?

dell@dell:~$ ps -a
    PID TTY          TIME CMD
    737 tty2     00:00:09 Xorg
    845 tty2     00:00:00 gnome-session-b
   2239 pts/0    00:00:00 less
   2296 pts/0    00:00:00 less
   2315 pts/0    00:00:00 ps

8. Display only the processes of a specific user.

ps -u dell

9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps command)?

vmstat 2
pcp
dstat

10. What information does top command display?

The top (table of processes) command shows a real-time view of running processes in Linux and displays kernel-managed tasks.

top - 21:54:05 up 22 min,  1 user,  load average: 0,23, 0,36, 0,36
Tasks: 190 total,   1 running, 185 sleeping,   4 stopped,   0 zombie
%Cpu(s):  1,9 us,  4,1 sy,  0,0 ni, 94,1 id,  0,0 wa,  0,0 hi,  0,0 si,  0,0 st
MiB Mem :   1978,0 total,    178,5 free,    713,2 used,   1086,2 buff/cache
MiB Swap:    448,5 total,    446,5 free,      2,0 used.   1089,4 avail Mem 

11. Display the processes of the specific user using the top command.

top -u dell

12. What interactive commands can be used to control the top command? Give a couple of examples.

us, user : time running un-niced user processes
sy, system : time running kernel processes
ni, nice : time running niced user processes
wa, IO-wait : time waiting for I/O completion
hi : time spent servicing hardware interrupts
si : time spent servicing software interrupts
st : time stolen from this vm by the hypervisor

13. Sort the contents of the processes window using various parameters (for example, the amount of processor time taken up, etc.)

top -hv|-bcEeHiOSs1 -d secs -n max -u|U user -p pids -o field -w
       [cols]

14. Concept of priority, what commands are used to set priority?

You can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority. Renice command will modify the scheduling priority of a running process. Linux Kernel schedules the process and allocates CPU time accordingly for each of them

15. Can I change the priority of a process using the top command? If so, how?

Once given top command, press r. Give PID value of the process you want to change the process value. Give renice value (from -20 to +19)
Nice value of -20 means highest priority value and +19 means lowest priority value. 0 is by default value

16. Examine the kill command. How to send with the kill command process control signal? Give an example of commonly used signals.

Signal Name : HUP, INT, TERM

17. Commands jobs, fg, bg, nohup. What are they for? Use the sleep, yes command to demonstrate the process control mechanism with fg, bg.

The jobs command will list all jobs on the system; active, stopped, or otherwise.
The fg command, short for the foreground, is a command that moves a background process on your current Linux shell to the foreground. 
This contrasts the bg command, short for background, that sends a process running in the foreground to the background in the current shell.



