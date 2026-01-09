# Python Utilities Repository

This repository contains small Python utilities and demos.  
One of the included tools is an Image-to-PNG converter GUI application located in the `ImgToPngConverterApp` folder.

## Overview — ImgToPngConverterApp

A simple Tkinter-based GUI application that converts image files in a source folder to PNG files and saves them to a destination folder. The application supports common image formats (JPEG, BMP, GIF, TIFF, WEBP, etc.) via Pillow and preserves transparency for images with an alpha channel.

Features
- Select a source folder of images.
- Select a destination folder (created automatically if missing).
- Batch-convert supported images to PNG.
- Simple GUI using Tkinter.

## Requirements

- Python 3.8+ (3.10/3.11 recommended)
- Pillow (PIL fork) for image handling
- Tkinter (typically included with standard Python on Windows/macOS; on some Linux distributions you may need to install `python3-tk`)

Install dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install Pillow
# On Debian/Ubuntu if tkinter missing:
# sudo apt-get install python3-tk
```

## Running the App

1. Open a terminal and navigate to the repository root.
2. Find the GUI script inside the `ImgToPngConverterApp` folder. Run it with:

```bash
python path/to/the/script.py
```

(Replace `path/to/the/script.py` with the actual filename — e.g., `ImgToPngConverterApp/img_to_png_converter.py` — if the script has that name.)

When the GUI opens:
- Click "Browse" next to "Select Source Folder" and choose the folder that contains images to convert.
- Click "Browse" next to "Select Destination Folder" and choose (or create) the folder where PNGs should be saved.
- Click "Convert All to PNG" to start batch conversion. A message will show the number of converted images or any error that occurs.

Supported input formats (by file extension):
- .jpg, .jpeg, .bmp, .gif, .webp, .tiff

Behavior notes:
- Images with alpha/transparency are converted to PNG with RGBA preserved.
- Other images are converted to RGB PNG.
- The destination folder is created automatically if it does not exist.

## Example (command-line usage idea)

The repository ships a GUI script, but you can adapt the logic for a command-line workflow like:

```bash
python convert_images_cli.py /path/to/source /path/to/destination
```

(There is no CLI script in the repo by default — adapt the GUI script logic if you need headless batch conversion.)

## Contributing

- Create a new branch for your change:
  - git checkout -b feat/your-feature-name
  - git push -u origin feat/your-feature-name
- Open a Pull Request against `main`.
- Keep changes small and focused; include tests or manual verification steps if appropriate.

Branch name examples:
- feat/add-gif-to-png
- fix/handle-corrupt-images
- docs/update-readme

## Troubleshooting

- If you see "tkinter not found" install platform package for tkinter (e.g., `python3-tk` on Debian/Ubuntu).
- If Pillow fails to open a certain format, ensure system libraries for that format are available on your OS (for example, libwebp for WEBP support on some Linux distros).
- If you encounter permissions errors when creating the destination folder, run the script with appropriate permissions or choose a writable destination.

## License

Specify a license for the repository (e.g., MIT). If you want, I can add a LICENSE file with a specific license text.

## Contact / Author

Repo owner: [vikasprasad7](https://github.com/vikasprasad7)

---

This README was added by GitHub Copilot via API.
