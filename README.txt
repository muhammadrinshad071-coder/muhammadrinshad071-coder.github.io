RINSHAD'S PERSONAL PORTFOLIO + AZODER'S COMPANY WEBSITE

Personal portfolio: index.html
Company website: azoder/index.html

The personal portfolio introduces Muhammed Rinshad, his skills, education,
AceZoder project and role as founder. Azoder has its own design, services,
business challenge explorer, delivery process and enquiry flow.

PERSONAL PORTFOLIO: GITHUB PAGES

Repository:
  https://github.com/muhammadrinshad071-coder/muhammadrinshad071-coder.github.io

Website:
  https://muhammadrinshad071-coder.github.io/

Publishing source: main branch, / (root) folder. No build command is needed.
The .nojekyll file makes GitHub Pages serve the static files directly.
Changes committed to main publish automatically at the same website address.

To update through GitHub:
 1. Open the repository above and select index.html.
 2. Use the pencil / Edit button to make your changes.
 3. Commit the changes to main. Wait for the Pages deployment to finish.
 4. Refresh the website. Assets can be replaced using Add file / Upload files.

To publish local edits, run these commands from this folder:
  git add index.html photo.webp favicon.svg azoder/assets/acezoder-preview.jpg
  git commit -m "Update portfolio"
  git push origin main

Chosen custom address: rinshad.us.kg. Registration and connection are pending.
Before adding a CNAME file or changing Pages' custom-domain setting, confirm
registration, the free slot, renewal requirements, and the DNS configuration.
When the custom address is working, update og:url, og:image and the canonical
link in index.html to use https://rinshad.us.kg/ and commit those changes.

The previous manually deployed portfolio was https://rinshadportfolio.netlify.app/.

AZODER'S SEPARATE COMPANY SITE

Published on Cloudflare Pages on 21 November 2026:
  https://azoder.pages.dev/

Cloudflare project: azoder. Production branch: main. Static deployment; no build.
The personal index.html now links to this separate company site.
Keep azoder/assets/acezoder-preview.jpg in the personal deployment, as it is the
AceZoder project screenshot used by the personal portfolio. The .gitignore file
includes that screenshot and excludes the separately deployed company source.

Requested custom domain: azoder.eu.org. The EU.org request was submitted on
21 November 2026 (confirmed by the user). It is attached to the Cloudflare Pages
project, but registration approval and public DNS activation are not confirmed.
The Cloudflare DNS zone is on the Free plan. Its assigned nameservers are:
  ara.ns.cloudflare.com
  yadiel.ns.cloudflare.com

Follow azoder/README.txt for redeployment and the remaining domain setup.
Once https://azoder.eu.org/ is approved and working over HTTPS, replace the two
https://azoder.pages.dev/ links in the personal index.html and redeploy the
personal portfolio. The current company address works while approval is pending.

LOCAL PREVIEW

Open index.html for the personal page, or azoder/index.html for the company.
For working folder links, run this command from this folder:

 python -m http.server 8080

Then visit http://localhost:8080/ and http://localhost:8080/azoder/.

EDITING

Personal content, styles and interactions: index.html
Company content: azoder/index.html
Company design and motion: azoder/styles.css
Company interactions: azoder/script.js
Project screenshot: azoder/assets/acezoder-preview.jpg

The company enquiry form prepares an email draft for the visitor to review
and send. It includes a copy option for webmail. To change the company email,
replace muhammedrinshad071@gmail.com in azoder/index.html and redeploy.
The company script automatically follows the contact email link.
See azoder/README.txt for company mailbox setup and post-deployment changes.
