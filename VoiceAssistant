import subprocess
import speech_recognition as sr
import webbrowser

# Initialize recognizer class (for recognizing the speech)

r = sr.Recognizer()

# Reading Microphone as source
# listening the speech and store in audio_text variable


with sr.Microphone() as source:
    print("Talk")
    audio_text = r.listen(source)
    print("Time over, thanks")

    # recognize_() method will throw a request error if the API is unreachable, hence using exception handling
    try:
        # using google speech recognition
        print("Text: " + r.recognize_google(audio_text))

    except:
        print("Sorry, I did not get that")
cmd = r.recognize_google(audio_text)

if cmd == "change MAC address":
    subprocess.run(['macchanger', '-r', 'eth0'])

elif cmd == "open Google":
    #subprocess.run(['firefox'])
    webbrowser.open("https://google.com")
# NMAP Command Voice Assistant

elif cmd == "Run network scan":
    print("scanning network")
    subprocess.run(['nmap' ,'wscubetech.com']) #change domain name as per requirement

elif cmd == "network scan on Google":
    print("running scan on google")
    subprocess.run(['nmap', 'google.com'])

elif cmd == "find subdomain":
    print("finding subdomains")
    webbrowser.open("https://subdomainfinder.c99.nl/")
    #subprocess.run(['sublist3r'])
    #find a command to get user input through its voice

elif cmd == "Run Community Edition":
    print("Burp opened")
    subprocess.run(['burpsuite'])

elif cmd == "professional edition":
    print("Redirecting to the file location")
    #subprocess.run(['pwd'])
    subprocess.run(['cd ','/home/kali/Downloads/Burpsuite'])



elif cmd == "scan my local network":
    print("Here are the results for the ARP scan")
    subprocess.run(['arp-scan','-l'])
