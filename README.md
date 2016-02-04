# rpmsg-neo
General rpmsg for TTY and usr space interface using multiple endpoints

The current implmentation is for the Udoo Neo (http://www.udoo.org/udoo-neo/)  
Linux on A9 (rpmsg) <-----> (rpmsg) M4 on FreeRTOS 

The goal is to have one general Linux driver to support (1) Channel and (2) endpoints
- endpt 127 is for usr space 
- endpt 126 is for tty usr space
- endpt 125 is for Ethernet driver. Linux (Ethernet) (rpmsg) <-----> rpmsg LwIP stack FreeRTOS (M4)


usr-neoproxy.c is a test program to send, validate and provide bandwidth information.  Uses libev (http://software.schmorp.de/pkg/libev.html) library to manage epoll 

