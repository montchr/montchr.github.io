---
layout: post
title: philadelphia daily news PDFs
---

I subscribed to the Philadelphia Daily News to get access to their "Digital Replica," which is essentially a PDF of every issue loaded into a clunky ASP/Flash application. Fortunately they provide a download option for PDFs. Unfortunately, they only expose access to the past month of issues. Which seems to defeat the purpose of such an application to me.

By chance, I discovered not only that it's possible to access PDFs not exposed by their application, but it's also possible to access these *without authentication*. Yes, they are publicly available.

I wouldn't have discovered this were it not for me installing the [PDF Viewer extension](https://chrome.google.com/webstore/detail/pdf-viewer/oemmndcbldboiebfnladdacbdfmadadm?hl=en) in Chrome last week, to avoid dealing with Chrome's horrible PDF support. PDF Viewer doesn't automatically download the PDF and open it locally in the browser like Chrome does. Instead, it prepends the URL and opens the file remotely. Like so:

```
chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/http://digital.olivesoftware.com/Olive/ODE/PhiladelphiaDailyNews/DownloadPdf.aspx?dochref=PHDN%2F2014%2F09%2F21&pdf-download-item=document&physical-path=true&contentsrc=pdf-download&Type=Content&For=PdfDownload
```

So I figured, why not remove the appended extension URL to get this:

```
http://digital.olivesoftware.com/Olive/ODE/PhiladelphiaDailyNews/DownloadPdf.aspx?dochref=PHDN%2F2014%2F09%2F21&pdf-download-item=document&physical-path=true&contentsrc=pdf-download&Type=Content&For=PdfDownload
```

I disabled the PDF Viewer extension and opened that URL to download today's PDF directly.

I don't think the archives go very far back – I tried changing the URL to get PDFs from 2013, but I kept getting the stock ASP runtime error message.

![Imgur](http://i.imgur.com/izh6s0u.png)

Doesn't matter to me – I'm only interested in the PDFs from the past month, which DN already provides to its paying customers. ;)

So, for the project I'm working on – the whole reason I've been trying to get the Daily News Digital Replica – I needed an entire month's worth of the print issue or a digital version of it. When I realized how easy it was to get a whole bunch of issues just by changing the date in the URL, I LOLed.

I took the URL into Sublime Text, duplicated it 30 times, then went through each and changed the dates. Then I found the [Bulk URL Opener Extension](https://chrome.google.com/webstore/detail/bulk-url-opener-extension/hgenngnjgfkdggambccohomebieocekm?hl=en) for Chrome, which allows you to take a bunch of URLs separated by new lines, and open them in new tabs. Which, in my case, means downloading all of the files at once. I suppose a dedicated download manager would have been able to handle this too. But the resulting video is quite magical:

<iframe width="420" height="315" src="//www.youtube.com/embed/k01-VRZf6oE" frameborder="0" allowfullscreen></iframe>
