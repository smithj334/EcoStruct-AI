To ensure EcoStruct AI provides safe, actionable intelligence to construction firms, testing will be divided into three rigorous phases:

1. Data Pipeline & API Validation

Objective: Ensure external data is pulled correctly.

Method: Run 50 automated test queries using diverse U.S. addresses. Verify that the system retrieves the correct latitude/longitude, topological grade, and regional weather averages without timing out or crashing. Include basic error handling to output a "Data Unavailable" flag if an API drops.

2. Model Accuracy & Back-Testing

Objective: Validate the accuracy of the concrete volume and financial predictions.

Method: Utilize a holdout dataset of 20 previously completed 3D-printed homes (data the model has never seen). Input the parameters of those homes into EcoStruct AI and compare the AI's predicted concrete volume and cost against the actual historical volume and cost. The success threshold is a prediction margin of error of less than 5%.

3. RAG Hallucination Testing

Objective: Ensure the LLM does not fabricate ("hallucinate") building codes.

Method: Input deliberate edge-case queries (e.g., attempting to build a 5-story 3D printed structure in a hurricane zone). Evaluate the LLM's response to ensure it strictly cites the vector database (flagging the height as a code violation) rather than generating a compliant but legally false response.
