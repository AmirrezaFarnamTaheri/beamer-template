[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Beamer Presentation Template

Welcome to the **Beamer Presentation Template**! This is a comprehensive and highly customizable LaTeX Beamer template designed to help you create professional, visually appealing presentations with ease. Whether you're preparing for academic lectures, research presentations, business meetings, or any other type of presentation, this template provides a robust foundation to build upon.

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

This Beamer template provides a solid foundation with a plethora of customization options to suit your presentation needs. It includes multiple themes, color schemes, font options, and additional features that enhance the overall look and functionality of your slides. By utilizing this template, you can save time and ensure consistency across your slides, while also having the flexibility to tailor the presentation to your preferences.

### Repository Information

- **Repository Name:** `beamer-template`
- **Repository URL:** [https://github.com/AmirrezaFarnamTaheri/beamer-template](https://github.com/AmirrezaFarnamTaheri/beamer-template)
- **Hosting Platform:** GitHub

---

## Key Features

### Customizable Themes

#### Outer Themes

Modify the outer appearance of your slides with options like:

- `shadow`
- `smoothbars`
- `split`
- `sidebar`
- `tree`
- `miniframes`
- `default`

These themes alter navigation bars, frame transitions, and the overall slide structure to suit your presentation style.

#### Inner Themes

Adjust the inner elements of your slides with themes such as:

- `rounded`
- `rectangles`
- `inmargin`
- `circles`

Inner themes affect the styling of items like blocks, lists, and the appearance of content within frames.

### Extensive Color Schemes

Choose from 12 predefined artistic color schemes, or define your own custom schemes to match your branding or personal preference. Each color scheme carefully pairs foreground and background colors for optimal readability and aesthetic appeal.

### Flexible Layouts

- **Aspect Ratios**: Support for different aspect ratios, including standard (4:3) and widescreen (16:9).
- **Handout Version**: Generate handouts without overlays, suitable for printing or sharing as PDFs.
- **Navigation Styles**: Choose navigation styles with or without mini frames, and customize headers and footers.

### Enhanced Functionality

- **Mathematical Typesetting**: Integrated packages for mathematics (`amsmath`, `amssymb`, `mathtools`).
- **Graphics Support**: Include graphics and draw vector images using `graphicx` and `tikz`.
- **Code Listings**: Add code snippets with syntax highlighting using the `listings` package.
- **Table Enhancements**: Create professional-quality tables with `booktabs`, `multirow`, and `array`.

### Custom Header/Footer

- **Customizable Content**: Options to include or exclude headers and footers, and to customize their content.
- **Dynamic Information**: Display author, date, page numbers, and section titles in the header or footer.

### Section Title Slides

- **Automatic Section Slides**: Automatically create section title slides when new sections begin.
- **Customizable Backgrounds**: Customize section title slides with default backgrounds, images, or solid colors.

### Reusable Commands

Utilize predefined commands for:

- Highlighting text
- Creating custom boxes and alerts
- Including custom symbols
- Formatting footnotes

### Appendix Support

Seamlessly add appendix sections with proper numbering and inclusion in the table of contents.

### Font Customization

- **Font Themes**: Options for professional fonts, serif, sans-serif, and more.
- **Advanced Font Settings**: Use `fontspec` with `XeLaTeX` or `LuaLaTeX` for advanced font customization.

### Custom Bullets and Logos

- **Custom Bullet Points**: Replace default bullet points with custom images.
- **Slide Logos**: Include custom logos on each slide, such as institutional or company logos.

### Frame Title Alignment

Set the alignment of frame titles to left, right, or center, according to your preference.

### Support for Short and Long Section Names

Define short and long formats for section names to control their display in navigation and content.

---

## Prerequisites

To use this Beamer template effectively, ensure you have the following installed:

- **LaTeX Distribution**: [TeX Live](https://www.tug.org/texlive/), [MiKTeX](https://miktex.org/), or [MacTeX](https://www.tug.org/mactex/)
- **Compiler**: `pdflatex` (for basic usage), `xelatex`, or `lualatex` (for advanced font customization)
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

  1. **Rich Red** & **Light Pink**
  2. **Deep Blue** & **Light Blue**
  3. **Teal** & **Light Cyan**
  4. **Orange** & **Light Orange**
  5. **Forest Green** & **Light Green**
  6. **Steel Blue** & **Light Steel Blue**
  7. **Deep Wine** & **White**
  8. **Crimson** & **White**
  9. **Indigo** & **Light Lavender**
  10. **Hot Pink** & **Light Pink**
  11. **Gold** & **Light Gold**
  12. **Purple** & **Light Purple**

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

This allows you to have concise labels in navigation elements while providing full titles in the content.

#### Creating Frames

Create individual slides (frames) using the `frame` environment:

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
  \setbeamertemplate{frametitle}[default][left]   % Align left
  \setbeamertemplate{frametitle}[default][center] % Align center
  \setbeamertemplate{frametitle}[default][right]  % Align right
  ```

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
\definecolor{MyCustomColor}{RGB}{123, 45, 67}       % Define a new color
\definecolor{LightCustomColor}{RGB}{230, 200, 210}  % Define a light variant
```

### Adding New Color Schemes

1. **Create a New Color Scheme Command**:

   ```latex
   \newcommand{\setcolorschemecustom}{
       \setbeamercolor{structure}{fg=MyCustomColor}
       \setbeamercolor{titlelike}{parent=structure, bg=MyCustomColor, fg=white}
       \setbeamercolor{itemize item}{fg=MyCustomColor}
       \setbeamercolor{block title}{bg=MyCustomColor, fg=white}
       \setbeamercolor{block body}{bg=LightCustomColor, fg=black}
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

For advanced font customization using `XeLaTeX` or `LuaLaTeX`:

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

Utilize `amsmath`, `amssymb`, and `mathtools` for advanced mathematical typesetting:

```latex
\begin{equation}
  E = mc^2
\end{equation}
```

Include equations, alignments, and matrices as needed.

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

Ensure to include the `[fragile]` option in the `frame` environment when using `lstlisting`.

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
  \custombox{RichRed}{
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

  - `fontspec` (requires `XeLaTeX` or `LuaLaTeX`) - Advanced font selection
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

For more information on each package, refer to their documentation on [CTAN](https://www.ctan.org/).

---

## Troubleshooting

- **Compilation Errors**:

  - **Missing Packages**: Ensure all required packages are installed. Use the package manager included with your LaTeX distribution to install missing packages.
  - **Outdated Distribution**: Update your LaTeX distribution to the latest version to ensure compatibility.

- **Images Not Found**:

  - **Incorrect Paths**: Verify that image file paths are correctly specified, and that the images are located in the `images/` directory.
  - **Unsupported Formats**: Ensure images are in a format supported by your compiler (`.png`, `.jpg`, `.pdf`).

- **Font Issues**:

  - **Custom Fonts Not Applied**: If using custom fonts, compile with `XeLaTeX` or `LuaLaTeX` instead of `pdfLaTeX`.
  - **Missing Fonts**: Ensure the fonts are installed on your system.

- **Bibliography Not Displaying**:

  - **Bibliography File**: Ensure `references.bib` exists and is correctly formatted.
  - **Compilation Order**: Run `bibtex` as part of the compilation process to generate the bibliography.

- **Header/Footer Not Displaying Correctly**:

  - **Boolean Flags**: Check the boolean flags (`\includeheader`, `\includefooter`) in the preamble.
  - **Package Inclusion**: Verify that the `ifthen` package is included.

- **Navigation Symbols Not Showing**:

  - **Default Setting**: By default, navigation symbols are hidden. To display them, comment out or remove:

    ```latex
    \setbeamertemplate{navigation symbols}{}
    ```

- **Frame Numbering Issues**:

  - **Suppressing Frame Numbers**: For frames where you don't want the frame number to appear, use:

    ```latex
    \begin{frame}[plain, noframenumbering]
    ```

- **Appendix Numbering**:

  - **Starting the Appendix**: Ensure that you use `\appendix` before starting the appendix sections to reset numbering.

- **Date Formatting**:

  - **Custom Date**: Set the date manually if you don't want to use `\today`:

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

- **Coding Standards**: Follow standard LaTeX coding conventions and maintain consistent formatting.
- **Branch Naming**: Use descriptive names like `feature/new-theme` or `bugfix/header-issue`.
- **Documentation**: Update the README and comment your code where applicable.
- **Code of Conduct**: Be respectful and considerate in communications. Follow the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/0/code_of_conduct/).

---

## License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this template in your projects.

[View the Full License](LICENSE)

---

## Acknowledgements

- **Beamer Class**: [Beamer](https://ctan.org/pkg/beamer) - The LaTeX class for creating presentations.
- **Overleaf**: [Overleaf](https://www.overleaf.com/) - Online LaTeX editor.
- **LaTeX Community**: For continuous support and resources.
- **Contributors**: Special thanks to all contributors who have improved this template.
- **Open Source Packages**: Gratitude to the maintainers of the LaTeX packages used in this template.

---

## Contact

For questions, suggestions, or feedback, please contact:

**Amirreza "Farnam" Taheri**

- **Email**: [TaheriFarnam@gmail.com](mailto:TaheriFarnam@gmail.com)
- **GitHub**: [AmirrezaFarnamTaheri](https://github.com/AmirrezaFarnamTaheri)
- **LinkedIn**: [Amirreza Taheri](https://www.linkedin.com/in/amirreza-farnam-taheri/)

---

*Created with ❤️ by [Amirreza "Farnam" Taheri](https://github.com/AmirrezaFarnamTaheri).*

---

*This README is intended to help users effectively utilize the Beamer Presentation Template. Your contributions and suggestions are highly appreciated.*

---

*Last updated on: November 2024*

---

# License

MIT License

[Full License Text](LICENSE)

---

# Acknowledgements

- **Beamer Class**: The foundation of this template.
- **LaTeX Community**: For the wealth of knowledge and support.
- **All Users**: Thank you for using and contributing to this template.

---

# Shortcuts for Quick Navigation

- **[Back to Top](#beamer-presentation-template)**
