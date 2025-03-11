# [CycleSGAN: A cycle-consistent and semantics-preserving generative adversarial network for unpaired MR-to-CT image synthesis](https://doi.org/10.1016/j.compmedimag.2024.102431)

## [[Runze Wang]]; [[Alexander F. Heimann]]; [[Moritz Tannast]] et al.

## Abstract
CycleGAN has been leveraged to synthesize a CT image from an available MR image after trained on unpaired data. Due to the lack of direct constraints between the synthetic and the input images, CycleGAN cannot guarantee structural consistency and often generates inaccurate mappings that shift the anatomy, which is highly undesirable for downstream clinical applications such as MRI-guided radiotherapy treatment planning and PET/MRI attenuation correction. In this paper, we propose a cycle-consistent and semantics-preserving generative adversarial network, referred as CycleSGAN, for unpaired MR-to-CT image synthesis. Our design features a novel and generic way to incorporate semantic information into CycleGAN. This is done by designing a pair of three-player games within the CycleGAN framework where each three-player game consists of one generator and two discriminators to formulate two distinct types of adversarial learning: appearance adversarial learning and structure adversarial learning. These two types of adversarial learning are alternately trained to ensure both realistic image synthesis and semantic structure preservation. Results on unpaired hip MR-to-CT image synthesis show that our method produces better synthetic CT images in both accuracy and visual quality as compared to other state-of-the-art (SOTA) unpaired MR-to-CT image synthesis methods.

## Key concepts
#claim/adversarial_learning; #adversarial_learning; #computed_tomography; #finding/synthesis; #synthesis

## Quote
> The study presents a novel approach, CycleSGAN, for unpaired MR-to-CT image synthesis, which incorporates semantic information into CycleGAN using a pair of three-player games, resulting in superior performance compared to state-of-the-art methods.


## Figures
![Figure 1. A schematic illustration of our proposed CycleSGAN framework. Blue and red colored blocks and arrows show parts related with MR and CT domains, respectively. Solid arrows denote the data flow and yellow blocks represent the loss functions used in the training process](https://x.scholarcy.com/images/0/CycleSGAN__A_cycle-consistent_and_semantics-preserving_generative_adversarial_network_for_unpaired_MR-to-CT_image_synthesis/img-Figure-000.webp)
![Figure 2. Network architecture for generators and discriminators used in the proposed CycleSGAN. We denote 3D instance normalization, 3D convolution, 3D transpose-convolution and LeakyReLU as IN3D, Conv3D, TConv3D and LReLU, respectively](https://x.scholarcy.com/images/0/CycleSGAN__A_cycle-consistent_and_semantics-preserving_generative_adversarial_network_for_unpaired_MR-to-CT_image_synthesis/img-Figure-001.webp)
![Figure 3. Qualitative results of different image translation methods when evaluated on a testing MR image (the 1st row) from the Fribourg dataset. From the 2nd row to the 6th row, we show the qualitative results of MUNIT, 3D-CycleGAN, 3D MINDCycle, 3D-CycleSeg and CycleSGAN, respectively. Results are visualized in three views: axial view (the left three columns), saggital view (the middle three columns), and coronal view (the right three columns). In each view, the first column presents the CT images synthesized by different methods; In the second column, the ground truth annotation of the input MR image is overlaid onto the synthetic CT images, where red and green color corresponds to the pelvis and the proximal femur, respectively. The third column shows a zoomed view of a local region in the second column](https://x.scholarcy.com/images/0/CycleSGAN__A_cycle-consistent_and_semantics-preserving_generative_adversarial_network_for_unpaired_MR-to-CT_image_synthesis/img-Figure-002.webp)
![Figure 4. Qualitative results of the analytical ablation study on the Fribourg dataset. Top row: an input testing MR image with the corresponding annotation; 2nd–4th rows: results obtained when different types of discriminators were used for training](https://x.scholarcy.com/images/0/CycleSGAN__A_cycle-consistent_and_semantics-preserving_generative_adversarial_network_for_unpaired_MR-to-CT_image_synthesis/img-Figure-003.webp)
## Key points
- The limitations of the study include the requirement of label supervisions to train the model, although the model can take an MR image as input to generate a synthetic CT image without the need of annotation labels at testing stage.
- The study acknowledges that the evaluation was only conducted on hip MR-CT datasets, and further investigation is required to determine whether similar performance can be obtained on datasets of different anatomical regions or acquired with different imaging protocols. The study also acknowledges that CycleSGAN requires label supervisions to train a model for unpaired MR-to-CT image synthesis.
- The study acknowledged the limitations of the present study, including the evaluation being only conducted on hip MR-CT datasets and the requirement of label supervision to train a model.
- The future work includes further investigation of the influence of different backbone generators and discriminators on the performance of CycleSGAN, as well as the exploration of using automatically generated annotations instead of manual annotations.
- The study suggests that CycleSGAN can be applied to datasets of other anatomical regions, such as brain and abdomen. The study also suggests that CycleSGAN can be used for clinical applications, such as radiation treatment planning and multimodal image registration.
- The study suggested that further investigation is required to determine whether similar performance can be obtained when CycleSGAN is applied to datasets of different anatomical regions or to datasets acquired with different imaging protocols.
- The practical applications of the study include the use of synthetic CT images generated by CycleSGAN for radiotherapy treatment planning and positron emission tomography (PET) attenuation correction, which can help to reduce the radiation dose to patients and improve the accuracy of treatment planning.
- The study suggests that CycleSGAN has potential practical applications in clinical settings, including radiation treatment planning and multimodal image registration. The study also suggests that CycleSGAN can be used to facilitate the development of MRI-based radiation treatment planning.
- The study highlighted the importance of the approach for down-stream tasks such as treatment planning and attenuation correction.


## Summary

### Snapshot
The study presents a novel approach, CycleSGAN, for unpaired MR-to-CT image synthesis, which incorporates semantic information into CycleGAN using a pair of three-player games, resulting in superior performance compared to state-of-the-art methods.

### Key findings
The key findings of the study include the development of a novel CycleSGAN method that outperforms other state-of-the-art methods in terms of accuracy and visual quality, and the demonstration that only a limited number of semantic annotations are needed to train the structure adversarial learning.
The study finds that CycleSGAN outperforms multiple state-of-the-art methods, including 3D-CycleGAN, 3D-MINDCycle, and MUNIT, in terms of segmentation score and image-based metrics. The study also finds that CycleSGAN requires limited supervision, with 10 annotations sufficient to learn the label-conditional image generation.
MUNIT exhibited the worst segmentation score (S-score) results while 3D-CycleGAN, which operated on a volume-level rather than on a slice-level as in MUNIT, demonstrated an average Dice Overlap Coefficient (DOC) increase of 6.61% and an average Average Symmetric Surface Distance (ASSD) decrease of 0.48 mm when compared to MUNIT
We developed and validated a new unpaired MR-to-CT image synthesis method
Our approach outperformed multiple state-of-theart methods and demonstrated the value of the three-player game in ensuring both realistic image synthesis and semantic structure preservation, which were of importance for down-stream tasks such as treatment planning and attenuation correction

### Objectives
The objective of the study is to propose a cycle-consistent and semantics-preserving generative adversarial network for unpaired MR-to-CT image synthesis, which can generate synthetic CT images that are both realistic and structurally consistent with the input MR images.

### Methods
The method used in the study is based on the CycleGAN framework, with a pair of three-player games that consist of one generator and two discriminators to formulate two distinct types of adversarial learning: appearance adversarial learning and structure adversarial learning.
The study uses a pair of three-player games within the CycleGAN framework, with each game consisting of one generator and two discriminators. The study evaluates the performance of CycleSGAN using segmentation score and image-based metrics, including DOC, ASSD, MAE, PSNR, and SSIM.
The study used a cycle-consistent and semantics-preserving generative adversarial network, referred to as CycleSGAN, which consists of a pair of three-player games within the CycleGAN framework.

### Results
The results of the study show that the proposed CycleSGAN method outperforms other state-of-the-art methods in terms of accuracy and visual quality, with an increase of 11.28% average DOC and a decrease of 0.98 mm average ASSD when compared to the second-best method.
The study finds that CycleSGAN achieves the best results in terms of DOC and ASSD, with an average DOC of 95.13% and an average ASSD of 0.45 mm. The study also finds that CycleSGAN outperforms other state-of-the-art methods, including 3D-CycleGAN, 3D-MINDCycle, and MUNIT.
The results of the study showed that CycleSGAN outperformed multiple state-of-the-art methods, with the best results obtained when all discriminators were used.

### Conclusions
The conclusions of the study are that the proposed CycleSGAN method is effective for unpaired MR-to-CT image synthesis, and that it can generate synthetic CT images that are both realistic and structurally consistent with the input MR images.
The study concludes that CycleSGAN is a superior approach for unpaired MR-to-CT image synthesis, outperforming state-of-the-art methods. The study also concludes that CycleSGAN requires limited supervision, with 10 annotations sufficient to learn the label-conditional image generation.
The study concluded that CycleSGAN is a novel and effective approach for unpaired MR-to-CT image synthesis, which can ensure both realistic image synthesis and semantic structure preservation with limited label supervision.

## Data analysis
- #method/t_tests

## Findings
- MUNIT exhibited the worst <a title="segmentation score" href="#" class="keyword">S-score</a> results while 3D-CycleGAN, <mark class="fact">which operated on a volume-level</mark> rather than on a slice-level as in MUNIT, demonstrated an average <a title="Dice Overlap Coefficient" href="#" class="keyword">DOC</a> increase of 6.61% and an average <a title="Average Symmetric Surface Distance" href="#" class="keyword">ASSD</a> decrease of 0.48 mm when compared to MUNIT
- CycleSGAN, which only utilized 10 annotations from each modality, achieved the best results in terms of both <a title="Dice Overlap Coefficient" href="#" class="keyword">DOC</a> and <a title="Average Symmetric Surface Distance" href="#" class="keyword">ASSD</a>, with an increase of 11.28% average <a title="Dice Overlap Coefficient" href="#" class="keyword">DOC</a> and a decrease of 0.98 mm average <a title="Average Symmetric Surface Distance" href="#" class="keyword">ASSD</a> when compared to the secondbest method (3D-MINDCycle)
- When only the structure discriminators were used, we observed improved results with an average <a title="Dice Overlap Coefficient" href="#" class="keyword">DOC</a> of 91.84% and an average <a title="Average Symmetric Surface Distance" href="#" class="keyword">ASSD</a> of 0.73 mm
- <mark class="claim">Our approach outperformed multiple state-of-theart methods and demonstrated the value of the three-player game in ensuring both realistic image <a title="synthesis" href="https://en.wikipedia.org/wiki/synthesis" class="keyword">synthesis</a> and semantic structure preservation, <mark class="fact">which were of importance for down-stream tasks</mark> such as treatment planning and attenuation correction</mark>

##  Builds on previous research
- Similarly, after training, we extracted 2D slices along the coronal view from the 3D testing MR images, which were then fed to the trained MUNIT model to get the synthetic CT slices. ==Subsequently, we placed the synthetic 2D slices back into the original 3D space for a volume-level evaluation==; (2) 3D-CycleGAN: CycleGAN ([^Zhu_et+al_2017_a]) is another unsupervised image-to-image translation method based on cycle-consistency.
- We thus chose to use ResNet as the backbone network. In ==this study, we investigated two different backbone generators==: ResNet ([^He_et+al_2016_a]) (referred to as Ours) and U-Net ([^Ronneberger_et+al_2015_a]) (referred to as Ours (U-Net)).

## Differs from previous work
- Thus, [^Cai_et+al_2019_a]) proposed to add simultaneously trained a target-domain segmentor to enhance shape-consistency. ==However, a careful analysis reveals that the same criticism that they raise for cycle-consistency can also be applied here, i==.e., when the translated image with geometric distortion is fed to the target-domain segmentor, the distortion can be recovered without provoking any penalty in the segmentation cost, leading to sub-optimal synthesized images.
- To address the intrinsic ambiguity of cycle-==consistent reconstruction with respect to geometric transformation in CycleGAN, other works introduced shape consistency ([^Cai_et+al_2019_a]; [^Phan_et+al_2023_a]), anatomy regularization ([^Chen_et+al_2020_a]), structural similarity ([^Hiasa_et+al_2018_a]), structure consistency ([^Yang_et+al_2020_a]) and deformation correction layers ([^Wang_et+al_2021_a]). However, a careful analysis reveals that the same criticism that they raise for cycle-consistency can also be applied here, i==.e, when the translated image with geometric distortion is fed to the target-domain segmentor, the distortion can be recovered without provoking any penalty in the segmentation cost, leading to sub-optimal synthesized images.

## Counterpoint to earlier claims
- The joint distribution is represented as a channel-wise concatenation of images and their corresponding multi-label annotation masks where each voxel has a distinct label. ==Unlike the conventional CycleGAN== ([^Zhu_et+al_2017_a]), which is restricted to the two-player framework, CycleSGAN adopts a three-player game in each domain.

## Limitations
- The limitations of the study include the requirement of label supervisions to train the model, although the model can take an MR image as input to generate a synthetic CT image without the need of annotation labels at testing stage.
- The study acknowledges that the evaluation was only conducted on hip MR-CT datasets, and further investigation is required to determine whether similar performance can be obtained on datasets of different anatomical regions or acquired with different imaging protocols. The study also acknowledges that CycleSGAN requires label supervisions to train a model for unpaired MR-to-CT image synthesis.
- The study acknowledged the limitations of the present study, including the evaluation being only conducted on hip MR-CT datasets and the requirement of label supervision to train a model.

## Future work
- The future work includes further investigation of the influence of different backbone generators and discriminators on the performance of CycleSGAN, as well as the exploration of using automatically generated annotations instead of manual annotations.
- The study suggests that CycleSGAN can be applied to datasets of other anatomical regions, such as brain and abdomen. The study also suggests that CycleSGAN can be used for clinical applications, such as radiation treatment planning and multimodal image registration.
- The study suggested that further investigation is required to determine whether similar performance can be obtained when CycleSGAN is applied to datasets of different anatomical regions or to datasets acquired with different imaging protocols.


