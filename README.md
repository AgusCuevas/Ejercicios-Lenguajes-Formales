# Ejercicios-Lenguajes-Formales

# Parcial 1
## Temas

# Parcial 2
## Temas
### Gramática Independiente de Contexto (GIC)

-------------------------------------------------

- Diséñese una GIC para L = {a^n b^m / n <> m; n,m > 0}
#### Solucion
S -> A | B \
A  -> aAb | aA | aab \
B -> aBb | Bb | abb 
  
-------------------------------------------------

- Diséñese una GIC para L = {[], [id], [id,id], [id,id,id], ...}
#### Solucion
S -> [A] \
A -> idBA | id \
B -> ,

-------------------------------------------------

- Diséñese una GIC para L = {x^n y^m z^n / n > 0 ^ m es par} U {a^n b^m a^m b^n / n, m >= 0}
#### Solucion

S -> A | C | λ \
A -> xAz | xBz | xz \
B -> yyB | yy \
C -> aCb | ab | D \
D -> bDa | ba

-------------------------------------------------

- Diseñese una GIC en FNC para L = {bcc, abccc, abbccccc, aabcccc, aabbcccccc, aaaaabccccccc, ...}
#### Solucion

L= {a^n b^m c^(n+2m) / n>=0, m>=1 } 

#### GIC 
S -> aSc | A \
A -> bAcc | bcc 

#### GIC FNC 
S -> XB | YC | YD \
A -> YC | YD \
B -> SZ \
C -> AD \
D -> ZZ \
X -> a \
Y -> b \
Z -> c

-------------------------------------------------

- Determínese por comprensión simbólica el LIC generado por GIC <{a, b}, {S, U, T, V}, S, \
{ \
S -> UT \
U -> aa | ab | ba | bb \
T -> aTa | bTb | V \
V -> aa | ab | ba | bb \
}>. Normalícese a FNC.

#### Solucion
L = {w1w2w3w2^R / w1,w3 ∈ {a, b}^2 ^ w2 ∈ {a, b}* } 

#### FNC 
S -> UT \
U -> AA | AB | BA | BB \
T -> AX | BY | AA | AB | BA | BB \
X -> TA \
Y -> TB \
A -> a \
B -> b 
 
-------------------------------------------------

- Diséñese una GIC FNC para L = {[^n]^m / m > n >= 0} \
#### Solucion

m > n =>  m = n + a

L = {[^n ]^n ]^a / n >= 0 ^ a > 0}

S -> AB | B \ 
A -> [A] | [] \
B -> ]B | ]

FNC: \
S  -> AB | CB | ] \
A  -> OA' | OC \
A' -> AC \
B  -> CB | ] \
O  -> [ \
C  -> ] 

-------------------------------------------------

- Diséñese la GIC bien formada del lenguaje L = {a^n b^m c^(n+m) / n, m >= 0} U {d^n ww^R g^n / w ∈ {e, f}* ^ n > 0}

#### Solucion

S -> λ | aAc | bBc | bc | ac | dCg | eDe | fDf | ee | ff | dg \
A -> aAc | bBc | bc | ac \
B -> bBc | bc \
C -> dCg | eDe | fDf | ee | ff | dg \
D -> eDe | fDf | ee | ff

-------------------------------------------------

- Diséñese AP por vaciado de pila para L = {a^n b^m c^k / n, m , k >= 0; k + m = n v k + n = m}

#### Solucion

caso 1: n,m,k >= 0; k + m = n
L = {a^k a^m b^m c^k / m,k >= 0}

S -> λ | aAc | aBb | ac | ab
A -> aAc | ac | aBc
B -> aBb | ab

caso 2: n,m,k >= 0; k + n = m
L = {a^n b^n b^k c^k / n,k >= 0}

S -> λ | aCbD | abD | ab | bc | aCb | bDc
C -> aCb | ab
D -> bDc | bc

S -> λ | aAc | aBb | ac | ab | aCbD | abD | bc | aCb | bDc
A -> aAc | ac | aBc
B -> aBb | ab
C -> aCb | ab
D -> bDc | bc 

FNG:
S -> λ | aAZ | aBY | aZ | aY | aCYD | aYD | bZ | aCY | bDZ
A -> aAZ | aZ | aBZ
B -> aBY | aY
C -> aCY | aY
D -> bDZ | bZ
Y -> b
Z -> c

AP
Q = {q0}
F = {}
Σ = {a, b, c}
q0 = q0
p = S
Γ = {A, Z, B, Y, C, D, S}
δ(q0, λ, S) = (q0, λ)
δ(q0, a, S) = (q0, AZ)
δ(q0, a, S) = (q0, BY)
...

-------------------------------------------------



### Autómata de Pila (AP)

-------------------------------------------------

- Diseñese AP por vaciado de pila (algoritmo) que reconoce el lenguaje generado por GIC <{a, b}, {S, A}, S, {S -> AA, S -> a, A -> AA, A -> b}>
  
#### Solucion

GIC en FNG \
S -> bA | bZA | a \
A -> b | bZ \
Z -> b | bZ | bZZ


-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------


