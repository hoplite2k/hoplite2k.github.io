---
layout: page
title: SocketChat App
description:
img: assets/img/socketchat-1.png
importance: 4
category: Academic
---

A Chat Application is where many users or clients connect to have a conversation and share
information. A server is set up which enables clients to connect to each other, the conversation
the clients have should be encrypted to secure critical information. Sockets allow communication
between two different processes on the same or different machines. To be more precise, it's a
way to talk to other computers using standard Unix file descriptors. In Unix, every I/O action is
done by writing or reading a file descriptor. A file descriptor is just an integer associated with an
open file and it can be a network connection, a text file, a terminal, or something else. To a
programmer, a socket looks and behaves much like a low-level file descriptor. This is because
commands such as read() and write() work with sockets in the same way they do with files and
pipes.

Socket.IO provides the ability to implement real-time analytics, binary streaming, instant
messaging, and document collaboration. Notable users include Microsoft Office, Yammer, and
Zendesk. Socket.IO handles the connection transparently. It will automatically upgrade to
WebSocket if possible. This requires the programmer to only have Socket.IO knowledge.
Socket.IO is not a WebSocket library with fallback options to other real time protocols. It is a
custom real time transport protocol implementation on top of other real time protocols. A
Socket.IO implementing server cannot connect to a non-Socket.IO WebSocket client. A
Socket.IO implementing client cannot talk to a non-Socket.IO WebSocket or Long Polling
Comet server. Socket.IO requires using the Socket.IO libraries on both client and server side. As
of version 2.0, Socket.IO makes use of WebSockets as the underlying WebSocket library.

The Advanced Encryption Standard (AES) is a symmetric block cipher chosen by the U.S.
government to protect classified information. AES is implemented in software and hardware
throughout the world to encrypt sensitive data. It is essential for government computer security,
cybersecurity and electronic data protection. The National Institute of Standards and Technology
(NIST) started development of AES in 1997 when it announced the need for an alternative to the
Data Encryption Standard (DES), which was starting to become vulnerable to brute-force
attacks. NIST stated that the newer, advanced encryption algorithm would be unclassified and
must be "capable of protecting sensitive government information well into the [21st] century." It
was intended to be easy to implement in hardware and software, as well as in restricted
environments -- such as a smart card -- and offer decent defenses against various attack
techniques. AES was created for the U.S. government with additional voluntary, free use in
public or private, commercial or noncommercial programs that provide encryption services.
However, nongovernmental organizations choosing to use AES are subject to limitations created
by U.S. export control.

AES includes three block ciphers: AES-128, AES-192 and AES-256. AES-128 uses a 128-bit
key length to encrypt and decrypt a block of messages, while AES-192 uses a 192-bit key length
and AES-256 a 256-bit key length to encrypt and decrypt messages. Each cipher encrypts and
decrypts data in blocks of 128 bits using cryptographic keys of 128, 192 and 256 bits,
respectively. Symmetric, also known as secret key, ciphers use the same key for encrypting and
decrypting, so the sender and the receiver must both know -- and use -- the same secret key. The
government classifies information in three categories: Confidential, Secret or Top Secret. All key
lengths can be used to protect the Confidential and Secret level. Top Secret information requires
either 192- or 256-bit key lengths. There are 10 rounds for 128-bit keys, 12 rounds for 192-bit
keys and 14 rounds for 256-bit keys. A round consists of several processing steps that include
substitution, transposition and mixing of the input plaintext to transform it into the final output of
ciphertext.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/socketchat-1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/socketchat-2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images are taken from the project demo.
</div>

Codebase: <a href="https://github.com/hoplite2k/encrypted-socketchat-application">https://github.com/hoplite2k/encrypted-socketchat-application</a>
