# Project Context: Babacar GUEYE's Resume Website

## Project Overview
This project is a personal resume and portfolio website for Babacar GUEYE. It is a static site built using **Jekyll**, a Ruby-based static site generator. The site structure follows the "Jekyll Professional Resume" template, designed to showcase professional experience, education, skills, and projects in a clean, modern format.

## Key Technologies
*   **Jekyll:** Static site generator.
*   **Ruby:** The underlying language for Jekyll.
*   **Liquid:** Templating language used in HTML files.
*   **Sass/SCSS:** Used for styling (`assets/css/style.scss`).
*   **YAML:** Used for configuration (`_config.yml`) and data storage (`_data/*.yml`).

## Building and Running
To develop and preview the site locally, follow these steps:

### Prerequisites
*   Ruby (version 2.5.0 or higher)
*   Bundler (`gem install bundler`)

### Installation
Install the project dependencies defined in the `Gemfile`:
```bash
bundle install
```

### Local Development
Start the local Jekyll server to preview the site. This command will watch for file changes and regenerate the site automatically.
```bash
bundle exec jekyll serve
```
Access the site at: `http://localhost:4000/`

## Project Structure & Content Management

### Configuration
*   **`_config.yml`**: The main configuration file. It contains site-wide settings such as the site title, base URL, and personal profile information (Name, Job Title, Contact Info, Social Links).

### Resume Content (`_data/`)
The content of the resume is data-driven and stored in YAML files within the `_data/` directory. To update specific sections, edit the corresponding file:
*   **`_data/Certifications.yml`**: List of certifications.
*   **`_data/Education.yml`**: Academic background.
*   **`_data/Experience.yml`**: Professional work history.
*   **`_data/Languages.yml`**: Spoken languages and proficiency.
*   **`_data/Skills.yml`**: Technical and soft skills.
*   **`_data/Projects.yml`** (in `unused data/`): Project portfolio.
*   **`_data/Awards.yml`** (in `unused data/`): Awards and honors.
*   **`_data/Publications.yml`** (in `unused data/`): Publications.

**Data Format:**
Each YAML file generally follows this structure:
```yaml
subject: Section Title
listing-order: Number (determines order on page)
icon: Path to icon (e.g., /assets/img/icon.svg)
contents:
  - title: Item Title
    description:
      - Detail 1
      - Detail 2
    # Other specific fields like date, grade, etc.
```

### Visual Assets (`assets/`)
*   **`assets/img/`**: Stores images, including the profile picture (`profile.webp`, `profile original.webp`) and icons.
*   **`assets/css/style.scss`**: The main stylesheet. You can customize the color palette and other styles here.
*   **`assets/js/main.js`**: JavaScript file for site interactivity.

### Layouts (`_layouts/`)
*   **`_layouts/home.html`**: The primary layout file that structures the main page. It likely loops through the data collections to render the resume sections.

## Common Tasks

### Updating Profile Information
Edit `_config.yml` to change:
*   Name (`name`)
*   Job Title (`job`)
*   Contact details (`phone_number`, `email`, `address`)
*   Social media links (`linkedin_username`, `github_username`, etc.)
*   Profile image path (`profile_img`)

### Adding/Editing Experience
1.  Open `_data/Experience.yml`.
2.  Add a new entry under `contents` or modify an existing one.
3.  Ensure indentation matches the YAML format.

### Changing the Color Scheme
Open `assets/css/style.scss` and modify the CSS variables (e.g., `--theme1-light`, `--theme1-dark`) defined in the `:root` block.
