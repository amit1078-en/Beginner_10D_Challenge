Day 6 - Question 2 : 
	You are given two strings a and b. You are going to print the string a character by character, from the first character to the last one.

	When printing a character, instead of pressing the button corresponding to it, you can press the "Backspace" button. It deletes the last character you have printed among those that aren't deleted yet (or does nothing if there are no characters in the current string). For example, if string a is "abcbd" and you press Backspace instead of typing the first and the fourth characters, you will get the string "bd" (the first press of Backspace deletes no character, and the second press deletes the character 'c'). Another example, if string a is "abcaa" and you press Backspace instead of the last two letters, then the resulting text is "a".

	Your task is to determine whether you can obtain the string b, if you print the string a and press "Backspace" instead of printing several (maybe zero) characters of a.
	
	
Example

Input:
	4
	ababa
	ba
	ababa
	bb
	aaa
	aaaa
	aababa
	ababa

Output:
	YES
	NO
	NO
	YES

