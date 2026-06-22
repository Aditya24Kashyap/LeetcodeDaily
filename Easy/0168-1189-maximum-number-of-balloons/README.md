# 🟢 #168 - 1189. Maximum Number of Balloons

## Problem Info
| Field | Value |
|-------|-------|
| **Difficulty** | Easy |
| **Topics** | Hash Table, String, Counting |
| **Language** | Unknown |
| **Runtime** | N/A |
| **Memory** | N/A |
| **Solved** | 6/22/2026 |

## Solution
```txt
// Frequency Array / Hash Map + Limiting Resource (minimum ratio)
class Solution {
public:
    int maxNumberOfBalloons(string text) {
        vector<int> freq(26, 0);
        for(char t : text){
            freq[t - 'a']++;
        }
        return min({
            freq['b' - 'a'],
            freq['a' - 'a'],
            freq['l' - 'a'] / 2,
            freq['o' - 'a'] / 2,
            freq['n' - 'a']
        });
    }
};

```



---
*Auto-synced by [LeetPush](https://github.com/yourusername/leetpush) 🚀*
