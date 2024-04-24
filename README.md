<h1>Top-level description</h1>
This repo considers data from two sources:
<ul>
  <li><a href="https://science.ebird.org/en/use-ebird-data">EBird</a>, which compiles data regarding where, how often, which species of, 
    and how many birds are seen at any given time and place</li>
  <li>GHCNd, weather data from <a href="https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily">NOAA</a></li>
</ul>
Its goal is to use this information to train various models whose inputs consist of weather and bird data,
and which attempt to predict how many birds of some species will be seen at some time and place in the future.
In particular, we run a linear regression model, a time series model, and a recurrent neural network.
<h2>Missing files</h2>
Some files had to be removed from this repo due to the 100MB file size limit for our version of GitHub. Those coming directly from our above sources are as follows:
<ul>
  <li>Data/ghcnd_all.tar.gz</li>
  <li>Data/amegfi/ebd_amegfi_smp_relFeb-2024.zip</li>
</ul>
Those which can be constructed with the files given, and are only in our local filesystems for efficiency, are as follows:
<ul>
  <li>Data/amegfi/2019_ebd_amegfi_Feb-2024.txt</li>
  <li>Data/amegfi/2019_ebd_amegfi_Feb-2024_secondclean.csv</li>
  <li>Data/amegfi/2023_ebd_amegfi_Feb-2024_aggregate.csv</li>
  <li>AllSpecYear.csv</li>
</ul>
<h1>Workflow for this repo</h1>
<ul>
  <li>Weather data gathering happens in weather.ipynb</li>
  <li>Bird data gathering:
    <ul>
      <li>FirstClean.ipynb</li>
      <li>SecondClean.ipynb</li>
    </ul>
  </li>
  <li>Integrating the data happens in Final Clean.ipynb</li>
  <li>Building linear regression model happens in Basic Regression.ipynb</li>
  <li>Building time series model happens in Basic Time Series from time_series.ipynb</li>
  <li>Building RNN model happens in rnn.ipynb</li>
</ul>
