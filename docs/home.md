![banner](banner.jpg)

***Training course in data analysis for genomic surveillance of African malaria vectors***

---

# Home

Welcome to this training course on data analysis for genomic surveillance of African malaria vectors, developed jointly by [MalariaGEN](https://www.malariagen.net) and [PAMCA](https://www.pamca.org). 


## Data access

Vector Observatory data are stored in Google Cloud Storage (GCS) in the US region. The current set-up requires users to request access and authenticate prior to accessing data. 

### Fair Usage

Vector Observatory data are currently stored in Google Cloud Storage (GCS) in the US region. Access to Vector Observatory data in Google Cloud is free for all users. However, large transfers of data outside of Google Cloud in the US region substantially increase our running costs, and so we ask users to adhere to the following fair usage policy. This will allow us to continue making the data freely available.

- **Data access from Google Colab -** If you are using Google Colab to access data, please check if your allocated virtual machine (VM) is within the US region. If not, please request a new VM by selecting “Runtime > Disconnect and delete runtime” from the Colab menu. 

Please note that we monitor data access logs to detect any unexpected large data transfers outside of Google Cloud in the US region, and may temporarily suspend access to users performing large data transfers. If we do suspend access, we will reach out to you to see if we can help optimise your data access.

### Data Access using Google Colab
To access data from the Vector Observatory, you will need to follow these steps:

#### Step 1. Make sure you have a Google Account

To allow us to configure data access permissions, you will need to provide us with an email address that is associated with a Google account. This could be a standard Google (i.e., Gmail) account, or alternatively it could be your work email address if your employer uses Google Workspace.

#### Step 2. Fill out the data access request form

Please fill out and submit the following form:

> [MalariaGEN cloud data access form](https://forms.gle/kCqistorZyxaU4LP7)

All requests for data access will be granted subject to verification checks and agreement to reasonable use. This is to ensure that the data resources remain accessible to everyone. Submitting this form will allow us to configure storage permissions and monitor storage for excessive network usage in future.

#### Step 3. Ensure you are using the latest version of the `malariagen_data` Python package

If you access data via the `malariagen_data` Python package, please upgrade to version 9.0 or higher. These versions will automatically use your authentication credentials when accessing data in Google Cloud.

#### Step 4. Ensure you are using the same Google Account you registered with

When you start running some code in Google Colab using the `malariagen_data` Python package, you will be asked to authenticate with your Google Account. Make sure that you use the same account you used during Steps 1 and 2 as you will not be able to use the `malariagen_data` Python package otherwise.

If you have any questions during the course of the workshop, feel free to ask your Teaching Assistant. 

If you have any questions outside of the course of the workshop, please contact us at: <support@malariagen.net>. 

More general details about Data Access can also be found on the [Vector Observatory website](https://malariagen.github.io/vector-data/vobs/vobs-data-access.html).

## Workshop programme

The course will consist of a series of workshops. The workshop programme is as follows:

* {doc}`workshop-1/about`
* {doc}`workshop-2/about`
* {doc}`workshop-3/about`
* {doc}`workshop-4/about`
* {doc}`workshop-5/about`
* {doc}`workshop-6/about`
* {doc}`workshop-7/about`
* {doc}`workshop-8/about`

## Context and motivation

The main motivation for this course, and for the ongoing work by MalariaGEN and PAMCA to develop capacity for *Anopheles* genomics, comes from the current situation in malaria control in Africa. This situation is well described in the [WHO World Malaria Report 2021](https://www.who.int/teams/global-malaria-programme/reports/world-malaria-report-2021) and in the [WHO Global Technical Strategy for Malaria 2016-2030](https://www.who.int/publications/i/item/9789240031357), but here are some key highlights.

### Progress towards malaria elimination has stalled

Between 2000 and 2015, the incidence and mortality rates for malaria in Africa reduced substantially, primarily due to the scaling up of vector control interventions using long-lasting insecticidal nets (LLINs) and indoor residual spraying (IRS). However, since 2015, neither incidence nor mortality have reduced substantially. 

### Biological threats to the efficacy of malaria vector control

The reasons for this stalling in progress are complex and not fully understood, but there are some current biological threats which are playing a part. In particular, resistance to insecticides is now widespread among the *Anopheles* mosquitoes which primarily transmit malaria in Africa. 

### Malaria vector control is changing

Malaria vector control programmes are responding to the threat of insecticide resistance by deploying new LLIN products which combine a pyrethroid insecticide either with the synergist piperonyl butoxide (pyrethroid-PBO LLINs) or with a second insecticide with a different mode of action (dual active LLINs). New IRS products are also being used which introduce insecticides not previously used in public health. These new LLIN and IRS products are already being deployed at scale.

These are the biggest changes in malaria control in at least a decade. These new vector control tools are known to be highly effective now, but we know from past experience that malaria vector populations will evolve new forms of resistance in response to these new selective pressures. Without a capability to detect these new biological threats, these new tools will not remain effective for long.

### Surveillance as a core intervention

Different countries face different malaria control challenges and threats, and the consensus is that there is no "one size fits all" approach to malaria vector control. Rather, vector control strategy needs to be tailored based on the local situation. Gathering of data on malaria vector populations (vector surveillance) thus has a key role to play in guiding decisions about vector control. In order to make this a reality, there is a need for strengthened national capacity to generate, analyse and use high-quality surveillance data.

### Genomic surveillance

Malaria vector surveillance needs to gather and integrate data from a variety of different sources. Vector genomics has a potential role to play in generating a new source of data, complementing and adding new insights when brought together with existing surveillance data on intervention coverage, vector bionomics and insecticide resistance phenotypes. 

To understand the potential value of vector genomic surveillance, a useful parallel is consider the role that genomic surveillance has played in responding to the COVID-19 pandemic. Although COVID-19 and malaria are very different diseases, they share something in common, which is that evolution leads to the emergence of new biological threats, and early detection of those threats can be valuable. In the case of COVID-19, early detection of highly-transmissible variants *alpha*, *delta* and *omicron* helped alert public health authorities that action needed to be taken sooner rather than later. 

By analogy, vector genomic surveillance could enable early detection of new insecticide resistance variants emerging in malaria vector populations in response to deployment of new LLIN or IRS products, which in turn could be beneficial in designing and adapting insecticide resistance management plans. 


## Intended audience

The primary audience for this training course is scientists and data analysts in African research groups and disease control programmes who are collaborating with MalariaGEN and PAMCA to generate *Anopheles* genomic data, and who want to use the data to answer questions about malaria vector surveillance. E.g., if vector control strategy has recently changed in a given country or region, what impact has that had on the local vector populations?

We hope this training course will also be useful to a broader audience including anyone who is interested in learning more about genomic data and how it could be used for vector surveillance.


## Learning objectives

At the end of this course, you will be able to:

1. Perform a range of analyses of *Anopheles* genomic data that are relevant to malaria vector surveillance.
1. Generate plots, tables and statistics that can be used in a surveillance report.
1. Interpret your results and explain to others what they mean.


## Prerequisites

This is a hands-on training course involving the analysis of real genetic data. To follow this course you will need to have some prior experience of data analysis using a programming language such as Python, R, Julia, Matlab or Stata. The practical exercises in each workshop will use the Python programming language, and some prior experience of Python will be advantageous, but is not required.

During the practical sessions in each workshop we will use [Google Colaboratory](https://colab.research.google.com/) (a.k.a. Colab), which is an interactive cloud computing service provided for free by Google. In order to use Colab you will need to have a Google user account. If you do not already have a Google user account, please make sure to create one before you start the course.
