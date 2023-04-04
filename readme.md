# 11) Summary
**By introducing a feature which was motivated based on pyhsics and removing outliers, I increased the performance of the model from roughly 97.7% to almost 100%.**

This short project showed how phyiscal intuition help with the following problems:
 - Feature selection: Identifying features which carry relevant and not redundant information of a physical system, therefore choosing features which are likely to be relevant for model performance and reduce noise. If applyable, this methodology, combined with rather brute methods like correlation matrices, should represent a rather save way of selecting features.
 - Feature creation: Based on the physical context of the problem I guessed that a quantity which is "proportional" to the general intensitiy of the electromagnetic radiation coming from the objects, might me relevant. With the help of this additional feature model performance improved from around 97.7% to practically 100%.

Even though the performance is already close to best here are some ideas for improvements:
 - In the final model, it seems like the 'redshift' feature is not really well picked up by our model, also, most if not all of the falsely predicted objects, have their added feature 'extra_1' really close to 0. Both of these observations could be implemented by additional feature engineering, to potentially further increase model performance.

Finally, the biggest improvement came from the introduction of the physically motivated feature, the impovement made by the outlier detection through Isolation forest is negligable, therefore further implementation of the model should be done with the 'outlier_score' feature, since it suggested to be good input for our model, but without removing the labeled outliers.