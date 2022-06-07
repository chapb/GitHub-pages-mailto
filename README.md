# How to use GitHub Pages to serve a "mailto:"

A "mailto:" link (defined in [RFC6068](https://datatracker.ietf.org/doc/html/rfc6068)) prompts the user to create a new email in their default mail client, with an address, subject, and body you specify. Using GitHub pages, we can create a simple website that automatically opens a mailto: link without user interaction.

## Purpose

Using this scheme, you can share a mailto: link where it is normally only be possible to share a URL, such as a QR code. 

## Example

[Click Here](http://chapmanb.com/GitHub-pages-mailto/) to open the example website, which should open an email to "someone@example.com", with the subject "Example Subject Line", and the body "Example Body Contents".

## How To

1. Click "Use this template" above to create a new repo.
2. Update [index.html](index.html) to customize your mailto: link, replacing the default contents.
3. Navigate to Settings > Pages and enable GitHub Pages on your repo, by selecting the main branch as a source.
4. Copy the link generated (based off your username and repo title); this is the link to your new site.
5. Wait 1 - 2 minutes while your site is brought online (a similar wait is required after commiting changes), and try it out! 

## mailto: Specifications

- "mailto:?tag1=contents&tag2=contents&tag3=contents ..."
  - the first tag is prefixed with "?"
  - subsequent tags are prefixed with "&"
- all contents **must** be URL (percent) encoded
  - find [an explanation and simple encoder here](https://www.w3schools.com/tags/ref_urlencode.asp)
- common tags include:
  - ?to=
  - ?subject=
  - ?body=
