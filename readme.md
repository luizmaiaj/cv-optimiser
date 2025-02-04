# AI-Powered CV Optimizer

This repository provides a LaTeX CV template and an AI-powered system to optimize your CV based on job descriptions. The system uses Claude Desktop with Multi-Context Protocol (MCP) to analyze job descriptions, suggest improvements, and generate tailored CVs.

Only tested on macOS.

## Features

- 📄 Professional LaTeX CV template
- 🤖 AI-powered CV optimization
- 📊 Job description analysis
- 🎯 Keyword matching and optimization
- 📝 Automated cover letter generation
- 📌 Application tracking system (ATS) compatibility
- 🔄 Version control for different applications
- 📂 Automated application tracking and history
- 🎨 Job-specific CV templating system
- 📈 Skills match percentage calculation
- 💼 Company research integration
- 📋 Structured application organization

## Prerequisites

### LaTeX Environment
- TeXLive distribution (full installation recommended)
- XeLaTeX compiler
- Required LaTeX packages:
  - article (document class)
  - geometry
  - hyperref
  - multicol
  - color
  - xcolor
  - graphicx
  - fontspec
  - url
  - tooltip

### Claude Desktop
- Claude Desktop app with MCP capabilities
- Access to file operations tools
- Access to web search tools

## Project Structure

```
.
├── LaTex/                  # LaTeX template files
│   ├── build.sh           # Build script for compiling LaTeX
│   ├── cv.tex             # Main CV template
│   ├── style.sty          # LaTeX style definitions
│   ├── summary.tex        # Professional summary
│   ├── experience.tex     # Work experience
│   ├── projects.tex       # Project portfolio
│   ├── skills.tex         # Detailed skills
│   ├── skills-short.tex   # Condensed skills
│   └── education.tex      # Education and certifications
├── prompt.md              # AI assistant instructions
└── readme.md              # Project documentation

Generated Application Structure:
/Users/USERNAME/CV/
├── applications/
│   └── YYYY-MM-DD/
│       └── COMPANY_NAME/
│           └── POSITION/
│               ├── LaTeX/            # Job-specific CV files
│               ├── build/            # Compiled outputs
│               ├── *-JD.md          # Job description
│               ├── *-CL.md          # Cover letter
│               └── applications.json # Application tracking
```

## Important Notes

⚠️ Before using this template, you must update the Font Awesome path in `style.sty`. Look for the following section and update the path to match your Font Awesome installation:
```latex
\newfontfamily{\fa}{Font Awesome 6 Free}[
    Path = /path/to/fonts/,  % Update this path
    Extension = .otf,
    UprightFont = *-Solid-900
]
```

## Installation

1. Install TeXLive distribution:
   ```bash
   # Ubuntu/Debian
   sudo apt-get install texlive-full

   # macOS (using Homebrew)
   brew install --cask mactex

   # Windows
   # Download and install from https://tug.org/texlive/
   ```

2. Clone this repository:
   ```bash
   git clone https://github.com/luizmaiaj/cv-optimiser.git
   cd cv-optimiser
   ```

3. Make the build script executable:
   ```bash
   chmod +x build.sh
   ```

## Usage

1. Prepare Your Base CV:
   - Edit the relevant .tex files in the LaTeX directory
   - Customize your personal information in cv.tex
   - Compile to test the base template:
     ```bash
     cd LaTeX && ./build.sh
     ```

2. For Job Applications:
   - The system will create an application directory structure:
     `/Users/USERNAME/CV/applications/YYYY-MM-DD/COMPANY_NAME/POSITION/`
   - Save the job description as `YYYY-MM-DD-COMPANY_NAME-POSITION-JD.md`
   - The system will:
     - Analyze the job description
     - Research the company
     - Calculate skills match percentage
     - Generate a tailored CV
     - Create a targeted cover letter
     - Track the application in applications.json

3. AI-Powered Optimization:
   - Use Claude Desktop with MCP
   - The AI will:
     - Analyze company background and culture
     - Identify key requirements and skills
     - Optimize keyword placement
     - Ensure ATS compatibility
     - Generate a compelling cover letter
     - Provide application insights and recommendations

## CV Template Features

- Clean and professional design
- ATS-friendly structure
- Modular sections for easy customization
- Short and detailed skills versions
- Hyperlinked content
- Multi-column layout where appropriate
- Unicode support through XeLaTeX
- Automated version control for different applications
- Application tracking and history

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- LaTeX Project for the document preparation system
- Anthropic for Claude AI assistance
- Contributors to the TeXLive distribution

## Disclaimer

This software is provided "as is", without warranty of any kind. Use at your own risk.