### serial2midi

This is a replacement for [https://github.com/projectgus/hairless-midiserial](https://github.com/projectgus/hairless-midiserial) and [https://github.com/chava100f/SerialMidiBridge](https://github.com/chava100f/SerialMidiBridge).

It is based on the excellent [serialmidi](https://github.com/raspy135/serialmidi) python script.

Not as fancy as hairless-midiserial, but it works and is for end-users easier to use than the serialmidi script (I know at least one of them :wink:).

### Download

```
git clone https://github.com/chromalock/serial2midi
```

### Install Dependencies

```
pip install -r requirements.txt
```

### Usage

After starting you will be able to choose the serial port, baudrate, serial-to-midi port and midi-to-serial port. The Scan button will re-scan for available serial and midi ports. Your selection is remembered for next usage. After starting the server no changes can be made until the server is stopped.

### Usage (Linux)

If you wish to create a virtual MIDI device, you will need to make sure the correct kernel module is loaded:

```bash
sudo modprobe snd_virmidi midi_devs=1
```

You can then choose "Virtual Raw MIDI ..." as your serial2midi/midi2serial ports.


### Starting from the command line

It can also be started in the Terminal after downloading the python script as follows:

```
python3 serial2midi.py
```

This requires some python extra packages. You can install them as follows:

```
pip install pyserial python-rtmidi pysimplegui
```

### Adapting/building

If you want to make changes or build your own application you can use pyinstaller:

```
pyinstaller --onefile --windowed serial2midi.py
```

N.B. pyinstaller can be installed as follows:

```
pip install pyinstaller
```

You are free to modify it as long as it's not for commercial purposes.

### Notes

This is a fork of [https://github.com/chava100f/SerialMidiBridge](https://github.com/chava100f/SerialMidiBridge), except the dependency on `PySimpleGui` has been swapped out for `FreeSimpleGui`.
