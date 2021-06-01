# CLIMP
Command Line Music Player (C++) for Windows.
  
    
    
**Description**  
This project can be used to play, pause and replay mp3 files of constant bitrate from terminal.

Uses mciSendStringA() function of Windows Multimedia API (winmm.dll) to play mp3 files.

It is restricted to 9 songs in 'Show List'. If more mp3s are present in the songs folder it will only take first 9.

Displays error messege for mp3s which could not be played.

Doesn't change song by itself. Have to select 'next' or 'previous' button.

Stores list of songs in a list.txt file in 'songs' folder.

UI is made manually instead of using libraries like ncurces etc. and mp3s are played using Windows Multimedia API instead of SFML,FMOD etc. since it was a college project 🙂.
Works as a proof of concept. Does not have much practical use.

![image](https://user-images.githubusercontent.com/71930390/120257394-d1356400-c2ad-11eb-8a9d-898969487f3e.png)


![df](https://user-images.githubusercontent.com/71930390/120257743-62a4d600-c2ae-11eb-9c20-2653a5dcf6f4.png)


![lst](https://user-images.githubusercontent.com/71930390/120257932-c929f400-c2ae-11eb-8134-b2ba3d8b1d45.jpg)

  
  
**How To Use**  
1. Place constant bitrate mp3 files in the 'songs' folder which is in the same directory as the main.cpp file (up to 9 mp3s are supported).  
   Song filename must follow this convention : (artistname)-(songname)-(duration).mp3 without any whitespace.  
   Example - OzzyOsbourne-Dreamer-4.44.mp3  
   Note - Space should not be used in filenames.
   
2. winmm.dll (dynamic library) must be linked to main.cpp. This could be done in different ways in different IDEs or text editors.  
   For Visual Studio Code Use - ![image](https://user-images.githubusercontent.com/71930390/120261277-35a7f180-c2b5-11eb-91c4-118d5c433c62.png)  
   Note the addition of '-lwinmm' in the above line. 

3. run main.cpp.

  
  
**Working Environment**  
C++ Compiler – MinGW gcc x64 (could work on others, not tested)  
C++ standard 11 or newer (could work on older versions, not tested)  
Operating System – Windows XP(SP1 64 bit) or newer.  
Note - terminal should accept ANSI Escape Sequences for the UI to work. (Example - Windows Powershell)

  
  
**References**  
CodeSpeedy - https://www.codespeedy.com/play-and-pause-an-mp3-file-in-cpp/, https://www.codespeedy.com/play-a-part-of-an-mp3-file-in-cpp/  
CodeProject - https://www.codeproject.com/Articles/14709/Playing-MP3s-using-MCI  
Stackoverflow - https://stackoverflow.com/questions/22253074/how-to-play-or-open-mp3-or-wav-sound-file-in-c-program  
Microsoft - https://docs.microsoft.com/en-us/previous-versions/dd757161(v=vs.85), https://docs.microsoft.com/en-us/windows/win32/multimedia/mci-functions?redirectedfrom=MSDN
