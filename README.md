[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Welcome to the **Beamer Presentation Template**, a comprehensive and highly customizable LaTeX template designed to help you create professional, visually appealing presentations effortlessly. This template is ideal for academic lectures, research presentations, business meetings, and more.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Selecting Themes and Color Schemes](#selecting-themes-and-color-schemes)
  - [Customizing Header and Footer](#customizing-header-and-footer)
  - [Adding Content](#adding-content)
    - [Defining Sections with Short and Long Names](#defining-sections-with-short-and-long-names)
    - [Creating Frames](#creating-frames)
  - [Aspect Ratio and Handout Options](#aspect-ratio-and-handout-options)
- [Customization](#customization)
  - [Defining Custom Colors](#defining-custom-colors)
  - [Adding New Color Schemes](#adding-new-color-schemes)
  - [Modifying Fonts](#modifying-fonts)
- [Advanced Features](#advanced-features)
  - [Mathematical Equations](#mathematical-equations)
  - [Code Listings](#code-listings)
  - [Inserting Images and Tables](#inserting-images-and-tables)
  - [Section Title Slides](#section-title-slides)
  - [Custom Commands](#custom-commands)
- [Packages and Libraries](#packages-and-libraries)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
  - [Contribution Guidelines](#contribution-guidelines)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

---

## Overview

This Beamer template provides a solid foundation with a plethora of customization options to suit your presentation needs. It includes multiple themes, color schemes, font options, and additional features that enhance the overall look and functionality of your slides.

### Repository Information

- **Repository Name:** beamer-template
- **Repository URL:** [https://github.com/AmirrezaFarnamTaheri/beamer-template.git](https://github.com/AmirrezaFarnamTaheri/beamer-template.git)
- **Hosting Platform:** GitHub

---

## Key Features

- **Customizable Themes**
  - **Outer Themes:** `shadow`, `smoothbars`, `split`, `sidebar`, `tree`, `miniframes`, `default`
  - **Inner Themes:** `rounded`, `rectangles`, `inmargin`, `circles`
- **Extensive Color Schemes**
  - 12 predefined color schemes with artistic choices
  - Ability to define custom color schemes
- **Flexible Layouts**
  - Support for different aspect ratios (e.g., 4:3, 16:9 widescreen)
  - Handout version without overlays
  - Navigation styles with or without mini frames
- **Enhanced Functionality**
  - Integrated packages for mathematics (`amsmath`, `amssymb`, `mathtools`)
  - Graphics and drawing support (`graphicx`, `tikz`)
  - Code listings with syntax highlighting (`listings`)
  - Table enhancements (`booktabs`, `multirow`, `array`)
- **Custom Header/Footer**
  - Options to include or exclude headers and footers
  - Customizable content in headers and footers
- **Section Title Slides**
  - Automatic creation of section title slides
  - Customizable backgrounds: default, image, or color
- **Reusable Commands**
  - Commands for highlighting text, custom boxes, alerts, and more
- **Appendix Support**
  - Seamless addition of appendix sections with proper numbering
- **Font Customization**
  - Options for professional fonts, serif, sans-serif, and more
  - Advanced font settings using `fontspec` (with `xelatex` or `lualatex`)
- **Custom Bullets and Logos**
  - Ability to include custom bullet points and logos on each slide
- **Frame Title Alignment**
  - Options to align frame titles to left, right, or center
- **Support for Short and Long Section Names**
  - Define short and long formats for section names to control display in navigation and content

---

## Prerequisites

To use this Beamer template effectively, ensure you have the following installed:

- **LaTeX Distribution**: [TeX Live](https://www.tug.org/texlive/), [MiKTeX](https://miktex.org/), or [MacTeX](https://www.tug.org/mactex/)
- **Compiler**: `pdflatex` (basic usage), `xelatex`, or `lualatex` (for advanced font customization)
- **Text Editor**: Any LaTeX-compatible editor such as [Overleaf](https://www.overleaf.com/), [TeXstudio](https://www.texstudio.org/), [Visual Studio Code](https://code.visualstudio.com/) with LaTeX extensions, etc.

---

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/AmirrezaFarnamTaheri/beamer-template.git
   ```

2. **Navigate to the Template Directory**

   ```bash
   cd beamer-template
   ```

3. **Organize Assets**

   - Place all your images in the `images/` directory.
   - Ensure that the `references.bib` file is updated with your bibliography entries.
   - Update the `TEIAS-LOGO.png` file in the root directory with your institution's logo if desired.

4. **Compile the Template**

   Open `main.tex` in your LaTeX editor and compile it using:

   - **Basic Compilation**:

     ```bash
     pdflatex main.tex
     ```

   - **With Bibliography**:

     ```bash
     pdflatex main.tex
     bibtex main
     pdflatex main.tex
     pdflatex main.tex
     ```

   - **Advanced Font Compilation** (if using custom fonts):

     ```bash
     xelatex main.tex
     ```

---

## Usage

### Selecting Themes and Color Schemes

#### Outer Theme

- **Options**: `shadow`, `smoothbars`, `split`, `sidebar`, `tree`, `miniframes`, `default`
- **Selection**:

  ```latex
  \newcommand{\outertheme}{shadow} % Change to your desired outer theme
  \useoutertheme{\outertheme}
  ```

- **Additional Options**:

  You can pass options to the outer theme, such as disabling subsections in `miniframes`:

  ```latex
  \useoutertheme[subsection=false]{miniframes}
  ```

#### Inner Theme

- **Options**: `rounded`, `rectangles`, `inmargin`, `circles`
- **Selection**:

  ```latex
  \newcommand{\innertheme}{rounded} % Change to your desired inner theme
  \useinnertheme[shadow=true]{\innertheme}
  ```

#### Color Scheme

- **Predefined Schemes**: 12 artistic color schemes
- **Selection**:

  ```latex
  \newcommand{\colorschemenumber}{7} % Choose a number from 1 to 12
  ```

- **Color Schemes Include**:

  1. Rich Red & Light Pink
  2. Deep Blue & Light Blue
  3. Teal & Light Cyan
  4. Orange & Light Orange
  5. Forest Green & Light Green
  6. Steel Blue & Light Steel Blue
  7. Deep Wine & White
  8. Crimson & White
  9. Indigo & Light Lavender
  10. Hot Pink & Light Pink
  11. Gold & Light Gold
  12. Purple & Light Purple

### Customizing Header and Footer

Customize headers and footers by setting the following commands in the preamble:

- **Header Options**:

  ```latex
  \newcommand{\includeheader}{true} % Set to 'false' to remove the header
  \newcommand{\showsectionintoc}{true} % Set to 'false' to hide sections in the header
  ```

- **Footer Options**:

  ```latex
  \newcommand{\includefooter}{true} % Set to 'false' to remove the footer
  \newcommand{\showauthorinfo}{true} % Set to 'false' to hide author info in the footer
  \newcommand{\showdateinfo}{true} % Set to 'false' to hide date info in the footer
  \newcommand{\showpagenumber}{true} % Set to 'false' to hide page numbers in the footer
  ```

### Adding Content

#### Defining Sections with Short and Long Names

You can provide both short and long names for sections to control how they appear in the navigation and in the content.

```latex
\section[Short Name]{Long Name}
```

- **Short Name**: Used in headers, footers, and navigation bars.
- **Long Name**: Used in the table of contents and section title slides.

**Example:**

```latex
\section[Intro]{Introduction to Machine Learning}
```

#### Creating Frames

```latex
\begin{frame}{\textsc{Introduction}}
  \begin{itemize}
    \item Point 1
    \item Point 2
  \end{itemize}
\end{frame}
```

- **Frame Title Alignment**:

  You can set the alignment of the frame title by adjusting the `frametitle` template:

  ```latex
  \setbeamertemplate{frametitle}[default][left]
  ```

  Options: `left`, `right`, `center`.

- **Including a Logo on Each Slide**:

  ```latex
  \logo{\includegraphics[height=1cm]{images/your-logo.png}}
  ```

- **Custom Bullet Points**:

  ```latex
  \setbeamertemplate{itemize item}{\includegraphics[height=0.3cm]{images/custom-bullet.png}}
  ```

### Aspect Ratio and Handout Options

- **Aspect Ratio**:

  Set the aspect ratio of your presentation:

  - **Standard (4:3)**:

    ```latex
    \documentclass[compress]{beamer}
    ```

  - **Widescreen (16:9)**:

    ```latex
    \documentclass[compress, aspectratio=169]{beamer}
    ```

- **Handout Version**:

  Generate a handout version without overlays:

  ```latex
  \documentclass[compress, handout]{beamer}
  ```

---

## Customization

### Defining Custom Colors

Define your own colors using the `\definecolor` command:

```latex
\definecolor{My_Custom_Color}{RGB}{123, 45, 67} % Define a new color
\definecolor{Light_Custom_Color}{RGB}{230, 200, 210} % Define a light variant
```

### Adding New Color Schemes

1. **Create a New Color Scheme Command**:

   ```latex
   \newcommand{\setcolorschemecustom}{
       \setbeamercolor{structure}{fg=My_Custom_Color}
       \setbeamercolor{titlelike}{parent=structure, bg=My_Custom_Color, fg=white}
       \setbeamercolor{itemize item}{fg=My_Custom_Color}
       \setbeamercolor{block title}{bg=My_Custom_Color, fg=white}
       \setbeamercolor{block body}{bg=Light_Custom_Color, fg=black}
   }
   ```

2. **Update the Selection Logic**:

   Add your custom scheme to the `\ifcase\colorschemenumber` logic:

   ```latex
   \ifcase\colorschemenumber
     \or % case 1
       \setcolorschemeone
     % ...
     \or % case 13
       \setcolorschemecustom
   \fi
   ```

3. **Select Your Custom Scheme**:

   ```latex
   \newcommand{\colorschemenumber}{13} % Select your custom scheme
   ```

### Modifying Fonts

For advanced font customization using `xelatex` or `lualatex`:

1. **Uncomment the Fontspec Package**:

   ```latex
   \usepackage{fontspec}
   ```

2. **Set Custom Fonts**:

   ```latex
   \setmainfont{Times New Roman}
   \setsansfont{Arial}
   \setmonofont{Courier New}
   ```

3. **Choose a Font Theme**:

   ```latex
   \newcommand{\fonttheme}{professionalfonts} % Options: professionalfonts, serif, sansserif, etc.
   \usefonttheme{\fonttheme}
   ```

---

## Advanced Features

### Mathematical Equations

Utilize `amsmath`, `amssymb`, and `mathtools` for typesetting:

```latex
\begin{equation}
  E = mc^2
\end{equation}
```

### Code Listings

Incorporate code with syntax highlighting using the `listings` package:

```latex
\begin{frame}[fragile]{\textsc{Code Example: Linear Regression in Python}}
  \begin{lstlisting}[language=Python]
import numpy as np
from sklearn.linear_model import LinearRegression

# Sample data
X = np.array([[1, 1], [1, 2], [2, 2], [2, 3]])
y = np.dot(X, np.array([1, 2])) + 3

# Create model and fit
model = LinearRegression().fit(X, y)

# Predictions
predictions = model.predict(X)
print(predictions)
  \end{lstlisting}
\end{frame}
```

### Inserting Images and Tables

- **Images**:

  ```latex
  \begin{frame}{\textsc{Machine Learning Workflow}}
    \begin{figure}
      \centering
      \includegraphics[width=0.8\textwidth]{images/ml_workflow.png}
      \caption{Typical steps in a machine learning project.}
    \end{figure}
  \end{frame}
  ```

- **Multiple Images with Subfigures**:

  ```latex
  \begin{frame}{\textsc{Visualization Examples}}
    \begin{figure}
      \centering
      \begin{subfigure}{0.45\textwidth}
        \includegraphics[width=\textwidth]{images/scatter_plot.png}
        \caption{Scatter Plot}
      \end{subfigure}
      \hfill
      \begin{subfigure}{0.45\textwidth}
        \includegraphics[width=\textwidth]{images/confusion_matrix.png}
        \caption{Confusion Matrix}
      \end{subfigure}
      \caption{Common visualizations in machine learning.}
    \end{figure}
  \end{frame}
  ```

- **Tables**:

  ```latex
  \begin{frame}{\textsc{Comparison of Algorithms}}
    \begin{table}[h!]
      \centering
      \begin{tabular}{lccc}
        \toprule
        \textbf{Algorithm} & \textbf{Type} & \textbf{Complexity} & \textbf{Interpretability} \\
        \midrule
        Linear Regression & Regression & Low & High \\
        Decision Trees & Both & Medium & Medium \\
        Neural Networks & Both & High & Low \\
        \bottomrule
      \end{tabular}
      \caption{Comparison of common machine learning algorithms.}
    \end{table}
  \end{frame}
  ```

### Section Title Slides

Customize section title slides with different backgrounds:

- **Background Options**: `default`, `image`, `color`
- **Setting Background**:

  ```latex
  \newcommand{\sectiontitleslidebackground}{image} % Options: 'default', 'image', 'color'
  \newcommand{\sectiontitleslideimage}{images/background.jpg} % Path to background image
  \newcommand{\sectiontitleslidecolor}{blue} % Background color (if 'color' is selected)
  ```

- **Configuration**:

  The section title slide is automatically configured in the preamble to use your settings.

### Custom Commands

Utilize predefined commands to enhance your content:

- **Highlight Text**:

  ```latex
  \newcommand{\highlight}[1]{\colorbox{yellow!50}{#1}}
  ```

  **Usage:**

  ```latex
  \highlight{Important Text}
  ```

- **Note Highlight**:

  ```latex
  \newcommand{\notehighlight}[1]{\colorbox{pink!50}{#1}}
  ```

  **Usage:**

  ```latex
  \notehighlight{Note: Remember this point.}
  ```

- **Custom Colored Box**:

  ```latex
  \newcommand{\custombox}[2]{\begin{tcolorbox}[colback=#1!5!white, colframe=#1!75!black]
  #2
  \end{tcolorbox}}
  ```

  **Usage:**

  ```latex
  \custombox{Rich_Red}{
    \begin{itemize}
      \item Point 1
      \item Point 2
    \end{itemize}
  }
  ```

- **Alert Text**:

  ```latex
  \newcommand{\alerttext}[1]{\textcolor{red}{\textbf{#1}}}
  ```

  **Usage:**

  ```latex
  \alerttext{This is a critical point.}
  ```

---

## Packages and Libraries

The template includes the following packages:

- **Essential Packages**:

  - `beamer` - Core package for presentations
  - `etoolbox` - Programming tools for LaTeX
  - `amsmath`, `amssymb`, `mathtools` - Enhanced mathematical typesetting
  - `graphicx` - Including graphics
  - `xcolor` - Color manipulation
  - `tikz` - Drawing vector graphics
  - `hyperref` - Hyperlinks in documents
  - `babel` - Multilingual support

- **Typography and Fonts**:

  - `fontspec` (requires `xelatex` or `lualatex`) - Advanced font selection
  - `setspace` - Line spacing adjustments
  - `tcolorbox` - Colored boxes with enhanced features

- **Code and Listings**:

  - `listings` - Code listings with syntax highlighting
  - `caption`, `subcaption` - Enhanced captions for figures and tables

- **Tables**:

  - `booktabs` - Professional-quality tables
  - `multirow`, `array` - Advanced table formatting
  - `siunitx` - SI units and number formatting

- **Bibliography and Citations**:

  - `natbib` - Flexible bibliography support
  - `bibtex` - Bibliography tool

- **Miscellaneous**:

  - `appendixnumberbeamer` - Correct numbering for appendices
  - `ifthen` - Conditional commands
  - `cleveref` - Intelligent cross-referencing

---

## Troubleshooting

- **Compilation Errors**:

  - Ensure all packages are installed. Use a comprehensive LaTeX distribution like TeX Live or MiKTeX.
  - For missing packages, use the package manager to install them.

- **Images Not Found**:

  - Verify that images are in the correct directory (`images/`).
  - Ensure that image file paths are correctly specified in the code.

- **Font Issues**:

  - If using custom fonts, compile with `xelatex` or `lualatex`.
  - Ensure the fonts are installed on your system.

- **Bibliography Not Displaying**:

  - Ensure `references.bib` exists and is correctly formatted.
  - Run `bibtex` as part of the compilation process.

- **Header/Footer Not Displaying Correctly**:

  - Check the boolean flags (`\includeheader`, `\includefooter`) in the preamble.
  - Verify that the `ifthen` package is included.

- **Navigation Symbols Not Showing**:

  - By default, navigation symbols are hidden. To display them, comment out or remove:

    ```latex
    \setbeamertemplate{navigation symbols}{}
    ```

- **Frame Numbering Issues**:

  - For frames where you don't want the frame number to appear, use:

    ```latex
    \begin{frame}[plain, noframenumbering]
    ```

- **Appendix Numbering**:

  - Ensure that you use `\appendix` before starting the appendix sections.

- **Date Formatting**:

  - Set the date manually if you don't want to use `\today`:

    ```latex
    \date[Nov 2024]{November 2024}
    ```

---

## Contributing

Contributions are welcome! Please follow these guidelines:

1. **Fork the Repository**

   Click on the 'Fork' button at the top right of the repository page.

2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add YourFeature"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Open a Pull Request**

   Navigate to your forked repository and click on 'New Pull Request'.

### Contribution Guidelines

- **Coding Standards**: Follow standard LaTeX coding conventions.
- **Branch Naming**: Use descriptive names like `feature/new-theme` or `bugfix/header-issue`.
- **Documentation**: Update the README and comment your code where applicable.
- **Code of Conduct**: Be respectful and considerate in communications.

---

## License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this template in your projects.

[View License](LICENSE)

---

## Acknowledgements

- **Beamer**: [https://ctan.org/pkg/beamer](https://ctan.org/pkg/beamer) - The LaTeX class for creating presentations.
- **Overleaf**: [https://www.overleaf.com/](https://www.overleaf.com/) - Online LaTeX editor.
- **LaTeX Community**: For continuous support and resources.
- **Contributors**: Special thanks to all contributors who have improved this template.

---

## Contact

For questions, suggestions, or feedback, please contact:

**Amirreza "Farnam" Taheri**

- **Email**: [TaheriFarnam@gmail.com](mailto:TaheriFarnam@gmail.com)
- **GitHub**: [AmirrezaFarnamTaheri](https://github.com/AmirrezaFarnamTaheri)

---

*Created with ❤️ by [Amirreza "Farnam" Taheri](https://github.com/AmirrezaFarnamTaheri).*

---

*This README is intended to help users effectively utilize the Beamer Presentation Template. Your contributions and suggestions are highly appreciated.*

---

*Last updated on: November 2024*

---

# License

MIT License

---

# Acknowledgements

- **Beamer Class**: The foundation of this template.
- **LaTeX Community**: For the wealth of knowledge and support.
- **All Users**: Thank you for using and contributing to this template.
