# Voice Assistant Tips for getting setup.
Getting the voice assistant working is pretty easy, if you're running Home Asssitant OS you can just follow their instructions.

If you're running the docker container like I am you'll need 3 more containers setup.
- whisper (or faster-whisper)
- piper
- open wake word

I've added the docker-compose files I use for all of these to a folder in this repo.

Basically just start those docker-compose files up and then add them as wyoming protocol hosts, be sure to give the IP and port number for the docker containers.

then go into the settings for home assistant and click on Voice Assistants.
![image](https://github.com/user-attachments/assets/af5bc0da-1c28-418f-8560-b7f248ef02bf)

then click on home assistant voice at the top
![image](https://github.com/user-attachments/assets/9959a483-eab0-422b-89b0-2163d045f90a)

configure the speech-to-text, text-to-speech, and wake word sections to use the integrations you've added for whisper, piper, and openwakeword respectively

![image](https://github.com/user-attachments/assets/f11a833e-6fa1-4982-a1f2-61c6f47cbd3a)

Next all you need to do is set the home asssistant app as your digital assistant in your phone settings, you can follow the offical instructions for that.

# Wake Word on Android
in order to use the wake word on android you'll need a few apps.
- tasker or automate
- hotword plugin

once you have those you'll need to set up the hotword to use the same wake word as you have set up in home assistant and set the sensitivity.

## set up tasker

you'll need to create a new profile in tasker.
1. tap the + button
2. tap event
3. tap plugin
4. tap hotwordplugin
5. tap the pencil by "configuration"
6. select the hotword you want to use
7. tap the check mark in the top right
8. tap the back arrow at the top left
9. tap new task
10. give it a name like "home assistant" or something you'll recognize
11. tap the check mark by the name you typed
12. tap the + button
13. tap app
14. tap launch app
15. find home assistant and long tap on it until the list of functions appears
16. tap on io.homassistant.companion.android.assist.AssistActivity entry.
17. save the task.

Now you should be able to use your wake word to start the home assistant voice assist, you may need to play with the sensitivity and mic device a bit to get it as reliable as possible.
