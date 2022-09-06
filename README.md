# Finetuning-mT5-and-DistillGPT2-for-paraphrasing-tasks
Este repositorio es parte de mi trabajo de fin de master. Se creo un dataset de entrenamiento para tareas de parafrassis que combina los conocidos datasets de parafrasis de dataset de TaPaCO y PAWS.
Ademas se muestra como se llevó a cabo el finetuning sobre dos modelos transformers(mT5 y DistilGPT2) para la realizacion de tareas de parafraseo.

La base de datos custom creada se encuentra bajo el nombre dataset_comb.csv, en la carpeta Dataset comb(TaPaCo +PAWS) y es de libre acceso.
En el Notebook Databases combination + finetuning DistilGPT2 .ipynb, esta disponible el codigo para la generacion de la base de datos custom, asi como el codigo para realizar finetunign sobre DistilGPT2 con la api de entrenamiento de la libreria de transformers de hugging face.
En el Notebook Finetuning mT5.ipynb se muestra el codigo para realizar finetuning a un modelo mT5 con la libreria simple transformers.

# Modelos usados 
mT5 es una variación del modelo original de Google T5 que fue pre-entrenado con un corpus de datos gigante en muchos idiomas. Es un modelo multilingue con 
arquitectura encoder-decoder. 
DistillGPT2 es un modelo inspirado en GPT2 que ha sufrido una destilación de parámetros, es decir, se ha reducido el número de parámetros y se ha compactado el modelo. Este modelo
es un modelo decoder-only basado en la arquitectura de los modelos generativos GPT, y es el más ligero de su familia.

# Hiperparametros utilizados para el finetuning 
A continuacion se muestran los valores elegidos para el numero de epocas, batch size, warm up datio y learning rate.
Para ver el resto de hiperparametros se debera comprobar en cada notebook respecivo
## mT5
• Se uso early stopping con un máximo de 5 épocas

• El tamaño del batch fue de 8

• El warm up ratio se estableció en 0.6

• Se usó una tasa de aprendizaje de 1e-4


## DistilGPT2
• La tasa de aprendizaje se ajustó en 1e-5

• Se entreno durante 5 épocas

• Se uso un warm up ratio de 0.6

• El tamaño del batch se estableció en 8



