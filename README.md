# KodeDay
## Crea un DataFrame De StarWars con Pandas


### Herramientas utilizadas

* Jupyter Notebook
* Pandas
* [Matplotly](https://matplotlib.org/?fbclid=IwAR2_L-pd4Ycnjd4WZWuP8us9L4Z07844QQ9gjTHtHD7GskLTeCh-c-03hro)
* [Data de StarWars](https://www.kaggle.com/jsphyg/star-wars?fbclid=IwAR1EOOXpTGlZmdOQRZ5d9KApoldJO2O7eCGlF1dB2Qg6hMDU9qtHA2SMRDU)

### Instalación

1.Instalaremos Anaconda
* Nos dirigimos a la [Home de Anaconda](https://www.anaconda.com/) e iremos a la sección de [Download](https://www.anaconda.com/products/individual) (descargas)

2. Abrir Jupyter despues de la instalación
* En nuestra consola escribiremos
`$jupyter notebook`

Despues de unos segundos te abrira automaticamente tu nootebook donde podras trabajar con Python

### Notebook

##### Comandos  Básicos de Jupyter

* Shit + Enter: en una celda: Mandas a compilar la Liena
* Enter: solo haces un salto de linea
* ESC: para salir de modo editor de celda

Fuera de editor
* A : Crea una celda arriba
* B : Crea una celda abajo
* X : Corta una celda
* M : Convertir celda a un Markadown
* Enter : Entrar en la celda

##### Inicio

1. Importamos la libreria Pandas 

  ```
  import pandas as pd
  ```

2. Importamos nuestro CSV que vayamos a utilizar
  ```
  tabla = pd.read_csv('characters.csv')
  ```
  Se asigna a una variable llamada *tabla* utilizando el metodo **pd.read_csv('')**
  
3. Imprimimos tabla
```
print(tabla)
```
y tenemos como resultado

	name	height	mass	hair_color	skin_color	eye_color	birth_year	gender	homeworld	species
0	Luke Skywalker	172.0	77	blond	fair	blue	19BBY	male	Tatooine	Human
1	C-3PO	167.0	75	NaN	gold	yellow	112BBY	NaN	Tatooine	Droid
2	R2-D2	96.0	32	NaN	white, blue	red	33BBY	NaN	Naboo	Droid
3	Darth Vader	202.0	136	none	white	yellow	41.9BBY	male	Tatooine	Human
4	Leia Organa	150.0	49	brown	light	brown	19BBY	female	Alderaan	Human
...	...	...	...	...	...	...	...	...	...	...
82	Rey	NaN	NaN	brown	light	hazel	NaN	female	NaN	Human
83	Poe Dameron	NaN	NaN	brown	light	brown	NaN	male	NaN	Human
84	BB8	NaN	NaN	none	none	black	NaN	none	NaN	Droid
85	Captain Phasma	NaN	NaN	NaN	NaN	NaN	NaN	female	NaN	NaN
86	Padmé Amidala	165.0	45	brown	light	brown	46BBY	female	Naboo	Huma
