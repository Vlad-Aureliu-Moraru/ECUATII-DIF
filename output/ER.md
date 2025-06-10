Ecuațiile de tip Riccati (ER) reprezintă o clasă importantă de ecuații diferențiale de ordinul I, neliniare. Mai jos găsiți algoritmul de rezolvare, un exemplu detaliat și câteva exerciții propuse.

***

## Algoritm de Rezolvare (ER)

O ecuație Riccati are forma generală:
$$x'(t) = p(t)x(t) + q(t)x^2(t) + r(t)$$
Rezolvarea generală a acestei ecuații se poate realiza doar dacă se cunoaște o soluție particulară, $x_p(t)$.

**[Pasul 1] Identificarea**
* [cite_start]Se identifică forma ecuației și funcțiile $p(t)$, $q(t)$, $r(t)$. [cite: 85]
* [cite_start]Se verifică că este dată o soluție particulară, $x_p(t)$. [cite: 85]

**[Pasul 2] Substituția**
* [cite_start]Se face schimbarea de funcție $x(t) = z(t) + x_p(t)$. [cite: 85]
* [cite_start]Se derivează această relație pentru a obține $x'(t) = z'(t) + x_p'(t)$. [cite: 85]

**[Pasul 3] Transformarea în Ecuație Bernoulli**
* [cite_start]Se înlocuiesc $x(t)$ și $x'(t)$ în ecuația inițială. [cite: 85]
* [cite_start]După înlocuire și simplificare, termenii care depind doar de $x_p$ se vor anula (deoarece $x_p$ este soluție), iar ecuația se va transforma într-o ecuație Bernoulli în $z(t)$ cu $\alpha=2$: [cite: 85]
    $$z'(t) = [p(t) + 2q(t)x_p(t)]z(t) + q(t)z^2(t)$$

**[Pasul 4] Rezolvarea Ecuației Bernoulli**
* Se rezolvă ecuația Bernoulli în $z(t)$ obținută la pasul anterior. Acest lucru se face de obicei cu o a doua substituție, de forma $u(t) = z^{-1}(t)$, care o va transforma într-o ecuație liniară.

**[Pasul 5] Determinarea Soluției Generale**
* După ce s-a găsit soluția generală pentru $z(t)$, se revine la substituția inițială pentru a scrie soluția generală a ecuației Riccati:
    $$x(t) = z(t) + x_p(t)$$

***

## Exemplu Rezolvat

[cite_start]Să se determine soluția generală a ecuației, știind că admite soluția particulară $x_p(t) = 3t$. [cite: 86]
$$x' = x^2 + \frac{x}{t} - 9t^2, \quad t > 0$$

* **Pasul 1: Identificarea**
    Ecuația este de tip Riccati cu:
    * $p(t) = \frac{1}{t}$
    * $q(t) = 1$
    * $r(t) = -9t^2$
    * Soluția particulară cunoscută este $x_p(t) = 3t$.

* **Pasul 2: Substituția**
    Fie $x(t) = z(t) + x_p(t) = z(t) + 3t$.
    Derivând, obținem $x'(t) = z'(t) + 3$.

* **Pasul 3: Transformarea în Ecuație Bernoulli**
    Înlocuim în ecuația inițială:
    $$z' + 3 = (z + 3t)^2 + \frac{z + 3t}{t} - 9t^2$$
    $$z' + 3 = z^2 + 6tz + 9t^2 + \frac{z}{t} + 3 - 9t^2$$
    Simplificăm termenii asemenea și obținem ecuația Bernoulli:
    $$z' = z^2 + 6tz + \frac{z}{t}$$
    $$z' = \left(6t + \frac{1}{t}\right)z + z^2$$

* **Pasul 4: Rezolvarea Ecuației Bernoulli**
    Aceasta este o ecuație Bernoulli cu $\alpha=2$. Împărțim la $z^2$:
    $$\frac{z'}{z^2} = \left(6t + \frac{1}{t}\right)\frac{1}{z} + 1$$
    Facem substituția $u(t) = \frac{1}{z(t)}$, deci $u'(t) = -\frac{z'(t)}{z^2}$.
    Ecuația devine liniară în $u(t)$:
    $$-u' = \left(6t + \frac{1}{t}\right)u + 1 \implies u' + \left(6t + \frac{1}{t}\right)u = -1$$
    Rezolvăm această ecuație liniară. Integrala din exponent este $\int (6t + \frac{1}{t})dt = 3t^2 + \ln t$.
    Soluția pentru $u(t)$ este:
    $$u(t) = e^{-(3t^2+\ln t)} \left(k + \int -1 \cdot e^{3t^2+\ln t} dt\right)$$
    $$u(t) = \frac{1}{t} e^{-3t^2} \left(k - \int t e^{3t^2} dt\right)$$
    Calculăm integrala rămasă: $\int t e^{3t^2} dt = \frac{1}{6}\int 6t e^{3t^2} dt = \frac{1}{6}e^{3t^2}$.
    $$u(t) = \frac{1}{t} e^{-3t^2} \left(k - \frac{1}{6}e^{3t^2}\right) = \frac{k}{t}e^{-3t^2} - \frac{1}{6t}$$
    Acum găsim $z(t)$:
    $$z(t) = \frac{1}{u(t)} = \frac{1}{\frac{k}{t}e^{-3t^2} - \frac{1}{6t}} = \frac{6t}{6ke^{-3t^2} - 1}$$

* **Pasul 5: Determinarea Soluției Generale**
    Soluția generală a ecuației Riccati este:
    $$x(t) = z(t) + x_p(t) = \frac{6t}{6ke^{-3t^2} - 1} + 3t$$

***

## Exerciții Propuse

1.  Să se rezolve ecuația $x' = x^2 - \frac{x}{t} - \frac{1}{t^2}$, știind că admite soluția particulară $x_p(t) = \frac{1}{t}$.
2.  Să se rezolve ecuația $x' = x^2 - 4x + 4$, știind că admite o soluție particulară constantă.
3.  Să se rezolve ecuația $x' = \frac{1}{t}x^2 - \frac{3}{t}x + \frac{2}{t}$, știind că admite soluția particulară $x_p(t) = 1$.
