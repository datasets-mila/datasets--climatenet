##########
ClimateNet
##########

`<https://www.nersc.gov/research-and-development/data-analytics/climatenet/>`_

************************************************************************************************
Bringing the power of Deep Learning to the climate community via open datasets and architectures
************************************************************************************************

Mission
=======

The ClimateNet Project seeks to address an major open challenge in bringing the
power of deep learning to the climate community, viz. creating
community-sourced open-access expert-labeled datasets and architectures for
improved accuracy and performance on a range of supervised learning problems,
where plentiful reliable labelled training data is a requirement.

Motivation
==========

Pattern recognition tasks such as classification, localization, object
detection and segmentation have remained challenging problems in the weather
and climate sciences.

While there exist many heuristics and algorithms for detecting weather patterns
or extreme events in a dataset, the disparities between the output of these
different methods even for a single class of event are huge and often
impossible to reconcile. See, for example, the `ARTMIP
<http://www.cgd.ucar.edu/projects/artmip/>`__ project that attempts to compare,
contrast and reconcile the dozen or so atmospheric river tracking algorithms.

Meanwhile, Machine Learning and Deep Learning based approaches for pattern
recognition and pattern discovery tasks are showing great promise across the
sciences.  However, for supervised ML and DL methods, availability of plentiful
reliable training data is key. Given the scarcity of reliable labelled training
data for supervised Deep Learning based approaches and the pressing need to
address this problem, we propose creating a community-sourced expert-labelled
database.

Vision and Proposed Approach
============================

The figure below captures our overall vision for a unified Deep Learning
workflow, as relevant to climate science. The workflow can be split into two
pieces: the Training phase and the Inference phase. The goal of the Training
phase is to produce a single, unified Deep Network that is trained by examples
from \`hand'-labeled examples by human experts. In the inference phase, the
unified Deep Network is applied to archives of multi-resolution, multi-modal
datasets from climate model output or reanalyses or observational datasets.

A fundamental challenge in training Deep Networks is the availability of
reliable suitably labeled training data. We propose creating a \`ClimateNet'
dataset, with an accompanying schema that can capture information pertaining to
pattern labels, bounding boxes and segmentation masks.  Domain experts
(atmospheric and climate scientists) contribute \`hand'-labeled information to
the ClimateNet dataset -- the proposal was first presented by Prabhat, Karthik
Kashinath et al. at AGU 2017 and a project update was presented at AGU 2018.

We have developed a web interface called `ClimateContours
<https://climatecontours-gold.nersc.gov/climatecontours_gold/tool.html>`__
based on the "Label-Me" tool developed at the MIT computer vision lab to
crowdsource the \`hand'-labeling task. Note that the overall spirit of the Deep
Learning methodology is to **avoid** the prescription of heuristics for
defining weather patterns; it has been established by the computer vision
community that Deep Learning is effective at learning relevant features for
pattern classification tasks, without requiring application-specific tuning or
feature engineering. The figure below shows a snapshot of the labelling tool on
the web interface mentioned earlier.

Once the ClimateNet dataset has over a thousand labelled images (multi-variate
snapshots from high-res 25-km CAM5 data), we will extend state-of-the-art
segmentation CNN architectures to learn unified representations for various
weather patterns, including atmospheric rivers, tropical cyclones,
extra-tropical cyclones, and weather fronts. This will build upon our previous
work, notably:

-  *Liu et al. (2016),* **Application of deep convolutional neural networks for
   detecting extreme weather in climate datasets**\ *, arXiv preprint
   arXiv:1605.01156,*
-  *Mudigonda et al. (2017),* **Segmenting and tracking extreme climate events
   using neural networks, Deep Learning for Physical Sciences**\ *, NIPS
   workshop,*
-  *Racah et al. (2017),* **ExtremeWeather: A large-scale climate dataset for
   semi-supervised detection, localization, and understanding of extreme weather
   events**\ **,** *31st conference on Neural Information Processing Systems,
   and*
-  *Kurth, T., Treichler, S., Romero, J., Mudigonda, M., Luehr, N., Phillips,
   E., Mahesh, A., Matheson, M., Deslippe, J., Fatica, M., Prabhat, and Houston,
   M.,* **Exascale deep learning for climate analytics**. In Proceedings of the
   Inter national Conference for High Performance Computing, Networking,
   Storage, and Analysis, pp. 51. IEEE Press, 2018. (Winner of the `2018 Gordon
   Bell Prize <https://awards.acm.org/bell>`__.)

We will then apply the unified network to archives of multi-resolution,
multi-modal datasets from climate model output, reanalyses and observations to
seamlessly extract class labels, bounding boxes and segmentation masks.

About NERSC and Berkeley Lab
============================

The National Energy Research Scientific Computing Center (NERSC) is a U.S.
Department of Energy Office of Science User Facility that serves as the primary
high-performance computing center for scientific research sponsored by the
Office of Science. Located at Lawrence Berkeley National Laboratory, the NERSC
Center serves more than 7,000 scientists at national laboratories and
universities researching a wide range of problems in combustion, climate
modeling, fusion energy, materials science, physics, chemistry, computational
biology, and other disciplines.  `Berkeley Lab <http://www.lbl.gov/>`__ is a
DOE national laboratory located in Berkeley, California. It conducts
unclassified scientific research and is managed by the University of California
for the U.S. Department of Energy.  »\ `Learn more about computing sciences
<http://cs.lbl.gov>`__ at Berkeley Lab. 
