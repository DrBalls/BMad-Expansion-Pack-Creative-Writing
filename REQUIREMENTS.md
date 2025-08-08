# Requirements & Dependencies

## System Requirements

### BMad Method Core
- **Version**: BMad Method v1.0 or higher
- **Installation**: Must have BMad Method installed and configured

### Runtime Environment
- **Node.js**: v14.0 or higher
- **Operating System**: Windows, macOS, or Linux
- **Memory**: 4GB RAM minimum (8GB recommended for large manuscripts)

## Dependencies

### Core Dependencies
This expansion pack requires only the BMad Method core framework. No additional npm packages or external dependencies are needed.

### LLM Requirements
- Compatible with any LLM provider configured in BMad Method
- Optimal performance with:
  - GPT-4 or GPT-4 Turbo
  - Claude 2 or Claude 3
  - Local models with 13B+ parameters

### Token Considerations
- **Novel workflows**: May consume 50k-100k tokens per complete session
- **Character development**: ~5k-10k tokens per character
- **Beta reading**: ~20k-30k tokens per manuscript review
- **Editing passes**: ~15k-25k tokens per chapter

## File System Requirements

### Directory Structure
The expansion pack expects the standard BMad Method directory structure:
```
bmad-method/
├── expansion-packs/
│   └── bmad-creative-writing/
├── .bmad-core/
├── docs/
└── package.json
```

### Storage Space
- **Installation**: ~2MB for expansion pack files
- **Working space**: 10-50MB per active project
- **Document storage**: Varies by manuscript size

## Compatibility

### BMad Agent Compatibility
- Fully compatible with all BMad core agents
- Can be combined with other expansion packs
- No conflicts with existing BMad workflows

### File Format Support
- **Input**: Markdown (.md), Plain text (.txt), YAML (.yaml)
- **Output**: Markdown (.md), YAML (.yaml)
- **Templates**: YAML format required

### Integration Points
- VSCode/Cursor IDE integration via BMad Method
- Git version control for manuscript tracking
- Export to standard formats for publishing platforms

## Optional Enhancements

### Recommended Tools
While not required, these tools enhance the experience:
- **Markdown editor**: For better manuscript viewing
- **Git**: For version control of your writing
- **Pandoc**: For converting to other formats (DOCX, PDF, EPUB)

### Publishing Platforms
The expansion pack generates content compatible with:
- Amazon KDP (Kindle Direct Publishing)
- Draft2Digital
- IngramSpark
- Smashwords
- Traditional submission formats

## Limitations

### Known Constraints
- Maximum file size: 10MB per document
- Character limit: 500,000 characters per file
- Concurrent workflows: Limited by system memory

### Not Supported
- Real-time collaborative editing
- Direct API integration with publishing platforms
- Automated copyright registration
- Audio/video content generation

## Troubleshooting

### Common Issues

**Expansion pack not appearing in installer:**
- Ensure pack is in `expansion-packs/bmad-creative-writing/`
- Verify `config.yaml` exists and is valid YAML
- Check BMad Method version compatibility

**Agent activation failures:**
- Confirm all agent files are in `agents/` directory
- Verify markdown formatting in agent files
- Check for file permission issues

**Workflow errors:**
- Ensure all referenced templates exist
- Verify YAML syntax in workflow files
- Check task dependencies are present

### Support Resources
- GitHub Issues: https://github.com/DrBalls/BMad-Expansion-Pack-Creative-Writing/issues
- BMad Method Docs: https://github.com/bmadcode/BMAD-METHOD/docs
- Community Forum: [BMad Method Discussions]

## Future Requirements

### Planned Features (May Require Updates)
- Multi-author collaboration support
- Real-time grammar checking integration
- Direct publishing API connections
- AI voice narration for audiobooks
- Translation workflow support

### Version Compatibility
This expansion pack will maintain compatibility with:
- BMad Method 1.x releases
- Future 2.x releases (with migration guide)
- LTS (Long Term Support) versions