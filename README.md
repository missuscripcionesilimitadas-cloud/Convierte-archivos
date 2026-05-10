# DocConvert — Conversor de Documentos

Aplicación web progresiva (PWA) para convertir documentos entre formatos.

## Formatos soportados

| Origen  | → EPUB | → PDF | → TXT |
|---------|--------|-------|-------|
| PDF     |   ✓    |   —   |   ✓   |
| DOCX    |   ✓    |   ✓   |   ✓   |
| TXT     |   ✓    |   ✓   |   —   |
| EPUB    |   —    |   ✓   |   ✓   |

## Instalación en Android

### Opción A — Desde Chrome (recomendado)
1. Abre `index.html` en Chrome
2. Toca el menú ⋮ → "Agregar a pantalla de inicio"
3. La app aparecerá como cualquier aplicación instalada

### Opción B — Servidor local con Python
```bash
cd converter-app
python3 -m http.server 8080
```
Luego abre `http://localhost:8080` en el navegador.

### Opción C — Despliegue en servidor
Sube todos los archivos a cualquier servidor web estático (Netlify, GitHub Pages, Firebase Hosting, etc.)

## Archivos incluidos

```
converter-app/
├── index.html       ← App principal
├── manifest.json    ← Configuración PWA
├── sw.js            ← Service Worker (modo offline)
├── icon.svg         ← Icono de la app
└── README.md        ← Este archivo
```

## Características

- ✅ Sin servidor — todo se procesa localmente en el dispositivo
- ✅ Funciona sin internet (modo offline) una vez instalada
- ✅ Historial de conversiones recientes
- ✅ Compatible con Android, iOS, Windows, macOS, Linux
- ✅ Compartir archivos directamente desde la app (Android)
- ✅ Temas oscuro optimizado para batería AMOLED

## Tecnologías utilizadas

- [PDF.js](https://mozilla.github.io/pdf.js/) — Lectura de PDFs
- [Mammoth.js](https://github.com/mwilliamson/mammoth.js) — Lectura de DOCX
- [JSZip](https://stuk.github.io/jszip/) — Generación/lectura de EPUB
- [jsPDF](https://github.com/parallax/jsPDF) — Generación de PDFs

---
Creado con DocConvert v1.0
