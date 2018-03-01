%W% %G% %U%


# Speak project
#	espeak was already installed on rpi3b-two
sudo apt-get update
sudo apt-get install espeak
sudo apt-get install python-espeak
#
mkdir -p $HOME/espeak/project1
cd $HOME/espeak/project1
sudo espeak "hello world"
vi read.txt
#	Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.
#
sudo espeak -ven+f5 -s200 -f read.txt
#
sudo espeak -s120 -f read.txt
#
#	The user has to be in the audio group:
#	gpasswd -a [user] audio
sudo gpasswd -a uadmin  audio
#	For some reason I had to rebo0t for this to work ???
reboot

#
sudo modprobe snd_bcm2835
sudo aplay /usr/share/sounds/alsa/Front_Center.wav
sudo aplay /usr/share/sounds/alsa/Rear_Left.wav
rpi3b-two:  
	 ~/espeak/project2/test-1.txt
