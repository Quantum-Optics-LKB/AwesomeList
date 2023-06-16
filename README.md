# Quantum Optics Awesome list

### Legend
- Home made: 🚀

### Lab automation - instrument controls
- [GUIMuquans](https://github.com/Quantum-Optics-LKB/GUIMuquans) -Laser GUI to control power, frequency and display Laser state.  🚀
- [Control scope](https://github.com/Quantum-Optics-LKB/ScopeInterface) -Python interface for oscilloscopes comminicating via SCPI commands through PyVisa. USB or TCPIP or anything.  🚀
- [Tenma power supply current and voltage](https://github.com/Quantum-Optics-LKB/Power_Suply_RS232_Control) -Code written for controlling the Tenma 72-2715. 🚀
- [Piezo](https://github.com/Quantum-Optics-LKB/Piezo). Python interface for Thorlabs piezo devices .  🚀
- [Arduino actuator](https://github.com/Quantum-Optics-LKB/Arduino_linear_actuator). Arduino driven linear actuator.  🚀
- [pylablib](https://pylablib.readthedocs.io/en/latest/) - Great repo to control different thorlabs motorized devices (piezo, rotating mounts), but works only on Windows. 
- [APT](https://thorlabs-apt-device.readthedocs.io/en/latest/) - lower level than kinesis, to control Thorlabs motorized devices. It works on Linux, so we should recode everything using it.

### Simulation
- [NLSE](https://github.com/Quantum-Optics-LKB/NLSE) -A small utility to easily simulate all sorts of non linear Schrödinger equation. It uses a split-step spectral scheme to solve the equation.  🚀
- [OBE](https://github.com/Quantum-Optics-LKB/OBE) -Small repo for Optical Bloch Equations.  🚀
- [Rubidium Spectrum Model](https://github.com/DawesLab/rubidium) -This script provides python code that is useful for calculating absorption spectra for the Rubidium D1 and D2 lines.
- [Transit](https://github.com/Quantum-Optics-LKB/Transit) - Code supporting Transit effects for non-linear index measurement in hot atomic vapors. This code aims at giving the tools for both measurement and numerical estimation of non-linear index of refractions in hot alkali vapors.  🚀

### Lab measure
- [Phase](https://github.com/Quantum-Optics-LKB/PhaseUtils) -A selection of utilities to retrieve and process phase information of optical fields, live monitoring of the phase.  🚀

### Raw tools
- Connection with instruments
	- [pyVISA](https://pyvisa.readthedocs.io/en/latest/) -PyVISA is a Python package that enables you to control all kinds of measurement devices independently of the interface.
	- [pySerial](https://pypi.org/project/pyserial/) -This module encapsulates the access for the serial port.
	- [pyUSB](https://pypi.org/project/pyusb/) -PyUSB offers easy USB devices communication in Python.
	- [Allied vision](https://www.alliedvision.com/en/products/vimba-sdk/) - Speak with the PCO camera (runs on Windows, Linux).
	- [PCO](https://www.pco.de/software/development-tools/pcosdk/) - Speak with the Allied vision camera (runs on Windows, not on linux).
	- [Basler](https://github.com/basler/pypylon) - Speak with the Basler camera (runs on Windows, Linux).
	- [FLIR/PointGrey](https://www.flir.fr/products/flycapture-sdk/) - Speak with the FLIR/PointGrey camera (runs on Windows, Linux).

### Computing tools
- [Cupy](https://cupy.dev/). CuPy is an open-source array library for GPU-accelerated computing with Python.
- [Numba](https://numba.pydata.org/). Numba is an open source JIT compiler that translates a subset of Python and NumPy code into fast machine code.
- [Cython](https://cython.org/). Cython is an optimising static compiler for both the Python programming language and the extended Cython programming language (based on Pyrex).
- [Tensorflow](https://www.tensorflow.org//). Create production-grade machine learning models. 
- [FFT](https://pyfftw.readthedocs.io/en/latest//) -pyFFTW is a pythonic wrapper around FFTW, the speedy FFT library-
        
### Stylish Matplotlib tools
- [Use a gradient of color in your plot](https://stackoverflow.com/questions/38208700/matplotlib-plot-lines-with-colors-through-colormap). See the 
[example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/gradient_color_plot.md)

	
- [Use a slider](https://matplotlib.org/stable/gallery/widgets/slider_demo.html) - To slide by hand a parameter and see the resulting plot evolving
[Example with a discrete slider and parametric plots (uses set_data)](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/slider.md)


- [f-string formatting](https://realpython.com/python-f-strings/) -To format the strings of your plot (labels, titles...) with data
[Example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/f-string.md)


- [Cycler](https://matplotlib.org/cycler/) -To personnalize the way matplotlib cycles through the colors of the colorbar
[Example](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/cycler.md)



- [Animation](https://matplotlib.org/stable/api/animation_api.html) -To animate your plot (1D or 2D)
[Example from PhaseUtils/monitor_phase.py](https://github.com/Quantum-Optics-LKB/awesome_list/blob/main/Examples/Figures/Stylish%20Matplotlib%20tools/animation.md)



