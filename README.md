# extract-clips

[![Crates.io](https://img.shields.io/crates/v/extract-clips.svg)](https://crates.io/crates/extract-clips)

Extract clips of audio and video from source files according to a
DaVinci Resolve 16 exported EDL file, using ffmpeg.

## Usage

In DaVinci Resolve 16, go to *File* &gt; *Export AAF, XML...* and then, in
the dialog that appears, select *EDL Files (\*.edl)*. Finally, press *Save*.

Run `extract-clips` with the name of the EDL file as argument.

E.g.:

```bash
extract-clips "Timeline 1 (Resolve).edl"
```

## DaVinci Resolve 16 exported EDL file format

EDL files exported by DaVinci Resolve 16 look like so:

```text
TITLE: Timeline 1
FCM: NON-DROP FRAME

001  AX       V     C        00:00:00:00 00:00:01:24 01:00:00:00 01:00:01:24  
* FROM CLIP NAME: IMG_2926.TRIM.mov

002  AX       V     C        00:00:01:24 00:00:02:02 01:00:01:24 01:00:02:02  
* FROM CLIP NAME: IMG_2926.TRIM.mov

003  AX       V     C        00:00:02:02 00:00:02:18 01:00:02:02 01:00:02:18  
* FROM CLIP NAME: IMG_2926.TRIM.mov

004  AX       V     C        00:00:02:18 00:00:02:21 01:00:02:18 01:00:02:21  
* FROM CLIP NAME: IMG_2926.TRIM.mov

005  AX       V     C        00:00:02:21 00:00:02:25 01:00:02:21 01:00:02:25  
* FROM CLIP NAME: IMG_2926.TRIM.mov

006  AX       V     C        00:00:02:25 00:00:04:14 01:00:02:25 01:00:04:14  
* FROM CLIP NAME: IMG_2926.TRIM.mov

007  AX       V     C        00:00:04:14 00:00:04:23 01:00:04:14 01:00:04:23  
* FROM CLIP NAME: IMG_2926.TRIM.mov

008  AX       V     C        00:00:04:23 00:00:04:28 01:00:04:23 01:00:04:28  
* FROM CLIP NAME: IMG_2926.TRIM.mov

009  AX       V     C        00:00:04:28 00:00:05:03 01:00:04:28 01:00:05:03  
* FROM CLIP NAME: IMG_2926.TRIM.mov

010  AX       V     C        00:00:05:03 00:00:06:19 01:00:05:03 01:00:06:19  
* FROM CLIP NAME: IMG_2926.TRIM.mov

011  AX       V     C        00:00:06:19 00:00:07:00 01:00:06:19 01:00:07:00  
* FROM CLIP NAME: IMG_2926.TRIM.mov

012  AX       V     C        00:00:07:00 00:00:09:18 01:00:07:00 01:00:09:18  
* FROM CLIP NAME: IMG_2926.TRIM.mov

013  AX       V     C        00:00:09:18 00:00:09:25 01:00:09:18 01:00:09:25  
* FROM CLIP NAME: IMG_2926.TRIM.mov

014  AX       V     C        00:00:09:25 00:00:09:29 01:00:09:25 01:00:09:29  
* FROM CLIP NAME: IMG_2926.TRIM.mov

015  AX       V     C        00:00:09:29 00:00:11:14 01:00:09:29 01:00:11:14  
* FROM CLIP NAME: IMG_2926.TRIM.mov

```
