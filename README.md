# QuasarSelection
Repository for exploring machine learning algorithms for quasar selection/classification.

SpIESHighzCandidateSelection.ipynb
is a notebook that takes the training sets that we used for KDE
selection of 3.5<z<5 quasars from SDSS+SpIES data.  KDE was about 78%
complete and 97% efficient.  The sklearn algorithms were about the
same, which gives confidence that the sample is not highly
contaminated and that we could replace our usage of the proprietary
KDE algorithm with public algorithms from sklearn.