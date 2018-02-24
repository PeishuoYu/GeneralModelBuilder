Introduction:
	This is a machine learning program that is easy to use. A lot of this program's
	code is borrowed from my number recognision project, but I have made several
	important improvements:
		This program is able to read CSV file, which is used very commonly.
		The target attribute does not have to be the last element of a
			piece of data, now it can be put anywhere.
		Now the program can deal with NUMERICAL attributes, which I think
			is the biggest improvement in this program.
		Now useless attributes can be included in the data set. (Sounds kind of
			weird :-)

Instruction:
	training('bank-data', 'pep', numericAttributes=['income', 'age', 'children'], 
	useless=['id'], maxdepth=5, minnum=20, model_name='wow')
	
	This means:

		the training set is bank-data.csv

		pep is the target attribute(the predicted attribute)

		numericAttributes is a list of numeric attributes,
			in the example it is income, age, and number of children
		useless is a list of attributes, which you do not want to include 
			in the learning process
		maxdepth is the maximum depth of the tree, in this case is 5
	
		minnum is the minimum size of sorted dataSet in this case is 20

	        model_name is the name of model that will be established 
	
	makePrediction('test', ['modelName0', modelName1'])
		This function will read the data in test.csv and make prediction based 
		on the models saved in the root folder.


This folder includes a sample, after I trained the model with training set and made
prediction using the data in test.csv, I found the model had an accuracy of 77%