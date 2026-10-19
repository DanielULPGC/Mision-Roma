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
| 3.6.1 | Incluir `modelo/hand_landmarker.task` aportado por la usuaria (descarga oficial de Google) | Tamaño (7 819 105 bytes) y huella SHA-256 idénticos a los esperados; el detector arranca con él | Mantener el modelo fuera del repositorio |
