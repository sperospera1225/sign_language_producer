# Progressive Transformers for End-to-End Sign Language Production

Source code for "Progressive Transformers for End-to-End Sign Language Production" (Ben Saunders, Necati Cihan Camgoz, Richard Bowden - ECCV 2020) 

# Usage

To run, start __main__.py with arguments "train" and ".\Configs\Base.yaml":

`python __main__.py train ./Configs/Base.yaml` 

Back Translation model created from https://github.com/neccam/slt. Back Translation evaluation code coming soon.

# Data

Phoenix14T data can be downloaded from https://www-i6.informatik.rwth-aachen.de/~koller/RWTH-PHOENIX-2014-T/ and skeleton joints can be extracted using OpenPose at  https://github.com/CMU-Perceptual-Computing-Lab/openpose

Prepare Phoenix14T (or other sign language dataset) data as .txt files for .skel, .gloss, .txt and .files. Data format should be parallel .txt files for "src", "trg" and "files", with each line representing a new sequence. The "src" file contains source sentences, with each line representing new sentence. The "trg" file contains skeleton data of each frame, with a space separating frames. Each frame contains 150 joint values and a subsequent counter value, all separated by a space. Each sequence should be separated with a new line. If your data contains 150 joints per frame, please ensure that trg_size is set to 150 in the config file. The "files" file should contain the name of each sequence on a new line. 
Examples can be found in /Data/tmp. Data path must be specified in config file.


# Reference

If you use this code in your research, please cite the following [paper](https://arxiv.org/abs/2004.14874):

```
@article{saunders2020progressive,
  title={Progressive Transformers for End-to-End Sign Language Production},
  author={Saunders, Ben and Camgoz, Necati Cihan and Bowden, Richard},
  journal={arXiv preprint arXiv:2004.14874},
  year={2020}
}
```

## Acknowledgements
<sub>This work received funding from the SNSF Sinergia project 'SMILE' (CRSII2 160811), the European Union's Horizon2020 research and innovation programme under grant agreement no. 762021 'Content4All' and the EPSRC project 'ExTOL' (EP/R03298X/1). This work reflects only the authors view and the Commission is not responsible for any use that may be made of the information it contains. We would also like to thank NVIDIA Corporation for their GPU grant. </sub>
