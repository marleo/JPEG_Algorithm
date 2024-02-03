# JPEG Image Compression and Decompression

## Introduction
This project implements a basic JPEG image compression and decompression algorithm in Python. 
It demonstrates converting an image to the YCbCr color space, downsampling the chrominance channels, applying the Discrete Cosine Transform, quantizing the DCT coefficients, and finally encoding the data using Huffman coding. 
The decoder reverses these steps to reconstruct the image.

## Features
- Color space conversion from RGB to YCbCr.
- Chroma channel downsampling.
- Block-wise DCT and inverse DCT.
- Quantization and dequantization with customizable quality factors (QP).
- Huffman encoding and decoding (Entropy Coding).
- PSNR calculation to evaluate compression quality.

## Requirements
- Python 3.x
- NumPy
- cv2
- Pillow 
- SciPy
- Scikit-Image (for PSNR and SSIM calculations)
- DA Huffman (for Huffman encoding and decoding)

## How to Use
Place an image called 'test.png' into the assets folder
Execute all cells in 'Encoder.ipynb'
Execute all cells in 'Decoder.ipynb'

After Compressing, a new file test.bin should appear in /output
After Decompressing, a new file rec.png should appear in /output

## How to modify the compression quality
In the 'Encoder.ipynb' you can Change the values of QP (affects the influence of the Quantization Matrix), as well as the downsampling_factor (affects the Chroma channel downsampling)
