---
title: Ekonometria Part 2
---

# Badanie Losowości
## Test liczby serii
1. Należy uporządkować niemalejąco reszty w próbie według zmiennej porządkującej. Zmienna porządkująca jest zmienną czasową, gdy dane pochodzą z szeregów czasowych, natomiast dla danych przekrojowych jest to jedna z zmiennych objaśniających.
2. Obliczamy ilość serii czyli ciągów reszt o tym samym znaku. Oznaczamy je jako $S$
3. Z tablic testu liczby serii odczytujemy wartość $S_1^*$ oraz wartość $S_1^*$ na podstawie wartości $n_1$ oraz $n_2$ czyli ilość reszt dodatnich i reszt ujemnych oraz dla istotności $\alpha/2$ oraz $1-\alpha/2$. Jeśli $S_1^*  \lt S \lt S_2^*$ to nie ma podstaw do odrzucenia hipotezy zerowej (czyli dobry model)
# Badanie normalności
## Test Shapiro-Wilka
### Informacje
- **Lewostronny**
### Wzory
$$ W = \frac{[\sum_{i=1}^{n/2}a_{n,i} (e_e())] }{s} $$
### Hipoteza
$H_0:$ Składnik losowy modelu $y = X\beta +\epsilon$ ma rozkład normalny
$H_0:$ Składnik losowy modelu $y=X\beta+\epsilon$ nie ma rozkładu normalnego
### Procedura
1. Należy uporządkować reszty według wartości niemalejących
2. Należy obliczyć wartość statystyki $W$ 
3. Należy odczytać z tablic $W^*$ dla danej wartości $\alpha$ i $n$.
4. Test Shapiro-Wilka jest lewostronny wiec jeśli $W$<$W*$ to należy odrzucić $H_0$ na rzecz $H_1$ 
## Test Jarque'a-Bery
### Informacje
- **Prawostronny**
### Wzory
$$JB = n \left( \frac{S^2}{6} + \frac{K^2}{24} \right)$$
**Miara skośności ($S$)**
$$S = \frac{\frac{1}{n} \sum_{i=1}^{n} e_i^3}{(\frac{1}{n} \sum_{i=1}^{n} e_i^2)^{3/2}}$$
**Miara kurtozy ($K$)**: $$K = \frac{\frac{1}{n} \sum_{i=1}^{n} e_i^4}{(\frac{1}{n} \sum_{i=1}^{n} e_i^2)^{2}}$$
**Wartość krytyczna testu chi-kwadrat**( $\chi^2_*$ )
dla dwóch stopni swobody oraz $\alpha = 0,05$
### Hipoteza
$H_0:$ Składnik losowy modelu $y = X\beta +\epsilon$ ma rozkład normalny
$H_0:$ Składnik losowy modelu $y=X\beta+\epsilon$ nie ma rozkładu normalnego
### Procedura
1. Policzyć współczynnik asymetrii i kurtozę.
2. Wyznaczyć wartość statystyki JB.
3. Jeśli  $JB \gt \chi^2_*$ to hipotezę o normalności składnika losowego należy odrzucić. Natomiast jeśli $JB\le \chi^2_*$ to nie ma podstaw do odrzucenia hipotezy. Czyli jest to test prawostronny.
# Badanie Autokorelacji
## Test Durbina-Watsona

### Informacje

### Wzory
$$\mathbf{d = \frac{\sum_{i=2}^{n} (e_i - e_{i-1})^2}{\sum_{i=1}^{n} e_i^2}}$$
**Empiryczny współczynnik autokorelacji pierwszego rzędu** ($\hat{\rho}$):
$$\hat{\rho} = \frac{\sum_{i=2}^{n} e_i e_{i-1}}{\sum_{i=1}^{n} e_i^2}$$
$$d\approx 2(1-\hat{\rho})$$

### Hipoteza
1. Jeśli $\hat \rho \gt 0$ to $H_0: \rho = 0$ , $H_1: \rho \gt 0$ 
2. Jeśli $\hat \rho \lt 0$ to  $H_0: \rho = 0$ , $H_1: \rho \lt 0$ 
### Procedura
1. Oblicz $\hat \rho$ 
2. Jeśli $\hat \rho \gt 0$  to oblicz $d$ , jeśli $\hat \rho \lt 0$ to oblicz $d' = 4 - d$ 
3. Na podstawie tych przedziałów dopasuj.


|       | $d_L$ |                 | $d_U$ |       |
| ----- | ----- | --------------- | ----- | ----- |
| $H_1$ | I     | Nierozstrzający | I     | $H_0$ |

## Test mnożnika Lagrange'a

### Test Breuscha-Godfreya (Szczególny przypadek Lagrange'a)

# Badanie Homoskedastyczności
## Test Godfelda-Quandta 
### Informacje
Należy go zastosować wtedy kiedy heteroskedastyczność została spowodowana przez jedną zmienną. Jeśli została spowodowana przez kilka lepiej użyć testu White'a lub testu Harveya-Godfreya.
## Test White'a
### Hipoteza
$H_0: \sigma_i^2 = \sigma^2$  
$H_1:$ Nie wszystkie $\sigma_i^2$ są równe $\sigma^2$
### Procedura 
1. Szacujemy parametry modelu wyjściowego $y_i = \beta_0 + \beta_1 x_{1i} + \dots + \beta_k x_{ki} + \epsilon_i$.
2. Wyznaczamy kwadraty reszt modelu wyjściowego. Uznajemy je za realizację wariancji składników losowych.
3. Szacujemy parametry modelu pomocniczego.
    - W teście White'a wartościami zmiennej objaśnianej są kwadraty reszt modelu wyjściowego, a zmiennymi objaśniającymi zmienne $x_{1i}, x_{2i}, \dots, x_{ki}, x_{1i}^2, x_{2i}^2, \dots, x_{ki}^2, x_{1i} x_{2i}, x_{1i} x_{3i}, \dots, x_{li} x_{ji}$, gdzie $l = 1, 2, \dots, k$, $j \neq l$.
    - W przypadku testu Harveya-Godfreya wartościami zmiennej objaśnianej są logarytmy naturalne kwadratów reszt modelu wyjściowego, a zmiennymi objaśniającymi zmienne $x_{1i}, x_{2i}, \dots, x_{ki}$.
4. Wyznaczamy wartość statystyki $nR^2$, gdzie $n$ jest liczebnością próby, a $R^2$ współczynnikiem determinacji w modelu pomocniczym. Porównujemy $nR^2$ z wartością krytyczną testu chi-kwadrat dla poziomu istotności $\alpha$ i $p$ stopni swobody $\chi^2_{p,\alpha}$, gdzie $p$ jest liczbą zmiennych objaśniających w modelu pomocniczym.
    - W teście White'a $p = \frac{(k+1)(k+2)}{2} - 1$.
    - Dla testu Harveya-Godfreya $p = k$.
5. Jeśli $nR^2 > \chi^2_{p,\alpha}$ to odrzucamy hipotezę o homoskedastyczności, natomiast jeśli $nR^2 \leq \chi^2_{p,\alpha}$ to nie ma podstaw do odrzucenia hipotezy zerowej o homoskedastyczności.

## Test Harveya-Godfreya

# Dobór zmiennych 

## Metoda Hellwiga

## Metoda Grafów

## Metoda macierzy wsp. korelacji

