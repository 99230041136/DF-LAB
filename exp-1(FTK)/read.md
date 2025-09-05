# Ex.No.1    FTK Imager: A Forensic Imaging Tool Overview

## Acquiring Volatile Memory (RAM) Using FTK Imager
<br>


### Steps to Capture RAM Using FTK Imager
<br>

### 1. Run as Administrator
- Open **FTK Imager** with administrative privileges.  
- Right-click the FTK Imager icon and select **Run as administrator**.
<br>
<br>

![hs ftk](https://raw.githubusercontent.com/Harini-Kannan1802/image/c3a3537e80a0c82cedb961c1c559727155c7968a/hs%20ftk.jpg)

 
<br>
<br>

### 2. Initiate Memory Capture
- In the top menu bar, click **File → Capture Memory...** from the dropdown list.
  <br>
<br>
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%202.png?raw=true" width="800" alt="F 2 Screenshot" />



<br>
<br>

### 3. Configure Destination
A dialog box will appear where you configure where and how the memory will be saved.

- **Destination Path:**  
  Click **Browse** to select a folder on an **external drive** (not the system drive).  

- **Destination Filename:**  
  You can keep the default `memdump.mem` or assign a more descriptive name.

- **Optional: Include pagefile.sys**  
  Check this box to capture `pagefile.sys`, which is virtual memory stored on the disk.  
  > Note: This may increase capture size and duration, but can contain valuable artifacts.

- **Optional: Create AD1 file**  
  Saves the memory dump in an AccessData-specific container file.  
  > Generally not necessary if using tools like **Volatility** for analysis.



<br>
<br>

<img width="641" height="496" alt="Screenshot 2025-09-01 153626" src="https://github.com/user-attachments/assets/df499331-ccb1-490d-ad38-492030bca78b" />

<br>
<br>

### 4. Start Capture
- Click the **Capture Memory** button to begin acquisition.
<br>
<br>


<img width="783" height="499" alt="Screenshot 2025-09-01 153712" src="https://github.com/user-attachments/assets/915a3985-7abd-4f94-83d4-7f1e0bf5670f" />

<br>
<br>

### 5. Wait for Completion
- A progress bar will indicate the capture status.  
- Capture time depends on the system’s RAM size.  
- Once finished, the memory dump file will be available in the destination folder.
---
<br>
<br>

## Acquiring Non-Volatile Memory (Disk Image) Using FTK Imager


### 1. Start the Process
- In FTK Imager, go to the top menu bar: **File → Create Disk Image...**.

<br>
<br>
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%202.png?raw=true" width="800" alt="F 2 Screenshot" />


<br>
<br>

### 2. Select Source Evidence Type
A window will appear asking you to choose the source type:

- **Physical Drive:** Images the entire disk, including all partitions, unallocated space, and the Master Boot Record (MBR).  
- **Logical Drive:** Images a specific partition (e.g., C: drive).  
- **Image File:** Converts or copies an existing image file.  
- **Contents of a Folder:** Creates an image of a specific folder only.  

> **Tip:** For full forensic imaging, select **Physical Drive**.
<br>
<br>
<p align="center">

<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%203.png?raw=true" width="800" alt="F 3 Screenshot" />


</p>
<br>
<br>

### 3. Select the Source Drive
- From the dropdown, choose the physical drive to image (connected via **write-blocker**).  
- Click **Finish**.
 <br>
<br>
<p align="center">
<img width="686" height="529" alt="Screenshot 2025-09-01 154002" src="https://github.com/user-attachments/assets/732b1f0f-1f95-4ca0-8916-2c534c7f320a" />

</p>
<br>
<br>

### 4. Configure the Image Destination
- Click **Add...** in the "Create Image" window to define the image **format** and **destination**.
  <br>
<br>
<p align="center">
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%204.png?raw=true" width="800" alt="F 4 Screenshot" />



<br>

#### Options:

- **Image Type:**  
  - **E01 (EnCase Format):** Recommended; includes compression, metadata, and error-checking.  
  - **Raw (DD):** Bit-for-bit copy with no extra features.
<br>
<br>
<p align="center">
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%205.png?raw=true" width="800" alt="F 5 Screenshot" />


</p>
<br>
<br>

- **Fill in Evidence Item Information:**  
  - Enter case details, examiner name, and description.  
  - This information is stored in the image metadata (important for documentation).
 <p align="center">
<img width="1302" height="1025" alt="Screenshot 2025-09-01 154252" src="https://github.com/Harini-Kannan1802/image/blob/a7a2c4147bf1e364cd50dfa62561301a71830160/F%206.png" />

</p>
<br>
<br>

- **Choose Destination Folder:**  
  - Must be a different drive from the source.  
  - Name the image file (e.g., `Case001_SuspectHDD`).  

- **Image Fragment Size:**  
  - Set a value to split the image into multiple parts.  
  - Set to `0` for a single image file.
  <br>
  <br>
  
<p align="center">
<img width="1359" height="1004" alt="Screenshot 2025-09-01 154325" src="https://github.com/Harini-Kannan1802/image/blob/a7a2c4147bf1e364cd50dfa62561301a71830160/F%208.png"/>

</p>
<br>
<br>


### 5. Start the Imaging Process
- Click **Finish** to return to the "Create Image" screen.  
- **Check "Verify images after they are created"** to calculate hash values and ensure integrity.  
- Click **Start**.
  <br>
  <br>
  <p align="center">
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%207.png?raw=true" width="800" alt="F 7 Screenshot" />


<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/F%2010.png?raw=true" width="800" alt="F 10 Screenshot" />

</p>
<br>
<br>

### 6. Completion and Hash Verification
- The imaging process may take time depending on the drive size.  
- After completion, FTK Imager verifies the hashes automatically.  
- A final window shows **MD5** and **SHA1** hashes for both the source drive and image.  
- Matching hashes confirm the forensic image’s integrity.

---
## Notes

- Always use a **write-blocker** to prevent modifications to the evidence.  
- **Hash verification** is critical to maintain a chain of custody and admissibility in court.  
- **Image Fragmentation** is useful for large drives or storage limitations.
---

## References

- [FTK Imager Official Website](https://accessdata.com/product-download/ftk-imager-version-4-5)  
- FTK Imager Documentation
