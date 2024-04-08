# RGoogle Blogger Contempo template - Remastering for SEO

To remaster the Google Blogger Contempo template to address the SEO issues you've identified, follow these steps:

1. **Remove Duplicate `<h1>` Heading:**
   - Locate the section of the template code that generates the `<h1>` heading containing the name of the blog.
   - Surround this code with conditional statements to ensure it only appears on the index page.
   - Here's an example of how to do this:

    ```html
    <b:if cond='data:blog.url == data:blog.homepageUrl'>
      <h1><a expr:href='data:blog.homepageUrl'><data:blog.title/></a></h1>
    </b:if>
    ```

2. **Mark Archive Pages and Search Labels as Noindex:**
   - Find the sections of the template code that generate archive pages and search label pages.
   - Insert the `<meta name="robots" content="noindex">` tag within these sections.
   - Here's where you can place it:

    ```html
    <b:if cond='data:blog.pageType != &quot;item&quot;'>
       <meta expr:content='&quot;noindex&quot;' name='robots'/>
    </b:if>
    ```

3. **Add Meta Tags for Twitter and Facebook Sharing:**
   - Locate the `<head>` section of the template code.
   - Insert the necessary meta tags for Twitter and Facebook sharing within this section.
   - Here's an example:

    ```html
    <b:if cond='data:blog.pageType == &quot;item&quot;'>
       <meta expr:content='data:blog.pageTitle' property='og:title'/>
       <meta expr:content='data:blog.pageName' property='og:url'/>
       <meta content='Your Image URL' property='og:image'/>
       <meta expr:content='data:blog.metaDescription' property='og:description'/>
    </b:if>
    ```

4. **Specify the Language of the Blog:**
   - Within the `<html>` tag of the template code, add the `lang` attribute to specify the language of the blog.
   - Here's how you can do it:

    ```html
    <html lang="en">
    ```

5. **Installation Instructions:**
   - Provide clear instructions for users to download the remastered template.
   - Include step-by-step guidance on how to upload the template to their Blogger account and apply it to their blog.

6. **AdSense Support:**
   - Ensure that any AdSense widgets included in the template are properly configured to avoid errors.
   - Test the template to verify that AdSense functionality is working as expected.

Once you've made these changes, test the remastered Contempo template to ensure that all SEO issues have been effectively addressed. Provide clear documentation and instructions for users to install and use the updated template on their Blogger blogs.
