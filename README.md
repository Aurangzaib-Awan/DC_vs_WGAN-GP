# Summary 
I did a comparison between DC-Gan and WGAN-GP. Both are the types of gan(generative adversarial network)

## DC-Gan
Deep convolution gan , it has main two networks ; 
- Generator : Use to make image and fool discriminator
- Discriminator : Use to detect images made from generator or real kind of like a deepfake detector

### Architecture of DC-Gan
- generator arch
  <img width="6528" height="197" alt="dcgan_gen_img" src="https://github.com/user-attachments/assets/4d610571-6567-4107-90a8-734eddbbce59" />
  <img width="1000" height="182" alt="image" src="https://github.com/user-attachments/assets/72a049c1-f623-4d9b-b578-b67ed286cbcd" />

- discriminator arch
  <img width="6195" height="197" alt="dcgan_disc_img" src="https://github.com/user-attachments/assets/245ecb07-069c-4419-9144-1089ddaf69f6" />


## WGAN-GP
Wassertian loss is used here and we also use gradient penalty inorder to make , it has main two networks ; 
- Generator : Use to make image and fool discriminator
- Discriminator : Use to detect images made from generator or real kind of like a deepfake detector

### Architecture of WGAN-GP
- generator arch (it remains same)
  <img width="6528" height="197" alt="dcgan_gen_img" src="https://github.com/user-attachments/assets/4d610571-6567-4107-90a8-734eddbbce59" />
- critic arch
  <img width="4728" height="197" alt="critic_wgan" src="https://github.com/user-attachments/assets/7185a05d-67e3-4bc2-b8fb-c9fe08f9e936" />


  

