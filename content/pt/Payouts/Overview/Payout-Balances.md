---
title: "Saldos de Payouts"
linkTitle: "Saldos de Payouts"
date: 2023-03-22T15:30:03-05:00
type: docs
Description: >
  El saldo es el monto de dinero que tiene para procesar las transacciones de Payout. Tenemos tres tipos de Saldos en los Payouts de Bamboo.
weight: 30
---
<!-- y los puede ver en dos modelos-->

Nosotros actualizamos los saldos de acuerdo con los movimientos realizados en su cuenta como depósitos y dispersiones.

## Tipos de saldos {#balance-types}
Usted puede ver los siguientes saldos en la consola de Payouts:

* **Saldo Total**: Este monto corresponde al total de dinero de su cuenta.
* **Saldo para procesamiento**: Este monto corresponde a todos las disposiciones solicitadas en Payouts. El monto de la tasa del Payout puede estar incluída dependiendo de la parte que va a asumir la tasa (ya sea usted o el beneficiario)<!-- y el [modelo](#balance-models) seleccionado-->. Una vez todos los Payouts hayan llegado a un estado final (Pagado o rechazado), el valor mostrado acá será 0.
* **Saldo disponible**: Corresponde al monto de dinero que tiene disponible para procesar más Payouts, el cual es la diferencia entre el _**Saldo Total**_ y el _**Saldo para procesamiento**_.

{{% alert title="Info" color="info"%}}
Si el pagador asume la tasa, no se agrega la misma a ningún tipo de saldo.
{{% /alert %}}

<!--
## Modelos de los saldos {#balance-models}
La funcionalidad de Payouts de Bamboo le ofrece la posibilidad de ver los tres tipos de saldos en dos modelos:

* **Modelo Simplificado**: un saldo único para Payouts.<br>
En este caso, Bamboo deduce el monto del pago y la tasa cobrada de su saldo global.

![](/assets/Payouts/Payouts3_en.png)

* **Modelo Detallado**: un saldo para Payouts y otro para tasas.<br>
En este caso, tienes dos saldos, uno para deducir los montos netos del Payout y otro para deducir exclusivamente las tasas cobradas.

![](/assets/Payouts/Payouts4_en.png)
-->

## Ejemplos {#examples}
Hagamos un ejemplo para que entienda el concepto de tipo <!--y modelo -->que hay detrás de los Saldos de pagos.

Supongamos que usted tiene la siguiente información:

<div id="shortTable"></div>

| | |
|---|---|
| Monto del Payout solicitado | 10 USD |
| tasa | 2 USD |
| Saldo inicial | 20 USD |
<!--| Saldo inicial para la tasa | 5 USD |-->

### <!--Modelo Simplificado - c-->tasa asumida por usted {#simplified-model---fee-assumed-by-you}

<div id="shortTable"></div>

| Saldo cuando el Payout es solicitado |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento<br>_Monto del Payout solicitado + tasa_ | 12 USD |
| Saldo disponible | 8 USD |

<div id="shortTable"></div>

| Saldo si el Payout fue pagado | |
|---|---|
| Saldo Total | 8 USD |
| Saldo para procesamiento | - |
| Saldo disponible | 8 USD |

<div id="shortTable"></div>

| Saldo si el Payout fue rechazado | |
|---|---|
| Saldo Total | 18 USD |
| Saldo para procesamiento | - |
| Saldo disponible | 18 USD |

_Si el Payout es rechazado, la tasa de procesamiento no se reembolsa._

### <!--Modelo Simplificado - c-->tasa asumida por el beneficiario {#simplified-model---fee-assumed-by-the-payee}

<div id="shortTable"></div>

| Saldo cuando el Payout es solicitado |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento| 10 USD |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo si el Payout fue pagado | |
|---|---|
| Saldo Total | 10 USD |
| Saldo para procesamiento | - |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo si el Payout fue rechazado | |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento | - |
| Saldo disponible | 20 USD |

<!--
### Modelo Detallado - tasa asumida por usted {#detailed-model---fee-assumed-by-you}

**Saldo cuando el Payout es solicitado**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento| 10 USD |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 5 USD |
| Saldo para procesamiento | 2 USD |
| Saldo disponible | 3 USD |

**Saldo si el Payout fue pagado**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 10 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 3 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 3 USD |

**Saldo si el Payout fue rechazado.**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 20 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 3 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 3 USD |

_Si el Payout es rechazado, la tasa de procesamiento no se reembolsa._

### Modelo Detallado - tasa asumida por el beneficiario {#detailed-model---fee-assumed-by-the-payee}
**Saldo cuando el Payout es solicitado**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento| 10 USD |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 5 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 5 USD |

**Saldo si el Payout fue pagado**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 10 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 10 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 5 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 5 USD |

**Saldo si el Payout fue rechazado.**

<div id="shortTable"></div>

| Saldo para Payouts |  |
|---|---|
| Saldo Total | 20 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 20 USD |

<div id="shortTable"></div>

| Saldo para tasas |  |
|---|---|
| Saldo Total | 5 USD |
| Saldo para procesamiento| - |
| Saldo disponible | 5 USD |
-->