# Deep Machine Translation [Work-In-Progress 2017-04-02]

This is a fun week-long project I did to implement a sequence to sequence model in PyTorch. The project uses language pairs from the Anki project as the training set.

## Key Learning

- **Good Demo can be trained quickly**. Sean Roberson's demos are very nice for teaching, partially because the training converges very quickly. Most of his demo converge in less than half an hour on a MBP. 

    As a corollary, any model that does not improve within a few minutes of training should raise a red flag.

- **Teacher forcing can be a hyper parameter**. During training, we can tune the teacher forcing ratio between 0 and 1.

- **Mini-batch hugely improves training speed**. Here I used a mini-batch of 128 pairs. For the small English-to-Chinese anki dataset, the training takes about 1 min 30 seconds on an i7 PC. And the translated result is acceptable within a few epochs.

- **Training and loss function need more work**. The loss function used here feels a bit unsatisfactory.

## TODO List

- [x] polish demo
- [x] write sequence to sequence example
- [x] get both training and evaluation to work
- [ ] Add BLUE as accuracy metric
- [ ] Add confusion matrix in demo.
- [ ] Add unzip script for languages
- [ ] polish repo
- [ ] Compare results with attention model

## DONE
- [x] write data scraper, download zip files from anki
- [x] convert zip to text file
- [x] write evaluation function
