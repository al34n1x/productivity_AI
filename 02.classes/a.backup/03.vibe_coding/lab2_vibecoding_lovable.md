# Building a mobile-ready eLearning platform - (Prompt Engineering)

In this lab, you’ll build a sleek, responsive eLearning web application using Lovable, a developer assistant designed to help you scaffold high-quality apps fast. Your mission is to create an educational platform focused on delivering AI-focused learning content, with a clean layout, seamless mobile experience, and intuitive course progression.

Inspired by platforms like Udemy and O'Reilly, you'll focus on:

- Modern frontend architecture (React, Tailwind, TypeScript, shadcn/ui)

- A beautiful, minimalist design inspired by Apple.com

- Features learners expect: course pages, video lessons, progress tracking, and mobile-first UX

By the end of this lab, you'll have a fully structured web app foundation that can be extended with real content, user auth, and backend logic — ready for deployment or customization.

Whether you're building a personal learning platform, an internal training tool, or a public course marketplace, this lab gives you the perfect starting point.

Let’s build something people will love to learn with. 🚀

## Role/Profession  
Frontend Developer

## Project Description

### Overview  
We are building a **responsive AI education web app** designed to deliver a high-quality learning experience across devices. The platform should support exploring courses, watching video lessons, tracking learning progress, and engaging with interactive activities. The tone and UX should be clean and professional like O'Reilly or Udemy, but built for speed and responsiveness.

### Tech Stack  
- **React.js** (frontend)  
- **Vite.js** (dev server)  
- **Tailwind CSS** for styling  
- **TypeScript**  
- **shadcn/ui** for UI components  

### Core Features  

#### 🌐 Frontend Routes  
- `/dashboard` – Personalized learner dashboard  
- `/courses` – Grid of all AI courses  
- `/courses/:id` – Course detail page with lessons list, description, and enroll/play options  
- `/lessons/:id` – Lesson player with video, transcript, and code examples  
- `/track` – Visual progress tracker: enrolled courses, completed lessons  
- `/settings` – User preferences: dark mode, email prefs, etc.  
- `/` should redirect to `/dashboard`

#### 🧭 Global UI Elements  
- **Top navigation bar** with links to: Dashboard, Courses, Track Progress, Settings  
- **Mobile hamburger menu** for smaller screens  
- **Breadcrumbs** beneath the navbar to indicate current position  
- **Dark mode toggle** stored in localStorage  
- **Auth placeholder components** (login/logout buttons, mock user avatar)

#### 📊 Dashboard  
- Welcome message and progress summary  
- Resume learning card (last lesson viewed)  
- Suggestions: “Courses to explore next,” based on interests

#### 🎓 Courses Index  
- Responsive **grid of course cards**:  
  - Course title  
  - Instructor  
  - Duration  
  - Difficulty badge  
  - Thumbnail  
  - “Enroll” or “Continue” button  
- Add **category filters** (e.g. ML, NLP, LLMs, Ethics)

#### 🧠 Course Detail  
- Cover image or thumbnail  
- Course title + description  
- Instructor bio  
- List of lessons with time estimates and completion status  
- “Enroll Now” or “Continue Course” CTA button  
- Optional: tags (e.g., beginner, GenAI, Python)

#### 🎬 Lesson View  
- Embedded **video player** (YouTube, Vimeo, or dummy video for now)  
- Scrollable **lesson transcript** with timestamps  
- Code snippets or exercises  
- "Mark as complete" button  
- Next/Previous lesson nav  

#### 📈 Track Progress  
- Timeline or checklist of completed lessons  
- Progress bars per course  
- Summary metrics: lessons watched, hours learned, % complete

#### ⚙️ Settings  
- Toggle dark/light mode  
- Update name/email (no real backend required)  
- “Clear Progress” button with confirmation dialog ("Type 'erase my data'")

### UI & UX Goals  
- **Fully mobile-responsive** using Tailwind breakpoints  
- **Clean and readable interface**, modern academic design  
- Use **shadcn/ui** for: cards, buttons, progress bars, modal dialogs, and dropdowns  
- Smooth transitions and hover/focus states  
- Prioritize accessibility (semantic HTML, focus indicators)

### Bonus Features (Optional)  
- Save user state (progress, theme) in localStorage  
- Placeholder for **search bar** (search by title or tag)  
- Add “Recommended for You” engine (basic logic or dummy data)  
- Easter egg on logo click: “You discovered the secret lab!”

### Deliverables  
- All routes scaffolded with example content  
- Reusable components: CourseCard, LessonPlayer, NavBar, ProgressTracker  
- Fully functional responsive layout  
- Sorting and filtering on courses page  
- Starter README and dev instructions (optional)

---
[⬅ Back to Course Home](../../README.md)