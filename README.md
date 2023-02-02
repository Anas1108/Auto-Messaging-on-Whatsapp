# Auto Messaging on Whatsapp using Selenium

## Introduction
This project aims to automate the process of messaging on Whatsapp. Using Selenium in Python, the script will open Whatsapp Web, search for the desired contact and send the pre-defined message.

## Requirements
1. Python 3
2. Selenium
3. ChromeDriver
4. Jupyter Notebook (optional)

## Setup
1. Install Python 3 on your computer
2. Install Selenium using `pip install selenium`
3. Download ChromeDriver from [ChromeDriver Downloads](https://sites.google.com/a/chromium.org/chromedriver/downloads) and place it in your PATH, e.g. place it in /usr/bin or /usr/local/bin

## Usage
1. Open Jupyter Notebook
2. Create a new Python 3 Notebook
3. Import the required libraries
- import selenium
- from selenium import webdriver
4. Initialize the ChromeDriver
- driver = webdriver.Chrom- e()
5. Open Whatsapp Web
- driver.get("https://web.whatsapp.com/")
6. Scan the QR code to log in to your Whatsapp account
7. Search for the desired contact and click on it
 search_box = driver.find_element_by_xpath('//*[@id="side"]/div[1]/div/label/input')
 search_box.send_keys("Contact Name")
 user = driver.find_element_by_xpath('//span[@title = "{}"]'.format("Contact Name"))
 user.click()
8. Send the pre-defined message

message_box = driver.find_element_by_xpath('//[@id="main"]/footer/div[1]/div[2]/div/div[2]')
message_box.send_keys("Hello! This is an automated message.")
send_button = driver.find_element_by_xpath('//[@id="main"]/footer/div[1]/div[3]/button')
send_button.click()


## Conclusion
This project provides a simple solution for automating messaging on Whatsapp. With a few lines of code, you can send messages to multiple contacts without having to manually type the message every time.

