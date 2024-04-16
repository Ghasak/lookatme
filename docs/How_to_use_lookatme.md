# Using Lookatme

Once Lookatme is installed, you can start creating and presenting interactive
Markdown presentations. Below is a guide on how to use Lookatme, including
basic commands and tips for creating effective presentations.

## ChangeLog

- `04/16/2024`: Added details for the current objectives and activities for the
  `lookatme` utility.

## Daily Activites

```sh
lookatme slides.md --debug
```

## Creating a Presentation

1. **Create a Markdown File**:
   Begin by creating a Markdown file that will contain your presentation
   content. You can use any text editor to create this file. Example filename:
   `presentation.md`.

2. **Structure Your Slides**:
   Use Markdown headings to define new slides. Each slide starts with a heading
   (typically `#` or `##`). Below the heading, add the content for that slide
   using standard Markdown syntax.

   ````markdown
   # Slide 1 Title

   Here is some content for slide 1:

   - Bullet point 1
   - Bullet point 2
   - Bullet point 3

   ## Slide 2 Title

   Text for slide 2 can include **bold**, _italics_, and even [links](http://example.com).

   ### Slide 3 Title

   Code can also be included:

   ```python
   def hello_world():
       print("Hello, world!")
   ```
   ````

   ```

   ```

3. **Embed Images**:
   To include images, use standard Markdown image syntax. Ensure that images
   are accessible from the location where you are running Lookatme.

   ```markdown
   ![Alt text](path/to/image.png "Image Title")
   ```

#### Running the Presentation

To run your presentation, use the `lookatme` command followed by the filename
of your Markdown file.

```sh
lookatme presentation.md
```

This command will open the presentation in your terminal.

#### Navigation Commands

While the presentation is running, use the following keyboard commands to navigate between slides:

- **Right Arrow** or **Space**: Move to the next slide.
- **Left Arrow**: Move to the previous slide.
- **Up Arrow**: Scroll up on the current slide (if the content is longer than the terminal window).
- **Down Arrow**: Scroll down on the current slide.
- **Q** or **Esc**: Quit the presentation.

#### Live Reload Feature

Lookatme can automatically reload the presentation when changes are made to the
Markdown file. This is particularly useful during the creation of your slides.
To enable live reload, use the `--live-reload` option.

```sh
lookatme presentation.md --live-reload
```

#### Exporting Slides

If you need to share your presentation or prepare it for a setting where
Lookatme isn't practical, you can convert your slides into a PDF or static
HTML. This requires additional tools like `pandoc` or `Marp`:

```sh
pandoc -s presentation.md -o presentation.pdf
```

This command uses Pandoc to convert the Markdown file into a PDF document.

### Tips for Effective Presentations

- **Keep It Simple**: Use simple language and structure to ensure clarity and
  effectiveness.
- **Visuals**: Incorporate diagrams, code snippets, and images to make slides
  more engaging.
- **Practice**: Run through your slides multiple times to ensure smooth
  delivery during actual presentations.

With Lookatme, you can create dynamic and visually appealing presentations
right in your terminal, leveraging the simplicity of Markdown for content
creation.
