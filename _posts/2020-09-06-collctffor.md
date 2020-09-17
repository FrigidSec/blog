---
layout: post
title: "FrigidSec: Forensics Challenge Write-up"
author: Satyam Kanojiya
subtitle: "College Level Team selection Forensics Challenge solution"
date: 2020-09-06 04:23:13 
background: '/img/posts/def.jpg'
---

Hello, pals!

> This is the story of Hannah, Hannah baker may Hannah also know about (.wav) file instead of using tapes...

Get to the point, it is a forensic write-up which starts from here:-}

I got this challenge from one of my college mates a week ago on WhatsApp group, listening through the audio file it’s a cool song with a knowledgeable rap about (.wav) extension. Let’s dive into it.

So it all starts with a huge audio file named `MaroonDareFiveFSec.wav`

Without any guess, I first put this file on the DeepSound app because of its `extension(.wav)`. After extracting I got an MS Word file from this audio file named `Hey.docx`.

![](https://miro.medium.com/max/700/1*6d3mT4FzDkQUmppdfwH7yg.png)

When opening `Hey.docx` it consists of 200 pages(approx.) full of encoding and the intro page looks like this:

![](https://miro.medium.com/max/700/1*eVye7W-3a68qgq60TED0eg.png)

After reading this hint I can proceed further and from the next page, our image starts in the form of encoding. (I apologize for not providing the whole encoding due to its big size). But you can make a guess by viewing this:-

![](https://miro.medium.com/max/700/1*R6_pj86-2IbjZGF0o0RhRQ.png)

So, after reviewing it 2 or 3 times I decided to go with Base64 and head over to `Base64Guru` and got this...

![](https://miro.medium.com/max/700/1*gv8MbglLg4rDtZdDsT_B2A.png)

A zip file as shown in the above screenshot and by extracting got a text file.

![](https://miro.medium.com/max/700/1*aSLKu9ra_hoResUasTx2Ng.png)

Opening this temp.txt file again a lot of encoding ><.

![](https://miro.medium.com/max/700/1*vgC-vlCRfiBuJUcFIFGjIQ.png)


My brain is pinging me where is the image and again I took a shot with Base64Guru. Voilà!
![](https://miro.medium.com/max/700/1*y0a1-VqR5GrTMzg8_12-kg.jpeg)

But sadly this is not the end I forgot that it is not a flag then, I head over to image steg.

> Note-There are many image stenography tools available on the internet but choose wisely for a particular approach/extension file.

Using `steghide` tool (Kali Linux) i got another JPG file named `frigid.jpg` but this time it is corrupted when looking through its magic bytes it didn't match with `JFIF/JPEG/JPG` so by correcting it with help of `hexedit`, now `frigid.jpg` is viewable.

![](https://miro.medium.com/max/700/1*dZavZewk5fSgfIQr7MHigg.png)

After spending 2–3 hrs on this image i didn't get much info because I forgot to pay attention to the real character in the whole steg process. By doing steghide nothing came up.

So, remember our intro page ….????
Image for post

![](https://miro.medium.com/max/700/1*eVye7W-3a68qgq60TED0eg.png)

It said about password then my mind hit me with the idea of using `stegcracker` that is the one i didn't try.

But it requires a word list to operate so head on to `crunch` tool because I had parameters to create wordlist as mentioned above in the screenshot. _Every time brute-force is not the option._ #Time_matters

![](https://miro.medium.com/max/700/1*KK3dDhxwu_-PLpc8OsWnSQ.png)

Using `stegcracker with custom wordlist` i finally got my flag in the form of `frigid.jpg.out`.

Hurrah!

Good job! So here is the flag…

```
F-Sec{1_g3t_h33b13_j33b1es_wh3n_d01ng_f0r3ns1cs_b77b7d86c10c}
```
It was a nice challenge and really enjoyed it!

Stay Hunting 💻

---

> This article is written by [Satyam Kanojiya]() and Taken from [This Medium Post](https://medium.com/@satyam29k/frigidsec-forensics-challenge-aa780adc2fd0) by the author hence do not come under Peer Review Policy. To check the profile of every writer of FrigidSec-Blog please visit [HERE](https://github.com/FrigidSec/blog/tree/master/Writers)
