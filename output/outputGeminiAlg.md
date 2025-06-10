
### **1. Ecuații cu Variabile Separabile (EVS)**
[cite_start]Acestea sunt ecuații de forma $x'(t) = f(t) \cdot g(x)$. [cite: 87]

**[Pasul 1]**
* **Explicație:** Se identifică funcțiile $f(t)$ și $g(x)$. Se caută soluțiile staționare (de echilibru) rezolvând ecuația $g(x) = 0$. [cite_start]Acestea sunt soluții constante ale ecuației. [cite: 87]
* [cite_start]**Exemplu:** Pentru ecuația $(t^2-1)x' = -2tx^2$, avem $x' = \left(\frac{-2t}{t^2-1}\right) \cdot x^2$. [cite: 94] Aici, $f(t) = \frac{-2t}{t^2-1}$ și $g(x) = x^2$. [cite_start]Soluția staționară se obține din $g(x)=x^2=0$, adică $x(t) = 0$. [cite: 94]

**[Pasul 2]**
* **Explicație:** Pentru $g(x) \neq 0$, se separă variabilele. [cite_start]Termenii cu $x$ se trec în partea stângă, alături de $dx$, iar termenii cu $t$ în partea dreaptă, alături de $dt$. [cite: 88]
* **Exemplu:** Pentru aceeași ecuație, $\frac{dx}{dt} = \frac{-2t}{t^2-1}x^2$. [cite_start]Separând variabilele obținem $\frac{dx}{x^2} = -\frac{2t}{t^2-1}dt$. [cite: 94]

**[Pasul 3]**
* [cite_start]**Explicație:** Se integrează ambele părți ale ecuației pentru a obține soluția generală, de obicei sub formă implicită. [cite: 88]
* **Exemplu:** $\int \frac{1}{x^2}dx = \int -\frac{2t}{t^2-1}dt$. Integrând, obținem $-\frac{1}{x} = -\ln|t^2-1| + C$, sau $\frac{1}{x} = \ln|t^2-1| + C'$, de unde rezultă soluția generală $x(t) = \frac{1}{\ln|t^2-1| + [cite_start]C'}$. [cite: 94]

---

### **2. Ecuații Omogene (EO)**
[cite_start]Acestea sunt ecuații care pot fi aduse la forma $x'(t) = f\left(\frac{x}{t}\right)$. [cite: 95]

**[Pasul 1]**
* **Explicație:** Se face schimbarea de funcție $z(t) = \frac{x(t)}{t}$. [cite_start]Din aceasta rezultă $x(t) = t \cdot z(t)$ și, prin derivare, $x'(t) = z(t) + t \cdot z'(t)$. [cite: 95]
* [cite_start]**Exemplu:** Pentru $tx' = x - te^{x/t}$, împărțind la $t \neq 0$, obținem $x' = \frac{x}{t} - e^{x/t}$. [cite: 97] [cite_start]Se substituie $z = x/t$ și $x' = z + tz'$, rezultând $z + tz' = z - e^z$. [cite: 97]

**[Pasul 2]**
* **Explicație:** Se simplifică ecuația obținută. [cite_start]Aceasta va deveni o ecuație cu variabile separabile în noua funcție $z(t)$. [cite: 95]
* [cite_start]**Exemplu:** După simplificare, obținem $tz' = -e^z$, sau $t\frac{dz}{dt} = -e^z$. [cite: 97]

**[Pasul 3]**
* **Explicație:** Se rezolvă ecuația cu variabile separabile pentru a-l găsi pe $z(t)$.
* [cite_start]**Exemplu:** Separăm variabilele: $\frac{dz}{e^z} = -\frac{dt}{t}$. [cite: 97] Integrând, $\int e^{-z}dz = -\int \frac{1}{t}dt$, de unde rezultă $-e^{-z} = -\ln|t| - C$, adică $e^{-z} = \ln|t| + [cite_start]C$. [cite: 97]

**[Pasul 4]**
* **Explicație:** Se revine la funcția inițială $x(t)$ folosind relația $x(t) = t \cdot z(t)$.
* **Exemplu:** Din $e^{-z} = \ln|t| + C$, avem $-z = \ln(\ln|t|+C)$, deci $z(t) = -\ln(\ln|t|+C)$. Soluția finală este $x(t) = -t \ln(\ln|t|+C)$.

---

### **3. Ecuații Liniare de Ordinul I (EL)**
[cite_start]Sunt ecuații de forma $x'(t) = p(t)x(t) + q(t)$. [cite: 73]

**[Pasul 1]**
* **Explicație:** Se identifică funcțiile $p(t)$ și $q(t)$.
* **Exemplu:** Pentru ecuația $x' + x \cdot \text{tg}(t) = \frac{1}{\cos(t)}$, avem $x' = -\text{tg}(t) \cdot x + \frac{1}{\cos(t)}$. [cite_start]Deci, $p(t) = -\text{tg}(t)$ și $q(t) = \frac{1}{\cos(t)}$. [cite: 74]

**[Pasul 2]**
* **Explicație:** Se aplică direct formula de rezolvare pentru soluția generală:
    [cite_start]$x(t) = e^{\int p(t)dt} \left( k + \int q(t)e^{-\int p(t)dt} dt \right)$. [cite: 73]
* [cite_start]**Exemplu:** Mai întâi calculăm integrala din exponențială: $\int p(t)dt = \int -\text{tg}(t)dt = \ln|\cos(t)|$. [cite: 74]
    [cite_start]Soluția este $x(t) = e^{\ln|\cos t|} \left( k + \int \frac{1}{\cos t} e^{-\ln|\cos t|} dt \right)$. [cite: 74]
    [cite_start]Presupunând $\cos(t)>0$, obținem $x(t) = \cos(t) \left( k + \int \frac{1}{\cos t} \frac{1}{\cos t} dt \right) = \cos(t)(k + \text{tg}(t))$. [cite: 74]

---

### **4. Ecuații Bernoulli (EB)**
[cite_start]Au forma $x'(t) = p(t)x(t) + q(t)x^{\alpha}(t)$, unde $\alpha \in \mathbb{R} \setminus \{0, 1\}$. [cite: 75]

**[Pasul 1]**
* **Explicație:** Se identifică $p(t)$, $q(t)$ și $\alpha$. [cite_start]Dacă $\alpha > 0$, se notează soluția staționară $x(t) \equiv 0$. [cite: 76, 78]
* [cite_start]**Exemplu:** Pentru $tx' = -x - t^5e^t x^3$, o rescriem ca $x' = -\frac{1}{t}x - t^4e^t x^3$. [cite: 78] Avem $p(t)=-\frac{1}{t}$, $q(t)=-t^4e^t$ și $\alpha=3$. [cite_start]Soluția staționară este $x(t)=0$. [cite: 78]

**[Pasul 2]**
* **Explicație:** Se împarte ecuația la $x^{\alpha}$ și se face substituția $z(t) = x^{1-\alpha}(t)$. [cite_start]Derivând substituția, obținem $z' = (1-\alpha)x^{-\alpha}x'$. [cite: 76]
* [cite_start]**Exemplu:** Împărțim la $x^3$: $\frac{x'}{x^3} = -\frac{1}{t}x^{-2} - t^4e^t$. [cite: 79] Facem substituția $z = x^{1-3} = x^{-2}$. [cite_start]Atunci $z' = -2x^{-3}x'$, deci $\frac{x'}{x^3} = -\frac{z'}{2}$. [cite: 79]

**[Pasul 3]**
* [cite_start]**Explicație:** Se înlocuiește în ecuație, obținând o ecuație liniară în $z(t)$: $z' = (1-\alpha)p(t)z + (1-\alpha)q(t)$. [cite: 76]
* [cite_start]**Exemplu:** Înlocuind, avem $-\frac{z'}{2} = -\frac{1}{t}z - t^4e^t$. [cite: 79] [cite_start]Înmulțind cu -2, obținem ecuația liniară: $z' = \frac{2}{t}z + 2t^4e^t$. [cite: 80]

**[Pasul 4]**
* **Explicație:** Se rezolvă ecuația liniară pentru a-l afla pe $z(t)$, apoi se revine la $x(t)$ prin $x(t) = z(t)^{\frac{1}{1-\alpha}}$.
* [cite_start]**Exemplu:** Rezolvând ecuația liniară în $z$ (vezi secțiunea 3), obținem $z(t) = t^2(k + 2t^2e^t - 4te^t + 4e^t)$. [cite: 80] [cite_start]Cum $z=x^{-2}$, soluția finală este $x(t) = \pm \frac{1}{\sqrt{z(t)}} = \pm \frac{1}{t\sqrt{k + 2t^2e^t - 4te^t + 4e^t}}$. [cite: 80]

---

### **5. Ecuații Exacte (EDE)**
[cite_start]Sunt ecuații de forma $P(t, x)dt + Q(t, x)dx = 0$. [cite: 59]

**[Pasul 1]**
* [cite_start]**Explicație:** Se identifică funcțiile $P(t, x)$ și $Q(t, x)$ și se verifică condiția de exactitate: $\frac{\partial P}{\partial x} = \frac{\partial Q}{\partial t}$. [cite: 61]
* [cite_start]**Exemplu:** Pentru $(8tx - 5x^2)dt + (4t^2 - 10tx)dx = 0$, avem $P = 8tx - 5x^2$ și $Q = 4t^2 - 10tx$. [cite: 62]
    Calculăm derivatele: $\frac{\partial P}{\partial x} = 8t - 10x$ și $\frac{\partial Q}{\partial t} = 8t - 10x$. [cite_start]Condiția este îndeplinită, deci ecuația este exactă. [cite: 63]

**[Pasul 2]**
* [cite_start]**Explicație:** Dacă ecuația este exactă, există o funcție $F(t, x)$ (numită integrală primă) astfel încât $\frac{\partial F}{\partial t} = P$ și $\frac{\partial F}{\partial x} = Q$. [cite: 60] Pentru a o găsi, integrăm $P$ în raport cu $t$.
* [cite_start]**Exemplu:** $F(t, x) = \int P(t, x)dt = \int (8tx - 5x^2)dt = 4t^2x - 5tx^2 + C(x)$, unde $C(x)$ este o "constantă" de integrare care poate depinde de $x$. [cite: 63]

**[Pasul 3]**
* **Explicație:** Se derivează expresia lui $F$ obținută la pasul anterior în raport cu $x$ și se egalează cu $Q$ pentru a determina $C(x)$.
* **Exemplu:** $\frac{\partial F}{\partial x} = \frac{\partial}{\partial x}(4t^2x - 5tx^2 + C(x)) = 4t^2 - 10tx + C'(x)$.
    [cite_start]Egalăm cu $Q$: $4t^2 - 10tx + C'(x) = 4t^2 - 10tx$. [cite: 63] [cite_start]Rezultă $C'(x) = 0$, deci $C(x)$ este o constantă reală (putem alege $C(x)=0$). [cite: 63]

**[Pasul 4]**
* **Explicație:** Soluția generală a ecuației este dată implicit de relația $F(t, x) = k$, unde $k$ este o constantă.
* **Exemplu:** $F(t, x) = 4t^2x - 5tx^2$. [cite_start]Soluția generală este $4t^2x - 5tx^2 = k$. [cite: 64]

---

### **6. Ecuații Liniare de Ordin Superior cu Coeficienți Constanți**

#### **Partea A: Cazul Omogen**
Ecuații de forma $a_n x^{(n)} + a_{n-1}x^{(n-1)} + \dots + a_1 x' + a_0 x = 0$.

**[Pasul 1]**
* [cite_start]**Explicație:** Se scrie și se rezolvă ecuația algebrică caracteristică: $a_n r^n + a_{n-1}r^{n-1} + \dots + a_1 r + a_0 = 0$. [cite: 35]
* [cite_start]**Exemplu:** Pentru $x^{(3)} - 3x'' + 3x' - x = 0$, ecuația caracteristică este $r^3 - 3r^2 + 3r - 1 = 0$, care este $(r-1)^3 = 0$. [cite: 6]

**[Pasul 2]**
* **Explicație:** Se construiește soluția generală $x_o(t)$ ca o combinație liniară de funcții, pe baza rădăcinilor ecuației caracteristice.
    * [cite_start]Pentru o rădăcină reală **simplă** $r$, termenul este $C e^{rt}$. [cite: 35]
    * [cite_start]Pentru o rădăcină reală $r$ de **multiplicitate** $m$, termenii sunt $(C_1 + C_2t + \dots + C_m t^{m-1})e^{rt}$. [cite: 7, 36]
    * [cite_start]Pentru o pereche de rădăcini complexe **simple** $\alpha \pm i\beta$, termenii sunt $e^{\alpha t}(C_1 \cos(\beta t) + C_2 \sin(\beta t))$. [cite: 37]
    * [cite_start]Pentru o pereche de rădăcini complexe $\alpha \pm i\beta$ de **multiplicitate** $m$, termenii sunt $e^{\alpha t}[(C_1 + \dots) \cos(\beta t) + (D_1 + \dots) \sin(\beta t)]$. [cite: 9, 10]
* **Exemplu:** Rădăcina este $r_1 = r_2 = r_3 = 1$ (multiplicitate 3). [cite_start]Soluția generală a ecuației omogene este $x_o(t) = C_1e^t + C_2te^t + C_3t^2e^t$. [cite: 8]

#### **Partea B: Cazul Neomogen**
Ecuații de forma $a_n x^{(n)} + \dots + a_0 x = f(t)$. [cite_start]Soluția generală este $x(t) = x_o(t) + x_p(t)$. [cite: 17]

**[Pasul 1]**
* **Explicație:** Se determină soluția generală a ecuației omogene asociate, $x_o(t)$, conform pașilor de la Partea A.
* [cite_start]**Exemplu:** Pentru $x^{(3)} - 3x'' + 3x' - x = t + e^t$, am găsit deja $x_o(t) = C_1e^t + C_2te^t + C_3t^2e^t$. [cite: 6, 8]

**[Pasul 2]**
* **Explicație:** Se caută o soluție particulară $x_p(t)$ a ecuației neomogene. Se folosește una din cele două metode:
    * [cite_start]**Metoda coeficienților nedeterminați:** Se folosește când $f(t)$ este un polinom, exponențială, funcție trigonometrică (sin, cos) sau combinații ale acestora. [cite: 17, 31] Se alege $x_p(t)$ de o formă similară cu $f(t)$. [cite_start]**Atenție:** Dacă un termen din forma aleasă pentru $x_p(t)$ apare deja în soluția omogenă $x_o(t)$ (cu multiplicitatea $m$), atunci se înmulțește acel termen cu $t^m$. [cite: 8]
    * [cite_start]**Metoda variației constantelor:** Se poate aplica pentru orice funcție continuă $f(t)$. [cite: 12] [cite_start]Se caută o soluție de forma $x_p(t) = C_1(t)y_1(t) + \dots + C_n(t)y_n(t)$, unde $y_i$ sunt soluțiile de bază din $x_o(t)$, iar funcțiile $C_i(t)$ se determină dintr-un sistem de ecuații. [cite: 12]
* **Exemplu (Coeficienți nedeterminați):** $f(t) = t + e^t$.
    * Pentru termenul $t$, am alege $At+B$. Deoarece $1$ (constanta) și $t$ nu sunt în $x_o(t)$, forma rămâne $At+B$.
    * Pentru termenul $e^t$, am alege $Ce^t$. Dar $e^t, te^t, t^2e^t$ sunt deja în $x_o(t)$. [cite_start]Rădăcina $r=1$ are multiplicitate 3. Prin urmare, trebuie să înmulțim cu $t^3$, deci forma corectă este $Ct^3e^t$. [cite: 8]
    * [cite_start]Forma totală a soluției particulare este $x_p(t) = At + B + Ct^3e^t$. [cite: 8]

**[Pasul 3]**
* **Explicație:** Se derivează $x_p(t)$ de câte ori este necesar, se introduce în ecuația neomogenă și se identifică coeficienții (A, B, C, etc.).
* [cite_start]**Exemplu:** Introducând $x_p(t)$ și derivatele sale în ecuație, se găsește $A=-1$, $B=0$, $C=1/6$. [cite: 8] [cite_start]Deci, $x_p(t) = -t + \frac{t^3e^t}{6}$. [cite: 8]

**[Pasul 4]**
* **Explicație:** Se scrie soluția generală finală ca sumă: $x(t) = x_o(t) + x_p(t)$.
* [cite_start]**Exemplu:** $x(t) = C_1e^t + C_2te^t + C_3t^2e^t - t + \frac{t^3e^t}{6}$. [cite: 8]
