---
permalink: /research/
title: false
---
## Developmental changes in alpha and mu rhythms

**Update**: We recently published this work on *bioRxiv* and it is under review at the *Journal of Neuroscience*!
{: .notice--info}

<img src="/assets/images/alpha_mu_traces.png" width="400">{: .align-right}
**Background**: Alpha rhythms in occipital cortex and mu rhythms in sensorimotor cortex are two of the most prominent rhythms in the human brain (example rhythms and corresponding spatial topographies are shown to the right). They have similiar characteristic frequencies in the canonical alpha band (8–12 Hz) and serve important functions in gating modality-specific information. Both alpha-band rhythms have been implicated in autism spectrum disorder (ASD) and attention-deficit hyperactivity disorder (ADHD) in disorder-relevant tasks (e.g., social encoding tasks for ASD and attention-demanding tasks for ADHD). In this project, we investigated whether these rhythms could serve as biomarkers for these developmental disorders in resting-state electroencephalography (EEG). Such biomarkers would greatly aid in developing effective early diagnostic tools for ASD and ADHD.
{: .text-justify}

**Methods**: We used an [openly available developmental dataset](http://fcon_1000.projects.nitrc.org/indi/cmi_healthy_brain_network/index.html) of resting-state EEG recordings from nearly 3000 children (ages 5–18) from the [Child Mind Institute](https://childmind.org/) published by [Alexander and colleagues (2017)](https://www.nature.com/articles/sdata2017181). We isolated high-fidelity alpha and mu rhythms from these recordings using an computationally efficient integration of [spectral parameterization](https://www.nature.com/articles/s41593-020-00744-x), [spatial filters](https://www.sciencedirect.com/science/article/pii/S1053811911000930), and source localization. We then used burst detection and [waveform shape analysis](https://journals.physiology.org/doi/full/10.1152/jn.00273.2019) to characterize the time series of these isolated alpha and mu rhythms:
{: .text-justify}
<img src="/assets/images/waveform_feats.png" width="700">{: .align-center}

**Results**: First, we demonstrated that alpha rhythms are lower frequency, less asymmetrical, and higher amplitude than mu rhythms. These results quantifiably replicate qualitative differences in alpha and mu at an unprecendented scale:
{: .text-justify}
<img src="/assets/images/alpha_vs_mu_feats.png" width="700">{: .align-center}

Next, we discovered that alpha and mu rhythms are significantly different at age five and change differently across development:
{: .text-justify}
<img src="/assets/images/fig3_age.png" width="700">{: .align-center}

Finally, we showed that neither alpha nor mu rhythms are sensitive biomarkers in resting-state EEG, implying sensitive EEG biomarkers for ASD and ADHD may require deficit-specific task operalization:
{: .text-justify}
<img src="/assets/images/fig4_diagnosis.png" width="700">{: .align-center}

**Conclusion**: We extended previous findings of alpha-band rhythms undergoing large changes in frequency during development, showing that these waveform shape measures also change substantially
across development. While none of these resting-state changes appear to be associated with common neurodevelopmental disorders, characterizing differences across rhythm types remains
vital for constraining generative models for alpha-band rhythms.

- **Manuscript**
    - **Bender A.**, Voytek B.\*, Schaworonkow N.\* Resting-state is not enough: alpha and mu rhythms change shape across development, but lack diagnostic sensitivity. doi: [https://doi.org/10.1101/2023.10.13.562301](https://doi.org/10.1101/2023.10.13.562301). \*These authors contributed equally to this work. 
- **Presentations**
    - **Bender, A.**, Schaworonkow, N., Voytek, B. Age-related changes in alpha and mu oscillation amplitude and waveform asymmetry. *Society for Neuroscience*; 2022, November 16; San Diego, CA. ([poster](/files/SfN2022Poster.pdf))
    - **Bender, A.**, Schaworonkow, N., Voytek, B. Quantifying waveform shape of EEG alpha and mu oscillations across development. *Cognitive Neuroscience Society*; 2022, April 26; San Francisco, CA. ([poster](/files/CNS2022Poster.pdf))
    - **Bender, A.**, Schaworonkow, N., Voytek, B. Quantifying waveform shape of EEG alpha and mu oscillations across development. *Society for Neuroscience*; 2021, November 9; remote. ([presentation](/files/SfN2021Presentation.pdf))
{: .text-justify}

## Representations of spatial location by aperiodic and alpha oscillatory activity in working memory

**Background**: Working memory (WM) refers to one’s ability to hold and manipulate a limited amount of information in mind for a short period of time, usually on the order of seconds, and is integral to many other cognitive functions. Previous work from [Foster and colleagues (2016)](https://journals.physiology.org/doi/full/10.1152/jn.00860.2015) demonstrated that the topopgraphy of alpha-band activity (8–12 Hz) tracks the spatial location in stimuli in WM, suggesting that alpha oscillations coordinate the cellular assemblies that code the content of WM. Previous work in our lab by [Donoghue, Haller, Peterson, et al., (2020)](https://www.nature.com/articles/s41593-020-00744-x) has shown that standard spectral analyses can conflate oscillatory changes with change in aperiodic activity. In this project, we sought to distiniguish the roles of alpha oscillatory and aperiodic activity in WM using sliding-window [spectral parameterization](https://fooof-tools.github.io/fooof/) to ensure the development of an accurate physiological understanding of visual WM and the true role of alpha oscillations therein.
{: .text-justify}

**Methods**: In collaboration with [Drs. Ed Awh and Ed Vogel](https://awhvogellab.com/), we used EEG data from participants at the University of Oregon (*n* = 56) and the University of Chicago (*n* = 56) that came from three published, publically available datasets ([Foster et al., 2016](https://journals.physiology.org/doi/full/10.1152/jn.00860.2015); [Foster et al., 2017](https://www.sciencedirect.com/science/article/pii/S096098221731196X); [Sutterer et al., 2019](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3000239)). Even though the EEG data come from seven different tasks, all data were collected while participants attended and remembered features of stimuli presented around fixation across a delay, requiring WM. All tasks were continuous report, where participants were required to report the location, color, or orientation of the target stimulus, except for task 3, where participants only had to indicate whether there was a change in the probe stimulus from the target stimulus:
{: .text-justify}
<img src="/assets/images/wm_tasks.png" width="700">{: .align-center}

We computed spectrograms for each sensor and determined the aperiodic exponent and alpha oscillatory power for each time point using [spectral parameterization](https://fooof-tools.github.io/fooof/). Following the procedure of the [Foster and colleagues (2016)](https://journals.physiology.org/doi/full/10.1152/jn.00860.2015), we then fit an inverted encoding model (IEM) to assess how strongly spatial location was represented by the aperiodic exponent and alpha oscillatory power throughout the trial.

**Results**: We first reproduced the authors’ findings that total alpha power represents spatial location during WM. The channel tuning function (CTF) slope, which assesses how strongly the population activity in the alpha band represents the spatial location of the stimulus, increases soon after stimulus presentation and remains high throughout the delay period (red line for each task below): 
{: .text-justify}
<img src="/assets/images/IEMs_tasks1-7.png" width="700">{: .align-center}

Representation of spatial location by alpha oscillatory power was high throughout the delay period (blue line for each task above) in each of the seven tasks, supporting the idea that alpha oscillations act as a scaffolding signal that coordinate which of the underlying retinotopic cellular assemblies maintain the stimulus features in working memory. This representation of spatial location by alpha oscillatory power was significantly greater across the delay period than when location labels were shuffled:
{: .text-justify}
<img src="/assets/images/pw_ctf_slope_paired_ttest.png" width="700">{: .align-center}

By contrast, representation of spatial locaiton by the aperiodic exponent peaks during the early portion of the stimulus presentation for all seven tasks (green line for each task above). Moreover, this early peak in aperiodic activity representation of spatial location occurs soon after stimulus onset regardless of the total stimulus presentation time, suggesting that aperiodic activity encodes spatial location quickly and automatically once the stimulus has been presented. This representation is consistent with previous work in our lab by [Gao et al., (2017)](https://www.sciencedirect.com/science/article/pii/S1053811917305621?via%3Dihub) that showed that the aperiodic exponent reflects the relative balance of excitation and inhibition in the underlying neural populations, such that a surge of excitation in the underlying neural populations necessary to encode the stimulus features during stimulus presentation is reflected in detectable changes in the EEG aperiodic exponent. The representation of spatial location by the aperiodic exponent was significantly greater in the first 400 ms following stimulus presentation than when location labels were shuffled:
{: .text-justify}
<img src="/assets/images/exp_ctf_slope_paired_ttest.png" width="700">{: .align-center}

**Conclusion**: We confirmed previous findings that the topography of alpha oscillatory activity represents spatial location in working memory, deconfounding these effects from changes in aperiodic activity. Furthermore, we discovered that the aperiodic exponent represents spatial location during the first 400 ms after stimulus presentation. Together, these findings highlight the utility of sliding-window spectral parameterization to decouple and characterize two, time-varying, physiologically distinct neural mechanisms for encoding and working memory.
{: .text-justify}

- **Manuscript**
    - **Bender A.**, Zhao, C., Awh E., Vogel E., Voytek B., Distinct, time-varying roles for aperiodic and alpha oscillatory activity in working memory. *In preparation*.
- **Presentation**
    - **Bender, A.**, Voytek, B. Decoding spatial location from aperiodic and alpha oscillatory activity in working memory. *Society for Neuroscience*; 2023, November 13; San Diego, CA. ([presentation](/files/SfN2023Presentation.pdf))

## Classification of autism spectrum disorder from structural and functional magnetic resonance imaging using machine learning

**Background**: Machine learning and deep neural networks have shown promise in helping to diagnose diseases such as Alzheimer’s disease from neuroimaging datasets. Given the utility machine learning has already shown in diagnosing diseases, here we aimed to develop machine learning classifiers, including a deep residual neural network called ASDNet, that can classify autism spectrum disorder (ASD) from neuroimaging data. Because early diagnosis and early treatment can improve quality of life for individuals with ASD and their families and current diagnostic measures can only be used with children 12 months and older, machine learning shows promise for enabling earlier diagnosis and treatment of ASD. 
{: .text-justify}

<img src="/assets/images/ASDNet.png" width="170">{: .align-right}
**Methods**: We used the following publicly available preprocessed data from the Autism Brain Imaging Data Exchange (ABIDE) ([Di Martino et al., 2014](https://www.nature.com/articles/mp201378)): (1) T<sub>1</sub>-weighted structural magnetic resonance imaging (sMRI), (2) 3D volumes of voxel-wise cortical thickness, and (3) mean functional activation volumes from 531 individuals with ASD and 570 typically developing individuals.
{: .text-justify}

We created nearest neighbor, Naïve Bayes, and linear discriminant analysis (LDA) classifiers to diagnose ASD on the first 1100 principal components for each individual imaging modality (structural, cortical thickness, and functional). We also trained classifiers for each combination of imaging modalities (e.g., structural + functional). We used 8-fold cross-validation to validate classifier performance. In addition, we trained a custom-built GPU implementation of a deep 3D residual neural network in TensorFlow to perform the classification, following a similiar architecture to a network used to diagnose Alzheimer's disease from neuroimaging data ([Yang et al., 2018](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6371279/)). The complete architecture of ASDNet is shown to the right.
{: .text-justify}

**Results**: The classification accuracy for each classifier on the structural, cortical thickness, and function volumes is shown below:
<img src="/assets/images/classifier_performance.png" width="700">{: .align-center}

LDA had the best average classification accuracy across the three types of imaging out of the four classification methods, with ASDNet classifying structural and cortical thickness volumes with similar accuracy and performing worse on the functional volumes than LDA. Putting data from two imaging types together into an ensemble increased classification accuracy with all three classifiers it was attempted with (LDA, Naïve-Bayes, and nearest neighbors). The ensemble containing all three imaging types performed the best. Finally, use of cortical thickness volumes and functional volumes led to higher classification than use of structural MRI, although the pairwise combinations of imaging types as an ensemble led to similar classification accuracies for all three pairwise combinations.  
{: .text-justify}

We further showed through [distance to bound analysis](https://www.frontiersin.org/articles/10.3389/fnins.2016.00190/full) that structural, cortical thickness, and functional differences extracted by classifiers were significantly correlated to Autism Diagnostic Observation Schedule (ADOS) ([Lord et al., 2000](https://pubmed.ncbi.nlm.nih.gov/11055457/)) scores, a common behavioral assessment for ASD that is considered to have state-of-the-art sensitivity ([Randall et al., 2018](https://pubmed.ncbi.nlm.nih.gov/30075057/)).
{: .text-justify}

**Conclusion**: The classification achieved was significantly above chance, but far below that which would be required for any utility in early diagnostics of ASD. There are a variety of possible causes—relatively raw neuroimaging data, limited training data (~1000 subjects of high-dimensional data is nothing compared to the training sets used on most deep ANNs), insufficient hyperparameter tuning—to name a few, and I would have approached this problem differently had I continued this research in graduate school. Nonetheless, I cultivated many technical skills that have benefitted my graduate career immensely and machine learning still shows great potential as an early diagnostic tool to reduce the financial, psychosocial, and developmental burden of ASD on our society despite our inability to demonstrate so with this particular work.
{: .text-justify}

- **Honors Thesis** (Awarded *Highest Honors in Neuroscience*)
    - **Bender, A.**, Tovar, D.A., Wallace, M.T. Classification of Autism Spectrum Disorder Using Machine Learning. *Honors Thesis Defense*; 2019, April 18; Nashville, TN. ([paper](/files/HonorsThesis.pdf), [presentation](/files/HonorsThesisPresentation.pdf))
- **Presentations**
    - **Bender, A.**, Tovar, D.A., Ramachandran, R., Wallace, M.T. ASDNet: Classification of autism from MRI images using residual neural networks. *Vanderbilt Translational Research Forum*; 2018, October 26; Nashville, TN. ([poster](/files/TranslationalResearchForumPoster.pdf))
    - **Bender, A.**, Tovar, D.A., Ramachandran, R., Wallace, M.T. ASDNet: Classification of autism from MRI images using residual neural networks. *Summer Student Poster Presentations: Vanderbilt Undergraduate Research Fair*; 2018, September 27; Nashville, TN. ([poster](/files/TranslationalResearchForumPoster.pdf))
{: .text-justify}