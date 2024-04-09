# Google Blogger Awesome Inc template - Remastering for SEO

## Introduction

To remaster the Google Blogger Awesome Inc template and address SEO issues, follow these steps:

1. **Optimize Heading Structure:**
   - Use proper heading hierarchy (e.g., `<h2>`, `<h3>`) for subheadings within the content to improve readability and SEO.
   - Ensure proper use of heading tags (`<h1>`, `<h2>`, etc.) throughout the template and blog posts. Use them hierarchically to structure your content logically.

2. **Remove Duplicate `<h1>` Heading:**
   - Ensure that each page has only one `<h1>` heading, which should ideally be the title of the blog post or page.
   - Find the section in the template code that generates the `<h1>` heading containing the blog name.
   - Surround this section with a conditional statement to ensure it only appears on the homepage:

   ```xml
   <b:if cond='data:blog.url == data:blog.homepageUrl'>
       <!-- Your <h1> heading code here -->
   </b:if>
   ```

3. **Mark Archive Pages and Search Labels as Noindex:**
   - Locate the sections in the template code that generate archive pages and search label pages.
   - Insert the `noindex` meta tag within these sections:

   ```xml
   <b:if cond='data:blog.pageType == "archive"'>
       <meta name="robots" content="noindex"/>
   </b:if>
   <b:if cond='data:blog.pageType == "search"'>
       <meta name="robots" content="noindex"/>
   </b:if>
   ```

4. **Add Meta Tags for Twitter and Facebook Sharing:**
   - Within the `<head>` section of the template code, insert meta tags for Twitter and Facebook sharing:

   ```xml
   <meta
      expr:content='data:blog.isMobile ? &quot;width=device-width,initial-scale=1.0,minimum-scale=1.0,maximum-scale=1.0&quot; : &quot;width=1100&quot;'
      name='viewport' />
    <b:include data='blog' name='all-head-content' />
    <meta content='article' property='og:type' />
    <link href='REPLACE_WITH_YOUR_GOOGLE_PLUS_PROFILE_URL' rel='publisher' />
    <meta content='REPLACE_WITH_YOUR_FACEBOOK_APP_ID' property='fb:app_id' />
    <meta content='REPLACE_WITH_YOUR_NAME' name='author' />
    <b:if
      cond='data:blog.pageType == &quot;archive&quot; or data:blog.searchQuery or data:blog.searchLabel'>
      <meta content='noindex,noarchive' name='robots' />
    </b:if>
   ```

5. **Specify the Language of the Blog:**
   - Add the `lang` attribute to the `<html>` tag:

   ```xml
   <html xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' lang='en'>
   ```

After making these changes, upload the modified template to your Blogger account. This should help improve the SEO performance of your blog using the "Awesome Inc Light" template.
