# Store Sales

**Table of Content**
- [Store Sales](#store-sales)
  - [Project Description](#project-description)
  - [Workflow Illustration](#workflow-illustration)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Contributing](#contributing)
  - [License](#license)
  

## Project Description 

*[Link](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data) to data used in this project.* 

This project is a simplified version of the original [Kaggle contest](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data). Instead of predicting daily sales for each store-product combination, the focus here is to explore the best method in predicting sales of the best selling *per-store-per-product* combination (i.e. `Grocery I` at `store_nbr 44`) to illustrate the steps involved in time series analyses.

Turned out that the (S)ARIMA(X) model(s) built using our manual reading using ACF & PACF plots (after data engineering steps) yielded better results than `auto_arima()`.

The output data format is demonstrated in the table below:

| date | store | product_family | predicted_sales |
| ---- | ----- | -------------- |  -------------- |
| '2017-01-01' | 44 | GROCERY_I | 5,029|
| '2017-01-02' | 44 | GROCERY_I | 4,380|

## Workflow Illustration
📌 Check out these report pages for more in-detail explanations in addition to the Jupyter notebooks provided in this repo.
1. [Data Engineering](https://www.notion.so/angie-xiao/1-Data-Engineering-7750f402b0f14db3bb00dbf5c85f5147)
2. [EDA](https://www.notion.so/angie-xiao/2-EDA-f2b02937db4c47da9b02e4ab896c6692)
3. [Understanding the Time Series](https://www.notion.so/angie-xiao/3-Understanding-the-Time-Series-Data-dc7a47281d694f2ebcad183ccadae2dd)
4. [Modeling](https://www.notion.so/angie-xiao/4-Modeling-040b592c3d88411b8c301a2bf5d49b4f)

## Installation
1. Clone the repo:
   ```bash
   # terminal
   git clone https://github.com/angie-xiao/store_sales
   ```
2. Install dependencies:
   ```bash
   # terminal
   pip3 install statsmodels
   pip3 install pmdarima
   pip3 install matplotlib
   pip3 install seaborn
   pip3 install statsforecast
   pip3 install --upgrade plotly
   ```

## Usage

To run the project, use the following command:
```bash
# terminal
jupyter notebook
```
Or directly run cells in the Jupyter notebooks.

## Contributing
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Make your changes.
4. Push your branch: `git push origin feature-name`.
5. Create a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

