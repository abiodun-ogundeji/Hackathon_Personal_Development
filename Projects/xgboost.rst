.. code:: ipython3

    import pandas as pd
    import numpy as np

.. code:: ipython3

    def read_and_display(filepath):
        data = pd.read_csv(filepath, index_col='comp_id')
        print(data.shape)
        display(data.head())
        return data

.. code:: ipython3

    desc_data_train = read_and_display("Description Data/train_desc_df.csv")


.. parsed-literal::

    (3000, 50)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>desc_41</th>
          <th>desc_42</th>
          <th>desc_43</th>
          <th>desc_44</th>
          <th>desc_45</th>
          <th>desc_46</th>
          <th>desc_47</th>
          <th>desc_48</th>
          <th>desc_49</th>
          <th>desc_50</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>-0.029430</td>
          <td>-0.029423</td>
          <td>0.052256</td>
          <td>0.007814</td>
          <td>0.023472</td>
          <td>-0.021134</td>
          <td>0.003324</td>
          <td>-0.004393</td>
          <td>0.004294</td>
          <td>-0.002223</td>
        </tr>
        <tr>
          <th>2</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>-0.029430</td>
          <td>-0.029423</td>
          <td>0.052256</td>
          <td>0.007814</td>
          <td>0.023472</td>
          <td>-0.021134</td>
          <td>0.003324</td>
          <td>-0.004393</td>
          <td>0.004294</td>
          <td>-0.002223</td>
        </tr>
        <tr>
          <th>3</th>
          <td>-0.356706</td>
          <td>0.213562</td>
          <td>0.252663</td>
          <td>0.090735</td>
          <td>0.328961</td>
          <td>-0.482705</td>
          <td>0.067300</td>
          <td>0.384217</td>
          <td>-0.147253</td>
          <td>-0.463378</td>
          <td>...</td>
          <td>-0.626436</td>
          <td>-0.102908</td>
          <td>0.576792</td>
          <td>-0.805986</td>
          <td>0.310637</td>
          <td>0.422263</td>
          <td>0.403496</td>
          <td>0.264240</td>
          <td>7.057590</td>
          <td>-0.252417</td>
        </tr>
        <tr>
          <th>4</th>
          <td>-0.294013</td>
          <td>0.165262</td>
          <td>0.257102</td>
          <td>0.421037</td>
          <td>0.463214</td>
          <td>-0.769155</td>
          <td>0.159450</td>
          <td>0.236385</td>
          <td>-0.183974</td>
          <td>-0.357842</td>
          <td>...</td>
          <td>-0.435836</td>
          <td>0.052975</td>
          <td>0.108777</td>
          <td>-0.599593</td>
          <td>0.408430</td>
          <td>0.591615</td>
          <td>0.415667</td>
          <td>0.334706</td>
          <td>7.025648</td>
          <td>-0.309093</td>
        </tr>
        <tr>
          <th>5</th>
          <td>-0.028657</td>
          <td>0.157017</td>
          <td>0.282709</td>
          <td>-2.674227</td>
          <td>-0.711383</td>
          <td>2.259387</td>
          <td>-0.162175</td>
          <td>0.605468</td>
          <td>0.712229</td>
          <td>0.027828</td>
          <td>...</td>
          <td>-1.714496</td>
          <td>0.297421</td>
          <td>-0.097744</td>
          <td>0.000669</td>
          <td>-1.639307</td>
          <td>0.244313</td>
          <td>0.099975</td>
          <td>0.371806</td>
          <td>-2.259024</td>
          <td>-0.131085</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 50 columns</p>
    </div>


.. code:: ipython3

    desc_data_public = read_and_display("Description Data/public_desc_df.csv")


.. parsed-literal::

    (986, 50)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>desc_41</th>
          <th>desc_42</th>
          <th>desc_43</th>
          <th>desc_44</th>
          <th>desc_45</th>
          <th>desc_46</th>
          <th>desc_47</th>
          <th>desc_48</th>
          <th>desc_49</th>
          <th>desc_50</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>-1.111625</td>
          <td>0.252028</td>
          <td>-0.193523</td>
          <td>0.346493</td>
          <td>-0.077318</td>
          <td>0.276308</td>
          <td>-0.045740</td>
          <td>-0.007150</td>
          <td>-3.448430</td>
          <td>-0.031262</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>-1.111625</td>
          <td>0.252028</td>
          <td>-0.193523</td>
          <td>0.346493</td>
          <td>-0.077318</td>
          <td>0.276308</td>
          <td>-0.045740</td>
          <td>-0.007150</td>
          <td>-3.448430</td>
          <td>-0.031262</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>-1.111625</td>
          <td>0.252028</td>
          <td>-0.193523</td>
          <td>0.346493</td>
          <td>-0.077318</td>
          <td>0.276308</td>
          <td>-0.045740</td>
          <td>-0.007150</td>
          <td>-3.448430</td>
          <td>-0.031262</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>-0.298706</td>
          <td>-0.022012</td>
          <td>0.552924</td>
          <td>0.046070</td>
          <td>0.044543</td>
          <td>0.132187</td>
          <td>-0.549770</td>
          <td>1.437774</td>
          <td>1.286943</td>
          <td>1.445921</td>
          <td>...</td>
          <td>0.246156</td>
          <td>-1.001942</td>
          <td>-1.502183</td>
          <td>1.105716</td>
          <td>-0.170937</td>
          <td>0.181976</td>
          <td>0.437707</td>
          <td>0.058352</td>
          <td>-2.209322</td>
          <td>0.104916</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>-1.111625</td>
          <td>0.252028</td>
          <td>-0.193523</td>
          <td>0.346493</td>
          <td>-0.077318</td>
          <td>0.276308</td>
          <td>-0.045740</td>
          <td>-0.007150</td>
          <td>-3.448430</td>
          <td>-0.031262</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 50 columns</p>
    </div>


.. code:: ipython3

    img_data_train = read_and_display("Image Data/train_image_df.csv")


.. parsed-literal::

    (3000, 4000)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>image_1</th>
          <th>image_2</th>
          <th>image_3</th>
          <th>image_4</th>
          <th>image_5</th>
          <th>image_6</th>
          <th>image_7</th>
          <th>image_8</th>
          <th>image_9</th>
          <th>image_10</th>
          <th>...</th>
          <th>image_3991</th>
          <th>image_3992</th>
          <th>image_3993</th>
          <th>image_3994</th>
          <th>image_3995</th>
          <th>image_3996</th>
          <th>image_3997</th>
          <th>image_3998</th>
          <th>image_3999</th>
          <th>image_4000</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>0.484456</td>
          <td>0.036087</td>
          <td>-0.149328</td>
          <td>0.144475</td>
          <td>-0.617386</td>
          <td>0.035018</td>
          <td>0.169174</td>
          <td>-0.005733</td>
          <td>-0.104908</td>
          <td>-0.041200</td>
          <td>...</td>
          <td>-0.090408</td>
          <td>-0.032915</td>
          <td>-0.010857</td>
          <td>-0.015954</td>
          <td>0.123416</td>
          <td>0.195833</td>
          <td>-0.066449</td>
          <td>0.115818</td>
          <td>-0.005140</td>
          <td>0.017278</td>
        </tr>
        <tr>
          <th>2</th>
          <td>0.074533</td>
          <td>-0.015655</td>
          <td>-0.016286</td>
          <td>-0.480964</td>
          <td>0.687917</td>
          <td>0.037131</td>
          <td>-0.149725</td>
          <td>-0.002098</td>
          <td>0.099383</td>
          <td>-0.021134</td>
          <td>...</td>
          <td>-0.625816</td>
          <td>-0.009616</td>
          <td>0.004558</td>
          <td>0.008310</td>
          <td>-0.173496</td>
          <td>0.133518</td>
          <td>-0.488898</td>
          <td>0.084832</td>
          <td>0.146566</td>
          <td>0.007997</td>
        </tr>
        <tr>
          <th>3</th>
          <td>-0.396809</td>
          <td>0.021490</td>
          <td>-1.723037</td>
          <td>0.666147</td>
          <td>-0.631924</td>
          <td>0.047724</td>
          <td>0.336041</td>
          <td>-0.003904</td>
          <td>0.039683</td>
          <td>0.002628</td>
          <td>...</td>
          <td>-0.078059</td>
          <td>0.086320</td>
          <td>-0.005606</td>
          <td>0.002414</td>
          <td>-0.164493</td>
          <td>0.218473</td>
          <td>0.151292</td>
          <td>-0.076860</td>
          <td>0.008321</td>
          <td>0.012555</td>
        </tr>
        <tr>
          <th>4</th>
          <td>0.995316</td>
          <td>0.012766</td>
          <td>0.387472</td>
          <td>-0.684791</td>
          <td>-0.209261</td>
          <td>0.013654</td>
          <td>0.138517</td>
          <td>0.005586</td>
          <td>0.079277</td>
          <td>-0.004665</td>
          <td>...</td>
          <td>-0.190714</td>
          <td>-0.005452</td>
          <td>-0.003889</td>
          <td>0.013430</td>
          <td>0.344406</td>
          <td>0.038220</td>
          <td>0.210446</td>
          <td>-0.145128</td>
          <td>-0.019172</td>
          <td>0.000532</td>
        </tr>
        <tr>
          <th>5</th>
          <td>-0.611648</td>
          <td>0.000860</td>
          <td>-0.572393</td>
          <td>0.894287</td>
          <td>-0.191228</td>
          <td>-0.111583</td>
          <td>-0.011111</td>
          <td>0.003231</td>
          <td>-0.160582</td>
          <td>0.032804</td>
          <td>...</td>
          <td>-0.040437</td>
          <td>-0.142134</td>
          <td>-0.022771</td>
          <td>-0.013134</td>
          <td>-0.024869</td>
          <td>0.125129</td>
          <td>0.215967</td>
          <td>0.005288</td>
          <td>0.145715</td>
          <td>0.001425</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4000 columns</p>
    </div>


.. code:: ipython3

    img_data_public = read_and_display("Image Data/public_image_df.csv")


.. parsed-literal::

    (986, 4000)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>image_1</th>
          <th>image_2</th>
          <th>image_3</th>
          <th>image_4</th>
          <th>image_5</th>
          <th>image_6</th>
          <th>image_7</th>
          <th>image_8</th>
          <th>image_9</th>
          <th>image_10</th>
          <th>...</th>
          <th>image_3991</th>
          <th>image_3992</th>
          <th>image_3993</th>
          <th>image_3994</th>
          <th>image_3995</th>
          <th>image_3996</th>
          <th>image_3997</th>
          <th>image_3998</th>
          <th>image_3999</th>
          <th>image_4000</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>-0.288211</td>
          <td>0.007964</td>
          <td>-0.318695</td>
          <td>-0.519448</td>
          <td>-0.707238</td>
          <td>0.018358</td>
          <td>-0.127491</td>
          <td>0.006911</td>
          <td>-0.163305</td>
          <td>-0.001028</td>
          <td>...</td>
          <td>0.095390</td>
          <td>-0.005706</td>
          <td>0.011662</td>
          <td>0.027501</td>
          <td>0.202042</td>
          <td>0.031049</td>
          <td>0.058993</td>
          <td>0.085795</td>
          <td>-0.033876</td>
          <td>-0.010047</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>-0.053049</td>
          <td>-0.019362</td>
          <td>-0.942308</td>
          <td>0.971880</td>
          <td>-0.145869</td>
          <td>0.190100</td>
          <td>0.323404</td>
          <td>0.001693</td>
          <td>0.052303</td>
          <td>0.008241</td>
          <td>...</td>
          <td>-0.152575</td>
          <td>-0.015299</td>
          <td>0.006474</td>
          <td>0.008779</td>
          <td>0.064745</td>
          <td>-0.130691</td>
          <td>0.519738</td>
          <td>-0.009965</td>
          <td>0.226757</td>
          <td>0.001792</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>0.527363</td>
          <td>0.027754</td>
          <td>-1.644639</td>
          <td>-0.362191</td>
          <td>-0.275900</td>
          <td>0.095907</td>
          <td>-0.083026</td>
          <td>-0.002009</td>
          <td>0.041976</td>
          <td>0.008518</td>
          <td>...</td>
          <td>-0.139857</td>
          <td>0.056012</td>
          <td>0.010546</td>
          <td>-0.013047</td>
          <td>0.395852</td>
          <td>0.064757</td>
          <td>0.061725</td>
          <td>0.081311</td>
          <td>0.094162</td>
          <td>-0.015818</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>0.709023</td>
          <td>0.002011</td>
          <td>-0.968376</td>
          <td>0.478994</td>
          <td>-0.451566</td>
          <td>0.217366</td>
          <td>-0.036373</td>
          <td>0.004914</td>
          <td>0.133615</td>
          <td>0.019694</td>
          <td>...</td>
          <td>-0.343643</td>
          <td>0.072151</td>
          <td>0.045109</td>
          <td>-0.009794</td>
          <td>-0.002994</td>
          <td>0.142427</td>
          <td>-0.001836</td>
          <td>0.116891</td>
          <td>0.078607</td>
          <td>-0.000430</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>-0.349026</td>
          <td>-0.060301</td>
          <td>-1.099632</td>
          <td>1.475574</td>
          <td>-0.076292</td>
          <td>0.153835</td>
          <td>-0.143689</td>
          <td>0.006389</td>
          <td>0.058670</td>
          <td>-0.021164</td>
          <td>...</td>
          <td>0.158350</td>
          <td>-0.024394</td>
          <td>0.002807</td>
          <td>-0.004787</td>
          <td>-0.012235</td>
          <td>0.022360</td>
          <td>0.034833</td>
          <td>0.084962</td>
          <td>-0.092006</td>
          <td>0.010375</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4000 columns</p>
    </div>


.. code:: ipython3

    title_data_train = read_and_display("Title_Data/train_title_df.csv")


.. parsed-literal::

    (3000, 50)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>title_1</th>
          <th>title_2</th>
          <th>title_3</th>
          <th>title_4</th>
          <th>title_5</th>
          <th>title_6</th>
          <th>title_7</th>
          <th>title_8</th>
          <th>title_9</th>
          <th>title_10</th>
          <th>...</th>
          <th>title_41</th>
          <th>title_42</th>
          <th>title_43</th>
          <th>title_44</th>
          <th>title_45</th>
          <th>title_46</th>
          <th>title_47</th>
          <th>title_48</th>
          <th>title_49</th>
          <th>title_50</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>-0.977637</td>
          <td>-0.543310</td>
          <td>0.079403</td>
          <td>0.205560</td>
          <td>-1.497104</td>
          <td>0.230466</td>
          <td>0.566112</td>
          <td>-0.662264</td>
          <td>0.130342</td>
          <td>-0.277137</td>
          <td>...</td>
          <td>0.059434</td>
          <td>-0.272340</td>
          <td>-0.030180</td>
          <td>-0.109040</td>
          <td>-0.033425</td>
          <td>0.728739</td>
          <td>0.142030</td>
          <td>0.397541</td>
          <td>1.270722</td>
          <td>-0.816523</td>
        </tr>
        <tr>
          <th>2</th>
          <td>0.041873</td>
          <td>0.644655</td>
          <td>0.140869</td>
          <td>-0.664714</td>
          <td>-0.062992</td>
          <td>0.240086</td>
          <td>-1.017593</td>
          <td>1.019706</td>
          <td>0.340133</td>
          <td>0.617302</td>
          <td>...</td>
          <td>0.242961</td>
          <td>-0.404538</td>
          <td>0.335224</td>
          <td>-0.158068</td>
          <td>-0.178225</td>
          <td>0.351125</td>
          <td>0.959121</td>
          <td>0.673848</td>
          <td>-0.530106</td>
          <td>0.133466</td>
        </tr>
        <tr>
          <th>3</th>
          <td>-0.905595</td>
          <td>0.097928</td>
          <td>0.111981</td>
          <td>-0.064753</td>
          <td>-1.566516</td>
          <td>0.140807</td>
          <td>-0.946588</td>
          <td>-0.342442</td>
          <td>0.031226</td>
          <td>-0.660981</td>
          <td>...</td>
          <td>0.414191</td>
          <td>-0.457968</td>
          <td>0.157185</td>
          <td>-0.116985</td>
          <td>0.404937</td>
          <td>-0.220503</td>
          <td>0.443171</td>
          <td>0.643445</td>
          <td>0.357957</td>
          <td>0.525154</td>
        </tr>
        <tr>
          <th>4</th>
          <td>0.069220</td>
          <td>0.411544</td>
          <td>0.177700</td>
          <td>-0.739998</td>
          <td>-0.932620</td>
          <td>-0.717982</td>
          <td>-0.406487</td>
          <td>-0.267096</td>
          <td>0.114066</td>
          <td>-0.045532</td>
          <td>...</td>
          <td>0.211731</td>
          <td>-0.812590</td>
          <td>0.258014</td>
          <td>-0.180143</td>
          <td>-0.564691</td>
          <td>-0.515378</td>
          <td>0.613686</td>
          <td>0.817547</td>
          <td>0.325042</td>
          <td>0.254415</td>
        </tr>
        <tr>
          <th>5</th>
          <td>0.503560</td>
          <td>-0.210970</td>
          <td>-0.085412</td>
          <td>0.549240</td>
          <td>-0.019521</td>
          <td>-0.255597</td>
          <td>0.841144</td>
          <td>0.250485</td>
          <td>0.224235</td>
          <td>0.082816</td>
          <td>...</td>
          <td>-0.517912</td>
          <td>0.543584</td>
          <td>0.492052</td>
          <td>-0.204867</td>
          <td>-0.011538</td>
          <td>-0.328607</td>
          <td>-0.150055</td>
          <td>-0.992373</td>
          <td>-0.266003</td>
          <td>-0.037134</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 50 columns</p>
    </div>


.. code:: ipython3

    title_data_public = read_and_display("Title_Data/public_title_df.csv")


.. parsed-literal::

    (986, 50)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>title_1</th>
          <th>title_2</th>
          <th>title_3</th>
          <th>title_4</th>
          <th>title_5</th>
          <th>title_6</th>
          <th>title_7</th>
          <th>title_8</th>
          <th>title_9</th>
          <th>title_10</th>
          <th>...</th>
          <th>title_41</th>
          <th>title_42</th>
          <th>title_43</th>
          <th>title_44</th>
          <th>title_45</th>
          <th>title_46</th>
          <th>title_47</th>
          <th>title_48</th>
          <th>title_49</th>
          <th>title_50</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>0.363698</td>
          <td>0.309343</td>
          <td>0.225138</td>
          <td>0.318105</td>
          <td>-0.523210</td>
          <td>0.143360</td>
          <td>-0.012829</td>
          <td>0.407408</td>
          <td>-0.048370</td>
          <td>-0.298985</td>
          <td>...</td>
          <td>0.532943</td>
          <td>0.194463</td>
          <td>-0.635401</td>
          <td>-0.419310</td>
          <td>0.142901</td>
          <td>-0.523376</td>
          <td>1.204893</td>
          <td>-1.413345</td>
          <td>-0.096672</td>
          <td>0.078235</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>0.218130</td>
          <td>1.117077</td>
          <td>0.122527</td>
          <td>-0.005565</td>
          <td>-0.158261</td>
          <td>0.390527</td>
          <td>0.189782</td>
          <td>0.685502</td>
          <td>-0.383055</td>
          <td>0.402898</td>
          <td>...</td>
          <td>0.548985</td>
          <td>0.066296</td>
          <td>-0.525967</td>
          <td>-0.674784</td>
          <td>0.151137</td>
          <td>-1.065329</td>
          <td>0.751027</td>
          <td>-1.075753</td>
          <td>-0.009242</td>
          <td>0.464259</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>0.209271</td>
          <td>0.785080</td>
          <td>0.287104</td>
          <td>0.508236</td>
          <td>0.306759</td>
          <td>0.505576</td>
          <td>-0.172887</td>
          <td>0.324774</td>
          <td>-0.032752</td>
          <td>0.168677</td>
          <td>...</td>
          <td>0.803655</td>
          <td>0.199135</td>
          <td>-0.580919</td>
          <td>-0.569989</td>
          <td>0.033141</td>
          <td>-0.658906</td>
          <td>0.956579</td>
          <td>-0.885134</td>
          <td>-0.233097</td>
          <td>0.235301</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>1.160773</td>
          <td>-0.491947</td>
          <td>0.188722</td>
          <td>-0.100140</td>
          <td>-1.738414</td>
          <td>-0.105218</td>
          <td>0.400427</td>
          <td>-0.216526</td>
          <td>-0.371494</td>
          <td>0.231583</td>
          <td>...</td>
          <td>0.125851</td>
          <td>0.735062</td>
          <td>0.330460</td>
          <td>0.646128</td>
          <td>0.809633</td>
          <td>0.162228</td>
          <td>0.274926</td>
          <td>-0.085908</td>
          <td>0.217528</td>
          <td>1.031500</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>1.338603</td>
          <td>0.599431</td>
          <td>0.519767</td>
          <td>-0.198956</td>
          <td>0.850357</td>
          <td>0.039661</td>
          <td>0.248881</td>
          <td>0.885659</td>
          <td>0.245418</td>
          <td>-0.147505</td>
          <td>...</td>
          <td>0.531473</td>
          <td>-0.406249</td>
          <td>-0.507858</td>
          <td>-0.187037</td>
          <td>0.802942</td>
          <td>-0.472328</td>
          <td>0.897817</td>
          <td>-1.227795</td>
          <td>0.746802</td>
          <td>-0.379223</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 50 columns</p>
    </div>


.. code:: ipython3

    meta_data_train = read_and_display("Metadata/train_meta_df.csv")


.. parsed-literal::

    (3000, 13)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>ad_blocked</th>
          <th>embed</th>
          <th>ratio</th>
          <th>duration</th>
          <th>language</th>
          <th>partner</th>
          <th>partner_active</th>
          <th>n_likes</th>
          <th>views</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>False</td>
          <td>True</td>
          <td>1.77778</td>
          <td>86</td>
          <td>3</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>290</td>
          <td>3</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>2</th>
          <td>False</td>
          <td>True</td>
          <td>1.33333</td>
          <td>1129</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>1443</td>
          <td>0</td>
          <td>2</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>3</th>
          <td>False</td>
          <td>True</td>
          <td>1.76667</td>
          <td>1163</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>329</td>
          <td>0</td>
          <td>1</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>4</th>
          <td>False</td>
          <td>True</td>
          <td>1.77778</td>
          <td>1326</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>63</td>
          <td>0</td>
          <td>3</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>5</th>
          <td>False</td>
          <td>True</td>
          <td>1.77273</td>
          <td>2612</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>3</td>
          <td>37</td>
          <td>0</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
        </tr>
      </tbody>
    </table>
    </div>


.. code:: ipython3

    meta_data_public = read_and_display("Metadata/public_meta_df.csv")


.. parsed-literal::

    (986, 12)



.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>ad_blocked</th>
          <th>embed</th>
          <th>ratio</th>
          <th>duration</th>
          <th>language</th>
          <th>partner</th>
          <th>partner_active</th>
          <th>n_likes</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>False</td>
          <td>True</td>
          <td>1.33333</td>
          <td>1675</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>False</td>
          <td>True</td>
          <td>1.33333</td>
          <td>1479</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>False</td>
          <td>True</td>
          <td>1.33333</td>
          <td>1505</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>False</td>
          <td>True</td>
          <td>1.77778</td>
          <td>50</td>
          <td>2</td>
          <td>True</td>
          <td>True</td>
          <td>1</td>
          <td>6</td>
          <td>5</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>False</td>
          <td>True</td>
          <td>1.33333</td>
          <td>1543</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>6</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
      </tbody>
    </table>
    </div>


.. code:: ipython3

    train_data = pd.concat([desc_data_train, title_data_train, img_data_train, meta_data_train], axis=1)
    print(train_data.shape)
    train_data.head()


.. parsed-literal::

    (3000, 4113)




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>duration</th>
          <th>language</th>
          <th>partner</th>
          <th>partner_active</th>
          <th>n_likes</th>
          <th>views</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>86</td>
          <td>3</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>290</td>
          <td>3</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>2</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>1129</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>1443</td>
          <td>0</td>
          <td>2</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>3</th>
          <td>-0.356706</td>
          <td>0.213562</td>
          <td>0.252663</td>
          <td>0.090735</td>
          <td>0.328961</td>
          <td>-0.482705</td>
          <td>0.067300</td>
          <td>0.384217</td>
          <td>-0.147253</td>
          <td>-0.463378</td>
          <td>...</td>
          <td>1163</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>329</td>
          <td>0</td>
          <td>1</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>4</th>
          <td>-0.294013</td>
          <td>0.165262</td>
          <td>0.257102</td>
          <td>0.421037</td>
          <td>0.463214</td>
          <td>-0.769155</td>
          <td>0.159450</td>
          <td>0.236385</td>
          <td>-0.183974</td>
          <td>-0.357842</td>
          <td>...</td>
          <td>1326</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>0</td>
          <td>63</td>
          <td>0</td>
          <td>3</td>
          <td>5</td>
          <td>6</td>
        </tr>
        <tr>
          <th>5</th>
          <td>-0.028657</td>
          <td>0.157017</td>
          <td>0.282709</td>
          <td>-2.674227</td>
          <td>-0.711383</td>
          <td>2.259387</td>
          <td>-0.162175</td>
          <td>0.605468</td>
          <td>0.712229</td>
          <td>0.027828</td>
          <td>...</td>
          <td>2612</td>
          <td>2</td>
          <td>True</td>
          <td>False</td>
          <td>3</td>
          <td>37</td>
          <td>0</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4113 columns</p>
    </div>



.. code:: ipython3

    test_data = pd.concat([desc_data_public, title_data_public, img_data_public, meta_data_public], axis=1)
    print(test_data.shape)
    test_data.head()


.. parsed-literal::

    (986, 4112)




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>ratio</th>
          <th>duration</th>
          <th>language</th>
          <th>partner</th>
          <th>partner_active</th>
          <th>n_likes</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>1.33333</td>
          <td>1675</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>1.33333</td>
          <td>1479</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>1.33333</td>
          <td>1505</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>-0.298706</td>
          <td>-0.022012</td>
          <td>0.552924</td>
          <td>0.046070</td>
          <td>0.044543</td>
          <td>0.132187</td>
          <td>-0.549770</td>
          <td>1.437774</td>
          <td>1.286943</td>
          <td>1.445921</td>
          <td>...</td>
          <td>1.77778</td>
          <td>50</td>
          <td>2</td>
          <td>True</td>
          <td>True</td>
          <td>1</td>
          <td>6</td>
          <td>5</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>1.33333</td>
          <td>1543</td>
          <td>2</td>
          <td>False</td>
          <td>False</td>
          <td>0</td>
          <td>6</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4112 columns</p>
    </div>



.. code:: ipython3

    ad_blocked = train_data.select_dtypes(exclude=np.number)['ad_blocked'].value_counts()
    embed = train_data['embed'].value_counts()
    partner = train_data['partner'].value_counts()
    partner_active = train_data['partner_active'].value_counts()
    
    train_data['Encoded_ad_blocked'] = train_data['ad_blocked'].map(ad_blocked)
    train_data['Encoded_embed'] = train_data['embed'].map(embed)
    train_data['Encoded_partner'] = train_data['partner'].map(partner)
    train_data['Encoded_partner_active'] = train_data['partner_active'].map(partner_active)
    
    train_data[['ad_blocked', 'Encoded_ad_blocked', 'embed', 'Encoded_embed', 'partner', 'Encoded_partner', 'partner_active', 'Encoded_partner_active']].head()




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>ad_blocked</th>
          <th>Encoded_ad_blocked</th>
          <th>embed</th>
          <th>Encoded_embed</th>
          <th>partner</th>
          <th>Encoded_partner</th>
          <th>partner_active</th>
          <th>Encoded_partner_active</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>False</td>
          <td>2980</td>
          <td>True</td>
          <td>2982</td>
          <td>True</td>
          <td>1806</td>
          <td>False</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>2</th>
          <td>False</td>
          <td>2980</td>
          <td>True</td>
          <td>2982</td>
          <td>True</td>
          <td>1806</td>
          <td>False</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>3</th>
          <td>False</td>
          <td>2980</td>
          <td>True</td>
          <td>2982</td>
          <td>True</td>
          <td>1806</td>
          <td>False</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>4</th>
          <td>False</td>
          <td>2980</td>
          <td>True</td>
          <td>2982</td>
          <td>True</td>
          <td>1806</td>
          <td>False</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>5</th>
          <td>False</td>
          <td>2980</td>
          <td>True</td>
          <td>2982</td>
          <td>True</td>
          <td>1806</td>
          <td>False</td>
          <td>2317</td>
        </tr>
      </tbody>
    </table>
    </div>



.. code:: ipython3

    train_data = train_data.drop(['ad_blocked','embed','partner','partner_active'], axis = 1)
    train_data.head()




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>n_likes</th>
          <th>views</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
          <th>Encoded_ad_blocked</th>
          <th>Encoded_embed</th>
          <th>Encoded_partner</th>
          <th>Encoded_partner_active</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>0</td>
          <td>290</td>
          <td>3</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
          <td>2980</td>
          <td>2982</td>
          <td>1806</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>2</th>
          <td>-0.009555</td>
          <td>0.002479</td>
          <td>0.002927</td>
          <td>0.015774</td>
          <td>-0.008177</td>
          <td>-0.016036</td>
          <td>0.026697</td>
          <td>-0.000106</td>
          <td>0.025788</td>
          <td>0.052237</td>
          <td>...</td>
          <td>0</td>
          <td>1443</td>
          <td>0</td>
          <td>2</td>
          <td>5</td>
          <td>6</td>
          <td>2980</td>
          <td>2982</td>
          <td>1806</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>3</th>
          <td>-0.356706</td>
          <td>0.213562</td>
          <td>0.252663</td>
          <td>0.090735</td>
          <td>0.328961</td>
          <td>-0.482705</td>
          <td>0.067300</td>
          <td>0.384217</td>
          <td>-0.147253</td>
          <td>-0.463378</td>
          <td>...</td>
          <td>0</td>
          <td>329</td>
          <td>0</td>
          <td>1</td>
          <td>5</td>
          <td>6</td>
          <td>2980</td>
          <td>2982</td>
          <td>1806</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>4</th>
          <td>-0.294013</td>
          <td>0.165262</td>
          <td>0.257102</td>
          <td>0.421037</td>
          <td>0.463214</td>
          <td>-0.769155</td>
          <td>0.159450</td>
          <td>0.236385</td>
          <td>-0.183974</td>
          <td>-0.357842</td>
          <td>...</td>
          <td>0</td>
          <td>63</td>
          <td>0</td>
          <td>3</td>
          <td>5</td>
          <td>6</td>
          <td>2980</td>
          <td>2982</td>
          <td>1806</td>
          <td>2317</td>
        </tr>
        <tr>
          <th>5</th>
          <td>-0.028657</td>
          <td>0.157017</td>
          <td>0.282709</td>
          <td>-2.674227</td>
          <td>-0.711383</td>
          <td>2.259387</td>
          <td>-0.162175</td>
          <td>0.605468</td>
          <td>0.712229</td>
          <td>0.027828</td>
          <td>...</td>
          <td>3</td>
          <td>37</td>
          <td>0</td>
          <td>0</td>
          <td>5</td>
          <td>6</td>
          <td>2980</td>
          <td>2982</td>
          <td>1806</td>
          <td>2317</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4113 columns</p>
    </div>



.. code:: ipython3

    ad_blocked = test_data['ad_blocked'].value_counts()
    embed = test_data['embed'].value_counts()
    partner = test_data['partner'].value_counts()
    partner_active = test_data['partner_active'].value_counts()
    
    test_data['Encoded_ad_blocked'] = test_data['ad_blocked'].map(ad_blocked)
    test_data['Encoded_embed'] = test_data['embed'].map(embed)
    test_data['Encoded_partner'] = test_data['partner'].map(partner)
    test_data['Encoded_partner_active'] = test_data['partner_active'].map(partner_active)
    
    test_data[['ad_blocked', 'Encoded_ad_blocked', 'embed', 'Encoded_embed', 'partner', 'Encoded_partner', 'partner_active', 'Encoded_partner_active']].head()




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>ad_blocked</th>
          <th>Encoded_ad_blocked</th>
          <th>embed</th>
          <th>Encoded_embed</th>
          <th>partner</th>
          <th>Encoded_partner</th>
          <th>partner_active</th>
          <th>Encoded_partner_active</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>False</td>
          <td>986</td>
          <td>True</td>
          <td>952</td>
          <td>False</td>
          <td>749</td>
          <td>False</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>False</td>
          <td>986</td>
          <td>True</td>
          <td>952</td>
          <td>False</td>
          <td>749</td>
          <td>False</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>False</td>
          <td>986</td>
          <td>True</td>
          <td>952</td>
          <td>False</td>
          <td>749</td>
          <td>False</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>False</td>
          <td>986</td>
          <td>True</td>
          <td>952</td>
          <td>True</td>
          <td>237</td>
          <td>True</td>
          <td>144</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>False</td>
          <td>986</td>
          <td>True</td>
          <td>952</td>
          <td>False</td>
          <td>749</td>
          <td>False</td>
          <td>842</td>
        </tr>
      </tbody>
    </table>
    </div>



.. code:: ipython3

    test_data = test_data.drop(['ad_blocked','embed','partner','partner_active'], axis = 1)
    test_data.head()




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>desc_1</th>
          <th>desc_2</th>
          <th>desc_3</th>
          <th>desc_4</th>
          <th>desc_5</th>
          <th>desc_6</th>
          <th>desc_7</th>
          <th>desc_8</th>
          <th>desc_9</th>
          <th>desc_10</th>
          <th>...</th>
          <th>language</th>
          <th>n_likes</th>
          <th>n_tags</th>
          <th>n_formats</th>
          <th>dayofweek</th>
          <th>hour</th>
          <th>Encoded_ad_blocked</th>
          <th>Encoded_embed</th>
          <th>Encoded_partner</th>
          <th>Encoded_partner_active</th>
        </tr>
        <tr>
          <th>comp_id</th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>3001</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>2</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
          <td>986</td>
          <td>952</td>
          <td>749</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3002</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>2</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
          <td>986</td>
          <td>952</td>
          <td>749</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3003</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>2</td>
          <td>0</td>
          <td>10</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
          <td>986</td>
          <td>952</td>
          <td>749</td>
          <td>842</td>
        </tr>
        <tr>
          <th>3004</th>
          <td>-0.298706</td>
          <td>-0.022012</td>
          <td>0.552924</td>
          <td>0.046070</td>
          <td>0.044543</td>
          <td>0.132187</td>
          <td>-0.549770</td>
          <td>1.437774</td>
          <td>1.286943</td>
          <td>1.445921</td>
          <td>...</td>
          <td>2</td>
          <td>1</td>
          <td>6</td>
          <td>5</td>
          <td>2</td>
          <td>3</td>
          <td>986</td>
          <td>952</td>
          <td>237</td>
          <td>144</td>
        </tr>
        <tr>
          <th>3005</th>
          <td>-0.266289</td>
          <td>0.151930</td>
          <td>0.188684</td>
          <td>0.935617</td>
          <td>0.021999</td>
          <td>0.100940</td>
          <td>0.107302</td>
          <td>-0.055652</td>
          <td>0.023322</td>
          <td>-0.523113</td>
          <td>...</td>
          <td>2</td>
          <td>0</td>
          <td>6</td>
          <td>2</td>
          <td>2</td>
          <td>3</td>
          <td>986</td>
          <td>952</td>
          <td>749</td>
          <td>842</td>
        </tr>
      </tbody>
    </table>
    <p>5 rows × 4112 columns</p>
    </div>



.. code:: ipython3

    y = train_data['views'].iloc[:-1].values
    X = train_data.drop(['views'], axis = 1).iloc[:-1].values

.. code:: ipython3

    from sklearn.model_selection import train_test_split
    from sklearn.metrics import accuracy_score,mean_squared_error, r2_score
    from math import sqrt
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=0)

.. code:: ipython3

    import xgboost as xgb
    from xgboost import XGBRegressor

.. code:: ipython3

    xgbr = xgb.XGBRegressor(verbosity=0) 
    print(xgbr)


.. parsed-literal::

    XGBRegressor(base_score=None, booster=None, colsample_bylevel=None,
                 colsample_bynode=None, colsample_bytree=None, gamma=None,
                 gpu_id=None, importance_type='gain', interaction_constraints=None,
                 learning_rate=None, max_delta_step=None, max_depth=None,
                 min_child_weight=None, missing=nan, monotone_constraints=None,
                 n_estimators=100, n_jobs=None, num_parallel_tree=None,
                 random_state=None, reg_alpha=None, reg_lambda=None,
                 scale_pos_weight=None, subsample=None, tree_method=None,
                 validate_parameters=None, verbosity=0)


.. code:: ipython3

    xgbr.fit(X_train,y_train)




.. parsed-literal::

    XGBRegressor(base_score=0.5, booster='gbtree', colsample_bylevel=1,
                 colsample_bynode=1, colsample_bytree=1, gamma=0, gpu_id=-1,
                 importance_type='gain', interaction_constraints='',
                 learning_rate=0.300000012, max_delta_step=0, max_depth=6,
                 min_child_weight=1, missing=nan, monotone_constraints='()',
                 n_estimators=100, n_jobs=4, num_parallel_tree=1, random_state=0,
                 reg_alpha=0, reg_lambda=1, scale_pos_weight=1, subsample=1,
                 tree_method='exact', validate_parameters=1, verbosity=0)



.. code:: ipython3

    from sklearn.model_selection import cross_val_score, KFold

.. code:: ipython3

    score = xgbr.score(X_train,y_train)  
    print("Training score: ", score)


.. parsed-literal::

    Training score:  0.9999346512292763


.. code:: ipython3

    ypred = xgbr.predict(X_test)
    print(ypred)


.. parsed-literal::

    [ 2.15366638e+02  1.87453985e-01  1.13193207e+02  4.49593658e+02
      3.22932373e+02  1.98979236e+03  1.74451263e+02  1.04207626e+02
      1.62196045e+02  3.61906763e+03  5.50671021e+02  2.68034153e+01
      3.72221832e+02  6.91043823e+02  1.32601425e+02  1.30825455e+02
      2.42097641e+02  5.79918442e+01  1.13335648e+02  2.36055481e+02
      2.00969086e+02 -2.80742340e+01  7.43785828e+02  9.30741730e+01
      2.44647186e+02  1.88815353e+02  3.56580261e+02  4.27766144e+02
      1.08428047e+02 -7.57772398e+00  1.54962659e+03  5.98864502e+02
      1.21867896e+03  1.85573502e+02  4.54880890e+02  1.75208420e+02
      2.48940170e+02  1.30075146e+03  3.74035217e+02  1.01070961e+02
      1.04867332e+02  9.06399612e+01  6.49661026e+01  1.52324341e+02
      1.44065125e+02  5.27919373e+02  2.32441788e+02  1.80428625e+03
      2.16864243e+02  2.25040039e+03  8.87740112e+02  2.26002319e+02
      4.63874725e+02  3.18845752e+03  3.25237518e+02  1.26341797e+02
      1.73745972e+02  8.12206543e+02  3.36417755e+02  3.07087921e+02
      2.61758545e+02  2.24076099e+03  2.32117935e+02  1.58278076e+03
      3.07692480e+03  2.56652527e+02  5.41836426e+02  2.56309052e+02
      1.68250879e+03  1.09020775e+02  3.80755005e+02  1.74879379e+02
      1.10486060e+03  1.95542099e+02  1.23935400e+03  4.48069191e+01
      2.34025345e+02  2.65103882e+02  2.90893555e+02  1.38366730e+02
      5.57679077e+02  8.75266800e+01  9.61439743e+01  3.28414062e+02
      3.44059668e+03  2.29898804e+03  8.91954834e+02  6.59145935e+02
      2.27899200e+02  9.29802979e+02  1.04385962e+03  2.03900650e+02
      5.36260620e+02  3.42412903e+02  2.63470508e+03  2.17701187e+02
      3.95956360e+02  1.24946495e+02  3.96949371e+02  4.79152557e+02
      3.48904327e+02  3.03273254e+02  1.66248596e+02  4.32888306e+02
      1.27046130e+03  6.65592468e+02  6.35078369e+02  1.48734253e+02
      1.37026245e+02  2.91291412e+02  8.06734680e+02 -7.09632568e+01
      5.77357788e+02  1.45179199e+02  2.30741592e+02  2.32121606e+03
      1.62972855e+02  3.39676392e+02  6.39116135e+01  5.23073181e+02
      4.80940521e+02  5.13567505e+02  5.40800552e+01  2.05246246e+02
      1.85131821e+02  2.56636566e+02  1.00222931e+03  1.61632633e+01
      3.04881500e+02  3.64506866e+02  4.75019684e+02  8.14916565e+02
      5.98925171e+02  1.82630188e+03  6.35017273e+02  3.20335388e+01
      1.39826990e+03  1.24220728e+03  1.66119659e+02  3.91082535e+01
      1.88092484e+02  1.44760620e+02  1.85694000e+02  1.59106763e+03
      5.47648376e+02  2.59910706e+02  3.04626617e+02  1.09885353e+02
      7.63078690e+01  3.63493256e+02  2.12147064e+02  4.63291565e+02
      2.16754868e+02  2.98912628e+02  9.71348038e+01  6.79429321e+02
      1.39250012e+03  2.50969559e+02  1.84749863e+02  2.58112457e+02
      2.84744110e+02  1.52295569e+03  5.75779114e+02  3.33320740e+02
      2.17021835e+02  1.25676990e+03  6.36641006e+01  2.76039154e+02
      3.87977356e+02  1.58667999e+02  7.72599640e+01  2.31192456e+03
      2.84100616e+02  3.27738251e+02  3.61351837e+02  1.80805862e+02
      3.49743378e+02  2.90268372e+02  3.03945703e+03  7.70232727e+02
      6.08904785e+02  4.12997711e+02  4.90653046e+02  3.18634094e+02
      3.60800171e+02  3.93493134e+02  3.19831238e+02  4.44124939e+02
      1.25279980e+03  7.97949036e+02  9.84784180e+02  2.47170850e+03
      2.88031677e+02  2.16116104e+02  1.44530167e+02  2.99998169e+02
      3.47234375e+02  3.42700775e+02  1.94019922e+03  4.49503235e+02
      2.61990387e+02  9.11503906e+02  1.66112656e+02  4.17357941e+02
      4.60706909e+02  4.88373444e+02 -3.01989555e+00  3.39539246e+02
      2.40639136e+03  1.13161148e+02  4.03307709e+02  5.61906982e+02
      2.18376740e+02  1.67848587e+02  1.52573706e+03  1.64892578e+03
      1.40171594e+03  8.02975769e+01  1.41284790e+02  4.48093018e+02
      4.66194916e+01  2.60232697e+02  9.43157593e+02  4.82878113e+02
      4.98508026e+02  4.41490326e+02  2.83404510e+02  1.04541313e+02
      1.91338013e+02  7.81741333e+02  1.58338745e+03  8.47134766e+02
      4.75871849e+01  2.15647125e+02  2.45800735e+02  2.37598236e+02
      1.21491570e+02  3.18225006e+02  3.92684326e+02  4.89742096e+02
      1.48388306e+02 -1.00017532e+02  4.00566498e+02  5.82547058e+02
      3.59671600e+02  5.99908508e+02  3.82034454e+02  4.60892578e+02
      9.72221558e+02  1.76659317e+02  2.81817963e+02  2.63705078e+02
      1.36838242e+02  5.13783760e+01  1.20159698e+02  1.79854163e+03
      9.87549683e+02  1.67043506e+03  1.33424301e+02  2.34464185e+03
      3.67371368e+02  9.89709717e+02  1.09057747e+02  1.78580765e+02
      2.41831528e+02  5.42425354e+02  1.04440804e+02  2.14685349e+02
      3.25215637e+02  8.33496857e+01  2.37408493e+02  1.93862476e+03
      2.41315338e+02  2.31617386e+02  1.85130753e+02  2.57904968e+02
      5.43904907e+02  2.00843704e+02  1.75218323e+02  2.15709570e+03
      1.76589282e+03  8.32388794e+02  9.38851471e+01  1.59046661e+02
      2.58144958e+02  8.00867432e+02  9.07782974e+01  1.71096024e+02
      3.72474487e+02  2.48985733e+02  1.08059387e+02  1.52318884e+03
      1.44354477e+02  3.75442810e+02  2.67082336e+02  2.91539459e+02
      1.78012866e+03  9.55291626e+02  3.01872253e+02  5.04593475e+02
      3.49719385e+03  1.67939987e+02  2.45552414e+02  1.58321350e+02
      3.62754517e+02  2.36906342e+02  1.25433464e+02  5.26431007e+01
      8.50802734e+02  1.86448727e+01  6.73869934e+01  4.69090485e+02
      9.68686890e+02  3.31723785e+02  3.24050598e+02  4.12371918e+02
      1.75563019e+02  5.49978271e+02  2.49977188e+02  1.05681046e+02
      6.98239685e+02  1.55008942e+02  3.44269226e+02  2.26815747e+03
      1.36185266e+03  2.61694458e+02  1.59075256e+03  1.96167084e+02
      1.69697464e+02  1.53008240e+02  1.69521875e+03  4.42548904e+01
      1.56372299e+02  5.51567932e+02  3.78045801e+03  1.33255298e+03
      2.88758453e+02  7.32131882e+01  2.79947784e+02  1.46032257e+02
      3.52029694e+02  8.34624512e+02  1.10583289e+03  1.66883087e+02
      1.98059647e+02  1.69193668e+01  2.81984741e+03  2.00211487e+02
      3.76977631e+02  3.72869165e+03  3.86468231e+02  4.79376129e+02
      5.35888611e+02  1.38502701e+02  1.11063026e+02  3.31162933e+02
      1.59291699e+03  1.07488853e+02  1.76164612e+03  2.25232697e+02
      6.34528870e+02  2.53564484e+02  2.05309341e+02  2.70904785e+02
      8.78279800e+01  2.64118103e+02  2.45023575e+02  4.47741425e+02
      5.29017029e+02  3.99140930e+02  1.93221603e+02  3.48058533e+02
      1.13346085e+02  2.05502274e+02  1.83793335e+02  1.83501257e+03
      9.48103271e+02  1.87172272e+02  3.51575439e+02  1.50246216e+02
      2.03540451e+02  5.71384827e+02  9.97154602e+02  2.51445038e+02
      2.33820053e+02  2.51760803e+02  8.58963745e+02  6.44952209e+02
      1.68396927e+02  3.13214172e+02  2.41832474e+02  2.30253937e+02
      3.33285492e+02  8.84771301e+02  3.66306519e+02  2.25259628e+02
      7.45116653e+01  1.88272842e+02  3.50509583e+02  1.05985916e+02
      7.54002380e+02  1.69724838e+02  3.38433685e+02  6.85980652e+02
      1.24358902e+02  2.05054370e+03  1.46463171e+03  2.81890045e+02
      2.73572601e+02  1.54941174e+03  2.32315704e+02  3.19291321e+02
      1.09177271e+03  4.31754120e+02  1.65819656e+02  3.22652405e+02
      1.04191321e+03  2.01180893e+02  3.66893959e+01  1.84571155e+03
      4.38273712e+02  9.76246948e+01  3.70254639e+02  2.63090637e+02
      3.21447815e+02  1.06399246e+02  2.18342163e+02  1.57625824e+02
      3.42859863e+02  2.14378784e+03  1.73790710e+03  8.95364441e+02
      1.24922310e+02  2.58686157e+02  2.50284317e+02  1.19320938e+02
      6.83423340e+02  1.85400659e+03  1.25831139e+02  2.54847794e+02
      1.19463220e+03  1.41956528e+02  3.19649933e+02  1.51736865e+03
      1.07161694e+03  8.30112793e+02  1.90714584e+02  7.89664368e+02
      7.70470428e+01  1.74362595e+02  2.30572485e+03  8.72763184e+02
      1.96585999e+02  2.00351318e+02  1.52685623e+02  9.99888611e+01
      1.78690323e+02  1.19651749e+02  4.26721375e+02  1.69861008e+02
      3.15717255e+02  1.75727829e+02  1.70803235e+03  1.12606529e+02
      1.46348035e+03  2.70257019e+02  8.12248962e+02  4.23125153e+02
      3.45750427e+02  2.08394485e+02  3.88527496e+02  2.18026031e+02
      1.91362744e+03  5.65739197e+02  1.09077405e+03  3.75364807e+02
      4.66786041e+02  3.08960785e+02  1.98065338e+02 -1.52636080e+01
     -1.67019691e+01  1.27049768e+03  3.74325635e+03  7.23180359e+02
      6.74367310e+02  3.56473541e+02  3.11020361e+03  3.07694794e+02
      6.35352417e+02  6.07482056e+02  2.41411087e+02  5.84194458e+02
      2.65085175e+02  6.72107483e+02  1.86608017e+02  5.58992424e+01
      3.93930725e+02  1.55344498e+02  7.83700684e+02  8.20833740e+01
      1.50044556e+02  2.52949402e+02  1.82244781e+02  1.28107117e+03
      4.59742126e+02  9.80948059e+02  1.10259651e+02  1.04636487e+03
      2.47768677e+02  2.40229834e+03  1.80060867e+02  1.46516449e+02
      1.21895142e+03  2.53014618e+02  1.04789619e+02  9.91652145e+01
      7.35182434e+02  1.87141708e+02  1.23720741e+02  3.84509003e+02
      5.80164429e+02  7.37957092e+02  2.30634674e+02  5.48963890e+01
      8.48840881e+02  1.92021399e+03  4.96894989e+02  3.39481232e+02
      1.93248688e+02  1.19749182e+03  1.33270859e+02 -3.29869690e+01
      6.24579811e+00  5.27376099e+02  3.71989777e+02  6.01404602e+02
      2.53289490e+02  2.52874969e+02  1.17606827e+02  1.50570602e+02
      1.80252820e+03  9.20445496e+02  1.59568954e+02  9.52542114e+02
      1.96387253e+02 -2.30038910e+01  2.07774277e+02  4.01279716e+01
      3.08565643e+02  3.40201141e+02  1.01261833e+02  1.39362708e+03
      4.45596802e+02  6.08425293e+02  6.43230103e+02  1.43999908e+02
      2.97880811e+03  1.83735764e+02  2.22824799e+02  1.88917877e+02
      1.04208264e+03  5.96443848e+02  4.75586151e+02  4.80196655e+02
      1.12557320e+02  2.39519348e+02  7.65945206e+01  2.46692578e+03
      6.78590775e+01  3.48308838e+02  1.36529175e+02  2.19640063e+03
     -4.75307587e+02  8.28671204e+02  1.39788681e+02  1.14494238e+03
      3.38327075e+03  2.08119949e+02 -1.78354855e+01  1.17855721e+02
      6.92091797e+02  6.34735657e+02  1.69312878e+03  3.34734772e+02
      2.68597046e+02  5.25180237e+02  4.14603424e+02  8.04950623e+02
      4.95139465e+02  2.99783936e+03  1.93170496e+03  4.82467743e+02
      2.88063019e+02  2.00737350e+02  5.24208565e+01  1.11877588e+03
      2.84692780e+02  1.77043488e+02  2.14026352e+02  2.69729126e+02
      1.60095581e+03  4.12899811e+02  2.85422266e+03  2.59551514e+02
      4.91656891e+02  3.65386902e+02  4.52641945e+01  1.77132172e+02
      1.25764587e+03  1.49701061e+01  1.68365405e+03  3.20215240e+02
      3.88688751e+02  7.93506958e+02  1.73418533e+02  3.50657654e+02
      9.97492065e+02  6.49841431e+02  3.61858734e+02  3.06138824e+02
      6.51159973e+02  1.12350182e+02 -8.24393616e+01  7.38424622e+02
      1.42100937e+02  9.47193909e+02  1.12723083e+03  2.01379608e+02
      3.70358643e+02  3.80812347e+02  1.29952667e+02  1.86652100e+02
      8.80943909e+02  8.55725784e+01  7.97315750e+01  3.67850342e+02
      6.66679810e+02  2.32018814e+02  1.42431396e+02  2.27699292e+03
      2.23498489e+02  1.29124466e+02  3.86191711e+02  5.76727600e+02
     -2.43269897e+00  1.87899689e+02  2.43247925e+02  9.89633484e+02
      3.63026709e+03  2.97164062e+02  3.96500977e+02  2.26345483e+03
      2.93700500e+02  1.16185738e+02  9.84792969e+02  1.85687576e+02
      8.35583801e+01  8.27959412e+02  3.27866943e+02  1.48456421e+02
      1.20673622e+02  1.59584488e+02  2.76185638e+02  2.41270523e+02
      2.46458069e+02  2.62817078e+02  5.52236061e+01  2.27915405e+03
      7.81906067e+02  1.35697037e+02  3.59880615e+02  6.06552307e+02
      1.19331596e+02  1.40968152e+03  1.18503128e+02  2.72843536e+02
      2.17142749e+03  1.77534851e+02  5.33697327e+02  3.96175018e+02
      1.56222729e+03  1.85182312e+02  4.03195770e+02  1.38326340e+02
      7.19732849e+02  3.87026550e+02  9.59407837e+02  1.76823746e+02
      2.40826462e+02  2.11488831e+02  3.79759613e+02  1.61083447e+03
      7.83074463e+02  6.20596130e+02  1.17893410e+02  1.74996902e+02
      2.93490387e+02  1.21780731e+02  1.42228470e+02  8.58070496e+02
      5.33133606e+02  1.82949084e+03  3.83850983e+02  2.81051910e+02
      1.14376160e+03  1.25448860e+02  4.91631317e+02  3.71389923e+02
      3.11295197e+02  1.08042316e+01  3.72220428e+02  1.85665329e+02
      4.41311462e+02  7.80131104e+02  5.63219482e+02  9.62498718e+02
      2.51311356e+02  2.28041962e+02  4.31815643e+02  2.20815170e+02
      3.11100922e+02  1.82002533e+02  7.56204956e+02  1.31195480e+02
      2.83104736e+02  7.89016876e+01  1.62565521e+02  5.17634964e+01
      6.65394211e+01  6.38360825e+01  2.03577026e+02  2.12364349e+02
      7.41269531e+02  1.98785995e+02  5.39296448e+02  1.67561966e+02
      5.31571465e+01  6.40320496e+02  3.28584766e+03  5.72616638e+02
      4.72532837e+02  1.55828735e+02  1.08372314e+02  3.76482239e+02
      3.06694214e+02  2.19954407e+02  2.56679688e+02  1.15186829e+02
      1.81407181e+02  4.92219818e+02  1.90110925e+03  7.16473206e+02
      7.31663452e+02  3.44044037e+02  2.27113403e+03  2.61841736e+02
      1.97818274e+03  3.06999170e+03  3.31494415e+02  1.02517769e+02
      4.74121063e+02  3.46341034e+02  3.22829926e+02  4.10938623e+03
      1.72009607e+03  1.53059021e+02  1.20489612e+03  1.29884247e+02
      1.72567761e+03  2.22473663e+02  7.32814941e+01  4.81049042e+01
      9.60302185e+02  1.78356354e+02  2.64828613e+02  4.31595306e+02
      2.57672388e+03  8.03229553e+02  2.63416656e+02  5.70598267e+02
      2.21519821e+02  8.52345352e+01  1.03397423e+02  2.49335327e+02
      1.87405121e+02  1.64562592e+02  4.98956512e+02  1.47029556e+02
      2.73254303e+02  2.47680466e+02  1.50185193e+03  3.49289459e+02
      6.57022888e+02  4.86915131e+01  9.94078430e+02  1.99401596e+02
      1.83115936e+02  2.23544907e+02  2.12355444e+03  2.06977646e+02
      6.09792480e+01  2.03981885e+03  1.39358459e+02  8.88781006e+02
      1.35718396e+03  2.61560181e+02  2.84803925e+02  3.76943726e+02
      6.29234009e+02  5.27583496e+02  6.89583313e+02  5.18032959e+02
      2.36666595e+02  5.64006714e+02  5.58505127e+02  1.87142929e+02
      6.22375732e+02  4.57115692e+02  3.17284058e+03  2.42144272e+02
      4.38534241e+02  1.24668732e+02 -5.15918999e+01  3.57901794e+02
      4.49897675e+02  4.17086182e+02  5.83136536e+02  1.99312103e+02
      4.56380402e+02  2.51394997e+01  3.18244667e+01  1.99558374e+03
      3.51118311e+03  3.17629297e+03  6.45478668e+01  1.55870361e+02
      2.90998596e+02  7.85725220e+02  2.70779541e+03  1.22905830e+02
      5.45911011e+02  2.10885086e+02  2.30742371e+02  2.41436722e+02
      2.99857788e+02  7.91165588e+02  2.69920258e+02  2.58889191e+02
      1.80914429e+02  3.81250946e+02  3.14171387e+02  4.89022919e+02
      5.32942322e+02  8.75208511e+01  1.55055725e+02  3.06241760e+02
      2.70722748e+02  7.86472412e+02  4.45209389e+01  8.31737900e+01
      1.17956982e+03  1.05403748e+02  8.36016785e+02  2.53621506e+02
      1.82473206e+03  4.10196289e+02  1.31214294e+02  3.84693359e+02
      1.14125720e+03  5.61655579e+02  2.54695694e+02  8.44939331e+02
      9.82484314e+02  4.00706970e+02  1.48813187e+02  8.29558716e+02
      3.64597046e+02  2.62608063e+02  2.25191650e+02  1.23051123e+03
      1.46820007e+02  3.11711884e+02  4.66297943e+02  2.72489307e+03
      1.92998810e+02  3.21038910e+02  3.09008759e+02  3.30511627e+02
      3.18119293e+02  1.57583237e+02  1.26077917e+03  9.21392578e+02
      2.79643463e+02  3.06381958e+02  7.82525864e+01  2.54546704e+03
      2.15709570e+03  9.42536774e+01  2.53114532e+02  5.79955078e+02]


.. code:: ipython3

    mse = mean_squared_error(y_test, ypred)
    print("MSE: %.2f" % mse)


.. parsed-literal::

    MSE: 1298440.04


.. code:: ipython3

    rmse = sqrt(mean_squared_error(y_test, ypred))
    print("RMSE: %.2f" %rmse)


.. parsed-literal::

    RMSE: 1139.49


.. code:: ipython3

    evaluation = rmse/ (max(y_test))
    print("Evaluation: %.2f" %evaluation)


.. parsed-literal::

    Evaluation: 0.12


.. code:: ipython3

    ypred_xgbr = xgbr.predict(test_data.values)

.. code:: ipython3

    submission = pd.DataFrame()
    submission["comp_id"] = index_col='comp_id'
    submission["views"] = ypred_xgbr
    
    submission.to_csv('sol_ypred_xgbr.csv', index=False)

.. code:: ipython3

    #XGBoost hyper-parameter tuning
    #def hyperParameterTuning(X_train, y_train):
        #param_tuning = {
            #'learning_rate': [0.01, 0.1],
            #'max_depth': [3, 5, 7, 10],
            #'min_child_weight': [1, 3, 5],
            #'subsample': [0.5, 0.7],
            #'colsample_bytree': [0.5, 0.7],
            #'n_estimators' : [100, 200, 500],
            #'objective': ['reg:squarederror']
       # }
    
        #xgbr = XGBRegressor()
    
        #gsearch = GridSearchCV(estimator = xgbr,
                               #param_grid = param_tuning,                        
                               #scoring = 'neg_mean_absolute_error', #MAE
                               #scoring = 'neg_mean_squared_error',  #MSE
                               #cv = 5,
                               #n_jobs = -1,
                               #verbose = 1)
    
        #gsearch.fit(X_train,y_train)
    
        #return gsearch.best_params_

.. code:: ipython3

    #xgbr = XGBRegressor(
            #objective = 'reg:mean_squared_error',
            #colsample_bytree = 0.5,
            #learning_rate = 0.05,
            #max_depth = 6,
            #min_child_weight = 1,
            #n_estimators = 1000,
            #subsample = 0.7)

.. code:: ipython3

    #Importing Packages
    import matplotlib.pyplot as plt
    
    from xgboost import XGBRegressor
    from xgboost import XGBRFRegressor
    from sklearn.model_selection import GridSearchCV
    
    from sklearn.metrics import mean_squared_error
    from sklearn.metrics import mean_absolute_error
    
    from sklearn.impute import SimpleImputer
    imputer = SimpleImputer(missing_values=np.nan, strategy='mean')

.. code:: ipython3

    def hyperParameterTuning(X_train, y_train):
        param_tuning = {
            'learning_rate': [0.01, 0.1],
            'max_depth': [3, 5, 7, 10],
            'min_child_weight': [1, 3, 5],
            'subsample': [0.5, 0.7],
            'colsample_bytree': [0.5, 0.7],
            'n_estimators' : [100, 200, 500],
            'objective': ['reg:squarederror']
        }
    
        xgb_model = XGBRegressor()
    
        gsearch = GridSearchCV(estimator = xgb_model,
                               param_grid = param_tuning,                        
                               scoring_MAE = 'neg_mean_absolute_error', #MAE
                               scoring_MSE = 'neg_mean_squared_error',  #MSE
                               cv = 5,
                               n_jobs = -1,
                               verbose = 1)
    
        gsearch.fit(X_train,y_train)
    
        return gsearch.best_params_

.. code:: ipython3

    xgb_model = XGBRegressor(
            objective = 'reg:squarederror',
            colsample_bytree = 0.5,
            learning_rate = 0.05,
            max_depth = 6,
            min_child_weight = 1,
            n_estimators = 1000,
            subsample = 0.7)
    
    %time xgb_model.fit(X_train, y_train, early_stopping_rounds=5, eval_set=[(X_test, y_test)], verbose=False)
    
    y_pred_xgb = xgb_model.predict(X_test)
    
    mae_xgb = mean_absolute_error(y_test, y_pred_xgb)
    mse_xgb = mean_squared_error(y_test, y_pred_xgb)
    
    print("MAE: ", mae_xgb)
    print("MSE: ", mse_xgb)


.. parsed-literal::

    CPU times: user 1min 36s, sys: 891 ms, total: 1min 37s
    Wall time: 35.1 s
    MAE:  529.7664769829644
    MSE:  1143347.2274445735


.. code:: ipython3

    rmse = sqrt(mean_squared_error(y_test, y_pred_xgb))
    print("RMSE: %.2f" %rmse)


.. parsed-literal::

    RMSE: 1069.27


.. code:: ipython3

    evaluation = rmse/ (max(y_test))
    print("Evaluation: %.2f" %evaluation)


.. parsed-literal::

    Evaluation: 0.11


.. code:: ipython3

    y_pred_xgb_model = xgb_model.predict(test_data.values)

.. code:: ipython3

    submission = pd.DataFrame({'comp_id':index_col,'views':y_pred_xgb_model})
    
    # Save results
    submission.to_csv("submission_xgb_model.csv",index=False)
    
    #submission = pd.DataFrame()
    #submission["comp_id"] = index_col='comp_id'
    #submission["views"] = ypred_xgbr
    
    #submission.to_csv('sol_ypred_xgbr.csv', index=False)

.. code:: ipython3

    from sklearn.ensemble import GradientBoostingRegressor #For Regression

.. code:: ipython3

    regr = GradientBoostingRegressor(n_estimators=100, learning_rate=0.1, max_depth=6)
    regr.fit(X_train, y_train)




.. parsed-literal::

    GradientBoostingRegressor(max_depth=6)



.. code:: ipython3

    y_pred = regr.predict(X_test)

.. code:: ipython3

    mae = mean_absolute_error(y_test, y_pred)
    mse = mean_squared_error(y_test, y_pred)
    
    print("MAE: ", mae)
    print("MSE: ", mse)


.. parsed-literal::

    MAE:  574.054938786696
    MSE:  1319439.1737216422


.. code:: ipython3

    rmse = sqrt(mean_squared_error(y_test, y_pred))
    print("RMSE: %.2f" %rmse)


.. parsed-literal::

    RMSE: 1148.67


.. code:: ipython3

    evaluation = rmse/ (max(y_test))
    print("Evaluation: %.2f" %evaluation)


.. parsed-literal::

    Evaluation: 0.12


.. code:: ipython3

    y_pred = regr.predict(test_data.values)

.. code:: ipython3

    submission = pd.DataFrame({'comp_id':index_col,'views':y_pred})
    
    # Save results
    submission.to_csv("submission_regr.csv",index=False)

.. code:: ipython3

    def hyperParameterTuning(X_train, y_train):
        param_tuning = {
            'learning_rate': [0.0001, 0.001, 0.01, 0.1, 0.2, 0.3],
            'max_depth': [3, 5, 7, 10],
            'min_child_weight': [1, 3, 5],
            'subsample': [0.5, 0.7],
            'colsample_bytree': [0.5, 0.7],
            'n_estimators' : [100, 200, 400, 600, 800, 1000],
            'objective': ['reg:squarederror']
        }
    
        xgbr_model = XGBRegressor()
    
        gsearch = GridSearchCV(estimator = xgbr_model,
                               param_grid = param_tuning,                        
                               scoring_MAE = 'neg_mean_absolute_error', #MAE
                               scoring_MSE = 'neg_mean_squared_error',  #MSE
                               cv = 10,
                               n_jobs = -1,
                               verbose = 1)
    
        gsearch.fit(X_train,y_train)
    
        return gsearch.best_params_

.. code:: ipython3

    xgbr_model = XGBRegressor(
            objective = 'reg:squarederror',
            colsample_bytree = 0.5,
            learning_rate = 0.01,
            max_depth = 8,
            min_child_weight = 1,
            n_estimators = 1000,
            subsample = 0.7)
    
    %time xgbr_model.fit(X_train, y_train, early_stopping_rounds=5, eval_set=[(X_test, y_test)], verbose=False)
    
    y_pred_xgbr = xgbr_model.predict(X_test)
    
    mae_xgbr = mean_absolute_error(y_test, y_pred_xgbr)
    mse_xgbr = mean_squared_error(y_test, y_pred_xgbr)
    
    print("MAE: ", mae_xgbr)
    print("MSE: ", mse_xgbr)


.. parsed-literal::

    CPU times: user 7min 25s, sys: 3.98 s, total: 7min 29s
    Wall time: 3min 2s
    MAE:  502.21637910630966
    MSE:  1133236.8376068969


.. code:: ipython3

    rmse = sqrt(mean_squared_error(y_test, y_pred_xgbr))
    print("RMSE: %.2f" %rmse)


.. parsed-literal::

    RMSE: 1064.54


.. code:: ipython3

    evaluation = rmse/ (max(y_test))
    print("Evaluation: %.2f" %evaluation)


.. parsed-literal::

    Evaluation: 0.11


.. code:: ipython3

    y_pred_xgbr_model = xgb_model.predict(test_data.values)
    
    submission = pd.DataFrame({'comp_id':index_col,'views':y_pred_xgbr_model})
    
    # Save results
    submission.to_csv("submission_xgbr_model.csv",index=False)


