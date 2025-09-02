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

![WhatsApp Image 2025-08-29 at 21 53 56_496e4388](https://github.com/srihari2082005-ctrl/img-1/blob/84fe5d7cd6694fe2314ec49d14a97b812cb32c83/WhatsApp%20Image%202025-09-02%20at%2007.58.48_388a9f70.jpg)

 
<br>
<br>

### 2. Initiate Memory Capture
- In the top menu bar, click **File → Capture Memory...** from the dropdown list.
  <br>
<br>
<img width="1119" height="1004" alt="Screenshot 2025-09-01 153504" src="https://github.com/user-attachments/assets/348fcee4-1727-419f-89a6-cd1842bed969" />

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
<img width="1106" height="1076" alt="Screenshot 2025-09-01 153832" src="https://github.com/user-attachments/assets/830d23cc-5285-4326-8478-fddf871edc54" />


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

<img width="722" height="607" alt="Screenshot 2025-09-01 153924" src="https://github.com/user-attachments/assets/22357840-7ba3-4c0c-b42b-806960cae99d" />

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
<img width="1526" height="991" alt="Screenshot 2025-09-01 154019" src="https://github.com/user-attachments/assets/406a4481-a3bb-4015-8feb-faaa22178f2c" />


<br>

#### Options:

- **Image Type:**  
  - **E01 (EnCase Format):** Recommended; includes compression, metadata, and error-checking.  
  - **Raw (DD):** Bit-for-bit copy with no extra features.
<br>
<br>
<p align="center">
<img width="1500" height="1015" alt="Screenshot 2025-09-01 154146" src="https://github.com/user-attachments/assets/9f1dc93f-77b7-43dd-8cb2-cc3cb932aa0c" />

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
 <img width="1173" height="651" alt="Screenshot 2025-09-02 073147" src="https://github.com/user-attachments/assets/019d7f00-be4a-461c-8901-a56cdd68696e" />


  <img width="1133" height="626" alt="Screenshot 2025-09-02 073200" src="https://github.com/user-attachments/assets/77107c48-fe69-4def-96fe-360471943ec7" />


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
