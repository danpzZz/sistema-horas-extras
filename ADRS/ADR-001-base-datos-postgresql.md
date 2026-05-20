# ADR-001: Uso de PostgreSQL como Base de Datos

Fecha: 2026-05-20

Estado: Aceptado

## Contexto

El sistema automatizado de cálculo de horas extras requiere almacenar usuarios, registros procesados, timbrados, horas trabajadas, horas extras y reportes históricos.

La información procesada corresponde a datos laborales, por lo que se requiere integridad, consistencia y trazabilidad.

## Decisión

Se utilizará PostgreSQL como motor principal de base de datos del sistema.

## Alternativas consideradas

### MySQL

Permite almacenamiento relacional y es ampliamente utilizado, pero PostgreSQL ofrece mejores capacidades para consultas complejas y manejo de integridad avanzada.

### MongoDB

Permite flexibilidad documental, pero no es la mejor opción para este caso debido a la necesidad de relaciones claras entre usuarios, funcionarios, timbrados, reportes y horas extras.

## Consecuencias

### Positivas

- Integridad referencial.
- Transacciones ACID.
- Buen rendimiento para reportes.
- Mayor seguridad y consistencia de datos.

### Negativas

- Mayor rigidez en el esquema.
- Necesidad de manejar migraciones cuando cambie el modelo de datos.

## Atributo de calidad relacionado

Seguridad e integridad de datos.