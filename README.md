<h1>Deep Raut (21070521023)</h1>

   <h1>Symptom Parsing Project</h1>
    <p>This repository contains a multi-step project for parsing patient symptoms data from a CSV file, enhancing a symptoms dictionary, and printing matching symptoms based on various criteria.</p>

   <h2>Steps Overview</h2>
    <ol>
        <li>
            <strong>Step1.ipynb:</strong> Reads the patient symptoms dataset and creates a symptoms dictionary from it.
        </li>
        <li>
            <strong>Step2.ipynb:</strong> Enhances the dictionary with symptoms present in the dataset and prints the loss columns (i.e., columns not present in the dictionary) and the quantified loss value.
        </li>
        <li>
            <strong>Step3.ipynb:</strong> Further enhances the dictionary by adding attributes to the symptoms such as mild, low, and high severities, reducing the loss to 0. The obtained symptoms dictionary is saved into <code>symptoms_dict.json</code>.
        </li>
        <li>
            <strong>Step4.py:</strong> A SymptomParser class is created, containing the following methods:
            <ul>
                <li><code>Constructor</code>: Loads the symptoms dictionary using the <code>load_dictionary</code> method.</li>
                <li><code>read_data</code>: Reads the dataset to parse through.</li>
                <li><code>parse_xml_to_dataframe</code>: Parses an XML file to a DataFrame.</li>
                <li><code>enhance_dictionary</code>: Enhances the dictionary with missing symptoms obtained from the dataset.</li>
                <li><code>print_data_based_on_dict</code>: Prints the matching values from the dataset using the dictionary.</li>
                <li><code>dump_dictionary</code>: Saves the modified dictionary into <code>symptoms_dict.json</code>.</li>
                <li><code>load_dictionary</code>: Loads the dictionary from the specified file.</li>
                <li><code>manual_update</code>: Manually adds symptoms to the dictionary.</li>
                <li><code>process_data</code>: Executes the full process:
                    <ul>
                        <li>Reads the dataset</li>
                        <li>Prints data matching the dictionary</li>
                        <li>Enhances the dictionary</li>
                        <li>Prints data matching the enhanced dictionary</li>
                        <li>Saves the dictionary</li>
                    </ul>
                </li>
            </ul>
        </li>
    </ol>

   <h2>Files</h2>
    <ul>
        <li><code>symptoms_dict.json</code>: A JSON file that stores the symptoms dictionary with severity levels (e.g., mild, low, high).</li>
        <li><code>data.csv</code>: The dataset containing patient symptoms and other attributes such as fever, cough, cold, and additional symptoms like body ache, shivering, etc.</li>
        <li><code>Step4_Output.png</code>: Demonstrates the output of the SymptomParser class, showing filtered results before and after dictionary enhancement.</li>
    </ul>

   <h2>Output Analysis</h2>
    <p>This section describes the output shown in the file <code>Step4_Output.png</code>, which demonstrates the functionality of the <code>SymptomParser</code> class in <code>Step4.py</code>. The output is a reflection of how the dictionary evolves over time and how matching improves with enhancements.</p>

   <h3>1. Initial Dictionary Matching</h3>
    <p>In the first part of the output, the symptom dictionary is used to filter the dataset. For each patient, symptoms like <code>Fever_Mild</code>, <code>Fever_Low</code>, <code>Fever_High</code>, <code>Cough_Mild</code>, <code>Cough_Low</code>, and <code>Cold_Mild</code> are matched against the dictionary. The matching data for the first 10 patients is displayed, but due to limitations in the initial dictionary, some symptoms from the dataset may not be present in the dictionary, resulting in fewer matching records.</p>
    <p>This part of the output shows the following details for each patient:</p>
    <ul>
        <li><strong>Patient_Id:</strong> The ID of the patient.</li>
        <li><strong>Symptom Severity:</strong> Severity levels of symptoms like <code>Fever</code> (Mild, Low, High), <code>Cough</code> (Mild, Low, High), and <code>Cold</code> (Mild, Low, High).</li>
        <li><strong>Other Symptoms:</strong> A list of additional symptoms such as <code>Body Ache</code>, <code>Head Ache</code>, <code>Vertigo</code>, etc.</li>
    </ul>

   <h3>2. Enhanced Dictionary Matching</h3>
    <p>After enhancing the dictionary with additional symptoms found in the dataset, a second filtered dataset is displayed. In this part, more records are matched as the dictionary now includes a broader range of symptoms. The output now shows data for 12 patients (Patient_Id 1 to 12), indicating that the enhancement process has successfully reduced the number of missing symptoms.</p>
    <p>This stage demonstrates how improving the dictionary by adding more symptoms leads to better alignment between the dataset and the dictionary, capturing more comprehensive symptom data for each patient.</p>

   <h3>3. Manual Symptom Addition</h3>
    <p>The output also demonstrates the ability to manually update the symptoms dictionary. In this example, the symptom <code>Vision Loss</code> was manually added to the dictionary with severity levels <code>Mild</code>, <code>Low</code>, and <code>High</code>.</p>
    <p>After manually adding <code>Vision Loss</code> to the dictionary, the updated dictionary was saved into the <code>symptoms_dict.json</code> file. This feature allows the user to add custom or newly discovered symptoms that are not automatically detected in the dataset.</p>

   <h2>Conclusion</h2>
    <p>The output shown in <code>Step4_Output.png</code> demonstrates how the <code>SymptomParser</code> class progressively enhances the matching process by first filtering with the initial dictionary, then improving with automatic enhancements, and finally allowing manual additions. The process ensures that the symptoms dictionary evolves over time to include all relevant symptoms, enabling more accurate parsing of patient data.</p>

   <h2>How to View the Output</h2>
    <ol>
        <li>Open the <code>Step4_Output.png</code> file in the repository.</li>
        <li>Analyze the two sets of filtered data based on available symptoms in the dictionary before and after enhancement.</li>
        <li>Check the manual update process where <code>Vision Loss</code> was added to the dictionary and saved in <code>symptoms_dict.json</code>.</li>
    </ol>

</body>
</html>
