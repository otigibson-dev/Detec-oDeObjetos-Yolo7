# Detec-oDeObjetos-Yolo7
#Acesse o resultado em vídeo: https://drive.google.com/file/d/1-3uge0tf7shIr4TyrAmVVJSZ8iUMMfwR/view?usp=sharing

from google.colab import drive
drive.mount("/content/gdrive")

# Commented out IPython magic to ensure Python compatibility.
# %cd /content/gdrive/MyDrive/

!pwd

"""# Criar Diretorios e Clonar Repositorio"""

import os

if not os.path.isdir("TheCodingBug"):
  os.makedirs("TheCodingBug")

# Commented out IPython magic to ensure Python compatibility.
# %cd TheCodingBug

!git clone https://github.com/WongKinYiu/yolov7.git

"""# Baixar Modelo Pré-Treinado"""

# Commented out IPython magic to ensure Python compatibility.
# %cd yolov7

!wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolo7.pt

"""# Rodar a Detecção de Video"""

!pwd

!python detect.py --weights yolov7.pt --conf 0.5 --img-size 640 --source Fabrica.mp4
