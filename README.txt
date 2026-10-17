Diamond API files
=================
Host these as plain text on GitHub (raw links) and paste the link into the dev panel's API tab.
The tab reads the SAME JSON the game's own /api/avatar/v4/items answers with, so every file is a JSON array.

avatar_items_all.txt  every avatar item in the server catalog (3609)   -> use this one for "everything"
clothing.txt          the catalog without the skin-like items (3171)
skins.txt             items whose NAME looks like a skin / head / body / fur / full body (438) - a name guess, there is no skin flag in the data
consumables.txt       the server's Consumables list (540) - NOT read by the API tab yet (it only swaps the avatar items answer)

Notes
- UGC (player-made outfits) is NOT needed for the normal clothing and skins: first-party clothing is ordinary avatar items. The UGC files on the
  server (FirstPartyUGC.json 7.7 MB, UGC.json 70 MB) are a different list and the API tab does not read them.
- AvatarItemDesc is "guid,combination,combination,combination" (4 fields, full UUIDs). Keep that shape for anything you add by hand.
- Mode "Add" keeps the server's list and appends what the file has that the server did not send; "Replace" answers with just the file.
