# Creating the Google Forms (two forms: Participants, Vendors)

Create these at https://forms.google.com signed in as the registration Gmail account (wcchscreg@gmail.com), so responses go there.

## One-time settings for both forms
1. **Settings > Responses**: turn on *Collect email addresses* (verified or "Responder input") and *Send responders a copy*.
2. **Settings > Responses > Get email notifications for new responses** (Responses tab > three dots): sends you an email each time.
3. **Responses tab > Link to Sheets**: creates a spreadsheet you can total up.
4. **Settings > Presentation > Confirmation message**: paste the payment text, e.g.
   > Thank you for registering. Registration is only complete on receipt of payment within 24 hours. Please e-transfer to wcchscreg@gmail.com, or mail a cheque payable to WCCHSC, 83 Granville Crescent, Sherwood Park, AB T8A 3C1. Please pray for the success of the conference.
5. When ready: **Send > link icon**, copy the link (use the shortened one), and paste it into `_data/event.yml` as `participant_form_url` / `vendor_form_url`. Then set `registration_open: true`.

## Form 1: Participant Registration
Sections and questions (mirrors the old site):
1. **Contact**: Email (collected), Phone number, City, Number of participants (short answer, number)
2. **Each participant's name** (paragraph: one name per line), mark which are adults/youth
3. **Registration** (number questions, 0 minimum): Single Adult ($120), Married couple ($160), Youth ($50)
4. **Accommodation** (do you need accommodation? Yes/No). If Yes, a new section: Room type (Single remote bathroom / Double with bathroom), Number of nights, Extra persons, plus text "Accommodation requires pre-approval: call 780-467-8410. Please do not call Providence Centre."
   Use *Go to section based on answer* so "No" skips it.
5. **Meals** (number, 0 minimum): Friday breakfast ($14), Friday lunch ($21), Friday supper ($22), Saturday breakfast ($14), Saturday lunch ($21)
6. **Special meal instructions** (paragraph: gluten-free / dairy-free)

## Form 2: Vendor & Exhibit Application
1. **Business**: Business/ministry name, Contact name, Email, Phone, What you sell, First time attending? (Yes/No)
2. **Tables**: Basic 1 table / 2 reps ($150), Additional tables ($40), Additional reps ($25); Need wall or electricity? (paragraph)
3. **Accommodation** (Yes/No, then same room questions and pre-approval text as above)
4. **Meals**: same as participant form
5. **Special meal instructions**

## About totals
Google Forms cannot add up prices. Two options:
* **Easiest**: you compute the total from the responses sheet (add a formula column in the linked Google Sheet, multiplying each answer by its price) and reply with the amount.
* Put the prices in the question text (e.g. "Single Adult ($120)") so people can work it out. The same prices are listed on the Registration page, from `_data/pricing.yml`.
**Remember**: when prices change, update both `_data/pricing.yml` and the question text in the forms. Make a copy of last year's form (**three dots > Make a copy**) each year instead of starting over.
