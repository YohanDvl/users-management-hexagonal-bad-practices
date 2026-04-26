## Regla 1 - Violación 1

**Archivo:**
UserRepositoryMySQL.java

**Problema:**
Se usaba un import con comodín (`java.util.*`), lo que oculta dependencias reales y viola la regla de imports explícitos.

**Solución:**
Se reemplazó el import comodín por imports específicos (`List` y `Optional`).

## Regla 1 - Violacion 5

**Problema:**
El caso de uso devolvia `null` cuando no existian usuarios, lo que viola la regla de no retornar `null`.

**Solucion:**
El caso de uso ahora devuelve una lista vacia cuando no hay resultados, manteniendo el contrato sin `null`.
