---
title: Posts concerning this investigation
a_number: 0

---
There are a sequence of Tests (Test 1 through Test 6). The Test
Plan containing the Test Cases and the Test Observations are found
in [Test Plan and Results](/posts/my-first-post).

This website is as bare as I can make it created as per the Hugo Quickstart.

The Forestry.io configuration is also kept as simple as I can devise to fit the purpose.

Having executed the Test Plan and examined the results, I am tempted to suggest that
the root cause of my issue is as a result of an import to Forestry.io from GITHUB.

To validate, this suspicion I created a further test, [Test 7](/posts/test-7-re-importing-the-site), and it would appear to show some support for my assertion. Re-importing the site causes issues with Number fields set to zero.

I also believe that this is the same vector for causing intermittent situations where by the building/starting of the Preview Server can sometime fail with a HUGO Error similar to...

> Error: Error building site: "/root/hugo/content/posts/test-7.md:3:1": unmarshal failed: Near line 2 (last key parsed 'a_number'): expected value but found "nil" instead