# waveconverter
(c) Factoria Labs 2016
WaveConverter is a Python application, built on GTK+ 3. The GUI has been
implemented via Glade. A sqlite database has been implemented via
sqlalchemy. Finally, waveform plotting uses matplotlib.

You will need gnuradio installed for this software to work. While you
can install this via:
```
sudo apt-get install gnuradio
```
You will benefit from a much more recent version if you follow the
instructions at:

http://fieldxp.com/Chapter-2-Installing-the-Software.pdf

NEW: waveconverter now relies on a collection of common, reusable
code called "rf_utilities". For waveconverter to work, you must
get this code and point your PYTHONPATH to its location. For Example:

```
git clone https://github.com/paulgclark/rf_utilities ~/code
export PYTHONPATH="$PYTHONPATH:~/code"
```
(or better yet, add it to the end of ~/.bashrc)

To install the other pre-requisites for execution:

```
sudo apt-get install python-sqlalchemy
sudo apt-get install libgtk-3-dev
sudo apt-get install python-matplotlib
sudo apt-get install python-gi-cairo
```
If you are contributing to development, you will also need glade:
```
sudo apt-get install glade
```
To execute a test using an attached input I-Q file:
```
cd <install path>/src
./waveconverter.py -q ../input_files/fan_all_dip1101_pruned_dec_c304p55M_s830k.iq -o ../output_files/test.log -g -p 3
```
This will pre-load the appropriate protocol and input file. Clicking the Demod button
will then produce a baseband waveform. Clicking the Decode button will then produce
decoded data.

Please check out the User Guide for more information:
    doc/user_guide.pdf
