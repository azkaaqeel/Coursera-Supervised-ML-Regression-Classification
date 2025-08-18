import all libraries
pandas is for reading csv files


1) One Hot Encoding: *This step is done for both Train & Test data sets.*
	1) get_dummies: n categories turn into n columns, of drop_first= true, n-1 columns
	2) Label Encoding
2) Separate Trainset into X & Y such that Y contains Target Variable column and X contains rest columns
3) Handle missing values. Avoid dropping columns. Make use of SimpleImputer, use strategy mean perhaps.
4) 