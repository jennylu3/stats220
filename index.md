## *hello!*
```r
library(magick)
image_blank(width = 500, height = 500,  color = "#000000")
meme <-image_read("https://p1-tt.byteimg.com/origin/pgc-image/94f8841639a246e8a293b2b1ad9543f6")
image_read( path =  "https://p1-tt.byteimg.com/origin/pgc-image/94f8841639a246e8a293b2b1ad9543f6") 
image_read("https://p1-tt.byteimg.com/origin/pgc-image/94f8841639a246e8a293b2b1ad9543f6") %>%
  image_scale(350) %>%
  image_annotate(text = "The little brown bear!")
kern <- matrix(0, ncol = 3, nrow = 3)
kern[1, 2] <- 0.1
kern[2, c(1, 3)] <- 0.1
kern[3, 2] <- 0.1
kern
img_blurred <- image_convolve(meme, kern)
image_append(c(meme, img_blurred))
image_write(meme, "my_meme.png")
```
#### information about the meme

