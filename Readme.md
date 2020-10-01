## Discord Video Bot

A unique bot which plays YouTube video and stream in Discord.

### How to use

This fetches command from discord channel chat and parse the command and execute the command accordingly.

```py
if command == 'p':
        if len(message.content) == 2:
            await pause_play(message.channel)
        elif len(message.content) < 4 or message.content[2] != ' ':
            return
        else:
            await search_video(message.channel, message.content[3:])
    elif command == 's':
        skip()
        await message.channel.send('Skipped')
    elif command == 'l' and len(message.content) > 3:
        play(message.content[3:])
    else:
        return
```

`,p video_name` plays video
`,s` skips the video and play the next video
`,l video_url` play url in video


