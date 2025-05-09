---
# You can also start simply with 'default'
theme: Default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

## AltSchool Semester presentation
#

## **Circle 11 Presentation**

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
src: ./pages/welcomePage/welcom.md
---

---
src: ./pages/victor/arrays-bundlers.md
---

---
src: ./pages/samson/functions.md
---

---
src: ./pages/bridget/promises.md
---

---
src: ./pages/ayomide/dom.md
---

---
src: ./pages/teminire/loops.md
---

---
src: ./pages/anita/data-types.md
---

---
src: ./pages/ibukunoluwa/js objects.md
---

---
src: ./pages/edith/conditional-statement.md
---

---
src: ./pages/mujeebat/strings-and-templates.md
---


