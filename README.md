# 45th LD Democrats Mailman Templates

HTML and TXT templates used by the [45th District Democrats of Washington State](https://www.45thdemocrats.org/) for our GNU Mailman 2.1 instance (the version used by our webhost's shared servers). Templates and messages have been fully skinned and customized extensively to support our organization's use case. HTML templates are mobile-friendly, responsive, and (mostly) accessible.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Support](#support)
- [Contributing](#contributing)

## Installation

For every list on your Mailman instance (including any future lists you may create), copy and paste the contents of these files into their equivalent templates in your Mailman instance, then modify as desired. This can be done through either the CLI or Mailman's built-in admin GUI (click the "Edit the public HTML pages and text files" link under "Other Administrative Activities").

## Usage

You'll want to switch out our organization's hardcoded info with your own, and may need to modify the content to fit your use case and feature set. Some of our customizations include:
- Using [our website's](https://www.45thdemocrats.org/) CSS styles as a basis for skinning the HTML templates
- Adding recommended password criteria
- Limiting the scenarios in which a plaintext password is sent to a subscriber
- Not using the built-in substitution variables for our mailing lists' full email addresses, instead concatenating the listname with the subdomain used for our "convenience addresses" (we don't want to confuse our members by referencing two sets of email addresses in various places)
- Hiding various subscriber options and features across templates that we don't want folks messing with, including:
  - Setting new password globally (sweet single point of failure, Batman!)
  - Language switching (we only support English)
  - Digest options (we've disabled digests)
  - Hide from subcribers list (we don't want invisible subscribers)
  - Send monthly password reminders
  - Receive acknowledgement mail when a message is sent
  - Administrator info in footers (we refer folks to our Tech Committee's email instead)
  - Notes about x-mailman-copy headers in options page
  - Overly-verbose explanations in subscription options and messages
  - Instructions to reply to emails to respond to requests instead of clicking links (confusing for most folks, and if you know, you know)

Additionally, our Mailman instance is configured with some overly-strict HTML security settings, so a lot of our code is duplicated, redundant, or otherwise not optimized as a result. If you're able to access your Mailman instance using SSH and can circumvent or disable this "feature", you can refactor this code to your heart's content. You may also be able to override Mailman's default templates, instead of having to rewrite them separately for every list.

## Support

Please [open an issue](https://github.com/pixelSHREDDER/45th-dems-mailman/issues/new) for support.

## Contributing

Please contribute using [Github Flow](https://guides.github.com/introduction/flow/). Create a branch, add commits, and [open a pull request](https://github.com/pixelSHREDDER/45th-dems-mailman/compare/).
