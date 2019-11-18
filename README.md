# MelanomaDetection
Melanoma Detection from Clinical Images rather than dermascopic images, built with transfer learning in pytorch.

The data has been collected from the following sources:
http://www.cs.rug.nl/~imaging/databases/melanoma_naevi/
https://www.isic-archive.com/#!/topWithHeader/onlyHeaderTop/gallery
https://www.skinvision.com/skin-cancer/pictures

The size of the data is small and data similarity is very low when compared to the ImageNet dataset the resnet18 model was originally trained on. So we finetune the top layers by freezing the initial  k (6) layers of the pretrained model and training just the remaining(n-k) layers again. The top layers would now be customized to the new data set. 

