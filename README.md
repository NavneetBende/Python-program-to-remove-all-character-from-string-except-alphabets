Remove all character from a string except alphabets
In this article we will learn about how to Remove all character from a string except alphabets

We will do this by checking ASCII values of each character present in the string and remove all character that does not lie in the range of alphabetic ASCII value whether it is an uppercase letter or a lowercase letter.

Remove all character from a string except alphabets in python
Algorithm
Step 1:- Start.
Step 2:- Take user input.
Step 3:- Initialize a empty string.
Step 4:- Start iterating through string.
Step 5:- Check for the ASCII value of character and whether it lie in the range.
Step 6:- If TRUE concatenate characters to empty string.
Step 7:- Print String2.
Step 8:- End.
Python program to remove all characters from string except alphabets
Run
#take user input
String1 = "#Justice!For@Chutki123"
#initialize empty String
String2 = ''
for i in String1:
    #check for alphabets
    if (ord(i) >= 65 and ord(i) <= 90) or (ord(i) >= 97 and ord(i) <= 122):
        #concatenate to empty string
        String2+=i
print('Alphabets in string are :' + String2)
Alphabets in string are :JusticeForChutki
Mehod 2
Run
def removeSpecialCharacter(s):
    i = 0
    while i < len(s):
        # Finding the character whose ASCII value fall under this range
        if (ord(s[i]) < ord('A') or ord(s[i]) > ord('Z') and ord(s[i]) < ord('a') or ord(s[i]) > ord('z')):
            # erase function to remove the character
            del s[i]
            i -= 1
        i += 1
    print("".join(s))

# main Code
if __name__ == '__main__':
    s = "P*r;e..pi, n'st^a?"
    s = [i for i in s]
    removeSpecialCharacter(s)
Output
Prepinsta
Method 3
Here we are keeping track of two indexes.

Run
def removeSpecialCharacter(s):
t = ""
for i in s:

# Store only valid characters
if (i >= 'A' and i <= 'Z') or (i >= 'a' and i <= 'z'):
t += i
print(t)

# Driver code
s = "$Pre*p;i..ns, '^ta?"
removeSpecialCharacter(s)
Output
Prepinsta
Related Pages
Juggling algorithm for array rotation
 
Balanced Parenthesis Problem
 
Toggle each character in a string

Find the ASCII value of a character

Length of the string without using strlen() function

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime

Login/Signup to comment


Yash st=’abc4a5s4e4xs’
for i in st:
if i.isalpha():
pass
else:
print(i)
st=st.replace(i,”)
print(st)
0Log in to Reply

2KL19CS019 a = ‘23423h4b2j3h42k3n4khb2jh34kn234kn’
b = ”
for i in a:
if i <= '9':
b = b+i
else:
pass
print(b)
0Log in to Reply

PrepInsta Support Hey! Join Here for all your technical queries.
0Log in to Reply

abhay tomar x=input(“enter string :”)
y=x
for i in x:
if i.isalpha() or i==” “:
pass
else:
y=y.replace(i,”)
print(y)
0Log in to Reply

PrepInsta Support Kindly refer Discord this link.
0Log in to Reply

DuttLuri Lalithasri s = input(‘enter a value:’)
t = ”
for i in s:
if (‘A’ <= i <= 'Z') or ('a'<= i <= 'z'):
t+=i
print(t)
