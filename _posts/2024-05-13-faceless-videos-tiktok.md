---
layout: post
title: "Generating capations for faceless TikTok videos"
date: 2024-05-13 10:53:08 +0700
categories: jekyll update
link: https://github.com/al3rez
link_name: View Github
---

Faceless videos are starting to become popular, so I decided to build a tool
that can write a story or get a story from users, connect it to the
ElevenLabs/TikTok API to generate the voice, do the voiceover on an GTA or
Minecraft video, transcribe the video using AWS, and then render the captions
over it Alex Horomozi style.

<img src="/images/diagram.png" alt="a diagram showing ahow we can make a faceless video" loading="lazy" />

I did a little of research and I realized `ffmpeg` is not such a good idea to burn subtitles/captions on a video, so instead we're going only use it to do the "voiceover" and cutting the video, instead we're going to use HTML 5 canvas to render the captions on top of a video player

So here's what I'm going to do:

1. Generate voice using TikTok API
2. Cut it short to the same length as the audio
3. Do the voiceover
4. Transcribe the video
5. Render the captions

## Generate voice using TikTok API

Thanks to open source, someone already written python code that using your `sessionId` which after you login into TikTok you can simply grab it from your cookies we can generate voice from text with variants and even different langauges such as English, Spanish and more.

[oscie57/tiktok-voice](https://github.com/oscie57/tiktok-voice)

By runnning

```
python main.py -v en_us_001 -f input.txt --session SESSION_ID
```

I went over to [r/confession](https://www.reddit.com/r/confession) and grabbed a engaging silly story about a relationship but you can use ChatGPT or even OpenAI to generate your stories with sample prompts online.

## Cut it short to the same length as the audio

After we have the `voice.mp3` all we have to do is to download the Youtube video which I will be using `youtube-dl` and sweet `ffmpeg` for that.

<a href="https://www.youtube.com/watch?v=VS3D8bgYhf4&t=6s"><img src="/images/thumbnail.jpeg" alt="gta 5 mega ramp faceless video" loading="lazy"></a>

```
youtube-dl -f bestvideo[ext=mp4] https://www.youtube.com/watch?v=VS3D8bgYhf4
```

After you download the video, you can cut it to the same length as the audio using `ffmpeg` manually

```
ffmpeg -i video.mp4 -ss 00:00:00 -to 00:00:10 -c copy cut.mp4
```

But I wrote a script to do that for me

```

```
