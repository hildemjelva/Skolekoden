# Alternative algoritmer for å finne nullpunkt til en funksjon

Det finnes mange ulike algoritmer for å finne nullpunkter til en funksjon, her er noen av dem. Alle har sine styrker og svakheter.

Felles for alle løsningene er at det er nyttig å ha noe kunnskap om skjæringssetningen, som kan formuleres slik: 

> Dersom vi har en kontinuerlig funksjon _f_, og _f(a)_ og _f(b)_ har ulikt fortegn, så må det være et odde antall nullpunkter mellom a og b.

## Brute force-metoden

Dette er en metode som begynner på et sted og regner seg gjennom alle mulige verdier for f(x) i et intervall.

1. Velg et startpunkt _x_ som du tror at ligger til venstre for nullpunktet.
2. Velg et lite positivt tall _dx_ som du skal legge til _x_ for å gradvis forflytte deg bortover tallinja.
3. Regn ut _f(x)_. Husk dette tallet.
4. Lag en ny x slik: <code>_x&nbsp;= x&nbsp;+&nbsp;dx_</code>.
5. Regn ut _f(x)_ igjen, og sammenlikn med forrige utregning. 
6. Dersom fortegnet er det samme, gå tilbake til punkt 4. Dersom fortegnet er ulikt, gå til punkt 7.
7. Regn ut midtpunktet mellom de to siste x-verdiene du brukte. Dette er svaret ditt.

## Halveringsmetoden

Metode som gjentagende fjerner halvparten av gjenstående område som ikke nullpunktet finnes i.

1. Velg et tall _a_ som du tror at ligger til venstre for nullpunktet, og et tall _b_ som du tror at ligger til høyre for nullpunktet.
2. Dersom <code>_a&nbsp;-&nbsp;b_</code> er et veldig lite tall, gå til punkt 9.
3. Regn ut midtpunktet _x_ mellom _a_ og _b_: <code>_x&nbsp;=&nbsp;(a&nbsp;+&nbsp;b)&nbsp;/&nbsp;2_</code>.
4. Regn ut _f(x)_. 
5. Regn ut produktet <code>_p&nbsp;=&nbsp;f(a)&middot;f(x)_</code>.
6. Dersom verdien til _p_ er positivt, gå til punkt 7. Dersom verdien til _p_ er negativt, gå til punkt 8.
7. Gi _a_ verdien til _x_ og gå til punkt 2.
8. Gi _b_ verdien til _x_ og gå til punkt 2.
9. Den siste x-verdien du regnet ut er svaret ditt.

## Newtons metode

Metode som bruker tangenten i et punkt på funksjonen til å nærme seg et nullpunkt.

1. Velg en verdi <code>_x<sub>n</sub>_</code> som startpunkt.
2. Lag uttrykket <code>_h(x<sub>n</sub>) = f((x<sub>n</sub>)/f'((x<sub>n</sub>)_</code>.
3. Vi kan nå beregne neste tilnærming til nullpuntet med koden <code>_x<sub>n+1</sub> = x<sub>n</sub> - h(x<sub>n</sub>)_</code>.
4. Gjenta fra punkt 2 inntil ønsket nøyaktighet er oppnådd.