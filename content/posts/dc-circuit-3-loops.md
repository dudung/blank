+++
title = 'DC circuit 3 loops'
date = 2024-01-14T17:12:38+07:00
draft = false
math = true
+++
Analyze DC circuit with 3 loops.


## simulator
One of the hosted version of [CircuitJS1](https://github.com/sharpie7/circuitjs1) is available on https://www.falstad.com/circuit/, where following code

```
$ 1 0.000005 0.7703437568215379 41 5 50 5e-11
v 80 176 80 80 0 0 40 6 0 0 0.5
r 80 80 240 80 0 1
r 240 80 240 176 0 1.5
r 240 176 80 176 0 2
r 240 176 400 176 0 2
v 400 176 400 80 0 0 40 12 0 0 0.5
r 80 176 80 288 0 16
v 400 288 80 288 0 0 40 16 0 0 0.5
r 240 80 400 80 0 1
w 400 288 400 176 0
```

will produce http://tinyurl.com/ytbrufmb with circuit diagram of


{{< svg "svg/circuit-20240114-1721.svg" >}}

where $\varepsilon_1 = 6 {\rm V}$, $\varepsilon_2 = 12 {\rm V}$, and $\varepsilon_3 = 16 {\rm V}$, respectively in CW direction from NW.


## elements
Let us name the elements as follow
```
   R1    R2
E1    R3    E2
   R4    R5
R6
      E3
```
according to the position of each element in previous figure.

Element | Value | Unit
:-: | :-: | :-:
$\varepsilon_1$ | 6 | V
$\varepsilon_1$ | 12 | V
$\varepsilon_1$ | 16 | V
$R_1$ | 1 | &Omega;
$R_2$ | 2 | &Omega;
$R_3$ | 1.5 | &Omega;
$R_4$ | 2 | &Omega;
$R_5$ | 2 | &Omega;
$R_6$ | 12 | &Omega;


## equations
Using [Kirchhoffs circuit laws](https://www.electronics-tutorials.ws/dccircuits/dcp_4.html) we can have following equations.
