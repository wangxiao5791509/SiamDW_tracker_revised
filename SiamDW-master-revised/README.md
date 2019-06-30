# Deeper and Wider Siamese Networks for Real-Time Visual Tracking

The original project can be found at: https://github.com/researchmm/SiamDW. 
The corresponding paper can be found at: https://arxiv.org/pdf/1901.01660.pdf 

I tried to run the code of SiamRPN on OTB2013 dataset, but met some issues. I modified their code and now it can run on the OTB-2013 successfully. 

############# The following operations are needed before you run the code: 

1. cd the main folder and mkdir a new folder: "snapshot". And download pre-trained models from: https://drive.google.com/drive/folders/19dBWxOqZnvM0FsgXGzH2Y7Bg7wgYMEoO?usp=sharing.  

2. mkdir a new folder: "dataset" and download the [OTB2013](https://drive.google.com/file/d/1ZV6m2cN_TnM8XKR0q3ElYEz0P23iy2qn/view)/[OTB2015](https://drive.google.com/file/d/1eIq7pCz_ik2toO1l9Npk1WXk4mZPK9_N/view) json files. Put these two files and dataset (OTB2013 or OTB2015) into the "dataset" folder. 

3. install the needed environment by: sh install_rpn.sh 

4. run the test code by: 

$ python test_siamrpn.py 
load pretrained model from ../snapshot/CIResNet22.pth
remove prefix 'module.'
missing keys:set(['connect_model.adjust.weight', 'connect_model.search_reg.bias', 'connect_model.search_cls.bias', 'connect_model.search_reg.weight', 'connect_model.template_reg.weight', 'connect_model.template_reg.bias', 'connect_model.search_cls.weight', 'connect_model.template_cls.bias', 'connect_model.template_cls.weight', 'connect_model.adjust.bias'])
unused checkpoint keys:set([u'connect_model.loc_adjust.weight', u'connect_model.loc_adjust.bias'])
Video: basketball   Time: 11.0s Speed: 66.1fps Lost: 0
Video: matrix       Time: 1.2s Speed: 82.1fps Lost: 0
......

