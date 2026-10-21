---
title: Registration
---

## Conference Registration

**{% include event-dates.html %}** &middot; {{ site.data.venue.name }}, {{ site.data.venue.address }}

**Your registration is only confirmed upon receipt of payment. Please make payment within {{ site.data.event.payment_hours }} hours of registration.**

{% if site.data.event.early_bird_deadline != "" %}**Early bird registration deadline is {{ site.data.event.early_bird_deadline }}.**{% endif %}

{% include register-button.html which="participant" label="Register as a Participant" %}

### Registration fees

{% include price-table.html rows=site.data.pricing.participant %}

### Meals

Meals are ordered at the time of registration. Gluten-free and dairy-free options are available; please note this in the special instructions when ordering.

{% include price-table.html rows=site.data.pricing.meals %}

### Accommodation

Accommodation requires pre-approval. Please call **{{ site.data.venue.accommodation.approval_phone }}**. *{{ site.data.venue.accommodation.warning }}.*

{% include price-table.html rows=site.data.pricing.accommodation suffix="/night" %}

{% for note in site.data.venue.accommodation.notes %}
*{{ note }}*
{% endfor %}

### How to pay

E-transfer to **[{{ site.data.event.etransfer_email }}](mailto:{{ site.data.event.etransfer_email }})**, or send a cheque payable to **{{ site.data.event.cheque_payable_to }}** to:

<address>
{% for line in site.data.event.mailing_address %}{{ line }}<br>
{% endfor %}
</address>

Please pray for the success of the conference.

### Have questions?

See the [Info & FAQ]({{ '/info.html' | relative_url }}) page, or email [{{ site.data.event.email.registration }}](mailto:{{ site.data.event.email.registration }}).
