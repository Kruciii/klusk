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
# Badanie Autokorelacji
## Test Durbina-Watsona

## Test mnożnika Lagrange'a
### Test Breuscha-Godfreya
# Badanie Homoskedastyczności
## Test Godfelda-Quandta 
## Test White'a
## Test Harveya-Godfreya
# Dobór zmiennych 
## Metoda Hellwiga
## Metoda Grafów
## Metoda macierzy wsp. korelacji

