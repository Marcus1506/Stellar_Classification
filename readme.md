# Summary
The goal of this project was to showcase typical data exploration, data analysis, feature engineering and model finetuning on a simple problem.

It shows beatifully, how physical understanding of the data and the system, from which the data emerged, can help to speed up feature selection, feature engineering as a whole and overall model performance.

**By introducing a feature which was motivated based on pyhsics and removing outliers, I increased the performance of the initial model iteration from roughly 97.7% to almost 100%.**

This short project showed how phyiscal intuition helps with the following problems:
 - Feature selection: Identifying features which carry relevant and not redundant information of a physical system, therefore choosing features which are likely to be relevant for model performance and reduce noise. If applyable, this methodology, combined with rather brute methods like correlation matrices, should represent a rather save way of selecting important features.
 - Feature creation: Based on the physical context of the problem I guessed that a quantity which is "proportional" to the general intensitiy of the electromagnetic radiation coming from the objects, might me relevant. Therefore I computed a quantity from the existing data which should fulfill this requirement (and is **inherently non-linear**). With the help of this additional feature model performance improved from around 97.7% to practically 100%.

Even though the performance is already close to its possible best here are some ideas for improvement:
 - In the final model, it seems like the 'redshift' feature is not really well picked up by our model, also, most, if not all of the falsely predicted objects, have their added feature 'extra_1' really close to 0. Both of these observations could be adressed by additional feature engineering, to potentially further increase model performance if needed.

Since the biggest improvement came from the introduction of the physically motivated feature, the impovement made by the outlier detection through Isolation forest is negligable. Therefore only using the 'outlier_score' generated from the Isolation forest model and not removing the identified 'outliers', should be considered for further implementation.
