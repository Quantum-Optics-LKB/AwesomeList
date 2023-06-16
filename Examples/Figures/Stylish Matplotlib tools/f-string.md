```python
tex = r"$\frac{\delta n}{\Delta n}$"
tex1 = r"$\frac{w_f}{\xi}$"
tex2 = r"$\frac{w_d}{\xi}$"
tex3 = r"$\frac{z}{z_{NL}}$"
fig.suptitle(
f"{tex} = {U/(n2*I/(1+I/Isat)):.2f}, {tex1} = {waist/xi:.2f}, {tex2} = {waist_d/xi:.2f}, {tex3} = {L/z_nl:.1f}")
```