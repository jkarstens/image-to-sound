# image-to-sound

What does an image sound like? This is a Max patch, which will run in [Max](https://cycling74.com/products/max/).

## General conversion process
Every song output has a key, a chord progession, a melody, and a tempo. A bag of emotions are predefined and chosen as labels for a certain chord progression, melody, and tempo. In this patch, the emotions are: happy, spooky, epic, sad, pensive, relaxing, dylan, hopeful, and spacey. Based on an image's average hue, saturation, lightness, and average RGB pixel values, a song is generated.

#### Example definition of emotion
 - Emotion: "happy"
 - Chord progesssion: A minor / F major / C major / G major
 - Possible notes for the melody: C, D, E, G, A
 - Number of harmonics in each note of a chord: 4 
 - Number of harmoincs in each note in melody: 8 
 - Tempo: some moderate value
 - Average image saturation level required to activate: 90-100%
 
 
This ends the subjective, predefined part of the image-to-sound mapping. 

The image uploaded has a certain hue, saturation, and lightness. The key of the song is chosen based on the average hue of the image (the chord changes and melody stay the same relatively, but are modulated based on the key), and the lightness of each pixel determines the melody note (from the predefined choice of melody notes that "go" with the emotion) at a given point in time in the song. The songs plays as a scan from left to right, top to bottom over the image. The average saturation of the image determines the emotion. Saturation levels are defined and mapped to emotions. For the "happy" example, the "happy" emotion is chosen if the image's average saturation level falls in a certain high range. A drum beat to go along with the rest of the song is chosen based on the RGB values of the image, which choose indices in a drum beat picker.

Instructions for use are provided in the Max patch.
Here are some good photos to try (for best results, scale each image to about 300x150 pixels):
 - http://wallpaperclicker.com/storage/Thumb/Nature-Yellow-flower-in-vally-91745800.jpg
 - https://lh3.googleusercontent.com/-EHDwU-MWjw0/Vw_2jcbjIXI/AAAAAAAAAhg/PLilLr3-nxcDwjhbVSJhxgc9_lk2G9i5w/w1920-h1200/wallpaper-203310.jpg
 - https://i3.wallpaperscraft.com/image/mountain_river_grass_trees_87739_3840x2160.jpg
 - http://i.imgur.com/rhkdNh3.jpg
  
