# Gothic loanwords in Hungarian?  
## How to search for old borrowings with [loanpy](https://github.com/martino-vic/loanpy) – a use-case
  
Open demo.ipynb and click yourself through the cells  
  
## Raw input files:  
  
- got_forms.csv: [Gothic CLDF word list](https://github.com/martino-vic/streitberggothic/blob/new/cldf/forms.csv)
- hun_forms.csv: [Hungarian CLDF word list](https://github.com/martino-vic/gerstnerhungarian/blob/main/cldf/forms.csv)
- wot_forms.csv: [West Old Turkic CLDF word list](https://github.com/martino-vic/ronataswestoldturkic)

## Files generated by [loanpy](https://github.com/martino-vic/loanpy) and used as secondary input:

1. scWOT2EAH.txt: Sound substitutions from West Old Turkic into Early Ancient Hungarian 
2. scH2EAH.txt: Historical sound changes from modern Hungarian into Early Ancient Hungarian
3. ad_got_forms.csv: Predictions how Gothic words would have been adapted into Early Ancient Hungarian
4. rc_hun_forms.csv: Predictions how Hungarian words would have sounded in Early Ancient Hungarian

## Files for manual insepction:

- cache_ad.csv, cache_ad2.csv: See how the model performs on predicting loanword adaptation from Gothic into Early Ancient Hungarian with different parameter settings
- cache_rc.csv: See how the model performs on reconstructing from Hungarian into Early Ancient Hungarian with different parameter settings
- eval_ad.csv, eval_rc.csv: See concrete predections, useful for debugging
- eval_ad.jpg, eval_rc.jpg: See the [ROC-curve](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) generated from eval_ad.csv/eval_rc.csv

## The final output file:
- loans.csv

## Error analyses:
- error_analysis.ods

## Dependencies
- [Jupyter Notebook](https://jupyter.org/install)
- [loanpy2.0.2](https://pypi.org/project/loanpy/)
- German word-vectors (738MB): [Download](https://cloud.devmount.de/d2bc5672c523b086/german.model)

## Notes:
- The repo has no folders because flat is better than nested.
- "sc" stands for "sound correspondences". These include sound substitutions in borrowings and historical sound changes in reconstructions
- "rc" stands for "reconstruct" and "ad" for "adapt"
- German word-vectors are not included because file limit is 100MB
