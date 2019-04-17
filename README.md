# AstroStacker
This application is used for pre-processing astronomical images. For now,
here's what's working and what will be added:
##### Working
- Average stacking of image sets
- Calibrating lights with darks and bias frames
- Star alignment using triangle similarity
- Setting threshold of star detection

##### To-Do
- ECC and center-of-gravity alignment (first one is good for solar/lunar
  surfaces, second one is good for planetary images)
- Reading RAW DSLR images
- Writing to various formats, like FITS, TIFF
- More stacking methods (median, average, maximum, minimum)
- Pixel rejection algorithms for stacking
- Flat calibration

### Installation
1. Clone this git repository: `git clone https://github.com/PawelPleskaczynski/AstroStacker.git`
2. Install packages with PIP:
 - `pip install PyQt5`
 - `pip install numpy`
 - `pip install opencv-python`
 - `pip install scikit-image`
 - `pip install imutils`
 - `pip install astropy`
 - Note: you might want to install these dependencies with `--user` option.
 - Note: don't install PyQt5 if you have Qt already installed. If you're using
 Arch Linux or its derivative, install OpenCV this way:
    - `pacman -S opencv opencv-samples hdf5`

### How to use
1. Launch the application with `python gui.py`
2. Load needed frames (you need to provide light frames, dark, and bias
  frames are optional)
3. Test number of detected stars (more stars = slower, but more
  precise alignment)
4. Click "Stack" button to process the images
5. Final image will be saved in directory with light frames
