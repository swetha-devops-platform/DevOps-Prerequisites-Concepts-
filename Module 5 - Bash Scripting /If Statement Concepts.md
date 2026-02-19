What is IF Statement?
 
       An if statement is used to make decisions in a script.

       It checks a condition

       If condition is TRUE → execute code

       If FALSE → skip or execute else block

Basic Syntax 

1. If Statement : 

      if [ condition ]
      then
            commands
      fi

Important:

      There must be space after [ and before ]

      fi means end of if (reverse of if)


2. If-Else Statement: 

      if [ condition ]
      then
          commands_if_true
      else
          commands_if_false
      fi


3.If-Elif-Else (Multiple Conditions):

      if [ condition1 ]
      then
           command1
      elif [ condition2 ]
           then
           command2
      else
           command3
      fi

4. Nested IF

       if [ $num -gt 0 ]
       then
             if [ $num -lt 100 ]
             then
         echo "Between 1 and 99"
              fi
        fi


Comparison Operators (Very Important)

Numeric Comparisons

               Operator	          Meaning
               -eq	              Equal
               -ne	              Not equal
               -gt	              Greater than
               -lt	              Less than
               -ge	              Greater or equal
               -le	              Less or equal

String Comparisons

              Operator	          Meaning
               =	                Equal
              !=	                Not equal
              -z	                String is empty
              -n	                String is not empty

File Conditions (DevOps Important)

             Condition	          Meaning

               -f	               File exists
               -d	               Directory exists
               -r	               Readable
               -w	               Writable
               -x	               Executable

Logical Operators

             Operator	            Meaning
             &&	                   AND
             ||	                   OR
             !	                   NOT

Extra Tips : Using Double Brackets (Advanced & Recommended)

Better practice:

         if [[ $num -gt 10 ]]
Why?

Supports logical operators easily

Safer for strings
