How google photos recommeends us to remove some duplicate photos from storage

Let's play this game with opencv

-> Use cv2.absdiff() function compute the difference change
and remove the duplicate if it passes a certain threshold
(basic1.py)

-> efficient approach: get structural similarity index for comparing
(basic2.py)

Above methods won't work in case of alignment of same pictures 


-> More efficient : (main.py)
using hashing: https://www.pyimagesearch.com/2017/11/27/image-hashing-opencv-python/
hashing is based on hamming distance(number of difference bits in 2 numbers)
Generally hamming disctance > 10 implies images are different
compute hash value of an image 
delete images with same hash value
(main.py)

https://www.pyimagesearch.com/2020/04/20/detect-and-remove-duplicate-images-from-a-dataset-for-deep-learning/

To detect duplicate run this command:
python main.py --dataset dataset

To detect duplicate and remove them from dataset:
python main.py --dataset dataset --remove 1
