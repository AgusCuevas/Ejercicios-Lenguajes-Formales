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



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



### Autómata de Pila (AP)

-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------



-------------------------------------------------


