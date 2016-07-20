# MM2-Voice-Control-Module
Voice Control Module for MichMich's Magic Mirror 2 based on annyang and angular

First of all i am not a programmer. I made this from snippets, tutorials, other gits and some api reading. (and logic)

###What i have done:
Made a stand alone module that can do basic answers, get flickr tags/images, turn my monitor on and off.

###Things that has to be done:**
- [ ] This module is still stand alone. You can install it by CD to the folder and then npm install and npm start.
This needs to be included as MM2 module.

- [ ] The voice controll is done with annyang. If someone could create a possibility to add your own api key to the module so we can avoid the 50 requests a day?

- [ ] Would be cool if we can pull maps on voice control with maps api.


- [ ] Maybe some mic debug.

- [ ] And the most important, fix those messy code (made by a n00b xD)

- [ ] Add some security/failure returns

- [ ] Some creativity!

####Additional notes:
For RPI3 users with a stand alone usb mic:
```
  sudo nano ~/.asoundrc
    pcm.!default {
            type asym
            playback.pcm "plughw:0"
            capture.pcm "plughw:1"
    }
    ctl.!default {
            type hw
            card 0
    }
```
OR
```
  pcm.!default {
            type asym
            playback.pcm "hw:0,0"
            capture.pcm "hw:1,1"
  }
  ctl.!default {
            type hw
            card 0
  }
``` 
- Also add a new file - sudo nano /etc/asound.conf and add the same code.
- then force-reloading alsa.

