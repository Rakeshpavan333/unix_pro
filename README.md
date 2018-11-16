# Building Labeled datasets using Bash
CZTQmyQJ
This repository contains code for the Project 'Image Scraping using Bash' for the course IT202 - Unix Programming and Practice. 

The primary objective of this project is to implement a tool to easily scrape images from Google Search. This allows the user to easily build huge datasets for various applications. It also supports resizing to specific dimensions.

## Usage

* To use the scrapper to download images, enter the names of the categories in the `query_list.txt` file.

* Then run the shell script as follows:
```bash
bash image_scraper.sh <number_of_images_per_category> <0 to use wget, 1 to use curl> <width> <heigth>
```
The images will be downloaded categor

## Presentation
Presentation for the project can be found [here](http://slides.com/mokshjain/unix)

## Team
* [Rakesh Pavan](https://github.com/MJ10), 16IT221
* [Suyash Ghuge](https://github.com/suyash0103), 16IT114
* [Nishanth Hebbar](https://github.com/nishanthebbar2011), 16IT234
* [Abhishek Kamal](https://github.com/abhishek371), 16IT202

## Contributing 

Follow the [Contributing Guidelines](https://github.com/MJ10/Unix-Project/blob/master/CONTRIBUTING.md)

## License

This repository is licensed under the [MIT License](https://github.com/MJ10/Unix-Project/blob/master/LICENSE.md)

# $1: Number of images to scrape
# $2: Downloader to use (0 for wget and 1 for curl)
# $3: Width of final resized image
# $4: Height of final resized image



if [ $# -ne 4 ];then
  echo "Error: Invalid arguments!"
  echo "Syntax: ./image_scraper.sh <number_of_images> <0 (wget) or 1 (curl)> <output_image_height> <output_image_width>"
  exit 1
fi  
