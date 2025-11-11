
#   Ex.No.3   Wireshark – Network Packet Capture and Analysis Tool


## Procedure: Capturing Plaintext Passwords

### Step 1: Start Capturing Packets
- First, open Wireshark. You will see a list of all available network interfaces (e.g., "Wi-Fi," "Ethernet").


- Select the interface your computer is using to connect to the internet (in this case, Wi-Fi).

  <br>
   <br>
  <p align="center">
  <img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/WS%202.png?raw=true" width="800" alt="WS 2 Screenshot" />


  </p>
  <br>
  <br>

- Click the blue shark fin icon 🦈 in the top-left corner to start the capture. Wireshark will immediately begin capturing all traffic passing through that interface.
 <br>
   <br>
  <p align="center">
  <img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/WS%203.png?raw=true" width="800" alt="WS 3 Screenshot" />


 </p>
  <br>
  <br>

  ### Step 2: Generate Login Traffic
  - Open a web browser and navigate to http://testphp.vulnweb.com/login.php.

- Enter any dummy credentials. For this example, we'll use:

   Username: darling

   Password: measatest143

- Click the login button. The login will fail, but the data has already been sent across the network.

 <br>
   <br>
  <p align="center">
<img width="1580" height="892" alt="Screenshot 2025-09-01 215438" src="https://github.com/Harini-Kannan1802/image/blob/a7a2c4147bf1e364cd50dfa62561301a71830160/WS%206.png" />


 </p>
  
  
### step 3: Stop Capture and Filter Traffic

- Return to Wireshark and click the Stop button (the red square).

- In the display filter bar, you need to find the packet containing the login data. Since the form data was sent to the server, we will look for an HTTP POST request.

- Apply the following filter to find the exact packet and press Enter:

 <br>
   <br>
  <p align="center">
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/WS%205.png?raw=true" width="800" alt="WS 5 Screenshot" />


 </p>
  <br>
  <br>

### step 4: Inspect the Packet to Find Credentials 

- In the filtered packet list, you should see a packet with information like "POST /userinfo.php". Select this packet.

- In the Packet Details pane below the list, expand the following sections:

Hypertext Transfer Protocol

HTML Form URL Encoded

- Inside the "HTML Form URL Encoded" section, you will see the credentials you entered in plaintext.

 <br>
   <br>
  <p align="center">
 <img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/WS%207.png?raw=true" width="800" alt="WS 7 Screenshot" />


 </p>
  <br>
  <br>

---

## Result
The experiment successfully intercepts the login credentials in a human-readable format. The analysis of the captured POST packet reveals the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol. Any sensitive data sent over HTTP is transmitted openly, making it trivial to intercept.
