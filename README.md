# Android Attack Surface Analyzer

## Motivation & Acknowledgements

This tool was inspired by the `show exposure` command found in Ch0pin's excellent [Medusa Framework (Mango)](https://github.com/Ch0pin/medusa/wiki/Mango). While Medusa/Mango offers a comprehensive suite of tools, the goal here was to create a more lightweight, standalone Python script focused specifically on identifying the initial attack surface (exported components, deeplinks) with minimal setup required beyond standard `apktool` output.

Credits to **Ch0pin** for the inspiration and the valuable work on Medusa.

## Relevance: Deeplinks & IPC on HackerOne

Analyzing exported components and deeplinks remains crucial for Android application security. Based on public HackerOne data (as of Apr 29, 2025, analyzing the last ~4 years):

* **Deeplinks:** Roughly 20% of disclosed Android application bug bounty submissions appear related to deeplink handling.
* **IPC Components:** Approximately 45% (~53 out of ~117 reviewed) of disclosed Android reports seem related to vulnerabilities stemming from exposed IPC components (Activities, Services, Receivers, Providers) or insecure Intent handling triggered via deeplinks or other apps.

*(Source: Approximate statistics derived from searching disclosed Android reports on [HackerOne Hacktivity](https://hackerone.com/hacktivity/overview?queryString=asset_type%3A%28%22Android%3A+Play+Store%22+OR+%22Android%3A+.apk%22%29+AND+disclosed%3Atrue&sortField=latest_disclosable_activity_at&sortDirection=DESC&pageIndex=1))*

## Description

A Python tool for Android application security analysis. Scans `apktool` directories to identify exported components (highlighting unprotected ones), deeplinks (with potential query parameters hinted from Smali), and custom permissions from the `AndroidManifest.xml`. Designed for quick attack surface identification with formatted console output.

## Example Output / Screenshot

*(Placeholder: Add a screenshot or GIF of the tool's output here)*

```ansi
# Example output would appear here...
# (See previous examples for the format)
