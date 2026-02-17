# Image Analysis tools - Institut Pasteur

<img src="assets/IP_Logo_Noir_RVB.png" alt="IP_Logo_Noir_RVB" height="150" />  <img src="assets/CNRS-logo.png" alt="IP_Logo_Noir_RVB" height="150" />

This organization contains repositories of the tools developed by bioimage analysis engineers of the Institute Pasteur, Paris, developed within two collaborating teams:

- [Image Analysis Hub](https://research.pasteur.fr/en/team/image-analysis-hub/) of Pasteur's Technology Department
- [Developmental and Stem Cell Biology Department](https://research.pasteur.fr/en/department/developmental-stem-cell-biology/) / CNRS UMR3738 of Institut Pasteur.

We are research engineers and a significant part of our work is the creation of custom image analysis pipelines for our users, tailored to their projects, developed in a collaborative manner.
Often, these developments materialized in widely usable tools, that we make available to the scientific community.
These tools are all included in this repository or linked from this page. 
They are **Findable** (we link and introduce them here), **Accessible** (you will find installation instructions, that work, for all of them), **Interoperable** (we build them within existing ecosystems) and **Reusable** (they have a scope and a usability more general than the specific project they were built for).


**Content**

   * [Our Tools](#our-tools)
      * [<a href="https://github.com/clEsperanto">clEsperanto</a>](https://github.com/clEsperanto)
      * [<a href="https://github.com/Image-Analysis-Hub/DeProj">DeProj</a>](https://github.com/Image-Analysis-Hub/DeProj)
      * [<a href="https://github.com/Image-Analysis-Hub/DeXtrusion">DeXtrusion</a>](https://github.com/Image-Analysis-Hub/DeXtrusion)
      * [<a href="https://github.com/Image-Analysis-Hub/LocalZProjector">LocalZProjector</a>](https://github.com/Image-Analysis-Hub/LocalZProjector)
      * [<a href="https://github.com/trackmate-sc/MaMuT">MaMuT</a>](https://github.com/trackmate-sc/MaMuT)
      * [<a href="https://github.com/mastodon-sc/mastodon">Mastodon</a>](https://github.com/mastodon-sc/mastodon)
      * [<a href="https://github.com/multiview-stitcher/multiview-stitcher">Multiview-Stitcher</a>](https://github.com/multiview-stitcher/multiview-stitcher)
      * [<a href="https://github.com/image-Analysis-Hub/pycellin">Pycellin</a>](https://github.com/image-Analysis-Hub/pycellin)
      * [<a href="https://github.com/trackmate-sc/TrackMate">TrackMate</a>](https://github.com/trackmate-sc/TrackMate)
   * [Scientific software platforms](#scientific-software-platforms)
      * [<a href="https://icy.bioimageanalysis.org/" rel="nofollow">Icy</a>](https://icy.bioimageanalysis.org/)
      * [<a href="https://fiji.sc/" rel="nofollow">Fiji</a>](https://fiji.sc/)
      * [<a href="https://scipion.i2pc.es/" rel="nofollow">Scipion</a>](https://scipion.i2pc.es/)






## Our Tools

### [clEsperanto](https://github.com/clEsperanto)

<a href="https://github.com/clEsperanto"><img src="assets/cle-logo.png" alt="deproj-logo" height="100" align="left" margin="10" /></a>

clEsperanto is a GPU-accelerated image processing library that offers your favorite image processing functions on GPU, a unified API accessible across various programming languages, and broad compatibility with different hardware and systems.
It is a large project involving several contributors, and it has its own Github org (https://github.com/clEsperanto).
You can find clEsperanto documentation [here](https://clesperanto.github.io/).
Our work there results from a collaboration with [Robert Haase](https://haesleinhuepf.github.io/) funded by a [CZI EOSS4](https://chanzuckerberg.com/eoss/proposals/gpu-accelerating-fiji-and-friends-using-distributed-clij-neubias-style/) grant.



### [DeProj](https://github.com/Image-Analysis-Hub/DeProj)

<a href="https://github.com/Image-Analysis-Hub/DeProj"><img src="assets/deproj-logo.png" alt="deproj-logo" height="150" align="left" margin="10" /></a>

DeProj is a MATLAB app made to yield accurate morphological measurements on cells in epithelia or tissues.
Typically, it works from 1/ a binary mask, from the segmentation of the apical surface of cells in tissue and 2/ a height map of the corresponding tissue (the Z position for all X, Y), and generates several morphological measurements on the cells, corrected for the curvature of the tissue.
It is made to work well with the LocalZProjector Fiji plugin (see below).

[Documentation](https://github.com/Image-Analysis-Hub/DeProj?tab=readme-ov-file#citation)

Paper:
>_LocalZProjector and DeProj: a toolbox for local 2D projection and accurate morphometrics of large 3D microscopy images_
>
>Sébastien Herbert, Léo Valon, Laure Mancini, Nicolas Dray, Paolo Caldarelli, Jérôme Gros, Elric Esposito, Spencer L. Shorte, Laure Bally-Cuif, Romain Levayer, Nathalie Aulner, Jean-Yves Tinevez
>
>BMC Biol 19, 136 (2021). https://doi.org/10.1186/s12915-021-01037-w



### [DeXtrusion](https://github.com/Image-Analysis-Hub/DeXtrusion)

<a href="https://github.com/Image-Analysis-Hub/DeXtrusion"><img src="https://raw.githubusercontent.com/Image-Analysis-Hub/DeXtrusion/main/images/DeX.png" align="left" margin="10" /></a>

DeXtrusion is a machine learning based python pipeline to detect cell extrusions in epithelial tissues movies.
It can also detect cell divisions and emergence of SOPs (sensory organ precursors).
It can easily be trained to detect other dynamic events.

[Documentation](https://github.com/Image-Analysis-Hub/DeXtrusion?tab=readme-ov-file#-dextrusion)

Paper:
>_DeXtrusion: automatic recognition of epithelial cell extrusion through machine learning in vivo_ 
>
>Alexis Villars, Gaëlle Letort, Léo Valon, Romain Levayer
>
>Development (2023). 150 (13): dev201747. doi: https://doi.org/10.1242/dev.201747



### [LocalZProjector](https://github.com/Image-Analysis-Hub/LocalZProjector)

<a href="https://github.com/Image-Analysis-Hub/LocalZProjector"><img src="assets/LocalZProjectorLogo-512-text.png" alt="LocalZProjectorLogo-512-text" height="150" align="left" /></a>

Local Z Projector (LZP) is an ImageJ2 plugin to perform local-Z projection of a 3D stack, possibly over time, possibly very large.
It processes images of epithelial tissues where the apical surface is curved but has no folds. 
The LZP plugin automatically creates a 2D projection of the apical surface of the tissue and the corresponding height map of the tissue. 
It is made to work even if there are spurious or unwanted structures in the 3D volume.
LZP is deployed as a [Fiji](https://fiji.sc/) plugin with a user interface and made to work well with the DeProj MATLAB analysis package (see above).

See also in this org the [LocalZBackProjector](https://github.com/Image-Analysis-Hub/localZBackProjector), that can retrieve the height map from 2D denoised projected epithelia image and the initial 3D image.

[Documentation](https://github.com/Image-Analysis-Hub/LocalZProjector?tab=readme-ov-file#local-z-projector-documentation)

Paper:
>_LocalZProjector and DeProj: a toolbox for local 2D projection and accurate morphometrics of large 3D microscopy images_
>
>Sébastien Herbert, Léo Valon, Laure Mancini, Nicolas Dray, Paolo Caldarelli, Jérôme Gros, Elric Esposito, Spencer L. Shorte, Laure Bally-Cuif, Romain Levayer, Nathalie Aulner, Jean-Yves Tinevez
>
>BMC Biol 19, 136 (2021). https://doi.org/10.1186/s12915-021-01037-w



### [MaMuT](https://github.com/trackmate-sc/MaMuT)

<a href="https://github.com/trackmate-sc/MaMuT"><img src="https://imagej.net/media/icons/mamut.png" align="left" height="150" /></a>

MaMuT is a [Fiji](https://fiji.sc/) plugin that combines the [BigDataViewer](https://imagej.net/plugins/bdv) and [TrackMate](https://imagej.net/plugins/trackmate) in an application that allow browsing, tracking cells and curating annotations for large 3D+T image data, possibly over multiple views (in the case of SPIM).
The code results from a collaboration with the lab of Pavel Tomancak, and is part of the dedicated [TrackMate org](http://github.com/trackmate-sc/).
It is still maintained, but today it has been superseded by Mastodon (see below).

[Documentation](https://imagej.net/plugins/mamut/)

Paper:
>_Multi-view light-sheet imaging and tracking with the MaMuT software reveals the cell lineage of a direct developing arthropod limb._
>
>Carsten Wolff, Jean-Yves Tinevez, Tobias Pietzsch, Evangelia Stamataki, Benjamin Harich, Léo Guignard, Stephan Preibisch, Spencer Shorte, Philipp J Keller, Pavel Tomancak, Anastasios Pavlopoulos 
>
>ELife, 7 (2018). [doi:10.7554/elife.34410](https://doi.org/10.7554/elife.34410)



### [Mastodon](https://github.com/mastodon-sc/mastodon)

<a href="https://github.com/mastodon-sc/mastodon"><img src="https://github.com/mastodon-sc/mastodon/blob/master/doc/Mastodon-logo-512x512.png?raw=true" align="left" height="150" /></a>

Mastodon is a large-scale tracking and track-editing framework for large, multi-view images, such as the ones that are typically generated in the domain Development Biology or Stem-Cell Biology or Cell Biology.
It is our effort to provide a framework that can track cells, curate tracks and analyze tracks in very large movies, following millions of objects in 3D+T, multiview, in a powerful and user-friendly tool.
The core code results from a collaboration with the lab of Pavel Tomancak and its several extensions involve many excellent collaborators. 
Because Mastodon is built on several repos with several people, it has its own [Mastodon Github org](https://github.com/mastodon-sc). 

[Documentation](https://mastodon.readthedocs.io/en/latest/)

Paper:
>_Mastodon: the Command Center for Large-Scale Lineage-Tracing Microscopy Datasets._
>
>Johannes Girstmair, Tobias Pietzsch, Vladimir Ulman, Stefan Hahmann, Matthias Arzt, Mette Handberg-Thorsager, Samuel Pantze, Ko Sugawara, Robert Haase, Jean-Yves Tinevez, Pavel Tomancak
>
>bioRxiv (2025).12.10.693416; doi: https://doi.org/10.64898/2025.12.10.693416



### [Multiview-Stitcher](https://github.com/multiview-stitcher/multiview-stitcher)

<a href="https://github.com/multiview-stitcher/multiview-stitcher"><img src="https://github.com/multiview-stitcher/multiview-stitcher/blob/main/docs/images/logo_color.png?raw=true" align="left" height="100" /></a>

Multiview-stitcher is an open-source modular toolbox for distributed and tiled stitching of 2-3D image data in Python. 
It is a collection of algorithms to register and fuse small and large datasets from multi-positioning and multi-view light sheet microscopy, as well as other modalities such as correlative cryo-EM datasets. 
As such, it shares considerable functionality with the Fiji plugin BigStitcher, with the difference that it is designed for interoperability with the Python scientific ecosystem. 
It has its own [Github org](https://github.com/multiview-stitcher) in which you will find a user interface within napari.

[Documentation](https://multiview-stitcher.github.io/multiview-stitcher/main/)



### [Pycellin](https://github.com/image-Analysis-Hub/pycellin)

<a href="https://github.com/image-Analysis-Hub/pycellin"><img src="https://github.com/Image-Analysis-Hub/pycellin/raw/main/pycellin_logo.png" align="left" height="100" /></a>

Pycellin is a graph-based Python framework to easily manipulate and analyze cell tracking data, at the single-cell level. 
In particular, it is made to analyze lineages comprising cell divisions, and can extract quantitative measurements linked to these events.
Pycellin provides predefined properties related to cell morphology, cell motion and tracking that can be automatically added to enrich lineages. 
It is designed to perform the last analysis after tracking,  and we made it interoperable with a very wide range of tracking tools (among them TrackMate, see below).
In addition, Pycellin is the medium through which we collaborate on [GEFF](https://github.com/live-image-tracking-tools/geff) with the _Live Image Tracking Tools_ consortium, working to build a universal file format to exchange tracking results between scientific tools.



### [TrackMate](https://github.com/trackmate-sc/TrackMate)

<a href="https://github.com/trackmate-sc/TrackMate"><img src="https://github.com/trackmate-sc/TrackMate/blob/master/src/main/resources/fiji/plugin/trackmate/gui/images/Logo50x50-color-nofont-72p.png?raw=true" align="left"  /></a>

TrackMate is a [Fiji](https://fiji.sc/) plugin that performs cell, organelle and object tracking.
It takes the shape of a user-friendly plugin, in wizard-like interface, where a user can select and configure a wide range of detection, segmentation and linking algorithms. 
Users can edit tracking results, perform automated, semi-automatic and fully automatic tracking.
TrackMate comes with a very wide range of extensions and additions, and is developed with a dedicated [Github repo org](https://github.com/trackmate-sc), collaborating with excellent people.

[Documentation](https://imagej.net/plugins/trackmate/)

Papers:
>_TrackMate 7: integrating state-of-the-art segmentation algorithms into tracking pipelines._
>
>Dmitry Ershov, Minh-Son Phan, Joanna W. Pylvänäinen, Stéphane U. Rigaud, Laure Le Blanc, Arthur Charles-Orszag, James R. W. Conway, Romain F. Laine, Nathan H. Roy, Daria Bonazzi, Guillaume Duménil, Guillaume Jacquemet & Jean-Yves Tinevez
>
>Nature Methods (2022). 19(7), 829–832. [doi:10.1038/s41592-022-01507-1](https://www.nature.com/articles/s41592-022-01507-1)

>_TrackMate: An open and extensible platform for single-particle tracking._ 
>
>Jean-Yves Tinevez, Nick Perry, Johannes Schindelin, Genevieve M. Hoopes, Gregory D. Reynolds, Emmanuel Laplantine, Sebastian Y. Bednarek, Spencer L. Shorte, Kevin W. Eliceiri
>
>Methods (2017). 115, 80–90. [doi:10.1016/j.ymeth.2016.09.016](https://www.sciencedirect.com/science/article/pii/S1046202316303346)





## Scientific software platforms

Most of our contributions are made within the Python scientific ecosystem or deployed in scientific software platforms.
We are core contributors of several of them, supporting their development and benefitting from the facilities they offer for deployment and maintenance.



### [Icy](https://icy.bioimageanalysis.org/)

<a href="https://icy.bioimageanalysis.org/"><img src="https://imagej.net/imagej-wiki-static/images/3/37/Icy-icon.png" align="left" height="100" /></a>

Icy is a bioiomage analysis platform written in Java for its core.
It offers to users a core user interface to open, inspect, and analyze microscopy images, along with a set of advanced image analysis and processing algorithms.
It is a modular software composed of a kernel and plugins, with a goal similar to that of Fiji (see below).
Its main development is carried on by the Biological Image Analysis unit at Institut Pasteur, with whom we collaborate.
We are currently working on developing its next major version with a full redesign, stronger integration with the Java scientific ecosystem and interoperability with the Python scientific ecosystem.



### [Fiji](https://fiji.sc/)

<a href="https://fiji.sc/"><img src="https://fiji.sc/site/logo.png" align="left" height="100" /></a>

Fiji is an image processing package — a "batteries-included" distribution of ImageJ, bundling many plugins which facilitate scientific image analysis.
It builds on top of the ImageJ2 and ImageJ core and is today one of the most used and cited scientific software tool.
We have been core contributors of the Fiji project since its inception, and contributed and maintained a set of plugins and utilities in Fiji, some of which are listed above.
Today, the Fiji core development is carried mainly by the team of Kevin Eliceiri in the University of Madison, with whom we collaborate.
The Institut Pasteur, Paris hosts a mirror for the Fiji software, including plugins.





### [Scipion](https://scipion.i2pc.es/)

<a href="https://scipion.i2pc.es/"><img src="https://scipion-em.github.io/docs/release-3.0.0/_images/scipion_logo_nobackground.png" align="left" height="100" /></a>

Scipion is an image processing framework for obtaining 3D models of macromolecular complexes using Electron Microscopy (3DEM). 
It integrates several software packages and presents a unified interface for both biologists and developers. 
Scipion allows executing workflows combining different software tools, while taking care of formats and conversions. 
It is the main platform with which we use to support our users with image processing for electron microscopy. 
