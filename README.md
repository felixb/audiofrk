# Audio fork

Audio fork is a little shell script letting you play your pulse controlled audio on a number of remote devices.
Audio is re-encoded and transmitted with gstreamer sending it via UDP.

# How to use

Run the server on the receiving side:

    audiofrk server [host[:port]]

Run the client on the sender side:

    audiofrk client [default-sink] host[:port] [host:[[port]] ...

Stop the service on any side with:

    audiofrk stop

# Dependencies

The following packages are necessary on Ubuntu/debian.

## On both sides

    gstreamer0.10-tools
    gstreamer0.10-plugins-base
    gstreamer0.10-plugins-good
    gstreamer0.10-plugins-ugly

## On the receiver side

    gstreamer0.10-alsa

## On the sender side

    pulseaudio

# Where I found the initial idea

gstreamer code comes mostly from [http://stackoverflow.com/a/15570501/2331953](here)

Initial idea and pulse code comes from [https://github.com/adgaudio/raspberry_pi_mopidy/blob/master/gstreamer.sh](here)
