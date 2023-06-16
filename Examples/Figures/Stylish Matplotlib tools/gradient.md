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