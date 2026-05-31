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
#### [placeholder@email.com](mailto:placeholder@email.com)

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
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::
---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Analysis
**Conditions:**
- Pressure: 200kPa
- Temperature: 338K

**Control Chart:**
Monitoring Part Length stability.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m1_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Capability
**Analysis:**
- Distribution vs Spec Limits (48-52).
- Verification of precision at high Temp.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m1_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2 Analysis
**Conditions:**
- Pressure: 200kPa
- Temperature: 338K

**Control Chart:**
Stability check for Machine 2.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m2_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2 Capability
**Analysis:**
- Process capability indices assessment.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m2_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3 Analysis
**Conditions:**
- Pressure: 200kPa
- Temperature: 338K
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m3_control.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3 Capability
**Analysis:**
- Final machine performance verification.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/m3_capability.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---
# Bibliography
<div id="refs"></div>
