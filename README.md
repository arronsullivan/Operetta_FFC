# Flat-Field Correction Script

This script applies flat-field correction to fluorescence microscopy images using the provided XML file with flat-field and background information. The script supports images with multiple channels, and it validates the image shape based on the XML data.

This uses the XML file exported when one exports data from Harmony:
Settings Gear -> Data Management -> Export Data -> Method: Measurements - Incl. Associated Files
The XML file shoudl be in an exported folder named FFC_Profile; Example "FFC_Profile_Measurement 2.xml"

This script will not work for multicahnnel images unless you have stacked (and max projected) them first such as with [BIOP's opperetta importer plugin in Fiji](https://github.com/BIOP/ijp-operetta-importer).

Adapatations to use this directly on the Operetta raw files may be something one could edit this script for.

## Requirements

- Python 3.7 or higher
- NumPy
- tifffile
- tkinter (usually comes with Python)

## Usage

1. Make sure you have Python 3.7 or higher installed, along with the required libraries (NumPy, tifffile, and tkinter).

2. Run the script `FFC_v1.py`. The script will prompt you to select the XML file containing the flat-field correction data.

3. Next, you will be prompted to select the input folder containing the microscopy images you want to correct.

4. After that, you will be prompted to select the output folder where the corrected images will be saved. The corrected images will have the same filenames as the original images, but with a "corrected_" prefix.

5. The script will process each image in the input folder and apply the flat-field correction based on the information in the XML file. If an image has an incorrect shape or does not match the expected number of channels, it will be skipped, and a message will be printed to the console.

## Contributing

If you have any suggestions or improvements, feel free to open an issue or create a pull request.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
