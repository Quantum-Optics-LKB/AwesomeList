
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