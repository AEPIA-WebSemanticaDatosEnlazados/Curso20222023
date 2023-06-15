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

La frecuencia de actualización de los datos es diaria, por lo que en la descarga del fichero con fecha 14/06/2023, tiene una totalidad del 78.511 filas. En la siguiente tabla se detalla el análisi de los datos a transformar:

|Nombre campo|	Tipo dato |Descripción|Características|                  
| --- | --- | --- | --- |
|_id|numeric|identificador del registro|pk, valor no nulo|
|CodEdificio|varchar|código edificio|valor no nulo|
|Tipo|varchar|tipo de edificación: nuevo, existente, terminado, proyecto|valor no nulo|
|CodRegistroComAutonoma|varchar|código registro de la comunidad autónoma|valor no nulo|
|Direccion|varchar|dirección del edificio|valor no nulo|
|Localidad|varchar|localidad del edificio|vacío|
|CP|varchar|código postal del edificio|valor nulo|
|Provincia|varchar|provincia del edificio|vacío|
|Zona|varchar|zona del edificio|valor nulo|
|AnioConstruccion|numeric|anyo de construcción del edificio|valor nulo|
|NormativaVigente|varchar|normativa vigente|valor nulo|
|ReferenciaCatastral|varchar|referencia catastral|valor nulo|
|TipoDeEdificio|varchar|tipo del edificio|valor nulo|
|Procedimiento|varchar|procedimiento certificación|valor nulo|
|Fecha|date|fecha edificación|valor nulo|
|SuperficieHabitable|numeric|superficie habitable de la vivienda|vacío|
|PorcentajeSuperficieHabitableCalefactada|numeric|porcentaje de superficie habitada con calefacción|vacío|
|PorcentajeSuperficieHabitableRefrigerada|numeric|porcentaje de superficie habitada con aire acondicionado|vacío|
|PorcentajeSuperficieHabitableAcristalada|numeric|porcentaje de superficie habitada acristalada|vacío|
|DemandaDiariaACS|numeric|demanda diaria ACS (agua caliente sanitaria)|vacío|
|GeneradoresCalefaccion|varchar|generadores de calefacción|valor nulo|
|GeneradoresRefrigeracion|varchar|generadores de refigeración|valor nulo|
|InstalacionesACS|varchar|instalaciones ACS (agua caliente sanitaria)|valor nulo|
|SistemasTermicos|varchar|sistemas térmicos|valor nulo|
|SistemasElectricos|varchar|sistemas eléctricos|valor nulo|
|PotenciaTotalInstalada|numeric|potencia total instalada|valor nulo|
|Nombre|varchar|nombre de la contribución energética|valor nulo|
|ConsumoFinalCalefaccion|numeric|consumo final de la calefacción|valor nulo|
|ConsumoFinalRefrigeracion|numeric|consumo final de refigeración|valor nulo|
|ConsumoFinalACS|numeric|consumo final ACS (agua caliente sanitaria)|valor nulo|
|DemandaACS|numeric|demanda ACS (agua caliente sanitaria)|valor nulo|
|Nombre1|varchar|nombre de la contribución energética|valor nulo|
|EnergiaGeneradaAutoconsumida|numeric|energía general de autoconsumo|valor nulo|
|ReduccionGlobalEnergiaPrimariaNoRenovable|numeric|reducción global de energía primaria no renovable|valor nulo|
|Global|numeric|en general|vacío|
|Calefaccion|numeric|calefacción|vacío|
|Refrigeracion|numeric|refrigeración|vacío|
|ACS|numeric|ACS (agua caliente sanitaria)|vacío|
|GasNatural|varchar|gas natural|valor nulo|
|GasoleoC|varchar|gasoleo|valor nulo|
|GLP|varchar|GLP (gas licuado de petróleo) combustión limpia|valor nulo|
|Carbon|varchar|carbón|valor nulo|
|BiomasaPellet|varchar|biomasa pellet|valor nulo|
|BiomasaOtros|varchar|biomasa otros|valor nulo|
|ElectricidadPeninsular|varchar|electricidad en la Península|valor nulo|
|ElectricidadBaleares|varchar|electicidad en Baleares|valor nulo|
|ElectricidadCanarias|varchar|electricidad en Canarias|valor nulo|
|ElectricidadCeutayMelilla|varchar|electricidad en Ceuta y Melilla|valor nulo|
|Biocarburante|varchar|biocarburante|valor nulo|
|EnergiaPrimNoRenovable|varchar|energía prima no renovable|valor nulo|
|EmisionesCO2|varchar|emisiones CO2|valor nulo|
|CalificacionDemandaEscalaCalefaccion|varchar|calificación de la demanda en escala de la calefacción|valor nulo|
|CalificacionDemandaEscalaRefrigeracion|varchar|calificación de la demanda en escala de la refrigeración|valor nulo|
|CalificacionDemandaCalefaccion|varchar|calificación demanda calefacción|valor nulo|
|CalificacionDemandaRefrigeracion|varchar|calificación demanda refrigeración|valor nulo|
|CalificacionEnePrinNoRenovEscalaGlobal|varchar|calificación energia principal no renovable en escala global|valor nulo|
|CalificacionEnePrinNoRenovGlobal|varchar|calificación energia principal no renovable global|valor nulo|
|CalificacionEnePrinNoRenovCalefaccion|varchar|calificación energia principal no renovable en calefaccion|valor nulo|
|CalificacionEnePrinNoRenovRefrigeracion|varchar|calificación energia principal no renovable en refrigeración|valor nulo|
|CalificacionEnePrinNoRenovACS|varchar|calificación energia principal no renovable en ACS|valor nulo|
|CalificacionEnePrinNoRenovIluminacion|varchar|calificación energia principal no renovable en iluminación|valor nulo|
|CalificacionEmiCO2EscalaGlobal|varchar|calificación en emisiones CO2 en escala global|valor nulo|
|CalificacionEmiCO2Global|varchar|calificación en emisiones CO2 global|valor nulo|
|CalificacionEmiCO2Calefaccion|varchar|calificación en emisiones CO2 en calefacción|valor nulo|
|CalificacionEmiCO2Refrigeracion|varchar|calificación en emisiones CO2 en refrigeración|valor nulo|
|CalificacionEmiCO2ACS|varchar|calificación en emisiones CO2 en ACS|valor nulo|
|CalificacionEmiCO2Iluminacion|varchar|calificación en emisiones CO2 en iluminación|valor nulo|



### 2.3. Estrategia de nombrado



### 2.4. Desarrollo del vocabulario



### 2.5. Transformación de datos


### 2.6. Enlazado

