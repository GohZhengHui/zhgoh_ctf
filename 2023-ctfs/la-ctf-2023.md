---
description: Online Capture-the-Flag by ACM Cyber @ ULCA
---

# LA CTF 2023

2/11/2023 12:00:00 PM - 2/13/2023 6:00:00 AM UTC+08:00

Completed 3/46 challenges mainly because I was busy with FYP report.

The first challenge was just joining the discord so technically I only solved 2 challenges.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>misc/CATS!</p></figcaption></figure>

By using [https://linangdata.com/exif-reader/](https://linangdata.com/exif-reader/) with the image, the location will be shown at USA. Then using google maps we can see that it is a place called Lānaʻi Cat Sanctuary. Website of the place is the flag.

![](<../.gitbook/assets/image (11).png>)![](../.gitbook/assets/image.png)



<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>web/college-tour</p></figcaption></figure>

On the website, I inspected the page source to reveal flags 1,2 and 4.

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption><p>Page source</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption><p>index.css</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>script.js</p></figcaption></figure>

Then by going through the index.css and script.js files, I obtained the last 3 flags to form the final flag: lactf{j03\_4nd\_j0S3phIn3\_bRU1n\_sAY\_hi}.



<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption><p>Final result</p></figcaption></figure>



What I learned: managed to use what I learned in my CTI module to solve the first challenge, and the second challenge showed me that so many data can be hidden in a website
