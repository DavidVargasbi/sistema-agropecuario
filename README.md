# 🌱 AgroVisión Antioquia

Prototipo de **analítica agrícola** para los 125 municipios de Antioquia (Colombia). Ayuda a decidir **qué sembrar, cuándo sembrar, cuándo cosechar, dónde vender y qué tan rentable** puede ser cada producto, según ubicación geográfica, piso térmico, precios, demanda, exportación y comportamiento del mercado.

Es un sitio **100% estático** (un solo `index.html` autosuficiente). No requiere build, servidor ni base de datos. Se despliega directo en Vercel.

---

## 🗂 Estructura del proyecto

```
agrovision-antioquia/
├── index.html      ← Tablero principal (mapa analítico interactivo)
├── propuesta.html  ← Propuesta estratégica (ruta /propuesta)
├── vercel.json     ← Configuración (URLs limpias)
├── .gitignore
└── README.md
```

---

## 🚀 Cómo desplegar en Vercel

1. Sube esta carpeta a un repositorio de **GitHub**.
2. En **vercel.com** → *Add New… → Project* → importa el repositorio.
3. **Framework Preset:** `Other` · **Build Command:** vacío · **Output Directory:** vacío (raíz).
4. *Deploy*. Vercel detecta `index.html` en la raíz y publica el sitio.

> Cada vez que hagas *push* a GitHub, Vercel vuelve a desplegar automáticamente.

---

## 🧭 Qué incluye el tablero

- **Mapa analítico interactivo:** 9 subregiones coloreables por indicador (piso térmico, rentabilidad, precio, oferta, riesgo), 125 municipios localizados dentro de su subregión, puntos de comercialización (Central Mayorista, Plaza Minorista, acopios regionales), *tooltips* al pasar el cursor y **gráficas vinculadas** que cambian al seleccionar una zona.
- **Filtro por familia agrícola:** Frutales y Pasifloras · Tubérculos y Plátanos · Granos, Cereales y Oleaginosas · Hortalizas, Verduras y Flores.
- **Calculador siembra → cosecha → venta** con ciclo del cultivo y ventana comercial.
- **Precios COP / USD** con TRM oficial editable.
- **Panel de exportación** con cifras reales 2025.
- **Explorador de los 125 municipios** (búsqueda y filtros).
- **Centro de conocimiento** (propuesta completa, modelo de IA, fuentes, roadmap).

---

## ⚠️ Honestidad de datos (importante)

Este prototipo **separa con claridad lo real de lo ilustrativo**:

**Datos REALES y verificados**
- División territorial: 9 subregiones y 125 municipios (Ordenanza 41/1975 · Anuario Estadístico de Antioquia).
- Pisos térmicos (clasificación de Caldas) y vocación productiva por subregión.
- Exportación 2025: Antioquia lidera el aguacate Hass (≈47% nacional, US$177,4 M, +50,2%); banano es la 1ª fruta de exportación; destinos en Europa (Países Bajos 35,8%, España, Alemania) y EE.UU.; producción de aguacate de Antioquia 1,67 M t (2024).
- TRM oficial: $3.667,06 COP/USD (26 may 2026).

**Datos ILUSTRATIVOS / DEMO (claramente etiquetados)**
- Precios por producto, proyecciones, rentabilidad, riesgo y oferta/demanda (motor sintético consistente).
- **Posiciones de los municipios en el mapa:** son esquemáticas dentro de su subregión real. Para volverlas geográficamente exactas se cargan los centroides/polígonos oficiales de **IGAC/DANE** (GeoJSON).

**Vacíos a completar con fuentes oficiales**
- Producto y precio por municipio → **EVA** (UPRA / datos.gov.co).
- Coordenadas exactas de municipios y plazas → **IGAC / DANE / Gobernación**.
- Empresas exportadoras y volúmenes por empresa → **DIAN / Legiscomex / Cámaras de Comercio**.

---

## 📚 Fuentes

DANE/SIPSA · EVA (UPRA/datos.gov.co) · IDEAM · IGAC · Agronet · ProColombia · Analdex · Corpohass · DIAN · Banco de la República (TRM) · Gobernación de Antioquia.

---

*Prototipo de demostración. Las cifras demo se reemplazan por datos reales al conectar las fuentes anteriores.*
