### **Algoritm Generalizat pentru Rezolvarea Ecuațiilor Diferențiale**

---

#### **1. Ecuații Diferențiale Separabile**  
**Forma generală:**  
\[ \frac{dx}{dt} = f(t) \cdot g(x) \]  

**Pași de rezolvare:**  
1. **Separarea variabilelor:**  
   - Mutăm toți termenii în \( x \) într-o parte și toți termenii în \( t \) în cealaltă parte.  
   - Exemplu:  
     \[ \frac{dx}{g(x)} = f(t) \, dt \]  

2. **Integrarea ambelor părți:**  
   - Integrăm fiecare parte în raport cu variabila corespunzătoare.  
   - Exemplu:  
     \[ \int \frac{1}{g(x)} \, dx = \int f(t) \, dt + C \]  

3. **Rezolvarea pentru \( x(t) \):**  
   - Exprimăm soluția explicit sau implicit.  
   - Exemplu:  
     \[ \ln|x| = t^2 + C \implies x(t) = Ce^{t^2} \]  

---

#### **2. Ecuații Liniare de Ordinul Întâi**  
**Forma generală:**  
\[ \frac{dx}{dt} + p(t)x = q(t) \]  

**Pași de rezolvare:**  
1. **Calculul factorului integrant:**  
   - Calculăm \( \mu(t) = e^{\int p(t) \, dt} \).  
   - Exemplu:  
     \[ \mu(t) = e^{\int 2t \, dt} = e^{t^2} \]  

2. **Înmulțirea ecuației cu factorul integrant:**  
   - Exemplu:  
     \[ e^{t^2} \frac{dx}{dt} + 2te^{t^2}x = te^{t^2} \]  

3. **Integrarea ecuației:**  
   - Exemplu:  
     \[ x(t) = \frac{1}{e^{t^2}} \left( \int te^{t^2} \, dt + C \right) = \frac{1}{2} + Ce^{-t^2} \]  

---

#### **3. Ecuații Omogene (de tip \( \frac{dx}{dt} = f\left(\frac{x}{t}\right) \))**  
**Pași de rezolvare:**  
1. **Substituția \( z = \frac{x}{t} \):**  
   - Exemplu:  
     \[ \frac{dx}{dt} = z + t \frac{dz}{dt} \]  

2. **Separarea variabilelor:**  
   - Exemplu:  
     \[ \int \frac{dz}{f(z) - z} = \int \frac{dt}{t} \]  

3. **Revenirea la variabila inițială:**  
   - Exemplu:  
     \[ x(t) = t \cdot z(t) \]  

---

#### **4. Ecuații Exacte**  
**Forma generală:**  
\[ P(t, x) \, dt + Q(t, x) \, dx = 0 \]  

**Pași de rezolvare:**  
1. **Verificarea condiției de exactitate:**  
   - Exemplu:  
     \[ \frac{\partial P}{\partial x} = \frac{\partial Q}{\partial t} \]  

2. **Calculul potențialului \( F(t, x) \):**  
   - Exemplu:  
     \[ F(t, x) = \int P(t, x) \, dt + C(x) \]  

3. **Determinarea constantei \( C(x) \):**  
   - Exemplu:  
     \[ \frac{\partial F}{\partial x} = Q(t, x) \]  

4. **Soluția implicită:**  
   - Exemplu:  
     \[ F(t, x) = C \]  

---

#### **5. Ecuații Liniare de Ordin Superior cu Coeficienți Constanți**  
**Forma generală:**  
\[ a_n x^{(n)} + \dots + a_0 x = f(t) \]  

**Pași de rezolvare:**  
1. **Soluția ecuației omogene:**  
   - Rezolvăm ecuația caracteristică.  
   - Exemplu:  
     \[ r^2 + 4 = 0 \implies r = \pm 2i \]  
     \[ x_0(t) = C_1 \cos(2t) + C_2 \sin(2t) \]  

2. **Determinarea soluției particulare:**  
   - Metoda coeficienților nedeterminați sau variația constantelor.  
   - Exemplu:  
     \[ x_p(t) = A \sin t + B \cos t \]  

3. **Soluția generală:**  
   - Exemplu:  
     \[ x(t) = x_0(t) + x_p(t) \]  

---

#### **6. Probleme Cauchy**  
**Pași de rezolvare:**  
1. **Rezolvarea ecuației diferențiale.**  
2. **Aplicarea condițiilor inițiale pentru determinarea constantelor.**  
   - Exemplu:  
     \[ x(0) = 1 \implies C_1 = 1 \]  

---

### **Exemplu Integrat**  
**Ecuație:**  
\[ \frac{dx}{dt} = kx \left(1 - \frac{x}{N}\right), \quad x(0) = x_0 \]  

**Pași:**  
1. Separare:  
   \[ \int \frac{dx}{x(N - x)} = \int \frac{k}{N} \, dt \]  
2. Integrare:  
   \[ \ln\left|\frac{x}{N - x}\right| = kt + C \]  
3. Soluție:  
   \[ x(t) = \frac{N}{1 + \left(\frac{N - x_0}{x_0}\right)e^{-kt}} \]  

Acest algoritm acoperă majoritatea tipurilor de ecuații diferențiale întâlnite în seminarii. Adaptați pașii în funcție de specificul fiecărei probleme!
