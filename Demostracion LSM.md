### Límite de suma de Riemann
\[
 \lim_{\lambda \to 0}\sigma(f, P, (\xi_i)) = I
\]

\( \forall \epsilon > 0, \exists P_\epsilon \) definida en \( [a, b] \): \( P \supset P_\epsilon \) se cumple que \( 0 \leq |\sigma(f, P, (\xi_i)) - I| < \epsilon \)

### Toda función no acotada no será integrable en ese intervalo

Supongamos que \( f \) es no acotada en \( [a, b] \). Para cualquier partición \( P \) de \( E \), siempre puede encontrarse un intervalo \( [x_{k-1}, x_k] \) donde f es no acotada. Sin pérdida de generalidad, en una partición cualquiera P, consideremos a \( \sigma_k\) como una suma integral a la que se le ha omitido el punto k-ésimo:

\[
 \sigma_k = \sum_{i=1}^{n} f(\xi_i) \Delta x_i, i \neq k
\]
Puesto que f no va a estar acotada en el intervalo \([x_{k-1}, x_k]\), pueden encontrarse puntos \(\xi_k\) que pertenezcan a él y que cumplan \(f(\xi_k) > M\) sea M cualquier número prefijado. Entonces en particular podemos tomar \( M > 0 \), \(\xi_k\), y \(\Delta x_k\) > 0 (es decir la longitud del intervalo \(\neq 0\)) tal que:
\(|f(\xi_k)| \geq \frac{|\sigma_k| + M}{ \Delta x_k}\)
\(|f(\xi_k)|\Delta x_k \geq |\sigma_k| + M \) 

Además, la suma integral asociada a P va a ser:
\[
\sigma(f, P, \xi_i) = \sigma_k + f(\xi_k)\Delta x_k
\]
Aplicando módulo a ambas partes:
\[
|\sigma(f, P, \xi_i)| = |\sigma_k + f(\xi_k)\Delta x_k|
\]
\[
|\sigma(f, P, \xi_i)| \geq |f(\xi_k)|\Delta x_k - |\sigma_k| 
\]
Sustituyendo \(|f(\xi_k)|\Delta x_k\) por \(|\sigma_k| + M\) encontrado anteriormente:
\[
|\sigma(f, P, \xi_i)| \geq |\sigma_k| + M - |\sigma_k| 
\]
\[
|\sigma(f, P, \xi_i)| \geq  M
\]
Esta demostración prueba que la suma integral de f no acotada puede hacerse tan grande como se quiera y por tanto no tendrá límite finito, lo que quiere decir que toda f no acotada es no integrable.

Establecido esto:

## Demostración: \( f \in \mathcal{R}[a, b]\)\( \Rightarrow \overline{I} = \underline{I} \)
Demostremos que si \( \forall \epsilon > 0,  \exists P_\epsilon \) tal que \(P \supset P_\epsilon \), se cumple que \( |\sigma(f, P, (\xi_i)) - I| < \epsilon \Rightarrow \lim_{\lambda \to 0}(S - s) = 0 \Rightarrow \underline{I} = \overline{I} \)

Primeramente, demostremos que:

### Demostración: \( \lim_{\lambda \to 0}(S) = \overline{I} \) y \( \lim_{\lambda \to 0}(s) = \underline{I} \)

Sea el intervalo \( [a, b] \) y sean \( P_1 \) y \( P_2 \) dos particiones del mismo. Digamos que \( P_2 \) es más fina que \( P_1 \), es decir, \( P_2 \supset P_1 \)
Sea los puntos \( X_{k-1} \) y \( X_k \) de ambas particiones y el punto \(X'\) en \( P_2\) tal que \( X_{k-1} \leq X' \leq X_k \)
Puesto que estamos trabajando en una función acotada y sus intervalos también lo estarán, podemos elegir \( M \) y \( m \) los supremos del intervalo \( [X_{k-1}, X'] \) y \( [X', X_k] \) respectivamente, y sea \( M_k \) el supremo del intervalo \( [X_{k-1}, X_k] \):

\( S(f, P_2) - S(f, P_1) = M(X'- X_{k-1}) + m(X_k - X') - M_k(X_k - X_{k-1}) \) por la definición de Sumas de Darboux

Pero \( m \leq M_k \) y \(M \leq M_k \) ( \( M_k \) es el supremo del intervalo completo y por tanto el mayor de los dos)

Por tanto es posible reemplazar \( m \) y \( M \) por \( M_k \) y cambiar el \( = \) por \( \leq \), obteniéndose:

\[
 S(f, P_2) - S(f, P_1) \leq M_k(X'- X_{k-1}) + M_k(X_k - X') - M_k(X_k - X_{k-1})
\]

Sacando factor común \( M_k \) y simplificando:

\[
 S(f, P_2) - S(f, P_1) \leq M_k(X_k - X_{k-1}) - M_k(X_k - X_{k-1}) = 0
\]
\[
 S(f, P_2) - S(f, P_1) \leq 0
\]

Por tanto,

\[
 P_2 \supset P_1 \Rightarrow S(f, P_2) \leq S(f, P_1)
\]

Esto significa que mientras más fina sea la partición, menor será la suma superior que le corresponde. Por tanto, mientras más disminuye \( \lambda \) (la longitud del intervalo mayor) menor es la suma superior. 

\[
 P_{n + 1} \supset P_n \Rightarrow S(f, P_{n + 1}) \leq S(f, P_n), 
\]
Entonces la función va a ser monótona decreciente con \( \lambda \) que tiende a 0, por lo que su límite es su ínfimo. 
Pero como el ínfimo de las particiones de la Suma superior está definido como \( \overline{I} \):
\[
 \lim_{\lambda \to 0}(S) = \overline{I}
\]

Ahora, para la suma inferior, planteamos a \(m, M\), y \( M_k \) como los ínfimos de los intervalos previamente dados, que sabemos que exiten por la acotación, y volvemos a expresar:
\( s(f, P_2) - s(f, P_1) = M(X'- X_{k-1}) + m(X_k - X') - M_k(X_k - X_{k-1}) \) por la definición de Sumas de Darboux

Pero \( m \geq M_k \) y \(M \geq M_k \) ( \( M_k \) es el ínfimo del intervalo completo y por tanto el menor de los dos)

Por tanto es posible reemplazar \( m \) y \( M \) por \( M_k \) y cambiar el \( = \) por \( \geq \), obteniéndose:

\[
 s(f, P_2) - s(f, P_1) \geq M_k(X'- X_{k-1}) + M_k(X_k - X') - M_k(X_k - X_{k-1})
\]

Sacando factor común \( M_k \) y simplificando:

\[
 s(f, P_2) - s(f, P_1) \geq M_k(X_k - X_{k-1}) - M_k(X_k - X_{k-1}) \leq 0
\]
\[
 s(f, P_2) - s(f, P_1) \geq 0
\]

Por tanto,

\[
 P_2 \supset P_1 \Rightarrow s(f, P_2) \geq s(f, P_1)
\]


Como mientras más fina sea la partición, mayor será la suma inferior, esta función va a ser monótona creciente de forma análoga y su límite el supremo, que está definido como \( \underline{I} \). Por tanto:
\[
 \lim_{\lambda \to 0}(s) = \underline{I}
\]

Concluyendo, \( \lim_{\lambda \to 0}(S - s) =  \lim_{\lambda \to 0}(S) -  \lim_{\lambda \to 0}(s) = \overline{I} - \underline{I} \)
Entonces, \( \lim_{\lambda \to 0}(S - s) = 0 \Rightarrow \overline{I} - \underline{I} = 0 \Rightarrow \overline{I} = \underline{I} \), al mismo tiempo que \( \overline{I} = \underline{I} \Rightarrow \overline{I} - \underline{I} = 0 \Rightarrow \lim_{\lambda \to 0}(S - s) = 0 \)

Por tanto :

\[
 \lim_{\lambda \to 0}(S - s) = 0 \iff \overline{I} = \underline{I}
\]

Ahora, demostremos que f integrable por Riemann \( \Rightarrow \lim_{\lambda \to 0}(S - s)= 0 \), lo cual a su vez va a implicar \( \overline{I} = \underline{I} \) :

Por hipótesis,  \( \forall \epsilon > 0, \exists P_\epsilon \) tal que \( P \supset P_\epsilon \) va a cumplirse:

\[
 I - \epsilon  < \sigma(f, P, (\xi_i)) < \epsilon + I
\]

Ahora, sabemos que \( \overline{I} \) es el ínfimo de las sumas superiores de las posibles particiones del intervalo, por tanto, \( \overline{I} \leq S(f, P) \), e \( \underline{I} \) es el supremo de las sumas inferiores de las posibles particiones del intervalo, por tanto \( \underline{I} \geq s(f, P) \)

Además, \( S(f, P) = sup(\sigma(f, P, {(\xi_i)})) \), y \( s(f, P) = inf(\sigma(f, P, {(\xi_i)})) \)

De lo anterior se deduce que \( inf(\sigma(f, P, {(\xi_i)})) = s(f, P) \leq \sigma(f, P, {(\xi_i)}) \leq S(f, P) = sup(\sigma(f, P, {(\xi_i)})) \)
Insertando este resultado en \( I - \epsilon < \sigma(f, P, (\xi_i)) < I + \epsilon \) , se cumple que \( I - \epsilon \leq s  \leq S \leq I + \epsilon \)

Ahora, dado que \( s \leq S: S - s \leq 0 \)

Usamos \( I - \epsilon \leq s \) y \( S \leq I + \epsilon \), restando, \( S - s \leq (I + \epsilon) - (I - \epsilon) = 2\epsilon \)

Uniendo ambas, \( 0 \leq S -s \leq 2 \epsilon \), y como \( \epsilon > 0 \), podemos decir \( -2\epsilon \leq S - s \leq 2\epsilon \) , es decir:

\[
 \lim_{\lambda \to 0}(S - s) = 0
\]

Que a su vez implica que \( \overline{I} = \underline{I} \)

Concluyendo, \( f(x) \in \mathcal{R}[a, b] \Rightarrow \overline{I} = \underline{I} \)

### Cualesquiera sean \( P_1 \) y \( P_2 \), \( s(f, P_1) \leq S(f, P_2) \)

Demostración: Sea \( P \supset P_1 \) y \( P \supset P_2 \), se cumple que:

\[
 s(f, P_1) \leq s(f, P) \leq S(f, P) \leq S(f, P_2)
\]
Como fue demostrado anteriormente.
Entonces por transitividad queda demostrado que \( s(f, P_1) \leq S(f, P_2) \).

## Demostración:\( \overline{I} = \underline{I} \Rightarrow f \in \mathcal{R}[a,b]\)
Es decir:
\[ \underline{I} = \overline{I} \Rightarrow \forall \epsilon > 0, \exists P_\epsilon: P \supset P_\epsilon \text{ tal que } |\sigma(f, P, (\xi_i)) - I| < \epsilon\]

De las definiciones de integral superior e inferior se obtiene que:

 \[
   s \leq \underline{I} \leq \overline{I} \leq S
 \]

Restando \( \overline{I} \leq S\) y \( s \leq \underline{I} \):
\[
 \overline{I} - \underline{I} \leq S - s
\]
Sea el caso \( \underline{I} = \overline{I} \), designaremos al valor común de \( \underline{I} \) y \( \overline{I} \) como la variable \( I \), entonces:

\[
 s \leq I \leq S
\]

Luego \( 0 \leq I - s \leq S - s \) (restando s), y como \( S - s \geq S - I \geq 0 \) (restando \( S \) en la inicial y multiplicando por -1), equivalente a \( 0 \leq S - I \leq S - s \), entonces:
\[
 \lim_{\lambda \rightarrow 0} (I - s) = 0 \quad \text{y} \quad \lim_{\lambda \rightarrow 0} (S - I) = 0
\]

Es decir que \( \forall \epsilon > 0, \exists P_\epsilon: P \supset P_\epsilon \), entonces \( I - s < \epsilon \) y \( S - I < \epsilon \).

Se tiene que \( s \leq \sigma(f, P, (\xi_i)) \leq S \Rightarrow -(S - I) \leq I - \sigma(f, P, (\xi_i)) \leq I - s \) (restándole a \(I\), cada miembro)

Luego reemplazamos lo anterior y llegamos a: \( -\epsilon \leq I - \sigma(f, P, (\xi_i)) \leq \epsilon \), lo cual multiplicando por -1, es equivalente a \( -\epsilon \leq \sigma(f, P, (\xi_i)) - I \leq \epsilon \) lo que significa que:

\[
 \lim_{\lambda \rightarrow 0} \sigma(f, P, (\xi_i)) = I
\]

Hemos demostrado que \( \overline{I} = \underline{I} \Rightarrow f \in \mathcal{R}[a,b] \)

Ahora que tenemos el implica en ambos sentidos, hemos llegado a:

\(f \in \mathcal{R}[a,b] \iff \overline{I} = \underline{I} \iff  \lim_{\lambda \to 0}(S - s) = 0\) 

Que es lo que queríamos demostrar.
