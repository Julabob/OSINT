# Open Source Intelligence (OSINT)

In simple words, OSINT is a methodology to gather information without directly interacting with the target. We gather information about the target through other sources and therefore won't be detected by the target. It is used to complement Active Intelligence Gathering which is more effective. 

The following post is about my OSINT journey experience.

## Requirements
* Kali Linux VM

![Image](https://github.com/user-attachments/assets/e8cdca9e-46a8-4507-a286-6e6b26741d19)

The [OSINT Framework](https://osintframework.com/) webpage provides a comprehensive list of all the different tools that can be used for various domains. Although a bit outdated, it provides a starting point to conduct information gathering. Each tool shown can be accessed and used.

I have selected [WhatsMyName(T)](https://whatsmyname.app/) which opens the following website. 

![Image](https://github.com/user-attachments/assets/8b849538-7905-420d-9653-ecea6db058ff)

WhatsMyName is an OSINT tool designed for searching usernames across a wide cast of websites. It helps to quickly find where specific usernames are being used, making it a crucial resource for conducting online investigations.

Taking a few common usernames from [jeanphorn GithHub Username.txt](https://github.com/jeanphorn/wordlist/blob/master/usernames.txt), we get several results.

![Image](https://github.com/user-attachments/assets/fa618e3d-279f-489a-a62a-7d415e0d06f0)

The boxes in green shown in the bottom left represent all usernames associated with accounts. Using a few usernames, the tool able to gather over 700 accounts. Clicking on each account opens a valid account page. The below picture represents one of the accounts identified.

![Image](https://github.com/user-attachments/assets/b1d08056-7848-4263-83d4-b1b2b0b38cd9)

You can also filter by username, show the accounts found, not found and false positives. It also allows to open all the links found by opening each result in a new tab (not recommended). 

Another tool I will be demonstrating is using Spiderfoot. SpiderFoot is an automated OSINT scanner. It comes by default with Kali. SpiderFoot queries and dipslays results from over 1000 open-information sources . SpiderFoot can be run from a console and a GUI. 

Running spiderfoot in our console opens up the following in our terminal.

![Image](https://github.com/user-attachments/assets/3bce9179-cee0-416a-bbee-07ab40709121)

Opening the address in a web browser, we are shown the Scan page of Spiderfoot.

![Image](https://github.com/user-attachments/assets/e3333d06-5d2e-42d0-a14b-379135b536d5)

As this is the first time using Spiderfoot, we have no previous scans. Navigating to the Settings tab shows the list of modules that are supported by Spiderfoot. The padlock symbol beside a module indicates that an API key must be provided in order for the module to work.

Clicking on Archive.org, we see the summary of the module and the category it belongs to. It is also mentioned as slow menaing the module takes time to scan. We can also configure the settings to personalise the scan.

![Image](https://github.com/user-attachments/assets/76ec7988-b94c-467c-9e8a-006270fbf7d6)

Clicking on the New Scan shows us the following page. We need to provide the name of the scan and the target. A help box is provided to aid our target format selection. I am using h4cker.org as my target albeit naming it Scan 1. To make my life easier, I am selecting the Footprint Usecase. We can also scan by module or the particular data we are looking for eg App Store Entry.

![Image](https://github.com/user-attachments/assets/45d3f17d-a1c5-41b5-ba05-f087b258e069)

After clicking on Run Scan Now, it will start to generate results.After stopping the scan, the summary is displayed. 

![Image](https://github.com/user-attachments/assets/9ab22b7f-8627-453f-acb7-6e7b0b6a3129)

We cab see all the different data types that were gathered. Clicking on any one of the columns provides us with more information. I clicked on Internet Name which provides us the following information.

![Image](https://github.com/user-attachments/assets/96d8b050-9f94-4455-a631-b13eebbcdf34)


![Image](https://github.com/user-attachments/assets/98dc373c-edeb-4820-8cad-24b0f10359fd)

![Image](https://github.com/user-attachments/assets/e78c014e-dbeb-485e-8d13-83358eb81b5f)