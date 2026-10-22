# Registro de decisiones · «Las manos que construyeron la historia»

Protocolo ARQ-3D-01, fase 3, adoptada de forma parcial. Las decisiones están ordenadas por versión.

| Versión | Decisión | Motivo | Alternativa descartada |
|---|---|---|---|
| Prototipo | Abandonar MindAR con marcador | La mano tapaba el marcador y la pendiente estaba exagerada sin aviso | Mantener el marcador de demostración |
| 2.0 | Realidad aumentada «espejo» con cámara frontal y pinza normalizada por el tamaño de la mano, con histéresis | La interacción con las manos es el núcleo del proyecto | Cámara trasera con marcador |
| 2.1 | Presentar como debatida la cifra de pendiente de Vitruvio | Los manuscritos no coinciden (Lewis, 1999) | Dar una cifra única |
| 2.2 | Paquete autoalojado (librerías y WASM locales, con SRI) y `PERMITIR_MODELO_REMOTO = false` | Privacidad del alumnado; ninguna petición externa | Cargar desde CDN |
| 3.0 | Cinco etapas evolutivas por capítulo, que se desbloquean en orden | Indicación de la usuaria: el proceso evolutivo es la idea central | Actividad única |
| 3.1 | Portada con línea del tiempo, de la Prehistoria en adelante, y navegación hacia atrás | Indicación de la usuaria | — |
| 3.2 | Arrastre relativo con ganancia 0,5 e imanes de ajuste | Precisión con el temblor real de la mano | Posición absoluta |
| 3.4 | Motor gráfico de calidad alta con texturas procedurales y degradación automática | Calidad visual sin descargar imágenes; rendimiento en tabletas | Texturas fotográficas externas |
| 3.5 | Bifaz con talla bifacial y córtex; cerámica cardial grabada en la superficie y ordenada en franja; decorados por etapa | Observaciones de la usuaria sobre la verosimilitud arqueológica | — |
| 3.5.1 | Pintadera basada en el catálogo de El Museo Canario: partes, formas, técnicas y esquemas pautados; estampación en reflejo y en negativo | Documento aportado por la usuaria | Pintadera circular genérica |
| 3.6 | No incluir el modelo de manos en el repositorio | Su integración quedó bloqueada por seguridad, al proceder de copias de terceros. Se documenta su huella y el diagnóstico comprueba el archivo descargado | Subir una copia de terceros |
| 3.6 | Comprobar la huella SHA-256 del modelo en el diagnóstico | Integridad del archivo que suba el centro | Comprobar solo el tamaño |
| 3.6 | Pared de la cueva integrada en un macizo rocoso | El panel rectangular restaba verosimilitud | — |
| 3.6 | Pintadera: excisión y forma rómbica | Completan las técnicas y formas del catálogo (excisión en 60 piezas; rómbica en 3) | — |
| 3.6 | Precisar el poblamiento de Canarias: estable hacia los siglos II-III d. C., en debate | Velasco Vázquez et al. (2020), dataciones de vida corta | «Hace unos dos mil años», sin matiz |
| 3.6 | Declarar que Prehistoria y Edad Antigua son saberes de Historia del segundo ciclo en el currículo canario | Contraste con el Anexo 2 del Decreto 211/2022 | Silenciar el desajuste de ciclo |
| 3.7 | Capítulos de la Edad Moderna («Nuevos horizontes») y de la Edad Contemporánea («Hierro, luz y viento»), cinco etapas cada uno, con una etapa final en Canarias | Completar la línea del tiempo; encajan de lleno en el saber III.2.1 del tercer ciclo | Dejarlos «en preparación» |
| 3.7 | Señalar la discrepancia entre ediciones del Diario de Colón sobre qué carabela cambió las velas | Honestidad sobre la fuente: unas ediciones dicen la Niña y otras la Pinta | Afirmar una sola versión |
| 3.7 | Presentar como modelos los destellos del faro, la viga del puente, el mecanismo del ingenio y las cifras de energía | No se han verificado las características reales; se declaran en la actividad | Atribuir datos no comprobados |
| 3.6.1 | Incluir `modelo/hand_landmarker.task` aportado por la usuaria (descarga oficial de Google) | Tamaño (7 819 105 bytes) y huella SHA-256 idénticos a los esperados; el detector arranca con él | Mantener el modelo fuera del repositorio |
| 3.8 | Pistas graduadas en dos niveles por etapa, que no dan la respuesta hecha; el botón se ilumina tras dos errores o 45 s sin avances | Auditoría de jugabilidad: el alumnado que se atasca no tenía más ayuda que el texto de estado | Mostrar la solución |
| 3.8 | Anillos de agarre solo donde lo que se mueve no es la respuesta; se ocultan en el valle (Roma 1), el arco (Media 2), el bifaz, la mano de la cueva, la ciudadela y el portulano | Las pinzas fallidas eran la principal fuente de frustración, pero señalar el lugar exacto resolvería la tarea | Anillos en todas las etapas |
| 3.8 | Onda verde o naranja tras cada pinza, y ayuda tras tres pinzas sin efecto | La pinza real no daba ninguna respuesta cuando no tocaba nada | Sin respuesta visual |
| 3.8 | Sonido sintetizado, suave, desactivable y recordado; ningún mensaje depende solo del sonido | Refuerzo inmediato sin descargar archivos y sin perjudicar a quien no oye o trabaja en silencio | Archivos de audio; sonido obligatorio |
| 3.8 | Confeti solo si el sistema no pide reducir el movimiento | Accesibilidad (WCAG 2.3.3) | Animación siempre |
| 3.8 | Faro: controles separados para los haces (linterna, arriba-abajo) y para los segundos por vuelta (relojería, a los lados) | Un solo gesto en dos ejes cambiaba dos variables a la vez y resultaba poco intuitivo | Mantener el gesto doble |
| 3.9 | Página de bienvenida con la mano en negativo como primera experiencia y «Pasaporte del aprendiz» como hilo entre capítulos | Indicación de la usuaria (combinar la portada de la mano y el pasaporte); la mano es el símbolo del proyecto y el pasaporte da continuidad entre sesiones | Landing informativa sin interacción |
| 3.9 | Sin cámara en la bienvenida: la mano es un dibujo | Privacidad y arranque inmediato; la cámara queda para los capítulos, cuando se elige | Detectar la mano real |
| 3.9 | Ideas previas sin nota, contrastadas al completar el capítulo | Activar conocimientos previos y hacer visible el cambio de idea; evitar la lógica de examen | Cuestionario con puntuación |
| 3.9 | La bienvenida se añade como página nueva y se enlaza desde la portada; `index.html` sigue siendo la entrada del sitio | Cambio conservador: no altera los enlaces ni los marcadores existentes | Sustituir la portada |
| 3.9.1 | La bienvenida es la pantalla de inicio: `index.html` sin parámetros redirige a ella y la línea del tiempo queda en `index.html#linea` | Indicación de la usuaria. Se conserva `index.html` como motor común de los capítulos y se evita cualquier bucle: los capítulos vuelven a `#linea`, y `?docente` y `?diagnostico` no pasan por la bienvenida | Renombrar `index.html` (rompería los constructores y los enlaces de los capítulos) |
