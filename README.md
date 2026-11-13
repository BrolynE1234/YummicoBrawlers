# Yummico Brawlers

A fighting game starring the Yummicos. It runs right in the browser, with nothing to install.

- **Play Yummico Brawlers (free):** open the site's main page (`index.html`)
- **Yummico Brawlers Deluxe (paid upgrade, $2.99):** `deluxe.html`. It stays locked until the player unlocks it.

## Putting it on GitHub Pages

1. Make a new **public** repository on GitHub (for example `yummico-brawlers`), or open the one you already have.
2. Click **Add file › Upload files** and drag in everything from this folder:
   `index.html`, `deluxe.html`, the three icon pictures, `README.md` and `.nojekyll`.
   (`.nojekyll` is hidden on some computers. The game still works without it.)
3. Click **Commit changes**.
4. Go to **Settings › Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*,
   pick the **main** branch and the **/ (root)** folder, then click **Save**.
5. Wait a minute or two, then refresh that page. GitHub shows your link, which looks like
   `https://YOUR-NAME.github.io/yummico-brawlers/`.

## Selling the Deluxe upgrade on itch.io

Every buyer gets their **own** unlock code. The game knows 200 codes. The list of codes is NOT in this folder:
it is the separate file `yummico-deluxe-unlock-codes.txt`. Keep that file private and never upload it to GitHub.

1. Make a free account at itch.io and click **Upload new project**. Call it *Yummico Brawlers Deluxe*.
2. Set **Kind of project** to *Downloadable*, and under **Pricing** pick *Paid* and type **2.99**.
   Upload the Deluxe HTML file as the download, and save the page.
3. On the project's edit page, open the **Distribute** tab (it may be called **Download keys**) and go to **External keys**.
   Add a new key type (use a custom/"Other" type, not Steam), name it *Deluxe unlock code*, and paste in all the codes from
   `yummico-deluxe-unlock-codes.txt`. itch.io then gives each buyer one code on their download page.
4. In the project's description, add: *After buying, copy your Deluxe unlock code from your download page. In Yummico Brawlers,
   go to STORY & MORE > GET DELUXE and type it in.*
5. Set the page to **Public** and copy its link (it looks like `https://yourname.itch.io/yummico-brawlers-deluxe`).
6. Open `index.html` **and** `deluxe.html` in a text editor (Notepad or TextEdit). Right at the very top is a short
   `DELUXE UPGRADE SETTINGS` part. Your page link (`https://poyopoyopoyo.itch.io/yummico-brawlers`) is already filled in. If it ever changes, replace it
   in both files, save, and upload them again.

Players press **BUY DELUXE** in the game, which opens your itch.io page. After buying, they type their code,
and **PLAY DELUXE** opens `deluxe.html`. The unlock is saved in their browser, so they only type it once per device.

### Good to know about the codes

- The lock runs in the browser, so a player who knows code could get around it. A code is not used up when someone types it,
  so if one buyer shares their code, it still works for others. Because every buyer has their own code, you can see in
  itch.io which buyer a shared code came from.
- To turn off a code that was shared: ask Claude to remove it from the game (or find its line in the code list,
  run `ybMakeCode('THAT-CODE')` in the browser Console (F12), and delete the long number it prints from `codes: [...]` in both files).
- When itch.io runs low on unused codes, ask Claude for more codes and an updated game.
- Don't use the upgrade button in the Google Play version: Google requires its own payment system for in-app purchases.
  Set `on: false` in that copy's settings to hide the button.
- itch.io needs payout settings (PayPal or Stripe) before it can pay you. Set these in your itch.io account settings.

## Good to know

- Opening `index.html` on github.com itself only shows the code. Use the GitHub Pages link to play.
- Progress and Mod Mode Yummicos save in each player's own browser.
- Works on computers, tablets and phones, with keyboard, controllers or touch.
