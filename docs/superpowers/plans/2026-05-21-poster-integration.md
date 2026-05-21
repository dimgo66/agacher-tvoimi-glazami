# Poster Integration Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Embed the retro theatrical poster directly under the text of the May 30 announcement on the website in a large, beautiful, responsive format.

**Architecture:** Modify the event card inside `index.html` by inserting a centered `<img>` container styled with Tailwind CSS utility classes and an inline style constraint for optimal sizing across all device sizes.

**Tech Stack:** HTML5, Tailwind CSS, custom inline styles.

---

### Task 1: Integrate Poster Image into index.html

**Files:**
- Modify: `index.html:350-362`

- [ ] **Step 1: Insert the image element under the description text**
  Locate the description paragraph for "Событие 1" in `index.html` (around line 354) and add the centered, styled poster image immediately below it.
  
  Replace:
  ```html
                            <p class="text-gray-300 text-sm">
                                Состоится в 13:00 на Международном книжном фестивале <strong>#читайгомель</strong> (Гомельская областная библиотека им. Ленина). Видео читки будет размещено на официальных каналах Софии Агачер в YouTube и ВК-видео.
                            </p>
  ```
  
  With:
  ```html
                            <p class="text-gray-300 text-sm">
                                Состоится в 13:00 на Международном книжном фестивале <strong>#читайгомель</strong> (Гомельская областная библиотека им. Ленина). Видео читки будет размещено на официальных каналах Софии Агачер в YouTube и ВК-видео.
                            </p>
                            <div class="mt-4 w-full flex justify-center">
                                <img src="assets/poster-gomel.jpg" 
                                     alt="Афиша презентации мюзикла 'Твоими глазами' в Гомеле" 
                                     class="rounded-lg shadow-2xl max-w-full md:max-w-xl lg:max-w-2xl border border-amber-500 border-opacity-30 transition-transform duration-300 hover:scale-[1.01] hover:border-opacity-60" 
                                     style="max-height: 550px; object-fit: contain;">
                            </div>
  ```

- [ ] **Step 2: Verify code correctness and file structure**
  Open the file locally or inspect the changed portion using a tool to make sure all HTML tags are opened and closed correctly, and that Tailwind classes match.

- [ ] **Step 3: Commit the integration**
  Run:
  ```bash
  git add index.html
  git commit -m "feat: add theatrical poster immediately under event description"
  ```

---

### Task 2: Verify Visuals and Responsiveness

- [ ] **Step 1: Verify the changes in a web browser**
  Check the rendering of the updated `index.html` in the Chrome browser, making sure the poster displays beautifully and responsively without vertical distortion. Ensure it is centered and has the gold border and hover micro-animations active.

- [ ] **Step 2: Finalize the work**
  Let the user know that the integration is complete and verify the final result.
