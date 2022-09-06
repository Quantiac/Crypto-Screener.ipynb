# Description
This notebook uses the Coingecko API to retrieve the bottom 50 tokens by marketcap, that satisfy the condition of being listed on the okx exchange. Tokens with unknown market cap (due to unknown circulating supply) are ignored.

It then orders those tokens by turnover rate, which is calculated by dividing global trading volume, by market cap (in both cases, average values over the last 7 days are used).

# Notes
From my experiments, a good waiting time between API calls, to avoid triggering restrictions, is 3 seconds. This value can be configured in the first cell.
With the default settings, it takes between 2 and 3 hours to finish. This is largely due to the fact that a separate API call needs to be made for each individual token, in order to check if it is listed on okx or not.
The code runs entirely in Google cloud, it doesn't touch the local machine. However, you have the option to save the data locally, by downloading the files from the temporary Google storage.
If you try this and it works and you find it useful, please consider supporting me:
(ethereum) 0xdc37Ca394FF485Bf4C605fc98E44a1F20896405d
