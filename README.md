# Repository to Update Details Shown on Widget
A place for product teams to configure details to be shown on the dev console widget.

## How It Works

Changes to the `main` branch in this repo will throw a webhook to api gateway in AWS, which will then invoke lambda function to update s3 bucket holding all of the latest product details json files.

Widget then consumes these updated details through REST API calls.

**NOTE : This repository will be the single source of truth for product details displayed on widget.**

## Usage Guide

1. Create a branch out of main.
2. Find your project's json files in `products-details/` folder.
3. Edit accordingly (refer to the `Recommended Practices for Editing Product Details` portion below).
4. Create a PR against main branch and see preview of your changes with the amplify link provided in the PR itself.
5. Code Owners will be notified of PR and if all's well, merge to main.
6. Ensure changes are reflected on the widget. It may take awhile for changes to take place.

## Code Owners

Every json file will have owner(s) assigned so that PRs with changes to a particular file will automatically assign owner(s) as reviewers.

For e.g if John is owner of `/products-details/test.json` then if a PR contains changes to `/products-details/test.json`, John will automatically be assigned as reviewer.

Details of code owners can be viewed in `CODEOWNERS` file. By default, if any changes to files outside of `/products-details/` folder were to happen, Dev Portal team will be the reviewer.

To learn more on how `CODEOWNERS` in github work check out [this link](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

## Recommended Practices for Editing Product Details

Coming soon.

