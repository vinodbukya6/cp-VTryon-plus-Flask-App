# cp-VTryon-plus-Flask-App

Falsk App version of https://github.com/minar09/cp-vton-plus for **custom images**. Thank you so much **minar09** for your Great Work!!!

**Installation**
conda install pytorch=0.4.1 torchvision=0.2.1 -c pytorch
For all packages, run pip install -r requirements.txt

**Testing with custom images**

to run the model with custom internet images, make sure you have the following:

image (image of a person, crop/resize to 192 x 256 (width x height) pixels)
        ''' # ..... Resize/Crop Images 192 x 256 (width x height) ..... # 
        img_p = cv2.imread("data/test/image/"+filename_person)
        person_resize = cv2.resize(img_p, (192, 256))
        # save resized person image
        cv2.imwrite("data/test/image/"+filename_person, person_resize) '''
        
image-parse (you can generate with CIHP_PGN or Graphonomy pretrained networks from the person image. See this comment)
cloth (in-shop cloth image, crop/resize to 192 x 256 (width x height) pixels)
cloth-mask (binary mask of cloth image, you can generate it with simple pillow/opencv function)
pose (pose keypoints of the person, generate with openpose COCO-18 model (OpenPose from the official repository is preferred))
Also, make a test_pairs.txt file for your custom images. Follow the VITON dataset format to keep same arrangements, otherwise you can modify the code.
