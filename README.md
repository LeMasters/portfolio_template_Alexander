# Alexander — student portfolio

A plain, fast portfolio site. You edit it in **Pages CMS**; **GitHub** builds it with Hugo and publishes it at `https://your-username.github.io/your-repository/`.

You never need to install anything or touch code. Everything you write is kept in ordinary text files that you own and can take to any other site.

> **Prototype, version 0.7.0 (November 2026).** This is a bare starter for review by Miami faculty and a few students: it holds no content yet, so a new copy shows only "Your Name" until you fill in the forms. Comments and problems to Garrison LeMasters (ETBD).

## Starting a new site from this template

You need a free GitHub account. Allow about fifteen minutes.

1. On this repository's GitHub page, choose **Use this template → Create a new repository**. Give it a name (it becomes part of your address), make it **Public**, and create it.
2. In the new repository, open **Settings → Pages** and set **Source** to **GitHub Actions**. Ignore the suggested workflows.
3. Open the **Actions** tab. The first run, made when the repository was created, will have failed with a red ✗ because Pages wasn't on yet. Open it and choose **Re-run all jobs**. When it turns green, your site is at the address shown under **Settings → Pages**.
4. Go to [app.pagescms.org](https://app.pagescms.org) and sign in with GitHub. If your repository isn't listed, give Pages CMS access to it: on GitHub, open **Settings → Applications → Installed GitHub Apps → Pages CMS → Configure**, add the repository under **Repository access**, and save. Then reload Pages CMS.
5. Open your repository in Pages CMS and start with **Profile**: replace "Your Name" and save.

Don't download the files and upload them to a new repository by hand: GitHub's uploader silently skips the files whose names start with a dot (`.pages.yml`, `.github/…`), and the site then neither builds nor shows any forms.

## Editing your site

Open [app.pagescms.org](https://app.pagescms.org), choose this repository, and use the eight forms:

| Form | What it holds | Leave it empty and… |
|---|---|---|
| **Profile** | Your name, area of expertise, your About paragraph, résumé (PDF), email, LinkedIn and GitHub addresses, and Custom Links (your other sites) | …the About section, Contact section, LinkedIn button or GitHub button disappears |
| **Selected Work** | One entry per piece of work: title, kind (case study, project or brief; shown as a small label before the title), caption, description, image and its alt text, year, role, links, tags, sections (case studies and projects only: a picture beside text, swapping sides on each row; a new entry starts with seven suggested headings, Problem to Reflection, which you fill, reorder, rename or delete), order | …the Selected Work section disappears |
| **Gallery** | One entry per image: title, image, whether to show it on the home page, alt text, order, caption | …the Gallery section, the Gallery page and the menu link disappear |
| **Experience** | One entry per job, internship or assistantship: role, organization (and its website), location, dates, order, what you did, and related work chosen from a list of your Selected Work | …the Experience section disappears |
| **Education** | One entry per degree or certificate: degree, school, year, order, optional detail | …the Education section disappears |
| **Tools** | The software, languages and media you use. Choose each from the **Tool** list, which shows it with its logo (or a plain icon); if yours isn't listed, type it under **Other tool**. Each has an optional note that stays general (how long, how much, what kind of work: "C#; three years"), never about one project | …the Tools section disappears |
| **Appearance** | Colour scheme (Ink or Dusk), typeface for text, typeface for titles | (defaults are used: Ink, Atkinson, Fraunces) |
| **Analytics** | Visitor statistics (a service, GoatCounter or Cloudflare, and its code); whether AI companies may train on your site (off unless you turn it on); an optional Google Search Console code | (no visitor statistics; AI training stays refused) |

Each save publishes the site again within a minute or two. The menu at the top lists only the sections that have something in them.

**Don't see your change?** Wait two minutes, then refresh the page (on a Mac, Cmd-Shift-R; on Windows, Ctrl-F5). Browsers often show a copy of a page they saved earlier. If it still hasn't changed, open your repository on GitHub and look at the **Actions** tab: a red ✗ means the site didn't rebuild, and your previous site is still online.

### What happens when you save

1. Pages CMS saves your words and images into your repository on GitHub (it records every version, so nothing is lost).
2. GitHub notices the change and runs **Hugo**, a program that turns your files into a finished website. Hugo makes smaller copies of your images for phones and laptops, builds a page for each piece of work and gallery image, and adds the details search engines and link previews need.
3. GitHub Pages publishes the result.

Nothing runs on your site itself; it is plain web pages, which is why it's fast. The full details are in `docs/DESIGN.md`, section 2.

### Selected Work: kinds and layout

Each entry in Selected Work has a **Kind**, shown as a small label ("Case study", "Project" or "Brief") before its title on the home page and above the title on its own page:

| Kind | On the home page | Its own page |
|---|---|---|
| **Case study** | A full-width card at the top | A long read: your title, caption and description in an outlined box; role, year, tags and links, with a contents list when you use three or more headings; the image; then your Sections |
| **Project** (the usual choice) | A card, laid out as below | Title, caption and description in an outlined box; links and tags; the image; then your Sections |
| **Brief** | One line in a list at the end of Selected Work | A short page: title, image, description, links, tags (no Sections) |

For a case study, keep the description to a short opening and tell the story in **Sections**: each is a picture beside a paragraph or two. A new entry starts with seven suggested headings (*Problem · My role · Research · Prototype · Iteration · Outcome · Reflection*); fill the ones that fit and rename, reorder or delete the rest. A section with neither picture nor text doesn't appear. You can change an entry's kind at any time; nothing you've written is lost.

Within each kind, entries appear in **Order** (1 first). Without any case studies, the layout adjusts to how many projects (kind **Project**) you have:

| Projects | Layout |
|---|---|
| 1 | One wide project |
| 2 | Two side by side |
| 3 | One wide, then two side by side |
| 4 or more | One wide, then rows of three; a last row that isn't full lines up from the left |

With case studies, the case studies are the wide ones, and all your projects go in rows beneath them. On a phone, rows of three stack into one column; pairs stay side by side.

### Images

Upload images through the Selected Work form. Recommended: **1800 × 1200 px (3:2), under about 400 KB**. The site makes smaller copies for phones automatically, with tidy names: spaces and unusual characters become underscores (`My level 2.png` → `My_level_2-800w.webp`). Your original keeps its name in the repository. On the home page, a wide card shows only about the middle 60% of a 3:2 image's height, so keep titles, HUD and faces away from the top and bottom edges. Squarer images (4:3, square or portrait) are shown whole there instead, on a tinted band. The project's own page always shows the whole image.

Gallery images can be any shape. Your home page has a Gallery section: tick **Show on home page** for each image you want there (as many as you like; they appear in Order). If you tick none, the first five appear. The section ends with a link to the full Gallery page, which shows every image as a square crop with its title under it; clicking one opens its own page with the whole image, its title and your caption, and links to the previous and next image. Up to 2000 px on the long side, under about 500 KB.

Always fill in **Alt text** ("alternative text"): one sentence saying what the image shows. It is read aloud to people who cannot see the image, and search engines use it too.

### Experience

List jobs, internships and assistantships, most recent first (**Order** 1). If a job relates to an entry in your Selected Work (the tool you built during an internship, say), choose it under **Related work**: the job then links to that entry's page. If you later delete or rename the entry, the link simply disappears; choose again.

### Links

Type full addresses (`https://…`). If you forget the `https://`, the site adds it for you.

### AI training and search

By default your site asks AI companies not to use it to train their models. It does this in every page (a TDM-reservation tag, the opt-out recognised under EU copyright law, plus informal "noai" tags) and in a `robots.txt` file listing the main AI-training crawlers. Search engines, including AI search tools that link back to you, are still welcome. To allow AI training instead, switch on **Allow AI companies to train on this site** in the **Analytics** form.

These are requests: reputable companies honour them, but nothing technical can force a crawler to comply. A `robots.txt` file only works when the site is at the top of its web address (`your-username.github.io` or your own domain), not in a subfolder; the page tags work everywhere.

To help people find you in search: write a clear area of expertise and captions for your work, describe every image, link to your portfolio from LinkedIn, itch.io and anywhere else you are, and (optionally) add your site to Google Search Console and paste its verification code into the **Analytics** form.

### Visitor statistics (optional)

Your site can count its visitors using one of two free services. Neither uses cookies or collects visitors' personal details, so you don't need a cookie banner. The numbers are private: only you see them, in the service's dashboard; nothing appears on your site. Pick one:

**GoatCounter**: simplest; a small independent service.

1. Go to [goatcounter.com](https://www.goatcounter.com) and choose **Sign up**.
2. Pick a **code**: a short name such as `janedoe`. Your dashboard will be at `janedoe.goatcounter.com`. Add your email and a password.
3. In Pages CMS, open **Analytics**. Set **Service** to **GoatCounter** and type your code (just `janedoe`) in **Code**. Save.

**Cloudflare Web Analytics**: run by a large company; also shows how fast your pages load.

1. Create a free account at [cloudflare.com](https://www.cloudflare.com). You don't need to move your site or change any settings on GitHub.
2. In the Cloudflare dashboard, open **Web Analytics** and choose **Add a site**.
3. For the hostname, type your site's address without `https://` or any folder: `your-username.github.io` (or your own domain). Choose **Done**.
4. Cloudflare shows a short piece of code (a "JS snippet"). Copy all of it.
5. In Pages CMS, open **Analytics**. Set **Service** to **Cloudflare Web Analytics** and paste the snippet into **Code**. Save.

**Then check it works.** Wait for the site to publish (a minute or two), visit it from your phone, and look at your dashboard; your visit should appear within a few minutes. If nothing appears:

- Turn off any ad blocker for your site. Ad blockers often stop these services, which also means real visitor counts run a little low.
- Check the code you pasted. If the site can't recognise it, it leaves analytics out rather than breaking. The GitHub **Actions** tab then shows a yellow warning on that build starting "Analytics:".
- Visits are not counted while you preview your site on your own computer.

**To stop counting**, set **Service** back to **NONE** in the **Analytics** form.

### Your web address

Your site starts at `https://your-username.github.io/your-repository/`. You can give it an address of your own (such as `janedoe.com`, about $11 a year): see the separate guide *How to Set Up Your Own Domain Name*. Nothing in your content changes; the site picks up its new address on the next publish.

### Which template made your site

The small print at the very bottom of your home page ends with the template's name and version, e.g. "Template: Alexander 0.7.0". It tells your instructors which version of the template your site was made from. It changes only if the template files in `themes/Alexander/` are updated.

## Where your content lives

| File | What it is |
|---|---|
| `content/_index.md` | Your profile; the text below the `---` lines is your About paragraph |
| `content/projects/*.md` | One file per entry in Selected Work (the folder keeps its earlier name, so existing sites and links still work) |
| `content/gallery/*.md` | One file per gallery image; the text below the `---` lines is its caption |
| `content/experience/*.md` | One file per job, internship or assistantship |
| `content/education/*.md` | One file per degree or certificate |
| `data/tools.yaml` | Your tools |
| `data/style.yaml` | Your colour scheme and typeface choices (appearance, not content) |
| `data/analytics.yaml` | Your visitor-statistics, AI-training and Search Console settings |
| `static/images/`, `static/files/` | Your uploaded images and files |

These are plain Markdown and YAML files. To move your portfolio somewhere else, download the repository (Code → Download ZIP): your words and images come with you.

## Everything else

| Path | What it is |
|---|---|
| `themes/Alexander/` | The design (templates, styles, fonts). The same for every student. |
| `hugo.toml` | Site settings |
| `.pages.yml` | The Pages CMS forms |
| `.github/workflows/hugo.yml` | Builds and publishes the site on every save |
| `docs/DESIGN.md` | How the theme works and why (for instructors and maintainers) |

## Typefaces

Six open-source typefaces are included and served from your own site (no requests to Google or any other company). Choose one for text and one for titles in **Appearance**:

| Choice | Designer | Kind |
|---|---|---|
| Atkinson Hyperlegible Next (default for text) | Braille Institute | Sans-serif, designed for legibility |
| Inter | Rasmus Andersson | Sans-serif, neutral |
| Source Serif 4 | Frank Grießhammer / Adobe | Serif, classic |
| Fraunces (default for titles) | Undercase Type | Serif, expressive |
| Figtree | Erik Kennedy | Sans-serif, friendly |
| Literata | TypeTogether, for Google | Serif, made for long reading |

All six are licensed under the SIL Open Font License 1.1; each licence is in its folder under `themes/Alexander/static/fonts/`.

## Credits

Alexander theme © 2026 Garrison LeMasters, Miami University (Department of Emerging Technology in Business and Design). MIT licence (`themes/Alexander/LICENSE`). Built with [Hugo](https://gohugo.io) and [Pages CMS](https://pagescms.org); fonts via [Fontsource](https://fontsource.org).
