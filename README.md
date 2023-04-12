<h1>IoT based Weight and Volume Measurement for Healthcare​</h1>

<h2>Introduction</h2>
    <p>The following report describes the potential applications of an IoT-based weight and volume measurement device for healthcare. The report discusses the motivation behind the development of such a device, its potential uses, and the benefits it offers over conventional weight and volume measurement methods. Furthermore, the report presents an example layout of the dashboard for monitoring and reporting patient consumption. the weekly update is also shown in the end. </p>

<h2>Motivation</h2>
<p>Conventional weight and volume measurement methods are cumbersome for both patients and caregivers. These methods are prone to errors, time-consuming, and difficult to analyze large amounts of data. The record is usually kept in diaries, and if you lose it, all data is lost. The development of an IoT-based weight and volume measurement device can overcome these challenges and provide an efficient and accurate way to manage patient hydration levels.</p>

<h2>Potential Uses</h2>
<p>The IoT-based weight and volume measurement device has a wide range of potential uses in healthcare, research, and other fields. The primary use of such a device is monitoring and tracking the water intake of patients, particularly those with conditions that require them to maintain a specific hydration level. For example, the device could monitor the water intake of patients with kidney disease, heart failure, or diabetes. This device could also be used in elderly care centers, long-term care facilities, and hospitals to track the water intake of elderly patients and ensure they receive the appropriate amount of hydration. Furthermore, the device has potential applications in research and clinical trials, providing accurate and reliable data on hydration levels that can be used to study the effects of hydration on health outcomes. Moreover, this device can be used in the sports and fitness industry to monitor the water intake of athletes and help them maintain optimal hydration levels during training and competitions.</p>

<h2>Benefits</h2>
<p>The IoT-based weight and volume measurement device offers several benefits over conventional weight and volume measurement methods. By automating the data collection process, our device can reduce the burden on patients and caregivers, minimize human error, and streamline record-keeping. The device also provides real-time data display, patient information, alerts and notifications, historical data, and settings and controls, making it easier for caretakers and medical staff to monitor and manage patient hydration levels.</p>

<h2>Dashboard Layout</h2>
<p>The dashboard layout of the IoT-based weight and volume measurement device should be user-friendly and easy to navigate, with clear and intuitive controls. The dashboard layout should be optimized for the specific needs of the target audience, in this case, caretakers, and medical staff. An example layout of the dashboard includes real-time data display, patient information, alerts and notifications, historical data, and settings and controls. The real-time data display shows weight, volume, and temperature of the water inside the glass in a clear and easy-to-read format, such as a graph or chart. The patient information section displays the patient's name, age, and medical history. The alerts and notifications section displays alerts and notifications related to the patient's water intake. The historical data section displays a graph or chart showing the patient's water intake over time. Finally, the settings and controls section allows caretakers and medical staff to adjust the device's sensitivity, set alarms, or change the units of measurement. The dashboard also has a feature that allows remote monitoring of the device, which could be useful for caretakers that are not physically present with the patient.</p>


<h1>Weekly Updates</h1>

<h3>17/02/23 :</h3>
<ul>
  <li>Collected DEVIO NB-DEVKIT I from Prof. Suramate</li>
</ul>

<h3>23/02/23 :</h3>
<ul>
  <li>Collected required hardware from Prof. Chayakorn</li>
</ul>

<h2> February 02-20, 2023 </h2>
<ul>
  <li>Literature review and finalize all the tools and devices that will be utilized in the proposed system.</li>
  <li>S11 Measurement of NB-IoT Antenna</li>
  <li>Simulation of existing antenna design of the NB-DEVKIT board</li>
</ul>


<h2> February 27, 2023 </h2>
<ul>
  <li>Project proposal presentation this week. You may find it at: 
    <a href="https://kmutnbacth-my.sharepoint.com/:p:/r/personal/s6509106860081_kmutnb_ac_th/Documents/IoT_ProposalV1_annotatedV1%20(1).pptx?d=w3adcc676a5a64be78801dab719e66fe9&csf=1&web=1&e=OUf46D">Proposal Presentation</a></li>
</ul>


<h2> March 03, 2023 </h2>
<ul>
  <li>Testing NB-IoT Connectivity with Magellan</li>
  <ul>
    <li>Sending Packet from Board and Plotting it on Dashboard (Success)</li>
    <li>Sending data using UDPSIM7020E (Fail: Unable to receive data on NodeRed)</li>
    <li>Tested different codes given by AIS to send and receive data via Magellan_SIM7020E at <a href="https://github.com/AIS-DeviceInnovation/Magellan_SIM7020E">https://github.com/AIS-DeviceInnovation/Magellan_SIM7020E</a></li>
  </ul>
</ul>


<h2> March 12, 2023 </h2>
<ul>
  <li>Following Tasks were performed</li>
  <details open>
    <summary>Antenna Development Progress</summary>
    <ul>
      <li>Simulation of Dipole Antenna</li>
      <li>Antenna Miniaturization using Meandering to be started</li>
    </ul>
  </details>
  <details open>
    <summary>Hardware Testing</summary>
    <ul>
      <li>Tested the load cell: attempted calibration</li>                   
      <img src="https://user-images.githubusercontent.com/80390361/224552007-baa1172f-74fd-4875-b554-551f38ac1b64.png" alt="load cell observation">
      <li>Tested I2C LCD</li>
      <img src="https://user-images.githubusercontent.com/80390361/224552322-bc39535c-76ac-4964-9007-f272c49f1699.png" alt="I2C LCD test">
    </ul>
  </details>
</ul>

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
<p>Hardware Integration and Assembly:</p>
<ul>
    <li> The LCD has been successfully integrated with the operational system, enabling it to retrieve weight data from the board and transmit it to the Node Red Server. Additionally, the design for the volume sensor was created using InkSpace, and the corresponding schematic was forwarded for fabrication. </li>
</ul>
<p>Dashboard Design:</p>
<ul>
<li>The Node Red server was established </li>
</ul>
<h2>Date: April 10, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>We tested the Interdigital Capacitor (IDC) based volume sensor using the the Nyanyan/FastCapacitiveSensor: Fast Capacitive Sensor Library (github.com). The code requires a 10M Ohm resistor connected with IDC sensor, but we tested it with a 2MOhm resistor that we had available. Unfortunately, the test showed that the IDC values were not incrementing with the increasing water level. The sensor was sensitive to detecting whether the electrode was dipped in water or not, but the traces of water on the sensor also affected the values, so the sensor needed to be cleaned again to return to the initial value.</li>
  <li>We also tested the OEM HW-038 Water level Sensor, which worked more or less the same as our sensor, only detecting the presence of water but not helping in detecting the level or volume. Further analysis with an oscilloscope and more testing with different values of resistor are needed to proceed further.</li>
  <li>We also tested the HC-SR04 ultrasonic sensor and used it to detect the water level in a glass of water. The sensor is working fine, and calibration needs to be done to be used to detect the volume in a glass of water.</li>
</ul>



 
             
 
                     
