# Installation

```sh
conda create -y fixationtask python=2.7
source activate fixationtask
conda install numpy scipy matplotlib pandas pyopengl pillow lxml openpyxl xlrd configobj pyyaml gevent greenlet msgpack-python psutil pytables requests cffi seaborn wxpython cython pyzmq pyserial
conda install -c conda-forge pyglet pysoundfile python-bidi moviepy pyosf
pip install zmq json-tricks pyparallel sounddevice pygame pysoundcard psychopy_ext psychopy
pip install git+https://github.com/grero/pylinkwrapper.git#egg=pylinkwrapper
conda install pyqt==4.11.4
```

In addition, the pylink package should be copied from the Eyelink directory to the site-packages directory of the `fixationtask` environment.
On a macOS, this could be

```sh
cp -r  /Applications/Eyelink/pylink/pylink2.7 ~/anaconda/envs/fixationtask/lib/python2.7/site-packages/pylink
```

# Usage

To start the Fixation task program, please follow these steps:

1) Click the "FixationTask" shortcut on the Destkop
 or
1\*) Run this command from the command line

```sh
python gui.py
```  

2) If you have a previous setting you would like to use, click the Load button
2.1) Select the file you want to load, e.g. w4_11_4_settings.txt, for settings for the 4th session of Wiesel's training conducted on the 11th of April
3) Make sure that the "Calibration" check box is checked under the "Setup" tab
4) If you want to make changes to how the calibration is done, please look under the "Calibration" tab
4.1) It's typically a good idea to choose 9 point calibration with white as the calibration color and "Circle"
     as the calibration stimulus
5) Once you are satisfied with the parameters, press "Start". You should hear the reward system clicking a few times
5.1) If you don't hear any clicking, make sure that the "Serial port" under the "Reward" tab is set to "com4"
6) Once you see the gray screen, click "Calibrate" on the Eyelink screen.
7) As you go through he calibration, click "Accept fixation" on the calibration screen (or press "Enter" on the stimulus computer keyobard) to accept each fixation in turn
8) It is advisable to run through the calibration a few times. To do so, just click "Restart" on the Eyelink sceen
9) Once you are happy with the calibration and you wish to move onto the actual task, click "Accept" on the Eyelink
   screen, and the click the Esc key on the stimulus computer keyboard
