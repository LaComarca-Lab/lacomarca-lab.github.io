---
title: Trabajos de Fin de Grado
description: Algunas ideas para el curso 2024-2025
background: assets/theme/backgrounds/tfg_formulas.jpg
permalink: /tfgs.html
---

Mostramos aquí propuestas de líneas de investigación para los TFGs dirigidos por miembros de LaComarca, así como breves descripciones y/o artículos de referencia de los mismos.

## Medidas de centralidad en redes

- **Axiomas de la centralidad.**
    
    Revisar las bases de las medidas de centralidad, establecidas en <a href="https://www.internetmathematicsjournal.com/article/1564.pdf">este artículo</a>, así como discernir cuáles cumplen qué axiomas.
    
- **Correlación entre medidas de centralidad y activación de neuronas.**
    
    Revisar los principales modelos biofísicos de activación de neuronas (Hodgkin-Huxley, Leaky Integrate-and-Fire, FitzHugh-Nagumo, ...) así como <a href="https://www.worldscientific.com/doi/abs/10.1142/S0129065717500137">este artículo</a> que los correlaciona con medidas de centralidad en grafos, reproduciendo sus resultados y posiblemente extendiéndolos.


{% comment %}
- Otros temas de centralidad: catalogación de medidas de centralidad espectral (<a href="https://www.cambridge.org/core/journals/network-science/article/spectral-ranking/99ACDCD0CC1B774AB0041FB16AB43D1B">referencia</a>), monotonicidad de ranking en medidas de centralidad (<a href="https://www.cambridge.org/core/journals/network-science/article/rank-monotonicity-in-centrality-measures/A9862BBD3DE668985941D21C3F63259C">referencia</a>), ...
{% endcomment %}

## Dinámica

- **Sincronización de sistemas caóticos (Master Stability Function).**
    
    En los 90 se descubrió que, bajo ciertas condiciones, los sistemas caóticos pueden sincronizarse entre sí una vez se les deja interaccionar. No solo eso, sino que se estableció un marco analítico (la llamada "Master Stability Function") que permite predecir cuantitativamente cómo debe ser dicha interacción (<a href="https://doi.org/10.1016/j.physrep.2008.09.002">referencia</a>).

- **Sincronización de osciladores de fase (Kuramoto-Sakaguchi).**
    
    Muchos sistemas pueden ser modelados como osciladores periódicos, acoplados. El modelo de Kuramoto, originalmente propuesto para grafos completos, ha sido generalizado y estudiado en distintos ámbitos y con distintas topologías de red. A día de hoy sigue siendo el principal modelos de sincronización de fase. Este trabajo consistiría en una revisión del modelo (<a href="https://www.sciencedirect.com/science/article/pii/S0370157315004408?via%3Dihub">referencia</a>) y alguna exploración numérica relacionada.

- **Bifurcaciones en sistemas dinámicos.**
    
    Revisión de los sistemas dinámicos no lineales y la catalogación de sus soluciones, en función de su comportamiento cualitativo, y aplicaciones al modelado de sistemas reales (<a href="https://www.biodyn.ro/course/literatura/Nonlinear_Dynamics_and_Chaos_2018_Steven_H._Strogatz.pdf">referencia</a>).

## Machine Learning

{% comment %}
Graph Neural Networks para problemas con estructuras de grafos.
{% endcomment %}

- **Redes de Kolmogorov-Arnold (KAM).**

    Este mismo año un artículo causó conmoción en la comunidad de investigación en redes neuronales, con la publicación de <a href="https://arxiv.org/abs/2404.19756">este preprint</a> sobre el uso del Teorema de representación de Kolmogorov-Arnold en lugar del Teorema de Aproximación Universal en tareas de Deep Learning, lo cual parece ser que mejora tanto la funcionalidad como la interpretabilidad. En este trabajo se entenderían los fundamentos teóricos subyacentes (ambos teoremas) y se propondría algún experimento numérico de comparación. 

- **Reservoir Computing para series temporales.**

    Hace unas décadas se propuso un nuevo tipo de estructura de aprendizaje automático, las llamadas "echo state networks", que se han utilizado con bastante éxito para tareas relacionadas con las series temporales debido a su sencillez: contrastado con el paradigma actual de redes neuronales, en estas estructuras se inicializa una red intermedia fija, con topología arbitraria, y el entrenamiento simplemente actualiza los pesos desde y hacia la red intermedia (<a href="https://martinuzzifrancesco.github.io/posts/a-brief-introduction-to-reservoir-computing/">referencia</a>).

- **Análisis de subtipos en el cáncer de vejiga.**

    El cáncer de vejiga es el cáncer del sistema urinario más frecuente en los Estados Unidos, con aproximadamente 82000 nuevos casos y 17000 muertes por año. Este es clasificado en “Non-Muscle-Invasive Bladder Cancer (NMIBC)” and “Muscle-Invasive Bladder Cancer (MIBC)” siendo este último el más agresivo. Además, este tipo de cánceres, MIBC, son altamente heterogéneos a nivel molecular por lo que hace más difícil su tratamiento. Por lo tanto, encontrar similitudes (subtipos) según la expresión del gen es de vital importancia, pudiendo estar relacionado con la supervivencia del paciente o la respuesta a terapias. 

    - Utilizando Redes Complejas:
        En este TFG el alumno aprenderá técnicas de redes complejas y comunidades/agrupamientos utilizando datos sobre el cáncer de vejiga. En concreto, utilizando medidas entre rankings (Spearman, Kendal Tau…) de la expresión de sus genes, el alumno podrá calcular similitudes entre los pacientes y construir así un grafo con el que encontrar los subtipos aplicando el algoritmo de Girvan-Newman.

    - Utilizando Machine Learning:
        En este TFG el alumno aprenderá técnicas de machine learning utilizando datos sobre el cáncer de vejiga. En concreto, utilizando la distancia entre la expresión de sus genes, el alumno podrá aplicar los algoritmos K means y Hierarchical para determinar los subtipos de dos formas distintas. Además, utilizando Principal Component Analysis podrá ilustrar los clusterings en el plano.

## Otros

- **Ciberseguridad.**
    
    Predicción de ciberataques a partir de datos espaciotemporales de IPs, e identificación de atacantes (<a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0124472">referencia</a>).

- **Redes simpliciales y el Laplaciano de Hodge.**
    
    Últimamente se están utilizando conceptos de (co)homología (cadenas, co-cadenas, operadores de borde, etc) para generalizar problemas clásicos de redes complejas, desde centralidad (<a href="https://link.springer.com/article/10.1007/s10107-010-0419-x">referencia</a>) hasta sincronización (<a href="https://arxiv.org/abs/2305.17977">referencia</a>). El estudiante podría escoger el que más le interese, reproduciendo los cálculos y realizando simulaciones numéricas.

- **Análisis de datos basado en técnicas topológicas.**
    
    La homología persistente es una de las principales técnicas de análisis topológico de datos (TDA en ingles), consistente en la construcción de una estructura (un "filtrado") a partir de una colección de datos, de la que se puede extraer información como las clases de homología o los números de Betti para cada etapa del filtrado (obteniendo un "código de barras persistente") relevante para aspectos prácticos (<a href="https://link.springer.com/article/10.1007/s10462-022-10146-z">referencia</a>)

{% comment %}
- Grafos y diagramas de Voronoi
- Redes complejas en cosmología

- **Fibrados en grafos.**
    
    Los fibrados son estructuras matemáticas fundamentales en geometría diferencial y algebraica, y hay una extensión de estos en la teoría de grafos (<a href="https://www.sciencedirect.com/science/article/pii/S0012365X00004556">referencia</a>).

{% endcomment %}

Si te interesa algún otro tema que no está incluido en esta lista, pero que crees que temáticamente es cercano a nuestro grupo, no dudes en preguntarnos al respecto, y seguramente podemos encontrarle hueco.