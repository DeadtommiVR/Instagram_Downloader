# Instagram Backup and Organization Application

## Objective

This application automatically scrapes your personal Instagram data—including posts, videos, audio tracks, captions, direct messages, saved posts, and historical stories—and organizes them neatly into structured folders according to Instagram categories, embedding metadata directly within media files.

---

## Project Workflow and Steps

### Step 1: Preliminary Data Size Scan

* Authenticate your Instagram account via automation.
* Scan and estimate the total size of your Instagram data (posts, videos, messages, historical stories, and saved content).
* Prompt user to confirm proceeding based on estimated file size.

### Step 2: Specify Download Location

* Prompt the user to choose a directory location on their desktop computer where the Instagram data will be downloaded and organized.

### Step 3: Data Download

* Automatically download Instagram profile content using the `instaloader` library.

### Step 4: Data Organization and Structuring

Upon download, data will be structured as follows:

```
InstagramBackup/
├── Posts
│   ├── Images (metadata embedded: original account name, caption, tagged names, date, category labels)
│   └── Videos (including audio, metadata embedded: original account name, caption, tagged names, date, category labels)
├── Messages
│   ├── Text messages
│   ├── Posts sent (media files with embedded metadata: original account name, caption, tagged names, date, category labels)
│   └── Links shared
├── Saved_Posts
│   ├── Category_Name_1 (Folder name tagged as metadata label)
│   │   └── Media files (metadata embedded: original account name, caption, tagged names, date, category labels)
│   └── Category_Name_2 (Folder name tagged as metadata label)
│       └── Media files (metadata embedded: original account name, caption, tagged names, date, category labels)
├── Historical_Stories (chronologically ordered with audio; metadata embedded: original account name, caption, tagged names, date, category labels)
```

### Step 5: Download Control

* During download:

  * **Pause:** Allow users to temporarily pause and later resume the download.
  * **Cancel:** Allow users to cancel the download at any point, ensuring data integrity for already downloaded files.

---

## Features Summary

* Preliminary file size estimation and user confirmation
* Customizable download location
* Comprehensive automated scraping and organization of Instagram data:

  * Posts, Videos (with audio), Historical Stories (chronologically ordered with audio), Direct Messages (including text messages, shared posts, and links)
  * Saved posts categorized as per Instagram’s original user-defined collections
  * Metadata embedded directly within media files: Original poster's username, caption, tagged names, date, and folder/category labels
* Interactive control during the download process (Pause/Cancel functionality)

---

## User Interaction Flow

1. User runs application.
2. Authentication with Instagram via automation.
3. Application scans and displays estimated download size.
4. User selects destination directory.
5. User confirms or aborts the operation.
6. Data download and organization commence.
7. User can pause or cancel download at any stage.






