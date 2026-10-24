# Evaluacion2 - Rutas con Graphhopper en español

## Descripción
Programa en Python que consulta la API REST de Graphhopper para convertir nombres de lugares en coordenadas (geocodificación) y calcular rutas entre un origen y un destino.

Toda la interacción con el usuario (solicitudes y respuestas) está en español. Los valores numéricos (distancia y tiempo) se muestran con un máximo de dos decimales, y el programa imprime la narrativa del viaje paso a paso en español.

Proyecto desarrollado para la Evaluación Experiencia 2 del curso CUY6142 (Telepresencia y Entornos Innovadores de Colaboración Humana).

## Requisitos
- Python 3
- Librería `requests`
- Una clave API gratuita de Graphhopper (https://www.graphhopper.com/)

## Cómo ejecutar el script
1. Clonar el repositorio y entrar a la carpeta:
   ```bash
   git clone https://github.com/manmardones/Evaluacion2.git
   cd Evaluacion2
   ```
2. Instalar la librería necesaria:
   ```bash
   pip3 install requests
   ```
3. Definir la clave API como variable de entorno:
   ```bash
   export GRAPHHOPPER_KEY="su_clave_api"
   ```
   Si no se define la variable, el programa pedirá la clave al iniciar.
4. Ejecutar el programa:
   ```bash
   python3 graphhopper_es.py
   ```
5. Ingresar los datos que solicita el programa:
   - Perfil de vehículo: `auto`, `bicicleta` o `a pie`
   - Ubicación de origen, por ejemplo: `Santiago, Chile`
   - Destino, por ejemplo: `Valparaiso, Chile`

Conviene escribir siempre la ciudad y el país, para evitar que la API elija un lugar homónimo de otro país.

## Cómo salir
En cualquier momento, ingrese `s` o `salir` para terminar el programa.

## Ejemplo de salida
- Distancia recorrida en millas y kilómetros (máximo dos decimales)
- Duración del viaje en formato HH:MM:SS
- Instrucciones del recorrido paso a paso, en español