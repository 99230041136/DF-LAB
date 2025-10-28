# 📱 Ex.No.7 — Use AFLogical OSE to Extract Data from an Android Device

## Aim

To perform a logical extraction of user data (contacts, SMS, call logs, calendars, app data where possible) from an Android device using **AFLogical OSE**, and preserve the extracted files for forensic analysis.




## Description

**AFLogical OSE (Open Source Edition)** is a forensic tool used for logical acquisition of Android devices.  
It extracts **user-level artifacts** such as:
- Contacts  
- SMS  
- Call history  
- Calendar entries  
- Browser data  
- Some application data  

This process is **non-destructive** — meaning no permanent changes are made to the phone. It works via **ADB (Android Debug Bridge)** to export data to a forensic workstation for safe analysis.

---

## Requirements

* **Operating System:** Windows or Linux
* **Software Needed:**

- Android device with USB debugging enabled  
- **AFLogical OSE** tool installed on forensic workstation  
- **ADB drivers** installed on system  
- USB cable for connection  
- Proper chain of custody documentation  
---

## Steps to Detect Hidden Data Using StegExpose

1. Connect the Android device to the forensic workstation via USB.  
2. Ensure **USB Debugging** is enabled on the device.  
3. Launch **AFLogical OSE** on the workstation.  
4. Select the device from the detected list.  
5. Choose the data types to extract (Contacts, SMS, Call Logs, etc.).  
6. Start extraction → the tool will pull logical data using ADB.  
7. Save the output `.zip` or `.csv` files to a secure analysis folder.  
8. Compute **hash values (SHA-256)** for the extracted data to ensure integrity.  
9. Document the extraction and store evidence properly.

**Screenshot:**
![Experiment 7](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(1).png)


---

**Screenshot:**
![Experiment 7 - 2](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(2).png)


---

### 3. View Results

* The output will show the list of analyzed images with corresponding scores.
* A higher score indicates a higher chance of hidden data being present.

**Screenshot:**
![Experiment 7 - 3](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(3).png)


**Screenshot:**
![Experiment 7 - 4](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(4).png)

---

## 📊 Output
The extracted data includes:
- `contacts.csv`
- `sms.csv`
- `calllog.csv`
- `browser.csv`
- `calendar.csv`

Each file contains readable text data suitable for forensic review.
---

## Result

AFLogical OSE successfully performed **logical extraction** of Android user data.  
Contacts, messages, call logs, and calendar details were safely pulled to the forensic workstation and verified with SHA-256 hash values.
![Experiment 7 - 5](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(5).png)

![Experiment 7 - 6](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(6).png)
---

## References
- AFLogical OSE GitHub: [https://github.com/nowsecure/aflogical](https://github.com/nowsecure/aflogical)
- Android ADB Documentation: [https://developer.android.com/studio/command-line/adb](https://developer.android.com/studio/command-line/adb)
