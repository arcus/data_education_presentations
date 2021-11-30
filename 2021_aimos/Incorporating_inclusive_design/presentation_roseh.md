In general, I feel like we'll be on safer ground with a talk focused on "how to incorporate inclusive design into data science education" rather than "how to make data science accessible" --- a subtle distinction, but it feels like we have more answers on the former than the latter.
For example, in talking about how to incorporate inclusive design, we could mention our review process (using a checklist template to create issues on GH to make sure we review for each of our inclusive design components).
We could also do a shout out to some of the excellent design resources available, such as the Inclusive Design Guide (https://guide.inclusivedesign.ca/) published by the Inclusive Design Research Center in Toronto, which includes a number of tools and activities for designers to help them build more inclusive material, like https://guide.inclusivedesign.ca/activities/inclusive-design-mapping/.
Another nice resource is the accessibility posters https://ukhomeoffice.github.io/accessibility-posters/posters/accessibility-posters.pdf .
We could talk about opportunities we've found to let users customize and control their own experience: Provide instruction in several ways (narrative text, screencast, binder exercise), leverage css and liascript options for appearance control, provide redundant modalities (subtitles for audio, alt text for images, etc.). We can also emphasize the importance of choosing open source tools like markdown + liascript and publishing everything on GH, since making all of our material open makes it possible for someone to adapt it down the line, such as translations into other languages or pulling all the text down for a text-to-speech automatic podcast from it, or who knows. And I do like the idea of ending with a call to action section, as we've talked about.

# Incorporating Inclusive Design into Open Education for Data Science

Hi, my name is Rose, and I'm excited for the opportunity to talk with you today about incorporating inclusive design into open education for data science.

---

First, what is meant by inclusive design? Inclusive design refers to the attempt to build your content to be as accessible and inclusive as possible from the beginning, rather than designing your content first and then applying accessibility fixes and adaptations after the fact.

---

In practice, inclusive design means avoiding unnecessary barriers that can be disabling for folks with differences in vision, language, hearing, motor function, attention and executive function, and other aspects of experience. You can think of these as static rules you can apply across the board.
It also means building in as much flexibility as you can, so that folks can choose how they interact with the material to make their experience a better fit for whatever their own needs are.
To be clear, this is a tall order. Prioritizing inclusive design is difficult and time consuming. But it's the right thing to do: historically, data science in general and data science education resources in particular have included a tremendous amount of barriers that have kept interested people from learning about and participating in this community. We want to help correct that, which means we need to allocate time and resources to designing better.
We're really passionate about this, but we're also really new. So our goal today is a little bit to share what we've come up with so far in the hopes that it could help someone else looking to make their materials more inclusive, but also hopefully to learn from you all about what we could do better. So definitely please feel free to chime in during the question time with suggestions for ways we could improve!

---

So what design tools are we using so far?

One important tool for us has been liascript. It's a markdown parser specifically designed for building courses. There are a number of things about it that we love:
It has integrated text-to-speech functionality
There are built-in controls that let learners change things about the appearance, like text size, colors, dark mode, etc. so they can adjust the way it displays to make it more readable for them.
And it makes it easy to use custom CSS, which has been important for us because it lets us tweak some of the liascript defaults to make them even more accessible.
Crucially, it's also a markdown parser, as I mentioned, which means all of our educational materials are written in markdown files. This is a huge advantage in terms of forward compatibility with accessibility tools we haven't thought to deisgn for, or that may not even have been invented yet --- plain text files like markdown are highly portable and work well with a very wide range of software.
On a related note, liascript is open source software, which is important to us both in terms of modeling open science values (practice what we preach!) and in terms of designing for inclusion. Sticking to open source tools means that we can leave the door open for someone else to take our materials and adapt them in ways we haven't thought of. For example, if someone wanted to render liascript courses in Braile, I'm sure it would be a lot of work, but the code is all available for them to build a braile version of the liascript parser.

---

Another important tool has been GitHub. Many of you are probably already familiar with some of the advantages of GitHub in terms of transparency, version control, and smooth collaboration across team members, all of which is great. We've also found some of GitHub's tools work really well to keep us on track with our inclusive design goals.
We have templates and checklists for ourselves to make sure we review every new data science module we create for inclusive design criteria. We've got the checklist saved as a markdown document (obviously), and then for each new module, we create a GH issue and copy-paste in the markdown checklist. This generates an interactive checklist in GH for that module, which we can step through to make sure we're not falling short of our own standards.
This aspect of the design process --- identifying guidelines for ourselves and then setting up a system to make sure we adhere to those guidelines --- has been crucial in terms of providing accountability for ourselves.

---

In order to determine what guidelines we want to hold ourselves to, we've relied on a number of really great existing resources for inclusive design. I don't have time to go through these all with you now, but this is a list of some of our favorites.
I will draw your attention quickly to the first resource on this list, The Inclusive Design Guide published by the Inclusive Design Research Center in Toronto. The reason I want to mention it is because it includes not just best practice guidelines and such, but also a number of activities you can do to help you and your team think more concretely about what inclusive design might look like for your product. We liked the [inclusive design mapping activity](https://guide.inclusivedesign.ca/activities/inclusive-design-mapping/) in particular.
These slides are available on GH, so I hope you'll go back and check out these other resrouces as well.

---

I want to end on an important reality check. While there is definitely a lot we can do to improve inclusive design for data science education materials, there are also some really persistent barriers that are difficult to address. In particular, RStudio and Jupyter notebooks are both extremely popular tools for data science, but neither works with screenreaders and other accessibility software. This is a huge issue for us as a field because if you want to learn about data science but you're limited to materials that don't teach in RStudio and Jupyter notebooks, that removes a lot of the most high quality educational resources. For our team, we had to decide whether to use RStudio and Jupyter, knowing that they have these serious accessibility shortcomings. We ended up deciding to use them, at least for now, because although they can be disabling to people with vision problems, we feel like they're helpful enough for other users that on balance it seems worth it.
Rstudio is working hard on this issue, and we're hopeful they'll have a fix soon. In fact, there is already an experimental version of screenreader support available in RStudio as of version 1.3, it's just not very good yet. (And if you've ever been in the position where you've needed to use software that *almost* works, you know how frustrating that is.) So for now, this is just to bring your awareness to these existing accessibility barriers in the field, and a plea to keep advocating for improvements, both in the things we build and the tools we use.

---

Thank you so much for your attention. Please reach out if you want to get in touch!
