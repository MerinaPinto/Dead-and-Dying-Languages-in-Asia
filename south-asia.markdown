---
layout: default
title: South Asia
permalink: /south-asia/
---

# South Asia

<p>Select a language to learn more.</p>

<div class="language-buttons">

<button onclick="openLanguage('seke')">Seke</button>

<button onclick="openLanguage('pangkhua')">Pangkhua</button>

<button onclick="openLanguage('lhokpu')">Lhokpu</button>

<button onclick="openLanguage('bo')">Bo</button>

<button onclick="openLanguage('sanskrit')">Sanskrit</button>

</div>

<div id="language-modal" class="modal">

<div class="modal-content">

<span class="close" onclick="closeLanguage()">&times;</span>

<h2 id="slide-title"></h2>

<p id="slide-content"></p>

<button onclick="previousSlide()">Previous</button>

<button onclick="nextSlide()">Next</button>

</div>

</div>

<script>

const languages = {

seke: [
{
title: "Seke",
content: "Region: South Asia (Nepal)"
},
{
title: "Origin",
content: "Seke, also called Serake, is a highly endangered language spoken in Nepal's Upper Mustang region. Local traditions describe it as the golden language. According to a Buddhist legend, the language originated with people who lived in the Himalayan mountains before settling in Mustang."
},
{
title: "Community",
content: "The Seke language is spoken in five villages in Upper Mustang. Only about 700 speakers remain, making it one of Nepal's most endangered languages."
}
],

pangkhua: [
{
title: "Pangkhua",
content: "Region: South Asia (Bangladesh)"
},
{
title: "Origin",
content: "Pangkhua is a Sino-Tibetan language spoken in southeastern Bangladesh, India, and Myanmar. The language has traditionally been preserved through oral communication."
},
{
title: "Community",
content: "Approximately 2,500 people speak Pangkhua. Folk songs, stories, and oral traditions help preserve the community's history and traditions."
}
],

lhokpu: [
{
title: "Lhokpu",
content: "Region: South Asia (Bhutan)"
},
{
title: "Origin",
content: "Lhokpu is an endangered language spoken by the indigenous Lhokpu people of western Bhutan and is closely tied to the geography of the region."
},
{
title: "Community",
content: "Around 2,500 speakers remain. Oral histories preserve stories of migration, land loss, and major historical events."
}
],

bo: [
{
title: "Bo",
content: "Region: South Asia (Andaman Islands)"
},
{
title: "Origin",
content: "Bo was one of the Great Andamanese languages and was connected to some of the earliest human populations in the Andaman Islands."
},
{
title: "Community",
content: "Bo became extinct in 2010 with the death of Boa Sr, its last fluent speaker."
}
],

sanskrit: [
{
title: "Sanskrit",
content: "Region: South Asia"
},
{
title: "Origin",
content: "Sanskrit is one of the oldest recorded languages of South Asia. Vedic Sanskrit dates back to around 1500 BCE."
},
{
title: "Community",
content: "Although rarely spoken natively today, Sanskrit remains important in religion, literature, philosophy, and education."
}
]

};

let currentLanguage = [];
let currentSlide = 0;

function openLanguage(language) {

currentLanguage = languages[language];

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

if(currentSlide < currentLanguage.length - 1) {

currentSlide++;

showSlide();

}
}

function previousSlide() {

if(currentSlide > 0) {

currentSlide--;

showSlide();

}
}

</script>