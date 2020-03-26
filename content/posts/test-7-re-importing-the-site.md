+++
a_number = 1
title = "Test 7 - Re-importing the Site"

+++
## Test Plan

Test 7 follows on from all of the tests.

Based on my guess that the issue occurs as a consequence of Forestry.io importing the site from GITHUB, but that whilst such an import is avoided then Forestry.io will be OK, then this test does the following:

1. Edit all of the Test Documents in /posts, e.g. Test 1, Test 2 etc.
2. Correct each document by setting the Front Matter Field called a_number to 0 (zero)
3. Review every document on a second pass to verify the edits
4. Start the Preview Server to verify it will start
5. Preview a Test Post, e.g. either of the Test 4 Posts
6. Stop the Preview Server
7. Tell Forestry.io to re-import the site
8. Start the Preview Server
9. Review the documents in the CMS Editor

## Test Result Prediction

Predicted outcome... all of the corrected documents will now be incorrect again.

## Actual Test Result

As predicted all of the corrected documents became problems again subsequent to the re-import from GITHUB.

See video [Test 7 Part 1](/uploads/test7-part1-20200326_123432.mp4), which covers Steps #1 through #5.

See video [Test 7 Part 2](/uploads/test7-part2-20200326_123921.mp4), which covers Steps #6 through #9.