# Hypertension-and-Hypotension-Clinical-Decision-Support-NICE-NG136-
This is a Streamlit web application implementing simplified NICE-based hypertension and postural hypotension decision support for adults.
The project is built in Python using Streamlit. The system collects blood pressure readings and clinical risk information, then applies simplified NICE-based rules to classify blood pressure, suggest hypertension treatment advice, and identify possible low blood pressure on standing (postural hypotension). NICE defines severe hypertension as clinic blood pressure of 180/120 mmHg or higher requiring urgent assessment, and NICE also advises checking for postural hypotension in people with symptoms such as falls or postural dizziness by comparing lying and standing blood pressure.

1.Target users:Secondary care: Hospitals (nurses, doctors, pharmacists )

2. Required Libraries
python
streamlit

Installation command:
python -m pip install streamlit
python -m streamlit run hypertension_hypotension_app.py

3. How to Run the System

Requirements:

 Python 3.8+ installed
 VS Code (recommended) or any code editor. I have used VS Code


Step-by-Step Instructions

1. Save the Python app file as:  hypertension_hypotension_app.py

2. Open a terminal in the folder where the file is saved.

3. Install Streamlit if needed usinng:  python -m pip install streamlit

4. Run the app using:  python -m streamlit run hypertension_hypotension_app.py

5. Streamlit will open the application in your browser so you can enter values and test the logic. 



Expected Output:

Interactive web interface with:

- Patient input fields (age, clinic BP, ABPM/HBPM, ethnicity, comorbidities)

- Postural hypotension input fields (lying SBP and standing SBP when symptoms are selected)

- "Get recommendation" button

- NICE-aligned hypertension results (classification, treatment decision, drug steps)

- Low BP / postural hypotension result when symptoms are selected

- Direct NICE links for hypertension and low BP / postural hypotension





4. Sample Data File

No external data file is required.
All inputs are entered directly in the web interface.



5. Low BP / Postural Hypotension Function - Later addition

The app includes a simple low blood pressure section based on suspected postural hypotension. If symptoms such as dizziness on standing, postural dizziness, or falls are selected, the user can enter lying systolic blood pressure and standing systolic blood pressure. The app then calculates the drop in systolic BP and gives a simple interpretation. NICE discusses postural hypotension under standing blood pressure assessment rather than as a separate general “low BP” adult algorithm. 



Current simplified rule used in the app:
- If systolic BP drops by 20 mmHg or more on standing, the app flags possible postural hypotension. 
- If symptoms are selected, the app shows only the low BP / postural hypotension result.
- If symptoms are not selected, the app shows the hypertension pathway results.



This is simplified educational logic and should not be used alone for real clinical decisions. 



6. Limitations & Clinical Use

✅ Decision support only — not a substitute for clinical judgement.
✅ NICE adult hypertension thresholds implemented. 
✅ Includes ethnicity and diuretic status.
✅ Includes simple postural hypotension / low BP standing check. 
❌ Not for pregnancy, children, or emergencies outside scope.
❌ No dose checks or contraindication screening.
❌ No full hypotension management algorithm.
❌ Prototype only — not for real clinical use without validation.



7. Validation / Performance

✅ Tested with NICE-based hypertension scenarios.
✅ Tested with low BP / postural hypotension example scenarios.
✅ Correct outputs for Normal, Stage 1, Stage 2, urgent hypertension, and possible postural hypotension.
✅ Fast output after user input.
❌ No external clinical validation yet.



8. Future Improvements

✅ Add more clinical variables.
✅ Improve treatment logic and follow-up support.
✅ Add diastolic standing BP logic for postural hypotension.
✅ Add EHR integration and better validation.
✅ Test with clinicians in real workflows.
✅ Including statistics on hypertension and hypotension.
✅ Include a link or feature for personalised recommendations. 
✅ Incorporating visual aids.



9. NICE Links Used in the App

Hypertension in adults:https://www.nice.org.uk/guidance/ng136 
Postural hypotension in adults:https://www.nice.org.uk/advice/esuom20 


10. Notes

This system is a simplified educational prototype for assignment purposes and should not be used for real clinical decision-making. NICE guidance contains fuller recommendations on diagnosis confirmation, investigations, treatment choice, monitoring, and follow-up for hypertension, and NICE material on postural hypotension should be reviewed directly for low BP on standing. 
