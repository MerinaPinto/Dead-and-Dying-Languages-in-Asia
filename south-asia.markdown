---
layout: default
title: South Asia
permalink: /south-asia/
---

<div class="language-buttons">

<button onclick="openLanguage('seke')">Seke</button>
<button onclick="openLanguage('pangkhua')">Pangkhua</button>
<button onclick="openLanguage('lhokpu')">Lhokpu</button>
<button onclick="openLanguage('bo')">Bo</button>
<button onclick="openLanguage('sanskrit')">Sanskrit</button>

</div>

<!-- FULLSCREEN MODAL -->
<div id="language-modal" class="modal">

  <div class="modal-content">

    <span class="close" onclick="closeLanguage()">&times;</span>

    <h2 id="slide-title"></h2>
    <p id="slide-content"></p>

    <div class="nav-buttons">
      <button onclick="previousSlide()">←</button>
      <button onclick="nextSlide()">→</button>
    </div>

  </div>
</div>

<script>

const languages = {
  seke: [
    {
      title: "Seke",
      content: "Region: Nepal (South Asia)"
    },
    {
      title: "Origin",
      content: "Seke, also called Serake, is a highly endangered language spoken in Nepal's Upper Mustang region. Local traditions describe it as the 'golden language.'"
    },
    {
      title: "Community",
      content: "Only about 700 speakers remain across five villages in Upper Mustang."
    }
  ],

  pangkhua: [
    {
      title: "Pangkhua",
      content: "Region: Bangladesh, India, Myanmar"
    },
    {
      title: "Origin",
      content: "Pangkhua is a Sino-Tibetan language preserved through oral tradition."
    },
    {
      title: "Community",
      content: "About 2,500 speakers remain, mostly in Rangamati region."
    }
  ],

  lhokpu: [
    {
      title: "Lhokpu",
      content: "Region: Bhutan"
    },
    {
      title: "Origin",
      content: "Closely tied to western Bhutan geography and history."
    },
    {
      title: "Community",
      content: "Around 2,500 speakers remain."
    }
  ],

  bo: [
    {
      title: "Bo",
      content: "Region: Andaman Islands"
    },
    {
      title: "Origin",
      content: "One of the oldest Great Andamanese languages."
    },
    {
      title: "Community",
      content: "Extinct since 2010."
    }
  ],

  sanskrit: [
    {
      title: "Sanskrit",
      content: "Region: South Asia"
    },
    {
      title: "Origin",
      content: "One of the oldest Indo-Aryan languages (Vedic Sanskrit ~1500 BCE)."
    },
    {
      title: "Community",
      content: "Still studied in religion, philosophy, and education."
    }
  ]
};

let currentLanguage = [];
let currentSlide = 0;

function openLanguage(lang) {
  currentLanguage = languages[lang];
  currentSlide = 0;
  document.getElementById("language-modal").style.display = "block";
  showSlide();
}

function closeLanguage() {
  document.getElementById("language-modal").style.display = "none";
}

function showSlide() {
  document.getElementById("slide-title").innerText =
    currentLanguage[currentSlide].title;

  document.getElementById("slide-content").innerText =
    currentLanguage[currentSlide].content;
}

function nextSlide() {
  if (currentSlide < currentLanguage.length - 1) {
    currentSlide++;
    showSlide();
  }
}

function previousSlide() {
  if (currentSlide > 0) {
    currentSlide--;
    showSlide();
  }
}

</script> 