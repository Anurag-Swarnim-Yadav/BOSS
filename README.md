# BOSS : A dataset to train ML-based systems to repair programs with out-of-bounds write flaws

ABSTRACT: C and C++ are widely-used, mature programming languages.
They have been extensively used in development of projects such as Linux, Windows, YouTube, Adobe, Firefox, and Google Chrome.
Due to poor memory safety, C and C++ programs are vulnerable to security attacks as are programs in languages that depend on C/C++ library code.
As per the Common Weakness Enumeration (CWE), out-of-bounds (OOB) write in C/C++ programs topped the list of the 25 most dangerous software weakness in 2021 and 2022.
Fixing OOB write at the source code level still requires human experts.
This is a tedious task that may result in erroneous programs. 
In this paper we propose a technique to create a data set of corresponding flawed and correct programs that can be used to perform supervised training of deep-learning models to automate the process of detecting and patching OOB writes. 
The proposed technique has two elements: collecting a set of C/C++ programs from online sources (correct programs) and injecting OOB write errors into them, thus yielding a set of corresponding flawed programs.
In this paper we focus on four main flaws associated with OOB writes: faulty access, faulty declaration, faulty guard in loops, and faulty usage of memory-write APIs.
We have found that popular fault localization tools can not localize complicated bugs in our buffer overflow sample set (BOSS).
In addition, the current state-of-the-art machine learning security flaw repair tool could not repair any of the bugs in a randomly selected set of BOSS samples and, in some cases, generated out-of-bound writes as suggested patches.
These results lead us to conclude that the bugs injected by our tool are significant and our dataset is useful for training neural program repair models.
We also propose two data-augmentation techniques to overcome problems associated with limited-size corpora.
