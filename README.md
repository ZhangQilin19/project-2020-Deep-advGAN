### Preparation
* **Attacked model:** Mobilenet_v2 ([Link](http://s0pytorch0org.icopy.site/hub/pytorch_vision_mobilenet_v2/))
* **Dataset:** [Download](https://onedrive.live.com/?authkey=%21AI8PYpczYU9HSN0&id=81DD74CEC613B8E4%21363509&cid=81DD74CEC613B8E4))
* **References:** ([Link](https://arxiv.org/pdf/1801.02610.pdf))
* **Pytorch** ([Instructions](https://pytorch.org/get-started/locally/))
* **NumPy** ([Instructions](https://scipy.org/install.html))
* **Matplotlib** ([Instructions](https://matplotlib.org/))

### Details
1）Change the input size: According to the different input data sets, change the input size to the appropriate 160*160, which is more suitable for the existing data set.

2）Adjust the data set: In order to improve the effect, the training data set used a mixed data set, and the original model training and test sets are used together.(white box attack)

3）Increase the number of layers: encoder of the generator increased 2 layers, decoder increased 2 layers, and discriminator increased 2 layers.

4）Add limit disturbance: In order to limit the disturbance more and make the disturbance effect close to invisible, through multiple experiments, in the environment of GTX1080Ti, when epoch=1000, learning rate=0.0001, add disturbance to each pixel of the picture during training limited to (-0.03,0.03).