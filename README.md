# C_Compiler_Simulator
Lexical, syntactic and semantic analysis of C program


README_LEXER:
The python program Lexer.py removes valid comments conforming to C Language specification.On the other hand,it also reports the incorrect or erroneous comments found in the input file provided by user.

*The program removes all valid comments and writes the new content to a file called "withoutcomments.txt'
*Errors are also detected to a good extent and reported on console discriminating if its an improperly terminated /* comment or invalid// comment
*Regular Expressions and Text processing are exclusively used to perform these tasks

REGEX FUNCTIONS USED:

compile()- Pattern Matching for future use
sub()- Substitue a pattern with replacement pattern on a string
findall()- Finds all the occurences of a given pattern
search()- Finds the first occurence of a pattern in a given string

STRING FUNCTIONS USED:

replace() - exchange a old substring with a new substring on a string
strip()- Remove whitespaces from a string
startswith()- Check if a string starts with a particular substring
endswith()- Check if a string ends with a particular substring

README_PARSER:
The program parser.c traverses through each token produced by the program scanner.c one by one and compares to find out if it is the expected token at that time in that particular statement. 
A flag variable called error_found is set to 0 indicating no errors initially. When, the program encounters any syntax error the flag is set to 1. After the entire input program is parsed, if there is no syntax error, the program prints “Correct Syntax” . Otherwise, prints the error encountered.
The functions stmt(),expr() and factor() achieves the aforementioned purpose.If syntax error is encountered, the specific message is printed. Currently, the program is capable of printing specific errors along with line numbers like:
1.	Missing parenthesis
2.	Invalid declarations
3.	Syntax error due to unexpected token 
If there are no syntax errors, the program traverses using DFS/pre-order traversal through each non-terminals/productions that lead to the variables/terminals ultimately and prints them.
To compile and run the program, execute the commands as below:
oscreader@OSC:~/Downloads$ gcc scanner.c parser.c -o parser
oscreader@OSC:~/Downloads$ ./parser < ip > op    
NOTE: 
1.	Kindly save the input program in a file(like ip) as seen above and execute the program
2.	The pre-order traversal is implemented in such a way that it prints upto the last non-terminal.
For.eg., let the statement be read a, output is
“Program stmt_list stmt read id “ 
3.	Sample outputs for three samples are attached in the zip file

                                                                                                                      JANANI JANARDHANAN




