---
title: "ZipNet"
excerpt: "Completely standalone web based neural network compression algorithm."
header:
  teaser: /assets/images/zipnet-image.jpg
sidebar:
  - title: "Techniques used"
    image: /assets/images/zipnet-image.jpg
    image_alt: "Generic AI image"
    text: "Rust, Neural Compression, WebASM"
  - text: <a href="https://github.com/Conzel/zipnet"><i class="fab fa-github"></i> GitHub repository</a>
  - text: <a href="https://conzel.github.io/zipnet/"><i class="fa fa-link"></i>Project Website</a>
--- 
ZipNet is a Work-In-Progress for the course project of [Data Compression With Deep Probabilistic Models](https://robamler.github.io/teaching/compress21/) offered by Robert Bamler at the University of Tübingen.

We want to provide a fully functional Neural Image-Encoder and Decoder on the Web. The goal is to achieve a superior compression rate over classical codes (JPEG, …) while retaining acceptable performance for a Web Application (compression in a few seconds). This results in a maximally portable application that could help Neural Compression Codecs achieve a higher adoption rate. For the implementation, we leverage the new, performant WebASM standard along with a simple, flexible, yet powerful model architecture.

You can track our progress in the [linked GitHub repository](https://github.com/Conzel/zipnet) and [on our website](https://conzel.github.io/zipnet/).
