# opencv-face-recognition

การใช้ face recognition

1.ดาวโหลด openface.nn4.small2.v1.t7 ที่ http://gitlab.ubocare.com/jiajunjie/face_detect/blob/5891825ac2f2acd8ad8ac31093f1048f4197f722/models/face_detector/openface.nn4.small2.v1.t7
เอาไปในโฟลเดอร์ opencv-face-recognition

2.เอารูปลงในโฟลเดอร์ datasetก่อน

3.เปิดไฟล์ extract_embeddings.py แล้วrun command line ด้วย python extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7(ถ้าเปิดไฟล์ขึ้นมา จะมี command ที่ใช้รันอยู่ที่บรรทัดที่2ครับ)

4.เปิดไฟล์ train_model.py แล้วรันด้วย python train_model.py --embeddings output/embeddings.pickle --recognizer output/recognizer.pickle --le output/le.pickle
(ถ้าเปิดไฟล์ขึ้นมา จะมี command ที่ใช้รันอยู่ที่บรรทัดที่2เช่นกันครับ)

5.เปิดrecognize_video.py แล้วรันด้วย python recognize_video.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle


