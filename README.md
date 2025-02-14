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

## **Example**
