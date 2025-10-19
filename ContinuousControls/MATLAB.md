# MATLAB
General tips/tricks in MATLAB doing system id

## Make `tf` given G(s) with poles
```
s = tf('s');
G = s / ((s + 3)*(s + 1));
G
bode(G)
step(G)
pzmap(G)
rlocus(G)
```
