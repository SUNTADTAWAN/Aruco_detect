# ArUco Marker Detection & Logging

This script detects **ArUco markers** in **MP4 video files**, extracts their **IDs**, and logs the results into:
- **An Excel file (.xlsx)** containing detected marker IDs.
- **A folder** with captured images labeled based on marker position (**UP** or **DOWN**).

## **How It Works**
1. **Automatically detects** all `.mp4` videos in the same folder as the script.
2. **Processes each video**, identifying **ArUco markers** and categorizing them as:
   - **UP**: If the marker appears in the **left half** of the frame.
   - **DOWN**: If the marker appears in the **right half** of the frame.
3. **Saves images** only when the same marker ID is detected **for 3 consecutive frames**.
4. **Records marker IDs in an Excel file**, categorized into two rows:
   - **Row 1**: Markers from the left half (**UP**)
   - **Row 2**: Markers from the right half (**DOWN**)
5. **Each video has its own folder** containing:
   - **An Excel file** (`video_name.xlsx`)
   - **Saved marker images** (`UP_x_ID.png`, `DOWN_x_ID.png`)

---
## **How to Run the Script**
To start detecting ArUco markers, run the following command ( Don't forget to change the path file in code ):

```sh
python New_Aruco_detect.py
```

## **Example**
**Place ArUco markers at two different levels** per frame.
   - Example: **Floor 2 & 3 visible together**, **Floor 4 & 5 visible together**
**To test this project, download sample warehouse videos from Google Drive:**
**[Download Sample Videos](https://drive.google.com/drive/folders/1UDL9ePxvtVyLZpOv65CRXm15x1VUbDG4)**  
**Expected Output from Running the Code**
When you run the ArUco Marker Detection script, the following output will be generated:
Naming Convention for Excel & Image Files (Based on Video Name)

![image](https://github.com/user-attachments/assets/cfeb2b83-f238-4f0c-b4b7-24fa81fd0156)
![image](https://github.com/user-attachments/assets/953cd328-55a0-4261-aec0-624a8e365b4f)

**Example of the Excel File (<video_name>.xlsx) Output**

![image](https://github.com/user-attachments/assets/ff7ccb0b-c1fc-4283-bfd1-aa5a5d8f6fcd)
In the Excel file (<video_name>.xlsx), the rows represent the detected ArUco markers based on their position in the video frame:
Top Row (UP - Upper Level) → Contains markers detected in the upper shelf level captured in the video.
Bottom Row (DOWN - Lower Level) → Contains markers detected in the lower shelf level captured in the video.


**Example Frame with Detected ArUco Markers**
When an ArUco marker is detected in the video, the script captures and saves an image with a structured filename that indicates:

![image](https://github.com/user-attachments/assets/01f39589-498e-4970-a88f-66b21d1f74dd)

Position (UP or DOWN) → Specifies whether the marker is on the upper or lower level.
Marker ID → The unique identifier of the detected ArUco marker.
Detection Order → The sequence in which the marker was detected in the video.


