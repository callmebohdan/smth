Network traffic daemon
====

This daemon allow user to sniff packets from particular network interface (or all interfaces).
It can work in two modes - via CLI (Command Line Interface) and as independent daemon in background. Be careful about both modes! If user doesn't stop daemon (using 'make clean' or 'stop' command while executing daemon in CLI mode), then it will continue sniffing packets. In future that will lead to memory leaks.

Available options
----

This program uses build automation tool (make). It support following commands:
* **make**, **make all** - process all targets, in our case it's ``main`` and ``daemon``.
* **make main** - process target ``main``. It starts daemon, using command line interface..
* **make daemon** - process target ``daemon``. It starts daemon itself independently in background mode.
* **make clean** - delete all files, created by running make, including log.txt and IPlog.txt.
* **make help** - show this message.
