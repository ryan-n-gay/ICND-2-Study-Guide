# Cisco CCNA ICND2 200-105

## Welcome to ICND2

* Course Overview
  * Cisco's Mission
    * Move you to the Wide Are network
    * PPP
    * PPPoE
  * Content You'll Cover
    * Routing
      * OSPF
      * EIGRP
      * BGP
      * HSRP
      * SNMP
      * IP SLA
* Supplementary Files
  * GNS3
* Getting the most from this series
  * Repetition, Repetition, Repetition
  * Take Notes; Write Down Key Information you hear
  * Build a lab or GNs3/VIRL Away
  * Study Hard
  * Dig Deeper
  * "Fall" In Love

## Review Lab:

### Rebuilding ICND 1

* Understanding the Rebuilding Lab
  * Building the Topology in GNS3
    * Drop 4 Routers
      * Configuration
        * ISP symbol = Cloud
        * ISP, R1, R2, R3 Slot 1 = NM-4t
    * Drop 3 Routers
      * Configuration
        * S1, S2, S3 Slot 1 NM-16ESW
        * Change Symbol to ethernet-switch
    * Drop 3 Routers
      * Configuration
        * A, B, C
        * Change Symbol to Computer
    * Route Cables Per the Scenario Parameters
    * ![Base Topology](images/baseTopology.png)

### Step 1: Base Config

* Deploying the Base Configuration
  * ```text
    hostname PC-B
    line vty 0 4
      password NuggetLove
      login
      exit
      line console 0
        password NuggetLove
        login
        logging synchronous
        no exec-timeout
        exit
      enable secret cisco
      no ip domian-lookup
      banner motd %
        ********************
           DO NOT LOGIN IN
        ********************
        YOUR CHAIR WILL SINK
        IN QUICKSAND QUICKLY
        ********************

        %
    ```
  * Make your edits, and copy and past into the proper device.
  * ![Completion of Step 1 Topology](images/step1.png)

### Step 2: IP Addressing, Speed, and Duplex

* Configure Router and Switches IP Addresses, Speed, and Duplex