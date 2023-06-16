# Quantum Optics Awesome list
## Contents

- [Contents](#contents)

### Lab automation
- [GUIMuquans](https://github.com/Quantum-Optics-LKB/GUIMuquans) -Laser GUI to control power, frequency and display Laser state.-
- [Control scope](https://github.com/Quantum-Optics-LKB/ScopeInterface) -Python interface for oscilloscopes comminicating via SCPI commands through PyVisa. USB or TCPIP or anything.-
- [Tema power supply current and voltage](https://github.com/Quantum-Optics-LKB/Power_Suply_RS232_Control) -Code written for controlling the Tenma 72-2715-
- [Piezo](https://github.com/Quantum-Optics-LKB/Piezo) -Python interface for Thorlabs piezo devices-
- [Arduino ](https://github.com/Quantum-Optics-LKB/Arduino_linear_actuator) -Arduino driven linear actuator-
### Simulation
- [NLSE](https://github.com/Quantum-Optics-LKB/NLSE) -A small utility to easily simulate all sorts of non linear Schrödinger equation. It uses a split-step spectral scheme to solve the equation.-
- [OBE](https://github.com/Quantum-Optics-LKB/OBE) -Small repo for Optical Bloch Equations.-
- [Rubidium Spectrum Model](https://github.com/DawesLab/rubidium) -This script provides python code that is useful for calculating absorption spectra for the Rubidium D1 and D2 lines.-
### Lab measure
- [Phase](https://github.com/Quantum-Optics-LKB/PhaseUtils) -A selection of utilities to retrieve and process phase information of optical fields, live monitoring of the phase-
- [Velocity](https://github.com/Quantum-Optics-LKB/Turbulence) - Analyze the phase of the fluid in order to retrieve the velocity fields, detect vortices and cluster them in order to extract useful statistical properties.-
- [Transit](https://github.com/Quantum-Optics-LKB/Transit) - Code supporting Transit effects for non-linear index measurement in hot atomic vapors. This code aims at giving the tools for both measurement and numerical estimation of non-linear index of refractions in hot alkali vapors. -
### Raw tools
- Connection with instruments
	- [pyVISA](https://pyvisa.readthedocs.io/en/latest/) -PyVISA is a Python package that enables you to control all kinds of measurement devices independently of the interface -
	- [pySerial](https://pypi.org/project/pyserial/) -This module encapsulates the access for the serial port.-
	- [pyUSB](https://pypi.org/project/pyusb/) -PyUSB offers easy USB devices communication in Python. -    
	- [Allied vision](https://www.alliedvision.com/en/products/vimba-sdk/) - Speak with the PCO camera (runs on Windows, Linux)
	- [PCO](https://www.pco-tech.com/software/camera-control-software/pcocamware/) - Speak with the Allied vision camera (runs on Windows, not on linux)
	- [Basler](https://github.com/basler/pypylon) - Speak with the Basler camera (runs on Windows, Linux)
	- [FLIR/PointGrey](https://www.flir.fr/products/flycapture-sdk/) - Speak with the FLIR/PointGrey camera (runs on Windows, Linux)
- Computing tools
	- [Cupy](https://cupy.dev/) -  CuPy is an open-source array library for GPU-accelerated computing with Python -
	- [Numba](https://numba.pydata.org/) -Numba is an open source JIT compiler that translates a subset of Python and NumPy code into fast machine code. -
	- [Cython](https://cython.org/) -Cython is an optimising static compiler for both the Python programming language and the extended Cython programming language (based on Pyrex).-
	- [Tensorflow](https://www.tensorflow.org//) -Create production-grade machine learning models -
	- [FFT](https://pyfftw.readthedocs.io/en/latest//) -pyFFTW is a pythonic wrapper around FFTW, the speedy FFT library-
        
### Stylish Matplotlib tools
- [Use a gradient of color in your plot](https://stackoverflow.com/questions/38208700/matplotlib-plot-lines-with-colors-through-colormap)
	Other (improvised) example
```python
times = np.linspace(0,10)
periods = np.linspace(2,6)
fig, ax = plt.subplots()
colors = plt.cm.ocean(np.linspace(0,1,len(freq)))
for i in range(len(freq)):
	ax.plot(times,np.cos(times*2*np.pi/periods[i]),color=colors[i],label=f'T={periods[i]}')
ax.set_xlabel('time')
plt.show()
```
	
- [Use a slider](https://matplotlib.org/stable/gallery/widgets/slider_demo.html) - To slide by hand a parameter and see the resulting plot evolving
Example with a fractionnal slider and set_data (parametric plot of the varying parameter):
```python
def ellipse_det(det):
i = np.where(det_arr==det)
Ex, Ey =  all_Ex[i,:], all_Ey[i,:]
return Ex[0,0,:],Ey[0,0,:]

Ex, Ey = ellipse_det(det_arr[0])

fig, ax = plt.subplots()
ax.set_aspect('equal')
ax.set_xlabel(r'$E_x$')
ax.set_ylabel(r'$E_y$')
ax.set_xlim([-30,30])
ax.set_ylim([-30,30])
line, = ax.plot(np.zeros(Ex.shape),np.zeros(Ey.shape), color='blue')
# line.set_data(Ex,Ey)
allowed_det = det_arr
# adjust the main plot to make room for the sliders
fig.subplots_adjust(left=0.25, bottom=0.25)
# create the sliders
ax_det = fig.add_axes([0.25, 0.1, 0.65, 0.03])
det_slider = Slider(
ax=ax_det, label=r"$\Delta$ (GHz)", valmin=det_arr[0], valmax=det_arr[-1],
valinit=det_arr[0], valstep=allowed_det,
color="blue"
)

def update(val):
det = det_slider.val
Ex, Ey = ellipse_det(det)
line.set_data(Ex,Ey)
fig.canvas.draw_idle()

# register the update function with each slider
det_slider.on_changed(update)
```

-[f-string formatting](https://realpython.com/python-f-strings/) -To format the strings of your plot (labels, titles...) with data
Example:
```python
tex = r"$\frac{\delta n}{\Delta n}$"
tex1 = r"$\frac{w_f}{\xi}$"
tex2 = r"$\frac{w_d}{\xi}$"
tex3 = r"$\frac{z}{z_{NL}}$"
fig.suptitle(
f"{tex} = {U/(n2*I/(1+I/Isat)):.2f}, {tex1} = {waist/xi:.2f}, {tex2} = {waist_d/xi:.2f}, {tex3} = {L/z_nl:.1f}")
```

-[Cycler](https://matplotlib.org/cycler/) -To personnalize the way matplotlib cycles through the colors of the colorbar
```python
import matplotlib.pyplot as plt
from cycler import cycler

# for plots
tab_colors = ['tab:blue', 'tab:orange', 'forestgreen', 'tab:red', 'tab:purple', 'tab:brown',
		'tab:pink', 'tab:gray', 'tab:olive', 'teal']
fills = ['lightsteelblue', 'navajowhite', 'darkseagreen', 'lightcoral', 'violet', 'indianred',
	'lavenderblush', 'lightgray', 'darkkhaki', 'darkturquoise']
edges = tab_colors
custom_cycler = (cycler(color=tab_colors)) + \
(cycler(markeredgecolor=edges))+(cycler(markerfacecolor=fills))
plt.rc('axes', prop_cycle=custom_cycler)
# to use latex
plt.rcParams.update({
"text.usetex": True,
"font.family": "serif"
})
fig, ax = plt.subplots()
# to change the starting point of the cycler
ax.set_prop_cycle(cucstom_cycler[1:])
```

-[Animation](https://matplotlib.org/stable/api/animation_api.html) -To animate your plot (1D or 2D)
Example from PhaseUtils/monitor_phase.py , in the function monitor_phase:
```python
fig, ax = plt.subplots(1, 2)
divider0 = make_axes_locatable(ax[0])
cax0 = divider0.append_axes("right", size="5%", pad=0.05)
divider1 = make_axes_locatable(ax[1])
cax1 = divider1.append_axes("right", size="5%", pad=0.05)
im0 = ax[0].imshow(phase, cmap='twilight_shifted',
				vmin=-np.pi, vmax=np.pi)
im1 = ax[1].imshow(cont**2/np.max(cont**2),
				cmap='viridis', vmin=0, vmax=1)
fig.colorbar(im0, cax=cax0)
fig.colorbar(im1, cax=cax1)
ax[0].set_title("Phase")
ax[1].set_title("Intensity")

def animate(i):
"""Animation function for the window

Args:
	i (int): Counter from the animate function
"""
ret, frame[:, :] = cam.read()
im_fringe[:, :] = contrast.im_osc_fast_t(frame, cont=False)
phase[:, :] = contrast.angle_fast(im_fringe)
cont[:, :] = np.abs(im_fringe)
im0.set_data(phase)
im1.set_data(cont**2/np.max(cont**2))
return im0, im1
anim = animation.FuncAnimation(fig, animate,
							interval=33, blit=True)
plt.show(block=True)
```


