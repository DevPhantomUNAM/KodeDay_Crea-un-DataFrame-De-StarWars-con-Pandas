# KodeDay
## Crea un DataFrame De StarWars con Pandas


### Herramientas utilizadas

* Jupyter Notebook
* Pandas
* [Matplotly](https://matplotlib.org/?fbclid=IwAR2_L-pd4Ycnjd4WZWuP8us9L4Z07844QQ9gjTHtHD7GskLTeCh-c-03hro)
* [Data de StarWars](https://www.kaggle.com/jsphyg/star-wars?fbclid=IwAR1EOOXpTGlZmdOQRZ5d9KApoldJO2O7eCGlF1dB2Qg6hMDU9qtHA2SMRDU)

### Instalación

+ Instalaremos Anaconda
  + Nos dirigimos a la [Home de Anaconda](https://www.anaconda.com/) e iremos a la sección de [Download](https://www.anaconda.com/products/individual) (descargas)

+ Abrir Jupyter despues de la instalación
  + En nuestra consola escribiremos
  + `$jupyter notebook`

Despues de unos segundos te abrira automaticamente tu nootebook donde podras trabajar con Python

### Notebook

##### Comandos  Básicos de Jupyter

| Combinación	| Description                    |
| ------------- | ------------------------------ |
| `Shit + Enter`| Mandas a compilar la linea.	 |
| `Enter`	| Solo haces un salto de linea     |
| `ESC`	| Para salir de modo editor de celda     |


Fuera de editor


| Combinación	| Description                    |
| ------------- | ------------------------------ |
| `A`| Crea una celda arriba	 |
| `B`	| Crea una celda abajo     |
| `X`	| Corta una celda    |
| `M`	| Convertir celda a un Markadown     |
| `Enter`	| Entrar en la celda    |

#### Inicio

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
Y tenemos como resultado:

| number| name	| height	| mass	| hair_color	| skin_color	| eye_color	| birth_year	| gender	| homeworld	| species |
| ------------- | --------| --------| --------| --------| --------| --------| --------| --------| --------|  --------| 
|0	|Luke Skywalker	|172.0	|77	|blond	|fair	|blue	|19BBY|	male	|Tatooine	|Human|
|1	|C-3PO	|167.0	|75	|NaN	|gold	|yellow	|112BBY	|NaN	|Tatooine	|Droid|
|2	|R2-D2	|96.0	|32	|NaN	|white, |blue	red	|33BBY	|NaN	|Naboo	|Droid|
|3	|Darth Vader	|202.0	|136	|none	|white	|yellow	|41.9BBY	|male	|Tatooine	|Human|
|4	|Leia Organa	|150.0	|49	|brown	|light	|brown	|19BBY	|female	|Alderaan	|Human|
|...	|...	|...	|...	|...	|...	|...	|...	|...	|...	|...|
|82	|Rey	|NaN	|NaN	|brown	|light	|hazel	|NaN	|female	|NaN	|Human|
|83	|Poe |Dameron	|NaN	|NaN	|brown	|light	|brown	|NaN	|male	|NaN	|Human|
|84	|BB8	|NaN	|NaN	|none	|none	|black	|NaN	|none	|NaN	|Droid|
|85	|Captain Phasma	|NaN	|NaN	|NaN	|NaN	|NaN	|NaN	|female	|NaN	|NaN|
|86	|Padmé Amidala	|165.0	|45	|brown	|light	|brown	|46BBY	|female	|Naboo	|Huma|


##### Manipular tabla

Para manipular la tabla, podemos utilizar funciones para elegir valores con condiciones, por ejmeplo

````
tabla.gender == "female"
````

Lo que hara es traernos los valores de genero donde se cumplan la condicion de si el genero es "female"
por lo cual nos desplegara lo siguiente: 

````
0     False
1     False
2     False
3     False
4      True
      ...  
82     True
83    False
84    False
85     True
86     True
Name: gender, Length: 87, dtype: bool
````

Pero para traer toda la tabla y que nos muestre los datos completos cuando alguien tiene en el genero "female"
lo podemos hacer con:
````
tabla[tabla.gender == "female"]
````
| | name|	height|	mass|	hair_color|	skin_color|	eye_color|	birth_year|	gender|	homeworld|	species|
| ------------- | --------| --------| --------| --------| --------| --------| --------| --------| --------|  --------| 
|4	|Leia Organa	|150.0	|49	|brown	light	|brown	|19BBY	|female	|Alderaan	|Human|
|6	|Beru Whitesun lars	|165.0	|75	|brown|	light	|blue	|47BBY	|female	|Tatooine	|Human|
|26	|Mon Mothma	|150.0	|NaN	auburn	|fair	|blue	|48BBY	|female	|Chandrila	|Human|
|40	|Shmi Skywalker	|163.0	|NaN	|black	|fair	|brown	|72BBY	|female	|Tatooine	|Human|
