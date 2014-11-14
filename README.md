## What is in this repo?

`PROCUREMENT` and `RDTE` justifications books (PDFs + attachments) harvested from the USD Comptroller website (http://comptroller.defense.gov/) for the years **2013**, **2014** and **2015**.


The catalog of files that were harvested can be found by looking at the `jbook_list.json` file:


```
example

{
  "PROCUREMENT": {
    "20xx": {
      "AIRFORCE_AMMUNITION": "http://www.saffm.hq.af.mil/shared/media/document/AFD-140310-040.pdf",
      "AIRFORCE_AIRCRAFT_VOL1": "http://www.saffm.hq.af.mil/shared/media/document/AFD-140310-041.pdf",
      "AIRFORCE_AIRCRAFT_VOL2": "http://www.saffm.hq.af.mil/shared/media/document/AFD-140310-042.pdf",
      "AIRFORCE_MISSILE": "http://www.saffm.hq.af.mil/shared/media/document/AFD-140310-044.pdf",
      "AIRFORCE_OTHER": "http://www.saffm.hq.af.mil/shared/media/document/AFD-140310-045.pdf",
      "NAVY_AIRCRAFT_BA1-4": "http://www.finance.hq.navy.mil/fmb/15pres/APN_BA1-4_BOOK.pdf",
      "NAVY_AIRCRAFT_BA5": "http://www.finance.hq.navy.mil/fmb/15pres/APN_BA5_BOOK.pdf",

..etc..

```


## Each PDF file was..

- Downloaded
- Parsed for attachments
- Any attachments that were zip files was unzipped (typically represented as .zzz files)

by the included `fetch_jbook_list.php` script.

```
The script does not properly handle the 2015 PROCUREMENT / P5A_P21Book.PDF (http://www.finance.hq.navy.mil/FMB/15pres/P5A_P21_Book.pdf) and this file was manually downloaded / extracted.  The issue is this file has the same filenames for attachments, and they end up overwriting each other.
```

> **IMPORTNAT NOTE** 
>
You do NOT necessarily need to run this script - as all of the extracted files are included in this repo.  A log of each the extract is also included in `fetch.log`


## Why was this done?

The XML files included in this repo are used by the FedAPI platform, but could also be used by others who want easy access to the data files that are locked in the PDF files.
