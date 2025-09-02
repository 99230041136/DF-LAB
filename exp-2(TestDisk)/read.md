#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## Aim :
To use TestDisk step by step to recover a missing partition and repair a corrupted one.



## 🛠️ Installation
Linux (Debian/Ubuntu): sudo apt-get install testdisk

macOS (Homebrew): brew install testdisk

Windows: Download the executable from the official CGSecurity website.

## Procedure

### 1. Create a Log File
- Launch TestDisk from your terminal or command prompt using sudo testdisk (or testdisk_win.exe on Windows).

- Select the [Create] option to generate a log file of the recovery session. This is helpful for future reference or troubleshooting.
<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/7d57a9be-f1ad-4148-9f1c-b8e9d95fc058" />


</p>
<br>
<br>

### 2. Select the Drive to Analyze
- TestDisk will display a list of all detected storage devices.

- Use the Up/Down arrow keys to highlight the drive that contains your lost data.

<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/395788ba-ef4b-44f9-bcd7-3c8e3bff3781" />

</p>
<br>
<br>

- Select [Proceed] to move to the next step.

### 3. Choose the Partition Table Type
- TestDisk will automatically suggest the most likely partition table type (e.g., Intel/PC, EFI GPT).

- The default value is usually correct. Confirm the selection by pressing Enter.
<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/823fc615-c36a-4398-a06e-cc214f9fca9a" />

</p>
<br>
<br>

### 4. Analyze Current Partition Structure
- From the main menu, choose [Analyse] and press Enter.
<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/cdc0b5aa-20a0-4533-8d53-259c72411f69" />

</p>
<br>
<br>

- This will display the current partition table and check for errors or missing partitions.

### 5. Perform a Quick Search
- After the analysis, you will be prompted to perform a [Quick Search].

<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/99a7d92c-f7cf-4246-853d-d91752b7f297" />

</p>
<br>
<br>

- Select it and press Enter to scan the drive for lost partitions.

- Once a partition is found, you can press p to list its files. Deleted files and folders often appear in red.

- Press q to return to the search results.

  ### 6. Perform a Deeper Search
- If the Quick Search fails to find your lost partitions, select [Deeper Search].

-<br>
<br>
<p align="center"> 
<img width="1920" height="1080" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/51be7b3c-63de-4c9d-955d-24ccc5768401" />

</p>
<br>
<br>

- This process can take a long time, as it scans the entire drive, block by block, to find remnants of partition structures.

- Again, use p to preview files and confirm if a found partition is the one you are looking for.

### 7. Modify Partition Status
- After finding the correct partitions, use the Left/Right arrow keys to set their status.

- Use **Left/Right arrow keys** to change status:  
  - **P**: Primary  
  - ***:** Bootable  
  - **L**: Logical  
  - **D**: Deleted

    <br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/0ffcf42a-fec9-4f4a-b656-dd70f700b9ab" />

</p>
<br>
<br>

- Ensure that the partitions you want to recover are marked as Primary or Logical (and not deleted).

### 8. Write the Partition Table
- Once you are confident the partition structure is correct, select [Write] from the menu.

<br>
<br>
<p align="center">
<img width="1920" height="1080" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/17df6cb7-099e-45a9-a43b-1949501305d4" />

<br>
<br>

- Confirm the operation by pressing y (for yes). This will write the new partition table to your disk.

<br>
<br>
<p align="center">
  <img width="1920" height="1080" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/537d1b31-667a-4606-b1d7-357519f1ab7a" />

</p>
<br>
<br>


- WARNING: This is a permanent change. Double-check your selections before writing.

### 9. Recover Files
- If you just need to recover a few files without fixing the partition table, you can do so from the file list (after pressing p).

- Navigate to the folder containing your desired files.

- Use the colon : key to select the files you want to recover.

- Press the uppercase C key to copy the selected file(s).

- Navigate to a safe destination on a different storage device and press uppercase C again to paste.

### 10. Exit and Restart
- Once your task is complete, select [Quit] to exit the program.

- If you wrote a new partition table to the drive, it is recommended to restart your computer to allow the operating system to recognize the changes.
