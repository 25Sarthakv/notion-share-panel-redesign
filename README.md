# notion-share-panel-redesign

Redesigning the share panel on notion so it is easy to see whether a page is private, open to the workspace, or only accessible with a link

## What this surface is

Tells you who can access a page

## Lock states

| State | What it means |
| --- | --- |
| Private | "No one can see this page except people with edit access." |
| Workspace | "Everyone in your workspace can open this page." |
| Anyone with Link | "Anyone with this link can open this page, including people outside your workspace." |

## Primary button behaviour

Copy link button, on click:
the page URL is placed on the clipboard, and the button label changes to "Copied" for 2 seconds, then back to "Copy link"

Copy link, by state:

| State | Who the copied link opens for |
| --- | --- |
| Private | Only people with edit access. Anyone else sees "You don't have access to this page" |
| Workspace | Everyone in your workspace. Anyone outside it sees "You don't have access to this page" |
| Anyone with Link | Anyone who has the link |

Expiry, when the user picks an expiry (Anyone with Link only):
the panel shows a line under the copy button reading "Link stops working on date", using the date chosen
Expiry, once the date has passed:
the link no longer opens the page and shows "This link has expired", the line under the copy button reads "Link stopped working on date", and the page goes back to Private

## Acceptance checks
1. 3 Rows are visible                                                                    Y/N
2. Switching the access to each state changes the status sentence to that state's row    Y/N
3. Page URL is placed on the clipboard on clicked                                        Y/N
4. Copy Link button changes to Copied for only 2s, then Copy Link                        Y/N
5. Panel shows a line under the copy button reading "Link stops working on date."        Y/N
6. After the expiry date, the link shows "This link has expired" and the page is Private Y/N


## Live prototype links
## Defect table
## Comparison scorecard
## Recommendation
