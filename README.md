# Proyecto Python
## Scope del Proyecto
| ETAPA | DESCRIPCION |
| ----- | ----------- |
|OBEJTIVOS| Definir el impacto de cobertura de internet en el pais para realizar programas en linea que disminuyan el analfabetismo contribuyendo al aumento de la poblacion economica activa|
|RECURSOS| -  Personal (Tres Personas) Trabajo 10 horas de trabajo a la semana durante 2 semanas|
|        | - 3 Archivos CVS cargados a S3|
|        | - 1 BD cargada a RDS por medio de DATAGRIP MYSQL|
|        | - Python desde Jupiter Lab en anaconda          |
|Entregable|Reporte BI para toma de decisiones|
|Cronograma|1 al 3 abril (Busqueda de informacion a utilizar)|
|          |4 al 6 abril (Revision y unificacion de informacion para Analisis BI)|
|          |6 al 8 abril (Realizacion de primer borrador|
|          |8 al 10 abril (Realizacion de presentacion Markdonw|
|          |10 al 12 abril (Revision para entrega final|
|          |        |
| |  |
           
## Modelo de Datos
Se utilizo el modelo relacional por su estructura y conveniencia, la principal ventaja de la base de datos relacional reside en la sencillez, que nos permitira manejar grandes cantidades de datos con puntos de relación entre sí, gestionándolos de forma segura y conforme a unas normas y un modo uniforme.

Permitira mantener la uniformidad de los datos en todas las aplicaciones y copias de de la propia base, esto nos garantiza que no se produzca la duplicidad de registros, Así mismo, para evitar conflictos cuando varios usuarios o aplicaciones intentan acceder a los mismos datos en el mismo momento, pueden bloquear dicho acceso mientras los datos se están actualizando.

Por su parte, la concurrencia se ocupa de gestionar las llamadas a consultas de varios usuarios o aplicaciones al mismo tiempo en la misma base de datos. A través de ella se proporciona el acceso corrector a los usuarios o aplicaciones según las normas o políticas definidas para el control de datos.

![Tabla](https://user-images.githubusercontent.com/89221655/162648026-98b9c145-8843-49fd-afa2-37fd577901f5.png)


## Procesamiento

1.         Seleccionar datos o archivos CSV para trabajar
           -          Los archivos que se trabajaron fueron descargados de: INE (Población Guatemalteca Censo, Educacion Formal)
           -          Cuentas de Usuarios Facebook (META)
           -          Usuarios Moviles (Data Interna)
                          
2.         Carga archivos a S3
![Cod2](https://user-images.githubusercontent.com/89221655/162655379-f1a56b02-523a-479b-94b0-0377484c5991.png)


![S3-2](https://user-images.githubusercontent.com/89221655/162654982-0a7394c1-96e5-4a8d-a4e7-d2c9277e462f.png)

3.         Exploracion de Datos 
           Se procedio a cargar los archivos en python para observar su contenido, y descartar aquellas que no aportaban al proyecto.         
![inciso3](https://user-images.githubusercontent.com/89221655/162655884-3e5beabe-1227-44b4-bdfa-0467c4e24962.png)

         
4.         Carga BD por DataGrip a RDS
         - Se creo la estructura de datos en SQL sobre el censo de la Poblacion de Guatemala 2018.
       
![RDS2](https://user-images.githubusercontent.com/89221655/162654327-d38a28d5-b83e-4192-a6fc-1a849ab241cf.png)


5.         Carga en Python, Limpieza de Datos, Joins, reshape de datos.


6.         Formacion de fact table para crear un archivo final de consumo para S3 (Analitica)


7.         Insights o hallazgos de la data.


## Analitica
 -  Se analizacion los siguientes variables con la realizacion del proyecto

![Preguntas](https://user-images.githubusercontent.com/89221655/162644423-97b969b8-129f-4b60-b585-61dd779580d5.png)

Internet ha estado evolucionando de la mano con las nuevas tecnologias las cuales son utilizadas para una diversidad de tareas para el ser Humano, por otro lado el analfabetismo que es un problema social, que va en aumento, y no solo se limita a personas que no saben leer y escribir, hoy en dia un analfabeta es aquel no sabe navegar en el ciber espacio, aquel no estudia una segunda Legua, el que no entiende las Matematicas,etc.
Se necesita inversion de las partes interesadas para lograr un aumento de programas que contraresten el/al analfabetismo en el pais; se tienen mas oportunidades laborares al estar capacitado, dando oportunidad a familias de mejorar su ingreso economico y asi lograr ser un pais encaminado al desarrollo.
