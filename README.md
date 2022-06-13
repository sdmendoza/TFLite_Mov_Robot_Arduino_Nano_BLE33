# TFLite_Mov_Robot_Arduino_Nano_BLE33
Proyecto entregable datos secuenciales, deployment de TFLite en arduino nano ble33

Este repositorio muestra la implementacion de la deteccion de gesto para un robot, usando tensorflow lite cuantizado en un embebido Arduino Nano BLE33. Usando los sensores Inerciales Acelerometro, Giroscopio y Campo magnetico.

En el notebook 'MOVIMIENTO_ROBOT_CON_ARDUINOBLE33' se detalla el procedimiento realizado, se analizan 3 arquitecturas diferentes para realizar la inferencia: Conv1D, Redes Simple RNN y Redes LSTM.

Se obtienen sus respectivos modelos entrenados, se convierten a formato tflite y se cuantizan para su posterior implementacion con el microcontrolador.

En la carpeta 'IMU_Classifier' se encuentran los archivos de prueba correspondientes, se modifica el archivo 'IMU_Classifier.ino' para que recoja las 9 senales del arduino, y se modifica el archivo 'model.h' que se usa para la inferencia del movimiento.

En la carpeta 'movimientos_robot_con_arduinoble33-nan-ble-sense-v7', se encuentra el modelo generado mediante la paltaforma Edge Impulse, con la que se tomaron los datos de entrenamiento y validacion. Dentro de esta, se usa el archivo 'Flash_linux.sh' para sobreescribir el modelo de esta plataforma en el arduino.
