**Summary**

Allow the display for the ColorToGrey module to show an arbitrary number of channels.  

**Background and rationale**

Increasingly CellProfiler is used to study images that have been imaged in >3 channels; for simplicity's sake, these are often stored as a single multichannel file whose colors are split using ColorToGrey's Split->Channels mode.  Split->Channels can work on images with an arbitrary number of channels to split them all out, but in this mode only displays the first 3 channels it has split out, no matter how many channels are included.  [This can cause confusion](http://forum.cellprofiler.org/t/can-you-use-cellprofiler-to-analyze-whole-tissue-samples-6-color-images/4711/5?u=bcimini).

![ColorToGrey's output splitting a 6 channel image](images/ColorToGreyScreenshot.png)


**Proposal**

One of two solutions would be helpful- ideally we could show every channel as it's split out, as CorrectIlluminationApply can for n-channel images.  If for some reason that wasn't possible, simply adding a sentence saying "N more channels not shown".  

**Implementation**

[See bethac07/CellProfiler branch RFC/2](https://github.com/bethac07/CellProfiler/blob/RFC/2/cellprofiler/modules/colortogray.py)
