# How to update the WCCHSC website

You can do everything below in your web browser on github.com. No software is needed.
Every change you save ("commit") is published automatically in about 2 minutes.

## How to edit a file
1. On the repository page, click the file (for example `_data/event.yml`).
2. Click the pencil icon (**Edit**).
3. Change the text. **Only change what comes after the colon, and keep the quote marks.**
4. Click **Commit changes** (green button). Done. Check the **Actions** tab if you want to watch it publish.

If you make a mistake, the site's build will turn red in **Actions** and the old site stays up. Fix the file and commit again.

## Yearly checklist
| I want to change... | Edit this file | What to change |
|---|---|---|
| Conference dates | `_data/event.yml` | `start_date`, `end_date` (YYYY-MM-DD). Schedule weekdays update by themselves |
| Theme / title line | `_data/event.yml` | `theme` |
| Welcome text | `_data/event.yml` | `intro` |
| Banner message (e.g. "Fr. X confirmed") | `_data/event.yml` | `announcement` (use `""` to hide) |
| Open or close registration | `_data/event.yml` | `registration_open: true` / `false`, `registration_opens`, `early_bird_deadline` |
| Google Form links | `_data/event.yml` | `participant_form_url`, `vendor_form_url` |
| Show the schedule / speakers | `_data/event.yml` | `show_schedule`, `show_speakers` (true / false) |
| Contact emails, payment address | `_data/event.yml` | `email:` and `mailing_address:` sections |
| Venue and map | `_data/venue.yml` | See the comment in the file for the map link |
| Prices (registration, meals, rooms, tables) | `_data/pricing.yml` | The `price:` numbers |
| Schedule | `_data/schedule.yml` | Copy an existing line and change the time/title/speaker |
| Speakers | `_data/speakers.yml` | Copy one block, change name, talk and bio |
| FAQ | `_data/faq.yml` | Copy one question/answer pair |
| Colors | `_data/theme.yml` | Hex color codes |
| Top menu | `_data/navigation.yml` | Add, remove or reorder links |
| Page wording (Info, Vendors, Used Curriculum, Registration) | `info.md`, `vendors.md`, `usedcurriculum.md`, `registration.md` | Just type. Text in `{{ ... }}` is filled in from the data files above, so leave it alone |

## Pictures
1. Open the `assets/img` folder, click **Add file > Upload files**, and commit.
2. Refer to it as `/assets/img/yourfile.jpg`, for example `hero_image` in `_data/event.yml`.
3. Keep pictures under about 500 KB (resize large photos first). For speaker photos use a folder `assets/img/speakers/` and put `photo: "/assets/img/speakers/name.jpg"` in `speakers.yml`.

## Writing in Markdown (the .md pages)
    ## A heading
    A paragraph of text. **Bold** and *italic*.
    - A bullet list
    [Link text](https://example.com)

## Things that look scary but are normal
* A `---` at the top of a page is required. Leave it.
* Spaces at the start of lines in the `.yml` files matter. Copy a whole existing block rather than typing from scratch.
* Don't remove the quote marks around text values.

## Domain and publishing (one-time setup, for the site owner)
* GitHub: **Settings > Pages > Source: GitHub Actions**, custom domain `www.wcchsc.net`, tick **Enforce HTTPS**.
* DNS for `wcchsc.net`: `CNAME` record `www` -> `jduteau.github.io`. For the bare domain `wcchsc.net` add four `A` records (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) so it redirects to `www`.
* Do the same for `wcchsc.org`; GitHub Pages redirects only one custom domain, so point `wcchsc.org` at your registrar's "URL redirect" to `https://www.wcchsc.net` (or tell your DNS host to forward it).
* Once it works, remove the old NearlyFreeSpeech deployment.
