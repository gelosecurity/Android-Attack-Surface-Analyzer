# 🔍 Android Attack Surface Analyzer

A Python script to quickly identify potential attack surfaces in Android Applications by scanning the `AndroidManifest.xml` and related Smali code. 

<img width="628" alt="image" src="https://github.com/user-attachments/assets/32dc68d0-83c1-4950-976d-6c0fe4e7d405" />


Inspired by Ch0pin's Medusa/Mango tool: https://github.com/Ch0pin/medusa/wiki/Mango

## Requirements

* Python 3.x
* Directory previously created by `apktool d <app.apk>` (must include `AndroidManifest.xml` and `smali*` folders for all features).

## Usage

```bash
python3 AASA.py /path/to/decompiled_apk_directory



## Relevance (HackerOne Data)

Public vulnerability data highlights why scanning these areas is important:

* **Deeplinks:** ~20% of disclosed Android bug reports on HackerOne (last ~4 years ending Apr 2025) appear related to deeplinks.
* **IPC Components:** ~45% seem related to exposed/insecure IPC components (Activities, Services, etc.) or Intent handling.

*(Source: Approx. stats from [H1 Hacktivity Search](https://hackerone.com/hacktivity/overview?queryString=asset_type%3A%28%22Android%3A+Play+Store%22+OR+%22Android%3A+.apk%22%29+AND+disclosed%3Atrue&sortField=latest_disclosable_activity_at&sortDirection=DESC&pageIndex=1))*
