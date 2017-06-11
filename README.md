# docker-know-how

### difference between docker and vagrant
*Vagrant*
* virtual machine, which provides virtual hardware on which an operating system and other programs can be installed
* It takes a long time (often minutes) to create and require significant resource overhead because they run a whole copy of an operating system

*Docker*
* no hardware virtualisation, programs running inside docker containers interface directly with the host's linux kernel
* no resources are wasted by simulating virtual hardware.
* docker is not a virtualisation technology, it helps you use the container technology already built into your operating system

### Why docker

### what problems does docker solve
* install software for an app, decide if it should be installed, then find out how to install it. Sometimes two software doesn't play well together now what do you do E.g 
** what if one application needs an upgraded dependency but the other does not
** what happens when you remove an application? Is it really gone?
** Can you remember all the changes you had to make to install the software you now want to remove and revert those changes?

### how does docker work 

##### Containers
* Unix operating system have used the term jail to describe a modified runtime environment, since 2005 after the release of Sun's Solaris 10 and Solaris Containers, container has became the prefered term

* Creating containers in Unix system is somewhat challenging and one can mistakenly configure a container that is prone to security loopholes or is in a inconsistent state.

* Docker uses existing container engines to provide consistent built according to best practices, in other words docker executes the pre-existing unix command for the user - reducing the risk of misconfiguration of containers and also the trouble of learning UNIX container commands.

##### What is docker
* Docker is a command-line program, a background daemon, and a set of remote services that take a logistical approach to solving common software problems and simplifying your experience installing, running, publish, and removing software. It accomplishes this using a unix technology called containers

##### basic computer stack vs docker
```                                                                                             
                                Basic computer stack                                            
                                                                                                
             ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┐                          
                                       ┌───────────────────────────┐                            
             │                      ┌──▶    Hello World Program    │ │                          
               ┌────────────────┐   │  └───────────────────────────┘                            
User Space   │ │  Command line  ├──┬┘  ┌───────────────────────────┐ │                          
               └────────────────┘  └───▶        Text Editor        │                            
             │                         └───────────────────────────┘ │                          
              ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                           
             ┌───────────────────────────────────────────────────────┐                          
             │                   Operating System                    │                          
             │                                                       │                          
             └───────────────────────────────────────────────────────┘                          
             ┌───────────────────────────────────────────────────────┐                          
             │                                                       │                          
             │                                                       │                          
             │       Hardware - cpu,ram,network interface..etc       │                          
             │                                                       │                          
             │                                                       │                          
             └───────────────────────────────────────────────────────┘                          
                                                                                                
                                                                      ┌───────────┐┌───────────┐
                                                                      │           ││           │
                           Docker running two containers              │           ││           │
                                                                      │           ││           │
             ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┐│           ││           │
                                       ┌───────────────────────────┐  │Hello World││Text Editor│
             │┌────────────────┐   ┌───▶        Docker CLI         │ ││  Program  ││           │
              │  Command line  │───┘   └───────────────────────────┘  │           ││           │
User Space   │└────────────────┘───┐   ┌───────────────────────────┐ ││           ││           │
                                   └───▶       Docker daemon       │  │           ││           │
             │                         └───────────────────────────┘ ││           ││           │
              ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ └───────────┘└───────────┘
             ┌─────────────────────────────────────────────────────────────────────────────────┐
             │                                Operating System                                 │
             │                                                                                 │
             └─────────────────────────────────────────────────────────────────────────────────┘
             ┌─────────────────────────────────────────────────────────────────────────────────┐
             │                                                                                 │
             │                                                                                 │
             │                    Hardware - cpu,ram,network interface..etc                    │
             │                                                                                 │
             │                                                                                 │
             └─────────────────────────────────────────────────────────────────────────────────┘
```


### when and origin

### future prospect