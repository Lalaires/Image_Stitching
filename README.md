# Image_Stitching

The image stitching pipeline which consisted of self-implemented functions creates panoramas from overlapping images.

### Implementation Steps

1. **Feature detection**: Apply self-implemented Harris corner detector on equalized images
2. **Feature description**: Extract SIFT descriptors at corner locations
3. **Feature matching**: Use FLANN-based matching with ratio test (threshold=0.8)
4. **Robust estimation**: Apply self-implemented RANSAC to find homography between images
5. **Image warping**: Transform second image to align with first
6. **Boundary determination**: Calculate output dimensions using transformed corners
7. **Blending**: Create seamless transitions in overlapping regions
