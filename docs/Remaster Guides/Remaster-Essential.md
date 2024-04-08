# Google Blogger Essential template - Remastering for SEO

## Introduction

To remaster the Google Blogger Essential template to address SEO issues, follow these steps:

1. **Remove Duplicate `<h1>` Heading:**
   - Locate the section of the template code that generates the `<h1>` heading containing the name of the blog.
   - Modify the code to ensure that this heading is only included on the index page and not on other pages, such as archive pages and search labels.
   - Implement conditional statements to display the `<h1>` heading only on the index page.

2. **Mark Archive Pages and Search Labels as Noindex:**
   - Find the sections of the template code that generate archive pages and search label pages.
   - Insert meta tags with the `noindex` directive within these sections to instruct search engines not to index these pages.
   - Add the following meta tag within the `<head>` section:

   ```html
     <b:if cond='data:blog.pageType == &quot;index&quot;'>
       <!-- Index Page Meta Tags -->
     <b:else/>
       <!-- Archive and Search Label Pages Meta Tags -->
       <meta name="robots" content="noindex">
     </b:if>
   ```

3. **Add Meta Tags for Twitter and Facebook Sharing:**
   - Locate the `<head>` section of the template code.
   - Insert meta tags specifically for Twitter and Facebook sharing, including necessary metadata such as title, description, and image.
   - Add the following meta tags within the `<head>` section:

   ```html
     <meta property="og:title" content="<data:blog.pageTitle/>"/>
     <meta property="og:description" content="<data:blog.metaDescription/>"/>
     <meta property="og:image" content="<data:blog.postImageUrl/>"/>
     <meta property="og:url" content="<data:blog.url/>"/>
     <meta name="twitter:card" content="summary_large_image"/>
     <meta name="twitter:title" content="<data:blog.pageTitle/>"/>
     <meta name="twitter:description" content="<data:blog.metaDescription/>"/>
     <meta name="twitter:image" content="<data:blog.postImageUrl/>"/>
   ```

4. **Specify the Language of the Blog:**
   - Within the `<html>` tag of the template code, add the `lang` attribute to specify the language of the blog.
   - Example: `<html lang="en">` for English.

5. **Installation Instructions:**
   - Download the remastered version of the Essential template with SEO fixes.
   - Log in to your Blogger account and navigate to the Template section.
   - Click on "Backup/Restore" and upload the updated template file.
   - Customize the theme as needed.

6. **AdSense Support:**
   - If AdSense support is required, ensure that the AdSense widgets are properly configured to avoid errors.
   - Test the AdSense functionality after implementing the SEO fixes to ensure compatibility.

## Conclusion

By following these steps, you can enhance the SEO performance of the Google Blogger Essential template and address the specified issues effectively.