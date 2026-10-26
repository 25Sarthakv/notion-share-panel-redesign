# notion-share-panel-redesign

Redesigning the share panel on notion so it is easy to see whether a page is private, open to the workspace, or only accessible with a link

## What this surface is

Tells you who can access a page

## Lock states

| State | What it means |
| --- | --- |
| Private | "Only you can see this page." |
| Workspace | "Everyone in your workspace can open this page." |
| Anyone with Link | "Anyone with this link can open this page, including people outside your workspace." |

## Primary button behaviour

Copy link button, on click:
the page URL is placed on the clipboard, and the button label changes to "Copied" for 2 seconds, then back to "Copy link"

Copy link, by state:

| State | Who the copied link opens for |
| --- | --- |
| Private | Only you. Anyone else sees "You don't have access to this page" |
| Workspace | Everyone in your workspace. Anyone outside it sees "You don't have access to this page" |
| Anyone with Link | Anyone who has the link |

Expiry, when the user picks an expiry (Anyone with Link only):
the panel shows a line under the copy button reading "Link stops working on date", using the date chosen
Expiry, once the date has passed:
the link no longer opens the page and shows "This link has expired", the line under the copy button reads "Link stopped working on date", and the page goes back to Private

## Acceptance checks
1. The share panel shows three state rows: Private, Workspace and Anyone with Link        Y/N
2. Picking each state in turn changes the status sentence to that state's row             Y/N
3. Clicking Copy link puts the page URL on the clipboard (paste it into a new tab)        Y/N
4. After clicking Copy link, the button reads "Copied" for 2 seconds, then "Copy link"    Y/N
5. Picking an expiry date shows "Link stops working on date" under the copy button        Y/N


## Live prototype links
## Defect table
## Comparison scorecard
## Recommendation
