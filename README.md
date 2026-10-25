# winepear
A simple lightweight Wine and Wineticks compatibility automation script inspired by Windows XP's compatibility behaviour with sysmain.sdb based on bash.

# Installation
TBA

# Building
TBA

# Intended behaviour
Essentially, the goal of this project is to make a basic bash script that stands between the user and wine + winetricks. When the user runs a program (either by launching an exe from their filesystem or desktop environment, or by running winepear <filepath>), Winepear uses information such as the hash, executable filename, and other elements, and matches it to a JSON database downloaded to your PC (compiled with each release and updatable by running winepear update). If a match is found on the JSON database, Winepear will automatically apply any settings required to execute the program to Wine, Winetricks, and any other helpful utilities, with as little user input as possible. If there is no match, it will simply fall back to the user's wine configuration.

The idea for this was initially a result of me discovering how Windows XP handled backwards compatibility for 9X/DOS era programs with the sysmain.sdb database. I essentially want to recreate this seamless experience for Wine, especially since this seems like an extremely quick and simple idea that is long overdue. The end result I envision is the ability to launch ~~every~~ most Windows programs within Wine, and have it run completely fine, with no user input, and no need to add said program to any frontend like Bottles or Steam. Essentially picture what those programs do, but invisible and automated.

# Who this is for
- **New Linux users** who want to run existing software easily and (close to) as seamlessly as on Windows, but without having to tweak with Wine settings or have to do everything through a launcher.
- **People seeking hardcore integration** of Win32 processes on their Linux distro, if that's even something you want.
- **People who need a large JSON of Wine related fixes** since that's the core element of this project.
### Who this is probably not for
- **People who like tweaking with Wine settings** since the default intended behaviour on graphical user interfaces will mostly override Wine if you don't explicitly run your programs in Wine (e.g, in the terminal with the 'Wine' command).
- **Gamers, sort of.** I know that sounds silly but I don't really want to compete with Steam or the many other brilliant gaming related Windows compatibility projects out there. There will be game related fixes, but I want this project to be aimed at desktop programs, so that will take top priority.

# Project roadmap
Quick note: This is my first proper programming related project. Progress will probably initially be slow, and I'm not sure how far I'll get with this, and there will be bugs down the line, despite how theoretically simple this is. I'm hoping all time progresses and this evolves, those issues get ironed out, and I improve my skills at bash scripting.

A more detailed roadmap will come in the future but this is what I have planned:

## Top priority
- Initial creation of sysmain.json database.
- Winetricks verb support
- Simple program identification by sha256 hash and/or program names.
- Windows version changing.
- Ability to request Winetricks to install dependencies - must consider user consent to EULA and proprietary content.

## Future additions
- Automatic Wine and Proton version management

# Why the name?
Because it's a take on "Wine" and "pair", expressing how this script pairs Windows programs to the optimal Wine configuration.

### "The name is ridiculous"
Thanks! That's the whole point.

### "No really. You should change it."
Nah. It's funny to me and I like that.
