---
layout: page
title: Advanced Keylogger
description:
img: assets/img/keylogger-1.jpeg
importance: 2
category: Fun
---

<b>* Introduction:</b>

Keyloggers collect information and send it back to a third party – whether that is a
criminal, law enforcement or IT department. “Keyloggers are software programs that
leverage algorithms that monitor keyboard strokes through pattern recognition and other
techniques,” explains Tom Bain, vice president security strategy at Morphisec.

The amount of information collected by keylogger software can vary. The most basic
forms may only collect the information typed into a single website or application. More
sophisticated ones may record everything you type no matter the application, including
information you copy and paste. Some variants of keyloggers – especially those targeting
mobile devices – go further and record information such as calls (both call history and the
audio), information from messaging applications, GPS location, screen grabs, and even
microphone and camera capture.

Data captured by keyloggers can be sent back to attackers via email or uploading log data
to predefined websites, databases, or FTP servers. If the keylogger comes bundled within
a large attack, actors might simply remotely log into a machine to download keystroke
data. Today spyware such as keystroke loggers are a common part of the cyber-criminal
toolset to capture financial information such as banking and credit card details, personal
information such as emails and password or names and addresses, or sensitive business
information around processes or intellectual property. They may sell that information or
use it as part of a larger attack depending on what was gathered and their motives.

<b>* Problem Statement:</b>

Develop a keylogger with spyware features using python. The keylogger will contain
features like the basic keylogger (logging keys in python), Incorporated email
functionality, Getting computer information, Gathering the clipboard contents, Collecting
audio using microphone, Taking screenshots, A timer, File encryption.

<b>* Methodology:</b>

Logging Keys: To log keys using python, we will be using the pynput module. Pynput has
multiple functions including on_press, write_file, and on_release.

Email: To add email functionality, we will be using the email module.

Computer information: To gather computer information, we will use socket and platform
modules. The hostname = socket.gethostname() method gets the hostname. To get the
internal IP address, use socket.gethostbyname(hostname) method. To receive processor
information, use the platform.processor() method. To get the system and version
information use platform.system() and platform.version(). To get the machine
information, use the platform.machine() method. To get external (public facing) IP
address, use api.ipify.org. Use the get(‘https://api.ipify.org’).text to get an external ip.

Clipboard: To get the clipboard information, we will be using the win32clipboard module,
which is a submodule of pywin32. The person may not have any writable data for the
clipboard (could have copied an image), so make sure to use a try – except block just in
case information could not be copied.Microphone: To record with a microphone, we will be using the sound device module and
writing to a .wav file using the scipy.io wavefile module. Ensure to set the fs variable: fs
= 44100. Ensure to add a seconds variable: seconds = microphone_time.

Screenshot: To take a screenshot, we will use the ImageGrab from the Pillow Module.
The ImageGrab.grab() method.

Timer: To build a timer which goes through a certain number of iterations before the
keylogger ends, we will be using the timer function.

Files encryption: To encrypt files, we will use the cryptography.fernet module.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/keylogger-1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/keylogger-2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images are taken from the internet.
</div>

Codebase: <a href="https://github.com/hoplite2k/advanced_keylogger">https://github.com/hoplite2k/advanced_keylogger</a>

