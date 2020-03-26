# cmsInvestigation
Just looking at a suspected problem with Forestry.io.

## Test 1

__Scenario__: Two Posts are created outside of Forestry.io using the Hugo CLI using __YAML__ Format for their Front Matter 
on a local Windows PC.
One Post is associated with the `mandatoryNumberDefaultZero` Forestry.io Front Matter Template. The 
other Post is associated with the `optionalNumberDefaultZero` Forestry.io Front Matter Template. 
In both Posts, the `a_number` Front Matter Field is set to 0 (zero). The objective of the test 
is to see what happens when the site is imported into Forestry.io and the Posts are opened in 
the Forestry.io CMS Editor.

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test1-mandatory-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test1-optional-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test1-mandatory-number.md` the Test Result observed was `a_number` had no value and the Forestry.io CMS Editor displayed an error message saying "A Number is required".

This is a Test Fail.

For `/posts/test1-optional-number.md` the Test Result observed was `a_number` had no value.

This is a Test Fail.


## Test 2

__Background__: Test 2 is essentailly a repeat of Test 1 but using TOML rather than YAML as the Test Pages Fornt Matter Format.

__Scenario__: Two Posts are created outside of Forestry.io using the Hugo CLI using __TOML__ Format for their Front Matter 
on a local Windows PC.
One Post is associated with the `mandatoryNumberDefaultZero` Forestry.io Front Matter Template. The 
other Post is associated with the `optionalNumberDefaultZero` Forestry.io Front Matter Template. 
In both Posts, the `a_number` Front Matter Field is set to 0 (zero). The objective of the test 
is to see what happens when the site is imported into Forestry.io and the Posts are opened in 
the Forestry.io CMS Editor.

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test-2-mandatory-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test-2-optional-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test-2-mandatory-number.md` the Test Result observed was `a_number` had no value and the Forestry.io CMS Editor displayed an error message saying "A Number is required".

This is a Test Fail.

For `/posts/test-2-optional-number.md` the Test Result observed was `a_number` had no value.

This is a Test Fail.

## Test 3

__Background__: Test 3 is essentailly a repeat of Test 2. I noticed that when Forestry.io creates a 
Post it uses TOML, puts the fields in a different order and leaves a blank line at the end 
of the Front Matter. So let's try that.

__Scenario__: Two Posts are created outside of Forestry.io using the Hugo CLI using __TOML__ Format for their Front Matter
leaving a blank line at the end of the TOML and replicating the field order saved by Forestry (all on a local Windows PC).
One Post is associated with the `mandatoryNumberDefaultZero` Forestry.io Front Matter Template. The 
other Post is associated with the `optionalNumberDefaultZero` Forestry.io Front Matter Template. 
In both Posts, the `a_number` Front Matter Field is set to 0 (zero). The objective of the test 
is to see what happens when the site is imported into Forestry.io and the Posts are opened in 
the Forestry.io CMS Editor.

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test-3-mandatory-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)

__Given__ the two Posts have been created using the Hugo CLI<br>
__AND__ they have been associated with their respective Front Matter Templates<br>
__AND__ the changes have been pushed to GITHUB<br>
__AND__ I log into Forestry.io in a new Browser Window<br>
__WHEN__ I open `/posts/test-3-optional-number.md` in the Forestry.io CMS Editor<br>
__THEN__ the value for `a_number` shown is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test-3-mandatory-number.md` the Test Result observed was `a_number` had no value and the Forestry.io CMS Editor displayed an error message saying "A Number is required".

This is a Test Fail.

For `/posts/test-3-optional-number.md` the Test Result observed was `a_number` had no value.

This is a Test Fail.

## Test 4

__Background__: Change of tack now. Rather than work from the CLI, do everything in Forestry.io.

__Scenario__: Two Posts are created using Forestry.io .
One Post is created using the `mandatoryNumberDefaultZero` Forestry.io Front Matter Template. The 
other Post is created with the `optionalNumberDefaultZero` Forestry.io Front Matter Template. 
In both Posts, the `a_number` Front Matter Field is set to 0 (zero). The objective of the test 
is to see what the Forestry.io CMS Editor creates in the `.md` files when viewed from GITHUB.

__Given__ the two Posts have been created using Forestry<br>
__WHEN__ I view the `test 4 .md files` GITHUB<br>
__THEN__ their values for `a_number` is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test-4-mandatory-number.md` the Test Result observed was `a_number` had the value 0 (zero).

This is a Test Pass.

For `/posts/test-4-optional-number.md` the Test Result observed was `a_number` had the value 0 (zero).

This is a Test Pass.

## Test 5


__Scenario__: Building on Test 4, in a new Window login and open the two Posts created by Test 4
reviewing their settings.

__Given__ the Test 4 has been run and passed<br>
__AND__ I have logged in to Forestry.io via a new Window
__WHEN__ I view the `test 4 .md files` GITHUB<br>
__THEN__ their values for `a_number` is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test-4-mandatory-number.md` the Test Result observed was `a_number` had the value 0 (zero).

This is a Test Pass.

For `/posts/test-4-optional-number.md` the Test Result observed was `a_number` had the value 0 (zero).

This is a Test Pass.

## Test 6


__Scenario__: Building on Test 5, cause Forestry.io to re-import the Site from GITHUB.

__Given__ the Test 5 has been run and passed<br>
__AND__ I have logged in to Forestry.io via a new Window
__AND__ I have pushed a new Commit to GITHUB by updating the Repositories README.md File with the Test Plan for Test 6.
__WHEN__ I view the `test 4 .md files` GITHUB<br>
__THEN__ their values for `a_number` is 0 (zero)


### Outcome

Test ran 26/03/2020.

For `/posts/test-4-mandatory-number.md` the Test Result observed was `a_number` had no value and the Forestry.io CMS Editor displayed an error message saying "A Number is required".

This is a Test Fail.

For `/posts/test-4-optional-number.md` the Test Result observed was `a_number` had no value.

This is a Test Fail.
