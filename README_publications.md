# ASP-LAB Publications Page Guide

This is a simple guide for maintaining and updating the publications.html page for the ASP-LAB website.

## How to Add a New Publication

### Step 1: Add a New Publication Entry

Copy and paste one of the existing publication entries and modify it with the new publication's information. The format is:

```html
<div class="publication-item">
    <p><span class="pub-number">X.</span> <strong>[Publication Type]</strong> Authors, "Title," <span class="journal">Journal/Conference Name</span>, vol. XX, no. YY, pp. ZZZ-ZZZ, Month Year. <a href="https://doi.org/XXXX" class="pub-link">View Publication</a></p>
</div>
```

Where:
- Replace `X` with the sequential number for that year
- Replace `[Publication Type]` with either `[Journal]` or `[Conference]`
- Add the author names, title, and publication details
- Include a link to the publication if available (otherwise remove the `<a>` tag)

### Step 2: Adding a New Year Section

If you need to add a new year section that doesn't exist yet:

1. Add the new section in chronological order (newest year at the top)
2. Add the year to the navigation sidebar
3. Use this template:

```html
<section id="YYYY">
    <div class="page-header">
        <h2>YYYY</h2>
    </div>
    <div class="publication-list">
        <!-- Publication items go here -->
    </div>
</section>
<hr>
```

Where `YYYY` is the new year.

4. Don't forget to also add the new year to the sidebar navigation:

```html
<li><a href="#YYYY">YYYY</a></li>
```

## Publication Entry Format

### Journal Articles

```html
<div class="publication-item">
    <p><span class="pub-number">X.</span> <strong>[Journal]</strong> Author1, Author2, and Author3, "Title of the article," <span class="journal">Journal Name</span>, vol. XX, no. YY, pp. ZZZ-ZZZ, Month Year. <a href="https://doi.org/XXXX" class="pub-link">View Publication</a></p>
</div>
```

### Conference Papers

```html
<div class="publication-item">
    <p><span class="pub-number">X.</span> <strong>[Conference]</strong> Author1, Author2, and Author3, "Title of the paper," in <span class="conference">Proc. Conference Name</span>, Month Day-Day, Year, Location, pp. ZZZ-ZZZ.</p>
</div>
```

### In-Preparation Papers

```html
<div class="publication-item">
    <p><strong>[Journal/Conference - In Preparation]</strong> Author1, Author2, and Author3, "Title of the paper," <span class="journal">Journal Name</span>, vol. XX, pp. xxx-xx, Year (in preparation).</p>
</div>
```

## Important Notes

1. Always maintain the chronological order (newest first)
2. Update the numbering of publications within each year section
3. Make sure to use consistent formatting for all entries
4. For DOI links, use the format: `https://doi.org/XXXX` where XXXX is the DOI
5. Use the proper CSS classes to maintain styling:
   - `journal` or `conference` for publication names
   - `pub-link` for links to publications
   - `pub-number` for the sequence number

## CSS Classes

The publications page uses these CSS classes:
- `.publication-list` - Container for all publications in a year
- `.publication-item` - Individual publication entry
- `.pub-number` - Sequential number of the publication
- `.journal` or `.conference` - Name of the publication venue
- `.pub-link` - Link to view the publication

## Example of Adding a New Publication

To add a new journal publication to 2025:

1. First, create the 2025 section if it doesn't exist
2. Add your publication entry
3. Add 2025 to the sidebar navigation

```html
<!-- Add to sidebar navigation -->
<li><a href="#2025">2025</a></li>

<!-- Add the new section before the 2024 section -->
<section id="2025">
    <div class="page-header">
        <h2>2025</h2>
    </div>
    <div class="publication-list">
        <div class="publication-item">
            <p><span class="pub-number">1.</span> <strong>[Journal]</strong> A. Author and M. T. Akhtar, "Title of the new paper," <span class="journal">Journal Name</span>, vol. XX, no. YY, pp. ZZZ-ZZZ, Month 2025. <a href="https://doi.org/XXXX" class="pub-link">View Publication</a></p>
        </div>
    </div>
</section>
<hr>
