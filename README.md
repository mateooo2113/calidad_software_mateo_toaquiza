# Calidad de Software

Este repositorio corresponde a la materia **Calidad de Software**. En él se presentan conceptos básicos para comprender cómo se evalúa la calidad de un sistema de software y cómo se utilizan las pruebas para detectar errores y prevenir regresiones.

## Objetivos

- Entender los conceptos básicos de calidad de software.
- Identificar los principales problemas y riesgos asociados al desarrollo de software.
- Diferenciar entre pruebas unitarias, pruebas de integración y pruebas E2E.
- Aplicar buenas prácticas en el diseño y mantenimiento de pruebas.

## Conceptos básicos

### Calidad de Software

La calidad de software es la capacidad del producto para satisfacer las necesidades del usuario, además de ofrecer una experiencia confiable, segura, mantenible y fácil de usar.

Se considera que un sistema tiene calidad cuando:

- Cumple con los requisitos funcionales.
- Funciona correctamente en los escenarios esperados.
- Tiene poca probabilidad de fallos.
- Responde de manera eficiente.
- Es seguro y fácil de mantener.
- Puede evolucionarse sin introducir errores.

### Requisitos

Un requisito describe lo que el sistema debe hacer. Puede ser:

- **Funcional:** una acción que el usuario puede realizar.
- **No funcional:** una propiedad como rendimiento, seguridad o mantenibilidad.
- **Obligatorio:** requerido para el correcto funcionamiento del sistema.
- **Deseado:** una mejora o característica que puede aportar valor, pero no es esencial.

### Defectos, errores y fallos

- **Error:** condición que hace que el sistema no produzca el resultado esperado.
- **Defecto:** error presente en el código o en la diseño del sistema.
- **Fallo:** situación en la que el sistema no cumple su propósito o produce un resultado incorrecto.

### Pruebas

Una prueba es una forma de validar el comportamiento del software antes de su entrega o después de cambios. Las pruebas ayudan a detectar defectos temprano, reducir riesgos y facilitar la modificación del código.

## Tipos de pruebas

### Pruebas unitarias

Las pruebas unitarias validan una unidad aislada, normalmente una función, método o clase. Se utilizan para comprobar su comportamiento individual.

Ventajas:

- Son rápidas de ejecutar.
- Facilitan localizar fallos concretos.
- Mejoran la cobertura de código.
- Permiten validar cambios pequeños de forma independiente.

Ejemplo:

1. Se crea una función que suma dos números.
2. Se ejecuta la función con entradas conocidas.
3. Se compara el resultado esperado con el obtenido.

Una prueba unitaria debe cubrir:

- Entradas válidas.
- Entradas inválidas o extremas.
- Resultados esperados.
- Comportamientos de error cuando corresponda.

### Pruebas de integración

Las pruebas de integración verifican que varias unidades se comportan correctamente cuando se conectan. Por ejemplo, se puede comprobar que una aplicación puede guardar datos en una base de datos y recuperar esa información.

### Pruebas E2E

Las pruebas **E2E** (*End-to-End*) validan el flujo completo de una aplicación desde el punto de vista del usuario. Se ejecutan normalmente en un entorno de prueba y suelen cubrir varias capas: interfaz, lógica de negocio, servicios y base de datos.

Objetivos de las pruebas E2E:

- Confirmar que el flujo principal funciona.
- Verificar la interacción entre componentes.
- Detectar problemas de integración.
- Comprobar que la aplicación funciona como se espera para el usuario.

Ejemplo: iniciar una aplicación, iniciar sesión, crear un pedido, confirmar el pedido y consultar su estado.

## Diferencia entre pruebas unitarias y pruebas E2E

| Característica | Pruebas unitarias | Pruebas E2E |
|---|---|---|
| Alcance | Una unidad aislada | Flujo completo de la aplicación |
| Objetivo | Validar una función o método | Validar el comportamiento del sistema |
| Velocidad | Generalmente rápidas | Puede ser más lentas |
| Datos | Entradas simuladas o aisladas | Datos reales o datos de prueba de integración |
| Detección de errores | Errores locales | Problemas de integración y flujo |

## Reglas para escribir pruebas de calidad

- Las pruebas deben ser **claras**, **reproducibles** y **mantenibles**.
- Deben comprobar un comportamiento real, no una implementación interna.
- Las pruebas deben tener una entrada, una expectativa y un resultado verificable.
- Se recomienda cubrir casos felices, casos de error y casos límite.
- Las pruebas deben ser independientes entre sí.
- Las pruebas que dependen de datos externos deben usar datos de prueba controlados.
- Los tests deben ejecutarse en un entorno consistente.

## Ciclo de vida de las pruebas

1. **Creación:** se define el comportamiento esperado.
2. **Ejecución:** la prueba se ejecuta contra el sistema.
3. **Resultado:** se compara el resultado obtenido con el esperado.
4. **Mantenimiento:** se actualizan las pruebas cuando cambian los requisitos.
5. **Automatización:** las pruebas se ejecutan de forma periódica.

## Automatización de pruebas

La automatización permite ejecutar pruebas de forma repetida y con menor intervención humana. Es útil para:

- Validar cambios en el código.
- Detectar regresiones.
- Verificar la calidad del producto en cada versión.
- Reducir el tiempo de validación.

## Pruebas de regresión

Las pruebas de regresión comprueban que un cambio o una corrección no haya introducido nuevos fallos. Suelen reutilizar casos que detectaron defectos previamente.

## Métricas de calidad

Algunas métricas básicas son:

- **Cobertura:** porcentaje de código ejecutado durante las pruebas.
- **Tasa de fallos:** número de fallos detectados durante una ejecución de pruebas.
- **Tiempo de ejecución:** cuánto tarda en validar el sistema.
- **Tasa de regresión:** frecuencia con la que se introducen nuevos defectos.
- **Cobertura de requisitos:** porcentaje de requisitos verificados por las pruebas.

## Conclusión

La calidad de software no depende únicamente de la funcionalidad. También requiere pruebas eficientes, requisitos claros, seguridad, rendimiento, mantenibilidad y colaboración entre desarrolladores y usuarios. Las pruebas unitarias ayudan a validar piezas individuales, mientras que las pruebas E2E permiten comprobar el sistema completo.

## Sugerencia de práctica

Al desarrollar un proyecto, se puede seguir este orden:

1. Define los requisitos del sistema.
2. Divide el sistema en funciones o componentes pequeños.
3. Escribe pruebas unitarias para cada componente.
4. Conecta los componentes y ejecuta pruebas de integración.
5. Valida los flujos principales con pruebas E2E.
6. Repite las pruebas después de cada cambio.

> La calidad no es un único paso: es una práctica continua de validación, medición y mejora.
