# 🌱 AgroData · BI Consulting Lab · v5.4 (Tour reparado)
> *Inteligencia que cultiva el futuro*

## ✅ v5.4 — Fixes críticos del tour
La versión 5.3 del tour tenía 3 bugs serios que dejaban la app congelada:

1. **Spotlight no era real** — solo era un anillo dorado, el mask oscuro tapaba el elemento debajo. AHORA: el spotlight tiene `box-shadow:0 0 0 9999px` que crea un "hueco" real, donde se ve y se puede interactuar con el elemento resaltado.

2. **Bucle recursivo de scroll** — si un elemento estaba fuera de viewport, `renderTourStep` se llamaba a sí mismo sin límite, colgando la app. AHORA: solo 1 reintento de scroll, después fallback automático.

3. **Mask bloqueaba toda la app** — el overlay con `pointer-events:auto` impedía cualquier clic. AHORA: el overlay es `pointer-events:none`; solo el tooltip captura clics.

Otros arreglos:
- CSS y JS sincronizados (ambos usan clase `.on`)
- Fallback a centrado si el target no existe o tiene tamaño 0
- `endTour()` limpia TODAS las clases para no dejar estado fantasma
- Aumentado el delay de cambio de tab a 450ms (era 280ms, muy corto)
- Reposición con `requestAnimationFrame` en lugar de setTimeout
