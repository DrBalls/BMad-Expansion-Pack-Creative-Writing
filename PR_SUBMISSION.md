# Pull Request Submission Guide

## Preparing Your Fork for BMad Method PR

### 1. Fork the BMad Method Repository
```bash
# Fork https://github.com/bmadcode/BMAD-METHOD on GitHub
# Then clone your fork locally
git clone https://github.com/YOUR-USERNAME/BMAD-METHOD.git
cd BMAD-METHOD
```

### 2. Add Your Expansion Pack
```bash
# Create the expansion pack directory
mkdir -p expansion-packs/bmad-creative-writing

# Copy your expansion pack files (excluding .git, .bmad-core, .claude)
cp -r /path/to/BMad-Expansion-Pack-Creative-Writing/* \
     expansion-packs/bmad-creative-writing/

# Remove any files that shouldn't be in the main repo
rm -rf expansion-packs/bmad-creative-writing/.git
rm -rf expansion-packs/bmad-creative-writing/.bmad-core
rm -rf expansion-packs/bmad-creative-writing/.claude
rm expansion-packs/bmad-creative-writing/.DS_Store
rm expansion-packs/bmad-creative-writing/PR_SUBMISSION.md
```

### 3. Verify Structure
Your expansion pack should have this structure in the BMad repo:
```
expansion-packs/
└── bmad-creative-writing/
    ├── config.yaml
    ├── package.json
    ├── README.md
    ├── agent-teams/
    │   └── agent-team.yaml
    ├── agents/
    │   ├── beta-reader.md
    │   ├── book-critic.md
    │   ├── character-psychologist.md
    │   ├── cover-designer.md
    │   ├── dialog-specialist.md
    │   ├── editor.md
    │   ├── genre-specialist.md
    │   ├── narrative-designer.md
    │   ├── plot-architect.md
    │   └── world-builder.md
    ├── checklists/
    │   └── [27 checklist files]
    ├── data/
    │   └── story-structures.md
    ├── tasks/
    │   └── [22 task files]
    ├── templates/
    │   └── [8 template files]
    └── workflows/
        └── [8 workflow files]
```

### 4. Create Feature Branch
```bash
git checkout -b add-creative-writing-expansion
git add expansion-packs/bmad-creative-writing/
git commit -m "Add Creative Writing expansion pack

- 10 specialized writing agents for fiction and narrative design
- 8 complete workflows (novel, screenplay, short story, series)
- 27 quality checklists for genre and technical validation
- 22 writing tasks covering full creative process
- 8 professional templates for structured writing
- KDP publishing integration support"
```

### 5. Push and Create PR
```bash
git push origin add-creative-writing-expansion
```

Then on GitHub:
1. Go to your fork
2. Click "Pull requests" → "New pull request"
3. Set base repository: `bmadcode/BMAD-METHOD` base: `main`
4. Set head repository: `YOUR-USERNAME/BMAD-METHOD` compare: `add-creative-writing-expansion`

### 6. PR Template

**Title:** Add Creative Writing Expansion Pack

**Description:**
```markdown
## Summary
This PR adds a comprehensive Creative Writing expansion pack to BMad Method, providing specialized AI agents and workflows for fiction writers, screenwriters, and narrative designers.

## What's Included
- **10 Specialized Agents**: Plot Architect, Character Psychologist, World Builder, Editor, Beta Reader, Dialog Specialist, Narrative Designer, Genre Specialist, Book Critic, Cover Designer
- **8 Workflows**: Novel writing (3 variants), screenplay development, short story creation, series planning, book cover design
- **27 Quality Checklists**: Genre-specific (fantasy, sci-fi, romance, etc.) and technical (plot structure, continuity, publishing)
- **22 Writing Tasks**: Complete creative process from brainstorming to publishing
- **8 Templates**: Character profiles, story outlines, world guides, scene lists, and more

## Testing
- [x] Verified config.yaml format matches existing expansion packs
- [x] Tested agent activation and commands
- [x] Validated workflow execution
- [x] Confirmed all file paths are correct
- [x] No external dependencies required

## Use Cases
- Novel development from premise to publication-ready manuscript
- Screenplay writing with industry-standard formatting
- Series planning with continuity management
- Self-publishing preparation (KDP integration)

## Documentation
Complete README included with installation instructions, usage examples, and component descriptions.

## Author
Created by @DrBalls (Wes) for the BMad Method community.
```

### 7. Post-PR Checklist
- [ ] Monitor PR for feedback
- [ ] Address any requested changes
- [ ] Update documentation if needed
- [ ] Test in main repo after merge

## Alternative: Standalone Repository

If you prefer to maintain your expansion pack as a standalone installable:

1. Keep your repository at: https://github.com/DrBalls/BMad-Expansion-Pack-Creative-Writing
2. Add installation instructions to your README:
```bash
# Clone the expansion pack
git clone https://github.com/DrBalls/BMad-Expansion-Pack-Creative-Writing.git

# Copy to your BMad installation
cp -r BMad-Expansion-Pack-Creative-Writing/* \
     ~/bmad-method/expansion-packs/bmad-creative-writing/

# Run BMad installer
cd ~/bmad-method
npm run install:bmad
```

## Support

For questions about the submission process:
- Open an issue in the BMad Method repository
- Tag @bmadcode for expansion pack reviews
- Join the BMad community discussions