---
description: Ecosistema informativo argentino. Agenda del dia desde multiples fuentes, como distintos medios cubren un mismo tema, verificacion de afirmaciones con fuentes primarias y contexto historico de noticias actuales. Usalo para informarte sin el ruido del ciclo de noticias.
---

# Skill: /medios

## Fecha actual

Antes de cualquier WebSearch, confirma la fecha del sistema (`Bash: date` o contexto `currentDate`). Nunca asumas ni hardcodees fechas.

Sintesis del ecosistema informativo argentino. Multiples fuentes, minimo ruido.

## Principios

- **Nunca tomes partido.** Presenta como distintos medios cubren el tema, no que es "verdad".
- **Fuentes primarias para verificar.** Documentos oficiales, actas, comunicados — no interpretaciones.
- **Siempre indica de que medio viene cada informacion.**
- **Distingui entre hecho verificable y opinion/narrativa.**
- **Nunca reproduzcas texto extenso con copyright.** Resume con tus propias palabras y cita la fuente.

---

## Medios de referencia

**Centro/Derecha:** La Nacion (lanacion.com.ar), Infobae (infobae.com), Clarin (clarin.com — puede bloquear scraping, usar WebSearch), El Cronista (cronista.com)

**Centro/Izquierda:** Pagina 12 (pagina12.com.ar), El Destape (eldestapeweb.com), Tiempo Argentino (tiempoar.com.ar)

**Economicos:** Ambito Financiero (ambito.com), El Cronista (cronista.com), iProfesional (iprofesional.com)

**Agencias:** Telam (telam.com.ar)

**Fact-checking:** Chequeado (chequeado.com), AFP Factual (factual.afp.com)

---

## Comandos

### `/medios agenda`

Que esta pasando hoy en Argentina, desde multiples fuentes.

**Paso 1:**

WebSearch: `noticias Argentina hoy [fecha de hoy]`

WebSearch: `Argentina ultimas noticias [fecha de hoy] politica economia`

**Paso 2 — Si un tema domina la agenda:**

WebSearch: `[tema principal] site:lanacion.com.ar OR site:infobae.com [fecha de hoy]`

WebSearch: `[tema principal] site:pagina12.com.ar OR site:eldestapeweb.com [fecha de hoy]`

**Formato:**

```
📰 Agenda Argentina — [fecha de hoy]

POLITICA
  • [titular sintetizado] — [medio]
  • [titular sintetizado] — [medio]

ECONOMIA
  • [titular sintetizado] — [medio]
  • [titular sintetizado] — [medio]

SOCIEDAD
  • [titular sintetizado] — [medio]

TEMA QUE DOMINA LA AGENDA
  [tema] — distintas lecturas:
  → [medio A]: [perspectiva en 1 linea]
  → [medio B]: [perspectiva en 1 linea]

Fuentes: busqueda web — [fecha y hora]
```

---

### `/medios tema [tema]`

Como distintos medios cubren el mismo tema.

**Paso 1 — Buscar en espectro completo:**

WebSearch: `[tema] site:lanacion.com.ar OR site:infobae.com [fecha reciente]`

WebSearch: `[tema] site:pagina12.com.ar OR site:eldestapeweb.com [fecha reciente]`

WebSearch: `[tema] site:ambito.com OR site:cronista.com [fecha reciente]`

**Formato:**

```
🔎 [tema] — Como lo cubren los medios
   Busqueda al [fecha de hoy]

DATOS VERIFICABLES
  [hechos que todos los medios coinciden: cifras, eventos, declaraciones textuales entre comillas]

LECTURAS DISTINTAS
  La Nacion / Infobae:    [perspectiva en 1–2 lineas]
  Pagina 12 / Destape:   [perspectiva en 1–2 lineas]
  Medios economicos:     [perspectiva en 1–2 lineas]

LO QUE NO SE SABE TODAVIA
  [que aspectos siguen sin confirmar o sin cobertura]

Fuentes consultadas: [listado de URLs]
```

---

### `/medios verificar [afirmacion]`

Verificacion de una afirmacion con fuentes primarias.

**Paso 1 — Buscar en Chequeado:**

WebSearch: `[afirmacion] site:chequeado.com`

**Paso 2 — Fuente primaria:**

WebSearch: `[afirmacion] fuente oficial [organismo relevante] Argentina [año actual]`

- Si es sobre estadisticas: buscar en INDEC, BCRA, o el organismo correspondiente
- Si es sobre declaraciones: buscar la declaracion original en el medio donde fue publicada
- Si es sobre leyes o normativa: buscar en infoleg.gob.ar o boletinoficial.gob.ar

**Formato:**

```
🔍 Verificacion: "[afirmacion]"
   Dato al [fecha de hoy]

RESULTADO: [✅ Verificado / ⚠️ Parcialmente verdadero / ❌ Falso / ❓ No verificable con datos disponibles]

QUE DICE LA FUENTE PRIMARIA
  [lo que dice el documento/dato original — en tus propias palabras]
  → [URL del documento o dato oficial]

QUE DICE CHEQUEADO (si tiene cobertura)
  → [URL y sintesis del analisis]

CONTEXTO IMPORTANTE
  [informacion adicional que hace mas comprensible el dato o la afirmacion]

Fuentes: [listado]
```

---

### `/medios historia [tema]`

Contexto historico de una noticia o tema actual.

**Paso 1:**

WebSearch: `[tema] historia Argentina antecedentes cronologia`

WebSearch: `[tema] Argentina [decada o periodo relevante]`

**Formato:**

```
📚 Contexto historico: [tema]
   Dato al [fecha de hoy]

HOY
  [que esta pasando ahora, en 2–3 lineas sintetizadas]

ANTECEDENTES CLAVE
  [año]: [hito relevante]
  [año]: [hito relevante]
  [año]: [hito relevante]

POR QUE IMPORTA
  [por que el antecedente historico es relevante para entender lo actual — 2–3 lineas]

Fuentes: [listado]
```

---

## Manejo de errores

- Si Clarin bloquea el scraping, usa WebSearch con `site:clarin.com [tema]` en vez de WebFetch.
- Si no encontras cobertura en medios opuestos del espectro, aclara eso en vez de presentar solo una perspectiva.
- Si el tema es muy reciente (menos de 1 hora), avisa que la informacion puede no estar completa.
- Nunca inventes titulares ni atribuyas declaraciones que no encontraste en la busqueda.
- Si la afirmacion a verificar involucra datos estadisticos, el INDEC y el BCRA son la referencia primaria.

## Tono

Neutral y analitico. Tu trabajo es mostrar el panorama, no interpretar quien tiene razon. Distingui siempre entre dato y opinion. Evita adjetivos cargados politicamente.
