# Contenuti didattici

6 pianeti con 3 problemi ciascuno: in tutto 12 esercizi di codice e 6 quiz. Ogni pianeta introduce **un solo concetto nuovo**.

| # | Pianeta | Argomento | Pezzo del razzo |
|---|---|---|---|
| 1 | Printia | `print` e testo | l'antenna |
| 2 | Variabilon | variabili | il computer di bordo |
| 3 | Calcolus | fare i conti | il motore |
| 4 | Inputera | `input`: fare domande | il pannello di controllo |
| 5 | Bivio Prime | `if` ed `else`: scegliere | il navigatore |
| 6 | Loopiter | cicli `for` e sfida finale | la chiave di accensione |

Legenda: 💻 = esercizio di codice, ❓ = quiz. Le "prove" sono gli input con cui la consegna viene verificata.

---

## 1 · Printia: `print` e testo

**Obiettivo:** far stampare del testo e capire che ogni `print` scrive una riga nuova.

| | Problema | Cosa si chiede | Verifica |
|---|---|---|---|
| 💻 | Ciao, mondo! | Stampare `Ciao, mondo!` | Output esatto |
| ❓ | Cosa appare? | `print("Ciao", "Pyto")` → **Ciao Pyto** | La virgola aggiunge uno spazio |
| 💻 | Due righe | Stampare `Mi chiamo Pyto` e sotto `Sono un robot` | Output esatto su 2 righe |

## 2 · Variabilon: variabili

**Obiettivo:** mettere un valore in una variabile con `=` e usarlo al posto del valore.

| | Problema | Cosa si chiede | Verifica |
|---|---|---|---|
| 💻 | La scatola del nome | Con `nome = "Pyto"`, stampare `Ciao Pyto` usando la variabile | Output e uso di `nome` dentro `print` |
| ❓ | La scatola cambia | `punti = 5`, `punti = punti + 1` → **6** | |
| 💻 | Il compleanno | Con `anni = 11`, creare `nuovi_anni = anni + 1` e stamparla | Output `12` e controllo che `nuovi_anni == 12` |

## 3 · Calcolus: fare i conti

**Obiettivo:** usare `+ - * /` e la divisione intera `//`, e rispettare la precedenza delle operazioni.

| | Problema | Cosa si chiede | Verifica |
|---|---|---|---|
| 💻 | La calcolatrice | Con `a = 12` e `b = 5`, `somma = a + b`, stampare `Totale: 17` | Output e `somma == 17` |
| ❓ | Chi va prima? | `print(2 + 3 * 4)` → **14** | |
| 💻 | Dividere le caramelle | 20 caramelle tra 4 amici con `//`, stampare `Ognuno riceve 5 caramelle` | Output, uso di `//` e `ognuno == 5` |

## 4 · Inputera: `input`

**Obiettivo:** chiedere dati all'utente e capire che `input()` restituisce sempre **testo**, da convertire con `int()`.

| | Problema | Cosa si chiede | Prove |
|---|---|---|---|
| 💻 | Come ti chiami? | Chiedere il nome e stampare `Ciao <nome>` | `Luca`, `Sara` |
| ❓ | Testo o numero? | `"2" + "3"` → **23** | |
| 💻 | Il doppio | Leggere un numero e stampare `Il doppio è <n*2>` | `7` → 14, `10` → 20 |

## 5 · Bivio Prime: `if` ed `else`

**Obiettivo:** scrivere una condizione, rientrare le righe di 4 spazi e distinguere `=` da `==`.

| | Problema | Cosa si chiede | Prove |
|---|---|---|---|
| 💻 | Grande o piccolo? | Se il numero è maggiore di 10 stampare `Grande`, altrimenti `Piccolo` | `15`, `3`, `10` (il caso limite) |
| ❓ | Quale strada? | `x = 4`, `if x > 5` → **Sinistra** | |
| 💻 | La parola segreta | Se la parola è `pyto` stampare `Porta aperta`, altrimenti `Porta chiusa` | `pyto`, `ciao` |

## 6 · Loopiter: cicli `for` (sfida finale)

**Obiettivo:** ripetere istruzioni con `for` e `range`, e usare la variabile del ciclo.

| | Problema | Cosa si chiede | Verifica |
|---|---|---|---|
| 💻 | Conta fino a 5 | Stampare i numeri da 1 a 5 | Output e uso di `for` |
| ❓ | Quante volte? | `for i in range(3)` → **3 volte** | |
| 💻 | Sfida finale: la tabellina | Stampare la tabellina del 5 da `5 x 1 = 5` a `5 x 10 = 50` (150 XP) | Output e uso di `for` |

---

## Soluzioni

Una soluzione possibile per ogni esercizio di codice. Nel gioco si vedono dopo 3 consegne sbagliate o in modalità docente.

```python
# 1.1 Ciao, mondo!
print("Ciao, mondo!")

# 1.3 Due righe
print("Mi chiamo Pyto")
print("Sono un robot")

# 2.1 La scatola del nome
nome = "Pyto"
print("Ciao", nome)

# 2.3 Il compleanno
anni = 11
nuovi_anni = anni + 1
print(nuovi_anni)

# 3.1 La calcolatrice
a = 12
b = 5
somma = a + b
print("Totale:", somma)

# 3.3 Dividere le caramelle
caramelle = 20
amici = 4
ognuno = caramelle // amici
print("Ognuno riceve", ognuno, "caramelle")

# 4.1 Come ti chiami?
nome = input("Come ti chiami? ")
print("Ciao", nome)

# 4.3 Il doppio
numero = int(input("Scrivi un numero: "))
print("Il doppio è", numero * 2)

# 5.1 Grande o piccolo?
numero = int(input("Numero: "))
if numero > 10:
    print("Grande")
else:
    print("Piccolo")

# 5.3 La parola segreta
parola = input("Parola segreta: ")
if parola == "pyto":
    print("Porta aperta")
else:
    print("Porta chiusa")

# 6.1 Conta fino a 5
for i in range(1, 6):
    print(i)

# 6.3 Sfida finale: la tabellina
for i in range(1, 11):
    print(5, "x", i, "=", 5 * i)
```

## Esempi del Laboratorio

| Esempio | Cosa mostra | Argomenti |
|---|---|---|
| Tabellina | La tabellina di un numero scelto dall'utente | `input`, `for`, f-string |
| Lancia il dado | Lanci casuali di un dado | `import random`, `randint` |
| Giochi con le stringhe | Maiuscolo, al contrario, lettere e parole | `upper()`, `[::-1]`, `len()`, `split()` |
| Rubrica | Cercare un numero di telefono | dizionari, `in`, `if/else` |

Gli ultimi tre esempi vanno **oltre** i contenuti dei 6 pianeti: sono utili come approfondimento per chi finisce prima.
