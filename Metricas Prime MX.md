# Métricas Prime MX

## Ventas

### ROLES:
- **Presidencia** (toda la información)
- **Gerente Regional** (solo lo concerniente a su región)
- **Gerente de Tienda** (solo lo concerniente a su tienda)

### Conceptos

**Reales**: Es la información que envía AT&T de forma periódica de las ventas que tiene registradas en sus sistemas, hechas por PRIME. Esta información se carga cada semana en el Portal PrimeMX y se utiliza para realizar el cálculo de las comisiones. AT&T envía un archivo por cada producto o métrica, con el acumulado de las ventas.

**Cantados**: Es la información de las ventas realizadas que capturan los ejecutivos y gerentes de tienda.

**Comisiones**: Es la remuneración económica que se otorga a la fuerza de ventas, por las ventas realizadas. Estas comisiones se pagan de forma semanal, los días Miércoles y abarcan las ventas realizadas en la semana inmediata anterior (Lunes a Domingo) al día que se paga. El cálculo de estas comisiones se realiza UTILIZANDO la información de venta enviada por AT&T.

**Cuota**: Es la cantidad de unidades de un producto o servicio que deben venderse en un periodo determinado. AT&T determina una cuota mensual de cada producto que debe ser alcanzada por Prime a nivel global. Esta cuota mensual global por cada producto se dispersa a cada tienda por semana.

### Métricas

- **Métricas o Productos**: Son los diferentes servicios o productos que ofrece AT&T y son comercializados por Prime. Actualmente se tienen los siguientes:
  - Pospago
  - Renovación
  - Prepago
  - Seguros
  - Accesorios
  - Add Ons
  - Transfer
  - Negocios

- **OPS**: La suma de las ventas de las métricas pospago, renovaciones y prepago, en el mes actual

- **CUOTA**: La suma de la cuota de las métricas pospago, renovaciones y prepago, en el mes actual

- **PER DOOR**: Cada total de métrica entre el número de tiendas que tenemos activas

- **PIA**: Paid In Advance, modalidad de plan tarifario con cobro por adelantado. Estos planes no se consideran para comisionamiento ni para alcance de cuota.

- **RR**: Run Rate, representa una medición de las ventas que se han hecho por cada día del mes que ha transcurrido. Se calcula dividiendo: Venta Total Actual / Día Actual del Mes

- **GAP**: Representa el número de unidades que se tienen que vender desde el día actual hasta el último día del mes para alcanzar la cuota establecida. Como el cálculo se realiza a día cerrado, es necesario considerar el día de ayer (día actual -1) para un cálculo correcto. (Cuota – Venta)/ (Ultimo día del mes – (Día actual-1))

- **ARPU**: Average Revenue Per User, Es una métrica utilizada para medir los ingresos promedio generados por cada usuario o cliente, se calcula sumando el costo de la renta mensual de los planes tarifarios / el número de planes vendidos.

- **Proyección**: Es el cálculo de las unidades que se venderían al final de mes, con el ritmo de venta al día actual, expresado en porcentaje de la cuota establecida.

  Como primer paso se calcula el ritmo de venta diario hasta el momento:
  - Ritmo de venta al día de hoy: Total de unidades vendidas / días del mes transcurridos
  - Cálculo del total de ventas proyectado: Unidades Vendidas Actualmente + (Ritmo de venta al día de hoy * días faltantes del mes)
  - (Cálculo del total de ventas proyectado * 100) / Cuota Mensual

- **Mostrar la siguiente información para cada uno de los productos o métricas**:
  - Porcentaje de Venta
  - Ventas Totales (reales + cantados)
  - Per Door
  - Cuota
  - Per Door
  - Proyección de Venta para final de mes
  - Run Rate
  - GAP
  - ARPU, para los productos pospago y renovación
  - Venta masiva
  - Venta masiva + Negocio
  - Número de Tiendas Activas

- **Tener la capacidad de filtrar la información bajo los siguientes criterios**:
  - Región Prime: Nacional, Bajío, Centro I, Centro II, Noroeste, Noroeste II, Norte I, Norte II, Pacífico, Sur Península
  - Estructura de Ventas: VPGM, Director, Gerente Regional, PDV (Tienda)
  - Periodo de Tiempo: Año + Mes /Semana
  - Propiedad del Equipo: Propio, Nuevo
  - Tipo de Venta: Masivo, Empresarial

- **Poder visualizar la composición de las ventas segmentadas por (mix pospago)**:
  - Planes PIAS
  - Valor de renta de los planes tarifarios
  - Tipos de Cliente (Empresarial / Masivo)
  - Origen del Equipo (Nuevo / Propio)

- **Tener visibilidad de la información antes mencionada considerando ventas reales y reales + cantados**

## Asistencia

### ROLES:
- **Presidencia** (toda la información)
- **Gerente Regional** (solo lo concerniente a su región)
- **Gerente de Tienda** (solo lo concerniente a su tienda)

### Métricas

Todas las métricas deben estar acotadas a un periodo mensual o semanal.

- **Porcentaje de Asistencia General**: porcentaje de todas las personas que registran asistencia o tienen justificación en el periodo, respecto del total de personas que están en tienda (todas las personas que aparecen en el reporte).

- **Porcentaje de Asistencia Por Región por mes o semana**: mismo caso que el porcentaje de asistencia general, pero acotado a regiones

- **Hora promedio de registro de asistencia**

- **Top 5 de tiendas con menor porcentaje asistencia**

- **Principales motivos de justificación de inasistencia**

- **Top 5 personas que más justifican asistencia**

- **Top 5 de personas con más justificaciones**

- **Hora promedio de la justificación de la inasistencia**

- **Porcentaje de personas que registran entrada pero no registran salida**

## Control de Contratos

### ROLES:
- **Presidencia** (toda la información)

### Métricas

- **Vencimiento de contrato de arrendamiento por mes** (fecha_vencimiento)

- **Precio promedio de las rentas** (renta)

- **Conteo de tiendas con documentación completa** (tienen todos los documentos marcados como obligatorios): Tiene registro de todos los documentos marcados como obligatorios en el catálogo de documentos.

- **Conteo de tiendas que tienen XX documento registrado** (XX: documento del catálogo de documentos)

- **Promedio de la superficie de nuestras tiendas** (superficie)

- **Monto total por concepto de renta que se paga mensualmente** (renta)

- **Conteo de tiendas abiertas** (estado: Operando)

- **Conteo tiendas cerradas** (fecha_cierre)