# Documento de decisiones de diseño

> Cada decisión: **qué** elegiste, **por qué**, y **qué alternativa descartaste**.
> Se evalúa la justificación, no la longitud. Máximo 2 páginas en la Fase 1.

## Ruta de trabajo

- [ ] Ruta A · Figma (enlace con permiso de lectura: …)
- [ ] Ruta B · VS Code (diseño directamente en `guia.html`)

## 1. Color (RA1 · CE b)

- Tono de acento de la ficha y cómo has obtenido la escala (50 … 950):
- Por qué el acento de texto/fondo es el 700 en claro y el 400 en oscuro (o el que elijas):
- Tokens semánticos añadidos y para qué:
- Pares de contraste añadidos a `$pares-contraste`:

## 2. Tipografía (RA1 · CE b)

- Familia elegida y por qué (rendimiento, legibilidad, licencia):
- Base y razón en móvil y escritorio. Por qué esas:
- Medida de línea (`max-inline-size` del párrafo en `ch`):

## 3. Espaciado y forma

- Escala de espaciado y radios. Si cambias algo respecto a la plantilla, por qué:

## 4. Componentes (RA1 · CE f)

| Componente | Estados | Cómo se resuelve cada estado en CSS |
| --- | --- | --- |
| Botón | normal, hover, foco, desactivado, secundario | |
| Turno | disponible, seleccionado, ocupado, foco | |
| Contador de invitados | | |
| Aviso de pago | | |

## 5. Comparativa de tecnologías (RA1 · CE e · RA2 · CE i)

| Criterio | Figma | Penpot | Diseño en código |
| --- | --- | --- | --- |
| Coste / licencia | | | |
| Traslado a código (handoff) | | | |
| Mantenimiento del sistema | | | |

| Criterio | Sass + CSS propio | CSS nativo sin preprocesador | Bootstrap / Tailwind |
| --- | --- | --- | --- |
| Tokens y temas | | | |
| Peso del CSS final | | | |
| Control de la cascada | | | |

**Decisión y motivo:**

La ruta de trabajo escogida sera la B -> VsCode.

1. Los colores escogidos de acento tienen el grado 22 (anaranjado). Cada uno de los acentos tiene una nivel de iluminación
diferente de mayor a menor. Acento-50 tiene una iluminacion del 95%, mientras que el acento-950 tiene una iluminación del 11%.
Para hacerlo utilice los colores con hsl y fui moviendo la iluminación.

El acento de texto/fondo es el 700 en claro y el 400 en oscuro. se necesita un acento mas claro en el fondo oscuro y un acento mas oscuro
sobre el fondo claro.

Se utilizan los tokens semánticos para no tener que usar los primitvos directamente. Al usar tokens si se realiza un cambio en los primitivos, no tienes que cambiarlo en todos los lugares en los que se usa.

2. He mantenido el que venia predefinido porque se ve bien

3. He mantenido los de la plantilla

4. Para los componentes he utilizado los estado que pedia el enunciado como :checked, :has :focus-visible :disabled
para establecer los estilos de cada uno de los estados. Se ha mantenido la especificidad de (0,2,0) que se exige en la
práctica.
