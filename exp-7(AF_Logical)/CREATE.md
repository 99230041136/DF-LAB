# Ex.No.8 — Detect Hidden Data in Images Using StegExpose

## Aim

To detect hidden data in image files using **StegExpose**, a steganography detection and analysis tool.



## Description

**StegExpose** is a Java-based forensic tool used to detect steganography in images.
It analyzes statistical features of image files to identify traces of hidden data and provides a **suspicion score** for each analyzed image.

---

## Requirements

* **Operating System:** Windows or Linux
* **Software Needed:**

  * Java Runtime Environment (JRE)
  * StegExpose tool (JAR file)
  * Sample image files (with and without hidden data)

---

## Steps to Detect Hidden Data Using StegExpose

### 1. Open Command Prompt

* Press `Win + R`, type `cmd`, and hit **Enter**.
* Navigate to the folder where **StegExpose.jar** is stored.

```
cd path\to\StegExpose
```

**Screenshot:**
![Experiment 7](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(1).png)


---

### 2. Run StegExpose

Use the following command to analyze your images:

```
java -jar StegExpose.jar folderpath
```

* Replace `folderpath` with the location of your image files.
* StegExpose will scan all images and display their **suspicion score**.

**Screenshot:**
![Experiment 7 - 2](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(2).png)


---

### 3. View Results

* The output will show the list of analyzed images with corresponding scores.
* A higher score indicates a higher chance of hidden data being present.

**Screenshot:**
![Experiment 7 - 3](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(3).png)

---

### 4. Export Report (Optional)

You can export the results to a `.csv` file for record-keeping:

```
java -jar StegExpose.jar folderpath -a report.csv
```

This generates a file named `report.csv` containing detection results.

**Screenshot:**
![Experiment 7 - 4](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(4).png)

---

## Observations

| Image Name  | Suspicion Score | Hidden Data Detected |
| ----------- | --------------- | -------------------- |
| sample1.jpg | 0.12            | No                   |
| sample2.jpg | 0.86            | Yes                  |
| sample3.jpg | 0.45            | Possible             |

---

## Result

Hidden data in images were successfully detected using **StegExpose**, and the analysis results were recorded for further investigation.
![Experiment 7 - 5](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(5).png)

![Experiment 7 - 6](https://raw.githubusercontent.com/Harini-Kannan1802/image/c02b7c54a412aff3b80fff0066db09ea229f5281/exp%207(6).png)
---

## References

* StegExpose GitHub Repository: [https://github.com/b3dk7/StegExpose](https://github.com/b3dk7/StegExpose)
* Digital Forensics Tools Documentation

