# Camera-Distortion-Corrector
Correct image distortion with openCV
녹화된 비디오를 캘리브레이션하고, 왜곡을 바로잡는 프로그램

녹화된 파일의 경로를 입력하고 실행시키면 녹화된 영상이 재생됩니다.
이때 Space키를 누르면 영상이 일시적으로 중단되고, 체스판의 격자점을 찾아 표시합니다.

![cap1](https://github.com/ajbuwidnnfjwj/Camera-Distortion-Corrector/assets/68640265/e33b7bb5-489c-49eb-a705-2c851af905cb)

엔터키를 누르면 영상이 다시 재생되고, 표시된 격자점이 사라집니다. 일시정지되며 출력된 프레임이 저장되었습니다.
저장된 프레임의 갯수는 좌측 상단에 표시됩니다.

![capture2](https://github.com/ajbuwidnnfjwj/Camera-Distortion-Corrector/assets/68640265/f270369c-27be-4aa8-9e5a-7aeee645cbd9)

영상을 다 재생했거나 ESC키를 눌러 창을 닫으면 콘솔창에 K행렬, 왜곡 계수들과 RMS Error값이 출력됩니다.
예시는 필자의 핸드폰(Iphone 13 Pro) 광각카메라로 녹화한 영상입니다.
RMS Error=0.909832789135831, f=1.25320688e+03, cx=9.57241496e+02, cy=4.99739793e+02
이제 영상의 왜곡을 바로잡을 준비가 완료되었습니다.


![capture3](https://github.com/ajbuwidnnfjwj/Camera-Distortion-Corrector/assets/68640265/1f82c779-886c-4767-8a9c-bd21b06c7f97)

비디오를 캘리브레이션하는 창이 닫히고 콘솔에 결과가 출력됨과 동시에 왜곡을 수정한 영상이 출력되는 창이 띄워집니다.
캘리브레이션의 결과값과 cv.undistort함수를 사용합니다. 

영상이 다 끝나거나 ESC키를 누르면 영상이 종료됩니다.
