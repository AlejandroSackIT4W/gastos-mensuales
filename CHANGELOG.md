# Changelog — Mis Gastos App

## [1.5.0] — 2026-05-06

### ✨ Nuevo
- **Sync Firebase automático:** la config de Firebase queda hardcodeada en la app. Al abrir, conecta solo sin necesidad de configurar nada. Si se borra el caché, los datos se recuperan solos desde Firestore.
- **Pill de estado sync:** reemplaza el puntito por una pill en el header con texto (`Sincronizando...` / `Conectado` / `Sin conexión`) y punto de color indicador.

### 🐛 Fix
- **Tabs fijas al scrollear:** las 3 pestañas ya no bajan con el scroll. Se migró el layout a flexbox (`body` como flex column, scroll solo en `.content`).
- **Drag & drop mobile:** se corrigió el contenedor de scroll para SortableJS, se aumentó el delay a 300ms y se agrandó el handle para mejor UX en mobile.
- **Emoji Mascotas roto:** el emoji 🐾 en Gastos Generales aparecía como `??` al guardar. Corregido encoding del `value` del `<option>`.
- **Renombre servicio:** "Fútbol (hijo)" → "Fútbol".

---

## [1.4.0] — 2026-05-04

### ✨ Nuevo
- **Sección Pagados/Pendientes:** al confirmar un pago, la tarjeta se mueve automáticamente a la sección verde "Pagados". Ambas secciones son reordenables con drag.
- **Drag & drop en tarjetas:** reordenamiento manual de servicios con el dedo en mobile (SortableJS). El orden se guarda y sincroniza.
- **Sincronización Firebase (modal):** integración opcional con Firebase Firestore para sync en tiempo real entre dispositivos.
- **Favicon:** ícono 💰 sobre fondo azul, funciona en barra de favoritos y como acceso directo en home screen.

### 🐛 Fix
- **Dark mode — tarjeta sumatoria:** en dark mode la tarjeta azul pasaba a ámbar. Corregido a gradiente azul marino oscuro consistente.
- **Dark mode — header banner:** mismo criterio de color que la tarjeta en dark mode.

---

## [1.3.0] — 2026-05-04

### ✨ Nuevo
- **Pestaña Gastos Generales:** calendario mensual navegable con vista diaria de gastos. Los días con gastos muestran el monto en verde. Toque en cualquier día abre modal para agregar/ver gastos del día.
- **Toggle dark/light mode:** botón 🌙/☀️ en el header. Preferencia guardada en localStorage.
- **Renombre pestaña:** "Servicios" → "Gastos Fijos".

---

## [1.2.0] — 2026-05-04

### ✨ Nuevo
- **GitHub Pages:** app publicada en `https://alejandrosackit4w.github.io/gastos-mensuales/` — accesible desde cualquier dispositivo sin necesidad de tener la PC encendida.

### 🐛 Fix
- **Regla de firewall:** se habilitó el puerto para acceso desde la red local (celular en la misma WiFi).

---

## [1.1.0] — 2026-05-04

### 🐛 Fix
- **INICIAR.bat colapsaba:** corregidos caracteres de codificación incorrectos y agregado `pause` para que la ventana no cierre inmediatamente.

---

## [1.0.0] — 2026-05-04

### ✨ Inicial
- App web de seguimiento de gastos mensuales accesible desde el celular.
- **Gastos Fijos:** lista de servicios predefinidos (Luz, Gas, Internet, Datos móviles, Monotributo, Fútbol, Tarjetas Uala y MercadoPago, Municipales, Patente, Agua corriente, Agua en bidón).
- Check de pagado con registro de monto por servicio.
- Sumatoria mensual con conteo de pagados/pendientes.
- Navegación por mes (anterior/siguiente).
- Posibilidad de agregar servicios personalizados con ícono.
- Servidor local (`INICIAR.bat`) para acceso en red WiFi.
