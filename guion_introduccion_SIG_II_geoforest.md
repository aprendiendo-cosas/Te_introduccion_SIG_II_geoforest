# Guión de la sesión introductoria de la asignatura "Sistemas de información geográfica y ecología espacial: aplicaciones"

> + **_Tipo de material_**: <span style="display: inline-block; font-size: 12px; color: white; background-color: #029BF9; border-radius: 5px; padding: 5px; font-weight: bold;"> Teoría</span>
> + **_Versión_**: 2024-2025
> + **_Asignatura_** : SIG II (Máster GEOFOREST). 
> + **_Autor_**: Antonio J. Molina Herrera (o22mohea@uco.es) y Curro Bonet-García (fjbonet@uco.es)
> + **_Duración_**: 0.5 horas.


## Objetivos

Esta sesión tiene los siguientes objetivos:
+ Disciplinares:
  + Definir el hilo argumental temático que seguiremos durante la asignatura: restauración post-incendio.
  + Enumerar las cuestiones relacionadas con la ecología espacial que se abordarán.
  
+ Instrumentales:
  + Entender el concepto de flujo de trabajo.
  + Conocer las variables ambientales que usaremos en la asignatura.
  + Reconocer las técnicas de análisis que usaremos.
  
   
## Contextualización ecológica y pedagógica de la asignatura

Esta asignatura tiene un carácter claramente instrumental. La idea es que los estudiantes se familiaricen con una serie de técnicas que nos permiten conocer mejor cómo se distribuyen en el espacio una serie de variables ambientales. Buena parte de estas técnicas se sostienen en conceptos relevantes para la ecología y para otras disciplinas básicas (hidrología, geomorfología, botánica, etc.). Por otro lado, tanto la neurociencia como la pedagogía nos enseñan que el aprendizaje profundo requiere un anclaje de lo aprendido al mundo real. Por eso, para fomentar el aprendizaje profundo y no estratégico, proponemos que esta asignatura se desarrolle usando la metodología de "aprendizaje basado en proyectos". Así pues, proponemos un proyecto (o un problema) cuyo abordaje requiere aprender una serie de técnicas.

En este curso académico, el problema a abordar tiene una gran importancia social y ecológica: restauración de la vegetación en zonas quemadas. Después de un incendio forestal ocurren varias cosas. En primer lugar se inicia un proceso bien conocido: la sucesión ecológica. Este proceso espontáneo es una propiedad emergente de los ecosistemas gracias al cual el sistema tiende a volver a la situación previa a la perturbación. Es decir, el sistema tiende a regenerarse. Además, los humanos intentamos acelerar esa sucesión mediante varios tipos de acciones: medidas para retener el suelo, reducción del riesgo de plagas forestales, cobijo para la fauna, restauración de la vegetación, etc. Si bien la sucesión ecológica ocurre de manera integrada en todo el territorio a la vez (aunque con diferentes intensidades dependiendo de las condiciones ambientales), las actuaciones de restauración están sujetas a limitaciones. No hay dinero para todo. Así que, los tomadores de decisiones se ven obligados a priorizar zonas de actuación. Además, algunos tipos de acciones tienen un grado de éxito variable en función de las características del territorio (ej. una plantación tiene más marras en una zona pedregosa o sin suelo). Por tanto, uno de los primeros pasos que se dan antes de iniciar los trabajos de restauración es zonificar la zona afectada. Para maximizar la inversión, se identifican aquellas zonas del territorio que comparten ciertas características (pendientes, vegetación original, grado de afección por el incendio, etc.). Se asume (con un nivel de incertidumbre muy alto) que todas las zonas de la misma clase podrán recibir las mismas actuaciones de restauración.

Según lo anterior, el problema concreto que abordaremos en la asignatura se puede describir así:

> Tras el incendio ocurrido en Sierra Bermeja (provincia de Málaga) en 2021, la Junta de Andalucía decide iniciar un proyecto de restauración de la zona quemada. Para ello, encarga a los estudiantes de GEOFOREST que realicen una zonificación (o estratificación) del territorio en virtud de una serie de variables ambientales: intensidad del fuego, radiación solar, biodiversidad previa al incendio, etc.

Seguro que te ha salido una sonrisa torcida al leer que "la Junta de Andalucía encarga a los estudiantes de GEOFOREST". No ha sido así en esta ocasión. Pero en menos de lo que te imaginas recibirás encargos parecidos... Así que, manos a la obra :)



## Flujo de trabajo

Un flujo de trabajo es una secuencia de acciones ordenadas cuya ejecución tiene un objetivo determinado. Esta definición tan genérica se puede particularizar más en nuestro ámbito de trabajo: secuencia de acciones que realizamos sobre un conjunto de datos para satisfacer un objetivo dado. En nuestro caso, el objetivo es responder a la pregunta descrita en la sección anterior.

Es importante que aprendamos a crear flujos de trabajo porque nos ayudan en el proceso de creación y análisis de la información ambiental. En esta sesión estudiaremos un flujo de trabajo que nos guiará durante el resto de la asignatura.

En los siguientes enlaces tienes información sobre flujos de trabajo. Recomendamos su lectura:

+ [El papel de los flujos de trabajo en la reproducibilidad de la ciencia.](https://github.com/aprendiendo-cosas/Te_introduccion_SIG_II_geoforest/raw/2024_2025/biblio/how_to_flow.pdf) 
+ Descripción de [Kepler](https://github.com/aprendiendo-cosas/Te_introduccion_SIG_II_geoforest/raw/2024_2025/biblio/kepler.pdf), un sistema de flujo de trabajo científico muy útil (y algo complejo).
+ [Ejemplos de flujos de trabajo.](https://github.com/aprendiendo-cosas/Te_introduccion_SIG_II_geoforest/raw/2024_2025/biblio/workflow_reusable.pdf) 

A lo largo de la asignatura trabajaremos ejecutando los pasos que se describen en el siguiente flujo de trabajo:



<iframe frameborder="0" style="width:100%;height:703px;" src="https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=flujograma_SIG_II.drawio#R7V1bl5s4Ev41fU72YfoA4mI%2F9sXpzZ5JMknv2ZnMGwa1rQxGrIC%2BzK%2BfEjdjiW5rYkC2mZduEGCgvqpPpSqpuEA3m%2Bc75ifrjzTE0YVlhM8X6PbCsixz7sI%2F3vJStpiWbZctK0bCqm3bcE%2F%2BxFWjUbXmJMTpzokZpVFGkt3GgMYxDrKdNp8x%2BrR72gONdu%2Ba%2BCssNdwHfiS3%2FkrCbF29GELu9sC%2FMVmt61u7TvWCG78%2Bu3qVdO2H9KnVhBYX6IZRmpVbm%2BcbHHHx1YIpr3v%2FytHmyRiOM5ULUmJ%2Buv%2Fd%2FP59gZbv4y%2Fm50X8n5%2Bqh330o7x64%2Bphs5daBDgEiVS7lGVruqKxHy22rdeM5nGI%2BW0M2Nue8zOlCTSa0PgdZ9lLBa%2BfZxSa1tkmqo6W9%2BQ3evXdqqaU5izAb7xQ9fyZz1Y4e%2BM81CAAyovpBmfsBa5jOPIz8rj7HH6lRKvmvK2YYaOS9N%2BQuiVJ%2FR5elMTcegTpg9YkfDN4iQgImSEQ19OaZPg%2B8QtBPIHl7UpzWcLx87Jp8IM%2FVgVIn%2FMMfgZX7WmJh%2Bk0EDxiluHnt0GQhVZd4FWKXtm6Nav2n7aG41ZN65bJ1Kf1LmXnxFUZKary7EBVri79hRJ4wgZNZO%2FCiSwBp%2FK5qqsEqJrH%2BHH0kGQjd4uFhChb080yT%2FcbRQ%2F6bRn7FXw2poKbpiSPETQcpMVefquuL3a%2B8Z1Lp969fW4fvH2p9nq0DFfRMkyjG9BxWN6VNPjm4gZdXJlRkEeUvycGfSShH%2F64Wu%2Bi2YOSO4LZm9qVXO4sT5zXZ4ra6%2FbB61eM%2BS%2BtExLO1%2BnrtG%2BLJLfrVcJG%2BYu9cr2JTonI8DPJftueCXvf6l%2BE7e1FfGcA8lNVH9MexC%2BwBYKw3XH9gtk%2BVg0x%2FCmabuOQBHzv0%2FVX%2BPvuE2UbPwJ1AMI1rnMWw7%2BvIAv6L0n9arcbAPKjCEd0xfwN4JgAYcMbYCYe%2B2V7YB9nP5BnXA91e3JNRGfNmsusbVodtC2C15%2FzfXa0XYck9hqe8wpWI3kdnuxNHMyUFeOZLb4zLj3nTcrD0bIId3DFJoEfHYfrqIyiOwx9mobQwSJvXP6sBdAyzI9%2B4tfE2fJJjTKaR%2BIAA5HSU%2BdIDwmebRdHOmNypClH34S%2BLCr7sQ3ICvb%2BBKOFf%2F%2FP8cYPfdnM9Q0aBNEi1e7HNAaTrZboz%2FAEt9%2Ftc1WZcBiCc0X%2F0BYgLh9sOH6Th923OCJgQn5AuDldo3i%2FLZ04t9mmdm6bn53%2F56la4KEB2cNyC64OOR%2BDZ6eKj3Uo8R1mGJ7sf93C5e9f5aDTS%2F24riXRz6ipn0ZpTpZsVKM8rVRyr734bBdRRzHK87fDjXPhPlXcYNBwo3VS4UYtWmVppUg5xqc792c7gp7OZYYbNS1STzM5WYazRgun%2FRAxmcgUmWmERIg7l7Vcd5qjHfQbLcmhrB0Hh%2BkO8zPeDqYlPHAG747TV527Ex1gOpbuAaajJ8DTGQnfEwjX3%2FHXg%2B8jz13Uw4hjoD8d0tdMZtabZEYZpzI%2FIDQ%2BPz5zDdmfG5fPrJkWPjsC67AVrcPytFqHnKy5v7q7kglL46jEs2QtHndUIiefJ6LEqsFHzR2sHBeblPSHSuo7QlLfm6uFy3qLaHUElVtdN4lTGrXTX%2BfVeXtIe%2Bd9dtkupDoAR1oJDckD8DNcSjM35NH2qPkUNNWIOVKddlFSkDYzMCUzOLaIeZcOj%2BubTnWAVfeOx%2B6byl3mpKSvN%2FhTP2aLQf6LQfhxQBo38tPt%2Fz68NVHhRN3HufbJUujslmEjR7Xf1BrUqR%2FzvN1H09C9FBtNdVIaUo1MIK2TBpEcPzg2%2F7FTicd1IOXk%2FKhKvNXbb%2B1jIyix6rQhzQ6kPEg9qskT%2B%2FLEOhDT7HTKE70%2BUpJmOSuWImUM80yjwbvbZ%2Fj%2F7uP9h5NfqukZIq91LZbpIrbh3M%2Bzi17aqtFLW2vYxpajl3fXH85pJrjZNOhyPe2pFkmxVQMPttZaWPVjtmzga6E%2FlvHl7sP9cfmgXdo8qg9am87kfFBbtRpWP9OF988HnolLVwdO8XryhO%2BpzmZU1oVzTffbcnG0drp%2FSWgIb8fSztpSp%2B4vd5VdG9dfto8jXKt5jGnPVf2LQ0O83VZoifUcHJGRB15pbk81qGmrBjVtrUFNWw5qHp9H2ZTP0uZRah4f6fMoTySqKa9zmWpUUxkxvVFNuyOq2fLOQpJmPk%2Br89Ambw18xrh75Z%2F%2BqgpTZLeO8bLpjeqrybHNNhjnI3tXRfSjusmulkmDPfKNozr5z9UaRa4fs11GLPJT8kCCnZJHcVFzOAf9fSRpUfTIePdVzqeM6Q6ZlriufubJWttVOUwccfentXI8sk0YvG4UJ24QEl0V1dnmMT599jBnwjC7c0HcqBVEvamuJXJVF8R5h1aIPsxQ5CjIgm%2FvcM4mjzISMFBnxitIGu%2B%2BrEiqmXOatetNJFdR1QfjHE%2BuWTdFzpmZiuQ%2FHOd0VJ7BMbiHEQ%2BlFpMRCkS6JkeBILJdmaUZo3%2FgGxpRVpyCQnfpOm4hzShqtT88PFhBAO1wn1UMbQEvGsFRqYvnXlUHNiQMC6LrgovC2Q9RUXR3DefhuC%2BDEYpL2x2epd0Bk%2FjFkP5gkp36GyAQEu9wj1gInKOH0wQHGeDZsYT9bAG0xaS8KoBoKADrccgOgHGAk6yp4N7UTuGjNCC%2Bop2Rx9JxLU6J%2BJYPHUyWh9NBcyaUTLO78iFdaDqDodkxABHQbIpHCOaZ860kjzN6eXk5IQzFgomOdgzlYc%2FnAJw3f8OB4zhmNAGnoaxPDUNLCnC5EYdnyWBrxbdA%2FgQ8k6ipH178ICP%2BclJ8OxOKJ3r6LbTja1pdfk1nRYuzxckRwpWeYSs6NrOhcJLXoyxSkAXhny2R2bPoABNGwzxoH0vAq%2BdWNx0kRT6dd2TVOpEUi5P3h2TH17%2F%2BcVGVATSPwEeV08dv2WJe1JOve7sCR5Ap%2FSnELU92snA2X4%2FU1gXO5SHHAqTtZ1KcvPzsCQiTkYyWYauUxMUzgURl5BOc0jqXFxWBmgn6PCYSElBOV%2F5pXMTlYYk64iXWcUj%2FAbg66gphU8%2FtiNb1BDDsbj%2BMXc7X2n5gHC3%2BAg%3D%3D"></iframe>



Si te mueves sobre el esquema verás en la parte inferior la herramienta lupa para acercarte.

En este flujograma los trapecios representan mapas, los rombos procesos analíticos y los cilindros fuentes de datos. También se añaden etiquetas de color amarillo que representan las principales competencias a adquirir por los estudiantes durante la asignatura. 




****

[Aquí](https://github.com/aprendiendo-cosas/Te_introduccion_SIG_II_geoforest/archive/refs/tags/2024_2025.zip) puedes descargar un archivo .zip que contiene este guión en formato html y todo el material que incluye.

****
Haz click [aquí](https://github.com/aprendiendo-cosas/Te_introduccion_SIG_II_geoforest/releases) para ver cómo ha cambiado este guión en los distintos cursos académicos.

****
 <p xmlns:cc="http://creativecommons.org/ns#" >El contenido de este repositorio se puede utilizar bajo la siguiente licencia:  <a  href="https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1"  target="_blank" rel="license noopener noreferrer"  style="display:inline-block;">CC BY-NC-SA 4.0<img  style="height:22px!important;margin-left:3px;vertical-align:text-bottom;"   src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"  alt=""><img  style="height:22px!important;margin-left:3px;vertical-align:text-bottom;"   src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"  alt=""><img  style="height:22px!important;margin-left:3px;vertical-align:text-bottom;"   src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1"  alt=""><img  style="height:22px!important;margin-left:3px;vertical-align:text-bottom;"   src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1"  alt=""></a></p> 

<p>Esta licencia no aplica a enlaces a artículos, libros o imágenes no originales. Estos productos tienen su licencia correspondiente.</p>









