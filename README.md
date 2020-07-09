# Proetein-level-post-processing-program-for-pfind
This algorithm is used for quantification of proteins based on quantificantion results from pFind (pQuant). All quantification results of 
peptides with Interference Score (used for estimating the result of quantification) <0.5 were used to calculate the final ratio of protein peptides 
belong to. The median of all ratios from peptides belong to the same protein was used as the final ratio of the protein.
	pFind download after 2020.01.01 is necessory.
	System requirements: This algorithm was developed by python3 and tested on python 3.7.3. Windows® is the uniqie operating system for this 
algorithm.
	Installation guide: Python 3.7.3 or any version higher than 3.7.3 should be installed (https://www.python.org/). Please make sure that python 
has been added to the path when installed. There is no need of installation of this algorithm. You can download this algotithm (two .py programs) in a 
new folder and run them follow to instructions.
	Instructions: 
	(1) Download and install python3; 
	(2) Download the two .py oprograms in a new folder; 
	(3) Creat two new subfolders, 'data' and 'data_protein', in chich folder .py programs in;
	(4) Creat a new .txt file and nominate it 'database'; 
	(5) Open the original database file in a .fasta format with a text editor, copy and paste all the contents into the text new created file 
	‘database’. Double click the program ‘construct_library.py’ to reconstruct the database. 
	(6) Copy the file ‘pQuant.spectra.list’ from the ‘results’ folder in the folder of pfind result you have assigned and paste it into the 
	subfolder ‘data’. Rename the file as ‘IPM[C]_XXX’. (7) Copy the file ‘pFind.protein’ from the folder ‘results’ in the location setup in Step 
	75 and paste it into the subfolder ‘data_protein’. Rename the file as ‘IPM[C]_XXX_P’.
	(8) Double click the program ‘pfind_post_processing_site_level.py’ and use the following command:
		‘Please enter the calculation style (lh for light/heavy & hl for heavy/light):’ Type ‘hl’ or ‘lh’ to proceed
		‘Please enter the cut off value of interference score:’ Type ‘0.5’ to proceed.
		‘Please enter the number of modification in each spectrum (a for single modification & b for multi-modification):’. Type ‘a’ to proceed. Press ‘Enter key’ and run the    algorithm. 
	(9) Find the output file with the prefix ‘site_’ in the subfolder ‘results’ and import it into Excel.
