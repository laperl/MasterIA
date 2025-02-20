# Predicción de color LAB para máquinas industriales

Este proyecto desarrolla un sistema de **predicción del color LAB** en procesos de impresión industrial sobre plástico. Su principal objetivo es **anticipar desviaciones de color** y optimizar el control del proceso, reduciendo el desperdicio de material y mejorando la eficiencia productiva.

## Descripción General

1. **Contexto Industrial**  
   - Impresión sobre plástico con requerimientos de color estrictos (espacio de color CIELAB).
   - Necesidad de predecir el color final para reducir mermas y tiempos de parada.
   - Arquitectura de maquinaria y mediciones basadas en cámaras industriales.

2. **Objetivos**  
   - **Desarrollar modelos predictivos** (LSTM, GRU, Transformers) que anticipen valores LAB.
   - Analizar la **viabilidad** de integrar estos modelos en la producción real.
   - **Comparar enfoques** de redes neuronales recurrentes (RNN) y basadas en atención (Transformers).

3. **Estrategia de Datos**  
   - **Datos Sintéticos**: Se generaron para simular condiciones de operación y validar prototipos.  
   - **Procesamiento y Transformación**: Se aplicaron transformaciones (log, escalado, codificación one-hot) para mejorar la calidad de los datos.
   - **Entrenamiento**: Se dividió en 80% (train), 10% (validación) y 10% (test), manteniendo el orden temporal.

4. **Modelos Principales**  
   - **RNN / LSTM / GRU**: Capturan dependencias secuenciales.  
   - **Transformers**: Excelente manejo de dependencias a largo plazo, pero demandan muchos datos y potencia de cómputo.  
   - Métricas: MSE (Error Cuadrático Medio) y MAE (Error Absoluto Medio).

5. **Resultados y Conclusiones**  
   - Los modelos actuales aún no están listos para producción: requieren un **mayor volumen de datos reales**.  
   - La precisión del color podría **mejorar** con variables adicionales (p. ej., humedad, temperatura) y un set de datos menos sintético.  
   - Es esencial explorar enfoques híbridos y refinar tanto la **simulación** (para prototipar) como la **recolección de datos reales**.
