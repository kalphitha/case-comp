# case-comp
# GCPL Bank Rationalization Model

## Overview

The **GCPL Bank Rationalization Model** is an interactive, browser-based decision-support tool designed to evaluate banking relationships, optimize the number of banking partners, and identify potential account consolidation opportunities across multiple countries.

The model uses a weighted scoring system and a country-level banking coverage matrix to classify banks as core partners, regional partners, or exit candidates while identifying account-transfer possibilities and areas requiring further verification.

## Key Features

- **Weighted Bank Scorecard:** Evaluates banks based on seven criteria: country coverage, cost, liquidity and pooling, connectivity and data, payments and FX, credit support, and service.
- **Customizable Weights:** Allows users to adjust the importance of each evaluation criterion.
- **Configurable Thresholds:** Enables users to modify the minimum scores required for core and regional bank classifications.
- **Credit and Regulatory Gate:** Flags banks that fail required credit or regulatory checks for further review.
- **Country Coverage Matrix:** Displays existing account coverage and the operational availability of alternative banks across countries.
- **Account Transfer Analysis:** Identifies potential alternative banks for account migration and highlights locations requiring verification.
- **Automated Recommendations:** Generates bank classifications and supporting explanations based on the selected inputs.
- **Interactive Interface:** Allows users to update scores, weights, coverage statuses, and decision thresholds directly in the browser.
- **Reset Functionality:** Restores the model to its initial assumptions.

## Bank Evaluation Criteria

The model evaluates banks using the following default weights:

| Evaluation Criterion | Weight |
|---|---:|
| Country Coverage | 25% |
| Cost | 20% |
| Liquidity and Pooling | 15% |
| Connectivity and Data | 15% |
| Payments and FX | 10% |
| Credit Support | 10% |
| Service | 5% |
| **Total** | **100%** |

Country coverage is calculated automatically using the country-level coverage matrix. Other criteria initially receive a neutral score of 3 out of 5 and can be adjusted based on the available evidence.

## Bank Classification

The model categorizes banks into four groups:

- **Core Partner:** Banks meeting the core score threshold and the minimum requirements for liquidity and pooling, connectivity and data, and the credit/regulatory gate.
- **Regional Partner — Keep and Review:** Banks meeting the regional score threshold but not qualifying as core partners.
- **Exit Candidate:** Banks scoring below the regional threshold, subject to account-transfer feasibility and local coverage requirements.
- **Freeze — Gate Failed:** Banks whose credit or regulatory gate has been disabled. The model recommends no new business and further review before any decision.

The default core threshold is 65/100, and the regional threshold is 55/100. Both can be changed through the interface.

## Account Coverage and Transfer Feasibility

The country-level matrix helps assess whether accounts can potentially be consolidated into other banking partners.

Coverage statuses include:

- **Acct:** An account currently exists with the bank.
- **Yes:** The bank is confirmed to operate in the country.
- **No:** The bank is confirmed not to operate in the country.
- **?:** Coverage information requires verification.

The model uses these statuses to suggest potential receiving banks, identify countries where alternative coverage needs confirmation, and flag locations where a local account may need to remain.

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript

The application is self-contained and runs directly in a modern web browser. It does not require a backend server, database, external JavaScript libraries, or a build process.

## How to Run

1. Clone or download this repository.
2. Open `GCPL bank rationalization model.html` in a modern web browser.
3. Review the bank scorecard and update the evaluation criteria.
4. Adjust weights and classification thresholds if necessary.
5. Review the country-level account coverage matrix and verify uncertain entries.
6. Examine the generated classifications and potential account-transfer recommendations.

## Project Structure

```text
GCPL-Bank-Rationalization-Model/
├── GCPL bank rationalization model.html
└── README.md
```

## Assumptions and Limitations

- Initial bank scores, country coverage entries, and decision thresholds are model assumptions that should be validated.
- Some bank-country relationships require further verification.
- Account-transfer recommendations indicate potential alternatives but do not establish actual transfer feasibility.
- The model does not connect to live banking systems or independently verify fees, banking services, credit facilities, or local regulatory requirements.
- Changes made in the browser are not automatically saved to a database or persisted between sessions.

## Disclaimer

This project is an analytical prototype intended to support bank rationalization and treasury decision-making. Its outputs should be validated against reliable data and reviewed by the relevant treasury, credit, compliance, and regulatory teams before any banking relationship or account-closure decisions are made.

