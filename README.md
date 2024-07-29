# streamlit
streamlit code explanation
=IF(OR(Product="GPS - Cards", Product="GPS - Liquidity & Channel", Product="GPS - Term Accounts", Product="GPS - Saving & Deposits Accounts", Product="GPS - PayMe & Peak", Product="GPS - International Payments", Product="GPS - Current Accounts", Product="GPS - Domestic Payments"), "GPS",
IF(OR(Product="GM - Forex - Cash", Product="GM - Forex Options", Product="GM - Fixed Income Rates", Product="GM - Metals", Product="GM - Other", Product="GM - Futures"), "FX",
IF(OR(Product="GTRF - Guarantees", Product="GTRF - Receivables Finance", Product="GTRF - Documentary Trade", Product="GTRF - CSTF", Product="GTRF - Supply Chain Solutions", Product="GTRF - Trade Loans"), "GTS", "Not TxB")))
