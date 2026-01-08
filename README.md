# Event Segment Annotator 🎬

A lightweight, web-based tool designed for manual event segmentation of movies and videos. This tool allows researchers to annotate narrative boundaries with precision, supporting both local video files and Vimeo embeds.

## ✨ Features

* **Workflow**: Support for both **Local Video Files** (`.mp4`) and **Web Embeds** (e.g., Vimeo).

* **Config**: Import movie lists via Excel (`.xlsx`) or CSV to auto-load metadata (names, crop limits, links).

* **Limits**: Automatically handles "Crop Start" and "Crop End" limits (e.g., removing opening logos or credits).

* **Cutting**: Visual indicators for event length (Target: **30s - 50s**).

  * 🟢 **Green**: Optimal (30-50s)

  * 🟡 **Yellow**: Too short (<30s)

  * 🔴 **Red**: Too long (>50s)

* **Keyboard Shortcuts**:

  * `Space`: Play / Pause (or Split if playing)

  * `Click`: Mark Segment

* **Export**: Generates structured JSON data with precise timestamps.

## 🚀 How to Use

### 1. Quick Start (No Config)

1. Select **"➕ Quick Start / Add New"** from the dropdown.

2. Enter a movie name.

3. Either **Upload a Local File** or **Paste an Embed Link**.

4. Press `Space` to start playing and annotating!

### 2. Using a Configuration File (Recommended)

1. Create an Excel or CSV file with the following headers to manage your dataset:

| Column Name | Description | Example |
| :--- | :--- | :--- |
| `name` | Movie title | `Big Buck Bunny` |
| `lower_lim` | Start time (skips intro) | `0:00:30` |
| `upper_lim` | End time (skips outro) | `0:10:00` |
| `link` | Direct URL | `http://.../movie.mp4` |
| `embed` | Embed URL  | `https://vimeo.com/...` |

2. Click **"1. Import Config"** and select your file.

3. Select a movie from the dropdown list.

4. If the source link is missing, upload the local file when prompted.

## ⌨️ Controls

* **Spacebar**: Play/Pause. If the video is already playing, pressing Space again (or the Split button) will **mark a segment boundary**.

* **Undo/Delete**: Click the trash icon 🗑️ next to a segment to delete it. The player will automatically **jump back** to the start of that segment for easy re-recording.
