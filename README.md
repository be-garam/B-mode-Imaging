# B-mode-Imaging
Code for B-mode imaging base on Ultrasound image

## File Tree
```
├── data
│   ├── personal
│   ├── phantom
│   └── parameters.json
└── b-mode-imaging.ipynb
```

## Data
- Ultrasound image data is in `data` folder
    - `personal`: my neck data
    - `phantom`: reference data
    - `final`: final data
    - `parameters.json`: metadata of image

## Task
- This is base on `Medical Image Processing` Homework1 in PNU University  

    ![alt tag](/resource/Screenshot%20from%202024-04-02%2012-59-08.png)

### B-mode Imaging
- Brightness-mode: 반사파의 강도를 위도로 변환한 밝기 표시법
- 회색도: 반사 강도의 분포를 휘도값 분포로 변환하여 주사선상의 격자에 표시되어 나타나는데, 이때의 분포의 범위를 의미
    - 반사파 강도가 강한 것은 희색으로, 반사파 강도가 약한 것은 점차 검은 색으로 나타나 반사파 강도에 따라 회색 범위를 갖는다.
    - 영상의 pixel이 가질 수 있는 휘도값의 범위로써 8bit(256) 이상이 되어야 한다. 

## Function
- Given Data(input): `arm_img.mat` / 2176px * 128px * 100 frames
- Final Image(= Region of Interest, output): 400px * 400px (dynamic range: 50dB)
### DAS
- Input: 2176px * 128px -> Output: 1580px * 128px
### Envelope Detection(Hilbert Transform)
- Input size == Output size
### Log Compression
- Input size == Output size
### Scan Conversion
- Input: 1580px * 128px -> Output: 400px(4cm) * 400px(3.84cm)

## Refer
- [python: B-mode-Ultrasound](https://github.com/kyledecker/B-mode-Ultrasound)
- [python: skin-segmentation](https://github.com/fqjin/skin-segmentation)
- [python: Ultrasound-B-Mode-Imaging](https://github.com/ItsMoss/Ultrasound-B-Mode-Imaging)
- [python: us_rf_processing](https://github.com/kelu124/us_rf_processing)
