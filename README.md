# PowerPoint Presentation File Size Reducer #

## Usage by CLI ##

```
pptxreduce [-w] file ...

-w  Overwrite the original pptx file.
    If the option isn’t chosen, the original file is renamed to *.pptx~
```

## Usage by GUI ##

1. Run `sudo cp pptxreduce /usr/local/bin`
2. Drag & drop \*.pptx to the Automator application, pptxreduce.app

## Background ##

PowerPoint for Mac often creates a huge pptx file. The cause is because it saves a pasted image as a **uncompressed** TIFF file in the pptx file. Mac user never pastes images and always have to use Insert ribbon.

This tiny script fixes the problem by the following step.

1. Uncompressed a \*.pptx as a ZIP file
1. Compress it again as a ZIP file

That’s all. The uncompressed TIFF files are compressed at the step 2.
