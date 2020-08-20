# contest-for-iiec

#Code for requirements


import os
import pyttsx3
import pywhatkit as kit

pyttsx3.speak("Welcome")

while True:
	pyttsx3.speak("Select your choice")
	print("Select your choice :")

	p=input()


	if(("run" in p) or ("open" in p) or ("launch" in p)) and ("notepad" in p):
		pyttsx3.speak("opening notepad")
		os.system("notepad")
	elif(("run" in p) or ("open" in p) or ("launch" in p)) and (("cmd" in p) or ("terminal" in p)):
		pyttsx3.speak("opening command prompt")
		os.system("start cmd")
	elif(("run" in p) or ("open" in p) or ("launch" in p)) and ("chrome" in p):
		pyttsx3.speak("opening chrome")
		os.system("start chrome")
	elif(("run" in p) or ("open" in p) or ("launch" in p)) and (("media" in p) or ("player" in p)):
		pyttsx3.speak("opening media player")
		os.system("start wmplayer")
	elif(("run" in p) or ("open" in p) or ("launch" in p)) and ("vlc" in p):
		pyttsx3.speak("opening vlc")
		os.system("start vlc")
	elif(("run" in p) or ("open" in p) or ("launch" in p)) and ("youtube video" in p):
		pyttsx3.speak("can you name the title of the video")
		print("can you name the title of the video:",end ='')
		q=input()
		pyttsx3.speak("Here's the video")
		kit.playonyt(q)
	elif(("send" in p)or("text" in p) and ("whatsapp" in p)):
		pyttsx3.speak("can you write the mobile number")
		print("can you write the mobile number(with country code):", end='')
		y=input()
		pyttsx3.speak("can you write the message")
		print("can you write the message:", end='')
		t=input()
		pyttsx3.speak("can you write the time")
		print("can you write the time hrs:", end='')
		u=input()
		pyttsx3.speak("can you write the time")
		print("can you write the time min:", end='')
		v=input()
		kit.sendwhatmsg(y,t,u,v)
	elif(("quit" in p)or("close" in p)or ("exit" in p)):
		pyttsx3.speak("Thank you for spending some wonderful time here!")
		break
	else:
		pyttsx3.speak("Your requirement doesnt exist")
		printf("doesnt exist...!Try again")


