## Notes for Sean's folder

File: "Simple-Image-Extraction" will get you a 2d array, with the first dimension as the image, 
second dimension as the label 1 as with mask, 0 as without mask.

File: "Image-Aug" will create a folder called "AUG-Train", which contains augmented data.

Structure:

```AUG-Train
├── Train-Mask
|   ├── mask0_0_1155.jpeg
|   └── mask0_0_2502.jpeg
└── Train-NoMask
    ├── nomask0_0_1155.jpeg
    ├── nomask0_0_2502.jpeg
    ├── nomask0_0_3896.jpeg
```

