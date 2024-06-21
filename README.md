# MThesis

## Identifying Institutions and Social Behaviour: A Method for Extracting Institutional Informal Rules from Surveys

### Objective
This project aims to develop a standard method to identify social structures embedded within survey questionnaire data using data analytics and Institutional Grammar (IG). By analyzing responses from a survey on behavior, the objective is to provide a comprehensive overview of norms and shared strategies present in the data.

### Methodology
The project involves the following steps:

1. **Literature Review**: Reviewing existing literature on behavior analysis and IG concepts.
2. **Dataset Exploration**: Exploring a survey dataset.
3. **Data Analysis Strategies**: Evaluating different data analysis strategies to extract social structures.
4. **Method Development**: Developing a method that aligns IG concepts with survey questions and responses.
5. **Validation and Testing**: Applying the developed method to the survey dataset to validate its effectiveness.

### Research Questions
The main research question guiding this project is:
- What standard method can be developed to extract informal rules-in-use for institutional analysis from survey data?

Sub-questions include:
1. What challenges do institutional analysts face when identifying institutional informal rules?
2. To what extent does Institutional Grammar align with survey data to identify and organize informal rules?
3. What are the possible approaches to connect survey results to Institutional Grammar concepts?
4. What requirements should the output data fulfil to ensure that the informal rules from surveys are usable for institutional analysis, consistent, and well-communicated?

### Steps:
The SIRE method
This section describes each stage of the proposed extraction method, outlining what the researcher is expected to do and the anticipated results. The process involves multiple steps, starting from the selection of relevant survey questions to the formation of ADICO statements. The methodology is structured to facilitate the extraction of informal rules-in-use from survey data for institutional analysis.
Survey Data Access: Ensure access to the survey data that includes questions relevant to the research context. There should be two datasets for a survey: question overview and responses


Data Overview: Review the survey overview data, which should include the following columns:
Question_ID: A unique identifier for each question.
Question_Text: The text of the question.
Response_Option: The text of each response option.
Response_Value: Numerical mapping of response options.
ADICO_Category (Optional): The ADICO component (Attribute, Aim, Condition, Deontic) identified by the question.


Selecting Relevant Questions: Select questions from the survey data relevant to research, ensuring a comprehensive representation of demographics, actions, opinions, and external factors. Prioritise dichotomous and ordinal questions due to their simplicity in coding and analysis.
Demographic Questions: If you are focusing on studying a specific demographic, include the attribute-categorised questions that capture the relevant demographic information.


Categorising Questions: If the ADICO_Category values have not been assigned yet, for the selected questions assign each of them an ADICO component (Attribute, Aim, Condition, Deontic). 
Attributes: Questions that distinguish relevant demographics (e.g., age, location, gender).
Aims: Questions about actions performed or intended, opinions held, or changes made.
Conditions: Questions about external factors influencing behaviour.



Review Response data: Check the contents of the response data for the relevant questions. 
The response data should consist of rows as responses and columns as question identification. 
For most, if not all, questions the response values should be numerical, making it possible to match it to the text value in the survey overview data.
 
Data Cleaning: Prepare data for decision tree analysis.
Exclude any response options that do not contribute to meaningful outcomes. E.g. Remove any n/a values or “Don’t Know” responses.
Ensure aim and condition responses are encoded as binary or ordinal values.


Converting Questions to ADICO Components: For each question and response option, convert the text to its ADICO component equivalent. Ensure the resulting attribute, aim, and condition questions combine into coherent sentences representing informal institutions:
Attribute: People in the Netherlands
Aim: install solar panels 
Condition: if they receive a subsidy.


Analysing Data with Decision Trees: Use decision trees to connect aims and conditions, identifying significant relationships within demographic groups.
Utilise Python to implement a decision tree algorithm, connecting aims to conditions. Identifying which conditions cause aims to have more consistent outcomes (response proportions).


Select Significant Nodes: Evaluate each node on the decision trees. 
If the node has enough samples and a low enough entropy, the relationship is informative enough to form an informal rule.
Extract the data from the decision tree and gather the resultant statements in a table, including relevant ADICO components and statistical values.


Visualize and plot: Plot the statements and proportions using the data from the decision tree to communicate the significance of the informal rule.


### Conclusion
This project seeks to address the gap in standardized methodologies for extracting social structures from survey data. By leveraging IG concepts and data analytics, the aim is to provide actionable insights for policymakers and researchers. The developed method will facilitate a deeper understanding of the norms and shared strategies that underpin community responses, ultimately supporting more effective and informed policy decisions.
