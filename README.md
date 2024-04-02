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
