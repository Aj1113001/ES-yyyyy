## Lab 8-1 零基礎Python快速入門與實作, 1/2, W13
````c
Python 3.7.12
                                  2021

      January                   February                   March
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
             1  2  3       1  2  3  4  5  6  7       1  2  3  4  5  6  7
 4  5  6  7  8  9 10       8  9 10 11 12 13 14       8  9 10 11 12 13 14
11 12 13 14 15 16 17      15 16 17 18 19 20 21      15 16 17 18 19 20 21
18 19 20 21 22 23 24      22 23 24 25 26 27 28      22 23 24 25 26 27 28
25 26 27 28 29 30 31                                29 30 31

       April                      May                       June
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
          1  2  3  4                      1  2          1  2  3  4  5  6
 5  6  7  8  9 10 11       3  4  5  6  7  8  9       7  8  9 10 11 12 13
12 13 14 15 16 17 18      10 11 12 13 14 15 16      14 15 16 17 18 19 20
19 20 21 22 23 24 25      17 18 19 20 21 22 23      21 22 23 24 25 26 27
26 27 28 29 30            24 25 26 27 28 29 30      28 29 30
                          31

        July                     August                  September
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
          1  2  3  4                         1             1  2  3  4  5
 5  6  7  8  9 10 11       2  3  4  5  6  7  8       6  7  8  9 10 11 12
12 13 14 15 16 17 18       9 10 11 12 13 14 15      13 14 15 16 17 18 19
19 20 21 22 23 24 25      16 17 18 19 20 21 22      20 21 22 23 24 25 26
26 27 28 29 30 31         23 24 25 26 27 28 29      27 28 29 30
                          30 31

      October                   November                  December
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
             1  2  3       1  2  3  4  5  6  7             1  2  3  4  5
 4  5  6  7  8  9 10       8  9 10 11 12 13 14       6  7  8  9 10 11 12
11 12 13 14 15 16 17      15 16 17 18 19 20 21      13 14 15 16 17 18 19
18 19 20 21 22 23 24      22 23 24 25 26 27 28      20 21 22 23 24 25 26
25 26 27 28 29 30 31      29 30                     27 28 29 30 31

                                  2022

      January                   February                   March
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
                1  2          1  2  3  4  5  6          1  2  3  4  5  6
 3  4  5  6  7  8  9       7  8  9 10 11 12 13       7  8  9 10 11 12 13
10 11 12 13 14 15 16      14 15 16 17 18 19 20      14 15 16 17 18 19 20
17 18 19 20 21 22 23      21 22 23 24 25 26 27      21 22 23 24 25 26 27
24 25 26 27 28 29 30      28                        28 29 30 31
31

       April                      May                       June
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
             1  2  3                         1             1  2  3  4  5
 4  5  6  7  8  9 10       2  3  4  5  6  7  8       6  7  8  9 10 11 12
11 12 13 14 15 16 17       9 10 11 12 13 14 15      13 14 15 16 17 18 19
18 19 20 21 22 23 24      16 17 18 19 20 21 22      20 21 22 23 24 25 26
25 26 27 28 29 30         23 24 25 26 27 28 29      27 28 29 30
                          30 31

        July                     August                  September
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
             1  2  3       1  2  3  4  5  6  7                1  2  3  4
 4  5  6  7  8  9 10       8  9 10 11 12 13 14       5  6  7  8  9 10 11
11 12 13 14 15 16 17      15 16 17 18 19 20 21      12 13 14 15 16 17 18
18 19 20 21 22 23 24      22 23 24 25 26 27 28      19 20 21 22 23 24 25
25 26 27 28 29 30 31      29 30 31                  26 27 28 29 30

      October                   November                  December
Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su      Mo Tu We Th Fr Sa Su
                1  2          1  2  3  4  5  6                1  2  3  4
 3  4  5  6  7  8  9       7  8  9 10 11 12 13       5  6  7  8  9 10 11
10 11 12 13 14 15 16      14 15 16 17 18 19 20      12 13 14 15 16 17 18
17 18 19 20 21 22 23      21 22 23 24 25 26 27      19 20 21 22 23 24 25
24 25 26 27 28 29 30      28 29 30                  26 27 28 29 30 31
31

3.141592653589793
pi=  3.141592653589793
pi= 3.141593
pi= 3.142
pi= 3.14
pi= 3
學AI真是太酷了!!
3 6 9
4
2
6
9
1
1.5
1
0
2 7 14 -1 1024
x=2, y=7, z=14, a=-1, b=1024
3
6
x=x+1, x=? 3
x += 1, x=? 3
x *= 2, x=? 6
<class 'float'>
2.5 3.5 5.0 6.25
x=2, type=? <class 'int'>
y=2.5 type=? <class 'float'>
z=hello, typ=? <class 'str'>
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
請輸入姓名
````
## Lab 8-2 零基礎Python快速入門與實作, 2/2, W14
![image](https://user-images.githubusercontent.com/89329295/142751689-46325346-4306-4b4b-9c5e-546d5d849a9a.png)
````c
### 實作1185
# -*- coding: utf-8 -*-
"""零基礎python快速入門


#使用Google Colab的Python零基礎快速入門教程


Prepared by Horace, Date: October, 2021

* Colaboratory (簡稱為「Colab」) 可讓你在瀏覽器上撰寫及執行 Python. 
* Colab 筆記本的互動式環境，可讓你撰寫和執行程式碼xxx

## 介紹

> Python 本身就是一種出色的通用編程語言，但在一些流行庫（例如: numpy、matplotlib）的幫助下，它成為了一個強大的科學計算環境。我們希望本節將作為Python 編程語言和人工智慧學習中的使用速成課程。

## 在本教程中，我們將介紹：

* Python必學: Basic data types (Containers, Lists, Dictionaries, Sets, Tuples), loops, flow control, Functions, Classes
* 作圖模組 (Matplotlib): Plotting, Subplots, Images
"""

# P1101
ts3 = 'Juncheng Liu' # Please input your English name
!python --version #  Python 版本確認

# P1129
animals = ['cat', 'dog', 'monkey']
for animal in animals:
    print(animal)

# P1130
# [Python] 使用 enumerate() 函式來同時輸出索引與元素
# enumerate() 是 Python 當中經常會看到的函式，前者輸入一個可迭代的對象、比如說 List 資料型態；後者輸入開始的起點編號，為數字，若不設定時從 0 開始。
animals = ['cat', 'dog', 'monkey']
for idx, animal in enumerate(animals):
    print('#%d: %s' % (idx, animal))

# P1131A
for idx, animal in enumerate(animals, start=1):
    print('#%d: %s' % (idx, animal))

for idx, animal in enumerate(animals):
    print('#%d: %s' % (idx+1, animal))

# P1131B
# range語法架構：range(start, stop[, step])

for i in range(1,10,1):
  print(i,'*'*i)

for i in range(1,10):
  print(i,'+'*i)

# P1131C
for i in range(9,0,-1):
  print(i,'*'*i)

# P1131D, Python Nested Loops(巢狀迴圈), 簡單來說，就是迴圈中又有一層迴圈
# 我們來看一個範例: 5X5乘法表
for i in range(1,6,1):
  for j in range(1,6,1):
    print('%dX%d=%2d, ' % (i, j, i*j), end="")
  print('\n')

# P1132A
nums = [0, 1, 2, 3, 4]
squares = []
for x in nums:
    squares.append(x ** 2)
print(nums, '>> ', squares)

# P1132B
nums = [0, 1, 2, 3, 4]
squares = [x ** 2 for x in nums]
print(squares)

# P1132C
nums = [0, 1, 2, 3, 4]
even_squares = [x ** 2 for x in nums if x % 2 == 0]
print(even_squares)

# P1133A, Python While-Loops敘述: Python迴圈的另一種型式，與for-loop不一樣的地方是，while-loop是依據條件來重複執行運算

aa = 0

while aa < 10:
  print('aa=%d, aa+2=%d, aa*2=%d, aa-2=%d' % (aa, aa+2, aa*2, aa-2))
  aa+=1 # a=a+1

print('Done!')


# P1133B, break：直接中斷迴圈(e.g., while loop, for loop)，在break指令之後的運算皆不會執行

aa = 0

while aa < 10:
  if aa>5:
    print('*** %d > 5, so, bye-bye and exit the while loop!' % aa)
    break

  print('aa=%d, aa+2=%d, aa*2=%d, aa-2=%d' % (aa, aa+2, aa*2, aa-2))
  aa+=1

# P1133C, continue：同樣的在continue指令之後的運算不會執行，但是不會中斷迴圈，而是會繼續讀取下一個元素

aa = 0

while aa < 10:
  if aa>5:
    aa+=1 # for increase the number of aa
    continue
    print('*** %d > 5, so, bye-bye and exit the while loop!' % aa)
    
    
  print('aa=%d, aa+2=%d, aa*2=%d, aa-2=%d' % (aa, aa+2, aa*2, aa-2))
  aa+=1

# P1135
d = {'cat': 'cute', 'dog': 'furry', 'fish':'wet'}  # Create a new dictionary with some data
print(d['cat'])       # Get an entry from a dictionary; prints "cute"
print('cat' in d)     # Check if a dictionary has a given key; prints "True"

# P1136
d['fish'] = 'wet'    # Set an entry in a dictionary
print(d['fish'])      # Prints "wet"


# P1137
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal, legs in d.items():
    print('Method 1: A {} has {} legs'.format(animal, legs))
    print('Method 2: A %s has %d legs' % (animal, legs))
    print("\n")

# P1138
animals = {'cat', 'dog', 'fish'}
for idx, animal in enumerate(animals):
    print('#{}: {}'.format(idx + 1, animal))


# P1139
from math import sqrt
print({int(sqrt(x)) for x in range(30)})
print({sqrt(x) for x in range(30)})


# P1140
def sign(x):
    if x > 0:
        return 'positive'
    elif x < 0:
        return 'negative'
    else:
        return 'zero'

for x in [-1, 0, 1]:
    print(sign(x))


# P1141
def hello(name='Horace', loud=False):
    if loud:
        print('HELLO by True, %s' % name.upper())
    else:
        print('Hello by False, %s' % name)

hello()
hello('Bob')
hello('Fred', loud=True)

### 實作1181: 一起來debug!
animals = ['cat', 'dog', 'fish', 'python','']
for xx in animals:
  hello(xx)

# P1142
class Car:

    # Constructor
    def __init__(self, name):
        self.name = name  # Create an instance variable

    # Instance method
    def greet(self, loud=False):
        if loud:
          print('HELLO, {}'.format(self.name.upper()))
        else:
          print('Hello, {}!'.format(self.name))

g = Car('Toyota')  
g.greet()        
g.greet(loud=True)

### 實作1182

"""### 作圖模組：Matplotlib

> Matplotlib 是一個繪圖庫。 本節簡單介紹一下`matplotlib.pyplot`模塊，它提供了一個類似於MATLAB的繪圖系統。

> Matplotlib is a plotting library. In this section give a brief introduction to the `matplotlib.pyplot` module, which provides a plotting system similar to that of MATLAB.
"""

# Commented out IPython magic to ensure Python compatibility.
# P1143
# 加載python模塊 (Load python module)
import numpy as np
import matplotlib.pyplot as plt
from math import pi
# 通過運行這個特殊的%matplotlib iPython命令，我們將可顯示圖形
# %matplotlib inline

"""### 作圖 (Plotting):

> matplotlib 中最重要的函數是 plot，它允許您繪製二維數據。 這是一個簡單的例子：
"""

# P1144
# Compute the x and y coordinates for points on a sine curve
x = np.arange(0, 2 * np.pi, 0.01)
y = np.sin(x)

# Plot the points using matplotlib
plt.plot(x, y)

# P1145
y_sin = np.sin(x)
y_cos = np.cos(x)

# 使用 matplotlib 繪製點
plt.plot(x, y_sin)
plt.plot(x, y_cos)
plt.xlabel('x axis label')
plt.ylabel('y axis label')
plt.title('Sine and Cosine')
plt.legend(['Sine', 'Cosine'])

# P1146
# 計算 x 和 y 坐標
x = np.arange(0, 2 * np.pi, 0.01)
y_sin = np.sin(x)
y_cos = np.cos(x)

plt.subplot(211) # Laytout 2X1, plot #1
plt.plot(x, y_sin, color = 'r') # red
plt.title('sin-red')

plt.subplot(212)
plt.plot(x, y_cos, color = 'g') # green
plt.title('cos-green')

plt.show() # Show圖

# P1147
# 如何用 matplotlib 繪製一個圓？

x1 = y_cos 
x2 = y_sin 

fig, ax = plt.subplots(1)

ax.plot(x1, x2, color = 'r')
ax.set_aspect(1)

plt.xlim(-1.1,1.1)
plt.ylim(-1.1,1.1)

plt.grid(linestyle='--')
plt.title('Plot a circle by Horace', fontsize=10)
plt.savefig("plot_circle_matplotlib_01.png", bbox_inches='tight')

plt.show()

### 實作1185
from math import pi
x = np.arange(0, 2 * np.pi, 0.01)
y_sin = np.sin(x)
y_cos = np.cos(x)

y_sin2 = np.sin(x+pi)
y_cos2 = np.cos(x+pi)

plt.subplots_adjust( left=0.1, right=1.5, top=1.5, bottom=0.1, wspace=0.2, hspace=0.2)

plt.subplot(221)
plt.plot(x, y_sin, color ='r') # red
plt.title('sin_red by Grace')

plt.subplot(222)
plt.plot(x, y_cos, color ='g') # green
plt.title('cos_green by Grac')

plt.subplot(223)
plt.plot(x, y_sin2, color ='y') # yellow
plt.title('sin_yellow by Grace')

plt.subplot(224)
plt.plot(x, y_cos2, color ='b') # blue
plt.title('cos_blue by Grace')

plt.show()

### Final Result
from datetime import datetime
today = datetime.now()
print('*** Done by %s at ' % ts3,today, type(today))
````
## Lab 8-3 建立新的Colab Notebook
![image](https://user-images.githubusercontent.com/89329295/142751719-ff65e800-f710-4de8-bcf4-b57552b12513.png)
````c
# 801
import tensorflow as tf
import tensorflow_hub as hub

import requests
from PIL import Image
from io import BytesIO

import matplotlib.pyplot as plt
import numpy as np

from datetime import datetime
now = datetime.now()
print("now =", now)
today = now
image_size = 224
dynamic_size = False
max_dynamic_size = 512

ts3 = 'Juncheng Liu' # Please input your English name

# 802
original_image_cache = {}

def preprocess_image(image):
  image = np.array(image)
  # reshape into shape [batch_size, height, width, num_channels]
  img_reshaped = tf.reshape(image, [1, image.shape[0], image.shape[1], image.shape[2]])
  # Use `convert_image_dtype` to convert to floats in the [0,1] range.
  image = tf.image.convert_image_dtype(img_reshaped, tf.float32)
  return image

def load_image_from_url(url):
  """Returns an image with shape [1, height, width, num_channels]."""
  user_agent = {'User-agent': 'Colab Sample (https://tensorflow.org)'}
  response = requests.get(img_url, headers=user_agent)
  image = Image.open(BytesIO(response.content))
  image = preprocess_image(image)
  return image

def load_image(image_url, image_size=256, dynamic_size=False, max_dynamic_size=512):
  """Loads and preprocesses images."""
  # Cache image file locally.
  if image_url in original_image_cache:
    img = original_image_cache[image_url]
  elif image_url.startswith('https://'):
    img = load_image_from_url(image_url)
  else:
    fd = tf.io.gfile.GFile(image_url, 'rb')
    img = preprocess_image(Image.open(fd))
  original_image_cache[image_url] = img
  # Load and convert to float32 numpy array, add batch dimension, and normalize to range [0, 1].
  img_raw = img
  if tf.reduce_max(img) > 1.0:
    img = img / 255.
  if len(img.shape) == 3:
    img = tf.stack([img, img, img], axis=-1)
  if not dynamic_size:
    img = tf.image.resize_with_pad(img, image_size, image_size)
  elif img.shape[1] > max_dynamic_size or img.shape[2] > max_dynamic_size:
    img = tf.image.resize_with_pad(img, max_dynamic_size, max_dynamic_size)
  return img, img_raw

def show_image(image, title=''):
  image_size = image.shape[1]
  w = (image_size * 6) // 320
  plt.figure(figsize=(w, w))
  plt.imshow(image[0], aspect='equal')
  plt.axis('off')
  plt.title(title)
  plt.show()

"""## 2. 選擇圖像 
您可以選擇以下圖像之一，或使用您自己的圖像。 請記住，模型的輸入大小各不相同，其中一些使用動態輸入大小（啟用對未縮放圖像的推斷）。 鑑於此，方法 load_image 已經將圖像重新縮放為預期格式。

選項: ['老虎'，'公共汽車'，'汽車'，'貓'，'狗'，'蘋果'，'烏龜'，'火烈鳥'，'鋼琴'，'蜂窩'，'茶壺']

param ['tiger', 'bus', 'car', 'cat', 'dog', 'apple', 'turtle', 'flamingo', 'piano', 'honeycomb', 'teapot']
"""

print('*** Done by %s at ' % ts3,today, type(today))
## Demo: Show tiger

image_name = 'tiger' 

images_for_test_map = {
    "tiger": "https://upload.wikimedia.org/wikipedia/commons/b/b0/Bengal_tiger_%28Panthera_tigris_tigris%29_female_3_crop.jpg",
    "bus": "https://upload.wikimedia.org/wikipedia/commons/6/63/LT_471_%28LTZ_1471%29_Arriva_London_New_Routemaster_%2819522859218%29.jpg",
    "car": "https://upload.wikimedia.org/wikipedia/commons/4/49/2013-2016_Toyota_Corolla_%28ZRE172R%29_SX_sedan_%282018-09-17%29_01.jpg",
    "cat": "https://upload.wikimedia.org/wikipedia/commons/4/4d/Cat_November_2010-1a.jpg",
    "dog": "https://upload.wikimedia.org/wikipedia/commons/archive/a/a9/20090914031557%21Saluki_dog_breed.jpg",
    "apple": "https://upload.wikimedia.org/wikipedia/commons/1/15/Red_Apple.jpg",
    "turtle": "https://upload.wikimedia.org/wikipedia/commons/8/80/Turtle_golfina_escobilla_oaxaca_mexico_claudio_giovenzana_2010.jpg",
    "flamingo": "https://upload.wikimedia.org/wikipedia/commons/b/b8/James_Flamingos_MC.jpg",
    "piano": "https://upload.wikimedia.org/wikipedia/commons/d/da/Steinway_%26_Sons_upright_piano%2C_model_K-132%2C_manufactured_at_Steinway%27s_factory_in_Hamburg%2C_Germany.png",
    "honeycomb": "https://upload.wikimedia.org/wikipedia/commons/f/f7/Honey_comb.jpg",
    "teapot": "https://upload.wikimedia.org/wikipedia/commons/4/44/Black_tea_pot_cropped.jpg",
}

img_url = images_for_test_map[image_name]
image, original_image = load_image(img_url, image_size, dynamic_size, max_dynamic_size)
show_image(image, 'Scaled image')

print('*** Done by %s at ' % ts3,today, type(today))
# 實作: Show teapot

# 你的程式

print('*** Done by %s at ' % ts3,today, type(today))
# 實作: Show turtle
image_name = "turtle"
img_url = images_for_test_map[image_name]
image, original_image = load_image(img_url, image_size, dynamic_size, max_dynamic_size)
show_image(image, 'Scaled image')

# 你的程式

print('*** Done by %s at ' % ts3,today, type(today))
# 實作: 請由以上的選項自選一個來試試
image_name = "car"
img_url = images_for_test_map[image_name]
image, original_image = load_image(img_url, image_size, dynamic_size, max_dynamic_size)
show_image(image, 'Scaled image')
# 你的程式
````

