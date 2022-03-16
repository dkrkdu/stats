``` r
library(magick)

frink <- image_read("https://jeroen.github.io/images/frink.png")
print(image_info(frink))


frink %>%
  image_rotate(270) %>%
  image_background("blue", flatten = TRUE) %>%
  image_border("red", "10x10") %>%
  image_annotate("The same thing with pipes", color = "white", size = 30)
  

logo <- image_read("https://jeroen.github.io/images/Rlogo.png")
img = c(frink,logo)
img %>%
  image_scale('200') %>%
  image_append()
```

## For the *first* snippet, try to find its info

### For the **second** snippet, try to modify its the image
- first of all, we rotate image 270 degrees
- then set background to blue 
- after that, adjust the border to red
- finally, add some text 

#### For the ***third*** snippet, try to merge two images
- find a new image
- combine two images
- show two images

[frink]["https://jeroen.github.io/images/frink.png"]

["https://jeroen.github.io/images/Rlogo.png"]



