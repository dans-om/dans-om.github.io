# DANS-OM Lab Website

**Data-driven NeuroScience Of Meditation Lab**  
Michigan State University

This is the official website for the DANS-OM Lab, hosted on GitHub Pages.

🌐 **Live Site**: [https://dans-om.github.io](https://dans-om.github.io)

## About

The DANS-OM Lab advances the scientific understanding of meditation through data-driven research, employing computational neuroscience, advanced signal processing, machine learning, and rigorous experimental psychology to study contemplative practices.

## Repository Structure

```
├── _config.yml           # Jekyll configuration
├── _layouts/             # Page templates
├── _includes/            # Reusable components (navigation, etc.)
├── _data/                # Data files (team, publications, news, gallery)
├── assets/               # CSS and JavaScript
│   ├── css/
│   └── js/
├── images/               # Image files
├── pdfs/                 # PDF files (posters, papers)
├── index.md              # Home page
├── news.md               # News & updates page
├── collaborators.md      # Collaborating institutions
├── dunes.md              # DUNES webinar series page
└── outreach.md           # Outreach & community page
```

## Local Development

### Prerequisites
- Ruby (2.7 or higher)
- Jekyll
- Bundler

### Setup
```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# View site at http://localhost:4000
```

## Deployment

This site is automatically deployed via GitHub Pages when changes are pushed to the main branch.

### Configuration
- The site is configured to be served from the root domain: `dans-om.github.io`
- `baseurl` is set to `""` (empty) in `_config.yml`
- `url` is set to `"https://dans-om.github.io"`

## Updating Content

### Team Members
Edit `_data/team.yml` to add/update team members.

### Publications
Edit `_data/publications.yml` to add new publications or conference presentations.

### News
Edit `_data/news.yml` to add news items.

### Gallery
Edit `_data/gallery.yml` to add images to the gallery.

## Contact

For questions about the website or lab:
- **Email**: ravisha3@msu.edu
- **Lab Director**: Dr. Saiprasad Ravishankar
- **Department**: Computational Mathematics, Science and Engineering, Michigan State University

## License

© 2026 DANS-OM Lab, Michigan State University
