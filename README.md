# Resume
Template from https://github.com/cies/resume
To output Chinese characters in a LaTeX document on Ubuntu, you will need to follow a series of steps to ensure that your system and LaTeX installation are properly configured. Here's how you can do it:

1. **Install TeX Live**: Make sure you have TeX Live installed. It's a comprehensive TeX system that includes XeLaTeX and LuaLaTeX, which are essential for processing Chinese characters. You can install TeX Live from the Ubuntu repositories:

   ```bash
   sudo apt-get update
   sudo apt-get install texlive-full
   ```

   The `texlive-full` package includes a full installation of TeX Live, including fonts and utilities for different languages, including Chinese.

2. **Install Chinese Fonts**: Ubuntu might not come with Chinese fonts pre-installed, so you should install some:

   ```bash
   sudo apt-get install fonts-noto-cjk
   ```

   This command installs the "Noto CJK" fonts, which cover Chinese, Japanese, and Korean.

3. **Configure Your LaTeX Document**:
   - Use the `ctex` package, which is specifically designed for typesetting Chinese text.
   - Compile your document with XeLaTeX or LuaLaTeX for better Unicode support.

   Here's a sample preamble for your LaTeX document:

   ```latex
   %!TEX program = xelatex  % Specify the LaTeX engine (XeLaTeX)
   \documentclass[10pt,a4paper]{article}
   \usepackage{ctex}
   % Other packages and settings...
   ```

   In this configuration, the `ctex` package will automatically select a suitable Chinese font installed on your system.

4. **Compile with XeLaTeX or LuaLaTeX**: When compiling your document, use XeLaTeX or LuaLaTeX. You can do this from the command line:

   ```bash
   xelatex your-document.tex
   ```

   Or you can configure your LaTeX editor to use XeLaTeX or LuaLaTeX as the default compiler.

By following these steps, your LaTeX installation on Ubuntu should be able to handle Chinese characters effectively. If you encounter any issues or need further assistance, feel free to ask.
