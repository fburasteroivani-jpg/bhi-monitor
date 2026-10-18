BHI Consultora Regional

# Simulador de bonos

BHI Consultora Regional, Asset Management. Sensibilidad de precio y retorno ante cambios de TIR.

Para actualizar precios desde IOL, abrí el simulador desde claude.ai con el conector de IOL activo.

## Sensibilidad de la cartera de bonos

Cuando la TIR (el rendimiento que exige el mercado) sube, el precio del bono baja, y al revés. Cuánto se mueve el precio depende de la **duration modificada**: un bono con duration 5 pierde cerca de 5% por cada 100 pb (1 punto porcentual) de suba de TIR. Si además se mantiene el bono un tiempo, los cupones y amortizaciones cobrados funcionan como colchón. El simulador calcula todo con el flujo de fondos de cada bono cargado.

Movés las barras y la tabla se recalcula. Tocá una fila para ver el detalle de ese bono. Los bonos, precios y montos se cargan en [Cartera y carga de bonos](#cartera).

### Escenarios predefinidos

Aplican un cambio de TIR distinto a cada bono

Tasa 10 años EE.UU. **0 pb**

Prima por ley local **0 pb**

Mueve solo a los Bonares: el spread de ley argentina sobre ley Nueva York.

Riesgo país **0 pb**

Suba/baja de TIR paralela **0 pb**

Pendiente de la curva **0 pb**

Positivo empina (los largos suben más); negativo aplana.

Horizonte de tenencia **Hoy**

Precios en

Filtrar:

Punto de partida Elegí una fecha anterior para simular desde esos precios y comparar con lo que pasó hasta hoy.

Ordenar por

| Bono | Ley | Precio hoy | TIR hoy | Duration | Δ TIR | TIR nueva | Precio si sube hoy | Var. hoy | Δ TIR real | Var. real | Simulado − real | Cobrado en el período | Precio al horizonte | Retorno al horizonte | Colchón de TIR | Monto US$ | Resultado US$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Precios por cada 100 nominales originales (valor dirty). Precios MEP de cierre del 23/09 (liquidación 24/09). En modo cable se descuenta el canje cargado en la pestaña Cartera. **Precio si sube hoy** = precio si la TIR saltara hoy mismo. **Precio al horizonte** = precio al final del plazo elegido con la TIR nueva. **Retorno al horizonte** = (cobrado en el período + precio al horizonte) ÷ precio hoy − 1, sin reinvertir. **Colchón de TIR** = cuántos pb puede subir la TIR durante el horizonte sin que el retorno sea negativo. Las columnas de monto aparecen cuando cargás montos en la cartera.

### –

Curva precio–TIR del bono seleccionado

Precio

–

TIR

–

Retorno al horizonte

–

### Matriz de sensibilidad

Verde: ganancia. Rojo: pérdida. La columna "Hoy" muestra el efecto precio inmediato.

### Retorno de todos los bonos en este escenario

## Soberanos vs obligaciones negociables

Las ONs de las empresas de primera línea rinden **menos** que el soberano de la misma duration. Es algo poco habitual: en casi todo el mundo una empresa paga más que su país. Acá pasa por varias razones: muchas de estas compañías generan dólares con exportaciones o tarifas en dólares, tienen casi todo su historial de pagos intacto en las crisis, hay poca oferta de ONs frente a mucha demanda local de dólares, y el inversor argentino las usa como refugio frente al riesgo soberano.

Esa diferencia es el **spread**: la TIR de la ON menos la TIR de la curva soberana a la misma duration. Un spread negativo significa que la ON rinde menos que el soberano. La curva soberana se estima con todos los Bonares o Globales cargados.

### Por qué importa para la sensibilidad

Qué implica el spread en cada escenario

- **Si el riesgo país sube**, las ONs suelen moverse menos (β RP bajo): amortiguan la cartera y el spread se hace más negativo.
- **Si el riesgo país baja**, los soberanos tienen más recorrido: su TIR puede caer hacia la de las ONs, que ya rinden poco. El spread tiende a cerrarse.
- **Si sube la tasa de EE.UU.**, pega parecido en los dos, porque ambos son bonos en dólares.

### Curvas de rendimiento

TIR según duration. Las líneas son las curvas soberanas estimadas.

### Spread de cada ON

En pb. Negativo: la ON rinde menos que el soberano de igual duration.

### Detalle por ON

Ordenar por

"En el escenario" usa las barras y el escenario elegidos en la pestaña Simulador. "Δ vs referencia" compara con la última foto guardada.

| ON | Duration | TIR | Curva Bonares | Spread vs Bonares | Curva Globales | Spread vs Globales | Spread vs Bonares en el escenario | Δ vs referencia |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

La curva soberana se estima con los bonos de cada grupo (TIR = a + b·ln(duration) + c·ln(duration)²) y se extiende plana más allá de la duration máxima del grupo. Es un promedio: un bono puntual puede quedar arriba o abajo. Las ONs son ley local, por eso la comparación más directa es contra Bonares; contra Globales se ve el spread respecto de la deuda ley Nueva York.

## Analizar una cartera

Elegí los bonos y cuánto tenés de cada uno. El simulador los analiza como un conjunto: rendimiento promedio, cuánto gana o pierde la cartera en cada escenario, a qué riesgos está expuesta y cuándo cobrás. Podés ver la parte en dólares, la parte en pesos o todo junto medido en dólares.

### Carteras guardadas

Guardá una cartera por cliente y volvé a abrirla cuando quieras

Administrar carteras guardadas

Pie del informe

### Composición

Cargá el monto en dólares de cada bono. Los que quedan en cero no forman parte de la cartera.

Total a repartir US$

|  | Bono | Grupo | Monto US$ | Peso | Precio | Nominales | TIR | Duration | Aporte a la duration |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

### Escenarios

Resultado de toda la cartera, hoy y a 12 meses si la nueva TIR se mantiene

### Sensibilidad

Cuánto cambia el valor de la cartera por cada factor, con los β de cada bono

### Si se mueve el riesgo país

Bonos en dólares: cambio de valor hoy y retorno a 12 meses si el riesgo país queda en cada nivel

### Qué se cobra y cuándo

Renta y amortización de toda la cartera por trimestre, en US$

### Distribución

Por tipo de bono y por plazo (duration)

### Cómo le hubiera ido

Valor de la cartera actual con los precios históricos, sumando lo cobrado. Necesita el historial de la pestaña Calibrar.

### Calibración de la cartera en conjunto

Cuánto se movió la cartera completa frente a la tasa de EE.UU., el riesgo país y la prima por ley local, semana a semana. Necesita el historial de la pestaña Calibrar.

### De dónde viene el riesgo

Qué parte de la sensibilidad total de la cartera aporta cada bono, con sus β

### Fondos comunes de inversión

Sumá fondos de Balanz, Valiant o IEB y cargá el monto en la moneda de cada fondo. El rendimiento esperado es la TIR de la cartera del fondo que calcula Fonditos (o, si no la informa o cubre menos de la mitad del fondo, su rendimiento de los últimos 30 días llevado a un año): en dólares para los fondos en dólares y dollar linked, en pesos para los fondos en pesos. La cuotaparte se actualiza con Fonditos: mientras no haya un dato nuevo queda el último.

Buscar fondo

El valor de la cuotaparte es cada 1.000 cuotapartes, como informa la CAFCI. En los escenarios, cada fondo rinde su tasa esperada durante el horizonte: los fondos en dólares, en dólares; los dollar linked, su tasa en dólares más la suba del dólar oficial de cada escenario; los fondos en pesos, su tasa en pesos, pasada a dólares con el dólar de cada escenario. Podés reemplazar la tasa esperada escribiendo otra en la tabla.

### CEDEARs

Sumá CEDEARs con el monto en dólares. Se valúan con el precio en pesos de IOL al dólar MEP. El retorno esperado y la volatilidad salen de los últimos 10 años de la acción (como en la optimización de Cartera CEDEARs).

CEDEARMonto US$

En los escenarios, cada CEDEAR rinde su retorno anual histórico de 10 años (en dólares) durante el horizonte, igual en todos los escenarios. La volatilidad es el desvío anual de los retornos diarios.

### Composición en pesos

Cargá el monto en pesos de cada instrumento. Son los mismos montos de la pestaña Renta fija en pesos.

Total a repartir $

|  | Instrumento | Tipo | Días | Tasa de mercado | Monto $ | Peso | Retorno al horizonte |
| --- | --- | --- | --- | --- | --- | --- | --- |

Horizonte

Medido en

Lo que vence antes del horizonte se reinvierte a la TAMAR de tus supuestos hasta esa fecha. Los retornos usan los supuestos de inflación, dólar y TAMAR de la pestaña Renta fija en pesos.

### Flujo de fondos esperado

Cuánto cobra cada instrumento al vencer (capital más intereses o ajuste) en cada escenario de la cartera completa, ponderado por su probabilidad. Las probabilidades se editan en Mi cartera → Todo junto.

En los duales se indica con qué probabilidad paga cada pata. "En US$ MEP al cobro" divide el cobro por el MEP proyectado a esa fecha en cada escenario; "En pesos de hoy" lo descuenta por la inflación proyectada.

### Escenarios

Retorno de toda la cartera al horizonte

### A qué está expuesta

Cuánto cambia el retorno de la cartera al horizonte si cada variable se aparta de tus supuestos

### Qué vence y cuándo

Cobro al vencimiento por mes, en millones de pesos: esperado (ponderado por la probabilidad de cada escenario), peor y mejor escenario

### Por tipo

### Tenencias

Todos los instrumentos de la cartera, valuados en pesos y en dólares

### Exposición por moneda

Qué parte de la cartera está atada a cada moneda

### Tipo de activo

Composición por tipo de instrumento

### Cartera total medida en dólares

Bonos en dólares con el escenario del Simulador a 12 meses; pesos con tus supuestos a 12 meses, pasados a dólares MEP

Los pesos se pasan a dólares al MEP (AL30/AL30D de IOL). Hacia adelante el MEP sigue al oficial de tus supuestos más el cambio de brecha de cada escenario.

### Retorno esperado de toda la cartera

Cada escenario combina qué pasa con los bonos en dólares y con los pesos. Asignale una probabilidad a cada uno: el retorno esperado es el promedio ponderado.

Horizonte

Medido en

Tipo de cambio

MEP hoy $ Cobros en US$ se reinvierten al % anual

### Cambio de la tasa de mercado de los instrumentos en pesos

Cuántos puntos básicos sube o baja la tasa que exige el mercado a cada segmento en cada escenario. Mueve el precio al horizonte (no el cobro al vencimiento). Sale de la calibración con el riesgo país y del traslado de la TAMAR; podés corregir cualquier valor (queda en negrita).

### Seguimiento diario

Guardá el valor de la cartera todos los días y calculá su retorno compuesto. Funciona sobre la cartera guardada que tengas elegida arriba; el historial queda en la pestaña **Seguimiento**.

Desde

Si elegís una fecha pasada, se reconstruye el valor de las tenencias actuales día por día con los precios históricos de IOL.

### Actualidad macro-financiera

Lo que dicen los informes de research de la semana (viernes a viernes), en Argentina y el mundo. Esta vista es de uso interno: muestra qué casa dice cada cosa. El PDF para clientes sale con la voz de BHI, sin nombrar casas y sin recomendaciones de inversión.

Semana

Todavía no hay semanas cargadas. Subí los informes de research en el chat con Claude y se van a ver acá.

### Lo más importante de la semana

### El mundo

### Argentina

### Gráficos de la semana

### Datos de la semana

### Ideas de inversión

Agrupadas por activo: cuántas casas lo recomiendan y cómo le fue desde la primera recomendación de la semana (solo precio). Verde: comprar · gris: mantener o neutral · rojo: reducir. Cada casa aparece con el color de lo que recomienda.

### Agenda

### Informes cargados

## Seguimiento de carteras

El valor de cada cartera que seguís, día por día, con su retorno compuesto en dólares y en pesos. Cada vez que abrís el simulador completa solo los días que falten con los precios de cierre de IOL, así no hace falta entrar todos los días.

### Actualizar

Completa todas las carteras hasta el último cierre

### Carteras

Tocá una para ver su detalle

### Comparar carteras

Retorno acumulado de cada cartera desde que la seguís (base 100). Cada una arranca en su propia fecha de inicio.

Valores al MEP de cada día. El retorno es por tiempo: las compras y ventas no cuentan como ganancia.

Ver períodoAñoDesdeHasta

### Informe de desempeño para el cliente

PDF con el retorno del período, en el año y desde el inicio, contra inflación (IPC y CER) y dólar; riesgo; resultado por activo; escenarios hacia adelante y cómo diseñamos la cartera.

Período MesTrimestreAño DesdeHasta Rendimiento a mostrarTipo de cliente

### Lo que esperábamos y lo que pasó

Retorno a 12 meses de cada escenario el día que se armó la cartera, llevado al tiempo transcurrido, contra lo obtenido.

### Revisiones trimestrales

Cada tres meses se guarda una foto: tenencias, TIR de ese día y el set vigente de la pestaña Escenarios, con lo que se espera para los 12 meses siguientes. Cada tramo se compara con su propia foto; la expectativa del inicio queda fija arriba.

### Aportes y rescates

El retorno de la gestión (TWR) no cuenta los aportes ni los rescates; el rendimiento del cliente sí pondera cuándo entró y salió la plata.

Movimiento Fecha Moneda Monto Destino Activo

El efectivo rinde (TNA %):PesosDólares

Un movimiento con fecha pasada se aplica al cierre de ese día y la cartera se recalcula desde el inicio con los precios de IOL. "Proporcional" reparte el aporte o el rescate según el peso actual de cada activo. Los cambios hechos con "Guardar" en Mi cartera aparecen acá como compras o ventas.

### Riesgo de la cartera

### Tenencias y precios

Nominales fijados con los precios del día en que se guardó la cartera. Cada día se valúan con el cierre de IOL y el retorno del día compara contra el cierre anterior.

## Renta fija en pesos: tasa fija, CER, TAMAR, dollar linked y duales

Cada instrumento en pesos paga según una variable distinta: la **tasa fija** (Lecap y Boncap) ya sabe cuánto va a cobrar; el **CER** ajusta por inflación; el **TAMAR** capitaliza la tasa de los plazos fijos mayoristas más un margen; el **dollar linked** ajusta por el tipo de cambio oficial (A3500), y los **duales** pagan lo mejor de dos de esas patas.

Con la tasa de mercado de cada uno y tus supuestos de inflación, TAMAR y dólar, el simulador proyecta cuánto cobrás en pesos, en términos reales y en dólares, y calcula el **breakeven**: la inflación, el dólar o la TAMAR que hace falta para empatar a la tasa fija.

### Escenarios rápidos

Se suman a tus supuestos de la tabla de abajo

### Supuestos macro

Promedio mensual de cada tramo. Editá cualquier celda; todo se recalcula al instante.

Tasas de mercado al Dólar oficial A3500 hoy Brecha MEP / oficial (%) [ ] Actualizar con el MEP Referencia: REM inflación 12m a dic-26 % Referencia: REM dólar dic-26

Inflación mensual **+0,0 pp**

Mueve el CER y la inflación que deflacta el retorno real.

Devaluación mensual **+0,0 pp**

Mueve el dollar linked y el retorno en dólares.

TAMAR **+0 pp**

Tasas de mercado **0 pb**

Solo afecta si vendés antes del vencimiento.

Horizonte **Al vencimiento**

0 = mantener hasta el vencimiento de cada uno.

Mostrar retornos

Filtrar:

### Qué implican tus variables

Con los supuestos de la tabla más lo que muevas en las barras: cuánta inflación se acumula, dónde queda el dólar oficial y qué TAMAR promedia en cada período

Ordenar por

| Instrumento | Tipo | Días | Tasa de mercado | TEM proyectada | Cobro por $100 | Retorno total | Retorno anual | Breakeven vs tasa fija | Tu supuesto | Monto $ | Resultado |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

**Tasa de mercado**: TEM para tasa fija, TIR real para CER, TIR en dólares para dollar linked y margen sobre TAMAR para TAMAR. **TEM proyectada**: tasa mensual en pesos que resulta de tus supuestos. **Retorno total** y **anual** se expresan en la unidad elegida arriba (pesos, reales o dólares). **Breakeven**: inflación mensual promedio (CER), devaluación mensual promedio (dollar linked) o TAMAR promedio (TAMAR) que iguala a la curva de tasa fija al mismo plazo; para una Lecap es la inflación que descuenta frente a la curva CER. **Tu supuesto** es el promedio de tu trayectoria hasta ese vencimiento: si supera al breakeven, gana el instrumento indexado. Cuando el plazo supera al de la curva de comparación (la tasa fija llega hasta jun-27), el breakeven se marca como extrapolado.

### CER breakeven

Qué inflación mensual promedio hace falta para que cada instrumento CER empate a la tasa fija de su mismo plazo, y en los duales CER/TAMAR, a partir de qué inflación paga más la pata CER que la TAMAR. Tocá una fila para verla en el gráfico.

### Inflación que descuenta la curva

Breakeven de cada CER según su plazo, contra tu trayectoria de inflación

### Instrumento seleccionado

Retorno anual en pesos al vencimiento según la inflación mensual constante

| Instrumento | Vence | TIR real | Breakeven vs tasa fija | Tu inflación | Margen de seguridad | Cruce con la pata TAMAR | Con tu inflación |
| --- | --- | --- | --- | --- | --- | --- | --- |

Margen de seguridad: cuánto puede bajar la inflación promedio respecto de tu supuesto antes de que el CER pierda contra la tasa fija. Los plazos más largos que junio 2027 se comparan contra la curva de tasa fija interpolada hasta el TY30P, por eso se marcan como aproximados.

### TAMAR breakeven

Qué TAMAR constante hace falta para que cada instrumento TAMAR empate a la tasa fija de su mismo plazo, y en los duales, a partir de qué TAMAR paga más la pata TAMAR que la otra. Tocá una fila para verla en el gráfico.

| Instrumento | Vence | Margen | TAMAR breakeven vs tasa fija | Cruce con la otra pata | Con tu TAMAR |
| --- | --- | --- | --- | --- | --- |

### TAMAR: tus supuestos contra lo que descuenta el mercado

Forwards de TAMAR de Fonditos: la TAMAR mensual que tienen implícita los precios de las Lecaps y Boncaps (curva de tasa fija corregida por el spread de la TAMAR). Se usan como escenario "Mercado (TAMAR forward)" en los escenarios de la cartera.

Analizar o tocá una fila de la tabla

### –

En pesos

–

Real

–

En dólares

–

### Matriz inflación × dólar

### Curva proyectada

Retorno anual según días al vencimiento

### Retorno de todos en este escenario

### Evolución de precios y tasas

Cada actualización con IOL guarda el precio y la tasa de cada instrumento del día, para ver cuánto se movieron.

Comparar contra

### Instrumentos en pesos

Cargá la tasa de mercado que ves en pantalla. En los duales completá las dos patas; el simulador toma la que paga más.

| Instrumento | Tipo | Vencimiento | TEM fija % | TIR real % | TIR USD % | Margen TAMAR % | Monto $ | Nota |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

### Importar o exportar desde Excel

Columnas: **instrumento; tipo; vencimiento; tem_fija; tir_real; tir_usd; margen_tamar; monto**. Tipo: fija, cer, dl, tamar o dual. Las columnas que no apliquen van vacías.

## CEDEARs: acciones y ETFs del exterior

Un CEDEAR representa una fracción de una acción o ETF del exterior. Su precio en pesos es el precio de afuera, dividido por el **ratio** y multiplicado por el **CCL**. Por eso gana o pierde por dos lados: lo que haga la acción en dólares y lo que haga el dólar contado con liquidación.

Los ratios salen del listado de BYMA. Con el precio en pesos de IOL y el de la acción afuera, el simulador calcula el **CCL implícito** de cada uno y marca los que se alejan del resto: casi siempre es un ratio que cambió o un papel que operó poco.

### Escenario

Cada CEDEAR se mueve β × S&P 500 + su ajuste propio; el CCL mueve a todos igual en pesos

S&P 500 %CCL %

### Todos los CEDEARs

Los precios se actualizan junto con los bonos, al tocar "Actualizar precios desde IOL", y quedan guardados. También podés actualizar solo los CEDEARs con el botón de acá.

BuscarSectorMercado

| CEDEAR | Sector | Mercado | Ratio | Precio $ | Acción US$ | CCL implícito | Desvío | Volumen $ M | β S&P | Correl. | R² | Ajuste % | Retorno US$ | Retorno $ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

El β calculado sale de los retornos diarios de la acción en su mercado de origen contra el SPY (con splits ajustados): β = covarianza / varianza del S&P 500. Un β alto con R² bajo quiere decir que la acción se mueve mucho pero por motivos propios, no por el mercado. Si cambiás un β a mano, queda el tuyo hasta que vuelvas a calcular. Antes de calcular, β por defecto: 1 para acciones; en los ETFs, según lo que siguen (QQQ 1,2; apalancados 3 o más; inversos negativos; oro, plata, cripto y materias primas 0). Son valores de referencia: corregilos en la tabla. Un desvío de CCL de más de 3% se marca en rojo: revisá el ratio en BYMA o si el papel operó poco.

## Cartera de CEDEARs: riesgo, retorno y frontera eficiente

Con los precios diarios de cada acción en su mercado de origen, el simulador calcula el retorno esperado, la volatilidad, el VaR y el CVaR de la cartera, la compara contra el **S&P 500** (SPY) con beta, alpha, tracking error e information ratio, y arma la **frontera eficiente de Markowitz**: la cartera de máximo Sharpe y la de mínima volatilidad.

El análisis es en dólares sobre la acción de afuera: un CEDEAR replica ese retorno y le suma lo que se mueva el CCL si lo medís en pesos.

### Parámetros

Historia Tasa libre de riesgo % anual Peso mínimo por activo % PPP cargado en Peso máximo por activo %

El mínimo y el máximo generales se aplican a los activos que no tengan uno propio: en la tabla de composición, las columnas Mín. % y Máx. % permiten fijarlos activo por activo. Los límites valen para las carteras optimizadas (sin ventas en corto). La tasa libre de riesgo se usa en el Sharpe y en el alpha.

### Composición

Elegí los CEDEARs (de la lista o escribiendo el ticker) y poné tus pesos. Si no suman 100%, se normalizan. **Para evaluar una cartera que ya tenés**, cargá la cantidad de CEDEARs y el precio promedio de compra (PPP): los pesos salen solos del valor de mercado de hoy y se calcula la ganancia de cada posición.

Agregar SectorMercado Cuántos

| CEDEAR | Acción afuera | Sector | Cantidad | PPP | Compra | Tus pesos % | Mín. % | Máx. % | Máx. Sharpe % | Mín. volatilidad % | Retorno anual | Volatilidad | β S&P | Correl. S&P |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

### Armar la cartera a precios de hoy

Con un monto a invertir y los pesos elegidos, calcula cuántos CEDEARs comprar de cada uno con los precios de hoy en IOL. Después la podés cargar como tu cartera para seguirla.

Monto a invertir Moneda Con los pesos de

Se compran CEDEARs enteros: primero la cantidad que entra en cada peso y después, con lo que sobra, un CEDEAR más de los que quedaron más lejos de su peso, mientras alcance. En dólares se usa el precio de la línea D si operó hoy; si no, el precio de la acción afuera dividido por el ratio. No incluye comisiones ni derechos de mercado.

### Tu cartera hoy

Valuada con los últimos precios de IOL

Valor en dólares: cantidad × precio de la acción afuera ÷ ratio (equivale a valuar al CCL implícito de cada CEDEAR). Con el PPP en pesos, la ganancia en dólares se calcula llevando el costo al CCL de hoy, así que no incluye lo que se movió el CCL desde que compraste: para eso cargá el PPP en dólares.

### Qué pasó desde que compraste

Con la fecha de compra de cada posición, reconstruye la historia de tu cartera en dólares y la compara con haber comprado el S&P 500 esos mismos días.

En dólares, sobre la acción en su mercado de origen (precios ajustados por splits, sin dividendos). El retorno de la cartera se mide por tiempo (TWR): cada posición entra el día que la compraste, sin contar esa compra como ganancia. "Si hubieras comprado S&P 500" invierte en el SPY lo mismo que valía cada posición el día de compra.

### Frontera eficiente

Cada punto gris es una cartera al azar; la línea es la frontera. Retorno y volatilidad anualizados.

### Evolución de US$ 100

Tus pesos, máximo Sharpe y mínima volatilidad contra el S&P 500, rebalanceando todos los días

### Métricas

Anualizadas con 252 ruedas. VaR y CVaR históricos de un día: la pérdida que no se supera en el 95% (o 99%) de los días, y la pérdida promedio en el peor 5% (o 1%).

Precios diarios de cierre de IOL en el mercado de origen (el mismo dato que publica Yahoo Finance; la página no puede conectarse a Yahoo directamente). Los splits se detectan y ajustan automáticamente (el mensaje al terminar indica cuáles). Los precios no están ajustados por dividendos: para acciones que pagan mucho dividendo, el retorno y el alpha quedan un poco por debajo del retorno total. El S&P 500 se mide con el ETF SPY. Retornos y riesgo pasados no garantizan los futuros: el retorno esperado de Markowitz es el promedio histórico y es la parte más inestable del cálculo.

### Correlaciones

Correlación de los retornos diarios entre cada par de activos y con el S&P 500. Cerca de 1: se mueven juntos y diversifican poco; cerca de 0 o negativa: diversifican.

β contra el S&P 500 = correlación × (volatilidad del activo ÷ volatilidad del S&P 500). Por eso dos activos pueden tener el mismo β con correlaciones muy distintas.

### Pesos de cada cartera

### Exposición por sector y por mercado

## Curvas de rendimiento

Rendimiento de cada bono contra su plazo, con precios del simulador (tocá "Actualizar precios desde IOL" para tener los de hoy). La línea es la tasa justa de cada curva: los bonos verdes rinden más que sus pares de igual plazo (baratos) y los rojos, menos (caros). Tocá cualquier bono para ver la explicación completa.

### Soberanos en dólares: Globales y Bonares

TIR en dólares contra duration modificada

### Obligaciones negociables en dólares

TIR en dólares contra duration modificada

### Tasa fija: Lecaps y Boncaps

Tasa efectiva anual (TEA) contra plazo en años

### CER

TIR real (por encima de la inflación) contra plazo en años

### TAMAR

Margen sobre la TAMAR (puntos anuales) contra plazo en años

### Dollar linked

TIR en dólares (ajusta por el dólar oficial) contra plazo en años

### Tabla de las curvas

Tocá un bono para ver la explicación completa.

### Rotaciones sugeridas

Salir de un bono caro (rinde menos que su curva) y entrar en uno barato de la misma curva, con igual o menor plazo y más tasa. Curva ajustada por mínimos cuadrados (tipo Nelson-Siegel, que sube rápido en el tramo corto y se aplana en el largo), restándoles peso a los bonos muy alejados; la banda punteada es ±1 desvío. Los que vencen en menos de \~36 días no se evalúan. Tocá un bono en el gráfico o en la tabla para ver la explicación.

## Fundamentals

Ratios de los estados contables de cada empresa, puntaje por estilo, DCF y DCF inverso. Sirve para elegir qué CEDEARs entran al análisis antes de optimizar la cartera.

Estilo

ROIC mínimo % Deuda/EBITDA máx. Piotroski mín. Altman Z mín. Margen de seguridad mín. % [x] Crecimiento implícito ≤ pronosticado

Prima de riesgo de mercado % Crecimiento de largo plazo %

## Fondos comunes de inversión: Balanz, Valiant e IEB

Todos los fondos de las tres gestoras, con datos de la CAFCI a través de Fonditos: categoría, moneda, patrimonio, honorarios, valor de la cuotaparte y rendimientos. Tocá un fondo para ver su evolución. Con **+ Mi cartera** lo sumás a la cartera de renta fija como una clase de activo más, y con **+ CEDEARs** a la cartera de CEDEARs.

El valor de la cuotaparte se informa cada 1.000 cuotapartes, como publica la CAFCI. Los rendimientos salen de la serie diaria de ese valor, ya netos de honorarios.

### Datos

Todavía no se cargó el listado.

Buscar Gestora Categoría [x] Solo con patrimonio mayor a $ 100 M

## Analizar un bono

Elegí cualquier bono de la cartera, en dólares o en pesos, y mirá su ficha completa: flujo de fondos, sensibilidad, escenarios y breakeven. Usa los mismos datos y supuestos que el resto del simulador.

Bono

## Calibrar con la historia de precios

Trae de IOL los precios diarios de cada bono, calcula su TIR día por día y mide cuánto se movió realmente frente al riesgo país. Así el β de cada bono sale de los datos y no de un supuesto.

El **riesgo país propio** se arma con los mismos precios: promedio de TIR de GD30, GD35, GD38, GD41 y GD46 menos la tasa a 10 años de EE.UU. (serie del Tesoro de EE.UU.). La **prima por ley local** es el promedio de AL30, AL35, AE38 y AL41 menos el de los Globales (bonos que cotizan desde 2020, para que la referencia sea siempre la misma). Se usan cambios semanales para filtrar el ruido diario.

### Período

Más historia da β más estables e incluye la crisis de septiembre–octubre 2025; menos historia refleja mejor el momento actual

### Factores en el período

Riesgo país (EMBI, oficial donde hay dato) y prima por ley local, día por día

### Bono seleccionado

Cada punto es una semana. La pendiente de la línea roja es el β estimado.

### Serie completa del riesgo país

Día por día, con la prima por ley local, las TIR promedio de Globales y Bonares y la tasa a 10 años de EE.UU. que se usan en la calibración

Fuente del dato oficial: cierres del EMBI Argentina de JP Morgan publicados por Rava (2025) y ámbito (2026). Esas series tienen días sin actualizar y a veces se publican con un día de diferencia; por eso se usan solo los días en que el dato cambió. El riesgo país propio se calcula con los precios de IOL y sirve para completar los días sin dato oficial.

### β estimados

Se estima en simultáneo cuánto se mueve cada bono con la tasa del Tesoro de EE.UU. a su mismo plazo (su duration, interpolando entre 2, 5 y 10 años), con el riesgo país y (en los Bonares) con la prima por ley local. Tocá una fila para ver su gráfico. Marcá los que quieras usar y aplicalos: reemplazan los β del simulador. Los soberanos quedan con β 1 en todos los factores (la curva soberana se mueve por plazo, no por nombre), salvo el AO27, que por estar descorrelacionado toma su β calibrado.

|  | Bono | Semanas | Tasa EE.UU. usada | β UST actual | β UST estimado | Correl. UST | β RP actual | β RP estimado | Correl. RP | β ley actual | β ley estimado | R² | Ruido propio |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

**Correlación**: de −1 a 1, qué tan juntos se mueven los cambios semanales de la TIR del bono con cada factor por separado. **R²**: qué parte del movimiento semanal explican los factores juntos. **Ruido propio**: cuánto se mueve por semana por su cuenta, en pb; sirve para saber el rango habitual alrededor de lo que dice el simulador. Se marcan por defecto los que tienen al menos 8 semanas y R² de 15% o más. Las semanas con saltos anómalos (más de 3 desvíos) se descartan antes de estimar.

### Tasas en pesos: cuánto se mueven con el riesgo país

Trae de IOL los precios semanales de las Lecaps, Boncaps, CER y TAMAR desde enero de 2025 y mide cuántos puntos básicos se mueve su tasa por cada punto básico de riesgo país (EMBI). Se estima por segmento, juntando todos los instrumentos del mismo tipo y plazo. Usa la serie de riesgo país de arriba: traé primero el historial de los bonos en dólares.

Con esto, cada escenario mueve la tasa de mercado de cada segmento. Si el escenario mueve el riesgo país: Δ tasa = β × Δ riesgo país (el β ya incluye cómo reaccionaron las tasas locales en los episodios de 2025 y 2026, así que la suba de TAMAR no se suma aparte). Si solo mueve la TAMAR (endurecimiento local): Δ tasa = traslado × Δ TAMAR, con 100% en tasa fija, 50% en CER y 0% en el margen de los TAMAR. Los dollar linked se mueven al revés: cuando sube el riesgo país aumenta la demanda de cobertura y su tasa en dólares baja (β de referencia −0,75, no calibrado). Los valores por escenario se ven y se corrigen en Mi cartera → Todo junto.

## Cartera y carga de bonos

Cada bono se define por su **precio** y su **flujo de fondos** (fecha y monto de cada pago de renta y amortización por cada 100 nominales originales). Con eso el simulador calcula TIR, duration y todo lo demás. El flujo se puede generar a partir de vencimiento, cupón y amortización, o pegar tal cual desde Excel o del prospecto.

Los **β** indican cuánto se traslada a la TIR de cada bono un movimiento de la tasa a 10 años de EE.UU. y del riesgo país. Un soberano en dólares toma 1 y 1; una ON corporativa, 1 y 0,5 por defecto; ajustalos según el emisor. Los Δ de **Normalización** y **Estrés** son los cambios de TIR que usa cada escenario predefinido. Si los dejás vacíos, se calculan solos: β RP × el Δ de la curva soberana de la misma ley a igual duration (en gris ves el valor que toma). El **ajuste propio** se suma siempre, para reflejar una visión específica sobre un emisor.

### Parámetros generales

Aplican a todos los bonos

Fecha de liquidación (un día hábil después del cierre) Canje MEP a cable % Tasa 10 años EE.UU. hoy % Riesgo país hoy pb

[x] Actualizar con el último dato cargado

Los pagos con fecha igual o anterior a la de valuación se ignoran.

Guardá una foto antes de actualizar precios: después podés usarla como punto de partida en el Simulador y comparar contra lo que pasó.

### Bonos cargados

Precio, monto y escenarios se editan en la tabla. Para cambiar el flujo, tocá Editar.

| Bono | Grupo | Ley | Precio MEP | Próximo pago | Vencimiento | Pagos | TIR | Duration | Monto US$ | Δ Normalización pb | Δ Estrés pb | β UST | β RP | Ajuste propio pb |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

### Agregar ONs desde IOL

Pegá uno o varios tickers de ONs en dólares (YMCXO, YMCXD o YMCXC, separados por espacio, coma o renglón). Se trae de IOL el cronograma de pagos y el precio en dólares, y la ON entra en escenarios, carteras e informes. Si ya estaba cargada, se actualizan su flujo y su precio sin tocar sus β ni sus ajustes.

β RP por defecto: 0,25 para las AAA —YPF, Vista, Tecpetrol, TGS y Pampa (tickers YM…, VS…, VM…, TT…, TSC…, MGC…)— y 0,4 para el resto; se corrigen en la tabla o con la calibración. Ley: local por defecto. Las ONs en pesos no se agregan acá.

### Nuevo bono

Completá los datos y generá o pegá el flujo de fondos

Bono / ticker Grupo Ley Precio MEP (por 100 VN) Monto en cartera US$ β UST β RP Ajuste propio pb

Vencimiento Cupón % anual Frecuencia Amortización Valor residual % (VN vigente)

Genera pagos cada tantos meses hacia atrás desde el vencimiento. El cupón se calcula sobre el saldo vigente y las cuotas de amortización caen en los últimos pagos. Para bonos con cupón step-up o cronogramas irregulares, pegá el flujo.

Una fila por pago: fecha y monto por cada 100 VN originales (renta + amortización). Separador tab, punto y coma o coma; fecha dd/mm/aaaa o aaaa-mm-dd.

Completá precio y flujo para ver la TIR.

### Importar o exportar desde Excel

Formato largo: una fila por pago. Las columnas son **bono; grupo; ley; precio; fecha; flujo; monto; beta_ust; beta_rp**. Grupo, ley, precio, monto y betas se toman de la primera fila de cada bono; en las demás pueden ir vacíos.

## Carteras offshore

Seguimiento de carteras en brokers del exterior, valuadas en dólares con precios de Interactive Brokers: acciones y ETFs en vivo, bonos con la punta compradora (como valúa el broker) y fondos con la cuotaparte del día.

### Cómo se calcula

**Valor**: cantidad × precio de cada activo, más la liquidez. Los bonos van a precio limpio (sin intereses corridos), igual que el resumen del broker.

**Rendimiento**: ponderado por tiempo (TWR) desde que empezó el seguimiento; los aportes y retiros no cuentan como ganancia ni pérdida.

**Cupones**: se acreditan solos en la fecha de pago de cada bono (estimados hasta que se confirmen con el resumen). Los dividendos y las distribuciones de fondos se cargan como movimiento.

**TIR y duration**: de cada bono a su precio actual; en los bonos de tasa fija a variable es aproximada (se supone que mantienen el cupón actual).

### Resumen

### Composición

Por tipo de activo, sobre el valor total

### Evolución del valor

En US$, un punto por cada día que se actualizó

### Métricas de la cartera

Rendimiento, sensibilidad a tasas y riesgo

Cómo hubiera evolucionado la cartera actual en el último año (base 100), con los precios diarios de cada activo. Sirve para medir el riesgo de la composición de hoy.

### Historia de la cuenta

### Tenencias

### Movimientos

Aportes (+), retiros (−), dividendos y distribuciones de fondos. Los aportes y retiros no afectan el rendimiento.

## Monitor internacional

Lo que pasa afuera mueve a los bonos argentinos: si sube la tasa de EE.UU. o hay miedo en los mercados, el inversor del mundo le pide más rendimiento a Argentina; si suben la soja o el petróleo, entran más dólares al país. Acá se ve todo eso en un solo lugar, con precios de Interactive Brokers.

### Cómo leerlo

**Índices**: cómo les va a las bolsas. Se siguen con el ETF que replica cada índice (SPY para el S&P 500, EWZ para Brasil, etc.).

**Tasas de EE.UU.**: lo que paga el Tesoro americano. Es el piso de rendimiento del mundo: cuando sube, todos los bonos (los argentinos también) tienen que pagar más y sus precios bajan.

**VIX**: el "termómetro del miedo". Debajo de 15, calma; entre 15 y 20, normal; entre 20 y 30, nervios; arriba de 30, pánico.

**Commodities**: los granos en dólares por tonelada (Chicago) y el petróleo y el oro en su unidad habitual. Granos y petróleo son dólares que entran a la Argentina.

### Qué está pasando afuera, en criollo

Se escribe solo con los últimos precios

### Bolsas del mundo

Variaciones en dólares

Gráfico: base 100 hace seis meses. Si una línea termina arriba de 100, ese mercado subió.

### Tasas del Tesoro de EE.UU.

Rendimiento anual en %

Gráfico: la curva de tasas hoy, hace un mes y hace un año. Si la curva sube, el mundo exige más rendimiento.

### Commodities

Contrato de futuro más cercano

Gráfico: base 100 hace seis meses.

### VIX: el termómetro del miedo

Último año, con las franjas de calma, nervios y pánico

## Política monetaria, explicada fácil

La pregunta de fondo es simple: **¿la gente quiere tener pesos o se los quiere sacar de encima?** A eso los economistas le dicen **demanda de dinero**.

Pensalo como una heladera: si la gente guarda pesos en la heladera (en la cuenta o en un plazo fijo), esos pesos no salen a comprar dólares ni a empujar los precios. Si la gente vacía la heladera, esos pesos salen todos juntos a la calle: suben el dólar y la inflación.

Todo se mide **en términos reales**, es decir, descontando la inflación. Si tenés 10% más de pesos pero los precios subieron 20%, en realidad tenés menos plata. Eso es lo que importa.

### Diccionario rápido

**Base monetaria**: los pesos que "fabrica" el Banco Central. Es la materia prima de todo lo demás.

**M2 transaccional**: la plata para **gastar**. Los billetes en la billetera más lo que hay en la cuenta sueldo o la caja de ahorro.

**Plazo fijo**: la plata para **ahorrar** en pesos, la que se deja quieta a cambio de una tasa.

**M3**: **todos** los pesos de la gente y las empresas juntos (para gastar + para ahorrar).

**Tasa real**: cuánto gana un plazo fijo **después** de descontar la inflación. Si es positiva, ahorrar en pesos conviene; si es negativa, el plazo fijo pierde contra los precios.

**Multiplicador**: cuántos pesos terminan circulando por cada peso que fabrica el Banco Central, porque los bancos prestan y vuelven a prestar lo que reciben.

### Qué está pasando, en criollo

Se escribe solo con el último dato cargado

### Cuántos pesos tiene la gente

Billones de pesos constantes, promedio mensual

Cómo leerlo: si la línea sube, la gente tiene más pesos "de verdad" (ya descontada la inflación). De 2023 a abril de 2024 cae fuerte: con inflación de dos dígitos por mes, los pesos se derretían. Hasta mediados de 2025 sube: con menos inflación, la gente volvió a guardar pesos.

### ¿Más o menos pesos que hace un año?

% contra el mismo mes del año anterior, ya descontada la inflación

Cómo leerlo: compara cada mes con el mismo mes del año anterior. Arriba de cero, la gente tiene más pesos que hace un año; abajo de cero, menos.

### ¿Conviene ahorrar en pesos?

Lo que paga un plazo fijo grande por mes (TAMAR) contra la inflación del mes, en %

Cómo leerlo: la barra verde significa que ese mes el plazo fijo le ganó a la inflación (ahorrar en pesos convino). La roja, que perdió. Cuando hay muchas barras rojas seguidas, la gente se cansa de los pesos.

### ¿Para gastar o para ahorrar?

Qué parte de los pesos está para gastar (izq.) y multiplicador (der.)

Cómo leerlo: la línea azul es qué parte de los pesos está "para gastar". Si baja pero el total aguanta, la gente no se está yendo del peso: pasa plata de la cuenta al plazo fijo. La línea verde es el multiplicador; se mueve mucho cuando el Banco Central cambia las reglas de cuánto tienen que guardar los bancos.

### ¿La gente se pasa a dólares?

Dólares que la gente tiene depositados en los bancos y dólares que tiene el Banco Central (reservas), en miles de millones de US$

### Últimos 13 meses

Montos en billones de pesos de hoy (ya ajustados por inflación). "i.a." es cuánto cambió contra el mismo mes del año anterior.

## Escenarios

Los escenarios que usan Mi cartera, el Seguimiento y los informes de carteras multimoneda. Salen del REM de septiembre 2026 (mediana y percentiles), de la TAMAR que descuenta el mercado y del episodio de sep-oct 2025. Todo se calcula a 12 meses desde la fecha base del simulador, con el mismo motor que valúa las carteras.

### Escenarios a 12 meses

### Trayectoria mes a mes

### Qué supone cada escenario

Definiciones, en el orden en que se usan en los informes

## Wealth Management

Planificación patrimonial e impositiva de BHI para personas, familias y empresas familiares residentes en Argentina. Arranca por el diagnóstico del cliente y arma una hoja de ruta. Después baja a cada herramienta: impuestos de cada inversión, la foto del 31/12, persona o sociedad, inversiones en el exterior, estructuras, sucesión, mudanza, seguros y empresa familiar. Cada regla indica su norma, su fecha y si está verificada en fuente oficial. Normativa relevada al **11/10/2026**.

**Método.** Seguimos la secuencia de diez pasos de Litwak: objetivos ordenados, riesgos, patrimonio y planes, régimen legal de cada país involucrado, capacitación, herramientas, cláusulas y roles, jurisdicción y proveedor, acompañamiento y revisión periódica. Nunca se empieza por la herramienta: nadie quiere un trust, quiere los efectos que cree que le da. Completá lo que sepas; lo que falte aparece como pregunta pendiente.

### Cliente

Los diagnósticos se guardan en tu cuenta y se pueden volver a abrir.

Nombre del cliente o familia Diagnóstico guardado Tipo Domicilio del titular Edad del titular Situación familiar Patrimonio total aproximado (US$) Parte en Argentina (%) Activos en EE.UU. a nombre propio (US$) Cripto (US$) Cartera BHI asociada Plan de mudanza

### Objetivos, en orden de importancia

Para cada objetivo, la prioridad que le da el cliente (0 = no le importa, 3 = imprescindible). El orden cambia la herramienta.

### Perfil del contribuyente

El mismo instrumento tributa distinto según quién lo tenga. Los rendimientos brutos son de referencia y se pueden editar en la tabla.

Titular Ganancias, tasa marginal persona Bienes Personales, alícuota marginal (%) Adhirió al ingreso anticipado (REIBP) Ganancias sociedad, tasa marginal Ingresos Brutos sobre renta gravada (%) Bienes Personales acciones y participaciones (sociedad) Devaluación por encima de la inflación (%) Ordenar por

### Rendimiento bruto y neto por instrumento

**Cómo se usa.** 1) Armá la ficha del cliente con **todos** sus bienes, no solo la cartera con BHI: inmuebles, autos, otras cuentas. 2) Mirá cuánto paga hoy de Bienes Personales y Ganancias (y, si es una sociedad, Ingresos Brutos, Bienes Personales de acciones e impuesto al cheque). 3) Probá los cambios sugeridos o movés vos cualquier bien: se ve al instante el antes y el después. 4) Guardala y descargá el informe.

### Ficha del cliente

Cada ficha se guarda en tu cuenta. Podés traer las tenencias de una o varias carteras del Seguimiento y completar el resto a mano.

Cliente Ficha guardada Titular Agregar tenencias de una cartera Período fiscal Dólar para valuar ($) Ajuste estimado del mínimo 2026 (%) Tasa marginal de Ganancias por sus otros ingresos Adhirió al REIBP (ingreso anticipado) Cumplidor (beneficio 2023–2025) FCI y BOPREAL sin confirmar Resultado impositivo de la operativa ($/año) Inflación esperada 12 meses (%) Devaluación esperada 12 meses (%) Ingresos Brutos sobre renta no exenta (%) Patrimonio neto contable ($) Movimientos bancarios que podrían ir por la ALyC ($/año) Utilidades acumuladas distribuibles ($) Caja que la operativa necesita ($)

### Patrimonio

### Cambios sugeridos

Ordenados por beneficio neto anual. Suponen el mismo rendimiento en el activo de destino: si no es así, ajustá el rendimiento de destino en la fila.

### Antes y después

### ¿Mantener la inversión en la sociedad o repartirla?

### Supuestos y normas

### ¿Invertir a nombre propio o desde la sociedad?

Compara el mismo capital invertido por la persona y por su sociedad. La sociedad paga Ganancias sobre toda la renta financiera; la persona tiene exenciones pero paga Bienes Personales.

Capital (US$) Rendimiento bruto anual (%) Parte exenta para la persona (%) Tasa marginal persona sobre lo gravado (%) Bienes Personales persona (%) Ganancias sociedad (%) Ingresos Brutos sociedad sobre la renta (%) BP acciones y participaciones (%) Impuesto al cheque al entrar y salir (%) La sociedad reparte lo ganado Horizonte (años)

### Capital acumulado

Reinvirtiendo el neto cada año

### Costo fiscal del primer año

### Lo que la cuenta simple no muestra

### Impuesto a la herencia de EE.UU.

Lo pagan los herederos de un extranjero no residente que muere con activos situados en EE.UU. por más de US$ 60.000. Argentina no tiene tratado con EE.UU.

Acciones y ETFs de EE.UU. (US$) Inmuebles en EE.UU. (US$) Otros activos situados en EE.UU. (US$) No situados: CEDEARs, ETFs irlandeses, bonos, depósitos (US$)

### Cómo tener S&P 500 desde Argentina

Mismo índice, cuatro vehículos. Cambian la retención, Ganancias, la herencia de EE.UU. y los costos.

Monto (US$) Retorno total anual (%) Dividendo anual (%) Años Tasa marginal Ganancias (%) Bienes Personales (%)

### Inmuebles en EE.UU.

Alquiler y venta de un inmueble por un no residente (presentación de E. Baltar, UCEMA 2026).

Valor de compra (US$) Alquiler bruto anual (US$) Gastos anuales (US$) Amortización + intereses deducibles (US$) Precio de venta futuro (US$) Titular

### Cinco formas de tener el inmueble en EE.UU.

"Elegí tu veneno": ninguna es perfecta

### Paso 1 · ¿Qué quiere lograr el cliente?

Elegí uno o más objetivos. Se cargan solos los que marcaste como importantes en el Diagnóstico.

### Paso 2 · Herramientas que conviene mirar

### Paso 3 · Comparación completa

Todas las herramientas contra todos los objetivos. **●** lo resuelve bien · **○** ayuda en parte · vacío: no sirve para eso. Las columnas elegidas están resaltadas.

### Trust: cuándo protege y cuándo no

### Elegir jurisdicción y proveedor

### Legítimas y porción disponible

Cuánto se puede dejar libremente por testamento o donación (Código Civil y Comercial, arts. 2445 y siguientes).

Patrimonio a transmitir ($ o US$) Hijos o descendientes Cónyuge sobreviviente Ascendientes vivos (si no hay hijos) Parte ganancial del patrimonio (%)

### Impuesto a la herencia y donaciones de la Provincia de Buenos Aires

Impuesto a la transmisión gratuita de bienes, escala 2026. Solo existe en esta provincia.

Monto que recibe cada beneficiario ($) Parentesco Cantidad de beneficiarios Dólar ($)

### Herramientas de sucesión en Argentina

**La herramienta definitiva, si es real.** Mudarse cambia todo: renta mundial, Bienes Personales y ley aplicable a la herencia. Pero lo difícil no es conseguir la residencia nueva sino perder la argentina, y las mudanzas simuladas terminan peor que no haberse ido.

### Del lado argentino

### Checklist antes de irse

### Destinos frecuentes para argentinos (relevado a oct-2026)

### Tipos de seguro de vida

### Seguro para acuerdo entre socios

Si muere un socio, la póliza paga su parte a la familia y los demás se quedan con las acciones.

Valor de la empresa (US$) Cantidad de socios Margen por crecimiento (%) Persona clave: meses de facturación a cubrir Facturación mensual (US$)

### Tratamiento en Argentina

### Checklist para revisar una póliza

### Estado del protocolo familiar

Marcá lo que la familia ya tiene. El avance se guarda en este navegador.

### Órganos de gobierno y reglas que funcionan

### Darle fuerza legal en Argentina

### Planificar sí, ocultar no

### Intercambio de información: qué ve ARCA

### Prevención de lavado: cómo trabaja BHI

### Señales de alerta

### Normas y parámetros que usa esta pestaña

Verificado: texto de la norma o sitio oficial. Fuente secundaria: estudios, consejos profesionales o medios especializados. A confirmar: no se encontró fuente; validar con el contador antes de usarlo con un cliente.

Este material es una herramienta de trabajo del área de Asset Management de BHI. No reemplaza el dictamen del contador ni del abogado: toda estructura se valida con ellos antes de implementarla.

## Cómo se calcula

Todo sale del flujo de fondos de cada bono. No se usan aproximaciones por duration: cada escenario revalúa el flujo completo, así que la convexidad y las amortizaciones ya están incluidas.

### TIR y duration

La TIR es la tasa efectiva anual que iguala el valor presente de los pagos futuros al precio cargado, con base de 365 días. La duration modificada es la duration de Macaulay dividida por (1 + TIR).

### Cambio de TIR de cada bono

Δ TIR = β UST × Δ tasa 10 años EE.UU. + β RP × Δ riesgo país + Δ prima por ley local (solo Bonares) + Δ del escenario predefinido + suba o baja paralela + pendiente × (duration − 3) ÷ 3 + ajuste propio. La TIR de un soberano en dólares es, en esencia, la tasa de EE.UU. más el riesgo país: por eso toma β 1 en ambos. Una ON corporativa suele moverse menos que el riesgo país (β RP entre 0,3 y 0,8 según el emisor), porque su spread depende también del riesgo propio de la empresa y de si tiene ingresos en dólares. La pendiente mueve más a los bonos de duration alta: con +100 pb, un bono de duration 6 sube 100 pb y uno de duration 1,5 baja 50 pb.

### Horizonte de tenencia

Supone que el cambio de TIR ocurre hoy y se mantiene. Al final del horizonte se suman los pagos cobrados (sin reinvertir) y el valor presente de los pagos restantes a la TIR nueva. El colchón de TIR es la suba máxima que deja el retorno en cero.

### Renta fija en pesos

Los supuestos se cargan por tramos (promedio mensual) y se convierten en índices diarios. **Inflación**: arma el nivel de precios que deflacta el retorno real. **CER**: entre el 16 de un mes y el 15 del siguiente crece con la inflación del mes anterior, y cada pago usa el CER de 10 días hábiles antes. **Dólar**: el A3500 crece con la devaluación mensual. **TAMAR**: capitaliza por día la TNA del tramo más el margen del instrumento.

**CER breakeven**: es la inflación mensual constante π que cumple (1 + TIR real)^(días/365) × (1 + π)^(días/30,44) = cobro de la tasa fija al mismo plazo. En los duales CER/TAMAR, el cruce es la inflación a partir de la cual la pata CER iguala a la pata TAMAR con tu trayectoria de TAMAR.

**TAMAR breakeven**: es la TAMAR constante x que cumple (1 + (x + margen)/365)^días = cobro de la tasa fija al mismo plazo. En los duales, el cruce es la TAMAR a partir de la cual la pata TAMAR iguala a la pata CER (con tu inflación) o a la pata dollar linked (con tu dólar).

Cada instrumento se define por su tasa de mercado. Una Lecap cobra (1 + TEM)^(días/30) por cada peso invertido; un CER, (1 + TIR real)^(días/365) por el CER proyectado; un dollar linked, (1 + TIR USD)^(días/365) por el dólar proyectado; un TAMAR, la TAMAR capitalizada más su margen. Los duales toman la pata que más paga desde hoy, lo que es una aproximación: el dual real compara ambas patas desde su emisión.

El breakeven es la inflación, la devaluación o la TAMAR constante que iguala el cobro de la curva de tasa fija interpolada al mismo plazo. Para una Lecap se muestra la inflación que descuenta frente a la curva CER. Si vendés antes del vencimiento, el precio de salida se calcula manteniendo la tasa de mercado de cada instrumento más el Δ elegido.

### Dólar cable

Divide el precio MEP por (1 + canje). Los flujos no cambian, así que la TIR en cable es más alta.

Herramienta de análisis. Los resultados dependen de los precios y flujos cargados; los precios reales difieren por intereses corridos, liquidez y plazos de liquidación. No constituye una oferta ni una recomendación de compra o venta de valores negociables.

BHI Consultora Regional S.A., 12 de Octubre 53, pisos 6 y 7, Bahía Blanca. Herramienta de análisis de sensibilidad. Los escenarios son hipotéticos y dependen de los datos cargados. No constituye una oferta ni una recomendación de compra o venta de valores negociables. Rendimientos pasados no garantizan rendimientos futuros.