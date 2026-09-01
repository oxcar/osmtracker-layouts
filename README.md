# OSM Tracker Layouts

Este repositorio contiene plantillas personalizadas para mapeos usando la herramienta [OSMTracker](https://github.com/labexp/osmtracker-android).

Cada plantilla está disponible en español (`es`) e inglés (`en`).

## Plantillas

### Mapatón Oaxaca

Para el mapeo de rutas de transporte público en Oaxaca (México).

* 🚏 Parada informal
* 🚏 Parada oficial
* 🗒️ Nota de texto

### Mapatón Puerto Escondido

Para el mapeo de rutas de transporte público en Puerto Escondido, Oaxaca (México).

* 🚏 Parada informal
* 🚏 Parada oficial
* 🗒️ Nota de texto
* 📷 Fotografía

### Mapatón Salina Cruz

Para el mapeo de rutas de transporte público en Salina Cruz, Oaxaca (México).

* 🚏 Parada informal
* 🚏 Parada oficial
* 🗒️ Nota de texto

### Mapatón Tuxtla

Para el mapeo de rutas de transporte público en Tuxtla Gutiérrez, Chiapas (México).

* 🚏 Parada oficial
* 🚏 Parada informal
* 🗒️ Nota de texto

### Mapatón Zamora

Para el mapeo de rutas de transporte público en Zamora, Michoacán (México).

* 🚏 Parada informal
* 🚏 Poste
* 🚏 Poste + Techo
* 🚏 Poste + Techo + Banca
* 📷 Fotografía
* 🗒️ Nota de texto

## Instalación

En los ajustes de OSMTracker, en **Configuración del Repositorio GitHub**, apunta a este repositorio:

| Campo | Valor |
| --- | --- |
| Usuario | `oxcar` |
| Repositorio | `osmtracker-layouts` |
| Rama | `main` |

Después, en **Disposiciones para descargar**, elige la plantilla y descárgala. Queda disponible en **Disposición de los botones**.

## Estructura del repositorio

```
layouts/
  <nombre_plantilla>/
    es.xml                      # botones en español
    en.xml                      # botones en inglés
    <nombre_plantilla>_icons/   # iconos propios de la plantilla
      *.png
  metadata/
    <nombre_plantilla>.xml      # descripción mostrada en la app
```

Para agregar una plantilla nueva:

1. Crea la carpeta `layouts/<nombre_plantilla>/` con `es.xml` y `en.xml`.
2. **La carpeta de iconos debe llamarse exactamente `<nombre_plantilla>_icons`.** La app la busca en `layouts/<nombre_plantilla>/<nombre_plantilla>_icons`; con cualquier otro nombre los iconos no se descargan.
3. En el XML, el atributo `icon` incluye el nombre de esa carpeta: `icon="<nombre_plantilla>_icons/parada.png"`. En el dispositivo el XML queda junto a la carpeta de iconos, no dentro de ella.
4. Los iconos integrados de la app (`text.png`, `camera.png`) se referencian directamente, sin prefijo.
5. Agrega `layouts/metadata/<nombre_plantilla>.xml` con la descripción en ambos idiomas.

Los iconos son PNG cuadrados; en este repositorio se usan de 700×700 px.
