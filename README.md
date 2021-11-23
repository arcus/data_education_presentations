# Data Education Presentations
Presentations for scholarship from the Data Education team's R25 grant work.

## Installation instructions

To use reveal.js and reveal-md, with the [reveal-a11y plugin](https://github.com/marcysutton/reveal-a11y).

### reveal-md

Install [reveal-md](https://github.com/webpro/reveal-md)

```
brew update
brew install node
npm install -g reveal-md
```

## reveal-a11y plugin

Go to https://github.com/marcysutton/reveal-a11y and either clone the repo or download a zip of all the files.

In the terminal, navigate to the reveal-a11y directory you saved. To copy the contents of the accessibility subfolder and its contents to your reveal plugins directory, use the following command:

```
cp -r ./accessibility /usr/local/lib/node_modules/reveal-md/node_modules/reveal.js/plugin/
```

Then navigate to the reveal-md template directory:

```
cd /usr/local/lib/node_modules/reveal-md/lib/template
```

Open the `reveal.html` file to edit. You can do this in the terminal with `nano reveal.html`.

Follow the instructions at https://github.com/marcysutton/reveal-a11y, adding a link to the `helper.css` file, and copying in the script to call `helper.js` as a dependency. Specifically...

- Paste `<link rel="stylesheet" href="plugin/accessibility/helper.css" />` within the header section of the html file (there's a short section of other css files linked there, so it makes sense to add this reference to that list).
- Paste the following into the body of the html file. I don't think it matters where, but I put it in at the end of the body section, just after `<script>  Reveal.initialize(options); </script>`.

```
<script>
Reveal.initialize({
	dependencies: [
                { src: 'plugin/accessibility/helper.js', async: true, condition: function() {
                	return !!document.body.classList;
                }
            }]
});
</script>
```

Now when you use reveal-md, the a11y plugin should be active. 

## Workflow

Write your presentation as a markdown file, including YAML header options and css in a `style` section at the end (you can also use a separate css file, if you prefer). To preview a rendered version of your presentation, in the terminal navigate to the folder with your presentation .md file and run `reveal-md presentation_template.md -w`, replacing with the name of your file instead of presentation_template.md (the -w flag makes it update as you go, so you can make changes to your .md file and save, and it will be reflected in your browser preview).

To save a static version of your presentation, e.g. to share via github, run `reveal-md presentation_template.md --static docs`. This generates a directory called "docs" with everything needed to host your presentation as a static site.
