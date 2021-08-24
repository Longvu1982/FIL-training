# WEEK 1 Overview
1. Overview of Network
   
    1. What is Network and its useage ? 
   
        * Network is a **collection of devices** capable of **transmitting data** including terminal devices and systems (such as users, servers) that are connected to each other to be able to communicate and transmit data. In a network system can transport many different types of data, data types and applications (such as video, image,...).
        
        * Networks devices: 
            * End to end users' devieces
            * Connectors
            * Netword interface card **NIC**
              * Switch, hub, brigde: Gather data form end-users
              * Router: find optimal path
        
        * Network parameters:
          * Speed : transmittion speed *bps* ( bit per second )
          * Cost: the cost to build, setup and maintain the system
          * Security : tha data must be protected
          * Availability : available to access anytime
          * Reliability : low packet-loss-rate
          * Topology : A network diagram that shows administrators how devices are connected in a system and how data flows in the system.
        ---
    
    
    2. Distinguish among **PAN, LAN, MAN, WAN**
       
       1. **LAN** (local area network). It is a group of network devices that allow communication between various connected devices. Private ownership has control over the local area network rather than the public. LAN has a short propagation delay than MAN as well as WAN. It covers the smallest area such as colleges, schools, hospitals, and so on.
       
       2. **MAN** (metropolitan area network). It covers the largest area than LAN such as small towns, cities, etc. MAN connects two or more computers that reside within the same or completely different cities. MAN is expensive and should or might not be owned by one organization.
       
       3. **WAN** (wide area network). It covers a large area than LAN as well as a MAN such as country/continent etc. WAN is expensive and should or might not be owned by one organization. ***PSTN*** or ***satellite*** medium is used for wide area networks
       
       4. **PAN** (personal area network). It's a network covering a very small area, usually a small room. The best known wireless PAN network technology is **bluetooth**, and the most popular wired PAN is **USB**. 
---
2. Networks reference models
   1. OSI Model **(Open Systems Interconnection Model)**
       *  Overview
          * Transmit data between 2 Hosts, contain a total of 7 layers  
&nbsp;


              ![osi-model](https://itforvn.com/wp-content/uploads/2017/08/Osi-model.png)
&nbsp;

        
          * **Physical Layer ( Layer 1)** : convert data into binary to transmit using physical transmition lines
          * **Data Link Layer ( Layer 2 )**: It defines data encapsulation methods for different types of transmission lines. To interact with the protocols of the upper layer, the Data Link layer uses the MAC address - the specific address on this layer. **SWITCH** is a device that operates in this layer.
          * **Network Layer (Layer 3 )**: Its main purpose is to route the transmission and find the most optimal path for entities. The commonly used IP address of layer 3 is **Logical address**. The ROUTER is a specific device that oparate in this layer.
          * ***LESS involved*** layers (specificly for network only):
            * **Transport Layer ( Layer 4 )** : Manage the data transfering tasks from source to destination ( end to end or host to host ). To ensure the most optimal data transmission and smooth from layers 1,2,3.
            * **Session Layer ( Layer 5 )** : Establish, maintain and release data exchange sessions between applications on the two hosts.
            * **Presentation Layer ( Layer 6 )** : Translate to make sure the 2 hosts can understand each other.
            * **Application Layer ( Layer 7 )**:  Direct user interaction between applications and network services.
        * How it works ?
          *  The higher layers will send data to the the lower ones and wait for the result without caring about how the lower layers work
          *  One layer form one Host will communicate with the corresponding layer from another host, but to do so it needs to go through all lower layers until it reachs Physical layer and communicate with Physical layer from Host 2, then moves up to the corresponding layer.
          *  Encapsulation 
&nbsp;
&nbsp;
 
          ![Encapsulation ](https://itforvn.com/wp-content/uploads/2017/08/image3.jpeg)  
&nbsp;
&nbsp;
&nbsp;
          *  De - encapsulation 
&nbsp;
&nbsp;
 
          ![de-encapsulation ](https://itforvn.com/wp-content/uploads/2017/08/image5.jpeg)  
&nbsp;
&nbsp;
          * Data unit on layers:
            * Application, Presentation, Session : Data
            * Transport : Segment
            * Network : Packet
            * Data Link : Frame
            * Physical : Bit  
&nbsp;
      
     1. TCP/IP model       
&nbsp;
                ![tcp/ip-model-compare-to-OSI](https://itforvn.com/wp-content/uploads/2017/08/FOfAU.jpg)    
         * It has 4 layers
           * **Application Layer**: It has all the work from layer 5,6,7 in OSI Model. The entities of this layer has the same protocol agree on the data format and the ways each session is **established and managed.
           * **Transport Layer**: Similar to Transport layer of OSI. Well known protocols for this layer are TCP and UDP.
           * **Internet Layer**: Function as Network of OSI. Ip is widely used in this layer.
           * **Network Access Layer**: Function as the Data Link và Physical of OSi.
&nbsp;         
         * Widely used Protocals:
&nbsp;         
         ![protocal](https://itforvn.com/wp-content/uploads/2017/08/image7.jpeg) 