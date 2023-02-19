---
description: Online Capture-the-Flag by 0xL4ugh
---

# 0xL4ugh CTF 2023

&#x20;Fri, 17 Feb. 2023, 20:00 SGT — Sat, 18 Feb. 2023, 20:00 SGT



### Forensics

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>ATT IP challenge description</p></figcaption></figure>

Checking Statistics > Protocol Hierarchy and applying the Data as filter brings me to the conversation between 2 IP addresses.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>Protocol Hierarchy</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>Following Data</p></figcaption></figure>

192.168.x.x is a private IP address so the C2 IP can only be 91.243.59.76 with the port 23927.

Hence the flag is 0xL4ugh{91.243.59.76\_23927}.



<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>Wanna 1 challenge description</p></figcaption></figure>

This challenge was quite similar to one of my malware analysis module assignment.

They provided a VMEM file which I used volatility to find the profile.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>imageinfo command</p></figcaption></figure>

Then I used the command in the screenshot to obtain the SHA256.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>SHA256 command</p></figcaption></figure>

Hence the flag is 0xL4ugh{7f7c94e941d39f7b6217e98295c761c90d215eea0fe988327984d8f57bf86205\_Win10x64\_19041}





### OSINT&#x20;

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Cat challenge description</p></figcaption></figure>

The file given is a cat photograph with the watermark of the photographer.

![](<../.gitbook/assets/image (27).png>)

At first, I tried checking the EXIF data of the image but it was already erased.

Then I googled the author + 'cat' to find his flickr account where he keeps a collection of his photos.

Scrolling through his profile allowed me to find the original picture.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>flickr account of author</p></figcaption></figure>

Then the information can be found when I clicked into the picture.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Photo detail</p></figcaption></figure>

Then upon clicking the map, the location can be found on the address bar.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>Answer</p></figcaption></figure>

Hence the flag is 0xL4ugh{29.386886,47.977166}



### Steganography

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption><p>Uraa challenge description</p></figcaption></figure>

For this challenge I had to install steghide and stegseek in Linux.

Stegseek can also be used to extract steghide metadata without a password, which can be used to test whether a file contains steghide data by using the wordlist built into Kali Linux.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption><p>stegseek</p></figcaption></figure>

Having the passphrase allows me to extract the hidden data.

![](<../.gitbook/assets/image (12).png>)![](<../.gitbook/assets/image (10).png>)

And there we have the flag 0xL4ugh{W4RM\_UP\_STE94N0\_G0OD\_J0B}.



This CTF was overall quite fun for me, presenting me a chance to apply what I have learnt in class as well as learning some new skills, unfortunately was quite busy with school to do more.
