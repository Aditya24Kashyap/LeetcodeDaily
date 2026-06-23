# 🔴 #3699 - 3699. Number of ZigZag Arrays I

## Problem Info
| Field | Value |
|-------|-------|
| **Difficulty** | Hard |
| **Topics** | Dynamic Programming, Prefix Sum |
| **Language** | Unknown |
| **Runtime** | N/A |
| **Memory** | N/A |
| **Solved** | 6/23/2026 |

## Solution
```txt
            ans++;
            return;
        }

        for (int x = l; x <= r; x++) {
            int sz = cur.size();

            if (sz >= 1 && cur.back() == x)
                continue;

            if (sz >= 2) {
                int a = cur[sz - 2];
                int b = cur[sz - 1];

                if ((a < b && b < x) || (a > b && b > x))
                    continue;
            }

            cur.push_back(x);
            dfs(cur, n, l, r);
            cur.pop_back();
        }
    }

    int zigZagArrays(int n, int l, int r) {
        vector<int> cur;
        dfs(cur, n, l, r);
        return ans % MOD;
    }
};

```



---
*Auto-synced by [LeetPush](https://github.com/yourusername/leetpush) 🚀*
