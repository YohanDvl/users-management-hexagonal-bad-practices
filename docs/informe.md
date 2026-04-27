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

## Regla 1 - Violacion 2

**Archivo:**
EmailNotificationService.java

**Problema:**
El metodo `renderTemplate` no usaba estado de instancia y no estaba declarado como `static`.

**Solucion:**
Se declaro `renderTemplate` como `static` para reflejar que no depende del estado del objeto.

## Regla 1 - Violacion 3

**Archivo:**
JavaMailEmailSenderAdapter.java

**Problema:**
Se uso el nombre completamente calificado `javax.mail.internet.InternetAddress` aunque ya estaba importado.

**Solucion:**
Se uso el import existente `InternetAddress` para mantener el estilo consistente.

## Regla 1 - Violacion 4

**Archivo:**
JavaMailEmailSenderAdapter.java

**Problema:**
Se uso un import con comodin `javax.mail.*`, ocultando dependencias reales.

**Solucion:**
Se reemplazo el comodin por imports explicitos de las clases usadas.

## Regla 2 - Violacion 1

**Archivo:**
UserValidationUtils.java

**Problema:**
Se usaba el valor magico `8` para la longitud minima de la contraseña.

**Solucion:**
Se creo la constante `MIN_PASSWORD_LENGTH` y se uso en la validacion.

## Regla 1 - Violacion 6

**Archivo:**
UserPassword.java

**Problema:**
Se hacia validacion de null con comparacion directa en vez de usar utilidades estandar.

**Solucion:**
Se reemplazo el chequeo por `Objects.requireNonNull(...)`.

## Regla 2 - Violacion 2

**Archivo:**
UserPassword.java

**Problema:**
Se usaban valores magicos para longitud minima y costo de BCrypt.

**Solucion:**
Se definieron las constantes `MINIMUM_LENGTH` y `BCRYPT_COST` y se usaron en el calculo.

## Regla 1 - Violacion 7

**Archivo:**
UserName.java

**Problema:**
Se validaba null con comparacion directa en lugar de `Objects.requireNonNull`.

**Solucion:**
Se reemplazo el chequeo por `Objects.requireNonNull(...)`.

## Regla 2 - Violacion 3

**Archivo:**
UserName.java

**Problema:**
Se usaba el valor magico `3` para longitud minima del nombre.

**Solucion:**
Se creo la constante `MINIMUM_LENGTH` y se uso en la validacion.

## Regla 1 - Violacion 8

**Archivo:**
UserId.java

**Problema:**
Se validaba null con comparacion directa en lugar de `Objects.requireNonNull`.

**Solucion:**
Se reemplazo el chequeo por `Objects.requireNonNull(...)`.

## Regla 1 - Violacion 9

**Archivo:**
EmailDestinationModel.java

**Problema:**
Se validaba null con comparacion directa en lugar de `Objects.requireNonNull`.

**Solucion:**
Se reemplazo el chequeo por `Objects.requireNonNull(...)`.

## Regla 2 - Violacion 4

**Archivo:**
EmailDestinationModel.java

**Problema:**
Los mensajes de error estaban hardcodeados en el metodo.

**Solucion:**
Se definieron constantes con nombres descriptivos para los mensajes.
