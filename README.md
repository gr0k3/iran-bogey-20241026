# Iran(?) Bogey
Someone on Reddit suggests an [Israeli F-35 was seen over Daraa, Syria](https://www.reddit.com/r/aviation/comments/1gcaxaj/israeli_f35_seen_over_daraa_syria_26_oct_2024/) on the night of 26 October 2024. Its widely reported the [Israeli military was conducting aistrikes against Iran](https://en.wikipedia.org/wiki/October_2024_Israeli_strikes_on_Iran) on that date, so the claim seems pausible, but is it really an F-35? 

Applying the [Sagan](https://en.wikipedia.org/wiki/Carl_Sagan) standard ([extraordinary claims require extraordinary evidence](https://en.wikipedia.org/wiki/Extraordinary_claims_require_extraordinary_evidence)), lets assume "no" and instead do what the military does and refer to the unidentified aircraft as a a "bogey" for the time being and see if can extract the answer from the video.

<figure>
    <kbd><img src="readme-bogey_010.png"
         alt="Original bogey video downloaded from Reddit"></kbd>
    <figcaption>Original bogey video downloaded <a href="https://www.reddit.com/r/aviation/comments/1gcaxaj/israeli_f35_seen_over_daraa_syria_26_oct_2024/">from Reddit</a>.</figcaption>
</figure>

# Metadata?
A bit of Googling suggested the following exiftool would extract any metadata from the file. None expected, but you never know...

Spoiler: Nothing useful from the source video. 
 
```bash
$ exiftool bogey-orig.mp4
ExifTool Version Number         : 13.00
File Name                       : bogey-orig.mp4
Directory                       : .
File Size                       : 908 kB
File Modification Date/Time     : 2024:10:27 15:52:32+10:00
File Access Date/Time           : 2024:10:27 15:52:32+10:00
File Inode Change Date/Time     : 2024:11:15 15:05:17+10:00
File Permissions                : -rw-r--r--
File Type                       : MP4
File Type Extension             : mp4
MIME Type                       : video/mp4
Major Brand                     : MP4 Base Media v1 [IS0 14496-12:2003]
Minor Version                   : 0.2.0
Compatible Brands               : isom, iso2, avc1, mp41
Movie Header Version            : 0
Create Date                     : 0000:00:00 00:00:00
Modify Date                     : 0000:00:00 00:00:00
Time Scale                      : 1000
Duration                        : 23.45 s
Preferred Rate                  : 1
Preferred Volume                : 100.00%
Preview Time                    : 0 s
Preview Duration                : 0 s
Poster Time                     : 0 s
Selection Time                  : 0 s
Selection Duration              : 0 s
Current Time                    : 0 s
Next Track ID                   : 3
Track Header Version            : 0
Track Create Date               : 0000:00:00 00:00:00
Track Modify Date               : 0000:00:00 00:00:00
Track ID                        : 1
Track Duration                  : 23.30 s
Track Layer                     : 0
Track Volume                    : 0.00%
Image Width                     : 480
Image Height                    : 534
Graphics Mode                   : srcCopy
Op Color                        : 0 0 0
Compressor ID                   : avc1
Source Image Width              : 480
Source Image Height             : 534
X Resolution                    : 72
Y Resolution                    : 72
Compressor Name                 : AVC Coding
Bit Depth                       : 24
Color Profiles                  : nclx
Color Primaries                 : BT.470 System B, G (historical)
Transfer Characteristics        : BT.601
Matrix Coefficients             : BT.601
Video Full Range Flag           : 0
Buffer Size                     : 0
Max Bitrate                     : 173252
Average Bitrate                 : 173252
Video Frame Rate                : 30
Matrix Structure                : 1 0 0 0 1 0 0 0 1
Media Header Version            : 0
Media Create Date               : 0000:00:00 00:00:00
Media Modify Date               : 0000:00:00 00:00:00
Media Time Scale                : 48000
Media Duration                  : 23.45 s
Media Language Code             : eng
Handler Description             : SoundHandler
Balance                         : 0
Audio Format                    : mp4a
Audio Channels                  : 2
Audio Bits Per Sample           : 16
Audio Sample Rate               : 48000
Handler Type                    : Metadata
Handler Vendor ID               : Apple
Encoder                         : Lavf59.27.100
Media Data Size                 : 880898
Media Data Offset               : 27065
Image Size                      : 480x534
Megapixels                      : 0.256
Avg Bitrate                     : 301 kbps
Rotation                        : 0
```

## Frame-by-frame
ffmpeg can turn the MP4 video into a bunch of JPEG images using the following command.

```bash
ffmpeg -i bogey.mp4 -qscale:v 2 bogey_%03d.jpg
```
### Output
<img border="1" src="./ffmpeg-out/bogey_001.jpg" width="15%" alt="bogey_001.jpg"/> <img border="1" src="./ffmpeg-out/bogey_002.jpg" width="15%" alt="bogey_002.jpg"/> <img border="1" src="./ffmpeg-out/bogey_003.jpg" width="15%" alt="bogey_003.jpg"/> <img border="1" src="./ffmpeg-out/bogey_004.jpg" width="15%" alt="bogey_004.jpg"/> <img border="1" src="./ffmpeg-out/bogey_005.jpg" width="15%" alt="bogey_005.jpg"/> <img border="1" src="./ffmpeg-out/bogey_006.jpg" width="15%" alt="bogey_006.jpg"/> <img border="1" src="./ffmpeg-out/bogey_007.jpg" width="15%" alt="bogey_007.jpg"/> <img border="1" src="./ffmpeg-out/bogey_008.jpg" width="15%" alt="bogey_008.jpg"/> <img border="1" src="./ffmpeg-out/bogey_009.jpg" width="15%" alt="bogey_009.jpg"/> <img border="1" src="./ffmpeg-out/bogey_010.jpg" width="15%" alt="bogey_010.jpg"/> <img border="1" src="./ffmpeg-out/bogey_011.jpg" width="15%" alt="bogey_011.jpg"/> <img border="1" src="./ffmpeg-out/bogey_012.jpg" width="15%" alt="bogey_012.jpg"/> <img border="1" src="./ffmpeg-out/bogey_013.jpg" width="15%" alt="bogey_013.jpg"/> <img border="1" src="./ffmpeg-out/bogey_014.jpg" width="15%" alt="bogey_014.jpg"/> <img border="1" src="./ffmpeg-out/bogey_015.jpg" width="15%" alt="bogey_015.jpg"/> <img border="1" src="./ffmpeg-out/bogey_016.jpg" width="15%" alt="bogey_016.jpg"/> <img border="1" src="./ffmpeg-out/bogey_017.jpg" width="15%" alt="bogey_017.jpg"/> <img border="1" src="./ffmpeg-out/bogey_018.jpg" width="15%" alt="bogey_018.jpg"/> <img border="1" src="./ffmpeg-out/bogey_019.jpg" width="15%" alt="bogey_019.jpg"/> <img border="1" src="./ffmpeg-out/bogey_020.jpg" width="15%" alt="bogey_020.jpg"/> <img border="1" src="./ffmpeg-out/bogey_021.jpg" width="15%" alt="bogey_021.jpg"/> <img border="1" src="./ffmpeg-out/bogey_022.jpg" width="15%" alt="bogey_022.jpg"/> <img border="1" src="./ffmpeg-out/bogey_023.jpg" width="15%" alt="bogey_023.jpg"/> <img border="1" src="./ffmpeg-out/bogey_024.jpg" width="15%" alt="bogey_024.jpg"/> <img border="1" src="./ffmpeg-out/bogey_025.jpg" width="15%" alt="bogey_025.jpg"/> <img border="1" src="./ffmpeg-out/bogey_026.jpg" width="15%" alt="bogey_026.jpg"/> <img border="1" src="./ffmpeg-out/bogey_027.jpg" width="15%" alt="bogey_027.jpg"/> <img border="1" src="./ffmpeg-out/bogey_028.jpg" width="15%" alt="bogey_028.jpg"/> <img border="1" src="./ffmpeg-out/bogey_029.jpg" width="15%" alt="bogey_029.jpg"/> <img border="1" src="./ffmpeg-out/bogey_030.jpg" width="15%" alt="bogey_030.jpg"/> <img border="1" src="./ffmpeg-out/bogey_031.jpg" width="15%" alt="bogey_031.jpg"/> <img border="1" src="./ffmpeg-out/bogey_032.jpg" width="15%" alt="bogey_032.jpg"/> <img border="1" src="./ffmpeg-out/bogey_033.jpg" width="15%" alt="bogey_033.jpg"/> <img border="1" src="./ffmpeg-out/bogey_034.jpg" width="15%" alt="bogey_034.jpg"/> <img border="1" src="./ffmpeg-out/bogey_035.jpg" width="15%" alt="bogey_035.jpg"/> <img border="1" src="./ffmpeg-out/bogey_036.jpg" width="15%" alt="bogey_036.jpg"/> <img border="1" src="./ffmpeg-out/bogey_037.jpg" width="15%" alt="bogey_037.jpg"/> <img border="1" src="./ffmpeg-out/bogey_038.jpg" width="15%" alt="bogey_038.jpg"/> <img border="1" src="./ffmpeg-out/bogey_039.jpg" width="15%" alt="bogey_039.jpg"/> <img border="1" src="./ffmpeg-out/bogey_040.jpg" width="15%" alt="bogey_040.jpg"/> <img border="1" src="./ffmpeg-out/bogey_041.jpg" width="15%" alt="bogey_041.jpg"/> <img border="1" src="./ffmpeg-out/bogey_042.jpg" width="15%" alt="bogey_042.jpg"/> <img border="1" src="./ffmpeg-out/bogey_043.jpg" width="15%" alt="bogey_043.jpg"/> <img border="1" src="./ffmpeg-out/bogey_044.jpg" width="15%" alt="bogey_044.jpg"/> <img border="1" src="./ffmpeg-out/bogey_045.jpg" width="15%" alt="bogey_045.jpg"/> <img border="1" src="./ffmpeg-out/bogey_046.jpg" width="15%" alt="bogey_046.jpg"/> <img border="1" src="./ffmpeg-out/bogey_047.jpg" width="15%" alt="bogey_047.jpg"/> <img border="1" src="./ffmpeg-out/bogey_048.jpg" width="15%" alt="bogey_048.jpg"/> <img border="1" src="./ffmpeg-out/bogey_049.jpg" width="15%" alt="bogey_049.jpg"/> <img border="1" src="./ffmpeg-out/bogey_050.jpg" width="15%" alt="bogey_050.jpg"/> <img border="1" src="./ffmpeg-out/bogey_051.jpg" width="15%" alt="bogey_051.jpg"/> <img border="1" src="./ffmpeg-out/bogey_052.jpg" width="15%" alt="bogey_052.jpg"/> <img border="1" src="./ffmpeg-out/bogey_053.jpg" width="15%" alt="bogey_053.jpg"/> <img border="1" src="./ffmpeg-out/bogey_054.jpg" width="15%" alt="bogey_054.jpg"/> <img border="1" src="./ffmpeg-out/bogey_055.jpg" width="15%" alt="bogey_055.jpg"/> <img border="1" src="./ffmpeg-out/bogey_056.jpg" width="15%" alt="bogey_056.jpg"/> <img border="1" src="./ffmpeg-out/bogey_057.jpg" width="15%" alt="bogey_057.jpg"/> <img border="1" src="./ffmpeg-out/bogey_058.jpg" width="15%" alt="bogey_058.jpg"/> <img border="1" src="./ffmpeg-out/bogey_059.jpg" width="15%" alt="bogey_059.jpg"/> <img border="1" src="./ffmpeg-out/bogey_060.jpg" width="15%" alt="bogey_060.jpg"/> <img border="1" src="./ffmpeg-out/bogey_061.jpg" width="15%" alt="bogey_061.jpg"/> <img border="1" src="./ffmpeg-out/bogey_062.jpg" width="15%" alt="bogey_062.jpg"/> <img border="1" src="./ffmpeg-out/bogey_063.jpg" width="15%" alt="bogey_063.jpg"/> <img border="1" src="./ffmpeg-out/bogey_064.jpg" width="15%" alt="bogey_064.jpg"/> <img border="1" src="./ffmpeg-out/bogey_065.jpg" width="15%" alt="bogey_065.jpg"/> <img border="1" src="./ffmpeg-out/bogey_066.jpg" width="15%" alt="bogey_066.jpg"/> <img border="1" src="./ffmpeg-out/bogey_067.jpg" width="15%" alt="bogey_067.jpg"/> <img border="1" src="./ffmpeg-out/bogey_068.jpg" width="15%" alt="bogey_068.jpg"/> <img border="1" src="./ffmpeg-out/bogey_069.jpg" width="15%" alt="bogey_069.jpg"/> <img border="1" src="./ffmpeg-out/bogey_070.jpg" width="15%" alt="bogey_070.jpg"/> <img border="1" src="./ffmpeg-out/bogey_071.jpg" width="15%" alt="bogey_071.jpg"/> <img border="1" src="./ffmpeg-out/bogey_072.jpg" width="15%" alt="bogey_072.jpg"/> <img border="1" src="./ffmpeg-out/bogey_073.jpg" width="15%" alt="bogey_073.jpg"/> <img border="1" src="./ffmpeg-out/bogey_074.jpg" width="15%" alt="bogey_074.jpg"/> <img border="1" src="./ffmpeg-out/bogey_075.jpg" width="15%" alt="bogey_075.jpg"/> <img border="1" src="./ffmpeg-out/bogey_076.jpg" width="15%" alt="bogey_076.jpg"/> <img border="1" src="./ffmpeg-out/bogey_077.jpg" width="15%" alt="bogey_077.jpg"/> <img border="1" src="./ffmpeg-out/bogey_078.jpg" width="15%" alt="bogey_078.jpg"/>
