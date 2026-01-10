# kssolutionsllc.github.io

This is the source code for the KSS Solutions LLC website, built with [Jekyll](https://jekyllrb.com/).

## Local Development (macOS)

This project is configured to run locally with **isolated dependencies** to avoid modifying your system configuration.

### Prerequisites

*   **macOS** (comes with Ruby installed by default)
*   **Bundler** (If not installed, run `gem install bundler`)

### First-Time Setup

1.  **Clone the repository** and navigate to the directory:
    ```bash
    cd kssolutionsllc.github.io
    ```

2.  **Configure Bundler to install gems locally** (this keeps your system clean):
    ```bash
    bundle config set --local path 'vendor/bundle'
    ```

3.  **Install dependencies**:
    ```bash
    bundle install
    ```
    *Note: If you encounter permission errors, ensure step 2 was run correctly so gems are installed in the project folder, not the system.*

### Running the Website

Start the local server:

```bash
bundle exec jekyll serve
```

Open your browser to: http://127.0.0.1:4000

The site supports live reloading, so changes to HTML/CSS files should appear automatically.

### Troubleshooting

*   **`ffi` gem errors**: The `Gemfile` is pinned to `ffi ~> 1.15.0` to ensure compatibility with the default macOS Ruby (2.6.x). Do not update this gem unless you upgrade Ruby.
*   **Clean start**: If you have issues, delete the local artifacts and reinstall:
    ```bash
    rm -rf vendor/bundle .bundle _site
    bundle install
    ```
