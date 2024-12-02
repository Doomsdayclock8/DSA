Given two strings `s` and `t`, return `true` if `t` is an anagram of `s`, and `false` otherwise.

**Example 1:**

**Input:** s = "anagram", t = "nagaram"

**Output:** true

**Example 2:**

**Input:** s = "rat", t = "car"

**Output:** false

**Constraints:**

- `1 <= s.length, t.length <= 5 * 104`
- `s` and `t` consist of lowercase English letters.
# Solution
```
from collections import defaultdict

class Solution(object):

    def isAnagram(self, s, t):

        if len(s)!=len(t):

            return False

        else:

            dicts=defaultdict(int)

            dictt=defaultdict(int)

            for c in s:

                dicts[c]+=1

            for c in t:

                dictt[c]+=1

            return dicts==dictt
```

## Using [[Collections.Counter]]
```
from collections import Counter

class Solution(object):

    def isAnagram(self, s, t):

        if len(s)!=len(t):

            return False

        else:

            dicts=Counter(s)

            dictt=Counter(t)

            return dicts==dictt
```