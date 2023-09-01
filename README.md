![DNAnalyzer-modified](https://user-images.githubusercontent.com/96280466/221687615-698969a1-8d39-4278-aa92-8f713625f165.png)


<p align=center><img src="https://img.shields.io/badge/copyright-2023-blue" alt="Copyright"> <img src="https://img.shields.io/github/v/release/VERISIMILITUDEX/DNAnalyzer" alt="Releases"> <img src="https://img.shields.io/github/repo-size/VerisimilitudeX/DNAnalyzer" alt="Repository Size"> <img src="https://hits.dwyl.com/verisimilitudeX/DNAnalyzer.svg?style=flat" alt="Hits Counter">  <img src="https://github.com/VerisimilitudeX/DNAnalyzer/actions/workflows/gradle.yml/badge.svg" alt=""> 
<a href="https://discord.gg/X3YCvGf2Ug"><img src="https://img.shields.io/discord/1033196198816915516" alt=""></a>
<a href="https://deepsource.io/gh/VerisimilitudeX/DNAnalyzer/?ref=repository-badge}"><img src="https://deepsource.io/gh/VerisimilitudeX/DNAnalyzer.svg/?label=active+issues&amp;show_trend=true&amp;token=9NBX3zsf0IZ3Nii3AApiX1Wa" alt="DeepSource" title="DeepSource"></a></p>

>Revolutionizing DNA analysis and making it accessible to all through innovative AI-powered analysis and interpretive tools.

<a href="https://www.producthunt.com/posts/dnanalyzer?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-dnanalyzer" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=401710&theme=dark" alt="DNAnalyzer - Revolutionizing&#0032;AI&#0045;powered&#0032;accessible&#0032;DNA&#0032;analysis | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

DNAnalyzer is a fiscally sponsored 501(c)(3) nonprofit organization (EIN: 81-2908499) dedicated to revolutionizing the field of DNA analysis. We aim to democratize access to DNA analysis tools for a deeper understanding of human health and disease and pushing the boundaries of what is possible in the field of genetics research to make a significant impact in the industry.

Our flagship product identifies protein-encoding sequences via recognizing start and stop codons, predicts high coverage regions, and locates promoter sequences and their associated regulatory sequences. It also provides a variety of other useful tools, such as a built-in DNA sequence editor, viewer, generator, and converter.

Researchers are working to extract valuable information from such software to better understand human health and disease. Currently, we have a Command-Line-Interface (CLI) and are working on a Graphical User Interface (GUI) that will enable physicians to quickly and more easily interact with the software, enabling them to identify genetic mutations that may cause disease.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=519909104&machine=largePremiumLinux&location=WestUs&skip_quickstart=true&geo=UsWest)

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Background](#background)
- [Features](#features)
- [Quick Introduction to DNA](#quick-introduction-to-dna)
  - [DNA](#dna)
  - [Databases](#databases)
- [Getting Started](#getting-started)
  - [System Requirements](#system-requirements)
  - [Build \& Run](#build--run)
  - [Usage](#usage)
    - [Executable](#executable)
    - [Arguments](#arguments)
  - [Example](#example)
    - [Gradle Run](#gradle-run)
    - [GUI](#gui)
  - [DNAnalyzer \& Java Download](#dnanalyzer--java-download)
  - [Java installation](#java-installation)
  - [Usage](#usage-1)
    - [Executable](#executable-1)
    - [Arguments](#arguments-1)
  - [Example](#example-1)
    - [Gradle Run](#gradle-run-1)
    - [GUI](#gui-1)
    - [Available Commands](#available-commands)
- [Future Support and Improvements](#future-support-and-improvements)
  - [Optimized SQL Database for Genomic Data](#optimized-sql-database-for-genomic-data)
  - [Improved Neural Network for Genotyped Data](#improved-neural-network-for-genotyped-data)
  - [DIAMOND Implementation, a BLAST fork](#diamond-implementation-a-blast-fork)
- [Citations](#citations)
- [Contributing](#contributing)
- [Terms of Use](#terms-of-use)
      - [Copyright © Piyush Acharya 2023. DNAnalyzer is a fiscally sponsored 501(c)(3) nonprofit (EIN: 81-2908499). Licensed under the MIT License.](#copyright--piyush-acharya-2023-dnanalyzer-is-a-fiscally-sponsored-501c3-nonprofit-ein-81-2908499-licensed-under-the-mit-license)


## <a name="background"></a>Background

The human genome is composed of over 3 billion base pairs, making human analysis nearly impossible. Consequently, using powerful computational and statistical methods to decode the functional information hidden in DNA sequences are necessary. The genome is also extremely intricate and contains a plethora of data, which need to be organized and converted into analyzable data appropriately. Current analytical tools and software make it arduous for both geneticists and physicians to do so, thus restricting them from acquiring crucial information to better understand humans. `[1]`

## <a name="features"></a>Features

* Start and stop codons
  * Indicate the start and stop of a protein. There are 20 different amino acids. A protein consists of one or more chains of amino acids (called polypeptides) whose sequence is encoded in a gene. `[2]`
* High coverage regions
  * Promoter sequences in the genome that code for proteins have a relatively high proportion of guanine and cytosine nucleotides to the 4 nucleotide bases (45-60% GC-content). Such CpG islands are likely to reveal important information about the genome. `[3]`
* Neurodevelopmental Disorders
  * A group of disorders, usually characterized by longer genes, that affect the development of the brain and nervous
                        system. These disorders are caused by genetic mutations that affect the development of the
                        brain and nervous system. These disorders include autism, attention deficit hyperactivity
                        disorder (ADHD), and schizophrenia. `[4]`
* Core promoter elements
  * Promoter sequences are short DNA sequences that are located upstream of a gene and are responsible for initiating transcription (e.g. BRE, TATA, INR, and DPE). `[5]`
* FASTA files (.fa)
  * Supports multi-line and single-line FASTA database files. Files can either be uploaded or linked to from the web. `[7]`
* CLI
  * The Methionine command-line interface (abbreviated as Met CLI) is a unified tool for running DNAnalyzer services from the command-line. The CLI is a powerful tool for using DNAnalyzer services and scripting a sequence of commands to execute. You can currently access all the core features present in DNAnalyzer without having to log in, although account support will be implemented soon. To get more information on Met CLI installation and currently supported commands, refer to Met CLI GitHub repository.
* GUI
  * A cross-platform GUI-based application that performs the algorithms implemented in the software. The Met CLI continues to be the best way to run the program. Currently, the following operations are supported:
    * Set name of DNA file to analyze
    * Set minimum and maximum number of reading frames
    * Run analysis
  * More features will be added in the future.

## <a name="quick-introduction-to-dna"></a>Quick Introduction to DNA

### <a name="dna"></a>DNA

DNA, present in most cells of the body, holds the blueprint for creating over 200 distinct cell types. Like a programming language, it is exclusive to living organisms. With the aid of Artificial Intelligence and Machine Learning, we can decode and comprehend DNA, leading to potentially life-saving discoveries and valuable insights.

### <a name="databases"></a>Databases

A DNA database is crucial for interpreting DNA sequences. By leveraging machine learning, predictions can be made on previously unseen DNA sequences. This is the foundation on which current DNA analysis programs operate.

## <a name="getting-started"></a>Getting Started

A [video tutorial](https://youtu.be/dOwkInn6eDw) covering the instructions below is also available.

### <a name="system-requirements"></a>System Requirements

* JDK [17](https://www.oracle.com/java/technologies/downloads/#jdk17-windows)+
   * A `JAVA_HOME` environment variable pointing to your JDK, or the Java executable in your PATH
* [Gradle](https://gradle.org/install/) (included)

### <a name="build-run"></a>Build & Run

The easiest way to run the program on Windows is by using the executable file located in the [releases](https://github.com/VerisimilitudeX/DNAnalyzer/releases/latest) section to install the program, build gradle and run the GUI.

* We use [Gradle](https://gradle.org) for building. The Gradle wrapper takes care of downloading dependencies, testing, compiling, linking, and packaging the code.
<details>

<summary>Windows</summary>

The easiest way to run the program on Windows is by using the executable file located in the [releases](https://github.com/VerisimilitudeX/DNAnalyzer/releases/latest) section to install the program, build gradle and run the GUI.

```pwsh
.\gradlew build
```

### <a name="usage"></a>Usage

```pwsh
<executable> <arguments>
```

#### <a name="executable"></a>Executable

```pwsh
java -jar build/libs/DNAnalyzer.jar
```

#### <a name="arguments"></a>Arguments

DNAnalyzer uses CLI arguments instead of `stdin`. For example, you can do:

```pwsh
assets/dna/random/dnalong.fa --amino=arg --min=16450 --max=520218 -r
```

### <a name="example"></a>Example

```pwsh
java -jar build/libs/DNAnalyzer.jar assets/dna/random/dnalong.fa --amino=ser --min=16450 --max=520218 -r
```

#### <a name="gradle-run"></a>Gradle Run

If you prefer, you can also run it directly from Gradle:

```pwsh
.\gradlew run --args="assets/dna/random/dnalong.fa --amino=ser --min=10 --max=100"
```

#### <a name="gui"></a>GUI

DNAnalyzer also comes with a (very basic) GUI; to start DNAnalyzer with the GUI, run:

```pwsh
.\gradlew run --args="--gui assets/dna/random/dnalong.fa"
```

Then:

* Enter the file name of the DNA file in the text field
* Set min and max
* Click analyze

* Note: Ensure you have Java [17](https://www.oracle.com/java/technologies/downloads/#java17) or higher installed and a `JAVA_HOME` path variable set for the program to function correctly!


The results of your analysis will be shown in the right pane.

</details>

<details>
      <summary>Linux & macOS</summary>


### <a name="features"></a>DNAnalyzer & Java Download

To run DNAnaylzer on Linux, you'll need to download the DNAnalyzer source code and download and install Java 17.

First, download the zip or tar.gz file from [DNAnalyzer releases](https://github.com/VerisimilitudeX/DNAnalyzer/releases/latest) and unzip it using the native utility. 

Then, download [Java 17](https://www.oracle.com/ca-en/java/technologies/downloads/#java17), find the download at https://www.oracle.com/ca-en/java/technologies/downloads/#java17, ensure you choose the Linux option and get the one for your correct processor architecture.

### Java installation

```bash
wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.tar.gz
```
Next, unzip it.

```bash
tar -xvzf jdk-17_linux-x64_bin.tar.gz
```
Then map the `JAVA_HOME` path. Fill it in with your JAVA directory where JAVA is unzipped.
```bash
export JAVA_HOME="{YOUR JAVA DIRECTORY HERE}/jdk-17.0.7" && export PATH=$JAVA_HOME/bin:$PATH
```
<details>
<summary>Example of a full path command.</summary>

```bash
export JAVA_HOME="/workspaces/DNAnalyzer/jdk-17.0.7"
```

</details>

```bash
./gradlew build
```
If you see `Task :compileJava FAILED`, the program cannot find your Java installation. You may need to export your JAVA_HOME path again.

### Usage

```bash
<executable> <arguments>
```

#### Executable

```pwsh
java -jar build/libs/DNAnalyzer.jar
```

#### Arguments

DNAnalyzer uses CLI arguments instead of `stdin`. For example, you can do:

```bash
assets/dna/random/dnalong.fa --amino=arg --min=16450 --max=520218 -r
```

### Example

```pwsh
java -jar build/libs/DNAnalyzer.jar assets/dna/random/dnalong.fa --amino=ser --min=16450 --max=520218 -r
```

#### Gradle Run

If you prefer, you can also run it directly from Gradle:

```pwsh
./gradlew run --args="assets/dna/random/dnalong.fa --amino=ser --min=10 --max=100"
```

#### GUI

DNAnalyzer also comes with a (very basic) GUI; to start DNAnalyzer with the GUI, run:

```pwsh
./gradlew run --args="--gui assets/dna/random/dnalong.fa"
```

Then:

* Enter the file name of the DNA file in the text field
* Set min and max
* Click analyze


The results of your analysis will be shown in the right pane.
</details>



#### Available Commands

```py


Usage: DNAnalyzer [-hrV] --amino=<aminoAcid> [--find=<proteinFile>]
                  [--max=<maxCount>] [--min=<minCount>] DNA
A program to analyze DNA sequences.
      DNA                    The FASTA file to be analyzed.
      --amino=<aminoAcid>    The amino acid representing the start of a gene.
      --find=<proteinFile>   The DNA sequence to be found within the FASTA file.
  -h, --help                 Show this help message and exit.
      --max=<maxCount>       The maximum count of the reading frame.
      --min=<minCount>       The minimum count of the reading frame.
  -r, --reverse              Reverse the DNA sequence before processing.
  -V, --version              Print version information and exit.
```

## Future Support and Improvements

### Optimized SQL Database for Genomic Data
 
Our goal is to find the best SQL database fork that can handle high performance and vertical scaling. We will store and query genomic data from thousands of species, including their genes and mutations. This will help us train our machine learning model more effectively.

### Improved Neural Network for Genotyped Data

This will bring the ability to use genotyped data from 3rd-party DNA testing services with our algorithm. In the future, to use this program, all you will need is a simple $99 DNA Test to be able to experience all the features of DNAnalyzer.

### DIAMOND Implementation, a BLAST fork

This will combine [DIAMOND](https://github.com/bbuchfink/diamond)'s performance advantage along with [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi")'s algorithm.

## Citations

View our in-line citations in the [Citations](docs/citations.md) document.

## Contributing

* [Contributing Guidelines](https://github.com/VerisimilitudeX/DNAnalyzer/blob/main/docs/Contribution%20Guideline/Contribution_Guideline.md)

* [How To Use Git](https://github.com/VerisimilitudeX/DNAnalyzer/blob/main/docs/contributing/CONTRIBUTING.md)

## Terms of Use

You are entirely responsible for the use of this application, including any and all activities that occur. While the DNAnalyzer Team strives to fix all major bugs that may be either reported by a user or discovered while debugging, they will not be held liable for any loss that the user may incur as a result of using this application, under any circumstances. For further inquiries, please contact the following email address: `contact@dnanalyzer.live`

If you use this software in your research, please consider citing it.

##### Copyright © Piyush Acharya 2023. DNAnalyzer is a fiscally sponsored 501(c)(3) nonprofit (EIN: 81-2908499). Licensed under the MIT License.
