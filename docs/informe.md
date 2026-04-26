## Regla 1 - Violacion 5

**Problema:**
El caso de uso devolvia `null` cuando no existian usuarios, lo que viola la regla de no retornar `null`.

**Solucion:**
El caso de uso ahora devuelve una lista vacia cuando no hay resultados, manteniendo el contrato sin `null`.
