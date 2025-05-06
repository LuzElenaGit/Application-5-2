**1. Business Understanding**

Used car dealerships face constant pressure to price vehicles accurately in a competitive market. Overpricing can lead to stagnating inventory, while underpricing erodes profit margins. The objective of this project is to build a predictive model that estimates a vehicle's market price based on its characteristics—supporting smarter inventory acquisition, pricing strategy, and turnover optimization.

**2. Data Understanding**

The dataset used for this project included over 200,000 vehicle listings across various U.S. states. Key fields analyzed included price, year, odometer reading, condition, fuel type, transmission, vehicle type, and location. Additional vehicle details were enriched by querying an external API using the Vehicle Identification Number (VIN) for each listing, allowing retrieval of standardized information such as make, model, and year. Feature engineering was performed to create meaningful variables such as vehicle age, mileage per year, price per mile, and age-condition interaction. Categorical fields were one-hot encoded, and numerical fields were scaled to improve model performance.

**3. Evaluation**

After testing several machine learning algorithms, XGBoost delivered the best balance of accuracy and speed. Prior to settling on XGBoost, countless models were evaluated, including various linear regressors, ensemble methods, and deep learning architectures. Some achieved promising training results but required excessive runtimes—up to 6 hours per iteration—making them impractical for deployment. Many others failed to produce competitive metrics, significantly underperforming in terms of both error rates and generalization. Ultimately, using cross-validation and hyperparameter tuning, XGBoost achieved:

Mean Squared Error (MSE): $2.57 million

Mean Absolute Error (MAE): $505

R² Score: 0.985

This means the model can predict vehicle prices with high reliability and a typical error margin under $510, making it a powerful tool for pricing decisions. Key predictors of price were vehicle age, condition, mileage, transmission type, and location.

**4. Deployment**

The final XGBoost model is fast and scalable, completing predictions on large datasets in under 3 minutes. We recommend integrating this model into your pricing workflow to:
Evaluate trade-ins and auction opportunities with greater accuracy
Detect undervalued vehicles for acquisition
Optimize pricing to increase turnover and maximize profitability
For further enhancement, the model can be integrated into a dashboard or pricing tool used by your sales and purchasing teams.
