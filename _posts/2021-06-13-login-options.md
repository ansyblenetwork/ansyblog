---
title: "Ansyble's login options"
---

Here is an explanation of the login options for Ansyble.

#### Cache nothing personal (default)

By default, Ansyble's persistent storage contains no personal data, except your username. This means that your display name (first and last), password, encryption key, messages, etc. all vanish immediately if for instance, you pull the battery from your device.

This also means that you need to enter your password every time you load or refresh Ansyble. This is necessary to derive your encryption key. Without it, your messages cannot be read in plaintext.

The most annoying property of this login option is perhaps that push notifications also cannot be read in plaintext. However, you will still receive notifications that indicate the arrival of new messages.

#### Cache encryption key only

This is a nice option because you don't need to enter your password every time you load Ansyble.

__Tip:__ In further contrast to the default login option, saving your encryption key allows push notifications to be read in plaintext.


#### Cache everything

This is the most similar to the operation of other common messaging apps. You can read messages offline, provided that they have been previously loaded while connected to the internet.

#### Cache everything, exclusively (Signal protocol)

This is essentially an implementation of the Signal protocol. The main advantages here are: 

1. Messages load quickly, similar to the previous option.
2. Messages enjoy [perfect forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy).

The main disadvantages are:

1. This obviously leaves all of your messages accessible on your device.
2. Your messages will not be accessible from other devices.

__Note:__ Existing chats that were initiated under any other login option will continue to be stored and accessible via the cloud. Only _new_ chats (initiated either by you or your contacts) will enjoy perfect forward secrecy.

#### Simulate how the server sees your data

This simulates what developers and attackers can reconstruct from the data that is stored on Ansyble's servers, ie. without your password.

You will find that the server can see a surprisingly large amount of information about you. However, I claim that no other centralized messaging app can prove to you that they collect anything less. For instance, Signal claims that they collect almost no information about you, but it is impossible for them to prove this. Everything that Ansyble collects, Signal might be secretly collecting as well. (To be clear: I personally trust that they aren't, but the theory of the matter is interesting.)

In other words, Ansyble's privacy claims are both optimal and trustless. If there is a protocol that can prove a piece of data is inaccessible to the server, Ansyble implements it. On the other hand, you may assume Ansyble collects everything it cannot prove to you that it does not collect. (Though, this likely disservices the actuality. For instance, Ansyble does not collect login timestamps or IP addresses at the time of writing.)
