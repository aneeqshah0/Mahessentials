**Mahessentials Shopify Theme**

This repository handles the versioning of Eahessentials Shopify theme. GitFlow is enforced on this repository

**Branches And Workflow**

Each theme or theme copy in Shopify is a branch on this repository.

**Main Branch**

This branch must be treated carefully, no work is done directly on this branch, the only way to update it is via gitflow releases. Any change here is inmediately reflected on the live Shopify store. This branch receives pushes also from a bot that tries to commit any changes that are done in the theme files by apps and humans. A perfect example is GemPages.

**Feature Branches**

Every time a new theme development is needed, a feature branch will be created from the Main branch with the name feature/<feature_name>. The developer taking care of the feature can create a Shopify theme synced with this branch to test partial progress of the feature. Only when a feature is finished and is working properly is that it can be merged to the ain branch and deleted.

**Release Branches**

After testing in PreProduction, the new features are moved to the Main branch via Gitflow releases. A release branch must be named release/<name_of_the_release> and it is then merged to the Main branch.

**Hotfix Branches**

Gitflow hotfixes are meant to bring commits from Shopify's bot and performing actual small critical hotfixes (this last case should always be avoided, but it can happen). Hotfix branches must be called hotfix/<name_of_the_hotfix> and after finished it should be merged to the Main branch.
