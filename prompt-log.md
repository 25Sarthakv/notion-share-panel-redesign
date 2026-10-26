# Prompt Session Log, Share Panel (v0)

I built a clickable share panel in v0 from this project's README so anyone can click through the three states and check it against the spec.

## Prompt 1, the paste-in

I pasted the README in as written, with one line added at the top: "I want one share panel screen only." I left off the empty headings at the bottom.

```
I want one share panel screen only.

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
```

## Follow-ups

v0 added a dropdown next to Copy link that isn't in the spec. I sent four follow-ups, one over the three allowed. The first three tried to fix the dropdown and the fourth deleted it.

1. "why doesn't the dropdown next to the copy link click?"
   *On screen:* clicking the dropdown next to Copy link now opens a menu. Before, nothing happened.

2. "The drop-down works, but anything that should be visible in the drop-down is not visible. It's covered by the edge, so you need to fix that."
   *On screen:* the menu's options are now fully visible. Before, they were cut off at the edge of the card.

3. "Now, when you do the drop-down during the anyone with link, the link expiry and that drop-down kind of coincide. It's not very UI-friendly. Find a way to make it UI-friendly."
   *On screen:* with Anyone with Link selected, the menu no longer sits on top of the Link expiry field.

4. "You know what? Get rid of the drop-down. We don't need it. Get rid of it."
   *On screen:* the dropdown is gone. The card shows only the three state rows, Copy link and the Link expiry field.

Next time I would add "Do not add any dropdowns or menus" to the first prompt.

## Live link

https://notion-share-panel-redesign.vercel.app/

Published with the Publish button. It opens with no login.

## Screenshots

One per state.

![Private](01-notion-private.png)
![Workspace](02-notion-public.png)
![Anyone with Link](03-notion-link.png)
