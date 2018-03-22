# Sample Dataset:

CategoryId | ParentCategoryId | Name | Keywords |
-----------|------------------|------|----------|
100 | -1 | Business | Money |
200 | -1 | Tutoring | Teaching |
101 | 100 | Accounting | Taxes |
102 | 100 | Taxation | |
201 | 200 | Computer | |
103 | 101 | Corporate | Tax |
202 | 201 | Operating | System |
109 | 101 | Small business | Tax |

Write a working program which should do the following:
* Given a category id return category name, parentCategoryId and key-word. Ensure that if
key-word is not present for the category, then the data from its parent should be
returned.

	* <u><b>Input:</b></u> 201
	* <u><b>Output:</b></u> ParentCategoryID=200, Name=Computer, Keywords=Teaching
	* <u><b>Input:</b></u> 202
	* <u><b>Output:</b></u> ParentCategoryID=201, Name=Operating System,
Keywords=Teaching

* Given category level as parameter (say N) return the names of the categories which are
of N’th level in the hierarchy (categories with parentId -1 are at 1st level).
	* <u><b>Input:</b></u> 2
	* <u><b>Output:</b></u> 101, 102, 201
	* <u><b>Input:</b></u> 3
	* <u><b>Output:</b></u> 103, 109, 202