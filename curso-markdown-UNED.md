---
title: "Escritura académica en texto plano"
toc-own-page: true
toc: true
subtitle: Propuesta de curso para la UNED 
author: Carlos J. Martínez Domingo (UNED) # ^[carlosmartinezdomingo@gmail.com]
date: Septiembre de 2022
lang: es-ES
csquotes: true
papersize: a4
fontsize: 12pt
colorlinks: true
urlcolor: ForestGreen
linkcolor: ForestGreen
link-citations: true
bibliography: '/home/carlosm/biblioteca/biblioteca-zotero.bib'
header-includes: \usepackage{xurl}
titlepage: true
titlepage-text-color: "FFFFFF"
titlepage-rule-color: "360049"
titlepage-rule-height: 0
titlepage-background: "background-verde.pdf"
---

# Introducción 

Las actividades académicas que realizan los miembros de universidades e institutos de investigación demandan eficiencia y excelencia en la producción de textos escritos de diversa índole: publicaciones científicas, materiales docentes, presentaciones, etc.

La escritura académica en texto plano puede ser de gran utilidad en este tipo de tareas y, de igual modo, supone un cambio de paradigma en la forma de enfrentarse a la redacción de textos que resulta beneficioso para el personal docente e investigador.

Así pues, se presenta la siguiente propuesta de curso a modo de iniciación en esta forma de crear textos. En el curso se ofrecen las indicaciones básicas para generar documentos y presentaciones de una gran calidad tipográfica con el mínimo esfuerzo posible. Además, se proporcionarán herramientas para la automatización de la gestión de la bibliografía, aspecto que suele consumir mucho tiempo a docentes, estudiantes e investigadores. Además, la elección de Markdown (muy sencillo si se compara con otros lenguajes como \LaTeX) hace que la transición sea cómoda. 

# Justificación y contextualización en el proyecto +PoeMAS^[+PoeMAS, “MÁS POEsía para MÁS gente. La poesía en la música popular contemporánea”, proyecto de investigación con financiación del Ministerio de Ciencia e Innovación (PID2021-125022NB-I00), coordinado en la UNED por Clara I. Martínez Cantón y Guillermo Laín Corona, entre enero de 2022 y diciembre de 2024.]

Los principios de la escritura en texto plano y el lenguaje de marcado Markdown presentan una serie de beneficios que son de singular utilidad en la escritura académica. @tenen2014 destacan las siguientes:

- Sostenibilidad e independencia de formatos.  
El texto plano no depende de formatos propietarios (por ejemplo, el `.docx`) y está garantizada su sostenibilidad a largo plazo. Así, un texto escrito en texto plano nunca cambia su formato a raíz de cambios en las versiones de formatos; se mantiene estable a lo largo del tiempo e independientemente del sistema operativo o del editor de texto.
- Separación de forma y contenido.  
Habitualmente, en la escritura académica en humanidades se emplean **procesadores** que siguen en el principio _WYSIWYG_^[_What you see is what you get_.]. Es decir, el proceso de creación de contenido y de aplicación de formato al texto suceden y se visualizan de forma simultánea. Frente a este paradigma se encuentra el principio _WYSIWM_^[*What you see is what you mean.*], que proporciona instrucciones sobre el formato que no se visualizan al instante. Aunque intuitivamente pueda parecer una desventaja, en realidad proporciona beneficios: el autor se centra en el contenido y las marcas de formato reproducen exactamente su intención y cobran un sentido _semántico_.
- Automatización del formateo y ahorro de tiempo y esfuerzo.  
A partir de las marcas de formato indicadas por el autor, el _software_ formatea el texto automáticamente. Ello se lobra con Pandoc [@macfarlane2021], un software que, a partir del potente lenguaje tipográfico \TeX y de \LaTeX, traduce las instrucciones en Markdown a formatos como `.pdf`. Un ejemplo de cómo se pasa de un fichero de texto plano escrito en Markdown a un archivo `.pdf` se puede encontrar en el repositorio que alberga este proyecto [@martinez-domingo2022]^[Compárese el documento `curso-markdown-UNED.md` con `curso-markdown-UNED.pdf`.].
- Reproducibilidad.  
A partir de un mismo archivo de texto plano escrito en Markdown, es posible generar todo tipo de documentos sin necesidad de rehacer el documento "fuente": archivos `.docx`, `.pdf`, `.odt`, presentaciones, páginas web... 
- Control de versiones.  
El texto plano facilita el control de versiones cuando se emplea de forma conjunta a otros programas como Git. Este _software_ registra el historial de cambios de un documento y permite revertirlos de una forma segura y transparente.

Gran parte de estos principios están en consonancia con los objetivos del proyecto +PoeMAS. Para comenzar, este tipo de escritura se integra fácilmente con plataformas empeladas en las humanidades digitales, como [GitHub](https://github.com/) o [GitLab](https://about.gitlab.com/). Además, tal y como se ha dicho, favorece la "interoperabilidad y la reutilización de datos" [@martinez-canton2021, 5] y se enmarca dentro de la previsión sobre actualización de las competencias digitales de los miembros del proyecto [@martinez-canton2021, p. 34] 


# Objetivos

#. Familiarizarse con el texto plano y la línea de comandos.
#. Conocer y aplicar el lenguaje de marcado Markdown.
#. Usar Pandoc para convertir archivos de texto plano en ficheros `.pdf`, `.doc` y `.odt`.
#. Iniciarse en el trabajo con plantillas para automatizar los procesos de formateo del texto.
#. Generar presentaciones académicas a partir de archivos de texto plano.
#. Aplicar las posibilidades de Pandoc y Markdown a la escritura académica: índices, citas, tablas, referencias bibliográficas, estilos
de citación.
#. Iniciarse en el uso de archivos `.bib` para la gestión de la bibliografía.

# Contenidos

- Procesadores y editores de texto
- El lenguaje Markdown
- Edición de ficheros Markdown
- Introducción a Pandoc
- Pandoc: opciones aplicadas a la escritura académica
- Presentaciones académicas con Markdown y Beamer
- La gestión de la bibliografía para la escritura en texto plano.

# Método y  plan de trabajo

La metodología didáctica seguirá dos patrones:

- La instrucción directa mediante materiales escritos y grabados por el profesor y recursos facilitados en la sección [Recursos y bibliografía].
- La práctica guiada de los participantes en el curso, que deberán entregar tres [tareas]{#tareas}:
  #. Un archivo Markdown y su exportación a `.html` donde se empleen la mayoría de elementos de marcado del lenguaje.
  #. Un archivo Markdown y su exportación a `.pdf` y `.odt` a través de Pandoc donde se incluyan elementos de marcado del lenguaje, con especial atención a aquellos más relevantes para la escritura académica: citas, notas al pie, referencias bibliográficas, etc.
  #. Un archivo Markdown en forma de presentación de `beamer` y su exportación a `.pdf` a través de Pandoc.
  
Por lo que respecta al plan de trabajo, el curso se organizarán en cuatro semanas de acuerdo con la siguiente temporalización:

## Semana primera

- Presentación general
- Procesadores y editores de texto
- El lenguaje Markdown
- Edición de ficheros Markdown
- Tarea n.º 1

## Semana segunda

- Introducción a Pandoc
- Pandoc: opciones aplicadas a la escritura académica
- La gestión de la bibliografía para la escritura en texto plano (introducción)
- Tarea n.º 2

## Semana tercera

- Presentaciones académicas con Markdown y Beamer
- La gestión de la bibliografía para la escritura en texto plano (continuación)
- Tarea n.º 3

## Semana cuarta

- Dudas y repaso de los contenidos abordados
- Ampliación
- Entrega de tareas pendientes
- Valoración del curso

# Requisitos técnicos^[Se ofrecerán recursos para facilitar la instalación de todos los programas necesarios, que son gratuitos.]

- Ordenador personal
- Editor de texto plano (preinstalado en la mayoría de sistemas operativos)
- Conexión a internet
- Instalación de Pandoc
- Un intérprete de la línea de comandos (preinstalado en la mayoría de sistemas operativos)
- Instalación de \LaTeX 
- Foro para la interacción entre alumnos y profesor

# Evaluación

El curso se superará en el caso de que todos los alumnos entreguen las [tareas](#tareas) y se consideren superadas.


\newpage
# Recursos y bibliografía




::: {#refs}
:::

\newpage

# Breve currículum del ponente{.unnumbered}

Carlos Martínez Domingo es graduado en Lengua y Literatura Españolas por la UNED y tiene el Título Superior de Música (especialidad de Interpretación-Guitarra) con mención de honor por el Conservatorio Superior de Música “Joaquín Rodrigo” de Valencia. Asimismo, ha seguido estudios de posgrado en la Escola Superior de Música de Catalunya con Àlex Garrobé y está realizando actualmente el doctorado en la UNED, bajo la dirección de la Dra. Clara I. Martínez-Cantón. Ha ejercido la docencia en institutos de educación secundaria y en conservatorios de música. En el campo de la investigación, está especialmente interesado en las relaciones música-literatura y en retórica literaria y musical, áreas sobre las que ha escrito artículos y presentado ponencias en varias universidades de España y Portugal. Como intérprete, ha actuado en diversas salas de concierto de España y Europa, tales como el Palau de la Música de Valencia, el Centre Cultural “La Beneficència” o el Arvo Pärt Centre (Laulasmaa, Estonia). Es miembro del proyecto de investigación +PoeMAS.


---
nocite: |
  @tenen2014, @atazlopez, @macfarlane2021, @macfarlane, @cone2022
...
