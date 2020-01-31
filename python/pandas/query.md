# Using the df.query() feature

df.query() allows you to use strings to filter a df on multiple conditions.  For example when wanting to filter for a specific set of part numbers one could do the following... 

	part_num = ['PTS6710', 'PTS6711', 'PTS6736', 'PTS1557']

	df.query('Material == @part_num', engine='python')

note the `@part_num` in the query.  This tells the query to look for the part_num variable and not just a string with value part_num. [supporting article](https://jereze.com/fr/code/pandas-query-filter-list/)

#### What is we want to filter on multiple criteria? ####

We could do the following query to search for an equipmnet type and part desctiption

	# search_text MUST be all lowercase
	equipment = "30"
	part_text = "pump"
	
	USP.query('CatItem.str.lower().str.contains(@equipment) 
		and PartDesc.str.lower().str.contains(@part_text)'
		, engine='python')

notice the `str.lower().str.contains()` this ensures that all strings are lower case and you can search for a substring of the field. 



---
[Pandas](https://ch3ck3rs.github.io/knowledge_base/python/pandas)

[Python](https://ch3ck3rs.github.io/knowledge_base/python)

[Home](https://ch3ck3rs.github.io/knowledge_base)
