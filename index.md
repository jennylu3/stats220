## *hello!*
```r
library(magick)
# square one
bear <-image_read("https://p1-tt.byteimg.com/origin/pgc-image/94f8841639a246e8a293b2b1ad9543f6") %>%
  image_scale(350) %>%
  image_annotate(text = "The little brown bear!") 

# square two
stats_text <- image_blank(width = 350, 
                          height = 350, 
                          color = "#000000") %>%
  image_annotate(text = "cut bear",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")
                
              
# using the approach we used above

bear2 <-c(bear, stats_text )
meme<- image_append(bear2)
c(meme) %>%
  image_append(stack = TRUE) %>%
  image_scale(800)
image_write(meme, "my_meme.png")
```
#### **information about the meme**
I found a picture of a bear on the Internet. I reduced the size of the picture and added text to it. I added a black rectangle the same size as the reduced image and wrote the name of the image in white. Finally, I spliced the picture with the black rectangle and output the final picture.

