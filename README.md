# What's the manner?

1. What's this thingy here?
2. What it does?
3. What it needs?
4. Am I supposed to used it at all?

... good questions tho.
Let's see the answers, I got for ya'
---

## What's this thingy here?

It supposed to be a generator which in a unified way creates the so-called _Timesheet_ (in `GoogleDrive`).

This file is necessary, so we are able to track our working hours easily,
that for e.g. can be used to invoice, or simply follow the working hours on a monthly basis.

## What it does?

Creates a GoogleSheet (Google's own type&format of excel-like Google file).
U'r use-case not necessarily involves the usage of GoogleSheets, tho this way I fear not of losses, and am able to keep
track of all the Sheets.

### My use-case also involves a few steps which are necessary for me to do every time:

* copy-paste a new Sheet
* modify so it contains the up-to-date info
* keeping track of the already accumulated hourly-based salary only (so that I know where am I standing)
* rename
* move the previous Sheet to a folder to be _archived_
* being happy

### After using this notebook:

* month as a number
* configure every run by the strictly necessary info (excess or missing hours - per week, or one value as I wish)
* add some elements that are needed to be invoiced (e.g. accountable expenses: business-lunch, trips, whatever u'r
  use-case might be)

## What it needs?

### First, a Google project with its API settings for GSheet & credentials

This is essential, so aren't required to step in whenever any interaction is needed with Google.

To do this, we need:

* to first of all follow the
  lines [here based on Google's description](https://developers.google.com/sheets/api/quickstart/python),
  so we are able to make everything from the list below
* a new/existing Google project for this purpose
* API settings for GSheet
* create the credentials (for the bot choosing the type: [**Service
  account**](https://developers.google.com/workspace/guides/create-credentials#service-account))
* access right on the specific folder that you want to use for generating and storing GoogleSheets for this new bot
    * to get the email (for the bot): read the value from service_account.json using simple bash, so you're able to
      share GDrive folders with that mail
    * > $ cat ~/.config/gspread/service_account.json | jq -r '.client_email'

## Am I supposed to used it at all?

Only in case you want to have fun by simply spending 2 mins for a setup, 2 mins for verification at the end.
And willing to use GoogleSheet, as it's a must to have.
