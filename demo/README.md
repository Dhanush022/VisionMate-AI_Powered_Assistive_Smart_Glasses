# VisionMate Demo Video Directory

This directory contains the demonstration video for VisionMate.

## 📁 Recommended File Structure

```text
demo/
├── Visionmate_demo_video.mp4     # Main demo video (required)
├── Visionmate_demo_poster.png    # Thumbnail poster frame (optional)
└── README.md                       # This file
```

## 🎬 Adding Your Demo Video

Place your `Visionmate_demo_video.mp4` file in this directory. For best results:

| Specification | Recommendation |
|--------------|----------------|
| **File name** | `Visionmate_demo_video.mp4` |
| **Format** | MP4 with H.264 codec |
| **Resolution** | 1920x1080 or 1280x720 |
| **Duration** | 30-60 seconds (highlight reel) |
| **Size** | < 100MB for direct repo commit, or use Git LFS |

### Using Git LFS for Large Videos

If your video is > 100MB, enable Git LFS:

```bash
# Install Git LFS
git lfs install

# Track video files in this directory
git lfs track "demo/*.mp4"

# Add .gitattributes to repo
# (ensure .gitattributes is committed with: git lfs track "demo/*.mp4")
```

### Manual Addition (Small Videos ≤ 100MB)

1. Place `Visionmate_demo_video.mp4` in this directory
2. Commit normally (the file will be tracked in git)

## 📖 Usage in Documentation

The main `README.md` references this video in the **Demo** section. The video can be:

- **Opened in any media player** (VLC, mpv, browser)
- **Streamed** via `ffplay demo/Visionmate_demo_video.mp4`
- **Embedded** via poster image: `![Demo](demo/Visionmate_demo_poster.png)`

## 📋 Demo Script (30 seconds)

Use this highlight reel structure:

1. **0:0-0:10**: System boots, camera indicator lights
2. **0:10-0:20**: Object detection - phone/keys detected with labels
3. **0:20-0:30**: Face recognition - "Dhanush recognized"
4. **0:30-0:40**: Object memory - "Remember phone" then "Find phone"
5. **0:40-0:50**: Navigation - "Person ahead, clear path"
6. **0:50-1:00**: Summary - "VisionMate: AI-powered assistive smart glasses"

## 🖼️ Poster Frame (Optional)

Create `Visionmate_demo_poster.png` (300x200px) for a clickable thumbnail in GitHub README:

```markdown
[![Watch Demo](demo/Visionmate_demo_poster.png)](demo/Visionmate_demo_video.mp4)
```

Add this to any Markdown file to display a poster that links to the video.

## 🔧 Technical Notes

- **Supported players**: VLC, mpv, QuickTime, Windows Media Player
- **Command line preview**: `ffmpeg -i demo/Visionmate_demo_video.mp4`
- **Thumbnail extraction**: `ffmpeg -ss 00:00:05 -i demo/Visionmate_demo_video.mp4 -frames:v 1 demo/thumbnail.png`