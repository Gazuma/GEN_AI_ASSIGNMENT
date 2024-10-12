 <h1>Patient Symptoms Dictionary Assignment</h1>
    <p>This repository contains a 4-step assignment focused on processing a patient symptoms dataset, creating and enhancing a symptoms dictionary, and parsing the dataset using the dictionary. The steps are implemented in Jupyter notebooks and Python scripts.</p>

   <h2>Overview of Files and Steps</h2>

  <h3>1. <code>Step1.ipynb</code>: Creating a Symptoms Dictionary</h3>
    <p>This file reads the patient symptoms dataset and creates a dictionary containing the symptoms from the dataset.</p>
    <h4>Tasks:</h4>
    <ul>
        <li>Load the patient dataset.</li>
        <li>Extract symptoms present in the dataset.</li>
        <li>Create a dictionary that stores each symptom as a key.</li>
    </ul>

  <h3>2. <code>Step2.ipynb</code>: Enhancing the Symptoms Dictionary and Quantifying Loss</h3>
    <p>In this step, the dictionary is enhanced with the symptoms present in the dataset. Additionally, columns not present in the dictionary are printed along with a quantified loss value.</p>
    <h4>Tasks:</h4>
    <ul>
        <li>Load the symptoms dictionary.</li>
        <li>Check for symptoms in the dataset that are not present in the dictionary.</li>
        <li>Print missing symptoms (loss columns).</li>
        <li>Calculate and print the quantified loss.</li>
    </ul>

  <h3>3. <code>Step3.ipynb</code>: Attribute Enhancement and Loss Reduction</h3>
    <p>The symptoms dictionary is further enhanced by adding attributes such as <code>mild</code>, <code>low</code>, <code>high</code>, and the loss is reduced to 0. The final dictionary is saved as <code>symptoms_dict.json</code>.</p>
    <h4>Tasks:</h4>
    <ul>
        <li>Load the existing dictionary.</li>
        <li>Add severity attributes (mild, low, high) to each symptom.</li>
        <li>Enhance the dictionary to include all symptoms found in the dataset.</li>
        <li>Reduce the quantified loss to 0.</li>
        <li>Save the enhanced dictionary to <code>symptoms_dict.json</code>.</li>
    </ul>

  <h3>4. <code>Step4.py</code>: Symptom Parser Class</h3>
    <p>This Python script defines a <code>SymptomParser</code> class, which handles the processing of the dataset using the symptoms dictionary. The class includes methods for reading data, parsing XML to a DataFrame, enhancing the dictionary, printing results, and saving the dictionary.</p>
    <h4>Methods:</h4>
    <ul>
        <li><strong>Constructor:</strong> Initializes the <code>SymptomParser</code> object and loads the symptoms dictionary using <code>load_dictionary</code>.</li>
        <li><strong><code>read_data()</code>:</strong> Reads the patient dataset for parsing.</li>
        <li><strong><code>parse_xml_to_dataframe()</code>:</strong> Reads an XML file and parses it into a DataFrame.</li>
        <li><strong><code>enhance_dictionary()</code>:</strong> Enhances the symptoms dictionary with new symptoms found in the dataset that are missing in the current dictionary.</li>
        <li><strong><code>print_data_based_on_dict()</code>:</strong> Prints matching symptom values obtained by parsing through the dataset using the current dictionary.</li>
        <li><strong><code>dump_dictionary()</code>:</strong> Saves the modified symptoms dictionary to <code>symptoms_dict.json</code>.</li>
        <li><strong><code>load_dictionary()</code>:</strong> Loads the symptoms dictionary from a specified file.</li>
        <li><strong><code>manual_update()</code>:</strong> Allows manual addition of new symptoms to the dictionary.</li>
        <li><strong><code>process_data()</code>:</strong> Executes the entire processing pipeline, which includes:
            <ol>
                <li>Reading the dataset.</li>
                <li>Parsing the dataset and printing the matching data using the dictionary.</li>
                <li>Enhancing the dictionary with any missing symptoms.</li>
                <li>Printing the data after the dictionary has been enhanced.</li>
                <li>Saving the enhanced dictionary to <code>symptoms_dict.json</code>.</li>
            </ol>
        </li>
    </ul>
  <h3>5. <code>symptoms_dict.json</code>: Symptoms Dictionary</h3>
    <p>This file contains the symptoms dictionary in JSON format, with symptoms as keys and their attributes (such as severity levels) as values. It is generated and updated during the different steps of the assignment, particularly in <code>Step3.ipynb</code> and <code>Step4.py</code>.</p>

   <h3>6. <code>data.csv</code>: Patient Symptoms Dataset</h3>
    <p>This file contains the dataset of patient symptoms used in the assignment. It is loaded and processed in the notebooks and scripts to extract, enhance, and update the symptoms dictionary.</p>

  <h2>How to Use</h2>
    <ol>
        <li>Clone the repository:
            <pre><code>git clone https://github.com/Gazuma/GEN_AI_ASSIGNMENT.git
cd GEN_AI_ASSIGNMENT</code></pre>
        </li>
        
  <li>Run the steps in sequence:
            <ul>
                <li>Start with <code>Step1.ipynb</code> to create the initial symptoms dictionary.</li>
                <li>Proceed to <code>Step2.ipynb</code> and <code>Step3.ipynb</code> to enhance the dictionary and reduce the loss.</li>
                <li>Use <code>Step4.py</code> to parse the dataset using the <code>SymptomParser</code> class.</li>
            </ul>
        </li>
        <li>Modify the code as needed and save the enhanced dictionary by following the steps provided.</li>
    </ol>

