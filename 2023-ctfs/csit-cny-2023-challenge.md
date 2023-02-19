---
description: Online Capture-the-Flag by Centre for Strategic Infocomm Technologies
---

# CSIT CNY 2023 Challenge

Duration unsure but I cleared it on 27/1/2023.

I found out about this as I was browsing CSIT's LinkedIn page.

They uploaded a video which consisted of a QR code around 4 seconds into the video.

![](<../.gitbook/assets/image (6) (1).png>)

Upon scanning with a QR reader, it brought me to [https://www.csit-events.sg/cny2023-easter-egg-challenge-huat-ah](https://www.csit-events.sg/cny2023-easter-egg-challenge-huat-ah).

<figure><img src="../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p>CSIT CNY 2023 Challenge homepage</p></figcaption></figure>

Information given in the website states that it is related to Alternate Data Stream (ADS).

Unzipping the .7z file in VM produced a text file containing “$2”, however while unzipping I saw that it was taking awhile to unzip as well as it mentioning a ‘hidden’ in the file.

After reading up on ADS, it turns out that it means that the text file itself has hidden data in it.

Using Strings on the .7z file gave me a bunch of encrypted text and we can see the hidden streams as well.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Strings from the .7z file</p></figcaption></figure>

With “==” present, I can deduce that it is base64 encoded. So by using cyber chef, we can get the flag.

<figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption><p>CyberChef of encrypted string</p></figcaption></figure>

Although the flag was found, the challenge requires the flag as well the stream where the flag is found.

I couldn’t find any way to search the ADS in Windows, so I used Linux’s grep to find it.

<figure><img src="../.gitbook/assets/image (21) (1).png" alt=""><figcaption><p>grep function to find flag</p></figcaption></figure>

I used “7z x special\_hong\_bao.zip” command, x is to use extract command. Then grep -r to recursively search for the desired string in the current directory.

Therefore we have the flag CSIT{$888\_hAPpY\_Y3@R\_0f\_r@8b1T} in stream hidden588.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption><p>Completing the challenge</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>Congratulations from CSIT</p></figcaption></figure>



What I learned: ADS can be abused by adversaries to cause damage to the victims, so this challenge helped me understand how to detect and manage it
