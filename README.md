# fenu.dev-comments

**fenu.dev-comments** is a repository that integrates [utterances](https://utteranc.es/) to handle blog comments using GitHub issues. This lightweight, open source comments widget leverages GitHub issues for blog comments, wiki pages, and more, providing a secure, privacy-friendly alternative to traditional commenting systems.

---

## Features

- **GitHub Issues as Data Store:** Comments are stored as GitHub issues, ensuring that your data is always accessible and under your control.
- **Privacy First:** No tracking or ads – utterances remains completely free and private.
- **Lightweight & Fast:** Built with vanilla TypeScript, utterances is optimized for performance without unnecessary bloat.
- **Ease of Integration:** Automatically creates a GitHub issue when a comment is posted, simplifying the setup process.
- **Theming:** Styled with [Primer CSS](https://primer.style/), including support for a dark theme.

---

## How It Works

When the utterances widget loads on your blog, it uses the GitHub issue search API to:

1. **Identify the Associated Issue:** It searches for an issue that matches the current page based on `url`, `pathname`, or `title`.
2. **Automatic Issue Creation:** If no matching issue is found, the [utterances bot](https://utteranc.es/) will automatically create one when someone leaves a comment.
3. **Commenting Process:** Users can comment using GitHub OAuth for authorization, or directly on the GitHub issue page if they prefer.

---

## Installation & Setup

Follow these steps to integrate fenu.dev-comments into your blog:

1. **Fork or Clone this Repository:**
   ```bash
   git clone https://github.com/yourusername/fenu.dev-comments.git
   ```
   
2. **Configure Your GitHub Repository:**
   - Ensure that your repository contains GitHub issues enabled.
   - Add the `utterances` topic to your repository to signal its usage.

3. **Integrate with Your Blog:**
   - Include the utterances script in your blog pages where you would like comments to appear.
   - Example configuration snippet:

     ```html
     <script src="https://utteranc.es/client.js"
       repo="yourusername/your-repo"
       issue-term="pathname"
       theme="github-light"
       crossorigin="anonymous"
       async>
     </script>
     ```
   - Replace `"yourusername/your-repo"` with your actual GitHub repository details.
   - Adjust the `issue-term` and `theme` values as needed to match your blog setup.

4. **Test the Integration:**
   - Visit a page on your blog and leave a comment to verify that the comment is correctly linked to a GitHub issue.

---

## Customization

You can customize the comment widget further by adjusting the configuration parameters in the script. For instance:

- **`issue-term`:** Choose the method used to map a page to its GitHub issue (`pathname`, `url`, or `title`).
- **`theme`:** Select from multiple themes available in utterances, or create a custom theme to match your site's design.

Refer to the [utterances documentation](https://utteranc.es/) for more details on available options and advanced configurations.
