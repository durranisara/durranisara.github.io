---
layout: homepage
---

<style>
.menu-tabs {
  margin-bottom: 25px;
}

.tab-btn {
  padding: 8px 14px;
  margin-right: 6px;
  border: none;
  background: #eee;
  cursor: pointer;
  font-weight: 500;
}

.tab-btn.active {
  background: #333;
  color: #fff;
}

.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
}
</style>

<div class="menu-tabs">
  <button class="tab-btn active" onclick="openTab(event, 'about')">About</button>
  <button class="tab-btn" onclick="openTab(event, 'research')">Research</button>
  <button class="tab-btn" onclick="openTab(event, 'education')">Education</button>
  <button class="tab-btn" onclick="openTab(event, 'news')">News</button>
  <button class="tab-btn" onclick="openTab(event, 'publications')">Publications</button>
  <button class="tab-btn" onclick="openTab(event, 'experience')">Experience</button>
</div>

<div id="about" class="tab-content active">

## About Me

Hi, my name is Sara Durrani, an AI researcher with a strong focus on large language models, natural language processing, and multimodal learning. My work centers on building robust and scalable AI systems that perform effectively across languages, domains, and low-resource settings. I am particularly interested in addressing challenges such as data scarcity, class imbalance, and cross-lingual transfer, with real-world applications in areas including social media analysis, healthcare, and public safety.

I completed my Master’s degree in Computer Science from the [National University of Computer and Emerging Sciences (FAST-NUCES)](https://www.nu.edu.pk/), Pakistan, ranked #1 nationally for Computer Science. My research focused on speech affect and emotion recognition in low-resource languages, with a strong emphasis on Urdu. During my thesis, I worked on transfer learning, deep neural networks, and multimodal representations, which later expanded into research on cross-lingual sentiment analysis, threat detection, and multimodal fake-news detection using transformer-based and LLM-driven models.

I have over five years of teaching experience as a Lecturer in Artificial Intelligence and Computer Science, having taught at [Bahria University](https://bahria.edu.pk/) and [Capital University of Science and Technology](https://cust.edu.pk/).
</div>

<div id="research" class="tab-content">

## Research Interests

- **NLP & LLMs:** Cross-lingual and low-resource NLP, threat detection, domain adaptation, robustness, and calibration  
- **Vision–Language Models:** CLIP-based representation learning, multimodal fake news detection, zero-shot learning  
- **Speech & Multimodal AI:** Speech emotion recognition, multimodal fusion, low-resource learning
</div>

<div id="education" class="tab-content">

## Education

**National University of Computer & Emerging Sciences (FAST-NUCES), Islamabad, Pakistan**  
**MS in Computer Science** | 2019 – 2021  
- Coursework: Machine Learning, NLP, Speech Processing, Computer Vision  

**University of Engineering and Technology (UET), Lahore, Pakistan**  
**BS in Computer Science** | 2015 – 2019  
- Coursework: Artificial Intelligence, Machine Learning, Data Structures, NLP
</div>

<div id="news" class="tab-content">

## News

I am currently working on cross-lingual large language models to develop AI systems that can understand and operate across multiple languages and low-resource settings, and I am actively seeking PhD opportunities. Feel free to contact me.
</div>

<div id="publications" class="tab-content">
{% include_relative _includes/publications.md %}
</div>

<div id="experience" class="tab-content">
{% include_relative _includes/experiences.md %}
</div>

<script>
function openTab(evt, tabId) {
  const contents = document.querySelectorAll('.tab-content');
  const buttons = document.querySelectorAll('.tab-btn');

  contents.forEach(c => c.classList.remove('active'));
  buttons.forEach(b => b.classList.remove('active'));

  document.getElementById(tabId).classList.add('active');
  evt.currentTarget.classList.add('active');
}
</script>
