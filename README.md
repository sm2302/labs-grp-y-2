# Group lab exercise

## Instructions

Clone this repository onto your local machines. 
In your groups, make changes as necessary to this **single README.md file** only. 
To be clear, you are allowed to add files to this repo (e.g. images), but the main concentration of effort is this README file.

> Once you are done the group leader is responsible for submitting the final repo.

*Optional: For extra points, prettify your GitHub repo: Add descriptions, about, titles, create a GH page, etc.*

--------------------------------------------------------------------------------

## Group Details

(remove any unnecessary parts)
Each group member should fill in their respective parts.

### Group Member 1

- Name: Ang Woan Yean
- Student ID: 19B2068
- Favourite book: ...
- Favourite number: 8
- Favourite mathematical equation: E=mc^2
- Insert an inspiring photo: ![Coffie Bae](https://user-images.githubusercontent.com/110547502/187019987-790ce9be-1950-42f8-ad37-19e2051844d8.jpeg)

### Group Member 2

- Name: Soon Chin Yuen
- Student ID: 19B2155
- Favourite book: -
- Favourite number: 8
- Favourite mathematical equation: y=mx+c
- Insert an inspiring photo: ![WhatsApp Image 2022-08-27 at 3 27 49 PM](https://user-images.githubusercontent.com/110475079/187020045-4f32de43-22ea-487b-8f6a-fc51c82bf888.jpeg)


## Collaborative Work

(remove unnecessary parts when done)
In the previous exercise you used the R function called `ggsave()`. 
Your task is to copy over the relevant parts from the R help file regarding the `ggsave()` function.
In particular, this section should be populated (only) with 

1. Description 
ggsave() is a convenient function for saving a plot. It defaults to saving the last plot that you displayed, using the size of the current graphics device. It also guesses the type of graphics device from the extension.

2. Usage
ggsave(
  filename,
  plot = last_plot(),
  device = NULL,
  path = NULL,
  scale = 1,
  width = NA,
  height = NA,
  units = c("in", "cm", "mm", "px"),
  dpi = 300,
  limitsize = TRUE,
  bg = NULL,
  ...
)
3. Details
Note: Filenames with page numbers can be generated by including a C integer format expression, such as ⁠%03d⁠ (as in the default file name for most R graphics devices, see e.g. png()). Thus, filename = "figure%03d.png" will produce successive filenames figure001.png, figure002.png, figure003.png, etc. To write a filename containing the ⁠%⁠ sign, use %%. For example, filename = "figure-100%%.png" will produce the filename ⁠figure-100%.png⁠.


4. Examples
## Not run: 
ggplot(mtcars, aes(mpg, wt)) +
  geom_point()

ggsave("mtcars.pdf")
ggsave("mtcars.png")

ggsave("mtcars.pdf", width = 4, height = 4)
ggsave("mtcars.pdf", width = 20, height = 20, units = "cm")

# delete files with base::unlink()
unlink("mtcars.pdf")
unlink("mtcars.png")

# specify device when saving to a file with unknown extension
# (for example a server supplied temporary file)
file <- tempfile()
ggsave(file, device = "pdf")
unlink(file)

# save plot to file without using ggsave
p <-
  ggplot(mtcars, aes(mpg, wt)) +
  geom_point()
png("mtcars.png")
print(p)
dev.off()


## End(Not run)

In addition, answer the following question:

> What is the purpose of the arguments `width` and `height` in the `ggsave()` function?
Plot size in units ("in", "cm", "mm", or "px"). If not supplied, uses the size of current graphics device.
Dimensions of the graph.


This section of the Markdown file should be formatted nicely so that code is formatted as code, headings as headings, etc. Use the Markdown Cheat Sheet to help you out.






