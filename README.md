# Jonny-Jackson.com

![Jonny Jackson](static/uploads/this-portfolio-website/jonny-jackson.png)

My Portfolio Website, hosted on Netlify. Uses DecapCMS. I chose to use HUGO for my portfolio site for it's simplicity, incredible speed, good SEO, and easy maintenance. I used the [PaperMod Theme](https://github.com/adityatelange/hugo-PaperMod).

Make sure you `git pull` because any posts you add from the admin dashboard wont be here locally
`hugo server - start`

to deploy, simply push to github. it happens automatically.


Personal notes:
add image to media manager, then copy its path, then remove "static" so its "/uploads/learn-markdown-game/learn-markdown-game.png" (images are organized in project folders)

techstack formatting (if you type react the tooltip will be "React"):


- to add a new techstack, add a png (tho i technically dont think it needs to be png) in static/techstack_logos. update the list above. and thats it. you can add the filename in the list of techstack in the admin panel.
- some techstack logos are all black and therefore hard to see on dark mode. i open it upon in photoshop, add a blending options -> stroke of about 15 pixels white, and then it can be seen on light or dark mode
to add a new tooltip text, add to layouts/partials/techstack_logos.html