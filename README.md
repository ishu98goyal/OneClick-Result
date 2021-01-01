# OneClick-Result
This code was made to get the CGPA score of complete CSE department of a particular year using Selenium and Beautiful Soup.




## Table of contents
* [General info](#general-info)
* [Demo](#demo)
* [Technologies and Tools](#technologies-and-tools)
* [Code Examples](#code-examples)
* [Features](#features)
* [Status](#status)

## General info



## Demo
![Example screenshot](images/Demo.gif)




## Technologies and Tools
* Python 
* Pandas
* Selenium


 

## Code Examples

````
from selenium import webdriver
import pandas as pd

# Selenium automation using chrome
driver=webdriver.Chrome(executable_path='C:/Users/ishu/Desktop/chromedriver')
driver.get('https://erpsrm.com/srmhonline/online/results/onlineResult.jsp')

#Working 
from bs4 import BeautifulSoup

for i,j,k in zip(df['Roll'],df['DOB'],df['Name']):
    username=driver.find_element_by_name('txtRegisterno')
    username.send_keys(i)
    password=driver.find_element_by_name('txtDob')
    
    str1=''
    for x in j:
        if(x=='-'):
            str1=str1+'/'
        else:    
            str1=str1+x

    password.send_keys(str1)
    submit=driver.find_element_by_xpath('//*[@class="submitButton"]')
    driver.execute_script("arguments[0].click();", submit)
    driver.implicitly_wait(15)
    table=driver.find_elements_by_xpath('//table[@id="table2"]/tbody/tr/td')
    if (driver.find_elements_by_xpath('//table[@id="table2"]/tbody/tr/td')):
        print(k,table[1].text)
        driver.refresh()
    else:
        driver.refresh()

````

## Features


## Status
Project is: _finished_. 


<a href="https://www.linkedin.com/in/ishug/" target="_blank">LinkedIn</a>, or 
My other projects can be found [here](link).



