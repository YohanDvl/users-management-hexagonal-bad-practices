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

## Regla 2 - Violacion 5

**Archivo:**
LoginServiceTest.java

**Problema:**
Faltaban `@DisplayName`, comentarios AAA y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron `@DisplayName`, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 10

**Archivo:**
AppProperties.java

**Problema:**
Se usaban comparaciones directas con `null` y nombres abreviados (`props`, `val`).

**Solucion:**
Se uso `Objects.requireNonNull(...)` y se renombraron variables a nombres descriptivos.

## Regla 1 - Violacion 11

**Archivo:**
ConsoleIO.java

**Problema:**
Se usaban nombres abreviados en variables locales.

**Solucion:**
Se renombraron variables a nombres descriptivos (`value`, `rawInput`).

## Regla 2 - Violacion 6

**Archivo:**
ConsoleIO.java

**Problema:**
Textos hardcodeados en metodos en lugar de constantes.

**Solucion:**
Se agregaron constantes y se reutilizaron en los mensajes.

## Regla 1 - Violacion 12

**Archivo:**
UserController.java

**Problema:**
Se usaba una abreviatura (`usrs`) en una variable local.

**Solucion:**
Se renombro la variable a `users`.

## Regla 1 - Violacion 13

**Archivo:**
UserController.java

**Problema:**
El entrypoint construia commands directamente sin usar el mapper.

**Solucion:**
Se usaron metodos de `UserDesktopMapper` para construir los commands.

## Regla 1 - Violacion 14

**Archivo:**
UserEmail.java

**Problema:**
Se usaba logging dentro del dominio.

**Solucion:**
Se elimino el logger de la clase.

## Regla 1 - Violacion 15

**Archivo:**
UserEmail.java

**Problema:**
Se logueaba PII (el email del usuario) en el dominio.

**Solucion:**
Se elimino el log de validacion del email.

## Regla 1 - Violacion 16

**Archivo:**
UpdateUserHandler.java

**Problema:**
Se usaban abreviaturas en variables locales (`pw`, `upd`).

**Solucion:**
Se renombraron las variables a nombres descriptivos.

## Regla 1 - Violacion 17

**Archivo:**
CreateUserServiceTest.java

**Problema:**
Faltaban `@DisplayName`, comentarios AAA y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron `@DisplayName`, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 18

**Archivo:**
UserPasswordTest.java

**Problema:**
Faltaban `@DisplayName`, comentarios AAA y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron `@DisplayName`, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 19

**Archivo:**
UpdateUserServiceTest.java

**Problema:**
Faltaban comentarios AAA, @DisplayName y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron comentarios `// Arrange`, `// Act`, `// Assert`, `@DisplayName` y se usaron aserciones correctas.

## Regla 1 - Violacion 20

**Archivo:**
ConfigurationException.java

**Problema:**
Mensaje de error hardcodeado en el metodo factory.

**Solucion:**
Se definio una constante para el mensaje.

## Regla 1 - Violacion 21

**Archivo:**
PersistenceException.java

**Problema:**
Mensajes de error hardcodeados en metodos factory.

**Solucion:**
Se definieron constantes y se usaron en los format.

## Regla 1 - Violacion 22

**Archivo:**
EmailSenderException.java

**Problema:**
Mensajes hardcodeados en los metodos factory.

**Solucion:**
Se movieron a constantes descriptivas.

## Regla 1 - Violacion 23

**Archivo:**
InvalidCredentialsException.java

**Problema:**
Mensajes hardcodeados en los metodos factory.

**Solucion:**
Se definieron constantes para los mensajes.

## Regla 1 - Violacion 24

**Archivo:**
InvalidUserIdException.java

**Problema:**
Mensaje hardcodeado en el metodo factory.

**Solucion:**
Se creo una constante con el mensaje.

## Regla 1 - Violacion 25

**Archivo:**
InvalidUserEmailException.java

**Problema:**
Mensajes hardcodeados en los metodos factory.

**Solucion:**
Se definieron constantes y se usaron en format.

## Regla 1 - Violacion 26

**Archivo:**
InvalidUserRoleException.java

**Problema:**
Mensaje hardcodeado en el metodo factory.

**Solucion:**
Se definio una constante para el mensaje.

## Regla 1 - Violacion 27

**Archivo:**
InvalidUserStatusException.java

**Problema:**
Mensaje hardcodeado en el metodo factory.

**Solucion:**
Se definio una constante para el mensaje.

## Regla 1 - Violacion 28

**Archivo:**
InvalidUserNameException.java

**Problema:**
Mensajes hardcodeados en los metodos factory.

**Solucion:**
Se definieron constantes para los mensajes.

## Regla 1 - Violacion 29

**Archivo:**
UserAlreadyExistsException.java

**Problema:**
Mensaje hardcodeado en el metodo factory.

**Solucion:**
Se definio una constante y se uso en format.

## Regla 1 - Violacion 30

**Archivo:**
UserNotFoundException.java

**Problema:**
Mensaje hardcodeado en el metodo factory.

**Solucion:**
Se definio una constante y se uso en format.

## Regla 1 - Violacion 31

**Archivo:**
UserManagementCli.java

**Problema:**
Uso de literal repetido y nombre abreviado en el menu.

**Solucion:**
Se reutilizo la constante y se renombro la variable a `option`.

## Regla 1 - Violacion 32

**Archivo:**
UserNameTest.java

**Problema:**
Faltaban `@DisplayName`, comentarios AAA y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron `@DisplayName`, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 33

**Archivo:**
UserIdTest.java

**Problema:**
Faltaban `@DisplayName`, comentarios AAA y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron `@DisplayName`, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 34

**Archivo:**
GetUserByIdServiceTest.java

**Problema:**
Faltaban comentarios AAA, @DisplayName y se usaban aserciones poco expresivas.

**Solucion:**
Se agregaron comentarios `// Arrange`, `// Act`, `// Assert`, `@DisplayName` y se usaron aserciones correctas.

## Regla 1 - Violacion 35

**Archivo:**
GetAllUsersServiceTest.java

**Problema:**
Faltaban comentarios AAA, javadoc y se usaban aserciones poco expresivas.

**Solucion:**
Se agrego javadoc, comentarios `// Arrange`, `// Act`, `// Assert` y se usaron aserciones correctas.

## Regla 1 - Violacion 36

**Archivo:**
EmailNotificationServiceTest.java

**Problema:**
Faltaban javadoc, @DisplayName y comentarios AAA.

**Solucion:**
Se agregaron javadoc, `@DisplayName` y comentarios AAA.

## Regla 1 - Violacion 37

**Archivo:**
DatabaseConnectionFactoryTest.java

**Problema:**
Faltaba javadoc de clase.

**Solucion:**
Se agrego javadoc descriptivo.

## Regla 1 - Violacion 38

**Archivo:**
UserPersistenceMapperTest.java

**Problema:**
Faltaba javadoc de clase.

**Solucion:**
Se agrego javadoc descriptivo.

## Regla 2 - Violacion 7

**Archivo:**
UserResponse.java

**Problema:**
Se usaba una clase mutable con @Data en lugar de un record inmutable.

**Solucion:**
Se convirtio el DTO a record.

## Regla 2 - Violacion 8

**Archivo:**
DeleteUserService.java

**Problema:**
Se usaba un logger manual y un try-catch que capturaba excepciones no recuperables.

**Solucion:**
Se removio el logger manual y el try-catch para dejar propagar las excepciones.

## Regla 2 - Violacion 9

**Archivo:**
CreateUserHandler.java

**Problema:**
Se instanciaba un logger manual y se logueaba PII en el mensaje de error.

**Solucion:**
Se uso `@Log` y se registro un mensaje generico sin datos sensibles.

## Regla 2 - Violacion 10

**Archivo:**
LoginHandler.java

**Problema:**
Se logueaba el email del usuario al fallar el login (PII).

**Solucion:**
Se dejo un log generico sin datos personales.

## Regla 2 - Violacion 11

**Archivo:**
CreateUserCommand.java

**Problema:**
Se usaba `@Builder` en un record, lo que es redundante.

**Solucion:**
Se removio `@Builder` y se uso el constructor canonico del record.

## Regla 2 - Violacion 12

**Archivo:**
GetUserByIdQuery.java

**Problema:**
Se usaba `@Builder` en un record y un mensaje custom en la constraint.

**Solucion:**
Se elimino `@Builder` y se dejo el mensaje por defecto de `@NotBlank`.

## Regla 2 - Violacion 13

**Archivo:**
GetUserByIdService.java

**Problema:**
Se declaraba `@Valid` en la implementacion en vez de en el puerto.

**Solucion:**
Se elimino `@Valid` del metodo implementado.

## Regla 2 - Violacion 14

**Archivo:**
ValidatorProvider.java

**Problema:**
Clase utilitaria sin `@UtilityClass`.

**Solucion:**
Se anoto con `@UtilityClass`.

## Regla 2 - Violacion 15

**Archivo:**
DatabaseConnectionFactory.java

**Problema:**
Clase utilitaria sin `@UtilityClass` y metodo no estatico.

**Solucion:**
Se anoto con `@UtilityClass` y se declaro el metodo como estatico.

## Regla 2 - Violacion 16

**Archivo:**
DependencyContainer.java

**Problema:**
Se instanciaba `DatabaseConnectionFactory` en lugar de usar metodo estatico.

**Solucion:**
Se uso `DatabaseConnectionFactory.createConnection(...)`.

## Regla 2 - Violacion 17

**Archivo:**
UserPersistenceMapper.java

**Problema:**
Clase de mapeo sin `@UtilityClass` y metodos de instancia innecesarios.

**Solucion:**
Se anoto con `@UtilityClass` y se hicieron estaticos los metodos.

## Regla 2 - Violacion 18

**Archivo:**
UserRepositoryMySQL.java

**Problema:**
Se instanciaba el mapper en lugar de usar metodos estaticos.

**Solucion:**
Se llamo a los metodos estaticos de `UserPersistenceMapper`.

## Regla 2 - Violacion 19

**Archivo:**
DatabaseConnectionFactoryTest.java

**Problema:**
Se instanciaba el factory en tests aunque es utilitario.

**Solucion:**
Se uso el metodo estatico en los tests.

## Regla 2 - Violacion 20

**Archivo:**
UserPersistenceMapperTest.java

**Problema:**
Se instanciaba el mapper en tests aunque es utilitario.

**Solucion:**
Se usaron los metodos estaticos del mapper.

## Regla 2 - Violacion 21

**Archivo:**
LoginService.java

**Problema:**
Metodo con multiples responsabilidades y condicion de estado redundante.

**Solucion:**
Se dividio en metodos de validacion y se simplifico la verificacion de estado.

## Regla 2 - Violacion 22

**Archivo:**
UserModel.java

**Problema:**
El dominio dependia de una entidad de infraestructura.

**Solucion:**
Se elimino la conversion a entidad de persistencia desde el dominio.

## Regla 2 - Violacion 23

**Archivo:**
EmailSenderException.java

**Problema:**
Constructores publicos que permitian crear excepciones con mensajes arbitrarios.

**Solucion:**
Se hicieron privados los constructores y se conservaron los factory methods.
