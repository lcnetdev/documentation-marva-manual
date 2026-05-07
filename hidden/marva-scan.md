# Marva Scan Experiment


Testing possible workflows and use cases for scanning resources with mobile phone. Marva Scan connects your phone (or previous scans made with it) to the record you are editing. It uses a visual LLM to extract structured data from images taken with the phone.

⚠️ We don't have LC devices to test with, if using your personal device make sure to be on WiFi to prevent cell data usage. 

## Areas of Testing
- Do the workflows below make sense? Are they based in reality and how people work? What workflows are missing?
- What Data Patterns are missing and should be added?
- How does it work with non-Latin resources? (what changes need to be made to the prompt to better extract data)
- Does it make any mistakes? 
- Other comments / ideas welcome.

## Workflows

1. You have a book in hand and want to get some printed information from the book into Marva. Calling this "Live Mode"
    - s
 

2. You have a stack of books to be worked at some point in the future, you want to pre-scan information to be available later. Calling this "Off-line mode"


## Data Patterns Extracted:

- Title and Subtitle (from title_page scans)
- Statement of responsibility (from title_page scans)
- Publication Provision Activity (from title_page and copyright page scans)
- Primary Contributor and role (from title_page, does not reconcile name to LCCN)
- Other Contributors and their roles (from title_page, does not reconcile name to LCCN)
- Summary (from back_cover scans or summary scans)
- Contents (from toc scans)


## Basics

To access the interface in Marva open `Tools -> Marva Scan`  (If you don't see you need to be given access)


The main section of the Window has 3 areas:
#### QR Code:
![image](../images/image-1778163141043.png)

This section of the window provides you with the QR code to scan with your phone to get your phone to the mobile site to scan. It also connects your phone to this Marva record so anything you scan will be associated with this record via its LCCN (preferred) or ISBN (backup) that are entered in the record.
 

#### Existing Data:
![image](../images/image-1778163467964.png)

This section will check if there are already existing scans made previously based on LCCN or ISBNs

If there is data present it will look like this:

![image](../images/image-1778163688644.png)

The green indicates it found previous scans. In this case it found data scanned and stored by LCCN, and it shows what type of pages were scanned / processed.
![image](../images/image-1778163933858.png)
If there are scans and data processed it will show you components you can review / edit / insert into the record.

### Images Tab
You can access previous scans from this tab, a mangifying glass widget enlarges where you move your mouse cursor.
![image](../images/image-1778164700944.png)

