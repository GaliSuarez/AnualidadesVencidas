# AnualidadesVencidas
En este repositorio revisaremos las diferentes formulas de Anualidades vencidas 

## Valor futuro
Conociendo la anualidad, tasa de interés del periodo y el número (plazo) de anualidades.


La formula es la siguente:<br><br>


$$VF_t=A\cdot\frac{(1+r)^T\-1}{r}\$$<br>  <br>


Donde: <br>
$$A=$$ Anualidad <br>
$$r=$$ Tasa de interés del periodo <br>
$$T=$$ Plazos <br>


Aqui tenemos un ejemplo práctico para el Valor futuro
```
# Creamos objetos con valores de entrada
A=1500
i=0.05
r=0.05/12
Tp=60
# calculamos el valor futuro
VFt=ValorFuturoT(A=A,r=r,Tp=Tp)
# imprimimos el resultado
VFt
```
### Anualidades 
Para calcular el monto de la  Anualidad conociendo valor futuro, tasa del periodo y número de pagos, usamos la siguente formula, que resulta ser un despeje de la formula anterior <br><br>



$$A=\frac{VF_t}{\frac{(1+r)^T\-1}{r}}$$ <br><br>


Aqui tenemos un ejemplo practico para anualidades
```
# Creamos objetos con valores de entrada
VFt=102009.1
i=0.05
r=0.05/12
Tp=60
# calculamos el valor de la anualidad
A=Anualidad(VFt=VFt,r=r,Tp=Tp)
# imprimimos el resultado
A
```
### Plazos 
Para conocer el Número de pagos o plazo, conociendo valor futuro, número de pagos y tasa del periodo, utilizamos la siguente formula. <br><br>


$$T=\frac{log\frac{(VF_t\cdot r)}{A}\+1}{log(1+r)}$$<br><br>


Aqui tenemos un ejemplo practico para plazos
```
# Creamos objetos con valores de entrada
VFt=102009.1
i=0.05
r=0.05/12
A=1500
# calculamos el numero de plazos
Tp=Plazos(VFt=VFt,r=r,A=A)
# imprimimos el resultado
Tp
```
### Tasa del periodo
Para conocer la tasa del periodo, conociendo valor futuro, número de pagos y monto de la anualidad, utilizamos la siguente formula.<br><br>

$$\frac{VF_t}{A}=\frac{(1+r)^T-1}{r}$$<br><br>

Aqui tenemos un ejemplo practico para tasa del periodo
```
# Creamos objetos con valores de entrada
VFt=102009.1
Tp=60
A=1500
# calculamos la tasa del periodo
r=TasaPer(VFt=VFt,Tp=Tp,A=A)
# imprimimos el resultado
r
```
## Valor Actual
Conociendo la anualidad, tasa de interés del periodo y el número (plazo) de anualidades podemos obtener el valor actual


La formula es la siguente:<br><br>


$$VA_t=A\cdot\frac{1-(1+r)^-T\-1}{r}\$$<br>  <br>


Donde: <br>
$$A=$$ Anualidad <br>
$$r=$$ Tasa de interés del periodo <br>
$$T=$$ Plazos <br>


Aqui tenemos un ejemplo practico para Valor actual. (Para mis ejemplos de valor actual, y con la finalidad de distinguir de los calculos con valor final, a los nombres de las variables se les agregara un VA)
```
# Creamos objetos con valores de entrada
TpVA=48
rVA=0.12/TpVA
Ava=66.41
# calculamos el valor actual
VAt=ValorActualT(rVA=rVA,TpVA=TpVA,Ava=Ava)
# imprimimos el resultado
VAt
```
### Anualidades con Valor Actual
Para calcular el monto de la  Anualidad conociendo valor actual, tasa del periodo y número de pagos, usamos la siguente formula, que resulta ser un despeje de la formula anterior <br><br>



$$A=\frac{VA_t}{\frac{1-(1+r)^-T}{r}}$$ <br><br>


Aqui tenemos un ejemplo practico para Anualidad. (Para mis ejemplos de valor actual, y con la finalidad de distinguir de los calculos con valor final, a los nombres de las variables se les agregara un VA)
```
# Creamos objetos con valores de entrada
TpVA=48
rVA=0.12/TpVA
VAt=3000
# calculamos el valor de la anualidad
Ava=AnualidadVAt(rVA=rVA,TpVA=TpVA,VAt=VAt)
# imprimimos el resultado
Ava
```

### Plazos 
Para conocer el Número de pagos o plazo, conociendo valor futuro, número de pagos y tasa del periodo, utilizamos la siguente formula. <br><br>


$$T=\frac{-log(1-\frac{(VA_t\cdot r)})\{A}\}{log(1+r)}$$<br><br>


Aqui tenemos un ejemplo practico para Plazos. (Para mis ejemplos de valor actual, y con la finalidad de distinguir de los calculos con valor final, a los nombres de las variables se les agregara un VA)
```
# Creamos objetos con valores de entrada
rVA=0.12/48
Ava=66.41
VAt=3000
# calculamos el valor de la anualidad
TpVA=PlazosVA(rVA=rVA,VAt=VAt,Ava=Ava)
# imprimimos el resultado
TpVA
```

### Tasa del periodo
Para conocer la tasa del periodo, conociendo valor futuro, número de pagos y monto de la anualidad, utilizamos la siguente formula.<br><br>

$$\frac{VF_t}{A}=\frac{(1+r)^T-1}{r}$$<br><br>

Aqui tenemos un ejemplo practico para tasa del periodo. (Para mis ejemplos de valor actual, y con la finalidad de distinguir de los calculos con valor final, a los nombres de las variables se les agregara un VA)
```
# Creamos objetos con valores de entrada
VAt=3000
TpVA=48
Ava=66.41
# calculamos la tasa del periodo
rVA=TasaPerVA(VAt=VAt,TpVA=TpVA,Ava=Ava)
# imprimimos el resultado
rVA
```
