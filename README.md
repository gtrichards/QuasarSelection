# QuasarSelection

Repository for exploring machine learning algorithms for quasar
selection/classification.  These are intended for analysis of
SDSS+SpIES data, but can serve as an introduction for analysis of
other data sets (e.g., DES, LSST, etc.) for those looking for a
template to follow.  These are largely "sand boxes", so apologies if
they aren't fully coherent.  Though I have gone through them to try to
make sure that they have some longer-term value.

`SpIESHighzCandidateSelection.ipynb`<br> 
is a notebook that takes the training sets that we used for KDE
selection of 3.5<z<5 quasars from SDSS+SpIES data and does color-based
self classifation using other machine learning algorithsm from
Scikit-Learn.  KDE was about 78% complete and 97% efficient.  The
sklearn algorithms were about the same, which gives confidence that
the sample is not *highly* contaminated (which isn't to so that it
isn't contaminated at *all*) and that we could replace our usage of
the proprietary KDE algorithm with public algorithms from sklearn.  I
looked at neural networks, SVM, random forests, bagging, and boosting.
While bagging has the highest efficiency, it also takes considerably
longer than random forests, which provided the best overall solution
(in terms of completeness, efficiency and computing time).  The
results of this get applied to the test set in
`SpIESHighzQuasars.ipynb`.

`SpIESHighzCandidateSelection2.ipynb`<br> 
is similar to the notebook above, but here I was exploring what would
happen if we added i-band magnitude and u-band extinction as
classification attributes.  I also explored some different
combinations of selection algorithms.  I found that bagging including
i and extinctu has less contamin than anything else.
`SpIESHighzQuasars2.ipynb` is the notebook where I explore these
changes in selection.

`SpIESHighzQuasars.ipynb`<br>