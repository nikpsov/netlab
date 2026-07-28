---
title: "📝 Obsidian и ведение заметок"
tags: ["obsidian", "workflow"]
---

# 📝 Ведение заметок в Obsidian

Вы можете удобно составлять материалы в Obsidian и выгружать их на данный сайт Hextra.

---

## 🎨 Выноски (Callouts) в Hextra

Тема Hextra поддерживает стильные выноски:

{{< callout type="info" >}}
**Информация:** Выноска подсвечивается синим цветом.
{{< /callout >}}

{{< callout type="warning" >}}
**Предупреждение:** Выноска подсвечивается желтым цветом.
{{< /callout >}}

---

## 📊 Диаграммы Mermaid

Hextra поддерживает визуализацию Mermaid из коробки:

```mermaid
graph TD
    A[Obsidian Notes] -->|git push| B[GitHub Repo netlab]
    B -->|GitHub Actions| C[Hugo Build with Hextra]
    C -->|Deploy| D[GitHub Pages Site]
```
