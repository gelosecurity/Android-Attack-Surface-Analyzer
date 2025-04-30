# Android-Attack-Surface-Analyzer
This tool performs rapid attack surface analysis on decompiled Android apps. Given an apktool directory, it scans the manifest for exported components, deeplinks, and custom permissions, flagging unprotected IPC endpoints. Includes heuristic Smali scanning for potential deeplink parameters to aid security testing. 
