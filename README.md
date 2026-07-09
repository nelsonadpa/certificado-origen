# Certificado de Origen — Cuba · demo narrado bilingüe

Presentación narrada, auto-reproducible y bilingüe (ES/EN) del servicio **Certificado de
Origen** de Cuba, emitido por la **Cámara de Comercio de la República de Cuba** sobre la
plataforma eRegistrations (VUCE — Ventanilla Única de Comercio Exterior).

Sigue el patrón de [uganda-demo](https://github.com/unctad-ai/uganda-demo) y
[roe-colombia-demo](https://github.com/nelsonadpa/roe-colombia-demo): un MP3 de narración
por slide, el audio es el reloj, el slide avanza al terminar el clip, HTML estático puro.

- **Español:** `index.html` · **Inglés:** `en.html` (el selector conserva el slide vía `#N`).
- 15 slides · voz cubana · subtítulos alineados · barra de progreso · controles y teclado
  (← → espacio) · heartbeat de esquina reactivo a la voz (WebAudio).

## La historia
Primera persona: el/la **gerente de una empresa exportadora cubana grande**. Antes, el
certificado de origen era un trámite presencial en la Cámara de Comercio, con modelos en
papel por acuerdo/país; hoy se resuelve en línea. El recorrido muestra: empresa → país
destino e importador → producto y subpartida arancelaria → **acuerdo comercial que decide
el tipo de certificado** (ALADI / SGP / Normal) → operación y factura → certificado digital
bilingüe con QR de verificación → bases de datos e intercambio de datos → beneficios.

## Qué es REAL y qué es ILUSTRATIVO
- **Real (capturas y config en vivo por MCP):** la portada, el login y el catálogo del
  portal `cuba.eregistrations.dev`; la estructura y las etiquetas del formulario; el texto
  bilingüe y el layout del **certificado**, calcados del print document real "Certificado
  Normal" (`a270e443`) y "Certificado ALADI" (`ada012a5`) del servicio
  `8a2b5457-9656-424e-9e34-f09c27bed997` (v97).
- **Reconstruido fielmente (no captura):** las pantallas del formulario autenticado se
  reconstruyen como mockups a partir de la config real (campos y etiquetas verdaderos), no
  son screenshots del flujo logueado.
- **Ilustrativo (datos de ejemplo, coherentes entre sí):** la empresa "CUBAEXPORT S.A.",
  el importador mexicano, el ron 2208.40, los pesos/valor FOB y el número de certificado
  CO-2026-1487. El **QR** ilustra la verificación digital (dirección eCO / ISO/IEC 18004);
  el certificado en papel real hoy no lleva QR.

## Voz
- **Claudia — Relaxed, Natural and Warm** (acento cubano, ElevenLabs, `tGaqHUoNeMUctS0nje4o`).
- La misma voz narra ambos idiomas con `eleven_multilingual_v2` (en inglés conserva el acento).
- **Regenerar clips:** `export ELEVENLABS_API_KEY=$(security find-generic-password -s elevenlabs -w)`
  y `python3 gen_audio.py` (o `gen_audio.py es` / `gen_audio.py en`). El texto de cada slide
  está en `gen_audio.py` (arrays `ES` / `EN`), alineado con el array `NARR` de cada HTML.
  `gen_audio.py` no está publicado (contiene los guiones de trabajo); la key vive solo en el
  Keychain de macOS, nunca en el repo.

## Base legal (Cuba)
- **Ley No. 1091** Art. 3.9 y **Decreto No. 3363** (Reglamento Interno de la Cámara) — facultad de certificar origen.
- **Resolución Conjunta No. 6/2018 MFP–MINCEX** — *Reglamento sobre Normas de Origen* (deroga la Res. Conj. 4/1997), alineada con el Acuerdo de la OMC sobre Normas de Origen.
  - [UNEP LEAP](https://leap.unep.org/countries/cu/national-legislation/resolucion-conjunta-n-62018-mfp-mincex-pone-en-vigor-el) · [Gaceta Oficial / vLex](https://cuba.vlex.com/vid/resolucion-no-6-2018-760069693) · [Portal VUCE MINCEX](https://vuceregulaciones.mincex.gob.cu/procedure/1551?l=es)

## Estándares internacionales citados
- **OMC** — Acuerdo sobre Normas de Origen.
- **OMA (WCO)** — [Convenio de Kyoto Revisado, Anexo K](https://www.wcoomd.org/en/topics/facilitation/instrument-and-tools/conventions/pf_revised_kyoto_conv.aspx) · [Study on the Digitalization of the Certificate of Origin](https://www.wcoomd.org/-/media/wco/public/global/pdf/topics/origin/instruments-and-tools/origin-certification/study-on-the-digitalization-of-the-certificate-of-origin-en.pdf)
- **UN/CEFACT** — [estándares de facilitación e intercambio electrónico de datos de comercio](https://unece.org/trade/uncefact/mainstandards) (once-only, interoperabilidad, eCO).
- **ISO/IEC 18004** — código QR (verificación de autenticidad).
- **SGP/GSP (UE)** — [sistema REX](https://taxation-customs.ec.europa.eu/online-services/online-services-and-databases-customs/registered-exporter-rex-system_en) (reemplazó al Form A desde 2020).

## Cómo se ve mejor
Diseñado para pantalla de presentación 16:9 / 16:10. El botón "¿Cómo implementar esto?" del
cierre apunta a un one-pager local y protegido (no se publica).

---
Cámara de Comercio de la República de Cuba · ONU Comercio y Desarrollo (UNCTAD) · Gobierno Digital.
