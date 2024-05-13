import speech_recognition as sr
import os

#funtion for identifying HINDI language

def hindi():
    recognizer = sr.Recognizer()
    with sr.Microphone() as source:
        print("U have choosen Hindi language\nSpeak in Hindi")
        h = recognizer.listen(source)
        print("W2ait for a while...")
    try:
        print("Recognizing the text u said ")
        text = recognizer.recognize_google(h,language='hi-IN')
        print(f"You said : {text}")
    except sr.UnknownValueError:
        print("Sorry , I didn't get you ")
    except sr.RequestError as e:
        print(f"Couldn't fetch results; {e}")

#funtion for identifying ENGLISH language
        
def english():
    recognizer = sr.Recognizer()
    with sr.Microphone() as source:
        print("U have choosen English language\nSpeak in English")
        h = recognizer.listen(source)
        print("Wait for a while...")
    try:
        print("Recognizing the text u said ")
        text = recognizer.recognize_google(h,language='en-IN')
        print(f"You said : {text}")
    except sr.UnknownValueError:
        print("Sorry , I didn't get you ")
    except sr.RequestError as e:
        print(f"Couldn't fetch results; {e}")

#funtion for identifying TELUGU language

def telugu():
    recognizer = sr.Recognizer()
    with sr.Microphone() as source:
        print("U have choosen Telugu language\nSpeak in telugu")
        h = recognizer.listen(source)
        print("Wait for a while...")
    try:
        print("Recognizing the text u said ")
        text = recognizer.recognize_google(h,language='te-IN')
        print(f"You said : {text}")
    except sr.UnknownValueError:
        print("Sorry , I didn't get you ")
    except sr.RequestError as e:
        print(f"Couldn't fetch results; {e}")

x=0
while(x!=4):
    os.system('cls' if os.name == 'nt' else 'clear')
    print("\n\t\t\t\tWhich language you want to speak in ? ")
    print("\n\n\t\t\t\tPress 1.) for HINDI\n\t\t\t\tPress 2.) for ENGLISH \n\t\t\t\tPress 3.) for TELUGU \n\t\t\t\tPress 4 for Exit")
    x = int(input("\t\t\t\tEnter the number : "))
    if(x == 1):
        hindi()
    elif(x==2):
        english()
    elif(x==3):
        telugu()



