 ---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Control
**I-Chart Analysis:**
- Monitored at 200kPa / 338K.
- Stability assessment of individuals.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m1_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Capability
**Process Capability:**
- Specs: [48, 52]
- Analysis of $\sigma$ variation.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m1_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2 Control
**I-Chart Analysis:**
- Machine 2 performance data.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m2_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2 Capability
**Process Capability:**
- Distribution vs Limits.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m2_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3 Control
**I-Chart Analysis:**
- Data for Machine 3.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m3_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3 Capability
**Process Capability:**
- Professional distribution curve.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m3_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---
# Bibliography
<div id="refs"></div>
