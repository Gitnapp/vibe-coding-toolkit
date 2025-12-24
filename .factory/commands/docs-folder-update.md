---
description: Update FOLDER.md documentation for a specific directory
argument-hint: directory-path
---
<!-- FOLDER_UPDATE:START -->
**Purpose**
Update the FOLDER.md file in a specified directory to reflect current folder contents and architecture.

**Steps**
Track these steps as TODOs and complete them one by one.
1. Identify the target directory from the user's request or current working directory
2. List all files in the directory to understand the current structure
3. Read the existing FOLDER.md if it exists
4. Analyze each file to determine its role (Core, Util, Type, Export, Config, etc.) and function
5. Update the FOLDER.md with:
   - Folder name in the header
   - 3-line architecture description (purpose, patterns/technologies, relationships)
   - Complete file list table with accurate roles and functions
6. Verify the file list is complete and up-to-date

**Reference**
- Use `docs/templates/FOLDER.template.md` as the template format
- Architecture section should be exactly 3 lines max
- File roles: Core, Util, Type, Export, Config, Test, Doc, Asset, etc.

$ARGUMENTS
<!-- FOLDER_UPDATE:END -->
