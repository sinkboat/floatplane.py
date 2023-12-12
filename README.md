# floatplane.py
A simple python library for the Floatplane API, with inspiration from the discord.py syntax. Originally made for the server side part of the Sinkboat App, now available for anyone to use.

# Getting Started
> :warning: **floatplane.py is a W.I.P (Work In Progress) library**, most methods won't work and may change in the future, so its not recommended for production yet. Please feel free to create a Issue or PR, we won't bite!

Before you do anything, lets install the library. You can use these commands to install it via pip.
```bash
pip install git+github.com/sinkboat/floatplane.py
```

## Example

```python
from floatplane import FloatplaneClient, EVENTS

client = FloatplaneClient(username="john.doe@example.com", password="Password123", 2facode="12345")

@client.event(EVENTS.ON_NEW_VIDEO)
def on_new_video(video):
  if not video.isVOD:
    print(f"New Video: {video.title} by {video.author}")
  else:
    print(f"New VOD: {video.title} by {video.author}")

```

