Important Regular Expressions to know:

1. To match duplicates in a string: /(\b\w+\b)(?=.*\b\1\b)/

2. To match a Username:    /^[a-z0-9_-]{3,16}$/

3. To match a Password:    /^[a-z0-9_-]{6,18}$/

    Password Strength, For Complex: (Should have 1 lowercase letter, 1 uppercase letter, 1 number, 1 special character and be at least 8 characters)
    
/(?=(.*[0-9]))(?=.*[\!@#$%^&*()\\[\]{}\-_+=~`|:;"'<>,./?])(?=.*[a-z])(?=(.*[A-Z]))(?=(.*)).{8,}/ 

    For Moderate: (Should have 1 lowercase letter, 1 uppercase letter, 1 number, and be at least 8   characters)
    
       /(?=(.*[0-9]))((?=.*[A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z]))^.{8,}$/

4. To match an Email:      /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

5. To match a Hex Value:   /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

6. To match a Slug:        /^[a-z0-9-]+$/

7. To match a URL, http(s) Protocol: /https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#()?&//=]*)/ 

                   Optional Protocol:  /(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/ 

8. To match an IP Address: /^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/

9. To match an HTML Tag:   /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

10.To match a whole text or line that does not contain a word hello:   /^(?!.*?hello).*$/  

11.To match a line, other than those end with hello: .*(?<!\.hello)$ 

12.To match multiple words: ^(?!.*(hello|hola|Salve|Bonjour|Shalom))

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


