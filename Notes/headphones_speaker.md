# Use headphones and speaker at the same time

Switching the output device didn't work for me so I thought maybe I can keep both speakers and headphones active at the same time.
I wanted to be able to just pick up headphones and turn off speakers and vice versa when I want to switch.
This worked for a while but now it's broken again.

Open alsamixer: terminal → alsamixer
F6 -> second thing -> Auto-Mute Disabled
Then run.
```bash
sudo alsactl store
```
