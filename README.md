# streamlit
streamlit code explanation
=IF(OR(Product="GPS - Cards", Product="GPS - Liquidity & Channel", Product="GPS - Term Accounts", Product="GPS - Saving & Deposits Accounts", Product="GPS - PayMe & Peak", Product="GPS - International Payments", Product="GPS - Current Accounts", Product="GPS - Domestic Payments"), "GPS",
IF(OR(Product="GM - Forex - Cash", Product="GM - Forex Options", Product="GM - Fixed Income Rates", Product="GM - Metals", Product="GM - Other", Product="GM - Futures"), "FX",
IF(OR(Product="GTRF - Guarantees", Product="GTRF - Receivables Finance", Product="GTRF - Documentary Trade", Product="GTRF - CSTF", Product="GTRF - Supply Chain Solutions", Product="GTRF - Trade Loans"), "GTS", "Not TxB")))



# Manually position the legends for each subplot
barcharts.update_layout(
    annotations=[
        dict(x=0.12, y=0.95, xref='paper', yref='paper', text='Revenue', showarrow=False),
        dict(x=0.5, y=0.95, xref='paper', yref='paper', text='Credit RWA', showarrow=False),
        dict(x=0.88, y=0.95, xref='paper', yref='paper', text='Net EP', showarrow=False),
        dict(x=0.12, y=0.5, xref='paper', yref='paper', text='Total', showarrow=False),
        dict(x=0.5, y=0.5, xref='paper', yref='paper', text='Other', showarrow=False)
    ],
    legend_tracegroupgap=300,  # Control the gap between trace groups to separate legends
)

# Adjust axes if necessary
barcharts.update_xaxes(tickvals=graph_df_pivot.index, ticktext=[str(Year) for Year in graph_df_pivot.index])

# Show the final plot
barcharts.show()










# Update layout to place legends below each subplot
barcharts.update_layout(
    width=1700, 
    height=900, 
    barmode='stack',
    showlegend=True,
    legend=dict(
        orientation="h",  # Horizontal legend
        yanchor="top",     # Align legend to top of y axis
        y=-0.2,            # Position below the plot (-0.1 for just below, decrease further as needed)
        xanchor="center",  # Center the legend
        x=0.5              # Center it horizontally
    )
)

# Update X axis with tick values
barcharts.update_xaxes(tickvals=graph_df_pivot.index, ticktext=[str(Year) for Year in graph_df_pivot.index])

# Show the final plot
barcharts.show()
