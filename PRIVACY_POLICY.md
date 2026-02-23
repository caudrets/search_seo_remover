# Privacy Policy — SEO Remover Chrome Extension

**Last updated:** February 2026

## What This Extension Does

SEO Remover analyzes Google search results to identify SEO-optimized spam content. It fetches the text content of search result pages, sends that content to the Anthropic API for classification, and visually demotes results flagged as SEO spam.

## Data Collection and Use

### Data We Collect

- **Anthropic API key**: You provide your own API key through the extension popup. It is stored locally on your device using `chrome.storage.local` and is never synced to the cloud or transmitted to anyone other than Anthropic's API.

- **Search result URLs and page content**: When you perform a Google search, the extension reads the URLs, titles, and snippets shown on the search results page. It then fetches the text content of each result page. This data is sent to the Anthropic API solely for the purpose of classifying results as SEO spam or genuine content.

### Data We Do NOT Collect

- We do not collect, store, or transmit your search queries.
- We do not collect browsing history beyond the current search results page.
- We do not collect any personal information (name, email, etc.).
- We do not use cookies or tracking of any kind.
- We do not collect analytics or usage telemetry.

## Third-Party Data Sharing

The only third party that receives data from this extension is **Anthropic** (via their API at `api.anthropic.com`). The data sent consists of:

- Text content extracted from search result pages (titles, snippets, and page body text)
- Technical metadata about those pages (structured data types, meta tags)

This data is sent using your own Anthropic API key and is subject to [Anthropic's API Terms of Service](https://www.anthropic.com/api-terms) and their data handling practices. Anthropic's API does not use API inputs for model training.

No data is sold, shared with data brokers, or used for advertising purposes.

## Data Retention

- **API key**: Stored locally on your device until you clear it or uninstall the extension.
- **Search result data**: Processed in memory only. No search results, page content, or classification results are stored persistently. All data is discarded when the browser tab is closed or a new search is performed.

## Data Security

- Your API key is stored in `chrome.storage.local` (device-only, not synced to the cloud).
- The API key is never displayed in full in the UI — only a masked version is shown.
- All communication with the Anthropic API uses HTTPS encryption.
- Page fetches are made without cookies (`credentials: 'omit'`) to prevent leaking authenticated content.
- URLs are validated before fetching to prevent access to private/internal network resources.

## Permissions

This extension requires the following permissions:

- **`activeTab`**: To read Google search results on the current tab.
- **`storage`**: To store your API key locally.
- **`https://www.google.com/*`**: To run the content script on Google search pages.
- **`https://*/*`**: To fetch the content of search result pages for analysis. This broad permission is required because search results can link to any website. URL validation ensures only public HTTP(S) URLs are fetched.

## Your Rights

- You can view, change, or delete your API key at any time through the extension popup.
- You can uninstall the extension at any time to remove all locally stored data.
- No account or registration is required to use this extension.

## Changes to This Policy

If this privacy policy is updated, the changes will be reflected in the extension's store listing and this document.

## Contact

For questions about this privacy policy or the extension's data practices, please open an issue on the project's GitHub repository.
