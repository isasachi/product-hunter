# 🔍 Product Hunter — Buscador de Productos Ganadores para Perú

Encuentra productos con alto potencial de venta que todavía no están saturados en el mercado peruano, usando la biblioteca de anuncios de Facebook como fuente de datos.

---

## ¿Qué necesitas para empezar?

1. Una cuenta en [Claude.ai](https://claude.ai) o tener instalado [Claude Code](https://claude.ai/code)
2. Unos 5 minutos

---

## Instalación

### Paso 1 — Descarga el proyecto

Si tienes Git instalado, abre una terminal y escribe:

```bash
git clone https://github.com/tu-usuario/product-hunter.git
cd product-hunter
```

Si no tienes Git, descarga el ZIP desde el botón verde de GitHub y descomprímelo.

### Paso 2 — Abre el proyecto en Claude Code

```bash
claude .
```

---

## Antes de hacer tu primera consulta

Es importante que el agente tenga cargado el archivo `AGENTS.md` en contexto. Ese archivo contiene todas las instrucciones de cómo debe buscar, filtrar y evaluar los productos.

**¿Cómo verificarlo?**

Al abrir Claude Code en este proyecto, el archivo `AGENTS.md` se carga automáticamente. Para confirmar que está activo, puedes escribirle al agente:

> *"¿Tienes cargado el AGENTS.md? ¿Qué instrucciones tienes para buscar productos?"*

Si el agente te responde describiendo el proceso de búsqueda (Meta Ads Library, filtros, evaluación), está todo listo.

---

## Ejemplos de uso

### Modo libre — buscar por tema

Escríbele al agente una palabra o frase corta relacionada al problema que resuelve el producto:

> *"busca productos para dolor de espalda"*

> *"quiero ver qué se está vendiendo para bajar de peso"*

> *"busca productos para hombres que quieren verse bien"*

El agente va a expandir esa idea en muchas palabras clave, buscar en países de LATAM, filtrar los anuncios con más de 10 días activos y más de 30 anuncios, y al final te entrega una lista con los productos más prometedores explicados de forma simple.

---

### Modo catálogo — analizar un PDF de importadora

Si tienes el catálogo de una importadora en PDF, súbelo directamente al chat y escribe:

> *"analiza este catálogo y dime qué productos tienen mejor potencial para vender en Perú"*

El agente revisa cada producto del catálogo contra la biblioteca de anuncios y te dice cuáles ya están funcionando afuera y todavía no llegaron al mercado local.

---

## ¿Qué te entrega el agente?

El agente genera un archivo HTML interactivo listo para abrir en el navegador. El archivo se guarda en la carpeta del proyecto con el nombre `productos-[keyword]-[fecha].html`.

La presentación tiene tres tipos de pantallas:

**Portada** — muestra el resumen de la búsqueda: cuántos productos se analizaron, cuántos países y cuántos tienen prioridad alta.

**Slide por producto (mínimo 10)** — cada producto tiene:
- Nombre, descripción y el problema que resuelve
- Métricas de validación: número de anuncios activos, días corriendo y cantidad de vendedores en el país de referencia
- Países donde se está pautando
- Situación en Perú: sin competencia / competencia baja / saturado
- Enlace directo a Meta Ads Library para verificar la señal
- Badge de prioridad: 🔥 Alta o 🟡 Media

**Slide de cierre** — tabla resumen con los 10 productos, su prioridad, la señal externa y el estado en Perú.

Navegás con las flechas del teclado ← → o con los botones en pantalla.

---

## Preguntas frecuentes

**¿Necesito saber programar?**
No. Solo necesitas escribirle al agente en lenguaje normal.

**¿El agente busca solo en Perú?**
No. Primero busca en México, Colombia, Chile, Argentina y Ecuador para ver qué ya está funcionando. Luego verifica si ese producto todavía no está en Perú.

**¿Por qué busca anuncios con más de 10 días?**
Porque nadie invierte plata en publicidad durante tantos días si el producto no está vendiendo. Es una señal de que funciona.

**¿Puedo cambiar los países de búsqueda?**
Sí. Solo díselo al agente: *"busca también en España"* o *"enfócate en Colombia y Chile"*.
