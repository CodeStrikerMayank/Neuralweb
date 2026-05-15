# Design Document: Student AI/ML & Data Science Hub

## 1. Objective
Build a modern, interactive project browser for the Student AI/ML Hub that allows users to discover, search, and filter student-led projects across all repository categories.

## 2. Visual Style: "Modern App Portfolio"
- **Aesthetic**: Sleek dark mode (default) with a high-contrast light mode toggle.
- **Components**: 
  - Glassmorphism effects on cards and navigation.
  - Smooth CSS transitions for filtering and hover states.
  - Responsive grid layout (1 column mobile, 3+ columns desktop).
  - Lucide-style iconography for categories.

## 3. Tech Stack
- **Structure**: Semantic HTML5.
- **Styling**: Vanilla CSS3 using CSS Custom Properties (Variables) for theming. No external CSS frameworks (Tailwind/Bootstrap) to keep it lightweight.
- **Logic**: Vanilla JavaScript (ES6+).
- **Data**: External `projects.json` for easy updates.

## 4. Features & Components
### A. Hero Section
- Bold heading: "Student AI/ML & Data Science Hub"
- Subtext: "A community-run library of projects built by students, for students."
- Primary CTA: "Submit Your Project" (Link to the contribution guide).

### B. Search & Filter System
- **Global Search**: Real-time search by project name, author, or tech stack.
- **Category Tabs**: Toggle between "All", "AI & ML", and "Data Science".
- **Sub-category Pills**: Deep dive into specific topics (e.g., "NLP", "Time Series").

### C. Project Grid (Dynamic)
Each card will include:
- **Title**: Link to the project's sub-folder.
- **Category Badge**: Color-coded by repository type.
- **Tags**: Tech stack used (e.g., `Python`, `PyTorch`, `Scikit-learn`).
- **Description**: Concise 1-2 sentence overview.
- **Author**: Link to the contributor's GitHub profile.

### D. Communication Channels (Social Nodes)
- Integrated video backgrounds for interactive social link cards.
- **Nodes**: Discord (Community), GitHub (Source), WhatsApp (Direct Bridge).
- **Styling**: Cyberpunk-inspired glassmorphism with video loops.

### E. 'How to Contribute' Section
- A visually distinct section at the bottom explaining the 3-step PR process:
  1. Pick a category repo.
  2. Fork and add your folder to `/projects`.
  3. Open a Pull Request.

### F. Theme Toggle
- A simple button to switch between "Midnight AI" (Dark) and "Clean Lab" (Light) themes.

## 5. Data Schema (`projects.json`)
```json
[
  {
    "id": "iris-classifier",
    "name": "Iris Flower Classifier",
    "author": "example-student",
    "author_url": "https://github.com/example",
    "category": "supervised-learning",
    "parent_section": "AI & ML",
    "description": "A comparison of KNN and SVM classifiers on the Iris dataset.",
    "stack": ["Python", "Scikit-learn", "Jupyter"],
    "url": "../ai-ml/supervised-learning/projects/example-project/README.md"
  }
]
```

## 6. Implementation Plan
1. **Initialize Data**: Create `projects.json` with the existing "Example Project".
2. **Setup HTML Structure**: Define the shell in `index.html`.
3. **Draft CSS**: Implement the design system and responsive grid.
4. **JS Logic**: Write the fetch and filter engine.
5. **Final Polish**: Add animations and verify responsive behavior.
