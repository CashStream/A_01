# A_01
#t01
def clean_list(values):
    """
    -------------------------------------------------------
    Removes all duplicate values from a list: values contains
    only one copy of each of its integers. The order of values
    must be preserved.
    Use: clean_list(values)
    -------------------------------------------------------
    Parameters:
        values - a list of integers (list of int)
    Returns:
        None
    -------------------------------------------------------
    """
    values: []
    clean = []
    for i in values:
        if i not in clean:
            clean.append(i)
    return("Cleaned: {}".format(clean))
    
    
    #t02
def dsmvwl(s):
    """
    -------------------------------------------------------
    Disemvowels a string. out contains all the characters in s
    that are not vowels. ('y' is not considered a vowel.) Case is preserved.
    Use: out = dsmvl(s)
    -------------------------------------------------------
    Parameters:
       s - a string (str)
    Returns:
       out - s with the vowels removed (str)
    -------------------------------------------------------
    """
    string =""
    rem_vowel(string)
    string = ""
    rem_vowel(string)
    vowels = ['a','e','i','o','u']
    result = []
    result = ''.join(result)
    print(result)

#t03
def file_analyze(fv):
    """
    -------------------------------------------------------
    Analyzes the characters in a file.
    The contents of the file must be unchanged.
    Use: u, l, d, w, r = file_analyze(fv)
    -------------------------------------------------------
    Parameters:
        fv - an already open file reference (file variable)
    Returns:
        u - the number of uppercase letters in the file (int)
        l - the number of lowercase letters in the file (int)
        d - the number of digits in the file (int)
        w - the number of whitespace characters in the file (int)
        r - the number of remaining characters in the file (int)
    -------------------------------------------------------
    """
    u, l, d, w, r = 0, 0, 0, 0, 0
    for i in fv.read():
        if i.isupper():
            u += 1
        elif i.islower():
            l += 1
        elif i.isdigit():
            d += 1
        elif i == " ":
            w += 1
        else:
            r += 1
    return u, l, d, w, r
    
    
    
def is_leap_year(year):
    """
    -------------------------------------------------------
    Leap year determination.
    Use: leap_year = is_leap_year(year)
    -------------------------------------------------------
    Parameters:
        year - year to determine if it is a leap year (int > 0)
    Returns:
        leap_year - True if year is a leap year, False otherwise (boolean)
    -------------------------------------------------------
    """
    if n % 400 == 0:
        return True
    if n % 100 == 0:
        return False
    if n % 4 == 0:
        return True
    else:
        return False
        
        
        
        
        
        
#t05
def is_palindrome(s):
    """
    -------------------------------------------------------
    Determines if s is a palindrome. Ignores case, spaces, and
    punctuation in s.
    Use: palindrome = is_palindrome(s)
    -------------------------------------------------------
    Parameters:
        s - a string (str)
    Returns:
        palindrome - True if s is a palindrome, False otherwise (boolean)
    -------------------------------------------------------
    """    l, h = 0, len(s) - 1
  
    # Lowercase string
    s = s.lower()
  
    # Compares character until they are equal
    while (l <= h):
  
        # If there is another symbol in left
        # of sentence
        if (not(s[l] >= 'a' and s[l] <= 'z')):
            l += 1
  
        # If there is another symbol in right 
        # of sentence
        elif (not(s[h] >= 'a' and s[h] <= 'z')):
            h -= 1
  
        # If characters are equal
        elif (s[l] == s[h]):
            l += 1
            h -= 1
        
        # If characters are not equal then
        # sentence is not palindrome
        else:
            return False
