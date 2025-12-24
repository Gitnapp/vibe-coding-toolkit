---
inclusion: always
---

# Documentation Maintenance Rules

This steering file defines the documentation update workflow for the three-layer documentation system.

## Update Trigger Conditions

### When to Update File Headers
- **Interface changes**: When a file's input dependencies or output exports change
- **Role changes**: When a file's position/responsibility in the system changes
- **New dependencies**: When new imports are added or removed

### When to Update FOLDER.md
- **File added**: New file created in the folder
- **File removed**: Existing file deleted from the folder
- **File renamed**: File name changed
- **Architecture change**: Folder's core responsibility or patterns changed

### When to Update Root Documents
- **Structural changes**: New folders added to the architecture
- **Documentation index**: New documentation files created
- **Global rules**: Changes to project-wide conventions

## Documentation Format Requirements

### File Header Format (TypeScript/JavaScript)
```typescript
/**
 * @input  依赖: [外部依赖列表]
 * @output 提供: [对外提供的接口/功能]
 * @pos    定位: [在系统中的角色]
 * 
 * 一旦本文件被更新，务必更新本文件头部注释及所属文件夹的 FOLDER.md
 */
```

### FOLDER.md Format
```markdown
# [Folder Name]

> 一旦本文件夹有所变化，请更新本文件。

## Architecture (3 lines max)
[Line 1: 模块职责]
[Line 2: 核心模式/技术]
[Line 3: 与其他模块的关系]

## Files

| File | Role | Function |
|------|------|----------|
| `file.ts` | Core/Util/Export/Type/Test/Config | 功能描述 |
```

## Agent Workflow Integration

### After ANY Code Modification
1. **Check file header**: Ensure input/output/pos comments are accurate
2. **Check FOLDER.md**: Ensure file list matches actual files
3. **Check root docs**: Update if architecture changed

### Validation Checklist
- [ ] File header contains @input, @output, @pos
- [ ] File header contains update trigger statement
- [ ] FOLDER.md architecture ≤ 3 lines
- [ ] FOLDER.md file list matches actual files
- [ ] Root document links are valid

### Update Chain
```
File Modified → Update File Header → Update FOLDER.md → Update Root Docs (if needed)
```

## Templates Location

Templates are located at: `docs/templates/`
- `FOLDER.template.md` - Folder README template
- `file-header.ts.template` - TypeScript header template
- `file-header.md.template` - Markdown header template
