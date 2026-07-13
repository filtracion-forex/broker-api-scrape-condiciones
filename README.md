```
╔═══════════════════════════════════════════════════════════════╗
║  SCRAPEO DE CONDICIONES DE BROKERS                           ║
║  Datos extraidos de APIs publicas y sitios web               ║
╚═══════════════════════════════════════════════════════════════╝
```

Los brokers publican sus spreads y comisiones como si fueran los mejores del mercado. Pero cuando pones todos los datos en una misma tabla, las diferencias son abismales.

Escribi este script para comparar condiciones reales de 6 brokers usando los mismos criterios. Sin marketing, sin "spreads desde" en letra chica.

═ METODOLOGIA ═

El script `scrape.py` extrae datos de:

- Paginas de spreads de cada broker
- Documentacion de sus plataformas
- Terminos y condiciones de cuentas

No uso APIs privadas ni nada ilegal. Solo informacion publica que los brokers ya tienen en sus sitios, pero que nadie se toma el trabajo de comparar directamente.

═ HALLAZGOS CLAVE ═

1. El spread "desde 0.0 pips" casi siempre aplica solo a cuentas Raw/ECN con comision. La cuenta Standard tipica paga 3-5 veces mas.
2. El broker con el spread real mas bajo es Exness en cuenta Raw Spread (0.0 pips + $3.5 por lote).
3. El broker con el spread Standard mas bajo es AvaTrade (0.9 pips EUR/USD sin comision).
4. XTB ofrece la mayor cantidad de instrumentos (4,000+), pero sus spreads en forex no son los mejores.
5. El deposito minimo varia de $0 (XTB) a $200 (Pepperstone, IC Markets). La diferencia importa si empiezas con poco capital.

═ EL SCRIPT ═

Incluyo el script completo para que puedas ejecutarlo tu mismo y verificar los datos. No requiere librerias externas, solo Python 3.

Los resultados estan en `resultados.json` con marca de tiempo para que sepas cuando se recopilaron los datos.

═ NOTA ═

Esto es solo una instantanea. Los spreads cambian segun el dia, la volatilidad del mercado y tu volumen de operaciones. Usa esto como referencia, no como verdad absoluta.
