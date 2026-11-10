# EsquemIA

Figuras conceptuales editables, con cada etiqueta comprobada. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/esquemia/

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- Cuatro tipos de figura: diagrama de flujo (con decisiones y ciclos), mecanismo o vía (con iconos, flechas de activación e inhibición y compartimentos), graphical abstract por paneles y diagrama de estudio (CONSORT o PRISMA, con cajas laterales de exclusiones y pérdidas).
- Contenido a partir de una frase o de una frase y un texto de referencia (pegado o leído de Word, PDF con texto o texto). La figura puede rotularse en español, inglés o portugués.
- La IA propone solo la **estructura** (cajas, flechas, grupos, iconos de una lista cerrada de 20); el código la maqueta por capas o por paneles de forma determinista.
- **El código comprueba**: la cita literal de cada etiqueta en el texto de referencia y que sus cifras de dos o más dígitos están en él; flechas a cajas inexistentes, repetidas o sobre sí mismas, ids repetidos e iconos desconocidos (se descartan y se informa); cajas solapadas y flechas que atraviesan cajas; tamaño de letra para el destino (artículo a una o dos columnas, póster o diapositiva); contraste; y, en los diagramas de estudio, que el n de cada caja es igual a la suma de los n de las cajas a las que apunta.
- Editor visual: arrastrar cajas (quedan fijadas), editar texto, forma, color, icono, grupo y tipo de flecha, conectar, borrar, deshacer y reordenar.
- Cambios en lenguaje natural: la IA devuelve la figura modificada y el código muestra la diferencia (cajas y flechas nuevas, quitadas y cambiadas) antes de aplicarla.
- Colores propios o cargados desde un estilo de PosterIA.
- Descargas escritas en el navegador, sin red: SVG, PNG a 300 ppp para el destino, PDF vectorial y PowerPoint con cajas, flechas y textos editables; figura en JSON para seguir otro día.
- Cuatro ejemplos (uno por tipo) que funcionan sin clave en los tres idiomas.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

Todo se guarda en el navegador (IndexedDB). Al proponer o pedir un cambio salen hacia el proveedor elegido la frase, el texto de referencia (con correos, teléfonos y DNI/NIE enmascarados) y la estructura de la figura, sin posiciones. Antes del primer envío de la sesión se enseña una muestra y se pide confirmación. La figura guardada no lleva la clave.

## Límites

- El código no comprueba que la figura sea correcta en lo científico ni que una flecha signifique lo que dice. Sin texto de referencia, las etiquetas no se pueden verificar.
- Hasta 30 cajas; flechas rectas o en codo (los ciclos rodean la figura); maquetación automática sencilla (por capas con baricentros): en figuras complejas habrá que mover cajas a mano.
- La aritmética de CONSORT/PRISMA solo se comprueba en cajas cuyo texto lleva «n = X» y cuyos destinos también lo llevan.
- Iconos de una lista cerrada de 20; en PowerPoint van como imagen PNG.
- El PDF usa Helvetica estándar (WinAnsi): letras griegas, ≥ y otros símbolos se sustituyen (se avisa). Los tamaños mínimos de letra por destino son orientativos.
- Probado con IA simulada en Chromium (Playwright); PDF validado con qpdf y PowerPoint abierto con python-pptx. No probado con claves reales ni en PowerPoint de Microsoft.

## Inspiración

La función se inspira en el generador de figuras científicas de Yila AI (yila.ai); no se ha reutilizado su código.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche).


ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. (2026). *EsquemIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
