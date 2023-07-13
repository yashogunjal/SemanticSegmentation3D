# SemanticSegmentation3D
Semantic Segmentation of 3D brain images of mitochondria in hippocampal region using 3D-Unet model.
The initial Model was a Vanilla 3D-UNet model, which was later improved.
Drawing inspiration from Google's Resnet model where they apply different convolutions on the same layer and then concatenate the output, I changed my model architecture to incorporate the idea, but instead of using multiple sizes of convolution blocks I used multiple pipelines. Now instead of my blocks going from (32x32x32)->(64x64x64)->(128x128x128) and then to the bottleneck layer of UNet, I have two parallel pipelines going from (32x32x32)->(64x64x64)->(128x128x128) and (16x16x16)->(32x32x32)->(64x64x64)->(128x128x128) after which I concatenate their results and pass them through the bottleneck layer of the UNet architecture
Project Report: https://tinyurl.com/3dsegmentation
