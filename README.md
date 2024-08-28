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


















Here’s a condensed version of the PowerPoint presentation, limited to 3-4 slides, that packs in as much information as possible:

---

### **Slide 1: Introduction & Problem Statement**
- **Report Generation Challenges**:
  - **Manual Process**: Time-consuming and repetitive.
  - **Inconsistent Formats**: Lack of standardization across reports.
  - **Limited Automation**: Difficulty in incorporating dynamic data visualizations.

- **Goal**: Streamline and automate report creation to save time and ensure consistency.

---

### **Slide 2: Tools Overview: Streamlit, Datapane, ReportLab**
- **Streamlit**:
  - **Purpose**: Build interactive web applications for data exploration.
  - **Strengths**: Easy to use, real-time updates, interactive visualizations.
  - **Weaknesses**: Limited export options, not ideal for static reports.

- **Datapane**:
  - **Purpose**: Create and share data-driven reports, both interactive and static.
  - **Strengths**: Good balance between interactivity and static content, easy web sharing and PDF export.
  - **Weaknesses**: Limited deep customization, moderate learning curve.

- **ReportLab**:
  - **Purpose**: Generate print-ready PDFs with detailed customization.
  - **Strengths**: High control over layout, ideal for static, professional documents.
  - **Weaknesses**: No interactivity, steeper learning curve, focused on static output.

---

### **Slide 3: Efficiency Gains & Key Differences**
- **Efficiency Gains**:
  - **Streamlit**: Quick setup for dynamic, interactive dashboards – reduced time for exploratory analysis.
  - **Datapane**: Fast generation and sharing of reports – streamlined report distribution.
  - **ReportLab**: Automated high-quality PDF creation – cut down on manual document formatting.

- **Key Differences**:
  - **Streamlit**: Best for interactive exploration and dashboards.
  - **Datapane**: Best for report sharing with a mix of interactivity and static content.
  - **ReportLab**: Best for fully customized, static, print-ready documents.

---

### **Slide 4: Conclusion & Summary**
- **Overall Impact**:
  - Significant time reduction in report creation by leveraging the right tool for the right task.
  - **Tool Selection Based on Needs**:
    - **Streamlit**: Ideal for real-time data exploration.
    - **Datapane**: Great for sharing comprehensive reports.
    - **ReportLab**: Perfect for static, customized documents.

- **Final Thoughts**:
  - By utilizing Streamlit, Datapane, and ReportLab, we optimized the workflow and improved the consistency and quality of our reports.

---

This condensed presentation provides a clear overview of how the three tools were used to streamline report generation, highlighting their unique strengths and differences.
