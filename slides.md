---
# try also 'default' to start simple
theme: seriph
browserExporter: true
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  Відділ підтримки програмного забезпечення
# persist drawings in exports and build
drawings:
  persist: false
---

# DreamTeam

<div @click="$slidev.nav.next" class="mt-10 py-1" hover:bg="white op-10">
  Натисніть Space, щоб перейти далі <carbon:arrow-right />
</div>

<Logo position="top-left" size="sm" />


---
src: ./pages/01.md
---

---
src: ./pages/02.md
---

---
src: ./pages/03.md
---

---
src: ./pages/last.md
---
