HVAC LEAD-TRACKING PORTFOLIO DEMO — START HERE

This is a fictional demo website for learning and portfolio evidence. It is not a real HVAC company. No requests are sent to a business. Use fictional test data only.

WHAT'S INCLUDED
- index.html: Responsive demo HVAC website
- Data-layer interactions: form_start, generate_lead, click_to_call, select_service, select_lead_cta
- No form names, email addresses, phone numbers, or free-text notes are pushed to dataLayer
- GTM placeholder is included in two places, waiting for your real GTM ID

STEP 1 — PUBLISH THE DEMO FOR FREE WITH GITHUB PAGES
1. Extract this ZIP on your computer.
2. Sign in at https://github.com/ and create a new PUBLIC repository named hvac-lead-tracking-demo (or similar).
3. Upload index.html and README-FIRST.txt to the repository's root directory (the main Code page). The index.html file must be at the root.
4. Open the repository's Settings > Pages.
5. Under Build and deployment, set Source to Deploy from a branch.
6. Select branch main and folder /(root), then Save.
7. Wait for the Pages deployment to finish. Copy the published HTTPS website URL shown in Settings > Pages. It usually looks like https://YOUR-USERNAME.github.io/hvac-lead-tracking-demo/.
8. The demo will display a yellow disclosure banner and is not a real business.

STEP 2 — CREATE A GTM CONTAINER
1. Open https://tagmanager.google.com/ and sign in.
2. Click Create account.
3. Account name: Fatema Portfolio Lab
4. Country: choose your own country (Bangladesh if that is where you are based).
5. Container name: use your published GitHub Pages URL or hvac-lead-tracking-demo.
6. Target platform: Web. Agree to the terms.
7. Copy the container ID, which starts with GTM-.
8. In index.html, replace ALL three occurrences of GTM-REPLACE_ME with your actual container ID. Upload/commit the changed file to GitHub.

STEP 3 — CREATE A GA4 PROPERTY
1. Open https://analytics.google.com/.
2. Create a property named HVAC Demo Analytics.
3. Set a suitable reporting time zone (Bangladesh is fine for your practice project) and currency USD for this U.S.-style demo.
4. Create a Web data stream using the published GitHub Pages URL.
5. Copy its Measurement ID, starting with G-.

STEP 4 — CONNECT GA4 THROUGH GTM (NOT DIRECTLY IN HTML)
1. In GTM, open Tags > New.
2. Choose tag type Google tag.
3. Enter your GA4 Measurement ID (G-...).
4. Trigger: Initialization - All Pages (or the default all-page initialization option offered in your interface).
5. Save. Do not add a second hardcoded GA4 tag to the website.
6. Preview GTM and connect to the HTTPS demo URL. Confirm the Google tag loads.
7. Publish only after you have verified the setup. For portfolio evidence, test first in Preview.

STEP 5 — TRACK CUSTOM EVENTS
The website pushes custom event objects to window.dataLayer after these user actions:
- form_start: first focus inside the quote form
- generate_lead: after the browser validates and accepts the demo form submission
- click_to_call: after a demo telephone link is clicked
- select_service: after a service CTA is clicked
- select_lead_cta: after a quote CTA is clicked

To send these events to GA4:
1. In GTM, create a Custom Event trigger for each exact event name above.
2. Create a GA4 Event tag for each event, use the Google tag/Measurement ID destination, and put the matching event name in the event-name field.
3. For generate_lead, you may add a Data Layer Variable for service_type if you want to send that parameter. Do not send form PII.
4. Test each event in GTM Preview's data layer and tag firing view, then confirm it appears in GA4 DebugView.
5. Document expected versus observed results. Don't claim a test passed unless you saw evidence.

IMPORTANT TEST NOTES
- This form simulates submission locally; it does not save or send form data to a server.
- The form is a test lead event, not a real customer inquiry or sale.
- A click_to_call event proves the link was clicked, not that a phone call connected.
- The GTM placeholder must be replaced before any tags can load.
- A GA4 event won't appear unless the relevant GTM event tag is configured correctly and the browser allows it.
- Don't submit real personal data. Don't claim the website belongs to a client.

OFFICIAL HELP
GTM account/container: https://support.google.com/tagmanager/answer/14842164
Install GTM: https://support.google.com/tagmanager/answer/14847097
Google tag in GTM: https://support.google.com/tagmanager/answer/14842872
Verify and publish: https://support.google.com/tagmanager/answer/14842769
GA4 setup: https://support.google.com/analytics/answer/14183469
GitHub Pages quickstart: https://docs.github.com/en/pages/quickstart
