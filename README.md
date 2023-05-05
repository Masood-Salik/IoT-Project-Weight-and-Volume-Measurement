<h1>IoT based Weight and Volume Measurement for Healthcare​</h1>

<h2>Introduction</h2>
    <p>The following report describes the potential applications of an IoT-based weight and volume measurement device for healthcare. The report discusses the motivation behind the development of such a device, its potential uses, and the benefits it offers over conventional weight and volume measurement methods. Furthermore, the report presents an example layout of the dashboard for monitoring and reporting patient consumption. the weekly update is also shown in the end. </p>

<h2>Motivation</h2>
<p>In today's world, smart devices have become ubiquitous, tracking our health, activities, and surroundings. However, one crucial aspect of our daily routine - water consumption - has largely gone unnoticed. To address this gap, we have developed a Water Weight and Volume Measurement Smart Device that accurately measures the weight and volume of water you consume.</p>

<p>Our device simplifies the tracking of daily water intake, providing real-time updates on hydration levels. By using this innovative product, users can better understand their hydration needs and optimize their water intake to stay healthy.</p>

<p>This technology is particularly useful in the healthcare industry, where conventional weight and volume measurement methods are time-consuming, prone to errors, and difficult to analyze large amounts of data. Our IoT-based device provides an efficient and accurate way to manage patient hydration levels, overcoming the challenges of conventional methods.</p>

<p>With the Water Weight and Volume Measurement Smart Device, users can easily track their water consumption, receive real-time updates on hydration levels, and identify potential health issues related to water intake. This product is the missing link in your smart device collection, ensuring that you stay hydrated, healthy, and on top of your game.</p>


<h2>Potential Uses</h2>
<p>The IoT-based weight and volume measurement device has a wide range of potential uses in healthcare, research, and other fields. The primary use of such a device is monitoring and tracking the water intake of patients, particularly those with conditions that require them to maintain a specific hydration level. For example, the device could monitor the water intake of patients with kidney disease, heart failure, or diabetes. This device could also be used in elderly care centers, long-term care facilities, and hospitals to track the water intake of elderly patients and ensure they receive the appropriate amount of hydration. Furthermore, the device has potential applications in research and clinical trials, providing accurate and reliable data on hydration levels that can be used to study the effects of hydration on health outcomes. Moreover, this device can be used in the sports and fitness industry to monitor the water intake of athletes and help them maintain optimal hydration levels during training and competitions.</p>

<h2>Benefits</h2>
<p>The IoT-based weight and volume measurement device offers several benefits over conventional weight and volume measurement methods. By automating the data collection process, our device can reduce the burden on patients and caregivers, minimize human error, and streamline record-keeping. The device also provides real-time data display, patient information, alerts and notifications, historical data, and settings and controls, making it easier for caretakers and medical staff to monitor and manage patient hydration levels.</p>

<h2>System Block Diagram</h2>
<p> This is how it work.</p>


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

<h2> April 24, 2023</h2>
<p>Embedded Software Design:</p>
<ul>
  <li>Tested the Interdigital Capacitor (IDC) based volume sensor using the LCR Meter and found its intrinsic capacitance to be 26pF. The capacitance value changes from 26pF to 120pF when dipped in water.</li>
  <li>Made another copper tape capacitor. Found its intrinsic capacitance to be 3pF. The capacitance value changes from 3.2pF to 250pF when dipped in water.</li>
  <li>Found that when the Esp32 is programmed using Arduino IDE, the resolution of touch sense value is in the range of 0 to 13, which does not enable measuring the volume. However, when programmed using Esp-IDF, the touch resolution is good, and we are able to detect the change in volume as its value changes from 600 to 740 range.</li>
  <li>Tested the HC-SR04 ultrasonic sensor and used it to detect the water level in a glass of water. The sensor was able to detect the change, but the discrete steps were large to detect small changes in volume.</li>
  <li>Tested the soil sensor to detect the volume, but the change in value is abrupt, and we are not able to detect the volume accurately.</li>
</ul>

<h1>Supplementary Achievements</h1>
<ul>
  <li>Antenna Characterization using Nano VNA:
    <ul>
      <li>Understanding the basics of antenna characterization</li>
      <li>Introduction to Nano VNA and its working principle</li>
      <li>Step-by-step guide for measuring S-parameters using Nano VNA</li>
      <li>Analyzing and interpreting the measurement results</li>
    </ul>
  </li>
  
  <li>Simulation of IoT Antenna in CST Microwave Studio:
    <ul>
      <li>Overview of CST Microwave Studio software</li>
      <li>Creating a 3D model of an IoT antenna in CST Microwave Studio</li>
      <li>Simulation setup and configuration</li>
      <li>Analyzing the simulation results and optimizing the antenna design</li>
    </ul>
  </li>
  
  <li>ESP8266 with NETPIE2020:
    <ul>
      <li>Introduction to ESP8266 and NETPIE2020</li>
      <li>Connecting ESP8266 to NETPIE2020 platform using MQTT</li>
      <li>Implementing simple IoT applications using freeboard on NETPIE2020</li>
    </ul>
  </li>
  <li>AT Command for SIM7020E:
    <ul>
      <li>Overview of SIM7020E module and its features</li>
      <li>Understanding AT commands and their syntax</li>
      <li>Step-by-step guide for sending AT commands to SIM7020E module</li>
      <li>Examples of common AT commands for SIM7020E</li>
    </ul>
  </li>
  <li>ESP-IDF Basics:
    <ul>
      <li>Introduction to ESP-IDF </li>
      <li>Setting up the development environment for ESP-IDF</li>
      <li>Understanding the basic concepts of ESP-IDF programming</li>
      <li>Examples of ESP-IDF projects</li>
    </ul>
  </li>
  <li>TCP Communication using NB-IoT board:
    <ul>
      <li>Overview of TCP communication protocol</li>
      <li>Configuring NB-IoT board for TCP communication</li>
    </ul>
  </li>
  <li>Design, Development, and Testing of Interdigital Capacitor:
    <ul>
      <li>Understanding the concept and working principle of interdigital capacitors</li>
      <li>Designing interdigital capacitors using simulation software</li>
      <li>Fabrication and testing of interdigital capacitors</li>
      <li>Analyzing the test results</li>
    </ul>
  </li>
</ul>


