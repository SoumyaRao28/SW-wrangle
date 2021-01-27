1)	Assigned Play: Number 5 – Tragedy: King Lear
2)	Speaker 1: KENT
3)	Speaker 2: ALBANY
4)	To find the count of characters of actors in the play and find the number of occurences of actors( I have selected ALBANY and KENT). Also,find the sum of count of   	         number of occurrences of Albany+Number of occurrences of Kent and store it in the file - Output_TotalCount.
5)	Script of the entire play:
	On Powershell: 
	
		curl "http://shakespeare.mit.edu/lear/full.html" -O "input.txt"

	On Bash: Using regular expression to remove the angular brackets and to make to look more presentable,

		curl "http://shakespeare.mit.edu/lear/full.html" | sed 's/<\/*[^>]*>//g' > data.txt

	Count of occurrences of KENT from data.txt file:
		
		grep 'KENT' data.txt -c >> Output_CountOf_KENT.txt

	Count of occurrences of ALBANY from data.txt file:
		
		grep 'ALBANY' data.txt -c >> Output_CountOf_ALBANY.txt

	Sum of occurrences of ALBANY and KENT from data.txt file:
		
		grep -oE 'ALBANY|KENT' data.txt -c >>Output_TotalCount.txt
