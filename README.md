# Multi-Agent Systems @ Birmingham (MAS@B)

This repository hosts the official website for **Multi-Agent Systems @ Birmingham (MAS@B)**, served via GitHub Pages at [`https://mas-birmingham.github.io`](https://mas-birmingham.github.io).

The site is built with pure Markdown and Jekyll to keep it clean, fast, text-focused, and easy for any group member to update via standard GitHub Pull Requests.

## 📁 Website Structure & File Directory

The site structure is intentionally flat and straightforward:

```text
mas-birmingham.github.io/
├── _config.yml        # Site metadata, Jekyll theme, and header navigation
├── Gemfile            # Local Ruby dependencies matching GitHub Pages
├── index.md           # Homepage (/)
├── members.md         # Member profiles & research interests (/members)
├── topics.md          # Reading group topics & schedule (/topics)
└── README.md          # Repository documentation & local setup guide

```

### File Breakdown

* **`_config.yml`**
* **Purpose:** The global configuration file for Jekyll.
* **What it controls:** Sets the site title, sub-description, GitHub Pages theme (e.g., `jekyll-theme-minimal` or `minima`), and the links displayed in the top header navigation (`header_pages`).


* **`Gemfile`**
* **Purpose:** Declares the software dependencies needed to build the site.
* **What it controls:** Locks the local build environment to the `github-pages` gem, ensuring your local preview looks identical to the live deployed site.


* **`index.md` (Homepage)**
* **Purpose:** Main landing page for MAS@B.
* **What to put here:** A high-level introduction to the research group, routine meeting times/locations, key links, and general group announcements.


* **`members.md` (Member Profiles)**
* **Purpose:** Public directory of group members and collaborators.
* **What to put here:** Member names, roles (Faculty, Postdoc, PhD, Student), research focus areas, contact emails, and personal site/GitHub links.


* **`topics.md` (Discussion & Schedule)**
* **Purpose:** Living agenda for reading group sessions and seminars.
* **What to put here:** A schedule table listing upcoming meeting dates, paper titles/topics, session leads, and locations, followed by a list of core research themes.


## 🤝 How to Contribute

Group members are encouraged to keep their profiles and seminar schedules up to date.

### Adding Yourself to `members.md`

1. Fork this repository or create a new branch.
2. Open `members.md` and add your profile using the standard layout:
```markdown
### Your Name
* **Role:** PhD Researcher / Faculty / Postdoc
* **Focus Areas:** Cooperative MARL, Swarm Robotics, Game Theory
* **Contact:** `username@bham.ac.uk` | [Website](https://your-website.com)

```


3. Submit a **Pull Request**.

### Updating the Schedule in `topics.md`

1. Edit the Markdown table in `topics.md` to add new dates, papers, or meeting topics.
2. Submit a **Pull Request**.

## 🛠️ Running the Site Locally

Follow these steps to preview changes on your computer before pushing to GitHub.

### 1. Prerequisites
GitHub Pages dependencies (specifically Jekyll and Liquid) require an older version of Ruby to build properly. Install **Ruby 3.1** and **Git** for your operating system:

* **macOS:** 
  Use Homebrew to install Ruby 3.1:
  ```bash
  brew install ruby@3.1 git
  ```

* **Linux (Ubuntu/Debian):**
  ```bash
  sudo apt update && sudo apt install ruby3.1 ruby3.1-dev build-essential zlib1g-dev git
  ```

* **Windows:**
Download and install [RubyInstaller with DevKit](https://rubyinstaller.org/). (We recommend choosing a **Ruby 3.1.x** version).

Ensure ruby is added to your system path. On macOS:
```bash
echo 'export PATH="$(brew --prefix ruby@3.1)/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
You can verify your active version by running `ruby -v` in your terminal.

### 2. Clone the Repository

```bash
git clone https://github.com/mas-at-birmingham/mas-at-birmingham.github.io.git
cd mas-at-birmingham.github.io
```

### 3. Install Dependencies

Ensure `Gemfile` is in the repository root, then run:

```bash
gem install bundler
bundle install
```

> *Note for macOS/Linux:* If you hit permission issues, run `bundle config set --local path 'vendor/bundle'` before `bundle install` to install gems inside the project folder without root permissions.

### 4. Start the Local Server

```bash
bundle exec jekyll serve --livereload
```

### 5. View in Browser

Open **`http://localhost:4000`** in your web browser. The server will automatically reload when you make changes to any `.md` file.