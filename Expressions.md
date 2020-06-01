Important Regular Expressions to know:

1. To match duplicates in a string: 

	   Regular Expression: /(\b\w+\b)(?=.*\b\1\b)/

2. To match a Username:   

	   Regular Expression: /^[a-z0-9_-]{3,16}$/

3. To match a Password: 

	   Regular Expression: /^[a-z0-9_-]{6,18}$/

Password Strength, 

For Complex: (Should have 1 lowercase letter, 1 uppercase letter, 1 number, 1 special character and be at least 8 characters)
    
	Regular Expression: /(?=(.*[0-9]))(?=.*[\!@#$%^&*()\\[\]{}\-_+=~`|:;"'<>,./?])(?=.*[a-z])(?=(.*[A-Z]))(?=(.*)).{8,}/ 

For Moderate: (Should have 1 lowercase letter, 1 uppercase letter, 1 number, and be at least 8   characters)
    
        Regular Expression: /(?=(.*[0-9]))((?=.*[A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z]))^.{8,}$/

4. To match an Email: 

	   Regular Expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

5. To match a Hex Value:

	   Regular Expression: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

6. To match a Slug:

	   Regular Expression: /^[a-z0-9-]+$/

7. To match a URL, 

http(s) Protocol: 

	   Regular Expression: /https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#()?&//=]*)/ 

Optional Protocol:

	   Regular Expression: /(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/ 

8. To match an IP Address: 

	   Regular Expression: /^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/

9. To match an HTML Tag:

	   Regular Expression: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

10.To match a whole text or line that does not contain a word hello:  

	Regular Expression: /^(?!.*?hello).*$/  

11.To match a line, other than those end with hello: 

	Regular Expression: .*(?<!\.hello)$ 

12.To match multiple words:

	Regular Expression: ^(?!.*(hello|hola|Salve|Bonjour|Shalom))

13. To match Time: Time Format HH:MM 12-hour, optional leading 0

                /^(0?[1-9]|1[0-2]):[0-5][0-9]$/
		
                   Time Format HH:MM 12-hour, optional leading 0, Meridiems (AM/PM)
		   
                /((1[0-2]|0?[1-9]):([0-5][0-9]) ?([AaPp][Mm]))/
		
                   Time Format HH:MM 24-hour with leading 0
		   
                /^(0[0-9]|1[0-9]|2[0-3]):[0-5][0-9]$/
		
                   Time Format HH:MM 24-hour, optional leading 0
		   
                /^([0-9]|0[0-9]|1[0-9]|2[0-3]):[0-5][0-9]$/
		
                   Time Format HH:MM:SS 24-hour
		   
                /(?:[01]\d|2[0123]):(?:[012345]\d):(?:[012345]\d)/

14.To match a City, example, Hyderabad from an Address line out of spaces and commas:

	Regular Expression: /[^\s,][^,]*(?=,[^,]*$)/
	
	Text String: 500001 Telangana, Hyderabad, India
	
   Explanation:
     
•	To match a char except whitespace and a comma: [^\s,]

•	To match 0+ chars except a comma: [^,]*

•	To match a positive lookahead that requires a comma and then 0+ chars except comma ([^,]*) till the end of the string ($) : (?=,[^,]*$)

15.  To select a line with 3 commas out of text document, which also includes lines with 2 & 1
Commas:

    		Regular Expression:  /.*,.*,.*,/g
	
    		Text String:  lovely day, lovely day, lovely day
		      lovely day, lovely day, lovely day, lovely day
		      lovely day, lovely day

16. To match Groups which has from_ format in Text:

    	Regular Expression: /(?:^|\s)from_(.*?)(?:\s|$)/g
    
    	Text String:  Stay safe from_Covid-19  from_Corona  from_Virus

17. To match specific url regex

    	Regular Expression:  /^htt:\/\/test\.com\/#\/example\/(?:[a-z0-9]+-){3}(?:[a-z0-9]+)\/records$

    	Test String: htt://test.com/#/example/a454-rte3-445f-4543/records

18. Count Vowels in a sentence

    	Regular Expression: /[aeiouAEIOU]/g

    	Test String: Abhishek
    
19. To neglect hyphens and select everything including dot(.)from a sentence.

		Regular Expression: /(\b[A-Za-z0-9À-ÖØ-öø-ÿ.]+)/g
    
	        Test String: abh-Abhishek                
			     Abhis-abhishek                
			     Ab.-abhishek-abhishek123  
			     abhishek                     
			     regex-expre-and-expressiÖn          
			     regular-expressions   
			     
20. To select everything other than double quotes in-between

		Regular Expression: /[^"]+/		(or)
		Regular Expression: /[[{:\w\\d',\d}]+]*/
		
		Test String: [{"id":"'1002001'","number":1}{"id":"'1002002'","number":1},{"id":"'1002003'","number":1},{"id":"'1002004'","number":2}]

21. To search multiple words ignoring case

		Regular Expression: \bworld\b|\bleader\b|\bmatchwordstart|word1|matchwordend\b|\bmatchwordstart|word2|matchwordend\b|\bmatchwordstart|word3|matchwordend\b|^matchmessagestart|matchmessageend$
			     
		Test String: world leader
		
22. User to enter Alphabets with spacing between the FirstName for example Abhijith Singh in the First Name

		Regular Expression: /^[A-Z][a-z]+\s[A-Z][a-z]+$/
		
		Field Name: Insured FirstName
		
23. User to enter Alphabets and/or Special Characters along with Spacing

		Regular Expression: /^[a-zA-Z0-9 !@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?]+$/
		
		Field Name: Insured LastName
		
24. Alphanumeric/Numeric (MaxLength 12 Characters)

		Regular Expression: /^([a-zA-Z0-9_-]){1,12}$/
		
		Field Name: Passport Number
		
25. Alphanumeric with Special Characters

		Regular Expression: /^[ A-Za-z0-9_@./#&+-]*$/
		
		Field Name: Proof ID detail
		
26. User to Select the Date in the DD/MM/YYYY Format

		Regular Expression: /(^(((0[1-9]|1[0-9]|2[0-8])[\/](0[1-9]|1[012]))|((29|30|31)[\/](0[13578]|1[02]))|((29|30)[\/](0[4,6,9]|11)))[\/](19|[2-9][0-9])\d\d$)|(^29[\/]02[\/](19|[2-9][0-9])(00|04|08|12|16|20|24|28|32|36|40|44|48|52|56|60|64|68|72|76|80|84|88|92|96)$)/
		
		Field Name: Date of Birth
		
		Field Value: Date Picker
		
27. User to Select the Date in the DD/MM/YYYY or DD-MM-YYYY or DD.MM.YYYY Format

		Regular Expression: /^(?:(?:31(\/|-|\.)(?:0?[13578]|1[02]))\1|(?:(?:29|30)(\/|-|\.)(?:0?[13-9]|1[0-2])\2))(?:(?:1[6-9]|[2-9]\d)?\d{2})$|^(?:29(\/|-|\.)0?2\3(?:(?:(?:1[6-9]|[2-9]\d)?(?:0[48]|[2468][048]|[13579][26])|(?:(?:16|[2468][048]|[3579][26])00))))$|^(?:0?[1-9]|1\d|2[0-8])(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2]))\4(?:(?:1[6-9]|[2-9]\d)?\d{2})$/
		
		Field Name: Date of Birth
		
		Field Value: Date Picker
