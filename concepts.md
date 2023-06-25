# Important concepts related to GANs

## Necessary Tip
Try to make the shape of your input data (mostly images) as small as possible. Large image shapes like (224, 224, 3) will cause memory exhaustion even if you're on Colab. 
Preferable image shape is (28, 28, _color_channels_)

## Generator
The generator is a neural network that takes random noise as input and generates synthetic data, such as images, text, or sound. Its purpose is to produce data that closely 
resembles real data samples. Random noise refers to randomly generated data.

## Discriminator
The discriminator is another neural network that learns to distinguish between real and synthetic data. Its objective is to correctly classify the generated data as fake
and the real data as genuine.

## Training
GANs use an adversarial training process where the generator and discriminator are trained in competition with each other. The generator aims to generate data that can fool
the discriminator, while the discriminator strives to accurately differentiate between real and fake data. Through this adversarial process, both networks improve over time.
So, instead of using normal training we need to create custom training loop.

## Loss Functions
GANs utilize specific loss functions to train the generator and discriminator. The generator's loss function encourages it to generate data that the discriminator is likely
to classify as real, while the discriminator's loss function promotes accurate classification of real and fake data.

## Optimizers
The learning rate of discriminator's optimizer should be less than learning rate of generator's optimizer.

### Recommended data for GANs
batch_size = 64
num_channels = 1
num_classes = 10
image_size = 28
latent_dim = 128
