# Personal website with jekyll themes and github

Personal website creation is a fantastic way to showcase your portfolio, blog, or professional information. GitHub Pages offers a free and straightforward way to host your website easily integrated with a custom domain. In this post, we’ll walk through the steps of setting up a personal website on GitHub Pages and linking it with a custom domain like vjcnp.co.in

### Why Use GitHub Pages?
GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files directly from a repository on GitHub and publishes them as a website. It’s an excellent option for developers and non-developers alike because:

*Free Hosting*: GitHub Pages is completely free to use.
*Easy to Set Up*: No need for complex server configurations.
*Integration with GitHub*: Automatically updates your website with each new commit to the repository.

**Step 1**: Create Your Website with Jekyll
Jekyll is a static site generator that takes plain text files (like Markdown) and templates (HTML/Liquid) and outputs a complete, ready-to-serve static website. It is particularly popular for blogs and personal sites, and is the engine behind GitHub Pages.Jekyll handles two main types of content: Pages and Posts.
Once you are happy with your site created using jekyll, you need to perform a final build and deploy the output.
This generates the complete, static HTML, CSS, and other assets into a directory named _site. This directory contains all the files you need to upload to any web host (e.g., Netlify, Vercel, or a traditional server).

If you are using *GitHub Pages*, simply pushing your source code (the entire Jekyll project folder) to the designated branch (usually main or gh-pages) of your repository will automatically trigger a build and deployment.

**Step 2**: Set Up GitHub Pages
2.1. Create a GitHub Repository
Create a new GitHub repository with the name yourusername.github.io.
Clone the repository locally and move your website files into this repository.
2.2. Push Your Website to GitHub
Add, commit, and push your files to the GitHub repository:

git add .
git commit -m "Initial commit of my website"
git push origin main
2.3. Enable GitHub Pages
Go to your repository on GitHub.
Navigate to the “Settings” tab.
Scroll down to the “Pages” section.
Under “Source,” select the main branch and set the root directory as /.
Save the settings.
GitHub will now build and deploy your site. It may take a few minutes for the changes to reflect. Once done, your site will be available at https://yourusername.github.io.

**Step 3**: Configure a Custom Domain
To make your website accessible via a custom domain like example.dev, you’ll need to configure your DNS settings:

3.1. Purchase and Set Up Your Domain
If you haven’t already, purchase a domain through a registrar (like Google Domains, GoDaddy, or Namecheap). Here, we assume you’ve already purchased youexample.dev.

3.2. Configure DNS Settings
In Your Domain Registrar’s DNS Settings:

Add an A Record:
Name: @ (or leave it blank depending on the registrar)
Type: A
Value: 185.199.108.153 (You can add multiple A records pointing to different GitHub IPs for redundancy)
TTL: Default or set as per your preference
The GitHub Pages IPs you can use:

185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
2. Add a CNAME Record (for www subdomain):

Name: www
Type: CNAME
Value: yourusername.github.io
3.3. Add a CNAME File in Your GitHub Repository
In the root of your repository, create a CNAME file containing your custom domain name:

yourdomainname
Commit and push this file to your repository. This file tells GitHub Pages to use your custom domain.

3.4. Enforce HTTPS
After the DNS changes have propagated, go back to the GitHub Pages settings in your repository. Check the box to enforce HTTPS so that your website is served securely.

**Step 4**: Update Your Favicon and Title
To customize the tab bar icon and title that appears in the web browser:

Favicon: Place your favicon (favicon.ico or favicon.png) in the root directory. Update the <link> tag in your index.html file:
<link rel="icon" href="favicon.png" type="image/png">
2. Title: Change the content of the <title> tag in your index.html file:

<title>My Portfolio</title>


### Conclusion
With these steps, you’ve successfully set up a personal website using GitHub Pages and a custom domain. Whether you’re showcasing your portfolio, writing a blog, or simply creating a personal landing page, GitHub Pages offers an excellent, cost-effective solution. Customizing your website with a personal domain like vjcnp.co.in adds a professional touch, making your online presence stand out.