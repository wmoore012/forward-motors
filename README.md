# Forward Motors: Auction Value Intelligence

DSBA 6165 AI and Deep Learning | Mam Salan Njie and Will Moore

A pricing tool for wholesale vehicle auctions. MMR is the price guide dealers rely on. It is
accurate on average but can miss badly on an individual car, and at roughly 1% margins a few
hundred dollars of mispricing erases the profit on a unit. We estimate what each vehicle will
sell for, with a likely range, before the bidding starts.

## Research questions

1. **Price.** Can a model given MMR plus the vehicle's details predict where MMR will miss?
2. **Range.** Does a prediction range that updates with new sales stay near 90% coverage, while
   one calibrated once drifts?
3. **Damage.** Does pretraining help a damage detector trained on only 4,000 photos, and does it
   hold up on photographs taken at a real auction lot?

## Repository layout

```
notebooks/
  01_eda_auction_prices.ipynb    Stage 3, auction price data (Salan)
  02_eda_damage_images.ipynb     Stage 3, CarDD and lot photos (Will)
data/                            Not tracked. See "Getting the data" below.
```

## Getting the data

**Auction prices.** "Vehicle Sales Data" by Syed Anwar Afridi on Kaggle, about 558,000 wholesale
auction sales from 2014 to 2015.
https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data

Download `car_prices.csv` and place it beside the notebook, or in
`/content/drive/MyDrive/forward-motors/`. The notebook checks both before falling back to a Kaggle
download.

**Damage images.** CarDD (Wang, Li and Wu, 2023), 4,000 images with over 9,000 annotated damage
instances. https://cardd-ustc.github.io/

Data files are not committed. They are large, and the Kaggle terms are better served by linking.

## Who does what

**Salan:** auction data cleaning and splitting, MMR and gradient boosting baselines, the
TensorFlow price model, the tabular foundation model, the mispricing-caught replay.

**Will:** standard versus adaptive prediction ranges, CarDD preparation, damage models and the
vision-language check, auction photographs and labeling, the past-sale demo.

Notebook cleanup, the final report and the presentation are shared.
