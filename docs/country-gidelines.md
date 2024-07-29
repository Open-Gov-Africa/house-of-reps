# Country-Specific Data Guidelines

## Adding Contact Details of Officials

### Finding Information
1. **Official Government Portals**: Check official government websites for contact details of officials.
2. **Public Records**: Use publicly available records and verified sources.

### Adding Contact Details
1. **Create Directories**: Follow the structure `data/country/{country-name}/contacts/{office-type}`.
```plaintext
repository-name/
├── data/
│   ├── country/
│   │   ├── nigeria/
│   │   │   ├── contacts/
│   │   │   │   ├── representatives/
│   │   │   │   │   ├── {official-name}.json
│   │   │   │   ├── senators/
│   │   │   │   │   ├── {official-name}.json
│   │   │   │   ├── ministers/
│   │   │   │   │   ├── {official-name}.json
│   │   │   │   ├── businesses/
│   │   │   │   │   ├── {official-name}.json
│   │   │   └── ...
│   │   ├── kenya/
│   │   └── ...
├── docs/
├── src/
├── tests/
├── README.md
├── LICENSE
└── CONTRIBUTING.md
```
2. **JSON Template**: Use the standard JSON template to add contact details for each official.

#### Example JSON Template
```json
{
  "name": "John Doe",
  "position": "Representative",
  "office": "House of Representatives",
  "country": "Nigeria",
  "phone": "+234-123-456-7890",
  "email": "john.doe@example.com",
  "address": {
    "office_address": "123 Government Building, Abuja, Nigeria",
    "postal_code": "12345"
  },
  "social_media": {
    "twitter": "@JohnDoe",
    "facebook": "facebook.com/JohnDoe"
  },
  "term_start": "2023-01-01",
  "term_end": "2027-01-01"
}
```
3. **File Naming Convention**: Use the official's name in the file name, formatted as `{official-name}.json`.

### Contribution Workflow
1. **Fork the Repository**: Fork the main repository to your GitHub account.
2. **Create a Branch**: Create a new branch for your additions (e.g., `add-nigeria-contacts`).
3. **Add Data**: Add your JSON files with contact details to the appropriate directories.
4. **Submit a Pull Request**: Submit a pull request with a detailed description of the added contact details.

### Review and Approval
1. **Initial Review**: A maintainer will review your pull request for structure and completeness.
2. **Feedback**: You may receive feedback or requests for additional information or changes.
3. **Approval**: Once approved, your data will be merged into the main repository.
