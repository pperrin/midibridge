# midibridge

A python script which listens for incoming WiFi MIDI messages and passes them to a virutal port where they can be be further proccessed by (say) mididings.

The IP addresses and ports are currently hardcoded - change them to suit your own setup!

## Incomming Formats
There are many 'standards' for MIDI over WiFi, this script listens for:-

### DSMidi
    * http://dsmi.tobw.net
    * https://code.google.com/p/dsmi/
### Websockets
    * WS:\<addr\>:\<port\>
###OSC - open sound control
    OSC can transmit MIDI messages, but tends to be used to transmit user defined text message. I am planning on using messages in the format /MIDI/PC for program control, /MIDI/CC for control changes etc... Translating these in the script to be fowarded as real midi.

## Outgoing Format
A single RTMidi virtual port.

## Dependencies
This took ages of digging around/experimenting, along the way I did all of the following(!)
