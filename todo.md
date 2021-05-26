# MJML compilation
Create a script that does the following regex-replace on the contents of a `.mjml` file before passing it to the MJML compiler to wrap all dangling Handlebars tags in `<mj-raw></mj-raw>` tags.

Regex: `/(?<!<[^>]*?)({{{?[\s\S]*?}}}?)(?![\w\s]*[>])/gim`
Replace: `<mj-raw>$1</mj-raw>`