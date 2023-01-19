
PROJECT DESCRIPTION AND GUIDELINES PROVIDED ON ASSIGNMENT INSTRUCTIONS

Recursion is a very useful programming skill. For each of the following functions, you should fill in the body, with semantics as indicated by the comment. You do not have to validate the inputs. If it says the input is a string or integer, your function doesn't have to check that it is or work if it's not.

Many of these can be solved easily using functions and class methods you've learned already this semester. But that would defeat the purpose of this homework. Your solutions must be recursive. That is, it must call itself, except for the final problem where the helper function is the recursive function. I've done the first couple for you. All of these functions return their answer; none print it.

def sumItemsInList( L ):
    """ Given a list of numbers, return the sum. """
    if L == []:
        return 0
    else:
        return L[0] + sumItemsInList( L[1:] )

def countOccurrencesInList( key, L ):
    """ Return the number of times key occurs in 
    list L. """
    if L == []:
        return 0
    elif key == L[0]:
        return 1 + countOccurrencesInList( key, L[1:] )
    else:
        return countOccurrencesInList( key, L[1:] )

def addToN ( n ):
   """ Return the sum of the non-negative integers to n.
    E.g., addToN( 5 ) = 0 + 1 + 2 + 3 + 4 + 5. """

def findSumOfDigits( n ):
   """ Return the sum of the digits in a non-negative integer. """

def integerToBinary( n ):
   """ Given a nonnegative decimal integer n, return the 
   binary representation as a string. """

def integerToList( n ):
   """ Given a nonnegative decimal integer, return a list of the 
   digits (as strings). """

def isPalindrome( s ):
   """ Return True if string s is a palindrome and False
   otherwise. Count the empty string as a palindrome. """

def findFirstUppercase( s ):
   """ Return the first uppercase letter in 
   string s, if any. Return None if there
   is none. """

def findFirstUppercaseIndexHelper( s, index ):
   """ Helper function for findFirstUppercaseIndex.
   Return the index of the first uppercase letter, 
   beginning at index. Return -1 if there is none."""

# The following function is already completed for you. But 
# make sure you understand what it's doing. 

def findFirstUppercaseIndex( s ):
   """ Return the index of the first uppercase letter in 
   string s, if any. Return -1 if there is none. This one 
   requires a helper function, which is the recursive 
   function. """
   return findFirstUppercaseIndexHelper( s, 0 )

Expected output

Below is the output from the functions I wrote for this assignment:

>>> from RecursiveFunctions import *
>>> addToN( 10 )
55
>>> addToN( 100 )
5050
>>> addToN( 0 )
0
>>> findSumOfDigits( 0 )
0
>>> findSumOfDigits( 12345 )
15
>>> integerToBinary( 25 )
'11001'
>>> integerToBinary( 100 )
'1100100'
>>> integerToBinary( 0 )
'0'
>>> integerToList( 123 )
['1', '2', '3']
>>> integerToList( 348914 )
['3', '4', '8', '9', '1', '4']
>>> integerToList( 0 )
['0']                        # this function is easier if you return
                             # this for 0
>>> isPalindrome( "abcDcba" )
True
>>> isPalindrome( "abcDcbaF" )
False
>>> isPalindrome( "" )
True
>>> isPalindrome( "X" )
True
>>> findFirstUppercase( "ab c  dEFg hi" )
'E'
>>> findFirstUppercase( "ab c  defg hi" )               # None doesn't print
>>> findFirstUppercaseIndex( "ab c  dEFg hi" )
7
>>> findFirstUppercaseIndex( "ab c  defg hi" )
-1
>>> findFirstUppercaseIndex( "" )
-1
