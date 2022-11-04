# Programma in assembly semplificato

## P1
Programma che legge due numeri naturali A e B da input e calcola in output il loro minimo
Considerate anche la variante del programma nel caso di registri che possono contenere solo numeri maggiori o uguali a zero.

### A.
```
1	READ 1
2	READ 2
3	LOAD 1
4	SUB 2
5	JGTZ 8
6	WRITE 1
7	JUMP 9
8	WRITE 2
9	HALT
```

### B.
---
## P2
Programma che legge un numero naturale N maggiore o uguale a 0 e quindi calcola il minimo di N valori letti da input.
```
1	READ 1 //1-5 read N, if >0 then start, if 0 then jump to HALT, else input again
2	LOAD 1
3	JGTZ 6 //start
4	JZERO 18 //skip to end
5	JUMP 1 //loop back to start
6	READ 2 //input MIN
7	SUB=1 //decrement N
8	STORE 1 //store updated value of N
9	JZERO 17 //jump to line before HALT (WRITE 2 should be there) if N = 0
10	READ 3 //input NUM
11	LOAD 3 //load NUM into ACC
12	SUB 2 //calculate difference
13	JGTZ 7 //if NUM - MIN = (+) then loop again from decrement N
14	LOAD 3 //if NUM - MIN = (-) then NUM is smaller, reload NUM
15	STORE 2 //store NUM as MIN
16	JUMP 7 //loop again from decrement N
17	WRITE 2
18	HALT
```
---
## P3
Programma che eseguire le stesse operazioni del programma 2 memorizzando però prima gli N valori letti in inputi in N registri distinti (supponete di avere sempre abbastanza registri per ogni N) e, in una seconda fase effettuando il calcolo del valore minimo usandi i dati operazioni sui dati nei registri attraverso l’accumulatore (suggerimento: usate operatore *R che opera sul registro con indirizzo contenuto in R).

```
//reserving R1 for N, R2 for pointer, R3 min, R4 and above for input
1	READ 1 //1-5 same as P2
2	LOAD 1
3	JGTZ 6
4	JZERO #skip to end
5	JUMP 1
6	READ 2 //input MIN
7	SUB=1 //decrement N
8	STORE 1 //store updated value of N
9	JZERO 17 //jump to line before HALT (WRITE 2 should be there) if N = 0
10	READ 3 //input NUM
11	LOAD 3 //load NUM into ACC
12	SUB 2 //calculate difference
13	JGTZ 7 //if NUM - MIN = (+) then loop again from decrement N
14	LOAD 3 //if NUM - MIN = (-) then NUM is smaller, reload NUM
15	STORE 2 //store NUM as MIN
16	JUMP 7 //loop again from decrement N
17	WRITE 2
18	HALT
```

---
---
---
# Circuiti Combinatori
7 segment display

## E1
Costruire la tabella di verità

##|  |**x** |**y** |**z** |  |a |b |c |d |e |f |g
--|--|--|--|--|--|--|--|--|--|--|--|--
0 |  |0 |0 |0 |  |1 |1 |1 |1 |1 |1 |0
1 |  |0 |0 |1 |  |0 |1 |1 |0 |0 |0 |0
2 |  |0 |1 |0 |  |1 |1 |0 |1 |1 |0 |1
3 |  |0 |1 |1 |  |1 |1 |1 |1 |0 |0 |1
4 |  |1 |0 |0 |  |0 |1 |1 |0 |0 |1 |1
5 |  |1 |0 |1 |  |1 |0 |1 |1 |0 |1 |1
6 |  |1 |1 |0 |  |1 |0 |1 |1 |1 |1 |1
7 |  |1 |1 |1 |  |1 |1 |1 |0 |0 |0 |0

---
## E2
Calcolare la forma normale disguintiva e conguintiva per ogni uscita

### Forma normale disgiuntiva
$$
\Large
\begin{aligned}
	a &= \bar x \bar y \bar z  + \bar x y \bar z + \bar x y z + x \bar y z + x y \bar z + x y z 
	\\
	b &= \bar x \bar y \bar z  + \bar x \bar y z  + \bar x y \bar z  +\bar x y z  + x \bar y \bar z  + x y z 
	\\
	c &= \bar x \bar y \bar z  + \bar x \bar y z  + \bar x y z  + x \bar y \bar z  + \bar x y z + x y \bar z + x y z
	\\
	d &= \bar x \bar y \bar z  + \bar x y \bar z + \bar x y z + x \bar y z + x y \bar z
	\\
	e &= \bar x \bar y \bar z  + \bar x y \bar z + x y \bar z
	\\
	f &= \bar x \bar y \bar z  + x \bar y \bar z + x \bar y z + x y \bar z
	\\
	g &= \bar x y \bar z + \bar x y z + x \bar y \bar z + x \bar y z + x y \bar z
\end{aligned}
$$

### Forma normale congiuntiva
$$
\Large
\begin{aligned}
a &= (x+y+\bar z)(\bar x + y + z)
\\
b &= (\bar x + y + \bar z)(\bar x + \bar y + z)
\\
c &= (x + \bar y + z)
\\
d &= (x + y + \bar z)(\bar x + y + z)(\bar x + \bar y + \bar z)
\\
e &= (x + y + \bar z)(x + \bar y + \bar z)(\bar x + y + z)(\bar x + y + \bar z)(\bar x + \bar y + \bar z)
\\
f &= (x + y + \bar z)(x + \bar y + z)(x + \bar y + \bar z)(\bar x + \bar y + \bar z)
\\
g &= (x + y + \bar z)(\bar x + \bar y + \bar z)
\end{aligned}
$$
---
## E3
Applicare il metodo delle mappe di Karnaugh ad ogni formula

|template|x0y0|x0y1|x1y1|x1y0|
|-- |--  |--  |--  |--|
|z0 |0   |2   |6   |4|
|z1 |1   |3   |7   |5|

---
### a
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |1   |1   |0
z1 |0   |1   |1   |1
![[Pasted image 20221104153433.png]]
$$
\Large
\begin{aligned}
	a &= \bar x \bar z + y + xz
\end{aligned}
$$
---
### b
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |1   |0   |1
z1 |1   |1   |1   |0
![[Pasted image 20221104155506.png]]
$$
\Large
\begin{aligned}
	b &= \bar x + \bar y \bar z + y z
\end{aligned}
$$
---
### c
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |0   |1   |1
z1 |1   |1   |1   |1
![[C karnaugh.png]]
$$
\Large
\begin{aligned}
	c &= \bar x \bar y + x+z
\end{aligned}
$$
---
### d
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |1   |0   |1
z1 |0   |1   |1   |0
![[Pasted image 20221104155952.png]]
$$
\Large
\begin{aligned}
	d &= \bar x \bar z + y z + \bar y \bar z 
\end{aligned}
$$
---
### e
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |1   |1  |0
z1 |0   |0   |0   |0
![[Pasted image 20221104160258.png]]
$$
\Large
\begin{aligned}
	e &= \bar x \bar z + y \bar z
\end{aligned}
$$
---
### f
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |1   |0   |1   |1
z1 |0   |0   |0   |1
![[Pasted image 20221104161054.png]]
$$
\Large
\begin{aligned}
	f &= \bar y \bar z + xz + x \bar z
\end{aligned}
$$
---
### g
-|x0y0|x0y1|x1y1|x1y0
-- |--  |--  |--  |--
z0 |0   |1   |1   |1
z1 |0   |1   |0   |1
![[Pasted image 20221104164935.png]]
$$
\Large
\begin{aligned}
	g &= \bar x y + x \bar z + x \bar y
\end{aligned}
$$
---
## E4
Disegnare il circuito
![[circuit(1).png]]