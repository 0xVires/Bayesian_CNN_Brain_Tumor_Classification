# Bayesian CNN - Brain Tumor Classification

Baysian Deep Learning with fast.ai, a project by Pascal Weber, M.Sc. and Paul Windisch, MD. in collaboration with the European CyberKnife Center in Munich.

A pretrained convolutional neural network (resnet50) was used as part of a transfer
learning approach and retrained on MRI slices belonging to one of three classes: First,
healthy MRI slices from the IXI dataset. Second, slices containing vestibular schwannoma
(VS) a benign tumor arising from Schwann cells of the vestibulocochlear nerve provided by
the European CyberKnife Center in Munich. Third, slices containing glioblastoma, a
highly malignant WHO grade IV tumor from The Cancer Genome Atlas (TCGA) dataset
provided as part of The Cancer Imaging Archive (TCIA).

1023 healthy, 388 VS and 336 GBM slices were used for training. Validation was performed on a set containing 188 normal, 91 VS and 87 GBM slices.

The model achieved a categorical accuracy of 0.93. Creating a bayesian neural network and allowing the model to make a prediction only if it was very certain to make a correct one (mean probability >= 0.90), further increased the categorical accuracy to 0.97. For 47 of the 366 slices of the validation dataset, the model was unable to make a prediction with sufficient confidence.
