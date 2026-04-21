# Summary 
I did a comparison between DC-Gan and WGAN-GP. Both are the types of gan(generative adversarial network)

## DC-Gan
Deep convolution gan , it has main two networks ; 
- Generator : Use to make image and fool discriminator
- Discriminator : Use to detect images made from generator or real kind of like a deepfake detector

### Architecture of DC-Gan
- generator arch
  <img width="1000" height="182" alt="image" src="https://github.com/user-attachments/assets/72a049c1-f623-4d9b-b578-b67ed286cbcd" />

- discriminator arch
  <img width="1000" height="182" alt="image" src="https://github.com/user-attachments/assets/f3946ff1-4d7e-410b-a249-1f499a87a2c8" />

## WGAN-GP
WGAN replaces the discriminator with Critc , here we used Wassertien loss to compute the difference between two probability distributions and to keep the signal valid not change alot we kept it 1 lipschitz, we ensure this with gradient penalty , during training we sampe interpolated points between real and fake images , take gradeint norm and penalize any deviation from 1 in either direction. 
- Generator : Use to make image and fool Critic
- Critc : gives an ubounded score instead of a probability or a weak signal squashed between 0-1 , We dont use batchnorm here to let the gradient move more freely and no sigmoid in the end to have a better score

### Architecture of WGAN-GP
- generator arch (it remains same as dcgan)
  <img width="1000" height="182" alt="image" src="https://github.com/user-attachments/assets/72a049c1-f623-4d9b-b578-b67ed286cbcd" />
- critic arch
  <img width="1045" height="121" alt="image" src="https://github.com/user-attachments/assets/3f172758-8672-4cba-aff9-55c54ceaa1da" />

## Main difference and why WGAN-GP better ?
here are few argumnets that make wgan-gp more valid choice among them both two :
- The crtic used in wgan-gp sends better signal to generator so it helps the generator to update itself better and hence constructing better images
- We also trained critic here 5 times and 1 time the generator, this helped in stable training as we all know GANs are headache to train, this technique also helped in giving better singal to generator as the loss of 5 samples was accuamlated and then average loss was propagated to the generator

  

