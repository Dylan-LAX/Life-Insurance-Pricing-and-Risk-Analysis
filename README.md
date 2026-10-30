
# Life Insurance Pricing & Risk Analysis

## Project Overview

The main purpose of this project is to price different life insurance products and analyse potential risks that insurance companies might face. This is achieved by developing actuarial models in Python.

Makeham's mortality law is applied to calculate survival and death probabilities, and the Expected Present Value (EPV) approach and the Equivalence Principle are applied to determine insurance premiums.

The project covers Term Life Insurance, Whole Life Insurance, and Endowment Insurance. It also includes portfolio cash flow analysis, interest rate and mortality sensitivity analysis, and liability concentration analysis.

## Actuarial Methodology

### Makeham Mortality Model

The Makeham mortality model is used to estimate mortality rates and calculate survival and death probabilities for policyholders of different ages.

The force of mortality is defined as:

The force of mortality is defined as:

**μₓ = A + Bcˣ**

The model uses the following parameters:

| Parameter | Value |
|-----------|-------|
| A | 0.00022 |
| B | 0.0000027 |
| c | 1.124 |

Based on these assumptions, annual survival and death probabilities are calculated and used in subsequent insurance pricing calculations.

### Expected Present Value (EPV)

The Expected Present Value (EPV) approach is used to calculate the expected value of future insurance benefits, taking into account mortality probabilities, the time value of money, and the sum insured.

Three types of life insurance products are considered:

- **Term Life Insurance:** A death benefit is payable only if the policyholder dies within the specified policy term.
- **Whole Life Insurance:** A death benefit is payable upon the policyholder's death, subject to the model's terminal age of 100.
- **Endowment Insurance:** A death benefit is payable during the policy term, or a maturity benefit is payable if the policyholder survives to the end of the term.

The EPV of insurance benefits is calculated by combining the probability of each benefit payment with its discounted value.

### Premium Calculation

The Equivalence Principle is applied to calculate insurance premiums based on the Expected Present Value (EPV) of future benefits and premium payments.

The pricing model calculates three types of premiums:

- **Net Single Premium:** The present value of expected future insurance benefits, assuming a single premium payment.
- **Net Annual Premium:** The annual premium calculated using the EPV of insurance benefits and the present value of future premium payments.
- **Gross Annual Premium:** The annual premium calculated under specified expense assumptions, in addition to expected insurance benefit costs.

The model considers initial expenses, renewal expenses, and commission when calculating expected cash flows and analysing the financial performance of insurance policies.

## Synthetic Insurance Portfolio

A synthetic portfolio of 500 life insurance policies is generated using Python to simulate an insurance company's portfolio.

The portfolio contains three types of insurance products: Term Life Insurance, Whole Life Insurance, and Endowment Insurance.

Each policy contains the following attributes:

- **Policy ID:** A unique identifier for each insurance policy.
- **Age:** The policyholder's entry age, ranging from 20 to 60.
- **Term:** The policy term, selected from 10, 15, 20, or 25 years.
- **Sum Insured:** The insurance coverage amount, ranging from €50,000 to €500,000.
- **Product Type:** The type of life insurance product.

A fixed random seed of 25 is used to ensure that the generated portfolio is reproducible.

The synthetic portfolio provides a basis for insurance pricing, cash flow projections, and portfolio risk analysis.

## Portfolio Risk Analysis

### Expected Cash Flow Analysis

The model projects annual expected net cash flows for the insurance portfolio by considering premium income, expected death benefits, maturity benefits, and expense assumptions.

Cash flow projections are used to investigate how insurance liabilities and premium income change over time.

Particular attention is given to Endowment Insurance, where maturity benefit payments may create significant cash outflows in specific years.

This analysis highlights potential liquidity risks and the importance of Asset-Liability Management (ALM) in ensuring that insurance companies can meet their future obligations.

### Interest Rate Sensitivity Analysis

Interest rate sensitivity analysis is conducted to investigate how changes in the assumed interest rate affect the Expected Present Value (EPV) of insurance benefits.

Different interest rate scenarios are applied to the pricing model to evaluate the relationship between discount rates and insurance liabilities.

Generally, a higher interest rate reduces the present value of future insurance benefit payments, while a lower interest rate increases their present value.

This analysis highlights the importance of interest rate assumptions in insurance pricing, liability valuation, and Asset-Liability Management (ALM).

### Mortality Sensitivity Analysis

Mortality sensitivity analysis is performed to investigate how changes in mortality assumptions affect expected insurance benefit costs.

By adjusting mortality assumptions, the model evaluates how the EPV of insurance benefits responds to different mortality scenarios.

For death benefit insurance, higher mortality generally increases the expected cost of death benefits, although the overall impact depends on the insurance product and its benefit structure.

This analysis demonstrates the importance of mortality risk in actuarial pricing and insurance liability management.

### Liability Concentration Analysis

Liability concentration analysis is conducted to investigate how expected insurance benefit liabilities are distributed across different insurance products and policyholder groups.

The analysis examines the distribution of Benefit EPV and identifies potential concentrations of insurance liabilities.

Particular attention is given to product-level liability concentration and the relationship between the number of insurance policies and their expected benefit obligations.

This analysis provides insights into portfolio risk exposure and supports the identification of potential risk concentrations.

## Key Findings

The analysis provides several insights into the pricing and risk characteristics of the synthetic insurance portfolio.

### Liability Concentration

One of the most significant findings is the concentration of expected benefit liabilities in Endowment Insurance.

Endowment Insurance represents approximately **31.6% of the total policies**, but contributes approximately **68.15% of the portfolio's total Benefit EPV**.

This indicates that the distribution of expected benefit liabilities differs significantly from the distribution of policy counts.

Such concentration may create potential liquidity and Asset-Liability Management (ALM) challenges, particularly when maturity benefits become payable.

### Interest Rate Risk

The interest rate sensitivity analysis demonstrates that the valuation of future insurance benefits is sensitive to changes in discount rates.

Lower interest rates generally increase the present value of future benefit payments, while higher interest rates reduce their present value.

This highlights the importance of interest rate assumptions when pricing insurance products and evaluating long-term insurance liabilities.

### Mortality Risk

The mortality sensitivity analysis demonstrates that changes in mortality assumptions can affect expected insurance benefit costs.

The impact depends on the structure of the insurance product, including whether benefits are payable upon death or survival.

This illustrates the importance of understanding mortality risk when evaluating insurance liabilities.

### Cash Flow and Liquidity Risk

The expected cash flow analysis demonstrates how premium income, death benefits, maturity benefits, and expenses contribute to the portfolio's projected net cash flows.

Endowment Insurance maturity payments may generate significant cash outflows in particular years.

These findings highlight the importance of liquidity planning and coordinating future asset and liability cash flows.

## Model Assumptions and Limitations

The project is developed for educational and analytical purposes. Several assumptions and limitations should be considered when interpreting the results.

### Synthetic Portfolio

The insurance portfolio consists of 500 randomly generated policies rather than real insurance company data.

Real insurance company data is difficult to access because I do not have permission to use it.

Therefore, the results are illustrative and may not represent the characteristics of an actual insurance portfolio.

### Mortality Assumptions

The model uses Makeham's mortality law with fixed parameters to estimate survival and death probabilities.

Actual mortality experience may differ from these assumptions due to factors such as population characteristics and changes in mortality over time.

### Interest Rate Assumptions

The pricing model uses assumed interest rates to discount future insurance benefit payments.

In practice, insurance companies may use more complex interest rate models and market-based discount curves.

### Policyholder Behaviour

The model does not explicitly incorporate all aspects of policyholder behaviour, such as policy lapses and early surrenders.

These factors may affect actual insurance cash flows and liabilities.

### Terminal Age Limitation

The mortality model uses a maximum age of 100.

As a result, Whole Life Insurance projections are limited by this terminal age rather than extending over all possible future lifetimes.

## Technologies Used

The project is developed using Python and the following libraries and tools:

- **Python:** Actuarial modelling, insurance pricing, and risk analysis.
- **NumPy:** Numerical calculations and mortality probability modelling.
- **pandas:** Insurance portfolio generation, data processing, and analysis.
- **Matplotlib:** Data visualisation and presentation of actuarial results.
- **Jupyter Notebook:** Interactive model development, documentation, and analysis.

## Project Structure

The main project files are organised as follows:

- `Life_Insurance_Pricing_and_Risk_Analysis.ipynb` — Main actuarial modelling and risk analysis notebook.
- `requirements.txt` — Required Python libraries.
- `README.md` — Project documentation.

The notebook also generates the following CSV files:

- `insurance_portfolio.csv` — Synthetic insurance portfolio data.
- `survival probabilities.csv` — Modelled survival probability data.

## How to Run

### 1. Download the Repository

Download or clone this GitHub repository to your computer.

### 2. Install Dependencies

Make sure Python and Jupyter Notebook are installed.

Install the required Python libraries using:

```bash
pip install -r requirements.txt
```

### 3. Open the Notebook

Navigate to the project directory and launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `Life_Insurance_Pricing_and_Risk_Analysis.ipynb`.

### 4. Run the Model

Execute all notebook cells in order.

The notebook generates the synthetic insurance portfolio, calculates mortality probabilities and insurance premiums, and performs portfolio cash flow and risk analyses.

## Learning Outcomes

Through this project, I learned how to apply a mortality model to life insurance pricing using Python, given assumptions about the sum insured and interest rates.

I also developed practical skills in building actuarial models, performing calculations, and analysing insurance portfolios to investigate relevant actuarial and business problems.

The project strengthened my understanding of how actuarial mathematics, programming, and quantitative risk analysis can be combined to support insurance pricing and risk management.

