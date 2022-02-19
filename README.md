# blender-colab

<a href="https://github.com/1kaiser/blender-colab/blob/master/blender_render.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This is a Python script that allows you to render Blender 2.9+ scene using Google Colaboratory.
You can upload the blender files using direct upload, Google Drive or URL. Rendered frames can be downloaded directly or through Google Drive.
This script provides basic functionality so you may modify the script to your liking to suit your needs.

## Usage
### Upload type
* `direct`: Upload your blender file in the next cell.
* `google_drive`: The blender file will be downloaded directly from Google Drive. You need to specify the path to the blender/zip file at `drive_path`.
* `url`: Direct link to the blender file in `url_blend`.
* `gdrive_relative`: The Google Drive folder specified at drive_path will be copied directly (as if it's a zipped file).

### Download type
* `direct`: Output files will be automatically downloaded in your browser. (Probably does not work with multiple files?)
* `google_drive`: The output files will be pasted into the specified `drive_output_path` once rendering is finished.
* `gdrive_relative`: The output frames will be automatically rendered into the specified `drive_output_path`.

### A few notes
1. You must own a Google account.
2. One notebook can only run for maximum time of 12 hours (24 hours for Google Colab Pro) but not guaranteed.
3. EEVEE rendering is not supported in a virtual machine.
4. This script is not tested fully yet. Expect some errors.
5. Do note that your access to GPU may be limited or blocked if you render for many hours.
6. This script is intended for those who have no access to high-end GPU for rendering. Please use them responsibly!

## FAQ
### An error occured!
Check which section of the code failed and identify the error (such as misspelled files or path). If you don't understand the error, try re-running the code with the play button at the side. If it still fails, go to `Runtime > Restart and run all` to restart the code or try `Runtime > Factory reset runtime`. If all else fails, open an issue in GitHub with the error log you encountered attached and the details of your setup.

Common errors:
* `MessageError: TypeError: Failed to fetch` while downloading: The tab must be opened so that the frames can be downloaded.

## Disclaimer
Google Colab is specialized for data centres, neural network etc, not rendering 3D scenes. Because the computing power provided are free, the usage limits, idle timeouts and speed of the rendering may varies. [ColabPro](https://colab.research.google.com/signup) is available for those who wanted to have more powerful GPU and longer session for rendering. See the [FAQ](https://research.google.com/colaboratory/faq.html) for more info.
