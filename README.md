# Proyecto Python
## Scope del Proyecto
| ETAPA | DESCRIPCION |
| ----- | ----------- |
|OBJETIVOS| Definir el impacto de cobertura de internet en el pais para realizar programas en linea que disminuyan el analfabetismo contribuyendo al aumento de la poblacion economica activa|
|RECURSOS| -  Personal (Tres Personas) Trabajo 10 horas de trabajo a la semana durante 2 semanas|
|        | - 3 Archivos CVS cargados a S3|
|        | - 1 BD cargada a RDS por medio de DATAGRIP MYSQL|
|        | - Python desde Jupiter Lab en anaconda          |
|ENTREGABLE| **Link a repositorio donde se ubican los codigos utilizados para realizacion de proyecto** https://github.com/androseo/tareas-y-proyectos/tree/main/ProyectoFinalPython|
|          |El archivo llamado RDS-S3.ipynb contiene todo el codigo de ETL|
||**Video Presentacion de Proyecto** |
|CRONOGRAMA|1 al 3 Abril (Busqueda de informacion a utilizar)|
|          |4 al 6 Abril (Revision y unificacion de informacion para Analisis BI)|
|          |6 al 8 Abril (Realizacion de primer borrador|
|          |8 al 10 Abril (Realizacion de presentacion Markdonw|
|          |10 al 12 Abril (Revision para entrega final|
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
            (Se realizo reshape de filas para todoas las tablas para que tuvieran la misma cantidad de filas y tambien que tuvieran como llave Depto ID y se normalizaron las bases de datos lo que permitio unicarlas y procesarlas)
            
           - Con codigo se cargo 1 tabla desde s3 y se llama telefonias

![Inciso5](https://user-images.githubusercontent.com/89221655/162656876-d99ed52a-c162-432b-95b2-bacac91ae450.png)

           - Codigo de Joins y union de Tablas.

![Inciso 5-2](https://user-images.githubusercontent.com/89221655/162656925-d0871d88-f2fb-4659-a369-a62d0d12987e.png)

           - Rename de Columnas

![inciso 5-3](https://user-images.githubusercontent.com/89221655/162656975-f295511d-9144-41b6-ab26-20098489bf75.png)

           - Operaciones entre columnas
           
 ![inciso 5-4](https://user-images.githubusercontent.com/89221655/162657198-5806ffcb-5345-418c-bc11-cbbade848e15.png)

           - Base para Analisis
           
 ![inciso 5-5](https://user-images.githubusercontent.com/89221655/162657566-a121af42-88ef-452c-9e01-2d02cfaf8cbf.png)

      

6.         Creacion de fact table como archivo final de CSV para consumo S3 (Analitica)
![Inciso 5-6](https://user-images.githubusercontent.com/89221655/162658169-66317275-7904-4739-bd7d-53a93486d5e3.png)


7.         Insights o hallazgos de la data.

![Inciso 7](https://user-images.githubusercontent.com/89221655/162658334-14027f33-2da2-4c43-958d-68d1ef4702a9.png)

Relación en la población GT arriba de 15 años que tiene lineas telefonicas y consumen internet

## Analitica
 -  Se analizacion los siguientes variables con la realizacion del proyecto

![Preguntas](https://user-images.githubusercontent.com/89221655/162644423-97b969b8-129f-4b60-b585-61dd779580d5.png)

Internet ha estado evolucionando de la mano con las nuevas tecnologias las cuales son utilizadas para una diversidad de tareas para el ser Humano, por otro lado el analfabetismo que es un problema social, que va en aumento, y no solo se limita a personas que no saben leer y escribir, hoy en dia un analfabeta es aquel no sabe navegar en el ciber espacio, aquel no estudia una segunda Legua, el que no entiende las Matematicas,etc.
Se necesita inversion de las partes interesadas para lograr un aumento de programas que contraresten el/al analfabetismo en el pais; se tienen mas oportunidades laborares al estar capacitado, dando oportunidad a familias de mejorar su ingreso economico y asi lograr ser un pais encaminado al desarrollo.

**Este es un extracto del Proyecto realizado, para ver toda la informacion ver el Github que esta al principio de esta presentacion.**
