---
permalink: /research/
title: "Research Projects"
---
## Graduate research

### Resting-state is not enough: alpha and mu rhythms change shape across development, but lack diagnostic sensitivity

This research is posted on [bioRxiv](https://www.biorxiv.org/content/10.1101/2023.10.13.562301v1.full) and under review at the *Journal of Neuroscience*! The analysis code is available on [GitHub](https://github.com/nschawor/eeg-mu-alpha-development).
{: .text-justify}

Alpha rhythms in occipital cortex and mu rhythms in sensorimotor cortex are two of the most prominent rhythms in the human brain. They have similiar characteristic frequencies in the canonical alpha band (8-12 Hz) and serve important functions in gating modality-specific information.
{: .text-justify}

![](/assets/images/alpha_mu_traces.png){: .align-center}

Both alpha-band rhythms have been implicated in autism spectrum disorder (ASD) and attention-deficit hyperactivity disorder (ADHD) in disorder-relevant tasks (e.g., social encoding tasks for ASD and attention-demanding tasks for ADHD). In this project, we investigated whether these rhythms could serve as biomarkers for these developmental disorders in resting-state electroencephalography (EEG). Such biomarkers would greatly aid in developing effective early diagnostic tools for ASD and ADHD.
{: .text-justify}

We used an [openly available developmental dataset](http://fcon_1000.projects.nitrc.org/indi/cmi_healthy_brain_network/index.html) of resting-state EEG recordings from nearly 3000 children (ages 5-18) from the [Child Mind Institute](https://childmind.org/) published by [Alexander and colleagues (2017)](https://www.nature.com/articles/sdata2017181). We isolated high-fidelity alpha and mu rhythms from these recordings using an computationally efficient integration of [spectral parameterization](https://www.nature.com/articles/s41593-020-00744-x), [spatial filters](https://www.sciencedirect.com/science/article/pii/S1053811911000930), and source localization. We then used burst detection and [waveform shape analysis](https://journals.physiology.org/doi/full/10.1152/jn.00273.2019) to characterized the waveform shape of these isolated alpha and mu rhythms:
{: .text-justify}

![](/assets/images/waveform_feats.png){: .align-center}

First, we demonstrated that alpha rhythms are lower frequency, less asymmetrical, and higher amplitude than mu rhythms. These results quantifiably replicate qualitative differences in alpha and mu at an unprecendented scale:
{: .text-justify}

![](/assets/images/alpha_vs_mu_feats.png){: .align-center}

Next, we discovered that alpha and mu rhythms are significantly different at age five and change differently across development:
{: .text-justify}

![](/assets/images/fig3_age.png){: .align-center}

Finally, we showed that neither alpha nor mu rhythms are sensitive biomarkers in resting-state EEG, implying sensitive EEG biomarkers for ASD and ADHD may require deficit-specific task operalization:
{: .text-justify}

![](/assets/images/fig4_diagnosis.png){: .align-center}


### Decoding spatial location from aperiodic and alpha oscillatory activity

## Undergraduate research

### Classification of autism spectrum disorder using machine learning