# SB-forwardmodel

This python notebook serves as an example of the surface brightness forward modeling procedure from the paper 
<i><b> Smooth and lightly stirred: gas homogeneity and turbulence at intermediate radii in the Perseus Cluster </b></i> (arXiv link to follow). 

Note that this is not meant to be a plug-and-play package, but as an example that might serve as the basis for similar modeling in other objects. The notebook as written requires several inputs, examples
of which are included (for a full description of the model and why these inputs are required, please refer to the paper):
<ol>
<li> A bin table with the following information about about each bin 
<ul>
<li> The number of counts </li>
<li> The summed exposure value  (from the un-normalized exposure map) </li>
<li> The surface brightness </li>
<li> The pixel size (the notebook assumes the images were binned 4x4 native ACIS resolution) </li>
<li> The number of counts in the particle background </li>
<li> The exposure time ratio t_src/t_bkg </li>
<li> The pixel radius </li>
</ul>
</li>
<li> background scaling table with the following information about about each bin 
<ul>
<li> The background scaling ratio of each ObsID the bin overlaps with </li>
<li> The error on the background scaling ratio of each ObsID the bin overlaps with </li>
<li> The exposure time of each ObsID the bin overlaps with </li>
<li> The exposure time of the stowed background file appropriate for each ObsID the bin overlaps with </li>
</ul>
</li>
<li> A set of unresolved AGN flux files, which contain samples of the range of possible SB values of the unresolved AGN background, as a function of bin size.
The integer behind the p refers to pixel size that the samples were drawn for, using the AGN luminosity function as described in the paper. The notebook finds
the appropriate samples for each bin, and used those in the modeling procedure. </li>

</ol>
