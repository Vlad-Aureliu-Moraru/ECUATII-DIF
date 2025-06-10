Sigur, iată o prezentare detaliată pentru ecuațiile de tip Bernoulli (EB), incluzând algoritmul de rezolvare, un exemplu complet și exerciții pentru practică.

***

## Algoritm de Rezolvare (EB)

O ecuație Bernoulli are forma generală:
$$x'(t) = p(t)x(t) + q(t)x^{\alpha}(t)$$
unde $\alpha$ este un număr real, $\alpha \neq 0$ și $\alpha \neq 1$.

**[Pasul 1] Identificarea**
* Se identifică funcțiile $p(t)$, $q(t)$ și exponentul $\alpha$.
* [cite_start]Dacă $\alpha > 0$, se notează soluția staționară (trivială) **$x(t) \equiv 0$**[cite: 77].

**[Pasul 2] Transformarea Ecuației**
* [cite_start]Se împarte întreaga ecuație prin $x^{\alpha}(t)$, presupunând că $x(t) \neq 0$[cite: 76]:
    $$\frac{x'(t)}{x^{\alpha}(t)} = p(t)x^{1-\alpha}(t) + q(t)$$

**[Pasul 3] Substituția**
* [cite_start]Se face schimbarea de funcție $z(t) = x^{1-\alpha}(t)$[cite: 78].
* [cite_start]Se calculează derivata noii funcții: $z'(t) = (1-\alpha)x^{-\alpha}(t)x'(t)$, de unde rezultă $\frac{x'(t)}{x^{\alpha}(t)} = \frac{z'(t)}{1-\alpha}$[cite: 76].

**[Pasul 4] Rezolvarea Ecuației Liniare**
* [cite_start]Se înlocuiesc expresiile de la Pasul 3 în ecuația transformată de la Pasul 2. Se obține o **ecuație liniară** în $z(t)$[cite: 76]:
    $$\frac{z'(t)}{1-\alpha} = p(t)z(t) + q(t)$$
    care se rescrie ca:
    $$z'(t) = (1-\alpha)p(t)z(t) + (1-\alpha)q(t)$$
* Se rezolvă această ecuație liniară pentru a determina $z(t)$.

**[Pasul 5] Determinarea Soluției Generale**
* După găsirea funcției $z(t)$, se revine la substituția inițială pentru a determina soluția generală a ecuației Bernoulli:
    $$x(t) = [z(t)]^{\frac{1}{1-\alpha}}$$

***

## Exemplu Rezolvat

Să se determine soluțiile ecuației diferențiale:
$$tx' = -x - t^5e^t x^3, \quad t \neq 0$$

* **Pasul 1: Identificarea**
    [cite_start]Rescriem ecuația în forma standard: $x' = -\frac{1}{t}x - t^4e^t x^3$[cite: 78].
    Este o ecuație Bernoulli cu:
    * $p(t) = -\frac{1}{t}$
    * $q(t) = -t^4e^t$
    * $\alpha = 3$
    [cite_start]Deoarece $\alpha=3 > 0$, ecuația admite soluția staționară $x(t) \equiv 0$[cite: 78].

* **Pasul 2: Transformarea Ecuației**
    Pentru $x \neq 0$, împărțim ecuația la $x^3$:
    [cite_start]$$\frac{x'}{x^3} = -\frac{1}{t}x^{-2} - t^4e^t$$ [cite: 79]

* **Pasul 3: Substituția**
    Avem $1-\alpha = 1-3 = -2$. [cite_start]Facem substituția $z(t) = x^{-2}(t)$[cite: 79].
    [cite_start]Derivata este $z'(t) = -2x^{-3}(t)x'(t)$, de unde $\frac{x'}{x^3} = -\frac{z'}{2}$[cite: 79].

* **Pasul 4: Rezolvarea Ecuației Liniare**
    Înlocuim în ecuația transformată:
    [cite_start]$$-\frac{z'}{2} = -\frac{1}{t}z - t^4e^t$$ [cite: 79]
    Înmulțim cu -2 pentru a obține ecuația liniară în $z(t)$:
    [cite_start]$$z'(t) = \frac{2}{t}z(t) + 2t^4e^t$$ [cite: 80]
    Rezolvăm această ecuație liniară. Factorul integrant este $e^{\int \frac{2}{t}dt} = e^{2\ln|t|} = t^2$.
    [cite_start]$$z(t) = t^2 \left(k + \int 2t^4e^t \cdot \frac{1}{t^2} dt\right) = t^2 \left(k + \int 2t^2e^t dt\right)$$ [cite: 80]
    Integrala se calculează prin părți de două ori și rezultă $\int 2t^2e^t dt = 2e^t(t^2 - 2t + 2)$.
    Astfel, soluția pentru $z(t)$ este:
    $$z(t) = t^2(k + 2e^t(t^2 - 2t + 2))$$

* **Pasul 5: Determinarea Soluției Generale**
    Revenim la substituția $z = x^{-2} \implies x^2 = 1/z \implies x = \pm 1/\sqrt{z}$.
    Soluția generală a ecuației Bernoulli este:
    [cite_start]$$x(t) = \pm \frac{1}{\sqrt{t^2(k + 2e^t(t^2 - 2t + 2))}} = \pm \frac{1}{|t|\sqrt{k + 2e^t(t^2 - 2t + 2)}}$$ [cite: 80]

***

## Exerciții Propuse

1.  Să se determine soluția generală a ecuației $x' - \frac{x}{2t} = t x^3$.
2.  Să se rezolve problema cu valoare inițială:
    $$\begin{cases} x' + x = tx^2 \\ x(0) = 2 \end{cases}$$
3.  Să se găsească soluțiile ecuației $x' + x \cos t = x^2 \cos t$.
