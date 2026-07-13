# sales-analysis-dashboard-excel
An interactive sales dashboard built in Microsoft Excel to analyze the performance of a fictional e-commerce business. The project combines data preparation, Pivot Tables, Pivot Charts, KPIs and custom visual design to provide an intuitive overview of sales performance.


# Dashboard de Análisis de Ventas

## 1. Descripción del proyecto

Este proyecto consiste en la creación de un dashboard interactivo de análisis de ventas desarrollado en **Microsoft Excel** como ejercicio práctico de visualización de datos.

El objetivo es explorar un conjunto de datos de pedidos de comercio electrónico ficticio y comunicar los principales indicadores de rendimiento mediante visualizaciones claras e interactivas.

---

## 2. Dataset

- **Archivo:** `ventas_dashboard.csv`
- **Formato:** CSV con separador punto y coma (`;`) y decimales con coma.
- **Compatibilidad:** Configuración regional española.
- **Volumen:** 3.000 filas · 16 columnas + 2 columnas calculadas.
- **Periodo:** 2023–2024.

### Columnas disponibles

| Columna | Descripción |
|---------|-------------|
| `order_id` | Identificador único del pedido |
| `fecha_compra` | Fecha de realización del pedido |
| `producto` | 30 productos distribuidos en 5 categorías |
| `categoria` | Electrónica, Hogar, Cocina, Ropa y Deporte |
| `cantidad` | Unidades compradas por pedido (1–5) |
| `precio_base` | Precio de catálogo sin descuento |
| `descuento_pct` | Descuento aplicado (0%, 5%, 10%, 15% o 20%) |
| `precio_unitario` | Precio final tras aplicar el descuento |
| `total_venta` | Precio unitario × cantidad |
| `estado_entrega` | Entregado, En tránsito, Pendiente, Cancelado o Devuelto |
| `canal_venta` | Web, App Móvil, Marketplace o Teléfono |
| `metodo_pago` | Tarjeta de Crédito, Débito, PayPal, Transferencia o Bizum |
| `ciudad` | 15 ciudades españolas |
| `region` | Comunidad Autónoma |
| `city_tier` | Clasificación de ciudad (Tier 1, Tier 2 y Tier 3) |
| `valoracion_cliente` | Valoración de 1 a 5 (solo pedidos entregados) |
| **Total bruto (calculada)** | `precio_base × cantidad` |
| **Descuento € (calculada)** | `Total bruto − total_venta` |

---

## 3. Importación y transformación de datos

Se recomienda el siguiente proceso:

1. Importar el archivo desde **Datos → De texto/CSV**.
2. No abrir el archivo CSV mediante doble clic.
3. Verificar que el separador es `;`.
4. Confirmar que los decimales utilizan `,`.

---

## 4. Métricas principales

Todos los KPIs económicos se calculan únicamente sobre los pedidos con estado **Entregado**.

| KPI | Descripción |
|-----|-------------|
| Revenue bruto | Suma de `precio_base × cantidad` |
| Revenue neto | Suma de `total_venta` |
| Revenue potencial | Pedidos En tránsito y Pendientes |
| Abonos por devolución | Total de pedidos Devueltos (valor negativo) |
| Pedidos cancelados | Número de pedidos Cancelados |
| Ticket medio | Revenue neto / pedidos entregados (**672 €**) |
| Revenue perdido por descuentos | **6,82%** |
| Pedidos con descuento | **56,31%** |
| Tasa de cancelación | **6,1%** |
| Tasa de devolución | **4,1%** |

---

## 5. Estructura del dashboard

El dashboard incluye:

- KPIs principales.
- Indicadores de descuentos.
- Evolución mensual de ventas (2023 vs 2024).
- Ventas por categoría.
- Unidades vendidas por categoría.
- Ranking de productos más y menos vendidos.
- Ranking de productos mejor y peor valorados.
- Ticket medio por categoría.
- Ventas por canal.
- Ventas por método de pago.
- Ventas por City Tier.
- Evolución de devoluciones y cancelaciones.
- Distribución de pedidos por estado mediante gráficos donut.

---

## 6. Filtros disponibles

Los filtros disponibles son:

- Año (2023 / 2024)
- Mes (enero–diciembre)
- Estado de entrega:
  - Entregado
  - En tránsito
  - Pendiente
  - Cancelado
  - Devuelto

> **Nota:** Los productos mejor y peor valorados permanecen fijos y no se ven afectados por los filtros temporales.

---

## 7. Notas y limitaciones

- El dataset es completamente sintético y tiene fines educativos.
- No representa datos de ninguna empresa real.
- No existe estacionalidad real.
- No se incluyen costes de producto, por lo que únicamente puede analizarse el revenue.
- La clasificación `city_tier` ha sido asignada manualmente.
- El porcentaje de pedidos con descuento (56,31%) responde al proceso de generación de datos y no a un caso real.

---

## 8. Tecnologías utilizadas

- Microsoft Excel
- CSV

---

## 9. Autora

**Raquel García García**

Proyecto desarrollado como parte del Máster en Data Analytics (Power Business School).
