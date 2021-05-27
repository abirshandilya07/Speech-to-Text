# Speech-to-Text
A simple speech to text program in python which uses speech_recognition
---
To install the speech_recognition library run the following commad in terminal:
```
pip install speech_recognition
```
So we first import the library as sr
```
import speech_recognition as sr

```
then we specify the recognizer..
```
listener = sr.Recognizer()
```
Then we take the microphone as source of the audio and print listening.. denoting that the program is ready and we recognize it using the google API and then we print results.. we put this part in try as there can be an error in opening the microphone in some computers..
```
try:
    with sr.Microphone() as source:
        print('listening...')
        voice = listener.listen(source)
        command = listener.recognize_google(voice)
        print(command)
```
Then we use except for the exception..
```
except:
    pass
```
