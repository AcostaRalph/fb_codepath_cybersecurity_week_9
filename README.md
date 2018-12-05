# fb_codepath_cybersecurity_week_9
# Week 9 Project: Honeypots

Total time spent: **10** hours

For this project, we deployed a couple VM's ucing Google Cloud Platform(GCP). The Honeypot framework that was used was [Modern Honey Network](https://threatstream.github.io/mhn/). Two instances were created, one to hold the honeypot and the other to hold the administrative controls. The instances were created with Ubuntu 14.04 Trusty.

Deployed Honeypots
* Dionaea
* Suricata
* p0f

## Issues Encountered
Some issues encountered were during my scanning of the honeypot. There were many more open ports than originally expected, and thus could lead to more attacks from outside sources.

## Summary of Data

The three honeypots were deployed and kept open for a 48-hour period. Honeypot 1 (Dionaea) was kept open for about 45 minutes more. The following statistics were gleaned from the export and the dashboard's data:
* There were over **25,000** total attacks across all 3 honeypots (dionaea: 10939, p0f: 6515, suricata: 7590).
* There seemed to be the most attacks on **port 80**, which makes sense since it is the default port for http.
* The most prevelant payload was **ET POLICY Python-urllib/ Suspicious User Agent**, which leads me to believe that it is a brute force type of attack which generally came from the IP address of **10.128.0.4**. This is because this attack was generally targeted at **port 80** specifically.
* Suricata was the only one which recieved payload attacks that were detected, even though it was second in total number of attacks.

The raw data can be found in the `session.json` file.

## Project Screenshots

<img src="https://github.com/AcostaRalph/fb_codepath_cybersecurity_week_9/blob/master/Sensor_Attacks.png" width="800">

<img src="https://github.com/AcostaRalph/fb_codepath_cybersecurity_week_9/blob/master/Suricata_Payloads.png" width="800">

## Other Notes/Questions

None.