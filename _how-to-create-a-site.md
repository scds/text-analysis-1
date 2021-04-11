Follow these steps to create a new workshop website from this template repository: 

## 1. Create a new repository using this template
1. Navigate to the [SCDS DMDS template repository](https://github.com/scds/dmds-template)
2. Above the file list, click **Use this template**
3. Select scds as the repository owner 
4. Give the new repository a name (we try to keep it to a few words and use hyphens to delimit words--e.g. *intro-voyant*)
5. Set the repository visibility to **Public**
6. Click **Create repository from template**
- Full instructions (from GitHub) [here](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template).

## 2. Configure GitHub Pages
1. In the new repository, go to **Settings > GitHub Pages**
2. As **Source**, select **main** branch
3. Do not choose a theme (a theme has already been configured) 
4. Click save. The URL to your new website will be displayed. It will take the form ```https://scds.githib.io/<repository_name>```, where ```repository_name``` is the name you created in step 4 of the previous section. 

## 3. Set up Google Analytics
1. Go to the [admin page](https://analytics.google.com/analytics/web/#/a2574088p251711101/admin) for the SCDS workshop pages
2. Click **Add Stream > Web**
3. Enter the GitHub Pages URL created in previous section (i.e. ```https://scds.githib.io/<repository_name>```). Provide a name.

## 4. Edit the README file 
1. Enter the workshop name, workshop URL, and contributor name(s) where prompted

## 5. Add necessary documents, images, and data  
```assets/docs```
- Add any PDFs (slides, worksheets, etc.) that you will either embed or link to in the main text

```assets/img```
- Add any workshop-specific image(s), including the title image and any images to be shown in the main content
- Keep the logo files, as they may be useful.

```data/```
- Add any datasets or other files that are required for the workshop.
  
## 6. Edit the config.yml file 
1. Update lines with inline comments beginning with ```***```. These include the following variables:
  - **title** (workshop title)
  - **github_repo_url** (GitHub Pages URL from Section 2)
  - **gh_edit_repository** (GitHub repository URL from Section 1)
  - **ga_tracking** (Tracking code from Section 3)
Colour schemes are dictated by the ```colour scheme``` variable. These schemes are managed [here](https://github.com/scds/just-the-docs/tree/master/_sass/color_schemes)

## 7. Add content to workshop pages 
Content is currently block-commented out with ```<!--``` and ```-->``` at the start and end, respectively. Edit content and replace links as needed. 

```index.md```
- Edit the link to the title image 
- Edit the other content

```preparation.md```
- Edit content and URLs to content (like data)

```instructions.md```
- Add any specific instructions 
- Update URLs to embedded videos, download links, workshop slides, etc.
- If you want to have pages for multiple lessons, you can replace ```instructions.md``` with multiple pages (e.g. ```lesson-1.md``` and ```lesson-2.md```, etc.). Each new page will need a unique title and the **nav_order** variable for these pages (and ```learn-more.md```, as well).

```learn-more.md```
- Add content



