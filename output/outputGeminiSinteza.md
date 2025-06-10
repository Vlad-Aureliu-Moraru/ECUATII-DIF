Aceasta este o sinteză a materialelor prezentate în seminariile de ecuații diferențiale, structurată pe principalele categorii de ecuații și metode studiate.

### **1. Ecuații Diferențiale de Ordinul I**

Aceste ecuații implică funcția necunoscută și derivata sa de ordinul întâi.

#### **a) Ecuații cu Variabile Separabile (EVS)**
* [cite_start]**Forma generală**: $x'(t) = f(t) \cdot g(x)$[cite: 87].
* [cite_start]**Metoda de rezolvare**: Se separă variabilele aducând toți termenii în $x$ de o parte și toți termenii în $t$ de cealaltă parte, apoi se integrează ambele părți: $\int \frac{dx}{g(x)} = \int f(t)dt$[cite: 88].
* [cite_start]**Soluții staționare**: Se obțin prin rezolvarea ecuației $g(x) = 0$[cite: 87].

#### **b) Ecuații Omogene (EO)**
* [cite_start]**Forma generală**: Pot fi aduse la forma $x'(t) = f\left(\frac{x}{t}\right)$[cite: 95].
* [cite_start]**Metoda de rezolvare**: Se utilizează substituția $z(t) = \frac{x(t)}{t}$, din care rezultă $x(t) = t \cdot z(t)$ și $x'(t) = z(t) + t \cdot z'(t)$[cite: 95]. [cite_start]Această substituție transformă ecuația omogenă într-o ecuație cu variabile separabile în funcția $z(t)$[cite: 95].

#### **c) Ecuații Liniare (EL)**
* [cite_start]**Forma generală**: $x'(t) = p(t)x(t) + q(t)$, unde $p, q$ sunt funcții continue[cite: 73].
* **Metoda de rezolvare**: Soluția generală se poate determina direct folosind formula:
    [cite_start]$x(t) = e^{\int p(t)dt} \left( k + \int q(t)e^{-\int p(t)dt} dt \right)$, unde $k$ este o constantă reală[cite: 73].

#### **d) Ecuații Bernoulli (EB)**
* [cite_start]**Forma generală**: $x'(t) = p(t)x(t) + q(t)x^{\alpha}(t)$, cu $\alpha \in \mathbb{R} \setminus \{0, 1\}$[cite: 75].
* [cite_start]**Metoda de rezolvare**: Se împarte ecuația prin $x^\alpha$ și se face substituția $z(t) = x^{1-\alpha}(t)$[cite: 78]. [cite_start]Această substituție transformă ecuația Bernoulli într-o ecuație liniară în variabila $z(t)$ [cite: 78][cite_start], de forma $z' = (1-\alpha)p(t)z + (1-\alpha)q(t)$[cite: 76].
* [cite_start]Dacă $\alpha > 0$, ecuația admite și soluția staționară $x(t) \equiv 0$[cite: 77].

#### **e) Ecuații Riccati (ER)**
* [cite_start]**Forma generală**: $x'(t) = p(t)x(t) + q(t)x^2(t) + r(t)$[cite: 85].
* [cite_start]**Metoda de rezolvare**: Rezolvarea generală necesită cunoașterea unei soluții particulare, $x_p(t)$[cite: 85]. [cite_start]Se face substituția $x(t) = z(t) + x_p(t)$, care transformă ecuația Riccati într-o ecuație Bernoulli în $z(t)$ cu $\alpha = 2$[cite: 85].

#### **f) Ecuații Diferențiale Exacte (EDE)**
* [cite_start]**Forma generală**: $P(t,x)dt + Q(t,x)dx = 0$[cite: 59].
* [cite_start]**Condiția de exactitate**: O ecuație este exactă dacă $\frac{\partial P}{\partial x} = \frac{\partial Q}{\partial t}$[cite: 61].
* [cite_start]**Metoda de rezolvare**: Dacă ecuația este exactă, există o funcție $F(t,x)$, numită integrală primă, astfel încât $\frac{\partial F}{\partial t} = P$ și $\frac{\partial F}{\partial x} = Q$[cite: 60]. [cite_start]Soluția generală este dată în formă implicită de $F(t,x) = k$, unde $k$ este o constantă[cite: 60, 64].

---

### **2. Ecuații Liniare de Ordin Superior cu Coeficienți Constanți**

[cite_start]Soluția generală a unei ecuații neomogene este suma dintre soluția generală a ecuației omogene asociate ($x_o(t)$) și o soluție particulară a ecuației neomogene ($x_p(t)$), adică $x(t) = x_o(t) + x_p(t)$[cite: 17].

#### **a) Cazul Omogen: $a_n x^{(n)} + \dots + a_1 x' + a_0 x = 0$**
* [cite_start]**Metoda de rezolvare**: Se atașează ecuația caracteristică algebrică $a_n r^n + \dots + a_1 r + a_0 = 0$[cite: 35].
* Soluția generală se construiește pe baza rădăcinilor acestei ecuații:
    * [cite_start]**Rădăcini reale distincte ($r_1, r_2, \dots$)**: Soluția este de forma $x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t} + \dots$[cite: 35].
    * [cite_start]**Rădăcini reale cu multiplicitate ($r$ de multiplicitate $m$)**: Contribuția la soluție este $(C_1 + C_2 t + \dots + C_m t^{m-1})e^{rt}$[cite: 36, 6].
    * [cite_start]**Rădăcini complexe conjugate ($\alpha \pm i\beta$)**: Contribuția la soluție este $e^{\alpha t}(C_1 \cos(\beta t) + C_2 \sin(\beta t))$[cite: 37, 9]. [cite_start]Rădăcinile complexe cu multiplicitate $m$ urmează un model similar, cu coeficienți polinomiali de grad $m-1$[cite: 9].

#### **b) Cazul Neomogen: $a_n x^{(n)} + \dots + a_0 x = f(t)$**
Pentru a găsi o soluție particulară $x_p(t)$, se folosesc două metode principale:

* **Metoda coeficienților nedeterminați (identificării coeficienților)**
    * [cite_start]Se aplică atunci când funcția $f(t)$ este un polinom, o exponențială, o funcție sinusoidală/cosinusoidală sau combinații ale acestora[cite: 31].
    * [cite_start]Se alege o formă pentru $x_p(t)$ similară cu cea a lui $f(t)$[cite: 8].
    * [cite_start]**Regula de rezonanță**: Dacă forma aleasă pentru $x_p(t)$ conține termeni care sunt deja în soluția omogenă $x_o(t)$, atunci forma trebuie înmulțită cu $t^s$, unde $s$ este ordinul de multiplicitate al rădăcinii corespunzătoare din ecuația caracteristică[cite: 8, 24].

* **Metoda variației constantelor**
    * [cite_start]Este o metodă generală care se aplică pentru orice funcție continuă $f(t)$[cite: 12].
    * [cite_start]Dacă soluția omogenă este $x_o(t) = C_1 y_1(t) + \dots + C_n y_n(t)$, se caută o soluție particulară de forma $x_p(t) = C_1(t) y_1(t) + \dots + C_n(t) y_n(t)$[cite: 12].
    * [cite_start]Derivatele funcțiilor $C_i'(t)$ se determină prin rezolvarea unui sistem liniar specific[cite: 12, 13].

---

### **3. Teorema de Existență și Unicitate (Picard)**

* [cite_start]**Context**: Se aplică problemelor Cauchy de forma $x' = f(t,x)$, $x(t_0) = x_0$[cite: 41].
* [cite_start]**Condiții**: Dacă funcția $f(t,x)$ este continuă și Lipschitz continuă în raport cu a doua variabilă într-un domeniu dat, atunci problema Cauchy are o soluție unică pe un interval în jurul lui $t_0$[cite: 42, 43].
* [cite_start]**Metoda iterațiilor lui Picard**: Teorema oferă o metodă constructivă de a aproxima soluția printr-un șir de funcții[cite: 43].
    * [cite_start]Se pornește de la $x_0(t) = x_0$[cite: 44].
    * [cite_start]Șirul se construiește recursiv cu formula: $x_n(t) = x_0 + \int_{t_0}^{t} f(s, x_{n-1}(s))ds$[cite: 45].

---

### **4. Aplicații: Dinamica Populațiilor**

* **Modelul exponențial (Malthus)**: Descrie creșterea unei populații fără constrângeri de mediu.
    * [cite_start]**Ecuația**: $\frac{dN}{dt} = rN$, unde $r$ este rata de creștere[cite: 104].
    * [cite_start]**Soluția**: $N(t) = N_0 e^{r(t-t_0)}$, unde $N_0$ este populația la momentul inițial $t_0$[cite: 104].

* **Modelul logistic (Verhulst)**: Descrie creșterea unei populații într-un mediu cu resurse limitate.
    * [cite_start]**Ecuația**: $\frac{dN}{dt} = rN\left(1 - \frac{N}{K}\right)$, unde $K$ este capacitatea mediului (carrying capacity)[cite: 105].
    * [cite_start]**Soluția**: $N(t) = \frac{K}{1 + Ae^{-rt}}$, unde $A = \frac{K-N_0}{N_0}$[cite: 108]. [cite_start]Populația tinde asimptotic către capacitatea mediului, $K$[cite: 108].
    * [cite_start]**Puncte de echilibru**: $N=0$ (instabil) și $N=K$ (stabil)[cite: 106, 109].
