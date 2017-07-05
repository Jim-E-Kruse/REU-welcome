Week 5 Updates
================
2017-06-30 12:30:00 CDT

Here's what we've done on our projects so far.

Shoeprints
----------

### James Kruse, Andrew Kimble III, Marion Gray-Lion, and Sam Rew

Project Week 1 (6/23 - 6/30) Update Slides: <https://prezi.com/p/xwjtd0_mxzvg/>

On the 22nd and 23rd of June, we scanned 8 pairs of shoes to be used later in the program. They were labeled and pushed into Git Hub for storage. In addition, we were trained to take shoe prints using dust and contact paper. They will not be extensively used later in the program, but this technique is still relevant and necessary in the field.

Over the past two days, the shoe print team has been working to understand Hu Moments and their use in shoe print analysis. In addition, we have developed a function in R studio that will allow us to take the shoe scans that were taken late last week and crop/grayscale the image for later analysis.

After being given both videos and files to review, we were tasked to put together a presentation that would both explain Hu Moments and their relevance in forensic shoe print analysis. This was then presented to our project leaders. In summary, Hu Moments are a snap shot of an image in time. If you would like to see the full presentation, please contact a member of the our CSAFE REU shoe print team.

On the 27th, we learned the program to code grayscale and crop images using RStudio after the files are downloaded from GitHub. Each of the images from the 8 sets were put through this code and saved. On the 28th, we cleaned up the code mentioned above by condensing it into a function. At this point in time, you can enter in the raw image, run the function, and end with a cropped/gray scale shoe print. Please see the finished code below for specifics.

``` r
    GrayCrop2 <- function(x){
      img <- readImage(x) 
      img <- channel(img, mode = "grey") 
      img_crop=img[160:1800, 200:4400]
      ###display(img_crop, method = "raster")
      img_crop
    }

    GrayCrop2("Jim2_right_1.tiff")

    compute_moments(GrayCrop2("Jim2_right_1.tiff"))

    filenames <- list.files(pattern="tiff")
    filenames[x]
```

After presenting on Hu Moments on the 29th, we continued to develop the code that is present in the attached presentation. Our end product for the day was the breakdown of each file and the cleaning up of the data.

On Friday the 30th, we put together the week summary presentation, listened to a presentation on experiment design, and continued to develop figures using the data we have collected.

The past few days have been both fascinating and challenging. We would like to thank our REU leaders and project leaders for their patience and assistance through it all.

-CSAFE REU Shoe Project Team

Steganography
-------------
