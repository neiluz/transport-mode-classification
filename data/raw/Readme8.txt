Project 8. Predicción del modo de transporte mediante registro de dispositivos
móviles usando SVM
Propuesto por Esteve Codina
Se dispone de conjuntos de datos en los que se registran las señales de diferentes sensores en
un dispositivo móvil, tales como acelerómetro, giróscopo, posición GPS, barómetro,
magnetómetro etc. Mediante esta información se pretende inferir usando SVM, el dispositivo de transporte
usado durante la grabación de estos datos en formato .csv

En concreto los datos consisten en:
- Instante de tiempo
- Coordenadas del vector aceleración: X, Y, Z
- Coordenadas X, Y, Z del vector orientación angular 
         y coordenadas X, Y, Z de su vector derivada
- Matriz de rotación + quaternion de rotación
- Ubicación: longitud, latitud, velocidad, rumbo, altitud
- tipo de dispositivo de transporte y confianza
- Barómetro: presión, altitud relativa
- Coordenadas X, Y, Z del campo magnético terrestre
- Modo de transporte usado

Si es necesario tomad un subconjunto de todos los datos (selección al azar). Usando este subconjunto, 
efectuar una estimación del error de predicción del modelo desarrollado usando Cross-validation.