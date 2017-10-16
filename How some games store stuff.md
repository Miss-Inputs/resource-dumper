For my own evil purposes, this is a list of some games, and how they store their data. So you know how to rip them I guess. I just woke up I don't know how to describe things.

## Commmon formats

### MADH
This resource is just a MADH file, which Resource Dumper extracts nicely. You just need to put the data of this resource as the data fork of a new file, change the file type to MADH and the creator to PlayerPRO, and then you can listen to it or convert it.

PlayerPRO is open source and once extracted with Resource Dumper it's just a data fork, so it'd be theoretically possible to make a MADH player on Windows/Linux/etc and you wouldn't need conversion. Nobody's done that though. I think.

### snd resource
I'm not sure of the format, it's not just raw streamed audio as you might think. Brian's Sound Tool can extract them (to WAV/AIFF), but it'll just give you every single sound resource at once. i suppose Resource Dumper would do that too with the way it's currently designed.

--------
## A Day at Work
Unknown. Uses the Cocoa engine (the one that was an engine before Cocoa was an appliction framework. It's okay to be confused, just know that the engine's called Cococa, and there's a DITL resource which credits the "Cocoa Autoplayer Engine" copyright Apple 1998 written by Peter Jensen). CanOpener can't even see anything except a picture of a bird thing on a hoverboard used in that DITL.

## Ares
### Text
The main executable contains the shareware nag dialog in the TEXT/styl resources 900, 901, and 902. 6500 is the credits, which seems to have a few formatting directives in there and doesn't even need to be a styl resource at all.

STR# resource 750 is named "cheats", but they look like garbage. But hey, they could be actual cheat codes, I haven't really played this game.

### Graphics
PICT 900 in the main executable is the Ambrosia logo from the splash screen, and 502 is the title screen.

Ares Sprites logically would contain the sprites, but when you open it up you just get a lot of SMIV resources. The names would suggest these are indeed the sprites, but I don't know the SMIV format yet.

### Music
MADH resources in Ares Sounds (in Ares Data f folder). If you just want to listen to it Ambrosia has mp3s on the game's addons page.

### Sound effects
They're all snd resources inside Ares Sounds.
