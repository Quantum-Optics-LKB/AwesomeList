# Quantum Optics Awesome list

```Home made = 🚀```


   * [Lab automation and instrument control](#lab-automation-and-instrument-control)
      * [Laser](#laser)
      * [Thorlabs](#thorlabs)
      * [Scope, driver and actuators](#scope-driver-and-actuators)
      * [Cameras](#cameras)
      * [Generic communication tools](#generic-communication-tools)
   * [Measurement utilities](#measurement-utilities)
   * [Numerical simulations](#numerical-simulations)
      * [Solvers](#solvers)
      * [Computing tools](#computing-tools)
   * [Publication](#publication)
      * [Stylish Matplotlib tools](#stylish-matplotlib-tools)

--- 

## Lab automation and instrument control
### Laser
- [GUIMuquans](https://github.com/Quantum-Optics-LKB/GUIMuquans). Laser GUI to control power, frequency and display Laser state.  🚀
### Thorlabs
- [Piezo](https://github.com/Quantum-Optics-LKB/Piezo). Python interface for Thorlabs piezo devices.  🚀
- [pylablib](https://pylablib.readthedocs.io/en/latest/). Control different Thorlabs motorized devices: piezo, rotating mounts. (Windows only). 
- [APT](https://thorlabs-apt-device.readthedocs.io/en/latest/) - lower level than kinesis, to control Thorlabs motorized devices. It works on Linux.

### Scope, driver and actuators
- [Control scope](https://github.com/Quantum-Optics-LKB/ScopeInterface). Python interface for oscilloscopes comminicating via SCPI commands through PyVisa. USB or TCPIP or anything.  🚀
- [Tenma power supply current and voltage](https://github.com/Quantum-Optics-LKB/Power_Suply_RS232_Control). Code for controlling the Tenma 72-2715. 🚀
- [Arduino actuator](https://github.com/Quantum-Optics-LKB/Arduino_linear_actuator). Arduino driven linear actuator.  🚀

### Cameras
- [Allied vision](https://www.alliedvision.com/en/products/vimba-sdk/). Allied vision camera (runs on Windows, Linux).
- [PCO](https://www.pco-tech.com/software/camera-control-software/pcocamware/). PCO camera (runs on Windows, not on linux).
- [Basler](https://github.com/basler/pypylon). Basler camera (runs on Windows, [Linux](https://www.forecr.io/blogs/connectivity/pylon-installation-for-basler-camera)): [GUI download](https://www.baslerweb.com/en/downloads/software-downloads/) and [Python SDK](https://github.com/basler/pypylon).
- [FLIR/PointGrey](https://www.flir.fr/products/flycapture-sdk/). FLIR/PointGrey camera (runs on Windows, Linux).


### Generic communication tools
- [pyVISA](https://pyvisa.readthedocs.io/en/latest/). Python package to enable control of measurement devices independently of the interface.
- [pySerial](https://pypi.org/project/pyserial/). Encapsulate the access for the serial port.
- [pyUSB](https://pypi.org/project/pyusb/). Easy USB devices communication in Python.




## Measurement utilities
- [Phase](https://github.com/Quantum-Optics-LKB/PhaseUtils). Utilities to retrieve and process phase information of optical fields, live monitoring of the phase.  🚀


## Numerical simulations
### Solvers
- [NLSE](https://github.com/Quantum-Optics-LKB/NLSE). Utility to  simulate non linear Schrödinger equation (Split-step spectral scheme).  🚀
- [OBE](https://github.com/Quantum-Optics-LKB/OBE). Solving Optical Bloch Equations.  🚀
- [Rubidium Spectrum Model](https://github.com/DawesLab/rubidium). Python code to calculate absorption spectra for the Rb lines.
- [Transit](https://github.com/Quantum-Optics-LKB/Transit). Transit effects for non-linear index measurement in hot atomic vapors. Both measurement utilities and numerical estimation.  🚀



### Computing tools
- [Cupy](https://cupy.dev/). Open-source array library for GPU-accelerated computing with Python.
- [Numba](https://numba.pydata.org/). Open source JIT compiler that translates a subset of Python and NumPy code into fast machine code.
- [Cython](https://cython.org/). Optimising static compiler for both the Python and the extended Cython programming language (based on Pyrex).
- [Tensorflow](https://www.tensorflow.org//). Create production-grade machine learning models. 
- [FFT](https://pyfftw.readthedocs.io/en/latest//). Pythonic wrapper around FFTW, the speedy FFT library.


## Publication	    
### Stylish Matplotlib tools
- [Use a gradient of color in your plot](https://stackoverflow.com/questions/38208700/matplotlib-plot-lines-with-colors-through-colormap). See the 
[example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/gradient_color_plot.md).
- [Use a slider](https://matplotlib.org/stable/gallery/widgets/slider_demo.html) - See the 
[example with a discrete slider and parametric plots](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/slider.md).
- [f-string formatting](https://realpython.com/python-f-strings/). Format strings of your plot (labels, titles...) with data.
See the [example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/f-string.md).
- [Cycler](https://matplotlib.org/cycler/). Personnalize the way matplotlib cycles through the colors of the colorbar. See the 
[example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/cycler.md).
- [Animation](https://matplotlib.org/stable/api/animation_api.html). Animate your plot (1D or 2D). See the [example from PhaseUtils/monitor_phase.py](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/animation.md).


### Markdown
- [TOC Generation](https://github.com/ekalinin/github-markdown-toc)
