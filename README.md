# Naked POC (nPOC) - Daily

A TradingView Pine Script v6 indicator that tracks unvisited daily Points of Control and displays them as clean dashed levels on the chart. No histogram. No boxes. Just the levels that still have magnetic pull on price.

## What is a Naked POC?

The Point of Control (POC) is the price where the most volume traded during a session. Once a session closes, that level becomes a reference - price tends to return to it. A POC is "naked" when price has not revisited it since the session closed. Once price touches the level, it is automatically removed from the chart.

## What makes this different from TradingView's built-in SVP?

TradingView's Session Volume Profile draws a full histogram for every visible session. This indicator draws nothing except the levels that are still relevant. The moment a POC is filled, it disappears. Your chart stays clean as price works through historical levels one by one.

## Volume Distribution

Most volume profile tools distribute each bar's volume uniformly across its high-low range. This indicator uses a **close-weighted triangular distribution** - bins near the bar's close receive more weight than bins at the extremes. The POC lands closer to where price repeatedly settled, not just where it briefly spiked.

## Settings

| Setting | Description | Default |
|---|---|---|
| TPO Bins | Resolution of the volume calculation (20-500). Higher = more precise POC. | 100 |
| Max Visible nPOCs | Cap on how many naked levels are shown at once. | 15 |
| Max Age (days) | Automatically expires levels older than N days. | 7 |
| Extend Forward (hours) | How far the dashed line extends to the right. | 30 |
| Remove When Filled | Toggle whether levels disappear on touch. | true |
| Color | Fully customizable line and label color. | Fuchsia |

## Recommended Timeframe

**1H to 4H.** A warning label appears if the indicator is applied to an incompatible timeframe.

## How to use

Add the published indicator directly from TradingView, no copy-paste needed:

1. Open it here: [Naked POC (nPOC): Clean and No Clutter](https://www.tradingview.com/script/3r5whRmf-Naked-POC-nPOC-Clean-and-No-Clutter/)
2. Click the star to add it to your favorites, then add it to any chart from your indicators list.

The full source (`nPOC_Daily.pine`) lives in this repo under the MPL 2.0 license if you want to read or fork it.

## License

Mozilla Public License 2.0
