# notion-share-panel-redesign

Redesigning the share panel on notion so it is easy to see whether a page is private, public, or only accessible with a link

## What this surface is

Tells you who can access a page

## Lock states

| Private | Public | Anyone with Link |
| --- | --- | --- |
| private to you only | open to the whole workspace | open to anyone with the link  |
| Only you can open this page  | Anyone in your workspace can open this page | "Everyone in your workspace can open this page." |
| "Anyone with edit access can change this page." | Anyone with a link can open this page | "Anyone with this link can open this page, including people outside your workspace." |

## Primary button behaviour

Copy link button, on click:
the page URL is placed on the clipboard, and the button label changes to "Copied" for 2 seconds, then back to "Copy link"
Expiry, when the user picks an expiry:
the panel shows a line under the copy button reading "Link stops working on date", using the date chosen
no invisible behaviour. if you cannot see it in the panel, do not write it.

## Acceptance checks
1. 3 Rows are visible                                                                    Y/N
2. Copy Link button is clickable                                                         Y/N
3. Page URL is placed on the clipboard on clicked                                        Y/N
4. Copy Link button changes to Copied for only 2s, then Copy Link                        Y/N
5. Panel shows a line under the copy button reading "Link stops working on date.         Y/N


## Live prototype links
## Defect table
## Comparison scorecard
## Recommendation
