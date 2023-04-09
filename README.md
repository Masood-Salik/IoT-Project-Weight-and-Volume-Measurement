<h1>IoT based Weight and Volume Measurement for Healthcare​</h1>

This page will show weekly update in description. 

02/02/23 -20/02/23 : Literature review and finalize all the tools and devices that will be utilized in the proposed system.

                     S11 Measurement of NB-IoT Anteena
                     Simulation of existing antenna design of the NB-DEVKIT board 
                     

17/02/23           : Collected DEVIO NB-DEVKIT I from Prof. Suramate

23/02/23           : Collected requried hardware from Prof. Chayakorn

27/02/23           : Project proposal presentation this week. You may find it at: 
[Proposal Presentation](https://kmutnbacth-my.sharepoint.com/:p:/r/personal/s6509106860081_kmutnb_ac_th/Documents/IoT_ProposalV1_annotatedV1%20(1).pptx?d=w3adcc676a5a64be78801dab719e66fe9&csf=1&web=1&e=OUf46D)

06/03/23           : Testing NB-IoT Connectivity with Magellan 
                     
                     Sending Packet from Board and Ploting it on Dashboard (Success)
                     Sending data using UDPSIM7020E (Fail: Unable to recive data on NodeRed)                     
   
                     Tested differnt codes given by AIS to send and recieve data via Magellan_SIM7020E @ https://github.com/AIS-DeviceInnovation/Magellan_SIM7020E
                     
                     
12/03/23           : Following Tasks were performed
                    <details open>
                        <summary>Antenna Development Progress</summary>
                            <ul>
                                <li>Simulation of Dipole Antenna</li>
                                <li>Antenna Miniturization using Meandring to be started</li>
                            </ul>
                    </details>
                    <details open>
                        <summary>Hardware Testing</summary>
                            <ul>
                                <li>Tested the load cell: attempted callibration</li>                   
                                 ![image](https://user-images.githubusercontent.com/80390361/224552007-baa1172f-74fd-4875-b554-551f38ac1b64.png)                      
                                  Observations: Need a platform for accurate callibration for the load cell
                                <li>Tested I2C LCD</li>
                                 ![image](https://user-images.githubusercontent.com/80390361/224552322-bc39535c-76ac-4964-9007-f272c49f1699.png)
                            </ul>
                    </details>
                   

<h2>March 24, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>Last week, I encountered an issue where I was unable to send data to Node-RED. To resolve this issue, I purchased a server with an IPv4 address from the Digital Ocean website. I deployed an Ubuntu droplet on Digital Ocean and am running Node-RED on it. I am now successfully able to receive data on Node-RED at a speed of 1 second. However, I am currently unable to send data from Node-RED to the board.</li>
</ul>
<h2>Date: March 27, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>Last week, I attempted to establish a connection with the Hivemq public broker using MQTT. I used AT commands via serial hardware to subscribe and publish data to the broker. I then used the AIS-provided MQTT code PUBSUB to connect to Node-RED. However, I encountered an issue where the ESP32 kept restarting instead of connecting with the broker. To resolve this issue, I downgraded the ESP32 core to version 1.06. I am now successfully sending and receiving data using MQTT on Node-RED.</li>
</ul>
<h2>Date: April 03, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>Last week, a significant milestone was achieved as we combined the hardware and software. We were able to send the weight by pressing a button. However, after connecting the load sensor, we encountered an issue where the data was not being sent to the server. We debugged the issue and found that the SPI pin used for the load sensor was actually the NB-IoT reset pin. This caused our device to reset when we tried to read weight. We updated the payload message and incorporated the date and time variable in the JSON frame. We were successfully able to get the current time and date via the NB-IoT board. The JSON data received at the payload was parsed, and a simple GUI was made to display the current values.</li>
</ul>
<h2>Date: April 10, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>We tested the Interdigital Capacitor (IDC) based volume sensor using the the Nyanyan/FastCapacitiveSensor: Fast Capacitive Sensor Library (github.com). The code requires a 10M Ohm resistor connected with IDC sensor, but we tested it with a 2MOhm resistor that we had available. Unfortunately, the test showed that the IDC values were not incrementing with the increasing water level. The sensor was sensitive to detecting whether the electrode was dipped in water or not, but the traces of water on the sensor also affected the values, so the sensor needed to be cleaned again to return to the initial value.</li>
  <li>We also tested the OEM HW-038 Water level Sensor, which worked more or less the same as our sensor, only detecting the presence of water but not helping in detecting the level or volume. Further analysis with an oscilloscope and more testing with different values of resistor are needed to proceed further.</li>
  <li>We also tested the HC-SR04 ultrasonic sensor and used it to detect the water level in a glass of water. The sensor is working fine, and calibration needs to be done to be used to detect the volume in a glass of water.</li>
</ul>



 
             
 
                     
