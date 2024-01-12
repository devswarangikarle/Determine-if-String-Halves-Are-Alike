# Determine-if-String-Halves-Are-Alike
You are given a string s of even length. Split this string into two halves of equal lengths, and let a be the first half and b be the second half.  Two strings are alike if they have the same number of vowels ('a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U'). Notice that s contains uppercase and lowercase letters.  

class Solution:
    def halvesAreAlike(self, s: str) -> bool:
        def count_vowels(string):
            return sum(1 for char in string if char.lower() in {'a', 'e', 'i', 'o', 'u'})

        
        mid = len(s) // 2
        a, b = s[:mid], s[mid:]

        
        return count_vowels(a) == count_vowels(b)


solution = Solution()
s1 = "book"
print(solution.halvesAreAlike(s1))  

s2 = "textbook"
print(solution.halvesAreAlike(s2)) 

