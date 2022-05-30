
# Sliding Window
### The sliding window algorithm idea is like this:
 - We start with two pointers, left and right initially pointing to the first element of the string S.
 - We use the right pointer to expand the window [left, right] until we get a desirable window that contains all of the characters of T.
 - Once we have a window with all the characters, we can move the left pointer ahead one by one. If the window is still a desirable one we keep on updating the minimum window size.
 - If the window is not desirable any more, we repeat step 2 onwards.

```
while (right < s.size()) {
    window.add(s[right]);
    right++;

    while (valid) {
        window.remove(s[left]);
        left++;
    }
}
```