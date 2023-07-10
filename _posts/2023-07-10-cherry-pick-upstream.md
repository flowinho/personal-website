---
layout: post
title: "Einzelne Commits als Pull-Request in ein Upstream-Repository einpflegen"
---

Manchmal ist es notwendig und / oder gewünscht, einzelne Commits als Pull-Request zur Verfügung zu stellen, beispielsweise
wenn gute Änderungen in einem Downstream-Repository ins Upstream-Repository fließen sollen.

Die Herangehensweise ist einfach:

1. Neuen Branch auf Basis des `main`-Branches des Upstream-Repository erstellen.
1. Die gewünschten Commits auf den neuen Branch cherry-picken.
1. Den neuen Branch _in die eigenen Fork_ pushen.
1. Einen Upstream-Pull-Request erstellen.

```bash
git fetch -all
git checkout -b awesome-hotfixes <fork/main>
git cherry-pick <hash>
git cherry-pick <hash>
git push -u origin awesome-hotfixes
```

Danach wie gehabt einen Pull-Requeust eröffnen.
