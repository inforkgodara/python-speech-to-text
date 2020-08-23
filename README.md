# Python Speech To Text

A few lines of code written in python using libraries (SpeechRecognition, PyAudio) that convert speech to text. 

## Prerequisites

In order to run the python script, your system must have the following programs/packages installed.
* Python 3.6.7
* SpeechRecognition 3.8.1 (Internet required to convert speech to text while execution)
* PyAudio

## Approach
* script.py execute in terminal.
* After a printed start in the terminal, you begin to speak in English and end once your sentence is completed. 
* It will take a few minutes to convert speech to text and print on your terminal.


## Code
```
# Program to convert speech to text
# Author @inforkgodara

import speech_recognition as sr
r = sr.Recognizer()

mic = sr.Microphone()

print('start')
with mic as source:
    audio = r.listen(source)
print('end')
print(r.recognize_google(audio))
```