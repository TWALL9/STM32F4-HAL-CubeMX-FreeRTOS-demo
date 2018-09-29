# STM32F4-HAL-FreeRTOS Start-Up Project

This is a quick demo of FreeRTOS running on the STM32F4 Discovery Board.

This project was configured using the STM32CubeMX software package, and as an extension, the HAL middleware libraries.  I made this as a quick example since I hadn't seen any HAL/CubeMX based solutions on GitHub (admittedly it was a quick search).  The reason I chose to use CubeMX and HAL rather than the older (and 'closer to the metal') StdPeriph Library is because these tools are what ST are pushing right now, so if a budding embedded programmer were to try out ST's board, these tools are what they'd be seeing on ST's website.  This project is very similar to what someone would see if they were to follow Atollic/CubeMX's workflow. 

## Build Instructions

I won't be going into extreme detail for setting up Atollic, as there are tons of [really good examples that already exist](https://www.youtube.com/watch?v=CsMUmFLNTok).  I will however detail my setup.

### What You Need
1. PC running Linux (Kubuntu 18.04).  Atollic also works well on Windows (some of my former coworkers have done this)
2. STM32F4Discovery Board, obviously.  I use the one with the F407VGTx, the most common one.
3. Mini-USB cable for communication and debug.
4. Atollic TrueSTUDIO, an Eclipse-based (and free) tool supported by ST that we'll use for building and debug.
5. A FTDI TTY-USB converter is a handy tool, but make sure it can work with 3v3 input, which the Disco uses.  Trying to read the serial output to an Arduino to print to the screen won't work, because I know you're thinking about it ;)

### Setting up Build Environment
1. Download Atollic TrueSTUDIO from [here](https://www.atollic.com/resources/download/)
2. Install it, using recommended settings.  Advanced setup is outside the scope of this project.
3. Download the STM32CubeMX **Eclipse Plugin** not the standalone program.
4. Install it using the instructions [here](http://gotland.atollic.com/resources/applicationnotes/CubeMX_installation_in_TrueSTUDIO.pdf).  It's a bit of a process, but I have faith in you.
5. In Atollic, select File->Import Projects and point it to this directory.  Import it as normal, as the project is already configured for the Disco and Atollic

## Suggestions and Questions

I'm sure that there are better ways to do what I'm doing in this example, and I'd like this demo project to highlight the easy pitfalls of using these tools.  I should know, this started as an excercise in using some new tools, and will likely become a simple template for future projects.  Eventually I'd like for this project to become something that a newcomer to the Discovery Board/ST products in general to use to understand some of the base concepts, in an easily digestable format.  But I'm no expert.  If you're in the mood for enlightening me to some changes/a better way to do things, I'm all ears.