# 🚧 Coming Soon

## Planned Features for AI Image Info Pro

---

### 🔄 ComfyUI Workflow Association

**Status:** Planned

**Description:**  
Associate ComfyUI workflow JSON files with your processed images. Each image can have its exact workflow saved alongside it for easy reproduction.

**How it will work:**

1. In the preset form, a new **"ComfyUI Workflow"** section will be added
2. Click **"Add Workflow"** button to browse for a `.json` workflow file
3. When you save the preset, the workflow is copied to your image folder as:
   - `imagename_workflow.json`

**File structure after processing:**
```
📁 Your Image Folder/
├── 🖼️ awesome_character.png
├── 📄 awesome_character_preset.json      (metadata, prompts, settings)
├── 🖼️ awesome_character_thumb.jpg        (thumbnail)
└── 📄 awesome_character_workflow.json    (ComfyUI workflow)   ← NEW
```

**Benefits:**
- Complete reproducibility - reload the exact workflow in ComfyUI
- Workflow travels with the image when you move/share folders
- No more searching for "which workflow made this image?"
- Survives browser cache clears (stored as files)

**Browser Support:**
| Feature | Chrome/Edge | Firefox |
|---------|:-----------:|:-------:|
| Browse for workflow | ✅ | ✅ |
| Auto-save to folder | ✅ | ⬇️ Downloads |
| Load existing workflows | ✅ | ✅ |

**UI Preview:**
```
┌─────────────────────────────────────────────┐
│ ComfyUI Workflow                            │
├─────────────────────────────────────────────┤
│ [No workflow attached]                      │
│                                             │
│ [📁 Add Workflow]  [❌ Remove]              │
└─────────────────────────────────────────────┘
```

---

### 💡 Other Ideas Under Consideration

- **Batch workflow assignment** - Apply the same workflow to multiple images
- **Workflow preview** - Show workflow node count and basic info
- **Workflow categories/tags** - Organize workflows by type
- **Quick workflow swap** - Replace workflow without re-processing

---

*Have a feature request? Open an issue on GitHub!*
