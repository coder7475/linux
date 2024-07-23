man grep

# Regex Operators

^ = The line begins with
ex: grep '^sam' names.txt

$ = The line ends with
ex: grep 'sam$' names.txt


. = Match any one character
ex: grep -r 'c.t' /etc/
ex: grep -wr 'c.t' /etc/

\ = Escaping for special characters
ex: grep '\.' name.txt

* = Match the previous element 0 or more times
ex: grep -r 'let*' /etc/

+ = Match the previous element 1 or more times
ex: grep -r '0+' /etc/

{} = Previous element can exist "this many" times
ex: egrep -r '0{3,}' /etc/ = at least 3 0's
ex: egrep -r '10{0,3}' /etc/ = at most 3 0's
ex: egrep -r '0{3}' /etc = exactly 3 0's
ex: egrep -r '0{3,5}' /etc = have 3 to 5 0's

? = Make the previous element optional
ex: egrep -r 'disabled?' /etc

| = Match One Thing Or The Other

ex: egrep -r 'enabled|disabled" /etc/
ex: egrep -r 'enabled?|disabled?" /etc/

[] = Ranges or Sets
ranges:
 [a-z]
 [0-9]
sets:
 [abz954]

ex: egrep -r 'c[au]t' /etc/
ex: egrep -r '/dev/[a-z]*[0-9]?' /etc/

() = Sub expression
ex: egrep -r '/dev/(([a-z][A-Z])*[0-9]?)*' /etc/

[^] = Negated Ranges or Sets
ex: egrep -r 'http[^s]' /etc




