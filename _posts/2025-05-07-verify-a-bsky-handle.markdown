---
layout: post
title:  "Verify your own domain-backed Bsky handle"
date:   2025-05-07 17:57:37 +0300
categories: web site
---
The initial version of the web site is now up. This started as an experiment with Bluesky handles and then I ventured into decentralised identities, and then decided to try it out myself. For now this is just a simple web page, a placeholder, if you will. 

This site is created with Jekyll and stored as Github Pages. 

# Configuring your own Bsky handle (the complicated way)

## Part 1: preparations 
1. Register a domain with your domain registrar. (GoDaddy, Namecheap, etc.) In my case it is `hamalainen.social`. Your Bluesky identity will be based on this domain. 
2. (Optional) Create a subdomain. In my case I added the host `janne`as a CNAME DNS record which results in domain `janne.hamalainen.social`. This can be done via your domain registrar's service. 
3. Create a github account at [github.com](github.com) if you don't have one already. 
4. Login to your Github account. Create Github pages by creating a new respository named `YOUR_USERNAME.github.io`. Follow the Quickstart guide here: [https://docs.github.com/en/pages/quickstart](https://docs.github.com/en/pages/quickstart)
5. Go to your profile `https://github.com/YOUR_USERNAME`
6. Click your avatar in upper right corner -> settings from the menu.  
7. In your profile's settings go to "pages". There is not much in here except verification of your custom domain. In your domain registrar's service add a new TXT record to your DNS registry according to instructions. 
8. While in your domain registrar's service, create also a DNS record of type CNAME that points to `YOUR_USERNAME.github.io`. Your web site contents will be in github.io although they appear at your custom domain after all of this is done. 
9. When those changes are done, go back to your Github and to the repository named `YOUR_USERNAME.github.io` that you created earier.  
10. Choose repository's settings -> Pages -> Type your custom subdomain here. In my case `janne.hamalainen.social`
11. Once the domain is verified and also the certificate creation for HTTPS connection completes, you can start creating your web site. 

Github pages uses Jekyll on the background so you can start pushing web site content right away and Github builds it for you behind the scenes. Or you can switch off Jekyll by adding a file named `.nojekyll` to the root of your repository, then the behaviour of the web site is more according to the expectations. 

## Part 2: verifying the new domain-backed handle 
12. Go to bsky.app and select settings -> account -> handle 
13. Click "I have my own domain" 
14. I selected "No DNS Panel" and pushed the text file name `atproto-did` to folder `.well-known` that contained the `did:...etc...`  according to instructions on the "No DNS Panel" page. I had the `.nojekyll` file present at this point so Jekyll wouldn't refuse to serve stuff from the dot folder. Alternatively you can use a TXT record again, but since I was registering a subdomain instead of an apex domain this approach seemed to work better. 

That's it. Updating DNS records and everything may take a moment, so if something doesn't succeed immediately try again after a while. 

# More about Jekyll 

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
