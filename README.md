# JP_morgan_quant_research_virtual_experience

# Task 1:

Given datatset : Natural_gas.csv 
Has monthly observations(end of month) for natural gas prices. 

Task (1.1): Interpolate time series to increase available data for subsequent modelling
     (1.2): Extrapolate or forecast prices using the dtata generation process modelled in task 1.1

**Explored models and final proposed solution(file): modelling_natural_gas_prices.ipynb**

Approach: 2 models have been implemented and compared

- model 1: auto regressive models with appropriate lags.
- model 2: additive time series modelling of trend(linear) and seasonality(using forier series)

# Task 2

Create a prototype pricing model that can go through further validation and testing before being put into production. 

You should write a function that is able to use the data you created previously to price the contract. ***The client may want to choose multiple dates to inject and withdraw a set amount of gas***. Consider all the cash flows involved in the product.

The input parameters that should be taken into account for pricing are:

- Injection dates : date X amount of gas bought at $p. 
- Withdrawal dates : date y amount of gas sold at $k
- The prices at which the commodity can be purchased/sold on those dates.
- The rate at which the gas can be injected/withdrawn.
- The maximum volume that can be stored.
- Storage costs.


Write a function that takes these inputs and gives back the value of the contract. **You can assume there is no transport delay and that interest rates are zero. Market holidays, weekends, and bank holidays need not be accounted for.** Test your code by selecting a few sample inputs.

**Suggested solution (file): storage_derivative_pricing.ipynb** 


# task 3

 
The risk manager has collected data on the loan borrowers. The data is in tabular format, with each row providing details of the borrower, including their income, total loans outstanding, and a few other metrics. There is also a column indicating if the borrower has previously defaulted on a loan. You must use this data to build a model that, given details for any loan described above, will predict the probability that the borrower will default (also known as PD: the probability of default). Use the provided data to train a function that will estimate the probability of default for a borrower. Assuming a recovery rate of 10%, this can be used to give the expected loss on a loan.

You should produce a function that can take in the properties of a loan and output the expected loss.

Data file: 'Task 3 and 4_Loan_Data.csv'

**Suggested solution (file): expected_loss_model.ipynb** 
