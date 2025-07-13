# GitHub Repository Setup Guide

This document provides step-by-step instructions for completing the GitHub repository setup for SuperClaude independence.

## 🎯 Phase 2: GitHub Features Setup

### Step 1: Set Default Branch to `latest`

1. **Navigate to Repository Settings:**
   ```
   https://github.com/luiscamaral/SuperClaude/settings/branches
   ```

2. **Change Default Branch:**
   - Click the pencil icon next to "Default branch"
   - Select `latest` from the dropdown
   - Click "Update"
   - Confirm the change by typing the repository name

3. **Verify Default Branch:**
   - Return to main repository page
   - Confirm it shows `latest` branch by default
   - Test: `git clone` should now default to `latest`

### Step 2: Enable Repository Features

1. **Navigate to Features Section:**
   ```
   https://github.com/luiscamaral/SuperClaude/settings
   ```

2. **Enable Core Features:**
   - ✅ **Issues** - For bug reports and feature requests
   - ✅ **Discussions** - For community Q&A and conversations
   - ✅ **Wikis** (Optional) - For extended documentation
   - ✅ **Projects** (Optional) - For project management

3. **Verify Features:**
   - Issues: `https://github.com/luiscamaral/SuperClaude/issues`
   - Discussions: `https://github.com/luiscamaral/SuperClaude/discussions`

### Step 3: Configure GitHub Discussions

1. **Access Discussions:**
   ```
   https://github.com/luiscamaral/SuperClaude/discussions
   ```

2. **Set Up Discussion Categories:**
   
   Create these categories (GitHub may create some automatically):

   | Category | Type | Description |
   |----------|------|-------------|
   | 💬 **General** | Discussion | General discussions about SuperClaude |
   | 💡 **Ideas** | Discussion | Ideas for new features and improvements |
   | ❓ **Q&A** | Q&A | Questions about usage and configuration |
   | 📚 **Show and Tell** | Discussion | Share workflows and success stories |
   | 🔧 **Setup & Installation** | Q&A | Help with setup and installation |
   | 🤝 **Announcements** | Announcement | Project updates and news |

3. **Create Welcome Discussion:**
   - Create a pinned welcome post
   - Use the content from the plan (welcome message)
   - Pin the discussion for visibility

### Step 4: Configure Issue Labels

1. **Navigate to Labels:**
   ```
   https://github.com/luiscamaral/SuperClaude/labels
   ```

2. **Create Priority Labels:**
   ```
   priority/critical    - #d73a4a (red)
   priority/high        - #e99695 (light red)  
   priority/medium      - #fbca04 (yellow)
   priority/low         - #0e8a16 (green)
   ```

3. **Create Type Labels:**
   ```
   type/bug            - #d73a4a (red)
   type/enhancement    - #a2eeef (blue)
   type/documentation  - #0075ca (dark blue)
   type/question       - #d876e3 (purple)
   ```

4. **Create Component Labels:**
   ```
   component/installer - #f9d0c4 (light orange)
   component/commands  - #c2e0c6 (light green)
   component/personas  - #bfdadc (light blue)
   component/mcp       - #fef2c0 (light yellow)
   ```

### Step 5: Optional Security Settings

1. **Navigate to Security & Analysis:**
   ```
   https://github.com/luiscamaral/SuperClaude/settings/security_analysis
   ```

2. **Enable Security Features:**
   - ✅ **Dependency graph**
   - ✅ **Dependabot alerts**
   - ✅ **Dependabot security updates**
   - ✅ **Secret scanning** (if available)

### Step 6: Branch Protection (Optional)

1. **Navigate to Branch Protection:**
   ```
   https://github.com/luiscamaral/SuperClaude/settings/branches
   ```

2. **Add Protection Rule for `latest`:**
   - Branch name pattern: `latest`
   - ✅ Require a pull request before merging
   - ✅ Require status checks to pass before merging
   - ✅ Include administrators (optional)

## ✅ Verification Checklist

After completing the setup, verify:

- [ ] Default branch is `latest`
- [ ] Issues are enabled and accessible
- [ ] Discussions are enabled with categories
- [ ] Issue templates work correctly
- [ ] PR template targets `latest` branch
- [ ] Repository links work correctly
- [ ] Labels are created and organized

## 📝 Notes

- The repository is already fully configured with templates and documentation
- All links and references point to the correct repository
- Branch strategy is implemented and documented
- Ready for community use once features are enabled

## 🚀 Next Steps

After completing GitHub setup:
1. Create first release (v2.0.1)
2. Test update functionality
3. Announce repository to community