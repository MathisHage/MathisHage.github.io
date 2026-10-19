---
title: "Principles of Digital Communication (COM-302): Simple Encoder & Decoder"
title_fr: "Principles of Digital Communication (COM-302) : Encodeur & Décodeur simples"
excerpt: "Implemented and studied the theoretical performance of a simple encoder / decoder. <a href='https://github.com/MathisHage/PDC'>[GitHub]</a>"
excerpt_fr: "Implémentation et étude des performances théoriques d'un encodeur / décodeur simple. <a href='https://github.com/MathisHage/PDC'>[GitHub]</a>"
collection: portfolio
date: 2025-11-01
fr_url: /fr/projects/
redirect_from:
  - /portfolio/pdc/
---

**Course**: Principles of Digital Communication (COM-302), Fall 2025  
**Institution**: EPFL  
**Repository**: [github.com/MathisHage/PDC](https://github.com/MathisHage/PDC)

---

## Choice of Implementation

### Encoder
The idea behind the encoder is the following. We have a sequence of 40 characters out of 64 possible symbols, which are hence treated as $40 \times 6 = 240$ bits of data. The user chooses the number of bits to encode in a single codeword. This number of bits is defined in the code as $r+1$. Then, the codeword for each set of $r+1$ bits is chosen from the rows of $\sqrt{\alpha} [B_r \quad B_r]$ as seen in the theory part: the integer value (unsigned) of these bits serves to choose the row. Each of the chosen rows is then "interleaved" meaning the top half becomes the even components, and the bottom half becomes the odd components, to pass through the channel. Finally, all the codewords are concatenated in a single vector $X$ which is output by the encoder.

### Decoder
To decode the vector $R$ going out of the channel, the decoder implements the decoding rule $\hat{i}_1$ seen in exercise two of the theory part. First, the interleaving operation done in the encoder is undone. Then, a separation is made based on the two possible states that the channel is able to take: $R$ is copied with the factor $\sqrt{G}$ multiplied with the top half components of each codeword (as the interleaving operation was undone), and copied another time with $\sqrt{G}$ multiplied with the bottom half components of each codeword. The scores are then computed via matrix products. Finally, the guess of the integer values made by the decoder are converted to binary (because they were encoded with $r+1$ bits), and then converted back to integer considering sequences of 6 bits. The corresponding symbols are lastly output.

## Results
The most efficient value of $r$ that we used is the value $r = 11$ (which is the default value). In fact, it corresponds to assigning exactly one codeword per two characters (so no redundant padding bits are sent), and the size of $\sqrt{\alpha} [B_r \quad B_r]$ allows for reasonably quick calculations.

## Links
* [Code on GitHub](https://github.com/MathisHage/PDC)
