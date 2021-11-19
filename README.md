# Data Education Presentations
Presentations for scholarship from the Data Education team's R25 grant work.

## To use reveal.js and reveal-md

```
brew update
brew install node
npm install -g reveal-md
```

Write your presentation as a markdown file, including YAML header options and css in a `style` section at the end (you can also use a separate css file, if you prefer). To preview a rendered version of your presentation, in the terminal navigate to the folder with your presentation .md file and run `reveal-md presentation_template.md -w`, replacing with the name of your file instead of presentation_template.md (the -w flag makes it update as you go, so you can make changes to your .md file and save, and it will be reflected in your browser preview).

To save a static version of your presentation, e.g. to share via github, run `reveal-md presentation_template.md --static docs`. This generates a directory called "docs" with everything needed to host your presentation as a static site. 
