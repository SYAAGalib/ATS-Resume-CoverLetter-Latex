# ATS-Friendly Resume & Cover Letter LaTeX Templates

A comprehensive collection of professional LaTeX templates for creating ATS (Applicant Tracking System) optimized resumes, cover letters, and job application documents. This repository provides multiple template styles to help you create polished, professional documents that pass through automated screening systems.

## 📋 Table of Contents

- [Features](#-features)
- [Templates Included](#-templates-included)
- [Prerequisites](#-prerequisites)
- [Quick Start](#-quick-start)
- [Template Structure](#-template-structure)
- [Customization Guide](#-customization-guide)
- [Compilation](#-compilation)
- [Examples](#-examples)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

- **ATS-Optimized**: Templates designed to be parsed correctly by Applicant Tracking Systems
- **Multiple Styles**: Choose from various professional designs (OtterCV, Job Application Letter, etc.)
- **Bilingual Support**: Templates support multiple languages (English, German, Spanish)
- **Modular Design**: Separate files for different sections (profile, experience, cover letter, motivation letter)
- **Professional Formatting**: Clean, modern layouts that impress both humans and machines
- **Easy Customization**: Simple commands to update personal information and content
- **PDF Generation**: Generate high-quality PDF documents ready for submission

## 📦 Templates Included

### 1. **OtterCV** (`otterCV/`)
A feature-rich CV template with multiple style options:
- Three design variants: `basic`, `fancy`, and `massive`
- Integrated cover letter and motivation letter
- Support for attachments and signatures
- Profile picture support
- Bilingual content support

### 2. **Job Application Letter** (`Job_Application_letter/`)
Professional job application letter template with:
- Clean, formal design
- Modular structure with separate style and content files
- Easy-to-customize personal and company information
- Signature support (image or line)
- Attachment listing

### 3. **Job Application Cover Letter** (`Job_Application_Cover_Letter/`)
Alternative cover letter template for job applications

### 4. **Carta de Motivación** (`Carta_de_motivación_presentación_/`)
Spanish language motivation letter template

## 🔧 Prerequisites

To compile these LaTeX templates, you need:

- **LaTeX Distribution**:
  - **Linux**: TeX Live (`sudo apt-get install texlive-full`)
  - **macOS**: MacTeX (`brew install --cask mactex`)
  - **Windows**: MiKTeX or TeX Live

- **Required LaTeX Packages**:
  - `fontenc`, `inputenc`
  - `hyperref`
  - `fontawesome5`
  - `tikz`
  - `xcolor`
  - `geometry`
  - `pdfpages`
  - `fancyhdr`
  - And more (most are included in full LaTeX distributions)

## 🚀 Quick Start

### Option 1: Using OtterCV Template

1. **Clone the repository**:
   ```bash
   git clone https://github.com/SYAAGalib/ATS-Resume-CoverLetter-Latex.git
   cd ATS-Resume-CoverLetter-Latex/otterCV
   ```

2. **Edit your personal information** in `main.tex`:
   ```latex
   \name{Your First Name}{Your Last Name}
   \email{your.email@example.com}
   \phone{CountryCode}{YourPhoneNumber}
   ```

3. **Customize your content**:
   - Edit `cv/profile.tex` for your CV content
   - Edit `letters/cover.tex` for your cover letter
   - Edit `letters/motivation.tex` for your motivation letter

4. **Compile**:
   ```bash
   pdflatex main.tex
   ```

### Option 2: Using Job Application Letter Template

1. **Navigate to the template**:
   ```bash
   cd Job_Application_letter
   ```

2. **Edit `main.tex`** with your information:
   ```latex
   \author{Your Name}
   \ProvideAdress{Your Street}{Your City}{I}
   \ProvideEmail{your.email@example.com}
   \ProvideName{Company Name}{I}
   ```

3. **Edit the letter content** in `Txt/Application-letter.tex`

4. **Compile**:
   ```bash
   pdflatex main.tex
   ```

## 📁 Template Structure

### OtterCV Structure
```
otterCV/
├── main.tex              # Main document file
├── ottercv.cls          # Document class definition
├── cv/
│   ├── bilangual.tex    # Bilingual CV content
│   └── profile.tex      # Profile section
├── letters/
│   ├── cover.tex        # Cover letter
│   └── motivation.tex   # Motivation letter
├── static/              # Images, signatures, photos
└── attachments/         # Additional documents to include
```

### Job Application Letter Structure
```
Job_Application_letter/
├── main.tex             # Main document
├── Code/
│   ├── Application.sty  # Custom style definitions
│   └── Preamble.tex     # Document preamble
├── Txt/
│   └── Application-letter.tex  # Letter content
└── Img/                 # Images and signatures
```

## 🎨 Customization Guide

### Changing Colors (OtterCV)

Edit colors in `ottercv.cls`:
```latex
\definecolor{orange}{rgb}{1,0.5,0}
\definecolor{blue}{rgb}{0.14, 0.27, 0.52}
\definecolor{purple}{rgb}{0.6,0.1,0.4}
```

### Adding Profile Picture

In `main.tex`:
```latex
\pathtopicture[size=40mm]{static/your-photo.jpg}
```

### Adding Signature

```latex
\pathtosignature[xshift=3mm, yshift=-5mm]{static/your-signature.png}
```

### Choosing OtterCV Style

Change the document class option in `main.tex`:
```latex
\documentclass[fancy]{ottercv}  % Options: basic, fancy, massive
```

## 🔨 Compilation

### Command Line Compilation

```bash
# Basic compilation
pdflatex main.tex

# Full compilation (for bibliography and references)
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### Using LaTeX IDE

- **Overleaf**: Upload the template folder and compile online
- **TeXstudio**: Open `main.tex` and press F5
- **VS Code**: Use LaTeX Workshop extension

### Makefile (if available)

```bash
make           # Compile the document
make clean     # Remove auxiliary files
```

## 📸 Examples

The repository includes several example PDFs:
- `SYAAGalib-Software_Engineer_Resume_ATS_Latex.pdf`
- `Software_Engineer_Resume_SYAAGalib.pdf`
- `Deedy_Resume_Reversed__1_.pdf`

These demonstrate the final output of the templates.

## 🤝 Contributing

Contributions are welcome! If you have improvements or new templates:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-template`)
3. Commit your changes (`git commit -am 'Add new template'`)
4. Push to the branch (`git push origin feature/new-template`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**SK. Yeasin Ahsanullah Al-Galib**
- GitHub: [@SYAAGalib](https://github.com/SYAAGalib)
- Email: syaagalib@nubtkhulna.ac.bd

## 🙏 Acknowledgments

- OtterCV template structure and design
- LaTeX community for excellent packages and documentation
- Contributors who help improve these templates

## 📚 Additional Resources

- [LaTeX Documentation](https://www.latex-project.org/help/documentation/)
- [Overleaf LaTeX Tutorials](https://www.overleaf.com/learn)
- [ATS-Friendly Resume Tips](https://www.jobscan.co/blog/ats-resume/)

---

**Note**: Remember to remove any personal information before sharing your resume publicly, and always tailor your resume and cover letter to the specific job you're applying for.

⭐ If you find these templates helpful, please consider giving this repository a star!