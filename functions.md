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
