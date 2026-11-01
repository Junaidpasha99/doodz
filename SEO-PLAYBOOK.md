# Doodz SEO, GEO and Promotion Playbook

## 0. Before you upload (5 minutes)
1. Your domain is already set everywhere to https://doodz-rust.vercel.app. If you later buy a custom domain, swap it with:
   `grep -rl "doodz-rust.vercel.app" . | xargs sed -i 's#https://doodz-rust.vercel.app#https://yournewdomain.com#g'`
2. Upload the whole folder to the site root. Keep `Doodz.apk` in the root too.
3. Check these open: `/robots.txt`, `/sitemap.xml`, `/llms.txt`, `/og-image.png`, `/guides/how-to-auto-draw-on-instagram-doodle/`.
4. You are on Vercel, so `vercel.json` handles security headers, caching and the APK download. Keep it in the project root. A custom domain later (even a cheap .com or .in) will rank and look more trustworthy than a vercel.app subdomain.
5. In `index.html`, the schema says the app is free (price 0 INR). Change it if it is not.

## 1. Keywords (you are creating a category, so own the exact phrases)
Because nobody else sells this, people search by what they want to *do*. Target these:

| Tier | Keywords | Where used |
|---|---|---|
| Brand | doodz, doodz app, doodz apk, hyper doodle | Title, H1, schema, llms.txt |
| Core | instagram doodle auto draw, auto draw instagram doodle, instagram doodle app, instagram doodle android app | Title, H1, meta, intro |
| Problem | draw image on instagram doodle, instagram doodle copy image, trace image instagram doodle, perfect instagram doodle | FAQ, guides |
| How-to | how to auto draw on instagram doodle, how to draw a picture on instagram automatically | Guide page, FAQ, HowTo schema |
| Ideas | instagram doodle ideas, instagram doodle portrait, instagram doodle logo, instagram doodle meme | Ideas guide |
| Hinglish/India | instagram doodle kaise banaye, instagram doodle auto draw app download | Future Hindi/Hinglish guide, YouTube titles |

Next guide pages to write (one new page every week, 400-700 words, answer first): "instagram doodle not drawing correctly (fix)", "best images for instagram doodle", "instagram doodle colour palette explained", "instagram doodle kaise banaye (Hinglish)", "Doodz vs drawing by hand".

## 2. What is already built into the site
- Keyword-rich title, meta description, H1, canonical, Open Graph and Twitter cards.
- JSON-LD: WebSite, Organization, SoftwareApplication, WebPage, HowTo and a FAQPage built from all 18 FAQs.
- Answer-first definition, "at a glance" table and Standard vs Hyper comparison table (easy for AI answers to quote).
- `llms.txt`, AI crawlers allowed in `robots.txt`, XML sitemap, 3 supporting guide pages with Article and Breadcrumb schema.
- Accessibility and speed basics: skip link, semantic `<main>`, noscript fallback, shorter loader.
- Contact: email, WhatsApp button (floating) and a Contact section.

## 3. GEO (getting cited by ChatGPT, Gemini, Perplexity, Claude, AI Overviews)
- Keep the product described the same way everywhere: "Doodz is an Android app that automatically draws any image as an Instagram doodle."
- Publish the same one-line description on every profile you create (see section 4). Repeated, consistent mentions on different sites are what AI systems trust.
- Get mentioned on third-party pages (Reddit answers, Product Hunt, directories, blogs, YouTube descriptions). AI answers lean heavily on these.
- Keep facts current and dated (the page shows "Last updated"). Update it when you ship a new version.
- Never fake reviews or ratings. The schema intentionally has no rating.

## 4. Promotion plan
**Free profiles (do first, same description + link):** Google Search Console, Bing Webmaster Tools, Product Hunt, AlternativeTo, Indie Hackers, GitHub README (link to site), LinkedIn page, X/Twitter, Instagram + YouTube channel named "Doodz".

**Content that sells this app (it is visual, so show it):**
- Screen-record a doodle being drawn, 15-30 seconds, as Reels, YouTube Shorts and TikTok. Hook: "I didn't draw this." Put the site link in bio and description.
- Post before/after: original picture vs finished doodle.
- Titles to use: "Auto draw anything on Instagram doodle", "Instagram doodle hack (Android)", "How I send perfect doodles on Instagram".
- Pin a comment with the link. Reply to every comment (it feeds the algorithm).

**Communities (read each rule first; give value, do not spam):** r/androidapps, r/InstagramTips-type subreddits, Android and Instagram Facebook groups, Telegram/WhatsApp tech groups, Discord servers about Instagram or Android tools. Answer real questions like "how do I draw X on Instagram doodle" and mention Doodz honestly as your own app.

**Outreach:** send a short WhatsApp/email to 20 small Android and Instagram-tips YouTubers offering early access. Template: "Hi, I made Doodz, an Android app that auto-draws images as Instagram doodles. Want a link to try it and a 20-second demo clip you can use?"

**Trust (this matters for conversion):** direct APK downloads trigger Chrome/Play Protect warnings. Sign the APK, host over HTTPS, keep the file size and version on the page, and scan it on VirusTotal. A Google Play listing, if you can get approved, would add more trust and a second ranking surface.

## 5. After launch (technical checklist)
1. Add a URL-prefix property in Google Search Console (vercel.app subdomains cannot use DNS verification, so use the HTML meta tag method: paste the tag into the commented line in index.html head), then verify, submit `sitemap.xml`, then use URL Inspection > Request indexing for the home page and each guide.
2. Add the site to Bing Webmaster Tools (also feeds ChatGPT search and Copilot). Turn on IndexNow if your host supports it.
3. Test: Rich Results Test (schema), PageSpeed Insights (target green Core Web Vitals), mobile-friendly check, and a Facebook/Twitter card preview of the home URL.
4. Add privacy-friendly analytics (Plausible, or GA4) and track clicks on the download button and WhatsApp button.
5. Build a few real backlinks: Product Hunt, AlternativeTo, your own ForVano site, GitHub, YouTube descriptions.
6. Consider a short Privacy Policy page; it helps trust and any future store listing.

## 6. 30-day plan
- **Week 1:** deploy, verify Search Console and Bing, submit sitemap, create all profiles.
- **Week 2:** post 5 short videos, submit to Product Hunt and AlternativeTo, answer 10 community questions.
- **Week 3:** publish 2 new guides, reach out to 20 creators.
- **Week 4:** check Search Console queries, rewrite the title and FAQ around the phrases people actually use, double down on the best-performing video type.

## 7. Honest notes
- SEO takes weeks to months. Nothing here guarantees rankings. Because competition is low, the exact-match phrases above are realistic to win.
- Doodz is unofficial. The FAQ explains it works on top of Instagram, never asks for an Instagram login and only uses the Accessibility permission. Keep that factual wording and avoid absolute claims like "ban-proof" or "100% safe", which you can't prove and AI answers will repeat.
