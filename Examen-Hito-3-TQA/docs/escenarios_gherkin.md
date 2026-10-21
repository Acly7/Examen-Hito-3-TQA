```gherkin
Feature: Inicio de sesión en SauceDemo
  Como usuario de demostración
  Quiero ingresar al sistema
  Para consultar el catálogo de productos

  Scenario: Acceso con credenciales válidas
    Given que estoy en la pantalla de inicio de sesión de SauceDemo
    When ingreso el usuario "standard_user" y su contraseña válida de demostración
    And presiono el botón "Login"
    Then debería visualizar el catálogo de productos

  Scenario: Rechazo de contraseña incorrecta
    Given que estoy en la pantalla de inicio de sesión de SauceDemo
    When ingreso el usuario "standard_user" y una contraseña incorrecta
    And presiono el botón "Login"
    Then debería permanecer fuera del catálogo
    And debería visualizar un mensaje de error
```
