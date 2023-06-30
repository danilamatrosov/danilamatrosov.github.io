[Luong Hieu Thi's blog](https://www.hieuthi.com/blog/)

[about](http://www.hieuthi.com)

# How I take notes with Joplin

Jan 2, 2023

As several disruptive global events happened in the last couple of years, I decided to take digital notes more actively. After one year of taking notes, I start to believe that note-taking is one of those life-changing activities you can do immediately and at zero cost (exercise is another one). I keep all my notes in Joplin, an open-source multi-platform note-taking application, and have developed several plugins to cater to my specific use cases.

## tl;dr

I started taking digital notes with [Joplin](https://joplinapp.org/) about a year ago. Joplin supports multimedia notes out-of-the-box and has a plugin system to extend its functionality further. Besides regular notes, I use Joplin to learn Japanese and online courses, manage medium and long-term projects, habit tracking, and as a Personal Knowledge Management (PKM) system. Along the way, I have developed and published several plugins to improve the overall experience: [Rubi and Furigana](https://github.com/hieuthi/joplin-plugin-rubi-and-furigana), [Quick Goto](https://github.com/hieuthi/joplin-plugin-quick-goto), [Copy Anchor Link](https://github.com/hieuthi/joplin-plugin-copy-anchor-link), [Containers with Classes](https://github.com/hieuthi/joplin-plugin-container-with-classes), [Markdown Table: Colorize](https://github.com/hieuthi/joplin-plugin-markdown-table-colorize), [Markdown Table: Sortable](https://github.com/hieuthi/joplin-plugin-markdown-table-sortable), [Metis](https://github.com/hieuthi/joplin-plugin-metis), [Slash Commands](https://github.com/hieuthi/joplin-plugin-slash-commands), [Life Calendar](https://github.com/hieuthi/joplin-plugin-life-calendar), and [Function Plot](https://github.com/hieuthi/joplin-plugin-function-plot).

## Learn Japanese with Digital Notes

<img width="740" height="175" src=":/ab621fb7c01f4746ae5d85f07bed3b85"/>

Joplin uses Markdown which supports HTML tags like &lt;ruby&gt;

I tried to learn Japanese for the past five years with pen and paper, which I believed would help with writing and retaining Kanji, but achieved little success. Writing Japanese is too time-consuming when you haven’t mastered it yet. Since the pandemic began, I decided to return to it with a more pragmatic approach: typing with digital notes and focusing on reading, listening, and speaking. This is when I started hunting for a note-taking app that supports furigana. Since I have web development experience and know HTML5 has excellent support for the ruby tag, I looked for a web-based app or something of that nature and came across Joplin. Is is surprising that Chromium-based applications are the best method to render furigana that I have found still this day, as most word processing applications don’t even support it. Using HTML tags within text does not look pleasant. Still, it is straightforward, reliable and it has significantly improved my learning. To make it more convenient, I developed the [Rubi and Furigana Plugin](https://github.com/hieuthi/joplin-plugin-rubi-and-furigana) to help turning brackets into tags. It is also my very first published Joplin plugin.

## Course Notes and Math Notations

<img width="740" height="183" src=":/8c328280d9214bfbb82d612c6d9024d9"/>

Joplin supports KaTeX and you can render functions with function-plot plugin

Besides Japanese, I regularly take one or two Massive Open Online Courses (MOOC) simultaneously. Most of them are technical courses with symbols, formulas, and figures. The two main problems I had with course notes were they felt isolated from the rest of my knowledge, and it was tricky to type math notations on a computer. Since Joplin supports KaTeX, writing equations is not as much of a problem, and I can integrate course notes with the rest of my knowledge. KaTeX is not so simple by itself, but it is much better than using immutable images for equations. Plotting functions is another feature that I want as I often try to plot a simple function but failed to find a free and simple solution that do not require writing codes. I published [Function Plot Plugin](https://github.com/hieuthi/joplin-plugin-function-plot), based on [Function Plot](https://github.com/mauriciopoppe/function-plot) library of Mauricio Poppe, for this exact purpose. Now you have a free and interactive plotting feature within Joplin, which may cost a couple of dollars per month if you use some other services.

## Linking and Navigation

<img width="740" height="175" src=":/e3ab764fcc11400b8eb9ebd13d79172f"/>

Joplin supports linking between notes like a website

One of the important features of Markdown-based note-taking apps is the ability to add hyperlinks between notes, which makes them essentially a webpage. It is what I always want, and it sparks my interest in this new note-taking paradigm. [Obsidian](https://obsidian.md/), a proprietary software, is better than Joplin in this aspect as it makes links the centre of its philosophy. Several plugins attempted to recreate a similar linking experience for Joplin, but they were not well-optimized, so I haven’t incorporated them into my workflow. With Joplin, you have to add links with intention instead of as a happy accident. I used [Quick Links Plugin](https://github.com/roman-r-m/joplin-plugin-quick-links), developed by Roman Musin, to make adding links easier and developed [Copy Anchor Link Plugin](https://github.com/hieuthi/joplin-plugin-copy-anchor-link) to make linking to a specific heading becomes more accessible.

Another reason to build a PKM is that the Internet, specifically the Search Engine, has become increasingly unreliable. Due to my work, I regularly search for the same information repeatedly. It never cross my mind that I should retain the information. But for the last couple of years, I noticed it took longer to search and the results are irrelevant. It takes time to develop a PKM, but then you will have access to a personal, offline, and instantaneous search engine. I use `Goto Anything...` feature (Shortcut: `Ctrl+P`) to search and jump to notes. This way, all my notes will contribute to the knowledge base, even the most obscure and dated ones. I also use links to create a navigation system between relevant notes manually.

As Joplin does not support a split view, it is tricky when you have to work with several notes at the same time. I published [Quick Goto Plugin](https://github.com/hieuthi/joplin-plugin-quick-goto), which helps assign a note to one of the keyboard shortcut slots. It sets the anchor point to the nearest heading, so you can use it to jump between two or three notes. I also use [Embeded Search Plugin](https://github.com/ambrt/joplin-plugin-embed-search), developed by ambrt, to create a Home Note that searches and presents several relevant notes like favorites, ongoing course notes, etc. I assign it to a shortcut slot of Quick Goto Plugin permanently so I can jump back to it quickly.

## Use Tables for Simple Data Processing

<img width="740" height="137" src=":/bf5d4e023baa4a98a98c0727d7b8f8bd"/>

Use Markdown Table: Colorize and Sortable plugins to make tables more useful and appealing

Tables supported by markdown might seem clunky and unintuitive, but with some tweaks, they can be valuable and essential to your notes. I published two plugins to enhance the experiences with tables: [Markdown Table: Colorize](https://github.com/hieuthi/joplin-plugin-markdown-table-colorize) which paints different columns with different colors and [Markdown Table: Sortable](https://github.com/hieuthi/joplin-plugin-markdown-table-sortable) which add the ability to sort the content of the table. Combining these two allows you to add meaningful interactable data content among your text notes. It has greatly reduced the number of times I had to open a spreadsheet software just to sort a small table quickly.

## Type Everything Out

<img width="740" height="125" src=":/1998e186058f45f98729b8d469c95c5e"/>

Slash Commands plugin helps typing unusual characters and datetime formats

It is common to want to create a perfect note, but the thing about perfect is that you end up wanting to put it into a glass frame instead of using it. As our thoughts are usually random and spontaneous, it is difficult to put them into an established note. And so, we may dismiss these ideas entirely to maintain the perceived perfection. To deal with this dilemma, I added a “Logging” section for notes that I had this experience. The logging section will keep the rest of the notes well-organized. At the same time, it allows me to immediately put any relevant and spontaneous thoughts down and organize them later. Accompanying these thoughts with a timestamp, similar to logging in software, creates a mental snapshot that helps remind the context when you have that idea. I also use this approach to keep a tab of recurrent tasks such as backup data. The act of manually typing out the action, instead of automatically, solidates the memory about it. I published [Slash Commands Plugin](https://github.com/hieuthi/joplin-plugin-slash-commands) to help type these timestamps in the format of your preferences as well as to type unusual or recurrent string text.

## Every Note is a Project

<img width="740" height="142" src=":/c26a0e1e00704cc89040d12ca3f15953"/>

Metis plugin provides a simple no-frills Task Management System

… or potentially be. For me, there is no points in keeping a PKM just for the sake of storing knowledge. Each note should mean something to you, not necessarily immediately but at least someday in the future. From this perspective, each note is essentially a medium or long-term project. A book is a project as you want to read it, research about it, or publish your review. A country can also be a project. You just have basic information about it now, but you may want to visit it in the future, or learn about its history when the opportunity arises. In those cases, keeping a list of actionable tasks is essential. By writing them down, your objectives are no longer a vague idea or a wishful thinking but something real and achievable. I published [Metis Plugin](https://github.com/hieuthi/joplin-plugin-metis), which provided a task management system based on [Todo.txt Specifications](http://todotxt.org/). It has more features than a task list but is simple enough to blend into the note’s contents. You can use [Slash Commands Plugin](https://github.com/hieuthi/joplin-plugin-slash-commands) to help with typing todo.txt format.

## Habit Tracking and Project Management

<img width="740" height="170" src=":/53d0f763206d43968afb8a839e5c622c"/>

Life Calendar as a unique tool for Retrospection, Management, and Planning.

Most calendar applications focus on catching up with coming events rather than for retrospective purposes. As it is easy to lose sight of what’s important when you have to keep up with immediate emergencies, it is vital to have a method to look at the grand scheme of things. Intrigued by [Your Life in Weeks](https://waitbutwhy.com/2014/05/life-weeks.html) article by Tim Urban, I developed the [Life Calendar Plugin](https://github.com/hieuthi/joplin-plugin-life-calendar), which presents the calendar as a seamless stream of days, weeks, months, or years. The ability to quickly quantify the amount of time that have passed and the amount of time you have left is a reassuring but terrifying experience. I use the Life Calendar Plugin to keep track of habits like exercises, keep up and plan for self-study courses, and document significant events in life. It’s also an excellent tool for managing and planning medium and long-term projects.

## No Note-taking “System”

Since taking digital notes more seriously, I have been exposed to many fascinating ideas and concepts about note-taking, knowledge management, and productivity. As you may have noticed from previous sections, some of which have greatly influenced my current setup. The biggest one is [Getting Things Done](https://en.wikipedia.org/wiki/Getting_Things_Done) or GTD method. While I do not subscribe to the system as a whole, I found the “put everything that matter into a trusted system” idea to be a life-changing lesson. I have a lot less anxiety and fewer “I think I forgot something important” moments since I started practicing it. [Evergreen notes](https://notes.andymatuschak.org/Evergreen_notes) is another concept that has grown on me with the idea that you should develop each note with you over time. It’s a common mistake to want to create a perfect note right at the start but then never look into them ever again. Typing your thoughts with a timestamp helps develop a sense of progress but does not require much effort. Even though [Zettelkasten](https://en.wikipedia.org/wiki/Zettelkasten) is interesting and relevant to my work, I have yet to find an effective way to incorporate it into my system.

It’s tempting to just follow the best practice created by someone else. However, to develop a habit that would stick, you should start from what you familiar with and expand it to the direction that makes sense to you personally. If you want to start taking digital notes, the best way to start is just doing it instead of looking for the perfect system.

## Conclusion

It has been a couple of difficult years for everyone, as is for me. Taking notes has been the main thing that helped me to keep up and move forward in these uncertain times. However, I believe note-taking can also help with taking the initiative and making things happen, which is one aspect I would like to improve this year. If you feel overwhelmed or anxious about your current situation, start typing down the crucial things in your life into a trusted system, while may not solve all your problems, does help create a clearer picture of it.

If you’re intrigued by the idea of note-taking but do not want to use Joplin, I would recommend the following softwares as alternatives. They are neither open-source nor entirely free but share the same Markdown paradigm as Joplin. Note-taking is too important to be locked in any particular software.

- [Obsidian](https://obsidian.md/) has a big community and a free option, but syncing is not easy without paid
- [Inkdrop](https://www.inkdrop.app/) is a beautiful note-taking app but it is not free or open-source. It has a smaller community.

- Copyright © 2017-2023 **hieuthi.com**

- [hieuthi](https://github.com/hieuthi)

From software engineering to computer science
