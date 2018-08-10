# Safari Highlights to Markdown

This is what I use to reformat my [O'Reilly Safari](https://www.safaribooksonline.com/home/) book highlights into Markdown for local reference.

## Method

1. Download your Safari hightlights and notes
2. Copy the name of the book title you want to extract highlights and notes for
3. Install Perl dependencies (you may need to install [cpanminus](https://metacpan.org/pod/App::cpanminus) and [Carton](https://metacpan.org/pod/Carton)):

```sh
$ carton install
```

4. Copy this script somewhere you can run it (e.g., `/usr/local/bin`) and set permissions (e.g., `chmod 0755 /usr/local/bin/highlights-to-md`)
5. Run this script:

```sh
$ highlights-to-md ~/path/to/highlights.csv "The Book Title" > the-book-title.md
```

## Example

```sh
$ highlights-to-md ~/Downloads/safari-annotations-export.csv "The Phoenix Project" > the-phoenix-project.md
```

## Results

```markdown
## Chapter 1

[[Link](https://www.safaribooksonline.com/a/the-phoenix-project/17601257/)]:

> CIO stands for “Career Is Over.” And VPs of IT Operations don’t last much longer.

[[Link](https://www.safaribooksonline.com/a/the-phoenix-project/17601212/)]:

> When she hangs up, I try to think of what good news would even look like these days. When I can’t, I turn the radio back on and immediately hear a commercial from our largest retailing competitor. They’re talking about their unparalleled customer service and a breathtaking new offering that allows people to customize their cars with their friends online.
>                       The ad is brilliant. I’d use the service in a second, if I weren’t such a loyal company man. How do they keep bringing such incredible new capabilities to market while we remain stuck in the mud?

## Chapter 2

[[Link](https://www.safaribooksonline.com/a/the-phoenix-project/17601617/)]:

> She has an uncanny knack for blaming other people for her screwups, especially IT people. For years, she’s been able to escape any sort of real accountability.

[[Link](https://www.safaribooksonline.com/a/the-phoenix-project/17601592/)]:

> “So now we’re supposed to take orders from you? Look, no offense, pal, but aren’t you a little out of your league? You’ve managed the midrange systems, which are basically antiques, for years. You created a nice little cushy job for yourself up there. And you know what? You have absolutely no idea how to run modern distributed systems—to you, the 1990s is still the future!
...
```

## Terms

Please fork and modify this script as you like. If you have a generally useful improvement, consider making a pull request and I'll consider merging it.
