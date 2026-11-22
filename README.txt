RINSHAD'S PERSONAL PORTFOLIO + AZODER'S COMPANY WEBSITE

Personal portfolio: index.html
Company website (local workspace): azoder/index.html

The personal portfolio introduces Muhammed Rinshad, his skills, education,
AceZoder project and role as founder. Azoder has its own design, services,
business challenge explorer, delivery process and enquiry flow.

PERSONAL PORTFOLIO: GITHUB PAGES

Repository:
  https://github.com/muhammadrinshad071-coder/muhammadrinshad071-coder.github.io

Website:
  http://rinshad.qd.je/

Intended secure address: https://rinshad.qd.je/ (certificate issuance is pending).
The default GitHub Pages address redirects to the custom domain.

Published on 21 November 2026. The Pages deployment completed successfully,
and the live page, portrait, favicon and AceZoder screenshot were checked.

Publishing source: main branch, / (root) folder. No build command is needed.
The .nojekyll file makes GitHub Pages serve the static files directly.
Changes committed to main publish automatically at the same website address.

To update through GitHub:
 1. Open the repository above and select index.html.
 2. Use the pencil / Edit button to make your changes.
 3. Commit the changes to main. Wait for the Pages deployment to finish.
 4. Refresh the website. Assets can be replaced using Add file / Upload files.

Before editing a clean checkout, synchronize changes made in GitHub's Pages settings:
  git pull --ff-only origin main

To publish local edits, run these commands from this folder:
  git add index.html photo.webp favicon.svg azoder/assets/acezoder-preview.jpg README.txt
  git commit -m "Update portfolio"
  git push origin main

CUSTOM DOMAIN AND HTTPS

Registered custom address: rinshad.qd.je, through DigitalPlat.
The repository's CNAME file and GitHub Pages custom-domain setting use this name.
Authoritative nameservers: dns1.digitalplat.org and dns2.digitalplat.org.

Configured DNS records:
  A (@): 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
  AAAA (@): 2606:50c0:8000::153, 2606:50c0:8001::153,
            2606:50c0:8002::153, 2606:50c0:8003::153
  CNAME (www): muhammadrinshad071-coder.github.io

Checked on 22 November 2026: both authoritative nameservers and public resolvers
return the expected records. GitHub's DNS health check approves the apex and www
hosts as HTTPS-eligible and reports no CAA error. The portfolio and its images
load over HTTP; www redirects to the apex domain.

HTTPS remains unfinished. GitHub reports certificate state bad_authz and
https_enforced: false. Its Pages settings show "Certificate Request Error" and
say provisioning will retry automatically. Curl and a browser both reject the
served *.github.io certificate because it does not cover rinshad.qd.je or www.
A controlled domain removal/restoration on 22 November returned the same error.
The original ACME rejection details are not exposed by the Pages REST API.
Keep the domain stable while GitHub retries; use Pages settings or GitHub Support
to obtain certificate details if the request remains failed.

To inspect the current state:
  gh api repos/muhammadrinshad071-coder/muhammadrinshad071-coder.github.io/pages
  gh api repos/muhammadrinshad071-coder/muhammadrinshad071-coder.github.io/pages/health

After a certificate has been issued, enable Enforce HTTPS in GitHub's Pages
settings and verify both hosts with normal certificate validation:
  curl.exe -I https://rinshad.qd.je/
  curl.exe -I https://www.rinshad.qd.je/
  curl.exe -I http://rinshad.qd.je/
  curl.exe -I http://www.rinshad.qd.je/
HTTP requests and the www host should redirect to https://rinshad.qd.je/.
Check the same addresses in a browser without bypassing certificate errors.

Once HTTPS works, update og:url and the canonical link in index.html to
https://rinshad.qd.je/, and og:image to https://rinshad.qd.je/photo.webp.

The previous manually deployed portfolio was https://rinshadportfolio.netlify.app/.

AZODER'S SEPARATE COMPANY SITE

Published on Cloudflare Pages on 21 November 2026:
  https://azoder.pages.dev/

Cloudflare project: azoder. Production branch: main. Static deployment; no build.
The personal index.html now links to this separate company site.
Keep azoder/assets/acezoder-preview.jpg in the personal deployment, as it is the
AceZoder project screenshot used by the personal portfolio. The .gitignore file
includes that screenshot and excludes the separately deployed company source.
The company's two founder links currently use the default GitHub Pages address,
which redirects to the personal custom domain. After the personal certificate
works, update those links to https://rinshad.qd.je/ and redeploy Azoder.

Requested custom domain: azoder.eu.org. The EU.org request was submitted on
21 November 2026 (confirmed by the user). It is attached to the Cloudflare Pages
project. Public DNS still returns NXDOMAIN as of 22 November 2026; registration
approval and public DNS activation remain unfinished.
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
