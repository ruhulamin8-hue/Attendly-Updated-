# Attendly

A simple attendance app with five windows:

1. **Attendance**: pick a date and subject, then mark each student present or absent.
2. **Import**: import students from an Excel or CSV file, add subjects, and choose the semester.
3. **Dashboard**: attendance percentage overall, by subject and by student.
4. **Report**: generate the attendance sheet as a PDF (college format), preview it, then download or share it.
5. **Developer**: developer details.

Data is stored on the device (localStorage inside the app).

## Before you build

Open `www/index.html` and edit the `DEV` block near the top of the script to change the developer details. Email and GitHub are optional and only shown when filled.

## Get the APK from GitHub

1. Create a new GitHub repository and push this folder to the `main` branch.
2. Open the **Actions** tab. The **Build APK** workflow runs on every push. You can also run it with **Run workflow**.
3. When it finishes, open the run and download **attendly-debug-apk** under Artifacts.
4. Unzip it and install `app-debug.apk` on your phone (allow installs from unknown sources).

## Excel format

| Roll No | Name | Category |
|---------|------|----------|
| CS301   | Aarav Sharma | GEN |
| CS302   | Diya Patel | OBC |

Category is optional. It is printed in the Report.

Choose the semester on the Import screen before selecting the file. Importing again with the same roll number updates the name.

## Change the app name or id

Edit `capacitor.config.json` (`appId`, `appName`) before the first build.


## Report window

Pick a semester and subject, set teacher, branch and session, and choose whether the date columns are filled with saved attendance (P / A) or left blank. **Preview** shows every page with zoom. **Download PDF** saves the file (on the phone it opens the share sheet so you can save or send it). More than 15 class dates, or more students than fit on a page, continue on extra pages.
