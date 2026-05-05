# medios

Plugin de Claude Code — ecosistema informativo argentino.

## Que hace

`/medios` te ayuda a navegar el ruido mediatico argentino: la agenda del dia desde multiples fuentes, como distintos medios cubren el mismo tema, verificacion de afirmaciones con fuentes primarias y contexto historico de lo que esta pasando.

## Instalacion

```bash
claude --plugin-dir /ruta/a/medios
```

## Comandos y ejemplos

### `/medios agenda`

```
📰 Agenda Argentina — 4 may 2026

POLITICA
  • El Congreso retomo el debate del presupuesto 2027 — La Nacion
  • Gremios anunciaron plan de accion ante vencimiento de paritarias — Pagina 12

ECONOMIA
  • Dolar blue cierra la semana en $1.420, brecha con el oficial en 18% — Ambito
  • INDEC publica inflacion de abril la proxima semana — Cronista

SOCIEDAD
  • Universidades publicas exigen actualizacion presupuestaria — Tiempo Argentino

TEMA QUE DOMINA LA AGENDA
  Paritarias docentes — distintas lecturas:
  → La Nacion / Infobae: "Los gremios rechazan la oferta del 4% mensual del gobierno"
  → Pagina 12 / Destape: "Los maestros resisten un ajuste encubierto ante la inflacion"

Fuentes: busqueda web — 4 may 2026, 10:30hs
```

---

### `/medios tema minas litio argentina`

```
🔎 Minas de litio en Argentina — Como lo cubren los medios
   Busqueda al 4 may 2026

DATOS VERIFICABLES
  Argentina tiene las segundas reservas de litio del mundo (Puna: Jujuy, Salta, Catamarca)
  La produccion exportada en 2025 fue de X toneladas (verificar dato en Secretaria de Mineria)
  Hay mas de 30 proyectos en distintas etapas de desarrollo al 2026

LECTURAS DISTINTAS
  La Nacion / Cronista:  Oportunidad de inversion y generacion de divisas. Marco regulatorio necesario para atraer capital.
  Pagina 12 / Destape:  Riesgos ambientales en el ecosistema puneño. Debate sobre soberania de los recursos y royalties.
  Medios economicos:    Potencial de USD 3.000M anuales en exportaciones si se escalan proyectos.

LO QUE NO SE SABE TODAVIA
  Impacto real en los recursos hidricos de la Puna — falta de estudios publicos completos
  Cuanto queda en manos de empresas argentinas vs. extranjeras

Fuentes: lanacion.com.ar, pagina12.com.ar, ambito.com — 4 may 2026
```

---

### `/medios verificar "la inflacion de marzo fue del 3%"`

```
🔍 Verificacion: "la inflacion de marzo fue del 3%"
   Dato al 4 may 2026

RESULTADO: ✅ Verificado (con matiz)

QUE DICE LA FUENTE PRIMARIA
  El INDEC publico el IPC de marzo 2026 con una variacion mensual del 3,1%
  → https://www.indec.gob.ar/indec/web/Nivel4-Tema-3-5-31

QUE DICE CHEQUEADO
  No encontre cobertura especifica de esta afirmacion en chequeado.com

CONTEXTO IMPORTANTE
  El 3% mensual equivale a un 42,6% anualizado si se mantuviera constante.
  Es el valor mas bajo desde [buscar contexto historico]. La comparacion con años
  anteriores es relevante para evaluar si es "alta" o "baja".

Fuentes: indec.gob.ar — 4 may 2026
```

---

### `/medios historia deuda externa argentina`

```
📚 Contexto historico: deuda externa argentina
   Dato al 4 may 2026

HOY
  Argentina atraviesa un nuevo programa con el FMI acordado en [buscar fecha vigente],
  con desembolsos condicionados a metas fiscales y de reservas.

ANTECEDENTES CLAVE
  1956: Ingreso al FMI tras la Revolucion Libertadora
  1983: Retorno a la democracia con deuda de USD 45.000M heredada
  2001: Default mas grande de la historia hasta entonces (~USD 100.000M)
  2005: Canje Kirchner — quita del 65% para los aceptantes
  2010: Segundo canje, reestructuracion con holdouts pendiente
  2016: Pago a holdouts ("fondos buitre") — vuelta a mercados voluntarios
  2020: Nuevo default y reestructuracion (~USD 65.000M con privados)
  2022: Acuerdo FMI por USD 44.000M — programa extendido

POR QUE IMPORTA
  La deuda externa es el factor estructural que mas condiciona la politica economica
  argentina en cada ciclo de gobierno. El debate entre ajuste y crecimiento gira
  invariablemente en torno a esta variable.

Fuentes: busqueda web — 4 may 2026
```

## Fuentes

- **La Nacion:** [lanacion.com.ar](https://www.lanacion.com.ar)
- **Infobae:** [infobae.com](https://www.infobae.com)
- **Pagina 12:** [pagina12.com.ar](https://www.pagina12.com.ar)
- **Ambito:** [ambito.com](https://www.ambito.com)
- **Chequeado:** [chequeado.com](https://www.chequeado.com)
- **AFP Factual:** [factual.afp.com](https://factual.afp.com)

Este plugin no toma posicion politica. Presenta la cobertura de cada medio sin endosar ninguna perspectiva. No reproduce textos con copyright — sintetiza y cita.
