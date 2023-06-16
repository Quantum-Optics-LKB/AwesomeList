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