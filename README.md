# Access To Insight

Access to Insight is an Internet website dedicated to providing accurate, reliable, and useful information concerning the practice and study of Theravada Buddhism, as it has been handed down to us through both the written word of the Pali canon and the living example of the Sangha.

Access to Insight is owned and managed by the [Barre Center for Buddhist Studies](https://www.bcbsdharma.org "Barre Center for Buddhist Studies").

The name "Access to Insight" refers to the particular collection of hyperlinked texts that resides at the [official Access to Insight website](https://www.accesstoinsight.org "Access to Insight").

You are invited to download the website for your own use, share it with others, or re-post it elsewhere on the web. You are encouraged to incorporate its texts into your own website (within the terms of the copyright licenses, of course),  to use its many articles and sutta translations as the seed for your own online anthology of Buddhist texts, or to develop new and improved tools for accessing, exploring, and sharing them. The possibilities are endless.

## Building derived works from Access to Insight

The relevant copyright license appears at the bottom of each rendered page on the site. The copyrighted portions are demarcated in the markup, thus:

>&lt;div id='COPYRIGHTED\_TEXT\_CHUNK'&gt;&lt;!-- BEGIN COPYRIGHTED TEXT CHUNK --&gt;
>
>.....

>&lt;/div&gt;&lt;!-- #COPYRIGHTED\_TEXT\_CHUNK (END OF COPYRIGHTED TEXT CHUNK) --&gt;

It is this chunk of text that is governed by the license that appears at the bottom of the page. You are free to strip off everything from that file that lies outside of this "protected text chunk" and replace it with your own formatting, packaging, etc., provided that you also abide by the terms of the copyright license. In general, this means that you must also include these three elements:

1. The copyright notice. For example: _"Copyright 1997 Thanissaro Bhikkhu"_
2. The license restatement. For example: _"The text of this page is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License. To view a copy of the license, visit [https://creativecommons.org/licenses/by-nc/4.0](https://creativecommons.org/licenses/by-nc/4.0)"_. Please include a link back to the "official" Creative Commons license page, so that your readers can read the fine print of the official license.
3. The attribution. For example: _"From [Access to Insight](https://www.accesstoinsight.org) (Offline Edition 2013.12.01.01)"_ Please include a link back to the "official" Access to Insight website, so that your readers can easily track down the original source.

The particular order or placement on the page of these three elements is not important, as long as you make it easy for your readers to find them.

In general, the HTML markup within the protected text chunk is __not__ subject to copyright. You are free to modify the HTML or strip it off entirely, as you please &mdash; unless the license explicity forbids re-formatting.

[Here is an example](https://www.accesstoinsight.org/repackaged-example-01.html) of one particular page from Access to Insight as it might appear in a repackaged form on someone else's website.

These guidelines also apply when converting the files into entirely different formats. For example, if you convert a file to Microsoft Word, PDF, or some other format, please include the three elements described above.

A few PDF files have been locked and password-protected by their publisher, to restrict reformatting. Please do _not_ attempt to circumvent these security measures. If you are interested in altering or converting password-protected files, please ask the author or publisher for permission.


## How to Update The Site

### Editing Pages on the Site:

1. Go to the site repo on Github → https://github.com/bcbsit/ati
2. Click on the file you need to edit → i.e. Edit `befriending.html` by clicking on the file. You will see the file menu to the left, code to the right.
3. Click the pencil item → Click the pencil item which is top-right of the file view to edit
4. Make changes in the editor → Use the editor to make the changes you need
5. Commit changes → Click the green Commit Changes button and fill out the commit message. Select the “Commit directly to the main branch” option.
6. Changes are automatically deployed → Your changes are automatically deployed by Netlify.

### Understand what Netlify is doing:

1. Log in to Netlify → Navigate to https://app.netlify.com/login and log in with your GitHub account. Look at the accesstoinsight.org project box. You’ll see a notice that says your site was published recently.
2. View your deploys → Click on the Access to Insight project. You’ll see a list of your deploys with details.


## GitHub to Backblaze B2 Nightly Backup Setup

The site uses a GitHub Actions workflow that backs up the entire repo nightly to B2. Details are:

* File: actions/workflows/nightly-b2-backup.yml
* Trigger: Nightly at 2am UTC (you can adjust if you want)
* Action: Exports repo as tarball, uploads to B2
* Credentials: Stored as GitHub secrets here: https://github.com/bcbsit/ati/settings/secrets/actions
    * B2_APP_KEY_ID - Your application key ID from Backblaze
    * B2_APP_KEY - The application key secret given you when you set up the bucket
    * B2_BUCKET_NAME - The B2 bucket name

To look at the workflow runs:

* Navigate to https://github.com/bcbsit/ati/actions/workflows/nightly-b2-backup.yml
* You will see a list of runs. 

To manually run the workflow:

* Navigate to https://github.com/bcbsit/ati/actions/workflows/nightly-b2-backup.yml
* Find the “Run workflow” button. Select “Use workflow from main” (unless you have a file in a branch you wish to run instead) and click “Run workflow”



