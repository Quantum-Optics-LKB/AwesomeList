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