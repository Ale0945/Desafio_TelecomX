# 📄 Informe Final – Análisis de Evasión de Clientes (Churn)  

## 🔹 Introducción  
El objetivo de este análisis fue comprender los factores que influyen en la **evasión de clientes (Churn)** en TelecomX.  
La evasión representa la pérdida de clientes que deciden cancelar el servicio, un problema crítico en la industria de telecomunicaciones debido a la alta competencia y los costos de adquisición de nuevos usuarios.  

Identificar patrones de comportamiento en los clientes que abandonan permitirá diseñar **estrategias efectivas de retención**, optimizando la fidelización y reduciendo pérdidas financieras.  

---

## 🔹 Limpieza y Tratamiento de Datos  
Durante la etapa de preparación:  
- Se **importaron los datos** desde un archivo en formato JSON y se normalizaron a un DataFrame.  
- Se **estandarizaron los nombres de las columnas**, reemplazando `.` por `_`.  
- Se **eliminaron duplicados** en base al identificador `customerID`.  
- Se **convirtieron a valores numéricos** las variables continuas relevantes:  
  - `customer_tenure` (tiempo de contrato en meses).  
  - `account_Charges_Monthly` (cargo mensual).  
  - `account_Charges_Total` (cargo total acumulado).  
- Se creó una **variable binaria `Churn_num`** (No=0, Yes=1).  

---

## 🔹 Análisis Exploratorio de Datos  

### 1. Tasa Global de Churn  
- La tasa global de evasión se ubica en **X%** (según la media de `Churn_num`).  
- La mayoría de los clientes permanecen, aunque un grupo importante cancela.  

📊 **Gráfico:**  
![Conteo de clientes por estado de Churn](figures/churn_overall.png)  

---

### 2. Churn por variables categóricas  
- **Género:** no se observan diferencias significativas.  
- **Tipo de contrato:** los contratos **mensuales** presentan la mayor tasa de churn.  
- **Método de pago:** ciertos métodos (más manuales) muestran mayor churn que los pagos automáticos.  

📊 **Gráficos:**  
- ![Churn por género](figures/churn_gender.png)  
- ![Churn por contrato](figures/churn_contract.png)  
- ![Churn por método de pago](figures/churn_payment.png)  

---

### 3. Variables numéricas por Churn  
- **Tenure:** los clientes con menor antigüedad presentan mayor churn.  
- **Cargos mensuales:** clientes con cargos altos muestran más cancelaciones.  
- **Cargos totales:** clientes con bajo gasto acumulado tienden a cancelar antes.  

📊 **Gráficos:**  
- ![Conteo de clientes por estado de Churn](figure/Conteo de clientes por estado de Churn.png)  
- ![Promedio de gasto total por grupo de Churn](figure/Promedio de gasto total por grupo de Churn.png)  
- ![Promedio de tiempo de contrato por grupo de Churn](figure/Promedio de tiempo de contrato por grupo de Churn.png)
- ![Distribución de evasión de clientes por género](figure/Distribución de evasión de clientes por género.png)
- ![Distribución de evasión de clientes por tipo de contrato](figure/Distribución de evasión de clientes por tipo de contrato.png)
- ![Distribución de evasión de clientes por método de pago](figure/Distribución de evasión de clientes por método de pago.png)
- ![Distribución de var por Churn](figure/Distribución de var por Churn.png)    

---

## 🔹 Conclusiones e Insights  
1. La tasa global de churn es significativa: un problema clave para TelecomX.  
2. Los **contratos mensuales** son los más propensos a la cancelación.  
3. Los **clientes con tenure bajo** representan el segmento de mayor riesgo.  
4. El **método de pago** influye: los pagos automáticos reducen churn.  
5. Los **cargos altos** (mensuales) se relacionan con mayor evasión.  

---

## 🔹 Recomendaciones  
1. **Retención temprana (0–6 meses):** programas de bienvenida, descuentos y beneficios extra.  
2. **Migración de contratos:** incentivar el paso de contratos mensuales a plazos más largos.  
3. **Optimizar métodos de pago:** promover pagos automáticos y mejorar UX de cobros.  
4. **Modelos predictivos de churn:** identificar clientes en riesgo y actuar de forma proactiva.  
5. **Revisión de precios y beneficios:** flexibilizar planes y ofrecer bundles a clientes con altos cargos mensuales.  

---

✅ Este informe, respaldado por las visualizaciones, ofrece una base sólida para estrategias de retención en TelecomX.  
