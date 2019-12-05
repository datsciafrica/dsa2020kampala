# DSA Event Stub

The new event theme, based on [https://github.com/gdg-x/zeppelin](https://github.com/gdg-x/zeppelin).

## Usage
For each new event installment, follow the following instructions.

1. Create the new repo in github by going to [https://github.com/organizations/datsciafrica/repositories/new](https://github.com/organizations/datsciafrica/repositories/new), use the name coding `dsaYYYYcity` where `YYYY` is the year of the archived conference and city is an abbreviation for the city.

2. In the conference description field, place the dates and location of the workshop.

3. [**IMPORTANT**] Do *not* create an initial README or gitignore for the conference repo.

4. Create the Repo.

5. Go to a suitable directory on your machine and run the following:

```
# Here we're basing the new repo on dsaconfstub
git clone --bare https://github.com/datsciafrica/dsaXXXX.git
# Renane to the event
mv dsaconfstub dsaYYYYcity.git
cd dsaYYYYcity.git
git branch -m gh-pages
git push --mirror git@github.com:datsciafrica/datsciafrica/dsaYYYYcity.git
```
6. Now the repo is on line and you can clone it in the normal way to start working on it.

```
git clone https://github.com/datsciafrica/dsaYYYYcity.git
cd dsaYYYYcity
````

7. If everything is OK you can delete the bare mirror in the subdirectory ```dsaYYYYcity.git```.

8. Edit the `_config.yml` file in the new repo to set `baseurl` to `dsaYYYYcity`.

9. Commit the changes and push the repo (the `gh-pages` branch).

10. Check that the archived page appears online at http://datascienceafrica.org/dsaYYYYcity.git

11. Now go ahead and put event relevant updates. Editting only the files in `_data/` folder should be enough to update speakers, schedule, sponsors and other event items. For the schedule, remember to first put speakers and sessions data, then the schedule just combines these two.
