✨ eTh3r ✨
---

Ether is a project aiming to implement end to end encryption on open source hardware to avoid as much as possible any malicious third party reading (like it could be done with regular apps on a phone ie.)

Ether is taking advantage of the Tor network to bring anonymity to its users but also can be used on regular networks.

*For now, Ether is still in developpement and there are no active server available to our knowledge, but we plan to host `vapor`, our implementation in go of the Ether protocol both as a web and Tor service*

# The architecture

The idea is to build a custom hardware, thus reducing the attack surface for 3rd parties. The hardware is planned to be built around the `nRF52840`, an affordable 2.4GHz SoC.
It will be discussing with a daemon running on a PC through a purposely archaic interface: ✨ *good old serial* ✨. The messages handed to the PC are already encrypted, thus making it impossible for it to know the content of the message. The PC then sends the encrypted message to an Ether server, either through regular web or through Tor for it to dispatch it correctly.

***The protocol yet doesn't implement any security regarding the recipient.***

There is an alternate layer of communication, based around the 2.4GHz capabilities of the SoC. It aims at a more "*mobile*" usage.


## Legal notice

This project is for educational purpose only and licensed under the MIT License. It is not linked to *Nordic Semiconductors ASA*.
