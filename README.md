# How to Install Quarto and View the Presentation

This guide explains, step by step, how to install **Quarto** on **Windows** and **Mac**, and how to open the presentation (`.qmd`) and view it in a web browser.

No programming knowledge is required. You only need to copy and paste a few commands.

---

## What is Quarto and Why Do We Need It?

**Quarto** is a free tool that converts a text file (`.qmd`) into a slide presentation that can be opened in a web browser (HTML format).

The workflow is simple:

```text
presentation.qmd  ──►  Quarto  ──►  presentation.html
```

You only need to install **Quarto once**. After that, a single command is enough to generate the presentation.

---

## Windows

### Option A — Installer (easiest)

1. Go to the official website: <https://quarto.org/docs/get-started/>
2. Click the blue **Download Quarto CLI** button.
3. Open the downloaded file (`.exe`).
4. Follow the installation wizard by clicking **Next** until the installation is complete. Leave all options at their default settings.
5. Close the wizard when finished.

### Option B — Using a command (for technical users)

Open **PowerShell** or **Command Prompt** and enter:

```powershell
winget install Posit.Quarto
```

### Verify the installation

Open **PowerShell** or **Command Prompt** and enter:

```powershell
quarto --version
```

If a version number appears (for example, `1.5.57`), everything is ready!

---

## Mac

### Option A — Installer (easiest)

1. Go to the official website: <https://quarto.org/docs/get-started/>
2. Click the blue **Download Quarto CLI** button (this will download a `.pkg` file).
3. Go to your **Downloads** folder and double-click the `.pkg` file.
4. Follow the installation instructions and click **Close** when finished.

### Option B — Using Homebrew (for technical users)

If you already have [Homebrew](https://brew.sh) installed, open the **Terminal** app and enter:

```bash
brew install --cask quarto
```

### Verify the installation

Open the **Terminal** app (find it using Spotlight: `Cmd + Space` and type "Terminal") and enter:

```bash
quarto --version
```

If a version number appears, everything is ready!

---

## View the Presentation

Once Quarto is installed, follow these steps (the process is the same on Windows and Mac):

1. Place the presentation file (`github-workshop-simple.qmd`) in an easy-to-find folder, such as the **Desktop**.

2. Open the terminal:
   - **Windows:** PowerShell or Command Prompt.
   - **Mac:** the Terminal app.

3. Navigate to the folder where the file is located. For example, if it is on the Desktop:

   ```bash
   cd Desktop
   ```

4. Generate the presentation:

   ```bash
   quarto render github-workshop-simple.qmd
   ```

   This will create a `github-workshop-simple.html` file in the same folder. Double-click it to open it in your browser.

### Alternative: Live Preview

If you prefer the presentation to update automatically whenever the file is edited, use:

```bash
quarto preview github-workshop-simple.qmd
```

The presentation will automatically open in your browser. To stop the preview, press `Ctrl + C` in the terminal.

---

## Navigating the Presentation

- **Keyboard arrows** (← →) or click to move forward and backward.
- Press **F** for full-screen mode.
- Press **Esc** to view all slides as thumbnails.
- Press **S** to open the speaker view (notes and timer).

---

## Frequently Asked Questions

**Do I need to install anything else?**

No, not for this presentation. Quarto generates the HTML by itself. (Additional tools would only be required if you wanted to export the presentation to PDF, which is not the case here.)

**Can I share the presentation with someone who does not have Quarto?**

Yes. Once the `.html` file has been generated, you can send it by email or upload it to a server. It will open in any web browser without requiring Quarto to be installed.

**Where can I find the official documentation?**

You can find Windows, Mac, and Linux guides at <https://quarto.org/docs/get-started/>.

---

*If you have any questions about the installation, we'll be happy to help you resolve them together.*