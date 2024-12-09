## 13.2 TNZ8NQ2

TNZ8NQ2: 4 x 10G line service processing board

## 13.2.1 Overview

| Board   | Description                           | Board Name (Silkscreen Name)   | Initial Version    |
|---------|---------------------------------------|--------------------------------|--------------------|
| TNZ8NQ2 | 4 x 10G line service processing board | NQ2                            | V100R009C00 SPC700 |

<!-- image -->

This document describes all boards supported by the device. Whether the boards can be supplied depends on the PCN release result. For details, contact the product manager of the local office.

## 13.2.2 Update Description

This section describes the hardware updates in V100R009C00SPC700 and later versions as well as the reasons for the updates. Any product versions that are not listed in the document means that they have no hardware updates.

## Hardware Updates in V100R021C10SPC300

| Hardware Update                          | Reason for the Change                                             |
|------------------------------------------|-------------------------------------------------------------------|
| The functions of the board are enhanced. | Added the support for the TNZ3UXCL board of the 1800 II Enhanced. |

## Hardware Updates in V100R009C00SPC700

| Hardware Update   | Reason for the Update                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Added the TNZ8NQ2 | The NQ2 board is a line board that supports                                                                                          |
| boards.           | hybrid transmission of OTN services  (ODU0/ ODU1/ODU2/ODU2e/ODUflex)  and packet data packets with a maximum bandwidth of 40 Gbit/s. |

## 13.2.3 Mappings and Substitution Relationships

## Mapping Relationship

Table 13-1 Mapping relationship of the TNZ8NQ2 board

| Board   | Matching Equipment   | Matching System Control Board - Cross- Connect Board   | Version of the Matching System Control and Cross- Connect Board   | Service Capacity                    |
|---------|----------------------|--------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------|
| TNZ8NQ2 | 1800 II Enhanced     | TNZ2UXCL                                               | V100R009C00 SPC700                                                | ● OTN: 40Gbit/s ● Packets: 40Gbit/s |
| TNZ8NQ2 | 1800 II Enhanced     | TNZ3UXCL                                               | V100R021C10 SPC300                                                | ● OTN: 40Gbit/s ● Packets:          |
| TNZ8NQ2 | 1800 V               | TNZ5UXCMS                                              | V100R009C00 SPC700                                                | ● OTN: 40Gbit/s ● Packets: 40Gbit/s |
| TNZ8NQ2 | 1800 V               | TNZ8XCH                                                | V100R009C00 SPC700                                                | ● OTN: 40Gbit/s ● Packets: Not      |

## NOTE

- ● The board inserted on a slave subrack can function only as a pure OTN board.
- ● The board supports only OTN features when it is used together with the TNZ8XCH board.

## RTU

None.

## Substitution

Table 13-2 TNZ8NQ2 substitution relationship

| Original Board   | Substitute Board   | Substitute Type       | Restriction                                                                                                                                                      |
|------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TNZ8N Q2         | TNZ8UNQ 2          | Version substitutio n | ● The TNZ8UNQ2 board can be created as Z8NQ2 on the NMS. The TNZ8UNQ2 can substitute for the TNZ8NQ2 with the NE software version is V100R019C10SPC700 or later. |
|                  | TNZ8UNQ 2          | Version substitutio n | ● After the substitution, the TNZ8UNQ2 board can function only as the substituted TNZ8NQ2 board.                                                                 |
|                  | TNZ8UNQ 2          | Version substitutio n | ● If the substitute board does not work with the system control board of the original board, the substitute board cannot be used.                                |

## 13.2.4 Front Panel

There are indicators and interfaces on the front panel of the NQ2 board.

## Appearance of the Front Panel

Figure 13-2 shows the front panel of the NQ2 board.

Figure 13-2 Front panel of the NQ2 board

<!-- image -->

## Indicators

There are some indicators on the front panel.

- ● Working status indicator (STAT) -red and green
- ● Service status indicator (SRV) - red, green, and orange
- ● WDM-side receive optical power status indicator (INn)- red, green, and orange

For details on the indicators, refer to 31.1 Board Indicators .

Table 13-3 describes each interface on the NQ2 board.

Table 13-3 Interfaces on the NQ2 board

| Interface    | Connector    | Function                                                                                                               | Required Cable      |
|--------------|--------------|------------------------------------------------------------------------------------------------------------------------|---------------------|
| IN1 to IN4   | LC           | Receives single-wavelength signals from the optical demultiplexing unit or the optical add and drop multiplexing unit. | 30.8.4.2 Connectors |
| OUT1 to OUT4 | LC           | Transmits single-wavelength signals to the optical multiplexing unit or the optical add and drop multiplexing unit.    | 30.8.4.2 Connectors |

## Laser Hazard Level

The laser hazard level of the board is HAZARD LEVEL 1, indicating that the maximum output optical power of each optical interface is lower than 10 dBm (10 mW).

## 13.2.5 Application

The NQ2 board is a line board that supports hybrid transmission of OTN services (ODU0/ODU1/ODU2/ODU2e/ODUflex) and packet data packets with a maximum bandwidth of 40 Gbit/s. It also supports transmission of one or two types of services. The NQ2 board processes and converts the received service signals into four OTU2/OTU2e signals, which are carried over ITU-T G.694.1-compliant DWDM wavelengths.

## Line Mode

Figure 13-3 illustrates the application of NQ2 board in a WDM system.

## Interfaces

Figure 13-3 Line mode applicationTable 13-4 Service mapping paths

<!-- image -->

| Input signal   | Mapping Path           |
|----------------|------------------------|
| Packets        |                        |
| OTN            | ODU0->ODU1->ODU2->OTU2 |
| OTN            | ODU0->ODU2->OTU2       |
| OTN            | ODU1->ODU2->OTU2       |
| OTN            | ODUflex->ODU2 ->OTU2   |
| OTN            | ODU2->OTU2             |
| OTN            | ODU2e->OTU2e           |

## NOTE

Figure 13-3 illustrates the service mapping path by considering that ODU Timeslot Configuration Mode has been set to Assign random .

- ● The NQ2 board supports the ODU0->ODU1->ODU2 mapping path when ODU Timeslot Configuration Mode is set to Assign consecutive .
- ● When the NQ2 board is provisioned with packet services, ODU Timeslot Configuration Mode cannot be set to Assign consecutive for the board.

The line boards at the two add/drop sites must have the same ODU timeslot allocation mode.

The NQ2 board supports only packet services when it functions as a regeneration board in line mode.

## Regeneration Mode

Figure 13-4 illustrates the regeneration mode application of the NQ2 board.

Figure 13-4 Regeneration mode application

<!-- image -->

NOTE

In regeneration mode, the NQ2 board supports bidirectional electrical regeneration. Ports IN1/ OUT1 and IN2/OUT2 are in the same group, and ports IN3/OUT3 and IN4/OUT4 are in the same group.

## 13.2.6 Functions and Features

## Functions and Features of the TNZ8NQ2 Board (OTN Line)

| Function and Feature   | Description                                                                                                                                                                                                                                |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic function         | Provides four line ports to convert a maximum of 32 channels of ODU0, 16 channels of ODU1, 4 channels of ODU2(e), or 32 channels of  ODUflex signals to 1 channel of OTU2(e). For details about the service mapping path, see Application. |
| Backplane capacity     | The total backplane bandwidth is 40 Gbit/s.                                                                                                                                                                                                |
| WDM  specification     | Supports the DWDM  specifications.                                                                                                                                                                                                         |

| Function and Feature       | Description                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tunable wavelength         | Supports tunable wavelength optical modules that provide for 80 wavelengths tunable in the C band with 50 GHz channel spacing.                                                                                             |
| FEC coding                 | FEC, AFEC-2 NOTE Boards adopting  different  error correction encoding modes cannot interoperate with each other.                                                                                                          |
| OTN overhead protocol      | Supports the OTN frame format and overhead processing  defined  by ITU-T G.709.                                                                                                                                            |
| OTN overhead               | ● WDM-side OTU2 layer: supports SM overhead processing. ● ODUk (k=0, 1, 2,  flex)  layer: supports PM overhead processing.                                                                                                 |
| Intra-board 1+1 protection | Supported                                                                                                                                                                                                                  |
| ODUk SNCP                  | Supported NOTE Support when k = 0, 1, 2, or  flex                                                                                                                                                                          |
| Tributary SNCP             | Supported                                                                                                                                                                                                                  |
| Overtemperature protection | Supported. If the temperature of a board exceeds the upper threshold and services are  affected,  the board will automatically reset the key chips to prevent a board damage.                                              |
| Physical clock             | Supported (ODU0, ODU1,  ODUflex)                                                                                                                                                                                           |
| IEEE 1588v2                | Not supported                                                                                                                                                                                                              |
| Outband DCN                | Supports communication over ESCs. NOTE For details about the DCN types supported by the board, see "Feature Description - Outband DCN - Introduction to DCN - DCN Communication Channel - Comparison Between OSC and ESC". |
| Electrical-layer ASON      | Supported NOTE Only supported when the TNZ5UXCMS/TNZ8XCH board is used.                                                                                                                                                    |
| Test frame                 | Not supported                                                                                                                                                                                                              |
| PRBS                       | Supports the PRBS function on the WDM side.                                                                                                                                                                                |
| Delay measurement          | Supported                                                                                                                                                                                                                  |

| Function and Feature                   | Description                                                                                               |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Channel loopback                       | Supports channel inloops and outloops.                                                                    |
| Port loopback                          | Supports WDM-side inloops and outloops. (This function has no impact on overheads and the PRBS function.) |
| Alarm and performance event monitoring | ● Supports the monitoring of BIP8 bytes (Bursty mode) to help locate line faults.                         |
| Alarm and performance event monitoring | ● Supports the monitoring of the laser bias current.                                                      |
| Alarm and performance event monitoring | ● Supports the laser temperature monitoring.                                                              |
| Alarm and performance event monitoring | ● Supports the optical power monitoring. ● Supports the monitoring of OTN alarms and performance events.  |

## Functions and Features of the TNZ8NQ2 Board (Packet)

| Function and Feature            | Description                                                                                                                                                                             |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic function                  | A maximum of 40 Gbit/s packets<->32 x ODU0/32 x  ODUflex/16 x ODU1/4 x ODU2/ODU2e<->4 x OTU2/OTU2e                                                                                      |
| Backplane bandwidth             | The total backplane bandwidth is 40 Gbit/s.                                                                                                                                             |
| Service processing capability   | The maximum service processing capability of the board is 40 Gbit/s. NOTE For the OptiX OSN 1800 II Enhanced chassis, if OTN services are  configured,  the board supports a maximum of |
| Ethernet data frame format      | IEEE 802.3/Ethernet II/IEEE 802.1q/IEEE 802.1p                                                                                                                                          |
| Maximum frame length for a port | The frame length is fixed at 9600 + 72 bytes and is not  configurable.                                                                                                                  |
| Service bearing medium          | Port, MPLS-TP, QinQ                                                                                                                                                                     |
| Native E-Line service type      | ● Point-to-point transparently transmitted E-Line services ● VLAN-based E-Line services                                                                                                 |
| Native E-LAN service type       | ● E-LAN service based on the IEEE 802.1d bridge ● E-LAN service based on the IEEE 802.1q bridge                                                                                         |

| Function and Feature                  | Description                                                                                                                                                                                             |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PW-carried E-Line service (VPWS) type | ● Port-based transparently transmitted E-Line services ● VLAN-based E-Line services                                                                                                                     |
| PW-carried E-LAN service (VPLS) type  | ● VPLS services based on Tag-Transparent ● VPLS services based on C-Aware ● VPLS services based on S-Aware                                                                                              |
| MS-PW                                 | Supported                                                                                                                                                                                               |
| HQoS                                  | Supported                                                                                                                                                                                               |
| LPT                                   | Supports point-to-point and point-to-multipoint link-state pass through (LPT) functions. NOTE If the LPT function is  configured,  the ports on the NQ2 board cannot be  configured  as UNI-side ports. |
| ERPS                                  | Supported                                                                                                                                                                                               |
| LAG                                   | ● Supports load sharing and non-load sharing. ● Supports manual and static aggregation.                                                                                                                 |
| MSTP                                  | Not Supported                                                                                                                                                                                           |
| MC-LAG                                | Supported NOTE Only supported when the 1800 V is used.                                                                                                                                                  |
| MC-PW APS                             | Supported NOTE Only supported when the 1800 V is used.                                                                                                                                                  |
| PW APS                                | Supports 1:1 PW APS.                                                                                                                                                                                    |
| PW FPS                                | Supports 1:1 PW FPS.                                                                                                                                                                                    |
| Tunnel APS                            | ● Supports 1:1 tunnel automatic protection switching (APS). ● Supports 1+1 tunnel automatic protection                                                                                                  |
| MRPS                                  | Supported NOTE MRPS protection can be  configured  together with PW APS but cannot be  configured  with tunnel APS.                                                                                     |
| IGMP Snooping                         | Supported                                                                                                                                                                                               |
| LLDP                                  | Supported                                                                                                                                                                                               |
| Ethernet service OAM                  | Supported                                                                                                                                                                                               |
| MPLS-TP OAM                           | Supported                                                                                                                                                                                               |

| Function and Feature     | Description                                                     |
|--------------------------|-----------------------------------------------------------------|
| RMON                     | Supported                                                       |
| Port  traffic  mirroring | Supported                                                       |
| Physical clock           | Not Supported                                                   |
| Inband DCN               | Supported                                                       |
| Jumbo frame              | Supports a jumbo frame containing a maximum of 9600 bytes. NOTE |

## 13.2.7 Working Principle and Signal Flow

The NQ2 board consists of switching interface module, signal processing module, WDM-side optical module, control and communication module, and power supply module.

## Functional Modules and Signal Flow

Figure 13-5 shows the functional modules and signal flow of the NQ2 board.

Figure 13-5 Functional modules and signal flow of the NQ2

<!-- image -->

The transmit and receive directions are defined in the signal flow of the NQ2 board. The transmit direction is defined as the directionfrom the backplane to the WDM side of the NQ2 board, and the receive direction is defined as the reverse direction.

## ● Transmit direction:

- -Packet service: The fabric interface circuit processes the data packets from the cross-connect board and maps the packets into the payload of ODUk signals.
- -OTN service:
- i. The ODUk cross-connect module receives the ODUk electrical signals from the cross-connect board through the backplane and sends the signals to the OTN processing module.
- ii. The OTN processing produces (by performing operations such as OTN framing and FEC coding) and sends four OTU2 electrical signals to the WDM-side optical module.
- iii. When the WDM-side optical module receives the four OTU2 electrical signals, it performs E/O conversion and sends out four

OTU2/OTU2e optical signals over four ITU-T G.694.1-compliant wavelengths through the OUT1 -OUT4 optical ports.

- ● Receive direction:
- -OTN service:
- i. The WDM-side optical module receives four OTU2/OTU2e optical signals over four ITU-T G.694.1-compliant wavelengths through the IN1 -IN4 optical ports. Then, the module performs O/E conversion, produces four OTU2/OTU2e electrical signals, and sends the four signals to the OTN processing module.
- ii. When the OTN processing module receives the four OTU2/OTU2e electrical signals, it performs operations, such as FEC decoding, demapping, and demultiplexing, and produces ODU0/ODU1/ ODUflex/ODU2/ODU2e signals.
- If Layer 2 processing has been defined, the module sends the signals to the packet processor. If the ODUk cross-connection has been defined, the module directs the signals to the ODUk cross-connect module.
- iii. The ODUk cross-connect module sends the ODUk signals to the backplane for grooming.
- -Packet service:
- The fabric interface circuit decodes the ODUk signals, performs serial/ parallel conversion, buffers the packets, and transmits them to the crossconnect board through the backplane.

## Module Functions

- ● WDM-side optical module

The module includes a receiver and a transmitter.

- -Receiver: performs the O/E conversion of OTU2/OTU2e optical signals.
- -Transmitter: performs the E/O conversion of OTU2/OTU2e optical signals.
- -Reports WDM side optical port performance.
- -Reports WDM side laser status.
- ● Signal processing module
- -ODUk cross-connect module
- Performs backplane cross-connections of ODUk signals.
- -OTN processing module
- Frames OTU2/OTU2e signals, processes the overheads of the OTU2/ OTU2e signals, and performs FEC encoding/decoding.
- ● Switching interface module
- Buffers packets, and manages and schedules queues. It also works with a cross-connect board to form a switching fabric, which performs switching on packets.
- ● Control and Communication Module
- -Controls all operations performed on the board.
- -Collects information about alarms, performance events, working status, and voltage monitoring from each module of the board.

- -Communicates with the system control and communication board.
- ● Power Supply Module

Converts the DC power supplied by the backplane into the power required by each module on the board.

## 13.2.8 Valid Slots

This topic describes the valid slots for the board.

Table 13-5 Valid slots

| Device                     |   Num ber of Occu pied Slots | Physical Slot         | Logical Slot          |
|----------------------------|------------------------------|-----------------------|-----------------------|
| OptiX OSN 1800 II Enhanced |                            1 | Slot1, Slot 4, Slot 6 | Slot1, Slot 4, Slot 6 |
| OptiX OSN 1800 V           |                            1 | Slot1 to Slot14       | Slot1 to Slot14       |

## NOTE

1800 II Enhanced Chassis:

- ● DC chassis: the board can be installed in Slot 4, Slot 6
- ● AC chassis: the board can be installed in Slot 1, Slot 6

1800 V Chassis:

- ● When the system control board is TNZ5UXCMS, TNZ8NQ2 can be installed in slot 9 to slot 14.
- ● When the system control board is TNZ8XCH, TNZ8NQ2 can be installed in slot 1 to slot 14.

## Restrictions on Board Insertion

When the board is installed in the OSN 1800 V chassis and works with TNZ5UXCMS, the restricted slots are classified into the following three groups, as shown in Figure 13-6 .

- ● Slots 2, 3, 9, and 10
- ● Slots 4, 5, 11, and 12
- ● Slots 6, 7, 13, and 14

Figure 13-6 Restricted slot groups

<!-- image -->

The use of the following boards in the preceding slot groups is restricted:

- ● Restricted dual-slot boards: TNZ8NS4/TNZ5UNS4/TNZ8UNS4/TNZ5EC1/ TNZ5TSC
- ● Restricted single-slot boards: TNZ5UNQ2/TNZ8UNQ2/TNZ8UTX2/TNZ6UNQ1/ TNZ8NQ2/TNZ8EX4
- ● Special board: TNF1EGS4D

The restrictions are as follows:

- ● When a restricted dual-slot board is installed in the left slot, only one restricted single-slot board can be installed in the right slot of the corresponding slot group.
- For example, when a restricted dual-slot board is installed in slots 2 and 3, only one restricted single-slot board can be installed in either slot 9 or 10.
- ● In each group of slots, the TNF1EGS4D board cannot be installed together with a restricted dual-slot board or restricted single-slot board.

<!-- image -->

The TNZ8NS4/TNZ5UNS4/TNZ8UNS4 board cannot be installed in slot 6, 7, 13, or 14.

## 13.2.9 NQ2 Parameters

This topic lists the board parameters that can be set or queried on the NMS.

## Working mode

Table 13-6 Working mode

| Value                            |
|----------------------------------|
| Line mode, Electrical relay mode |

## Parameters for WDM Ports

Table 13-7 Parameters for WDM ports

| Field                      | Value                                                | Description                                                                                                                   |
|----------------------------|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Optical Interface/ Channel | - port.                                              | Displays the position of the optical                                                                                          |
| Optical Interface Name     | -                                                    | Sets the optical port name.                                                                                                   |
| Channel Use Status         | Used, Unused Default: Used                           | Sets the occupancy status of the current channel of a board. When this parameter is set to Unused  for a port, service alarms |
| Optical Interface Loopback | Non-Loopback, Inloop, Outloop Default: Non- Loopback | Specifies  the loopback mode for the optical port on a board.                                                                 |
| Channel Loopback           | Non-Loopback, Inloop, Outloop Default: Non- Loopback | Sets the channel loopback mode.                                                                                               |
| Laser Status               | Off,  On Default: On                                 | Sets the laser status of a board.                                                                                             |
| Enable Auto- Sensing       | -                                                    | This parameter is unavailable for the board.                                                                                  |

| Field                                                       | Value                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEC Working State                                           | Enabled, Disabled Default: Enabled                                        | Determines whether to enable or disable the forward error correction (FEC) function for the optical port. For a colored optical module, the FEC function is enabled on the WDM side by default and cannot be disabled. For a gray optical module, disabling the FEC function on the WDM side will cause services to become abnormal, and disabling the FEC function on the clients ide will  affect  the transmission distance. |
| FEC Mode                                                    | FEC, SDFEC2 Default: ● Colored optical module: SDFEC2 ● Colorless optical | Sets the FEC mode of the current optical port. The setting of  FEC Mode  for two interconnected boards must be the same.                                                                                                                                                                                                                                                                                                        |
| Band Type/ Wavelength No./ Wavelength (nm)/ Frequency (THz) | -                                                                         | Sets the operating wavelength at the WDM-side optical port of a board.                                                                                                                                                                                                                                                                                                                                                          |
| Band Type                                                   | -                                                                         | Sets the band type.                                                                                                                                                                                                                                                                                                                                                                                                             |
| Tunable Wavelength Range                                    | -                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|                                                             |                                                                           | Sets the tunable wavelength range at the WDM-side optical port of a board.                                                                                                                                                                                                                                                                                                                                                      |
| Planned Wavelength No./ Wavelength (nm)/ Frequency (THz)    | C: 1/1529.16/196.050 to 80/1560.61/192.100 Default: /                     | Sets the wavelength number, wavelength and frequency of the current optical port on the WDM side of a board.                                                                                                                                                                                                                                                                                                                    |
| Planned Band Type                                           | C, Follow, / Default: /                                                   | Sets the band type of the current working wavelength.                                                                                                                                                                                                                                                                                                                                                                           |

| Field                                      | Value                                                             | Description                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OTN Overhead Transparently                 | Disabled, GCC1+GCC2 Enabled, Only GCC1 Enabled, Only GCC2 Enabled | Determines whether to process GCC1 and GCC2 in OTN overheads. ● When the parameter is set to Disabled , the system will process the GCC1 and GCC2 bytes in the OTN overhead.              |
| Transmitted                                | Default: Disabled                                                 | ● When the parameter is set to GCC1+GCC2 Enabled , the system will not process the GCC1 or GCC2 byte in the OTN                                                                           |
| OTN Overhead Transparent Transmission(Res) | Disabled, Enabled Default value: Disabled                         | Determines whether to process RES in OTN overheads. If the processing is not required, set this parameter to  Enabled ; otherwise, set it to  Disabled .                                  |
| Enable Line Rate                           | Disabled, Enabled Default value: Enabled                          | Determines whether to automatically switch between the Standard Mode  and  Speedup Mode  for the line rate.                                                                               |
| Line Rate                                  | Standard Mode, Speedup Mode Default: Standard Mode                | Used to  configure  the line rate of OTN. This parameter needs to be set to Speedup Mode  when ODU2e signals are cross-connect, and Standard Mode  when ODU2 signals are cross-connected. |

| Field                    | Value                                                | Description                                                                                                                                                                                                                                  |
|--------------------------|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRBS Test Status         | Enabled, Disabled Default: Disabled                  | Sets the pseudo-random binary sequence (PRBS) test status of a board. The PRBS test belongs to the fault diagnosis function and  affects channel services. After the PRBS                                                                    |
| NULL Mapping Status      | Enabled, Disabled Default: Disabled                  | Determines whether to enable the special frame test before deployment. When this parameter is set to  Enabled , the board sends the test frame where the payload consists of only 0. This parameter is used in the deployment commissioning. |
| ODUflex  Tolerance (ppm) | 0 to 100 Default: ● 3GSDI/ 3GSDIRBR: 10 ● CPRI4/6: 1 | Specifies  the tolerance of deviation between the actual client-side service rate and the specified  rate when the client-side service type is  ODUflex.                                                                                     |
| ASON Delay Time(ms)      | -                                                    | This parameter is unavailable for the board.                                                                                                                                                                                                 |

## Parameters for Ethernet Ports

Table 13-8 Basic attributes

| Field   | Value                                      | Description                                                      |
|---------|--------------------------------------------|------------------------------------------------------------------|
| Port    | -                                          | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1). |
| Name    | - Specifies  the  self-defined  port name. |                                                                  |

| Field                    | Value                                        | Description                                                                                                                           |
|--------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Port Enabled             | -                                            | This parameter is unavailable for the board.                                                                                          |
| Port Mode                | Layer 2, Layer 3, Layer Mix Default: Layer 2 | Specifies  the working mode of the Ethernet port. ● Layer 2 : The port can carry port- based or QinQ-link-based Ethernet              |
| Encapsulation Type       | 802.1Q, QinQ, Null Default: 802.1Q           | tunnels. Selects the means of processing the accessed packets. ● This parameter is set to  Null  when the port needs to transparently |
| Working Mode             | -                                            | This parameter is unavailable for the board.                                                                                          |
| Max Frame Length (bytes) | -                                            | Displays the maximum frame length, which is always 9600 bytes. This parameter is not  configurable.                                   |
| Logical Port Attribute   | -                                            | This parameter is unavailable for the board.                                                                                          |
| Physical Port Attribute  | -                                            | board.                                                                                                                                |
| ARP Aging Time (min.)    | 1 to 1440 Default: 720                       | This parameter is unavailable for the Indicates the ARP aging time of the port.                                                       |

Table 13-9 Flow control

| Field                           | Value                               | Description                                                                                                                                                                                                                              |
|---------------------------------|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Running Status                  | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                             |
| Optical Module Status           | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                             |
| Laser Interface Status          | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                             |
| Laser Transmission Distance     | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                             |
| Traffic  Policing Status        | Enabled, Disabled Default: Disabled | Enables or disables  traffic  monitoring on the port. When you need to monitor the  traffic on a port, enable the  traffic monitoring function to monitor the traffic  on a port in the period  specified by  Traffic  Policing Period . |
| Traffic  Policing Period (min.) | 1 to 30 Default: 15                 | Specifies  the  traffic  monitoring period.                                                                                                                                                                                              |

Table 13-10 Layer 2 attributes

| Field                                  | Value   | Description                                                      |
|----------------------------------------|---------|------------------------------------------------------------------|
| Port                                   | -       | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1). |
| Non- Autonegotiation Flow Control Mode | -       | This parameter is unavailable for the board.                     |
| Auto-Negotiation Flow Control Mode     | -       | This parameter is unavailable for the board.                     |

| Field   | Value   | Description                                                      |
|---------|---------|------------------------------------------------------------------|
| Port    | -       | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1). |

| Field            | Value                                        | Description                                                                                                                                                                                                                                                                                                                                               |
|------------------|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QinQ Type Domain | 0600 to FFFF Default: 81 00                  | Sets the QinQ type domain. This parameter is available only when you set Encapsulation Type in General Attributes to QinQ or 802.1Q.                                                                                                                                                                                                                      |
| Tag              | Tag Aware, Access, Hybrid Default: Tag Aware | Identifies  the type of packets. ● Tag Aware : If the port is set to Tag aware, the port transparently transmits the packets with a VLAN ID (namely, tagged packets) and discards the packets without a VLAN ID (namely, untagged packets). At this time,  Default VLAN ID  and  VLAN Priority  are unavailable. ● Access : If the port is set to Access, |
| Default VLAN ID  | 1 to 4094 Default: 1                         | Specifies  the default VLAN ID of the packets that can be transmitted by the port. ● If  TAG  is set to  Access , the port discards the packets that contain                                                                                                                                                                                              |

Table 13-11 Layer 3 Attributes

| Field         | Value             | Description                                                                                                                                                                                                                                                                   |
|---------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VLAN Priority | 0 to 7 Default: 0 | Specifies  the class of service (CoS) when  TAG  is set to  Access  or  Hybrid . 0  indicates the lowest priority and  7 the highest. When the network is busy, data packets of higher VLAN priority are processed  first  and those of lower VLAN priority may be discarded. |
| SVLANs        | 1-4094            | Specifies  the ID of the S-VLAN. When C-VLANs and S-VLANs are  configured on the same port, this parameter must be set.                                                                                                                                                       |

| Field                          | Value                 | Description                                                                                                                                                              |
|--------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Port                           | -                     | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1).                                                                                                         |
| Enable Tunnel                  | Enabled, Disabled     | After this parameter is set to  Enabled for a port, the port can identify and                                                                                            |
| Max Reserved Bandwidth(kbit/s) | -                     | Specifies  the max reserved bandwidth.                                                                                                                                   |
| Available Bandwidth(kbit/s)    | -                     | Displays the available bandwidth.                                                                                                                                        |
| Specify IP Address             | Manually, Unspecified | When a port carries tunnel services, or when  Port Mode  is set to  Layer 3 , set this parameter to  Manually . For other scenarios, set this parameter to Unspecified . |

| Field            | Value   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IP Address       | -       | Specifies  the port IP address. This parameter is valid only when Specify IP Address  is set to  Manually . NOTE When setting the IP address for a port, ensure that the IP address is in a  different network segment from the IP address of other service ports and the NE IP address, preventing service interruption from occurring or the NE from being unreachable by the NMS. For example, the IP address and subnet mask of an NE are 129.9.0.x and 255.255.0.0, respectively. This means that the NE IP address is in the 129.9 network segment. The IP address and subnet mask of a service-present port on the NE are 10.0.1.1 and 255.255.255.0, respectively. |
| IP Mask          | -       | Specifies  the port subnet mask. This parameter is valid only when                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Next Hop Address | -       | Specify IP Address  is set to  Manually . Indicates the IP address of the next                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

Table 13-12 Advanced attributes

| Field                   | Value                  | Description                                                                                                                                                                                                                                                                                          |
|-------------------------|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPLS Encapsulation Mode | GFP\_ETHERNET, GFP\_MPLS | Specifies  the MPLS encapsulation mode(This parameter can be set only for ODUk virtual ports and VP ports). ● GFP\_ETHERNET: GFP-F encapsulation is performed on the headers.                                                                                                                         |
|                         |                        | MPLS packets with Layer-2 Ethernet ● GFP MPLS: GFP-F encapsulation is not performed on the Layer-2 Ethernet headers of packets. This                                                                                                                                                                 |
|                         |                        | support  traffic classification. In  GFP MPLS  mode, the transmission overhead of packets is reduced and the bandwidth usage is improved. This parameter is available only when the following conditions are met: ● The port IP address is  configured. ● MPLS is enabled. That is,  MPLS TE is set. |
|                         |                        | NOTE The port using  GFP\_ETHERNET  cannot be interconnected with the port using  GFP MPLS .                                                                                                                                                                                                          |

| Field                       | Value                                        | Description              |
|-----------------------------|----------------------------------------------|--------------------------|
| -                           | Displays the port name.                      | Port                     |
| -                           | Displays physical parameters of the port.    | Port Physical Parameters |
| -                           | This parameter is unavailable for the board. | MAC Loopback             |
| -                           | This parameter is unavailable for the board. | PHY Loopback             |
| Default: 00-00-00-00-00-0 0 | Displays the MAC address of the port.        | MAC Address              |

| Field                                           | Value                               | Description                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transmission Rate (kbit/s)                      | -                                   | Displays the rate for transmitting data packets.                                                                                                                                                                                                                                                                                         |
| Receiving Rate (kbit/s)                         | -                                   | Displays the rate for receiving data packets.                                                                                                                                                                                                                                                                                            |
| Loopback Check                                  | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Loopback Port Block                             | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Egress PIR Bandwidth (kbit/s)                   | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Broadcast Packet Suppression                    | Disabled, Enabled Default: Disabled | By using this parameter, you can enable or disable the broadcast packet suppression function for a port. This controls the volume of the incoming broadcast packets on a port. When the broadcast packet suppression function is enabled for a port and the volume of the incoming broadcast packets exceeds the preset threshold on the |
| Broadcast Packet Suppression Threshold (Mbit/s) | Default: 30                         | are discarded. When the broadcast packet suppression function is enabled, if the broadcast packet occupies a bandwidth that exceeds the overall bandwidth of the port x the suppression threshold, the broadcast packet is suppressed.                                                                                                   |
| Network Cable Mode                              | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Optical Module Type                             | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Synchronous Clock Enabled                       | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |
| Mapping Protocol                                | GFP-F, GFP-T Default: GFP-F         | Indicates the Generic Framing Procedure (GFP) used by Ethernet services that traverse virtual ports on universal line boards.                                                                                                                                                                                                            |
| Enable Bit Error Detection                      | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                             |

| Field                                 | Value   | Description                                  |
|---------------------------------------|---------|----------------------------------------------|
| EXC Threshold for Packet Loss at Port | -       | This parameter is unavailable for the board. |
| SD Threshold fort Packet Loss at Port | -       | This parameter is unavailable for the board. |
| Band Type                             | -       | This parameter is unavailable for the board. |
| Wavelength No.                        | -       | This parameter is unavailable for the board. |

## 13.2.10 Adaptation Module

| Optical Modules                                                             | App lica tion s   | Service type   | Type               | Initial Version    |
|-----------------------------------------------------------------------------|-------------------|----------------|--------------------|--------------------|
| SFP+,1560.61nm,9.95Gb/ s-11.1Gb/s,-1dBm, 3dBm,-16dBm,LC,40km                | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R009C0 0SPC700 |
| TSFP+,Extended C Band, 9.95 to 11.3Gbps with CDR,-1dBm, 3dBm,-16dBm,LC,40km | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R009C0 0SPC700 |
| SFP+,1310nm,8.5Gb/ s-11.1Gb/s with CDR,-6.0 to -1.0dBm,-14.4dBm,LC,SM, 10km | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R009C0 0SPC700 |
| SFP+,DWDM,9.95Gb/ s-11.3Gb/s without CDR,-1dBm, 3dBm,-24dBm,LC,80km         | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R009C0 0SPC700 |
| SFP+,1550nm,10Gb/s,-1 to 2dBm,-16dBm,LC,SMF, 40km,with CDR                  | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R009C0 0SPC700 |
| SFP+,1550nm,10G with CDR,0dBm, 4dBm,-24dBm,LC,80km-002                      | Line - Side       | OTU2, OTU2e    | Plugga ble modul e | V100R019C1 0SPC700 |

## NOTE

There is a margin between the input power low alarm threshold and the receiver sensitivity and a margin between the input power high alarm threshold and the overload point. This ensures that the system can report an input power low alarm before the actual input power reaches the receiver sensitivity or an input power high alarm before the actual input power reaches the overload point.

## 13.2.11 Board Specifications

## Mechanical Specifications

| Board   | Item                      | Unit   | Value                |
|---------|---------------------------|--------|----------------------|
| TNZ8NQ2 | Dimensions (H x W x D)    | mm     | 19.80×193.80 ×205.90 |
| TNZ8NQ2 | Dimensions (H x W x D)    | in.    | 0.78×7.64×8.1 1      |
| TNZ8NQ2 | Weight                    | kg     | 1.2                  |
| TNZ8NQ2 | Weight                    | lb.    | 2.65                 |
| TNZ8NQ2 | Typical Power Consumption | W      | 44.2                 |
| TNZ8NQ2 | Maximum Power Consumption | W      | 48.3                 |
