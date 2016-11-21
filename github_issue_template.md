Creating GitHub Issue Templates
-------------------------------
Sometimes it's handy to offer someone a pre-determined template to create an issue in GitHub. This way, you can ensure that all the information you need is present.

There are two ways to create issue templates: an `ISSUE_TEMPLATE.md` file that prescribes what should appear anytime someone selects "New Issue" or a customized link that can be placed in the README. Links are more flexible, allowing you to customize the title and labels. Links allow you to create multiple templates per repository and, when used, override a file-based template.

### Creating an issue-template file
Select "New File" and create a file in the repository called `ISSUE_TEMPLATE.md`. Add the markdown you'd like to appear in new issues, and commit the changes. Select the "Issues" tab then "New Issue" to test your template. This method doesn't allow you to customize the issue title or add labels.

![file](https://dl.dropboxusercontent.com/u/834147/issue_template.png)

### Creating a link
Here's how to create a customized link that routes to a new, prefilled issue, overriding `ISSUE_TEMPLATE.md`. Want to watch a video of the process? [Right click here and choose 'Save Link As' to download a walkthrough](http://simple-monosnap.s3.amazonaws.com/Github_Link_Templates.mp4).

##### Base URL
Your base url should have the organization and repo you want to be posting to. Here's what it looks like and what you'll want to start with:

`https://github.com/bvp663/Tips-Tricks/issues/new?title=insertEncodedTitle&body=insertEncodedBody`

In the above example, the link will create a new issue in the this Tips & Tricks repository. Change the organization/username and repository to whatever is appropriate for your situation. Now we have add our title and the body of the template that we want.

##### Adding a Title and Body
Make sure you have you have the Title you want and your markdown-formatted template ready to go. Once you've got those, you'll want to use a [URL Encoder](http://meyerweb.com/eric/tools/dencoder/) to translate that text into a URL. Paste your issue title into the Encoder, select **Encode**, then copy and past the text into the appropriate spot in the base url above. Then do the same with the issue body.

![templating](https://dl.dropboxusercontent.com/u/834147/urlencoder.png)

Once that's done, you'll want to paste your completed url into a browser to make sure a new issue shows up in the right repository and all the info you want pre-filled shows up as expected. If everything looks good, add the link to the README in your repository, and whenever someone clicks on it they'll have a template ready to go!

##### Adding Labels
You can automatically assign a label to your template by adding `&labels=INSERT LABEL NAME HERE` to the end of the link. Label names are case sensitive and must already be created in the repository. To add multiple labels, use `&labels[]=insertLabelName&labels[]=insertLabelName`.
