---
layout: page
title: Image Encryption and Decryption
description:
img: assets/img/image-encrypt-decrypt-1.jpeg
importance: 5
category: Fun
---

<b>* Introduction:</b>

In the past few years, several encryption algorithms based on chaotic systems have been proposed as means to protect digital images against cryptographic attacks. These encryption algorithms typically use relatively small key spaces and thus offer limited security.

Traditional image encryption algorithms such as private key encryption standards (DES and AES), public key standards such as Rivest Shamir Adleman (RSA), and the family of elliptic-curve-based encryption (ECC), as well as the international data encryption algorithm (IDEA), may not be the most desirable candidates for image encryption, especially for fast and real-time communication applications.

<b>* Encryption:</b>

Let 𝐼𝑜 represent an 𝛼 -bit gray scale image of the size 𝑀×𝑁 . Here, 𝖨𝑜 represent the pixels values matrix of the image. The steps of encryption algorithm are as follows:

1. Generate randomly two vectors 𝐾𝑅 and 𝐾𝐶 of length 𝑀 and 𝑁 , respectively. Element 𝐾𝑅 (𝑖) and 𝐾𝐶 (𝑗) each take a random value of the set 𝒜={0,1,2,…,2 𝛼 −1} .
2. Determine the number of iterations, ITER max , and initialize the counter ITER at 0.
3. Increment the counter by one: ITER=ITER+1 .
4. For each row 𝑖 of image 𝐼 𝑜,
(i) compute the sum of all elements in the row 𝑖
(ii) compute modulo 2 of 𝛼(𝑖) , denoted by 𝑀𝛼(𝑖)      
{iii} row 𝑖 is left, or right, circular-shifted by 𝐾𝑅 (𝑖) positions.                                      
5. For each column 𝑗 of image apply the same but using 𝐾𝐶 (𝑗).
6. Using vector 𝐾𝐶 (𝑗) , the bitwise XOR operator is applied to each row of scrambled image. Same is applied to 𝐾𝑅 (𝑖)  on each columns.
7. If ITER=ITER max , then encrypted image is created and encryption process is done.

<b>* Decryption:</b>

The decrypted image, is recovered from the encrypted image and the secret keys, 𝐾𝑅 , 𝐾𝐶 , and ITERmax as follows in the following,

1. Initialize ITER=0.
2. Increment the counter by one: ITER=ITER+1.
3. The bitwise XOR operation is applied on vector 𝐾𝑅  and each column of the encrypted image.
4. Then by using the 𝐾𝐶 vector, the bitwise XOR operator is applied to each row of image.
5. For each column 𝑗 of the scrambled image,
(i) compute the sum of all elements in that column 𝑗
(ii) compute modulo 2 of 𝛽SCR (𝑗) , denoted by 𝑀𝛽SCR (𝑗)
(iii) column 𝑗 is down, or up, circular-shifted by 𝐾𝐶(𝑖) positions according to the value of 𝑀𝛽SCR (𝑗). 
6. For each row 𝑖 of scrambled image the above procedure is repeated.
7. If ITER=ITER max , then image 𝐼s decrypted and the decryption process is done,otherwise, the algorithm branches back to step 2.

<b>* Analysis</b>

1. A secure image encryption scheme must have a large key space in order to make brute-force attack practically (computationally) infeasible.
2. The encryption key used in our scheme is composed of the (𝐾r ,𝐾c ,ITER max ) triplet.
3. For an 𝛼 -bit gray-scale image 𝐼𝑜 of size 𝑀×𝑁 pixels, the vectors 𝐾r and 𝐾c can take 2 𝑀⋅𝛼 and 2 𝑁⋅𝛼 possible values, respectively.
4. For instance, for an 8-bits, scale gray image of size 256×256 pixels and ITER max =1 . The key space size is equal to 24096 −216 ≈101233 , this key space is large enough to resist the attack.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image-encrypt-decrypt-1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image-encrypt-decrypt-2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images are taken from the internet.
</div>

Codebase: <a href="https://github.com/hoplite2k/image-encryption-decryption">https://github.com/hoplite2k/image-encryption-decryption</a>
