# Certificaciones energéticas de edificios

1. Introducción
2. Proceso de transformación:
    * 2.1 Selección de la fuente de datos
    * 2.2 Análisis de los datos
    * 2.3 Estrategia de nombrado
    * 2.4 Desarrollo del vocabulario
    * 2.5 Transformación de datos
    * 2.6 Enlazado
    * 2.7 Publicación

4. Aplicación y explotación
5. Conclusiones
6. Bibliografía

## 1. Introducción

Del catálogo de datos publicado en _[Datos Gobierno de España](https://datos.gob.es/es/sector/medio-ambiente)_, se ha escogido un conjunto de datos en el ámbito del medio ambiente, en el que se informa sobre las certificaciones energéticas de un edificio. El objetivo de este documento es describir la transformación de dicho conjunto de datos con formato csv en datos enlazados, aplicando las metodologías más apropiadas, con el fin de aportar valor al usuario final. De forma que, toda la información enlazada sobre el registro de certificados de eficiencia energética de edificios le sea útil al comprador o usuario a la hora de comprar o alquilar un edificio o vivienda.

## 2. Proceso de transformación

Para llevar a cabo el proceso de transformación de los datos en formato csv a datos enlazados, primero se realiza una selección de la fuente de datos descrito en el aprtado 2.1, de dichos datos un análisis de los mismos: tipos, formato etc, desarrollado en el punto 2.2. En el apartado 2.3 se explica la estrategia de nombrado, cómo se van a nombrar los recursos del vocabulario y datos, y su desarrollo se comenta en el apartado 2.4. En el punto 2.5 se lleva a cabo la transformación de los datos, y su enlazado se explica en el punto 2.6. Por último, su publicación se describe en el apartado 2.7.

### 2.1. Selección de la fuente de datos

Los datos seleccionados se han descargado de la web _[Iniciativa de datos abiertos del Gobierno de España](https://datos.gob.es)_, se trata de una web del gobierno de España, del ministerio de asuntos económicos y transformación digital para la reutilización de información pública. Concretamente se han descargado del catálogo de datos, el conjunto de datos _[Certificaciones energéticas](https://datos.gob.es/es/catalogo/a15002917-certificaciones-energeticas)_. El publicador de los datos es la [Comunidad Foral de Navarra](https://datos.gob.es/es/catalogo?publisher_display_name=Comunidad+Foral+de+Navarra). El por qué de la selección de dichos datos, ha sido por el hecho de ser información muy útil para el usuario a la hora de comprar o alquilar una vivienda.

De acuerdo con la página web citada, se describen los datos como:

La certificación de eficiencia energética de un edificio es el proceso por el cual se obtiene la calificación de eficiencia energética del edificio, calificación que permite valorar el consumo de energía del edificio y  las emisiones de gases de efecto invernadero asociadas a dicho consumo energía. Esta calificación se expresa gráficamente mediante una etiqueta de eficiencia energética, similar a la de los electrodomésticos, que       
asigna a cada edificio una clase energética de eficiencia, que va desde la clase A, para los edificios de menor consumo energético, a la clase G, para los menos eficientes. El Registro de certificados de eficiencia 
energética de edificios ofrece información de las características energéticas de los edificios, para que los compradores y usuarios la tengan en cuenta a la hora de comprar o alquilar un edificio o vivienda.


### 2.2. Análisis de los datos

La licencia de los datos escogidos proviene de [Creative Commons Attribution License (cc-by)](http://www.opendefinition.org/licenses/cc-by), ésta permite la redistribución y la reutilización de una obra con licencia con la condición de que se acredite debidamente al creador. La licencia que utilizan es [CC-BY](https://creativecommons.org/choose/) con reconocimiento 4.0 internacional, de cultura libre, que permite compartir las adaptaciones de la obra y que permite usos comerciales. Por las características propias de la licencia, se utilizará la misma para los datos transformados. 

En la siguiente tabla se detalla el análisi de los datos a transformar:

|Nombre campo|	Tipo dato |Descripción|Rango|                  
| --- | --- | --- | --- |
|_id|
|CodEdificio|
|Tipo|
|CodRegistroComAutonoma|
|Direccion|
|Localidad|
|CP|
|Provincia|
|Zona|
|AnioConstruccion|
|NormativaVigente|
|ReferenciaCatastral|
|TipoDeEdificio|
|Procedimiento|
|Fecha|
|SuperficieHabitable|
|PorcentajeSuperficieHabitableCalefactada|
|PorcentajeSuperficieHabitableRefrigerada|
|PorcentajeSuperficieHabitableAcristalada|
|DemandaDiariaACS|
|GeneradoresCalefaccion|
|GeneradoresRefrigeracion|
|InstalacionesACS|
|SistemasTermicos|
|SistemasElectricos|
|PotenciaTotalInstalada|
|Nombre|
|ConsumoFinalCalefaccion|
|ConsumoFinalRefrigeracion|
|ConsumoFinalACS|
|DemandaACS|
|Nombre1|
|EnergiaGeneradaAutoconsumida|
|ReduccionGlobalEnergiaPrimariaNoRenovable|
|Global|
|Calefaccion|
|Refrigeracion|
|ACS|
|GasNatural|
|GasoleoC|
|GLP|
|Carbon|
|BiomasaPellet|
|BiomasaOtros|
|ElectricidadPeninsular|
|ElectricidadBaleares|
|ElectricidadCanarias|
|ElectricidadCeutayMelilla|
|Biocarburante|
|EnergiaPrimNoRenovable|
|EmisionesCO2|
|CalificacionDemandaEscalaCalefaccion|
|CalificacionDemandaEscalaRefrigeracion|
|CalificacionDemandaCalefaccion|
|CalificacionDemandaRefrigeracion|
|CalificacionEnePrinNoRenovEscalaGlobal|
|CalificacionEnePrinNoRenovGlobal|
|CalificacionEnePrinNoRenovCalefaccion|
|CalificacionEnePrinNoRenovRefrigeracion|
|CalificacionEnePrinNoRenovACS|
|CalificacionEnePrinNoRenovIluminacion|
|CalificacionEmiCO2EscalaGlobal|
|CalificacionEmiCO2Global|
|CalificacionEmiCO2Calefaccion|
|CalificacionEmiCO2Refrigeracion|
|CalificacionEmiCO2ACS|
|CalificacionEmiCO2Iluminacion|


### 2.3. Estrategia de nombrado



### 2.4. Desarrollo del vocabulario



### 2.5. Transformación de datos


### 2.6. Enlazado

