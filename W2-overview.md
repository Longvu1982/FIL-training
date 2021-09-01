  
# WEEK 2 Overview: Network Layer 1, 2 and 3
## Layer 1: Physical layer 
#### 1. Overview and purpose
* It is the lowest layer of the OSI reference model. This layer need to be established before any network communication can occur.
* It can be wired or wireless
* It contains information in the form of **bits**.
* It recives a complete Frame of the data link and transimits to other devices'physical layer after encodes the frame as a series of signals
* It requires a **NIC** to connect the devices to the network
#### 2. Characteristics
1. Encoding
    * Converts bits into predictable patterns which can be recognize by other devices (HDB3, manchester, NRZ, bipolar, ...)
    &nbsp;

    ![HDB3](https://upload.wikimedia.org/wikipedia/commons/6/63/AMI%2C_HDB3_%281%29.jpg)
    <div style="text-align: center; font-style: italic "> HDB3 encoding example </div>
2. Signaling
    * Is the way the bits values, could be 0 or 1 or others depend on the method
3. Bandwidth
    * The capacity that the medium can carry data, it mesures the amount of data that transmit from places to places in a given amount of time
    &nbsp;
    <div style="display: flex; justify-content: center;"> <img src="https://learn-networking.com/wp-content/oldimages/units-of-bandwidth.jpg" alt=""></div>
    &nbsp;
    <div style="text-align: center; font-style: italic "> Bandwidth Units </div>

    * Terminology
      * **Latency**: Amount of time, including delays, for data to travel from one given point to another

      * **Throughput**: The measure of the transfer of bits across the media over a given period of time

      * **Goodput**:
        * The measure of usable data transferred over a given period of time
        * Goodput = Throughput - traffic overhead
        &nbsp; 
4. Protocal: Ethernet (IEEE 802.3), Token Ring, RS-232, FDDI, and others       

5. Cabling
   1. Copper
      * The most common type of cabling used in networks today: inexpensive, easy to install and low resistance to electrical current flow.
      * Limitations:
        * Attenuation – the signal get weaker the further it goes/ 
        * It can distort and corrupt the data signals (Electromagnetic Interference (EMI) and Radio Frequency Interference (RFI) and Crosstalk). <!--xuyem am-->
      * Mitigation: <!--han che giam thieu gioi han-->
        * Strict adherence to cable length limits will mitigate attenuation.
        * Some kinds of copper cable mitigate EMI and RFI by using metallic shielding and grounding.
        * Some kinds of copper cable mitigate crosstalk by twisting opposing circuit pair wires together
      &nbsp;
    <div style="display: flex; justify-content: center;"> <img style="width: 300px;" src="https://www.shanpowercable.com/photo/pl15271230-2_5_core_flexible_copper_conductor_pvc_sheathed_pvc_insulated_wire_cable.jpg" alt=""></div>
    &nbsp;
    <div style="text-align: center; font-style: italic "> Copper cable</div>  
    &nbsp;
    &nbsp;
    &nbsp;

   2. UTP (Unshielded Twisted Pair)
      * UTP has **four pairs of color-coded copper wires** twisted together and encased in a flexible plastic sheath. No shielding is used. UTP relies on the following properties to limit crosstalk:
        * Cancellation - Each wire in a pair of wires uses opposite polarity. <!--phan cuc nguoc--> One wire is negative, the other wire is positive. They are twisted together and the magnetic fields effectively cancel each other and outside EMI/RFI.
        * Variation in twists per foot in each wire - Each wire is twisted a different amount, which helps prevent crosstalk amongst the wires in the cable.
        https://www.nestorcables.com/media/tuotekuvat/kaapelikuvat/cache/nestor_cables_fzovdmu-sd-1100x9999.png


   3. Fiber-Optic
      * Not as common as UTP because of the cost but suitable for some specific scenarios
      * Transmits data over longer distances at higher bandwidth than any other networking media
      * Less susceptible to attenuation <!--suy hao-->, and completely immune to EMI/RFI
      * Made of flexible, extremely thin strands <!--soi--> of very pure glass
      * Uses a laser or LED to encode bits as pulses of light
      * The fiber-optic cable acts as a wave guide to transmit light between the two ends with minimal signal loss
        &nbsp;
    <div style="display: flex; justify-content: center;"> <img style="width: 400px;" src="https://internetviettel.vn/wp-content/uploads/2017/05/Multimode-%C4%91a-mode-2-768x576.jpg" alt=""></div>
    &nbsp;
    <div style="text-align: center; font-style: italic "> Fiber-optic cable</div>  
    &nbsp;
    &nbsp;
    &nbsp; 
      

&nbsp;
&nbsp; 


## Layer 2: Data-link layer 
#### 1. Overview and purpose
* It is responsible for communications between end-device NIC (network interface card)
* It allows upper layer protocols to access the physical layer media 
* It also performs **error detection** and **rejects corrupts frames**.
* Packets exchanged between nodes may experience numerous data link layers and media transitions.
* At each hop along the path, a router performs **four basic Layer 2 functions**:
  * Accepts a frame from the network medium.
  * De-encapsulates the frame to expose the encapsulated packet.
  * Re-encapsulates the packet into a new frame.
  * Forwards the new frame on the medium of the next network segment.

#### 2. Characteristics and standards
1. Protocols
  Data link layer protocols are defined by engineering organizations:
     * Institute for Electrical and Electronic Engineers **(IEEE)**.
     * International Telecommunications Union **(ITU)**.
     * International Organizations for Standardization **(ISO)**.
     * American National Standards Institute **(ANSI)**.

2. Topologies  
     * The topology of a network is the **arrangement and relationship** of the **network devices and the interconnections** between them.
     * Two types of topologies: **Physical** and **Logical**
       * **Physical topology**– shows physical connections and how devices are interconnected.
       * **Logical topology** – identifies the virtual connections between devices using device **interfaces and IP addressing schemes**.
      &nbsp;
       <div style="display: flex; justify-content: center;"> <img src="https://www.researchgate.net/profile/Ye-Tian-63/publication/330952912/figure/fig2/AS:746079754674177@1554890683097/Physical-topology-of-Testbed.png" alt=""></div>
    &nbsp;
    <div style="text-align: center; font-style: italic "> Physical topology</div>   
    &nbsp;
    &nbsp;
      <div style="display: flex; justify-content: center;"> <img src="https://beautbelsblog.files.wordpress.com/2009/11/logical.jpg?w=584" alt=""></div>
    &nbsp;
    <div style="text-align: center; font-style: italic "> Logical topology</div>   
    &nbsp;
    &nbsp;

    1. Physical WAN topologies
       1. Point-to-point – the simplest and most common WAN topology. Consists of a permanent link between two endpoints.
              <div style="display: flex; justify-content: center;"> <img  src="https://www.timigate.com/wp-content/uploads/2018/05/ppp.png" alt=""></div>
              &nbsp; 
       1. Hub and spoke – similar to a star topology where a central site interconnects branch sites through point-to-point links.
               <div style="display: flex; justify-content: center;"> <img style="width: 300px;" src="https://blog.bmtmicro.com/wp-content/uploads/2015/08/hub-spoke-generic.gif" alt=""></div>
              &nbsp; 
       3. Mesh – provides high availability but requires every end system to be connected to every other end system.
              <div style="display: flex; justify-content: center;"> <img style="width: 450px;" src="https://i.pinimg.com/originals/0e/68/a6/0e68a6b77c6997a1de2159593ca4e6b7.png" alt=""></div>
              &nbsp;  
    2. Physical LAN topologies
      End devices on LANs are typically interconnected using a **star or extended star** topology. Star and extended star topologies are **easy to install**, very scalable and **easy to troubleshoot**.
      Additional:
         * Bus: All end systems chained together and terminated on each end.
         * Ring – Each end system is connected to its respective neighbors to form a ring.
                &nbsp;  
                <div style="display: flex; justify-content: center;"> <img style="width: 450px;" src="https://kysudien.files.wordpress.com/2013/08/topomang.png" alt=""></div>
              &nbsp;   
    3. Other toplogies
       1. Half and Full Duplex Communication
       2. Access Control Methods
       3. Contention-Based Access – CSMA/CD
       4. Contention-Based Access – CSMA/CA

3. Data link frame   
                &nbsp;  
                <div style="display: flex;  flex-direction: column; justify-content: center; align-items:center"> <img style="width: 550px;" src="https://lh3.googleusercontent.com/proxy/RmPHvL47MnjJRsx_tasr4CeldJp8FL1ogeNGo0RN9GdNfwQ8LWy9IXBrIaAtGIP7D0QAvtwGSQinoCn9AYID0s351edBACa6k9InSg" alt="">
                <img style="width: 800px;" src="./assets/img/Ảnh1.png" alt=""></div>
                &nbsp;    <!--Payload- tai trong-->
       
       



  
 

