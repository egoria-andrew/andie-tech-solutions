# Website maintenance

| Change | Where to edit |
| --- | --- |
| Service name, description, price, or booking message | `index.html` |
| Quick Fixes articles | `fixes.html` |
| Layout, colours, and responsive design | `style.css` |
| Logos and illustrations | `assets/` |
| Footer service list and navigation | `index.html` and `fixes.html` |

## Before publishing

- Check that every WhatsApp link uses the current business number.
- Ensure service cards and the footer’s **What we offer** list match.
- Test Home, Services, Quick Fixes, Contact, and booking links.
- Check the hamburger menu and service-card layout on a phone.
- Keep customer information out of public HTML files and Git commits.

## Versioning

- Keep the production site on `main`.
- Use descriptive feature branches for changes.
- Create Git tags for major approved releases, for example `v1.0.0` and `v2.0.0`.
