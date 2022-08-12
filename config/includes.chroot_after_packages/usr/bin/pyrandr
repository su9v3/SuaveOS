#!/usr/bin/python3

import gi
import subprocess

gi.require_version("Gdk", "3.0")
from gi.repository import Gdk

allmonitors = []
gdkdsp = Gdk.Display.get_default()

for i in range(gdkdsp.get_n_monitors()):
    monitor = gdkdsp.get_monitor(i)
    allmonitors.append(monitor.get_model())

print("Monitors detected: " + str(allmonitors))

brightness = input("Monitor brightness to adjust to: ")

for monitor in allmonitors:
    subprocess.run(["xrandr", "--output", monitor, "--brightness", brightness])
