<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logotipo de bestimage.ai"></a></p>

# Awesome Wan 3.0 Prompts — Guía en español

**148 propuestas de dirección de vídeo en 14 categorías, adaptadas y mantenidas por el equipo de [bestimage.ai](https://bestimage.ai/).** Define un acontecimiento claro, asigna una función a cada entrada y dirige la cámara, el sonido y la continuidad.

[Guía en inglés](README.md) · [Las 15 lenguas](locales/README.md) · [Índice completo](prompts/README.md) · [Contribuir](CONTRIBUTING.md)

![Ilustración conceptual de un archivista que abre un mapa estelar en un observatorio al amanecer](assets/wan-3-prompt-collection-hero.png)

*Ilustración estática creada con la herramienta integrada de generación de imágenes, no un vídeo generado con Wan 3.0. Consulta las [instrucciones de imagen y su procedencia](assets/README.md).*

## Qué incluye y cómo empezar

**148 propuestas de dirección de vídeo en 14 categorías**. Las seis primeras categorías contienen instrucciones de dirección en chino; las ocho restantes, en inglés. Hay guías de entrada y un ejemplo comparativo en 15 idiomas, **no traducciones completas de las 148 propuestas**. Las traducciones y el ejemplo comparativo no cuentan como entradas adicionales.

1. Elige una propuesta en el [índice completo](prompts/README.md).
2. Ajusta las variables y prepara las entradas necesarias. Las referencias describen funciones; el repositorio no incluye esos archivos.
3. Elige la modalidad y configura duración, relación de aspecto, resolución y sonido en la interfaz. Escribirlos en el texto no configura la solicitud de API.
4. Genera una prueba pequeña y revisa acción, geometría, identidad, tiempos y sonido según el objetivo de revisión de la propuesta.

## Fórmula de ocho capas

```text
[Salida] duración + relación de aspecto + medio visual
[Sujeto] rasgos de identidad reutilizables + detalles inmutables
[Entorno] momento + lugar + clima + profundidad espacial
[Acción] detonante → movimiento continuo → resultado visible
[Cámara] plano + ángulo + un recorrido + encuadre final
[Aspecto] luz + paleta + materiales + tratamiento del movimiento
[Sonido] ambiente + efectos + música + diálogo
[Restricciones] elementos que deben mantenerse + errores más probables
```

Usa un idioma principal para la descripción visual y especifica por separado el idioma, las palabras exactas y los turnos del diálogo. No dupliques toda la instrucción en varios idiomas. Las funciones disponibles dependen del producto, la región y los controles de la plataforma.

## Ejemplo comparativo completo

**Modalidad:** texto a vídeo · **Configuración:** 10 segundos, 16:9, sonido activado · **Entradas:** ninguna

```text
Crea una toma documental de 10 segundos en formato 16:9 en un tranquilo centro comunitario de préstamo de herramientas. Una persona adulta voluntaria, de pelo corto y rizado, con un delantal color mostaza y una camisa azul marino de mangas remangadas, repara un pequeño ventilador de mesa rojo que está desenchufado. De 0 a 3 segundos, coloca la rejilla protectora desmontada junto al ventilador inmóvil. De 3 a 7 segundos, limpia el polvo de una de las aspas con un paño suave mientras la cámara se desliza lentamente hacia la derecha a la altura de la mesa. De 7 a 10 segundos, deja el paño y alinea la rejilla con la carcasa, sin enchufar ni encender el ventilador. La luz de la ventana revela el metal desgastado y la textura del algodón. Sonido: roce del paño, un clic suave de la rejilla y ambiente tranquilo de la sala; sin voz ni música. Conserva la misma persona, el mismo ventilador, sus tres aspas, la carcasa roja y el cable desenchufado. Sin aspas girando, herramientas adicionales, etiquetas legibles, subtítulos ni cortes.
```

**Variables:** color del delantal, color del ventilador e iluminación de la sala. **Revisión:** el ventilador permanece desenchufado e inmóvil; el número de aspas y el contacto de las manos se mantienen coherentes. Es un concepto creativo, no una instrucción de reparación eléctrica.

## Categorías

| Categoría | Propuestas |
|---|---:|
| [Narrativa cinematográfica](prompts/cinematic-storytelling.md) | 8 |
| [Publicidad y productos](prompts/ads-and-products.md) | 8 |
| [Contenido de usuarios, comida y viajes](prompts/ugc-food-travel.md) | 8 |
| [Acción y deporte](prompts/action-sports.md) | 8 |
| [Animación y fantasía](prompts/anime-fantasy.md) | 8 |
| [Música, comedia y redes sociales](prompts/music-comedy-social.md) | 8 |
| [Empresa y servicios públicos](prompts/professional-business.md) | 13 |
| [Educación y ciencia](prompts/education-science.md) | 13 |
| [Arquitectura, hostelería y movilidad](prompts/architecture-mobility.md) | 13 |
| [Control de producción y edición](prompts/production-control.md) | 13 |
| [Comercio, belleza y venta minorista](prompts/commerce-beauty-retail.md) | 12 |
| [Personas, diálogo y localización](prompts/people-dialogue-localization.md) | 12 |
| [Naturaleza, animales y estaciones](prompts/nature-animals-seasons.md) | 12 |
| [Industria y fabricación](prompts/industrial-manufacturing.md) | 12 |

## API de Wan 3.0 en bestimage.ai

Estas páginas en inglés permiten consultar la interfaz de prueba y los ejemplos públicos de solicitudes.

| Modalidad | Entradas y propósito |
|---|---|
| [Texto a vídeo](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Descripción completa de una escena, con causa, acción intermedia y resultado visible. |
| [Imagen a vídeo](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Imágenes inicial **y final** para la modalidad documentada; describe la transición y conserva geometría y composición. |
| [Referencias a vídeo](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Referencias opcionales de identidad, objetos, espacio, movimiento o sonido; asigna una función a cada recurso. |
| [Edición de vídeo](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Vídeo original y un cambio acotado; conserva interpretación, duración, cámara y zonas no modificadas. |

Consulta la [guía de API y control de costes](guides/bestimage-wan-3-api.md) para las solicitudes, la consulta del estado de las tareas y la planificación de pruebas. **El servidor de API de bestimage.ai es `https://api.flaq.ai`.** Usa una clave de API emitida desde tu cuenta de bestimage.ai.

Consulta la página del modelo y tu cuenta antes de gastar créditos. Estas modalidades son las documentadas por bestimage.ai; no implican que todos los productos Wan ofrezcan los mismos controles.

## GPT Image 2 para preparar fotogramas de referencia

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) genera imágenes estáticas; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) edita imágenes y combina referencias visuales. Sirven para preparar fichas de personajes, referencias de productos o composiciones iniciales y finales antes de una tarea de vídeo.

Son **modelos de imagen independientes**, no interfaces de vídeo de Wan. Exporta y revisa las imágenes antes de usarlas como entradas en la modalidad Wan adecuada. El repositorio no automatiza este paso ni afirma que las ilustraciones conceptuales se generaran con esas API. Consulta el [flujo de preparación de referencias](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Guías y contribuciones

Las guías de [escritura de instrucciones](guides/prompting-guide.md), [capacidades y límites](guides/model-capabilities.md) y [solución de problemas](guides/troubleshooting.md) están en chino simplificado. La guía de API está en inglés. Las imágenes conceptuales no demuestran continuidad temporal, sincronización labial, precisión del modelo ni seguridad de los procesos representados.

Lee las [instrucciones de contribución](CONTRIBUTING.md) antes de compartir propuestas o archivos. Incluye configuración exacta, función de las entradas, derechos de uso, observaciones y una indicación honesta de si se ha probado. No compartas credenciales, documentos privados ni enlaces de medios firmados que caduquen. Usa el [formulario de propuestas](.github/ISSUE_TEMPLATE/prompt.yml) para preparar la información necesaria.

## Acerca de bestimage.ai

El equipo de [bestimage.ai](https://bestimage.ai/) selecciona y mantiene esta biblioteca de prompts, que conecta flujos de trabajo creativos con API de modelos de imagen y vídeo.

## Gana con el programa de afiliados de bestimage.ai

¿Publicas tutoriales, prompts o integraciones de API? Únete al [programa de afiliados de bestimage.ai](https://bestimage.ai/affiliate-program/) y gana comisiones al recomendar bestimage.ai a tu audiencia.

- **20 %** sobre el primer pedido de pago válido de cada usuario referido.
- **10 %** sobre sus pedidos de pago válidos posteriores, realizados durante los **60 días siguientes a su registro**.

Los requisitos de los pedidos y los pagos se rigen por el [acuerdo de afiliación vigente](https://bestimage.ai/affiliate-agreement/).

## Licencia

[MIT](LICENSE).
