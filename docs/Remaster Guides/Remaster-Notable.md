# Google Blogger Notable template - Remastering for SEO

## Introduction

To remaster the Google Blogger Notable template and address SEO issues, follow these steps:

1. **Remove Duplicate `<h1>` Heading:**
   - Locate the section of the template code that generates the `<h1>` heading containing the name of the blog.
   - Modify the code to ensure that this heading is only included on the index page and not on other pages, such as archive pages and search labels.
   - Use conditional statements to include the `<h1>` heading only on the homepage.

2. **Mark Archive Pages and Search Labels as Noindex:**
   - Find the sections of the template code that generate archive pages and search label pages.
   - Insert meta tags with the `noindex` directive within these sections to instruct search engines not to index these pages.
   - Add the following meta tag within the `<head>` section of each relevant template file:

   ```html
     <meta name="robots" content="noindex">
   ```

3. **Add Meta Tags for Twitter and Facebook Sharing:**
   - Insert meta tags specifically for Twitter and Facebook sharing within the `<head>` section of the template.
   - Ensure each blog post includes meta tags for title, description, and image.
   - For Twitter:

   ```html
     <meta name="twitter:card" content="summary_large_image">
     <meta name="twitter:title" content="Your Title">
     <meta name="twitter:description" content="Your Description">
     <meta name="twitter:image" content="URL to Your Image">
   ```

   - For Facebook:

   ```html
     <meta property="og:title" content="Your Title">
     <meta property="og:description" content="Your Description">
     <meta property="og:image" content="URL to Your Image">
   ```

4. **Specify the Language of the Blog:**
   - Within the `<html>` tag of the template code, add the `lang` attribute to specify the language of the blog.
   - For example: `<html lang="en">` for English.

5. **Installation Instructions:**
   - Download the updated SEO-friendly version of the Notable template.
   - Log in to your Blogger account and navigate to the Template section.
   - Click on "Backup/Restore" and upload the updated template.xml file.
   - Customize the theme as needed and apply any additional CSS provided.

6. **AdSense Support (Optional):**
   - If AdSense support is necessary, ensure that the AdSense widgets are properly configured to avoid any errors.
   - Test the AdSense functionality after implementing the SEO fixes to ensure compatibility.

## Conclusion

By following these steps, you can remaster the Google Blogger Notable template and address the specified SEO issues effectively. These improvements will help enhance the visibility and ranking of your blog on search engines.