1)	Assigned Play: Number 5 – Tragedy: King Lear
2)	Speaker 1: KENT
3)	Speaker 2: ALBANY
4)	
5)	Script of the entire play:
On Powershell: curl "http://shakespeare.mit.edu/lear/full.html" -O "input.txt"

On Bash: Using regular expression to remove the angular brackets and to make to look more presentable,

curl "http://shakespeare.mit.edu/lear/full.html" | sed 's/<\/*[^>]*>//g' > data.txt

Count of occurrences of KENT from data.txt file:
	grep 'KENT' data.txt -c >> Output_CountOf_KENT.txt

Count of occurrences of ALBANY from data.txt file:
	grep 'ALBANY' data.txt -c >> Output_CountOf_ALBANY.txt

Sum of occurrences of ALBANY and KENT from data.txt file:
grep -oiE 'ALBANY|KENT' data.txt -c >>Output_TotalCount_ALBANY&KENT.txt

grep -oE 'ALBANY|KENT' data.txt -c >>Output_TotalCount.txt
