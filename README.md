# RESTAURANTES DE SUSHI EN CULIACÁN SINALOA
<br>**Proyecto Final: Machine Learning**
<br > Master in Data Science/AI
<br> Módulo 6

Determinación de la localización ideal para un restaurante de sushi en el municipio de "Culiacán, Sinaloa" a través de un modelado no supervisado de Machine Learning.


## METOLOGÍA
 * Emplear variables demográficas para realizar un modelo supervisado, estableciendo como variable objetivo el número de puestos de sushi.
  <br>**Código Postal, Escuelas, Hospitales, ... , Sushis***
 * Emplear el CP como variable independiente para cruzar.
 * Considerar un minimo de 50 variables que influencen el establecimiento de variable objetivo, y con ellas crear un modelo NO supervisado para generación de cluster.
 <br>**KMedias**
 * Perfilar los Código Postal.
 * Entrenar un modelo supervisado considerando los cluster generados y  el resto de variables para predecir su Variable Objetivo. 
 <br>**Grid Search**
 * Determinar los 10 lugares en los que se abriría un puesto de comida
 * Determinar las 5 variables de mayor influencia.

## RESULTADOS
A partir del modelado No supervisado: KMeans se crearon 3 clusters, denominados **Zona Cero** , **Término Medio** y **Capitolio**, perfilados a los Código Postales de 
la ciudad. El cluster /*Capitolio*/ Corresponde al "Código Postal" del centro de la ciudad, mientras los otros se dividen los demás zonas de Culiacán. 

<br> Aplicando la regresión de Lasso se identificaron las 5 variables con mayor peso en el modelado de la variable objetivo "Cantidad de Sushis". Mismas que se presentan a
continuación:
<table align='center'>
  <tr>
    <th>Variable</th>
    <th>Coeficiente</th>
  </tr>
  <tr><td>Reparacion vehiculos</td><td>-4.326768</td></tr>
  <tr><td>Bibliotecas</td><td>-4.326768</td></tr>
  <tr><td>Construccion</td><td>4.268687</td></tr>
  <tr><td>Licores</td><td>8.077179</td></tr>
  <tr><td>Restaurantes </td><td>10.540529</td></tr>
  </tr>
  </table>
Mientras que los 10 lugares con una mayor cantidad de puestos de sushi, se encuentran en los presentan Códigos Postales (CP):
<br>

<table align='center'><tr>
  <th> CP </th> 
  <td>80020 </td> 
   <td>80000 </td> 
   <td>80194 </td> 
   <td>80050 </td> 
   <td>80430 </td> 
   <td> 80058 </td> 
   <td>80180 </td> 
   <td> 80197</td> 
   <td>80290 </td> 
    <td>80190 </td> 
  </tr></table>
  
 <br> Se recomienda abrir un restaurante en el cluster /*Capitolio o Término medio*/, otros factores como son la opinión del público, violencia o nivel socieconomico
 se pueden considerar.
 
### PRESENTACIÓN DE RESULTADOS
Los resultados del modelado se puede encontrar en la siguiente presentación: [Sushi](https://www.canva.com/design/DAFSyzMHpYc/CDgjD1YzBC8vkJfHz4vfhw/view?utm_content=DAFSyzMHpYc&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink)
  
## FUENTE
* INEGI: DENUE Sinaloa (2022): [Actividades Económicas](https://www.inegi.org.mx/app/descarga/?ti=6)
* INEGI: Sinaloa (2020): [Censo de Población y Vivienda ](https://www.inegi.org.mx/programas/ccpv/2020/#Microdatos)
