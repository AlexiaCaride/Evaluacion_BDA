# Ejercicio: Sistemas RAG con Bases de Datos Vectoriales

## Descripción

El objetivo de este ejercicio es crear un sistema **RAG** (Retriever-Augmented Generation) utilizando **llama3.2** que sea capaz de responder preguntas sobre artículos o archivos PDF relacionados con temas de actualidad. Además, se implementará **Gradio** para interactuar con uno de los sistemas creados.

## Pasos de Ejecución de los Scripts

### Crear el Entorno Virtual con Conda

Crea el entorno virtual utilizando el archivo `rag_env.yml` que contiene todas las dependencias necesarias para el proyecto.

```bash
conda env create --file rag_env.yml
```

### Ejecutar los Scripts

1. Abre **VSCode** y activa **WSL** (Windows Subsystem for Linux) si estás trabajando en un entorno Windows.
2. Selecciona el **kernel "rag"** en cada cuaderno de Jupyter que hayas descargado para trabajar con el entorno adecuado.

### Ejecutar la Versión de Chroma

En el cuaderno de Jupyter, despliega y ejecuta cada bloque de código relacionado con la integración de **Chroma**. Asegúrate de ejecutar los bloques de código en el orden correcto para asegurar que la funcionalidad se ejecute sin errores.

### Ejecutar la Versión de MongoDB Atlas

1. En el cuaderno de Jupyter, despliega el código relacionado con **MongoDB Atlas** y actualiza la URI de conexión con los detalles de tu **cluster** en MongoDB Atlas.

```bash
MONGODB_ATLAS_CLUSTER_URI = "mongodb+srv://usuarioMongoAltas:contrasenha@cluster0.xmaru.mongodb.net/"
```

2. La primera vez que ejecutes el código, se creará el índice necesario en la base de datos, pero no responderá a las preguntas aún. No te preocupes, es parte del proceso inicial.

3. Después de la creación del índice, puedes ejecutar el código tantas veces como desees, haciendo las preguntas que consideres necesarias para obtener respuestas del sistema RAG desde este trozo de código.

```bash
query = "What is the main topic of the webpage?"
response = qa_chain.run(query)
print("Response:", response)
```

