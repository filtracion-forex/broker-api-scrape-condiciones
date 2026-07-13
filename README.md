```
╔═══════════════════════════════════════════════════════════════╗
║  COMPARATIVA DE CONDICIONES DE BROKERS                       ║
║  Spreads, comisiones y depositos minimos lado a lado         ║
╚═══════════════════════════════════════════════════════════════╝
```

Los brokers publican sus spreads como si fueran los mejores. Cuando pones todos los datos en una misma tabla, las diferencias se ven claras.

Escribi este script para comparar las condiciones reales de 6 brokers usando los mismos criterios. Sin marketing, sin "spreads desde" en letra chica.

═ METODOLOGIA ═

El script extrae datos de paginas publicas de spreads, documentacion de plataformas y terminos de cuentas. No usa APIs privadas ni accede a informacion restringida. Solo datos que los brokers ya tienen publicos.

═ HALLAZGOS CLAVE ═

1. El spread "desde 0.0 pips" aplica solo a cuentas Raw/ECN con comision. La cuenta Standard tipica paga 3-5 veces mas.
2. El spread real mas bajo es Exness en cuenta Raw Spread (0.0 pips + $3.5 por lote).
3. El spread Standard mas bajo es AvaTrade (0.9 pips EUR/USD sin comision).
4. XTB ofrece mas instrumentos (4,000+), pero sus spreads en forex no son los mejores.
5. El deposito minimo varia de $0 (XTB) a $200 (Pepperstone, IC Markets).

═ EL SCRIPT ═

Incluyo el script completo para que puedas ejecutarlo tu mismo. No requiere librerias externas, solo Python 3. Los resultados estan en `resultados.json`.

═ NOTA ═

Los spreads cambian segun el dia, la volatilidad y tu volumen. Usa esto como referencia, no como verdad absoluta.
