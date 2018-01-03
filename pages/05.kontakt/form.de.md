---
title: Kontakt
form:
    name: contact-form
    fields:
        -
            name: email
            label: E-Mail-Adresse
            placeholder: 'Ihre E-Mail-Adresse'
            type: email
            validate:
                required: true
        -
            name: message
            label: Nachricht
            placeholder: 'Ihre Nachricht'
            type: textarea
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Absenden
    process:
        -
            email:
                subject: '[{{ site.title }} Kontaktformular] {{ form.value.email|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Wir antworten Ihnen baldmöglichst!'
        -
            display: thankyou
---

# Kontakt
Schreiben Sie uns eine E-Mail an [TODOmail](mailto:TODOmail), nutzen Sie das folgende Formular oder rufen Sie uns an:

- Festnetz: TODO
- Mobiltelefon: TODO