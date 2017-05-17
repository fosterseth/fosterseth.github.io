---
layout: post
title: "[Tutorial] msys2, sdl2, ffmpeg, and codelite"
---

This is a tutorial for setting up a native Windows GCC environment with the CodeLite IDE.

1. Go to msys2.org and follow the instructions there to install msys2.
(after installing, be sure to run msys2.exe and run pacman -Syu commands, as instructed)

2. Go to codelite.org and download and run the installer.

3. Launch msys2.exe and run the following commands,

4. pacman -S mingw64/mingw-w64-x86_64-gcc

5. pacman -S mingw64/mingw-w64-x86_64-SDL2

6. pacman -S mingw64/mingw-w64-x86_64-ffmpeg

7. pacman -S mingw64/mingw-w64-x86_64-make

8. Add C:\msys64\mingw64\bin to your Windows environment path. Plenty of online guides on how to do this if you get stuck.

9. Launch CodeLite.exe

10. Run the setup wizard to configure the build settings. Scan your computer and it should detect your MinGW compiler.

    ![setup_compilers]({{ site.url }}/assets/setup_compilers.PNG)

11. Your build settings should look like this,

    ![build_settings]({{ site.url }}/assets/build_settings.PNG)

    You will need to manually add mkdir.exe, probably since it's under /usr/ instead of /mingw64/

12. Create a workspace and a new project. Simple console gcc app will do fine.

    ![new_project]({{ site.url }}/assets/new_project.PNG)

13. In workspace panel, right click your new project folder and go to Settings.

14. For SDL2 to work properly, you need to add Include Paths and Preprocessors under the Compiler tab.

    ![compiler_tab]({{ site.url }}/assets/compiler_tab.PNG)

15. For Linker tab,

    ![linker_tab]({{ site.url }}/assets/linker_tab.PNG)

16. Time to test the whole thing. In your project /src/main.c, replace text with the following,

```c
#include <stdio.h>
#include <SDL2/SDL.h>
#include <libavutil/imgutils.h>
#include <libavutil/samplefmt.h>
#include <libavutil/timestamp.h>
#include <libavformat/avformat.h>
#include <libswresample/swresample.h>

int main(int argc, char *argv[]){
    SDL_Init(SDL_INIT_VIDEO);
    SDL_Quit();
    return 0;
}
```
17. Go to Build tab, click Build Project. Hopefully the console doesn't give you compilation errors.

18. Rejoice!
