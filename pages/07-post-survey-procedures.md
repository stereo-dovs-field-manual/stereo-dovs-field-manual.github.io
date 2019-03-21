---
layout: home
permalink: /post-survey-procedures
title: "Post-survey procedures"
excerpt: ""
image:
  feature: /banners/07_banner.jpg
---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}

Data management and quality assurance/control are crucial for monitoring and comparisons between studies within a given area. Following simple steps and using easily understandable and transferable metadata (see Table 6.5) will enable efficient harmonisation between studies. 


## Data management

Store used cards separately from unused cards.



33. Download the video data onto a portable hard-drive using a card reader or equivalent. 
34. Save the files from each camera in a separate folder named using the unique site/drop identifier and L for left side or R for right side (e.g. CH001L). 
35. Use multiple laptops or extra card readers to speed up the process.
36. During downloads, check that the videos are of good quality and note any interesting species etc. If any issue occurred with a camera, rig etc. attempt to rectify the issue before the next day's sampling.
37. At the end of each day, make a backup of the day's videos to two hard-drives stored in separate locations. 
38. Transcribe the data from the data sheets into an expedition spreadsheet updated and backed up daily. The spreadsheet should also include the hard drive number where each sample is saved.

<span style="text-decoration:underline;">Note:</span> It is important that all hard drives be clearly labelled – e.g. with the date, project name, contents and hard drive number. Ideally, files should also be labelled according to a standardised and unambiguous naming convention. All memory cards should be stored in waterproof containers. They should not be re-used or reformatted until data has been download and a backup created.

Pelagic BRUVs typically generate large volumes of data, including video imagery, field data sheets and software outputs. Consistently labelling folders and files is therefore essential to easily locating information and simplifying analyses. An example folder name is "176022_Groote_Island_stereo-BRUV_HD1", which concatenates the deployment date, study location/name, and hard drive number. Similarly, an appropriate file name could reflect the following structure:  OpCode_year_month_day_study_cam1_cam2_L (folders on hard drives should follow a naming convention so that programs like [Bulk Rename Utility](http://www.bulkrenameutility.co.uk/Download.php) can be easily used to rename all files with OpCode and camera number in the correct format). Template folder/file structures and further details on data management and quality control are provided in Chapter 5.

At this stage, there are no online video file storage databases, however the [GlobalArchive](http://globalarchive.org/) platform has been created to store metadata (see Section 6.7.4). Refer to the software's website for instructions on metadata and data recording instructions.


## Quality control

Quality assurance/quality control (QAQC) is an equally vital but potentially time-consuming undertaking for organisations and individual researchers. Following straightforward steps and using easily understandable and transferable metadata will enable harmonisation between studies.

It is important that any data corrections are made within the original annotation files to ensure consistency over time. Four complementary QAQC approaches are recommended:



*   Analysts should first be adequately trained by processing videos for which species composition and density are known, and to which their results can be compared.
*   Once the first annotation (fish counts and lengths) for a deployment is completed, a different analyst should view each MaxN annotation to double-check the species ID and abundance estimates.
*   Footage from any previously unrecorded (i.e. range or depth extensions) or unidentifiable species should be sent to the project taxonomist for formal ID. It is important to send footage clip rather than still images.

R workflows are provided in a [GitHub repository](https://github.com/TimLanglois/Stereo-or-mono-video-annotation-workflows) to enable comparison with regional species lists and likely minimum and maximum sizes for each species (Langlois 2017).

Importantly, any corrections should be made to the annotation files before data are exported to GlobalArchive or other repositories.


## Video processing

Trained analysts/fish biologists/taxonomists must be engaged to ensure that all footage can be appropriately processed and species can be correctly identified. Care must be taken to ensure that a consistent nomenclature is used, with [FishBase](http://www.fishbase.org/search.php), the [World Register of Marine Species](http://www.marinespecies.org/) (WoRMS) and the [Codes for Australian Aquatic Biota](https://www.cmar.csiro.au/caab/) (CAAB) being popular, authoritative sources of taxonomic information. Undescribed or unnamed species (e.g. defined operational taxonomic units, OTUs) must also be meticulously documented. Archives of reference images from previous sampling campaigns have been established by numerous agencies across Australia and can serve as a useful benchmark for problematic sightings. The Collaborative and Annotation Tools for [Analysis of Marine Imagery and Video (CATAMI) Project](http://catami.org) offers a framework for the cataloguing, annotation, classification and analysis of underwater imagery (Althaus et al. 2015).

A number of software tools are currently available for image analysis, with [SeaGIS EventMeasure](https://www.seagis.com.au/event.html) being arguably the most widespread but also the costliest. Advanced packages such as [Image-Pro Plus](http://www.mediacy.com/imageproplus), [SigmaScan](http://www.sigmaplot.co.uk/products/sigmascan/sigmascan.php), or simpler programmes such as [ScreenCalipers](http://www.iconico.com/caliper/) can also be used to make measurements calibrated by scale bars. The [StereoMorph](https://cran.r-project.org/package=StereoMorph) R package (Olsen & Westneat 2015) is an open-source alternative that additionally allows the reconstruction of 3D objects. Irrespective of the approach chosen, it is critical that any output be produced in a format comparable to other studies to facilitate comparison of data between campaigns and organisations.

Overestimates of abundance can occur as a result of double counting, for instance when the same individual/s is/are viewed at different time points throughout a deployment. To overcome this challenge, counts of the maximum number (MaxN) of individuals of any one species seen over the recording period have been used. In a monitoring context, comparative studies have suggested that the use of MaxN may be "hyper-stable" (i.e. underrepresents the magnitude of changes in true abundance) when fish abundance is high due to saturation of the field of view (Schobernd_ et al._ 2013) and have suggested alternative metrics (e.g. MeanCount). However, MaxN remains the most widely accepted metric, and provides the best option for standardisation between sampling programs.

The essential information produced by annotation software should include three main outputs:



*   Point information
*   Length measurements
*   3-D point information

Point information is typically used to calculate MaxN values, while length and 3D point information is used to calculate length and biomass metrics. EventMeasure-Stereo has established queries built-in that produce a number of chosen metrics over a user defined period within the footage. In addition, EventMeasure-Stereo annotation datasets held within GlobalArchive can be queried in a similar fashion to produce such metrics. While there are a number of relative abundance metrics available, MaxN is the most widely accepted (Harvey_ et al._ 2007).

The type of fish length measured (e.g. fork length or total length for fish and disc length for rays) should be clearly indicated as part of the annotation information for each sampling campaign.


## Data release

[GlobalArchive](http://www.globalarchive.org) is a centralised repository for stereo- and single-camera fish image annotation data, in particular for Baited Remote Underwater stereo-Video (stereo-BRUVs) and Diver Operated stereo-Video (stereo-DOVs). A user manual for GlobalArchive is available in an open-access [GitHub repository](https://github.com/TimLanglois/GlobalArchive). Metadata should be made publicly available via [GlobalArchive](http://globalarchive.org/) as soon as possible after survey completion and data QA/QC and validation. This should include positional data, as well as the purpose of the sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. Annotations can also be uploaded once complete. Spatial metadata from GlobalArchive data will in the future be harvested by the Australian Ocean Data Network, and the metadata will accordingly be available on their national portal. Until this is done, metadata should be published on both GlobalArchive and AODN to ensure data discoverability _[Recommended]_.

There is currently no national repository for BRUV imagery so we recommend following agency-specific protocols to ensure public release. A national marine imagery repository (including for BRUV imagery) will be scoped in 2018 and updates provided in Version 2 of this field manual.

Following the steps listed below will ensure the timely release of BRUV imagery and associated annotation data in a standardised, discoverable format.



39. Immediate post-trip reporting should be completed by creating a metadata record documenting the purpose of the BRUV sampling campaign, the survey design, sampling locations, equipment specifications, and any challenges or limitations encountered. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling.
40. Publish metadata record to the [Australian Ocean Data Network (AODN) catalogue](http://catalogue.aodn.org.au/geonetwork/srv/eng/main.home) as soon as possible after metadata has been quality controlled (see section 6.7.2). This can be done in one of two ways:
*   If metadata from your agency is regularly harvested by the AODN, follow agency-specific protocols for metadata and data release. 
*   Otherwise, metadata records can be created and submitted via the [AODN Data Submission Tool](https://metadataentry.aodn.org.au/submit). Note that user registration is required, but this is free and immediate.

Lodging metadata with the AODN prior to making annotation data available is an important step in documenting the BRUV campaign and enhancing future discoverability of the data.

41. Annotate video (fish counts and length) using EventMeasure or similar software.
42. Upload annotation data and any associated calibration, taxa and habitat data to GlobalArchive.
43. Upload raw video data to a secure, publicly accessible online repository ([contact AODN](mailto:info@aodn.org.au) if you require assistance in locating a suitable repository for large video collections).
44. Add links to GlobalArchive campaign and raw video storage location to previously published metadata record. You may also wish to attach or link a copy of the annotation data directly to the published metadata record.
45. Produce a technical or post-survey report documenting the purpose of the survey, sampling design, sampling locations, sampling equipment specifications, annotation protocol, and any challenges or limitations encountered. Provide links to this report in all associated metadata. See Appendix C _[Recommended]._

