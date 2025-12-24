---
agent: build
description: Update file header comments with input/output/pos declarations
---
The user has requested to update the file header documentation. Follow the instructions below. If you're not sure or if ambiguous, ask for clarification from the user.
<UserRequest>
  $ARGUMENTS
</UserRequest>
<!-- FILE_UPDATE:START -->
**Purpose**
Update the header comments in a specific file with input/output/pos declarations following the Layer 3 documentation standard.

**Steps**
Track these steps as TODOs and complete them one by one.
1. Identify the target file from the user's request
2. Read the file to understand its content and purpose
3. Determine the file type (TypeScript, JavaScript, Markdown, etc.)
4. Analyze the file to identify:
   - Dependencies (external imports, referenced files)
   - What the file provides (exports, functions, classes, components)
   - Role in the system (position in documentation hierarchy)
5. Update the file header with appropriate comment format:
   - For `.ts/.js` files: Use `/** ... */` block comment format
   - For `.md` files: Use `<!-- ... -->` HTML comment format
   - Include `@input`, `@output`, and `@pos` declarations
6. Verify the header accurately reflects the file's current state

**Reference**
- Use `docs/templates/file-header.ts.template` for TypeScript/JavaScript files
- Use `docs/templates/file-header.md.template` for Markdown files
- Header format:
  - `@input`: Dependencies and external references
  - `@output`: What the file exports or provides
  - `@pos`: Role in the system/architecture
<!-- FILE_UPDATE:END -->
