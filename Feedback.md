    "cell_type": "markdown",
    "source": [
      "4a) Subspace of All 16$\\times$16-Pixel Images\n",
      "\n",
      "The subspace consists of all 16$\\times$16-pixel images embedded within the 32$\\times$32 space. To embed a 16$\\times$16 image, it can be thought of as being placed within a 32$\\times$32 frame, with the remaining pixels set to zero (or padded appropriately).\n",
      "\n",
      "Justification of Subspace:\n",
      "\n",
      "This subspace is a proper subspace of the 32$\\times$32 image space because it is closed under addition and scalar multiplication. Any linear combination of 16$\\times$16 images remains within the space of 16$\\times$16 embedded images.\n",
      "\n",
      "Orthogonal Complement:\n",
      "\n",
      "The orthogonal complement consists of all 32$\\times$32 images whose energy (non-zero values) lies outside the central 16$\\times$16 region. In other words, it includes all images where the pixel values in the 16$\\times$16 region are orthogonal (zero contribution) to the embedded images.\n",
      "\n",
      "Mathematically, you can think of this complement as images that are zero within the 16$\\times$16 block and may have non-zero values in the outer regions of the 32$\\times$32 grid."
    ],
    "metadata": {
      "id": "JNjxXF2tD9Cm"
    }
  },
  {
    "cell_type": "markdown",
    "source": [
      "4b) Subspace of Low-Pass Filtered Images by a Rectangular LPF with Passband Frequency 5\n",
      "\n",
      "This subspace consists of images filtered by a low-pass filter (LPF) that passes only frequency components with a magnitude less than or equal to 5 in the frequency domain.\n",
      "\n",
      "Justification of Subspace:\n",
      "\n",
      "Low-pass filtered images form a subspace because filtering is a linear operation: the sum of two low-pass filtered images is still low-pass, and scaling a low-pass image results in another low-pass image.\n",
      "\n",
      "The LPF restricts high-frequency components, ensuring that only smooth, low-frequency variations remain in the image.\n",
      "\n",
      "Orthogonal Complement:\n",
      "\n",
      "The orthogonal complement of this subspace consists of high-pass components, i.e., images containing only frequency components above the cutoff frequency of 5.\n",
      "\n",
      "Mathematically, this complement can be visualized as images whose DFT coefficients are non-zero only for frequencies outside the passband region defined by the LPF. These images primarily contain sharp features, edges, or fine details absent in the low-pass subspace."
    ],
    "metadata": {
      "id": "pUALjYS3EK6B"
    }
  }
]
