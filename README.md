# George Rouse-Mighall

A one-page site for chefs who are short on time. It is published at [georgechef.miggle.net](https://georgechef.miggle.net/).

The words, jobs, photos, and videos all live in [content.js](content.js). Photos live in [images/](images/).

## Add a dish

1. Put the photo in the `images` folder. Use a simple file name, such as `roast-chicken.jpg`.
2. Open `content.js` and add a block inside `dishes`, using the commented example as the pattern:

```js
dishes: [
  {
    image: "images/roast-chicken.jpg",
    title: "Roast chicken",
    caption: "Crispy skin, gravy from the roasting juices.",
  },
],
```

3. Save, then commit and push. The Dishes section appears on its own once there is at least one photo. Until then it stays off the page. On the site, swipe left for the next photo. The caption sits in a strip along the bottom of the picture.

In Cursor you can say: “add this photo as a dish called roast chicken, with this caption.”

## Add a YouTube video

Paste a normal YouTube link into `videos` in `content.js`:

```js
videos: [
  {
    title: "Jointing a chicken",
    url: "https://www.youtube.com/watch?v=VIDEO_ID",
  },
],
```

The page turns that link into a player. The In the kitchen section stays hidden until there is a real link. This site does not use Instagram.

## Publish a change

From this folder:

```bash
git add content.js images
git commit -m "Add a dish"
git push
```

GitHub publishes the files a minute or two later. Open [georgechef.miggle.net](https://georgechef.miggle.net/) again. The page checks for a new copy of itself on each visit, so a normal reload is enough. If you replace a photo but keep the same file name, change `rev` in `content.js` to any new word so phones pick up the new picture.

## First-time Pages switch

This only needs doing once, and only George can do it. Push access cannot change repository settings.

1. Open [github.com/gjerm17/gjerm17.github.io/settings/pages](https://github.com/gjerm17/gjerm17.github.io/settings/pages).
2. Under Build and deployment, choose Deploy from a branch.
3. Branch: `main`. Folder: `/` (root). Save.
4. Custom domain should read `georgechef.miggle.net`, from the `CNAME` file. If the box is empty, type that and save.
5. When the certificate is ready, turn on Enforce HTTPS.

DNS is already in place: `georgechef` is a CNAME to `gjerm17.github.io`.
