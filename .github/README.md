# GitHub Labels and Milestones

This directory contains configuration files for managing GitHub labels and milestones as code.

## Files

- **labels.yml** - Defines all repository labels with colors and descriptions
- **milestones.yml** - Defines epic milestones for project management

## Using Labels

### Syncing Labels to GitHub

You can sync these labels to your GitHub repository using several methods:

#### Method 1: GitHub Label Sync (Recommended)
```bash
# Install github-label-sync
npm install -g github-label-sync

# Sync labels (requires GitHub personal access token)
github-label-sync --access-token $GITHUB_TOKEN PresidentAnderson/rubiconsoft.net --labels .github/labels.yml
```

#### Method 2: GitHub CLI
```bash
# Using gh CLI to create labels
gh label create "type: bug" --color "d73a4a" --description "Something isn't working"
# Repeat for each label...
```

#### Method 3: Manual Upload
You can also manually create these labels through the GitHub UI at:
`https://github.com/PresidentAnderson/rubiconsoft.net/labels`

### Label Categories

- **Type Labels** - Categorize the type of issue (bug, enhancement, documentation, etc.)
- **Priority Labels** - Indicate urgency (critical, high, medium, low)
- **Status Labels** - Track issue state (blocked, in progress, review needed, on hold)
- **Epic Labels** - Group related issues into larger initiatives
- **Size Labels** - Estimate effort required (XS, S, M, L, XL)
- **Special Labels** - Standard GitHub labels (good first issue, help wanted, etc.)

## Using Milestones

### Creating Milestones

#### Using GitHub CLI
```bash
# Create a milestone
gh api repos/PresidentAnderson/rubiconsoft.net/milestones \
  -f title="Epic: Initial Launch" \
  -f description="Complete the initial launch of rubiconsoft.net platform" \
  -f state="open"
```

#### Using GitHub UI
Navigate to: `https://github.com/PresidentAnderson/rubiconsoft.net/milestones/new`

### Epic Milestones Included

1. **Epic: Initial Launch** - Foundation work for going live
2. **Epic: Infrastructure Setup** - Core infrastructure and DevOps
3. **Epic: User Experience Enhancement** - UI/UX improvements
4. **Epic: Feature Development Phase 1** - Core features
5. **Epic: Feature Development Phase 2** - Advanced features
6. **Epic: Marketing & Growth** - Marketing initiatives
7. **Epic: Documentation & Support** - Documentation and support systems
8. **Epic: Testing & Quality Assurance** - Comprehensive testing
9. **Epic: Beta Release** - Beta testing and refinement
10. **Epic: Production Release v1.0** - Official v1.0 release

## Workflow

1. **Create Issues** - Create issues for specific tasks
2. **Apply Labels** - Categorize with type, priority, size labels
3. **Associate with Epic** - Add epic label and/or assign to epic milestone
4. **Track Progress** - Use status labels to track work
5. **Close Issues** - Close when complete, milestone tracks overall progress

## Automation

Consider setting up GitHub Actions to:
- Auto-label PRs based on changed files
- Sync labels from this configuration
- Update milestone progress
- Send notifications on milestone completion

## Example Issue

```markdown
Title: Implement user authentication
Labels: type: enhancement, priority: high, epic: backend, size: L
Milestone: Epic: Feature Development Phase 1

Description:
Implement OAuth2-based user authentication...
```

## Maintenance

- Review and update labels quarterly
- Archive completed milestones
- Create new epic milestones as project evolves
- Keep this documentation in sync with changes
