># Archived Aras Community Project
>This project has been migrated to GitHub from the old Aras Projects page (http://www.aras.com/projects). As an Archived project, this project is no longer being actively developed or maintained.

>For current projects, please visit the new Aras Community Projects page on the updated Aras Community site: http://community.aras.com/projects

# Life Cycle Based Properties and Form Fields

Latest version: r1-0. Adds the definition of generic property checks base on life cycle state of an item. it also add a report to show the results of these checks

It is a common requirement that properties defined by ItemType should also be checked as required properties based on a Life Cycle state. It is also common that visibility and disabled status of data fields (bound to properties) on a form must be controlled by Life Cycle State and/or defined Identities (User Groups). Rather than writing custom logic for the above behavior a generic logic can be introduced to read additional property configurations.

## History

This project and the following release notes have been migrated from the old Aras Projects page. Unlike community projects that have been migrated and archived, this project will be updated for compatibility with the latest release of Aras Innovator.

Release | Notes
--------|--------
[v1](https://github.com/ArasLabs/lc-based-props-and-fields/releases/tag/v1) | Add-on Solution Package and Documentation.

#### Supported Aras Versions

Project | Aras
--------|------
[v1](https://github.com/ArasLabs/lc-based-props-and-fields/releases/tag/v1) | 9.3

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **lc-based-props-and-fields** import packages

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\lc-based-props-and-fields\Import\imports.mf` file in the Manifest File field.
6. Select all packages in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

## Usage

See [Life Cycle Based Props and Fields v1-2.pdf](./Documentation/Life%20Cycle%20Based%20Props%20and%20Fields%20v1-2.pdf) for more information on using this project.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Created by Rolf Laudenbach for Aras Corporation.

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
