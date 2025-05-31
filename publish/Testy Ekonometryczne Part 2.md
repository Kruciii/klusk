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


|     |   $d_L$  |       | $d_U$    |     |
| --- | --- | --- | --- | --- |
|  $H_0$   |   I  | Nierozstrzający    |  I   | $H_1$    |

## Test mnożnika Lagrange'a

### Test Breuscha-Godfreya (Szczególny przypadek Lagrange'a)

# Badanie Homoskedastyczności
## Test Godfelda-Quandta 

## Test White'a

## Test Harveya-Godfreya

# Dobór zmiennych 

## Metoda Hellwiga

## Metoda Grafów

## Metoda macierzy wsp. korelacji

