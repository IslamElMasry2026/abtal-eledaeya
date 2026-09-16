<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>أبطال الإعدادية | منصة تعليمية شاملة للمرحلة الإعدادية</title>
<meta name="description" content="موقع أبطال الإعدادية يقدم أحدث الدروس والمراجعات التعليمية الشاملة لجميع صفوف المرحلة الإعدادية.">
<meta name="keywords" content="أبطال الإعدادية, ابطال الاعدادية, المرحلة الاعدادية, دروس اعدادي, مراجعات اعدادي, اولى اعدادي, ثانية اعدادي, ثالثة اعدادي">
<style>
@import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&family=Markazi+Text:wght@500;600;700&family=Amiri:wght@700&display=swap');

:root{
  --paper:#EEF2F8;
  --paper-dim:#E4EAF3;
  --ink:#132347;
  --ink-soft:#5B6480;
  --rule:#DCE3EF;
  --navy1:#1e3c72;
  --navy2:#2a5298;
  --navy-deep:#0f1c38;
  --gold:#f5b301;
  --gold-deep:#c98e00;
  --red:#c0392b;
  --red-dim:#f8e4e1;
  --green:#2F6B4F;
  --green-dim:#e4efe8;
  --card:#FFFFFF;
  --radius:14px;
}
*{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{
  background:var(--paper);
  color:var(--ink);
  font-family:'Tajawal',sans-serif;
  line-height:1.75;
}
h1,h2,h3,.display{font-family:'Tajawal',sans-serif;font-weight:800;}
::selection{background:var(--gold);color:var(--navy-deep);}
button{font-family:inherit;cursor:pointer;}
input,textarea{font-family:inherit;}
a{color:inherit;}

/* ---------- layout shell ---------- */
.page{display:none;}
.page.active{display:block;animation:fade .35s ease;}
@keyframes fade{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}

/* ---------- top gold banner ---------- */
.top-banner{
  background:var(--navy-deep);
  color:var(--gold);
  text-align:center;
  padding:11px 16px;
  font-size:.95rem;
  font-weight:700;
  border-bottom:2px solid var(--gold);
}

/* ---------- header / hero ---------- */
.hero{
  background:linear-gradient(135deg,var(--navy1),var(--navy2));
  color:#fff;
  padding:40px 24px 34px;
  position:relative;
  overflow:hidden;
  text-align:center;
}
.hero-inner{max-width:820px;margin:0 auto;position:relative;}
.hero h1{
  font-size:2.6rem;
  font-weight:800;
  line-height:1.2;
  margin-bottom:10px;
}
.hero p.tagline{
  font-size:1.05rem;
  color:#D9E2F5;
  max-width:560px;
  margin:0 auto;
}
.hero-actions{margin-top:24px;display:flex;gap:12px;flex-wrap:wrap;justify-content:center;}
.pill{
  border:2px solid var(--gold);
  background:transparent;
  color:#fff;
  padding:11px 24px;
  border-radius:999px;
  font-size:1rem;
  font-weight:700;
  transition:.2s;
}
.pill.solid{background:var(--gold);border-color:var(--gold);color:var(--navy-deep);}
.pill:hover{background:rgba(245,179,1,.15);}
.pill.solid:hover{background:var(--gold-deep);}

/* ---------- top nav ---------- */
nav.tabs{
  background:var(--navy-deep);
  display:flex;justify-content:center;gap:4px;
  padding:0 12px;
  overflow-x:auto;
}
nav.tabs button{
  background:none;border:none;
  padding:14px 18px;
  font-size:.95rem;
  font-weight:600;
  color:#B7C3E0;
  border-bottom:3px solid transparent;
  white-space:nowrap;
}
nav.tabs button.active{color:var(--gold);border-bottom-color:var(--gold);font-weight:700;}

/* ---------- container ---------- */
.wrap{max-width:1000px;margin:0 auto;padding:36px 24px 90px;position:relative;}
.section-title{
  font-size:1.7rem;font-weight:800;color:var(--ink);margin-bottom:4px;text-align:center;
}
.section-sub{color:var(--ink-soft);font-size:.95rem;margin-bottom:28px;text-align:center;}

/* ---------- grade tabs ---------- */
.grade-row{display:flex;gap:10px;margin-bottom:30px;flex-wrap:wrap;justify-content:center;}
.grade-btn{
  background:var(--card);
  border:2px solid var(--rule);
  padding:10px 22px;
  border-radius:999px;
  font-weight:700;
  font-size:.95rem;
  color:var(--ink-soft);
}
.grade-btn.active{
  border-color:var(--navy2);
  color:#fff;
  background:linear-gradient(135deg,var(--navy1),var(--navy2));
}

/* ---------- subject grid ---------- */
.subject-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:20px;}
.subject-card{
  background:var(--card);
  border:1px solid var(--rule);
  border-radius:var(--radius);
  padding:28px 20px;
  text-align:center;
  cursor:pointer;
  position:relative;
  box-shadow:0 3px 10px rgba(19,35,71,.06);
  transition:transform .15s, box-shadow .15s;
}
.subject-card:hover{transform:translateY(-4px);box-shadow:0 12px 22px rgba(19,35,71,.12);}
.subject-card .icon-circle{
  width:58px;height:58px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  margin:0 auto 14px;
}
.subject-card .icon-circle svg{width:28px;height:28px;stroke:#fff;}
.subject-card h3{font-size:1.1rem;font-weight:800;color:var(--ink);}
.subject-card .count{font-size:.8rem;color:var(--ink-soft);margin-top:5px;}

/* ---------- lesson list ---------- */
.lesson-list{margin-top:30px;}
.lesson-row{
  display:flex;justify-content:space-between;align-items:center;
  background:var(--card);
  border:1px solid var(--rule);
  border-radius:var(--radius);
  padding:16px 18px;margin-bottom:10px;
}
.lesson-row{border-radius:12px;}
.unit-head{
  margin:26px 0 12px;
  padding:10px 18px;
  background:linear-gradient(135deg,var(--navy1),var(--navy2));
  color:var(--gold);
  border-radius:10px;
  font-weight:800;
  font-size:1.02rem;
}
.unit-head:first-child{margin-top:8px;}
.lesson-row .name{font-weight:700;}
.lesson-row .name .done{color:var(--green);font-size:.8rem;font-weight:500;margin-right:8px;}
.btn{
  border:none;border-radius:999px;
  padding:10px 18px;font-weight:700;font-size:.88rem;
}
.btn-ink{background:linear-gradient(135deg,var(--navy1),var(--navy2));color:#fff;}
.btn-red{background:var(--gold);color:var(--navy-deep);}
.btn-ghost{background:none;border:1.5px solid var(--rule);color:var(--ink);}
.btn:hover{opacity:.9;}
.empty-note{
  border:1px dashed var(--rule);border-radius:var(--radius);
  padding:26px;text-align:center;color:var(--ink-soft);font-size:.92rem;
}

/* ---------- lesson detail ---------- */
.lesson-head{display:flex;justify-content:space-between;align-items:flex-start;gap:16px;flex-wrap:wrap;margin-bottom:22px;}
.lesson-head h1{font-size:2.1rem;color:var(--ink);}
.lesson-head .meta{color:var(--ink-soft);font-size:.9rem;margin-top:4px;}
.listen-bar{
  display:flex;gap:8px;align-items:center;
  background:var(--paper-dim);border:1px solid var(--rule);border-radius:var(--radius);
  padding:8px 14px;margin-bottom:26px;font-size:.9rem;color:var(--ink-soft);
}
.icon-btn{
  border:none;background:var(--card);border:1px solid var(--rule);
  width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;
  font-size:.9rem;
}
.quran-box{
  background:#FBF3DE;border:1px solid #E9D9A6;border-radius:var(--radius);
  padding:26px;text-align:center;font-family:'Amiri',serif;font-size:1.5rem;line-height:2.4;
  margin-bottom:28px;
}
.block{margin-bottom:26px;}
.block h2{font-size:1.25rem;color:var(--ink);border-bottom:2px solid var(--ink);display:inline-block;padding-bottom:5px;margin-bottom:14px;}
.tafsir-card{
  border-right:3px solid var(--red);background:var(--card);padding:14px 18px;border-radius:0 var(--radius) var(--radius) 0;margin-bottom:12px;
}
.tafsir-card h4{font-size:1rem;color:var(--red);margin-bottom:6px;}
table.vocab{width:100%;border-collapse:collapse;font-size:.92rem;}
table.vocab th,table.vocab td{border:1px solid var(--rule);padding:10px 12px;text-align:right;}
table.vocab th{background:var(--ink);color:#fff;font-weight:600;}
table.vocab tr:nth-child(even) td{background:var(--paper-dim);}
ul.balagha{list-style:none;}
ul.balagha li{padding-right:22px;position:relative;margin-bottom:10px;}
ul.balagha li::before{content:"—";position:absolute;right:0;color:var(--red);}
.divider{border:none;border-top:1px dashed var(--rule);margin:34px 0;}
.cta-band{
  background:var(--ink);color:#fff;border-radius:var(--radius);
  padding:26px;text-align:center;margin-top:20px;
}
.cta-band h3{font-family:'Tajawal';font-size:1.15rem;margin-bottom:4px;}
.cta-band p{color:#C9CBDA;font-size:.9rem;margin-bottom:16px;}

/* ---------- quiz ---------- */
.quiz-q{background:var(--card);border:1px solid var(--rule);border-radius:var(--radius);padding:18px;margin-bottom:16px;}
.quiz-q p.qtext{font-weight:700;margin-bottom:12px;}
.opt{
  display:block;border:1.5px solid var(--rule);border-radius:var(--radius);
  padding:10px 14px;margin-bottom:8px;font-size:.94rem;
}
.opt input{margin-left:10px;}
.opt.correct{border-color:var(--green);background:var(--green-dim);}
.opt.wrong{border-color:var(--red);background:var(--red-dim);}
.result-box{
  display:none;text-align:center;background:var(--green-dim);border:1px solid var(--green);
  border-radius:var(--radius);padding:26px;margin-top:10px;
}
.result-box .score{font-size:2.2rem;font-weight:800;color:var(--green);margin:10px 0;}

/* ---------- AI chat ---------- */
.chat-shell{
  background:var(--card);border:1px solid var(--rule);border-radius:var(--radius);
  display:flex;flex-direction:column;height:70vh;overflow:hidden;
}
.chat-top{
  background:linear-gradient(135deg,var(--navy1),var(--navy2));color:#fff;padding:14px 20px;display:flex;justify-content:space-between;align-items:center;
}
.chat-top h2{font-family:'Tajawal';font-size:1.05rem;}
.gear{background:none;border:1px solid rgba(255,255,255,.35);color:#fff;border-radius:var(--radius);padding:6px 12px;font-size:.82rem;}
.chat-body{flex:1;overflow-y:auto;padding:20px;background:var(--paper-dim);display:flex;flex-direction:column;gap:12px;}
.bubble{max-width:78%;padding:12px 16px;border-radius:var(--radius);line-height:1.7;font-size:.95rem;white-space:pre-wrap;}
.bubble.user{background:linear-gradient(135deg,var(--navy1),var(--navy2));color:#fff;align-self:flex-start;}
.bubble.bot{background:#fff;border:1px solid var(--rule);align-self:flex-end;}
.bubble.bot.loading{color:var(--ink-soft);font-style:italic;}
.chat-foot{display:flex;gap:8px;padding:14px;border-top:1px solid var(--rule);background:#fff;}
.chat-foot textarea{
  flex:1;resize:none;border:1px solid var(--rule);border-radius:var(--radius);padding:10px 12px;font-size:.95rem;height:44px;
}
.key-panel{
  background:var(--card);border:1px solid var(--rule);border-radius:var(--radius);padding:20px;margin-bottom:18px;
}
.key-panel input{width:100%;border:1px solid var(--rule);border-radius:var(--radius);padding:10px 12px;margin:10px 0;font-size:.9rem;}
.key-panel .note{font-size:.82rem;color:var(--ink-soft);}
.key-panel .note a{color:var(--red);text-decoration:underline;}

/* ---------- footer ---------- */
footer{text-align:center;padding:26px;color:var(--ink-soft);font-size:.85rem;border-top:1px solid var(--rule);background:var(--paper-dim);}

@media(max-width:640px){
  .hero h1{font-size:2.2rem;}
  .wrap.ruled::before{display:none;}
}
</style>
</head>
<body>

<div class="top-banner">⭐ إسلام المصري يقدم لكم هذه المنصة للتعلم أو الاستفسار أو المساعدة اليومية ⭐</div>

<header class="hero">
  <div class="hero-inner">
    <h1>🏆 أبطال الإعدادية</h1>
    <p class="tagline">المنصة التعليمية الشاملة والمساعد الذكي الأول — لطلاب الصف الأول والثاني والثالث الإعدادي</p>
    <div class="hero-actions">
      <button class="pill" onclick="switchTab('aiPage','navAi')">🤖 أبطال AI — مساعدك الذكي</button>
      <button class="pill solid" onclick="switchTab('learnPage','navLearn')">📚 الدروس والمناهج</button>
    </div>
  </div>
</header>

<nav class="tabs">
  <button id="navLearn" class="active" onclick="switchTab('learnPage','navLearn')">الدروس والمناهج</button>
  <button id="navAi" onclick="switchTab('aiPage','navAi')">المساعد الذكي</button>
</nav>

<!-- ======================= LEARN PAGE ======================= -->
<main id="learnPage" class="page active">
  <div class="wrap ruled">
    <div class="grade-row" id="gradeRow"></div>

    <div id="subjectsView">
      <h2 class="section-title" id="gradeTitle"></h2>
      <p class="section-sub">اختر المادة عشان تشوف الدروس المتاحة</p>
      <div class="subject-grid" id="subjectGrid"></div>
    </div>

    <div id="lessonsView" style="display:none">
      <button class="btn btn-ghost" style="margin-bottom:20px" onclick="backToSubjects()">⟵ رجوع للمواد</button>
      <h2 class="section-title" id="subjectTitle"></h2>
      <div class="lesson-list" id="lessonList"></div>
    </div>

    <div id="lessonDetailView" style="display:none"></div>
  </div>
</main>

<!-- ======================= AI PAGE ======================= -->
<main id="aiPage" class="page">
  <div class="wrap" style="max-width:820px">
    <h2 class="section-title">🏆 أبطال AI</h2>
    <p class="section-sub">اسأل أي سؤال في أي مادة — شرح، إعراب، حل مسألة، أو مراجعة سريعة.</p>

    <div class="key-panel" id="keyPanel">
      <strong>خطوة أولى: فعّل المساعد</strong>
      <p class="note" style="margin-top:6px">هتحتاج مفتاح Gemini مجاني (نفس اللي جبته قبل كده من Google AI Studio). بيتخزن في متصفحك بس، ومحدش يشوفه غيرك.</p>
      <input type="password" id="apiKeyInput" placeholder="الصق مفتاح الـ API هنا">
      <button class="btn btn-red" onclick="saveApiKey()">حفظ وتفعيل</button>
      <p class="note" style="margin-top:10px">مفيش مفتاح؟ هاته من <a href="https://aistudio.google.com/apikey" target="_blank">Google AI Studio</a> — مجاني ومستنى منك دقيقتين.</p>
    </div>

    <div class="chat-shell" id="chatShell" style="display:none">
      <div class="chat-top">
        <h2>🏆 أبطال AI</h2>
        <button class="gear" onclick="showKeyPanel()">⚙ الإعدادات</button>
      </div>
      <div class="chat-body" id="chatBody">
        <div class="bubble bot">أهلاً بك! أنا "أبطال AI" — المساعد الذكي الخاص بمنصة أبطال الإعدادية. اسألني في أي مادة أو درس، وهجاوبك بشرح كامل ومفصّل.</div>
      </div>
      <div class="chat-foot">
        <textarea id="chatInput" placeholder="اكتب سؤالك هنا..." onkeydown="handleChatKey(event)"></textarea>
        <button class="btn btn-red" onclick="sendChat()">إرسال</button>
      </div>
    </div>
  </div>
</main>

<footer>
  جميع الحقوق محفوظة © 2026 — تصميم وتطوير <strong>إسلام المصري</strong>
</footer>

<script>
/* ============================================================
   ICONS
   ============================================================ */
const ICONS = {
  book:'<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 5.5C4 4.4 4.9 3.5 6 3.5h8.5V19H6c-1.1 0-2 .9-2 2V5.5Z"/><path d="M14.5 3.5H18c1.1 0 2 .9 2 2V21H6"/></svg>',
  globe:'<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M3 12h18M12 3c2.5 2.6 3.8 5.7 3.8 9s-1.3 6.4-3.8 9c-2.5-2.6-3.8-5.7-3.8-9S9.5 5.6 12 3Z"/></svg>',
  calc:'<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="3" width="14" height="18" rx="2"/><path d="M8 8h8M8 12h.01M12 12h.01M16 12h.01M8 16h.01M12 16h.01M16 16h.01"/></svg>',
  flask:'<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M9 3h6M10 3v6l-5.2 8.5a1.8 1.8 0 0 0 1.5 2.5h11.4a1.8 1.8 0 0 0 1.5-2.5L14 9V3"/><path d="M7.5 15h9"/></svg>',
  map:'<svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M9 4 4 6v14l5-2 6 2 5-2V4l-5 2-6-2Z"/><path d="M9 4v14M15 6v14"/></svg>'
};

/* ============================================================
   CURRICULUM DATA
   To add a lesson: push an object into the relevant subject's
   `lessons` array. Fields:
   { id, title, meta, quranText(optional), tafsir(optional array),
     sections(optional array of {heading,body}),
     vocab(optional array of {word,meaning,opp}),
     balagha(optional array of strings),
     quiz: [{q, options:[...], correct: index, explain}] }
   ============================================================ */
const CURRICULUM = {
  prep1:{ label:'الصف الأول الإعدادي', subjects:{
    arabic:{label:'اللغة العربية', icon:'book', lessons:[
      {id:'p1-ar-1', unit:'الوحدة الأولى: أنا وضميري', title:'الفعل المجرد والفعل المزيد', meta:'النحو — الوحدة الأولى',
        sections:[
          {heading:'الفعل المجرد', body:'هو الفعل اللي كل حروفه أصلية، لو شلت منها حرف يختل المعنى.\nنوعان:\n1) مجرد ثلاثي: ثلاثة حروف أصلية. كَتَبَ — فَتَحَ — نَصَرَ — عَلِمَ — كَرُمَ.\n2) مجرد رباعي: أربعة حروف أصلية. دَحْرَجَ — زَلْزَلَ — بَعْثَرَ — وَسْوَسَ.'},
          {heading:'الفعل المزيد', body:'هو الفعل اللي زاد على حروفه الأصلية حرف أو أكتر.\nحروف الزيادة مجموعة في كلمة: "سألتمونيها".\nمثال: كَتَبَ (مجرد) → كاتَبَ، اكتتبَ، استكتبَ (مزيد).'},
          {heading:'أوزان المزيد الثلاثي', body:'• مزيد بحرف واحد (ثلاثة أوزان):\n  أفْعَلَ: أكْرَمَ — فَعَّلَ: كَرَّمَ — فاعَلَ: كاتَبَ\n• مزيد بحرفين (خمسة أوزان):\n  انْفَعَلَ: انكسرَ — افْتَعَلَ: اجتمعَ — افْعَلَّ: احمرَّ — تَفَعَّلَ: تعلَّمَ — تَفاعَلَ: تبادَلَ\n• مزيد بثلاثة أحرف (أربعة أوزان):\n  اسْتَفْعَلَ: استخرجَ — افْعَوْعَلَ: اخشوشنَ — افْعالَّ: اخضارَّ — افْعَوَّلَ: اجلوَّذَ'},
          {heading:'أوزان المزيد الرباعي', body:'• مزيد بحرف: تَفَعْلَلَ → تَدَحْرَجَ.\n• مزيد بحرفين: افْعَنْلَلَ → احْرَنْجَمَ، وافْعَلَلَّ → اطمأنَّ.'},
          {heading:'إزاي أعرف المجرد من المزيد؟', body:'حوّل الفعل للماضي، وشوف حروفه:\n• لو ثلاثة أو أربعة حروف كلها أصلية → مجرد.\n• لو فيه حرف من حروف "سألتمونيها" زائد، أو فيه حرف مُضعَّف (شدّة) → مزيد.\nمثال: "يستخرجُ" ماضيه "استخرجَ"، أصله "خَرَجَ"، فهو مزيد بثلاثة أحرف على وزن استفعل.'}
        ],
        quiz:[
          {q:'الفعل "دَحْرَجَ":', options:['مجرد ثلاثي','مجرد رباعي','مزيد بحرف'], correct:1, explain:'أربعة حروف كلها أصلية، فهو مجرد رباعي.'},
          {q:'الفعل "استخرجَ" وزنه:', options:['اسْتَفْعَلَ','افْتَعَلَ','تَفَعَّلَ'], correct:0, explain:'مزيد بثلاثة أحرف (الهمزة والسين والتاء) على وزن استفعل.'},
          {q:'الفعل "كرَّمَ" مزيد بـ:', options:['حرف واحد (التضعيف) على وزن فَعَّلَ','حرفين','ثلاثة أحرف'], correct:0, explain:'التضعيف زيادة بحرف واحد، والوزن فَعَّلَ.'},
          {q:'حروف الزيادة مجموعة في كلمة:', options:['نصرتموها','سألتمونيها','كتبتموها'], correct:1, explain:'حروف الزيادة مجموعة في "سألتمونيها".'},
          {q:'"انكسرَ" على وزن:', options:['افْتَعَلَ','انْفَعَلَ','تَفاعَلَ'], correct:1, explain:'زيدت الهمزة والنون، فالوزن انْفَعَلَ.'}
        ]},

      {id:'p1-ar-2', unit:'الوحدة الأولى: أنا وضميري', title:'الهمزة على الألف (المتوسطة والمتطرفة)', meta:'الإملاء — الوحدة الأولى',
        sections:[
          {heading:'القاعدة الذهبية للهمزة المتوسطة', body:'قارن بين حركة الهمزة وحركة الحرف اللي قبلها، والأقوى فيهما هو اللي بيحدد الكرسي.\nترتيب قوة الحركات من الأقوى للأضعف:\n1) الكسرة → وكرسيها النبرة (ئ)\n2) الضمة → وكرسيها الواو (ؤ)\n3) الفتحة → وكرسيها الألف (أ)\n4) السكون → أضعفها ومالوش كرسي'},
          {heading:'متى تُكتب الهمزة المتوسطة على الألف؟', body:'تُكتب على الألف (أ) إذا كانت الفتحة هي الأقوى، يعني في ثلاث حالات:\n1) مفتوحة بعد فتح: سَأَلَ — تَأَمَّلَ — رَأَى.\n2) مفتوحة بعد ساكن صحيح: مَسْأَلة — يَسْأَل — نَشْأَة.\n3) ساكنة بعد فتح: رَأْس — بَأْس — يَأْمَن — مُؤَجَّل... (لا: الساكنة بعد فتح مثل: رَأْس، فَأْس، كَأْس).'},
          {heading:'أمثلة على باقي الكراسي (للمقارنة)', body:'• على النبرة (ئ) إذا كانت الكسرة أقوى: سائِل، بِئْر، مِئَة، فِئَة، رِئَة.\n• على الواو (ؤ) إذا كانت الضمة أقوى: مُؤْمِن، سُؤَال، رُؤُوس، لُؤْلُؤ.\n• على السطر: إذا كانت مفتوحة بعد ألف ساكنة: قراءة، عباءة، تساءل.'},
          {heading:'الهمزة المتطرفة (في آخر الكلمة)', body:'هنا العبرة بحركة الحرف اللي قبلها فقط:\n• قبلها فتحة → تُكتب على الألف: قرَأ — بدَأ — ملجَأ — نبَأ.\n• قبلها ضمة → على الواو: تباطُؤ — تنبُّؤ — لؤلُؤ.\n• قبلها كسرة → على النبرة: شاطِئ — قارِئ — مبتدِئ.\n• قبلها ساكن أو حرف مد → على السطر: جزْء — بُطْء — ماء — سماء — ضوْء — شيْء.'}
        ],
        quiz:[
          {q:'كلمة "مَسْأَلة" كُتبت همزتها على الألف لأنها:', options:['مفتوحة بعد ساكن صحيح','مكسورة بعد ضم','ساكنة بعد كسر'], correct:0, explain:'الهمزة مفتوحة وقبلها ساكن صحيح، فالفتحة أقوى والكرسي ألف.'},
          {q:'الكتابة الصحيحة:', options:['مؤمن','مأمن','مئمن'], correct:0, explain:'الهمزة ساكنة وقبلها ضمة، والضمة أقوى فتُكتب على الواو.'},
          {q:'"قارِئ" كُتبت على النبرة لأن ما قبلها:', options:['مفتوح','مكسور','ساكن'], correct:1, explain:'في الهمزة المتطرفة العبرة بحركة ما قبلها، وهنا كسرة.'},
          {q:'الكتابة الصحيحة لكلمة تنتهي بهمزة بعد ساكن:', options:['جزأ','جزؤ','جزء'], correct:2, explain:'الهمزة المتطرفة بعد ساكن تُكتب على السطر.'},
          {q:'أقوى الحركات في قاعدة الهمزة المتوسطة:', options:['الفتحة','الضمة','الكسرة'], correct:2, explain:'الترتيب: الكسرة ثم الضمة ثم الفتحة ثم السكون.'}
        ]}
    ]},
    english:{label:'اللغة الإنجليزية', icon:'globe', lessons:[
      {id:'p1-en-1', unit:'Unit 1', title:'Present Simple Tense', meta:'القواعد — الوحدة الأولى',
        sections:[
          {heading:'إمتى بنستخدم Present Simple؟', body:'بنستخدمه علشان نتكلم عن حاجات ثابتة أو بتتكرر كل يوم زي العادات والحقائق العلمية.\nمثال: I go to school every day. — The sun rises in the east.'},
          {heading:'تكوين الجملة', body:'مع (I, You, We, They): الفعل بيفضل زي ما هو.\nمع (He, She, It): بنضيف s أو es للفعل.\nمثال: She plays football. — He watches TV.'},
          {heading:'النفي والسؤال', body:'النفي: don\'t / doesn\'t + الفعل الأصلي.\nالسؤال: Do / Does + الفاعل + الفعل الأصلي؟\nمثال: Does he play football? — He doesn\'t play football.'}
        ],
        quiz:[
          {q:'اختار الصح: She ____ to school every day.', options:['go','goes','going'], correct:1, explain:'مع She بنضيف s للفعل في Present Simple.'},
          {q:'اختار الصح: ____ they like football?', options:['Do','Does','Is'], correct:0, explain:'مع They بنستخدم Do في السؤال.'}
        ]}
    ]},
    math:{label:'الرياضيات', icon:'calc', lessons:[]},
    science:{label:'العلوم', icon:'flask', lessons:[]},
    social:{label:'الدراسات', icon:'map', lessons:[]}
  }},
  prep2:{ label:'الصف الثاني الإعدادي', subjects:{
    arabic:{label:'اللغة العربية', icon:'book', lessons:[
      {id:'p2-ar-1', unit:'الوحدة الأولى: انتمائي قوتي', title:'المعرب والمبني من الأسماء والحروف', meta:'النحو — الوحدة الأولى: انتمائي قوتي',
        sections:[
          {heading:'الفرق بين المُعرَب والمَبني', body:'المُعرَب: كلمة بتتغير حركة آخرها بتغيّر موقعها في الجملة.\nمثال: حضر محمدٌ / رأيتُ محمدًا / سلّمتُ على محمدٍ.\nالمَبني: كلمة بتلزم حالة واحدة مهما اتغيّر موقعها.\nمثال: هذا طالبٌ / رأيتُ هذا / سلّمتُ على هذا — "هذا" ثابتة دايمًا.'},
          {heading:'الأصل في الأسماء الإعراب', body:'معظم الأسماء مُعرَبة، والمبني منها قليل ومحصور، وده اللي بنحفظه.'},
          {heading:'الأسماء المبنية — احفظها', body:'1) الضمائر كلها: أنا، نحن، أنتَ، هو، هي، هم، التاء في "كتبتُ"، نا، الهاء...\n2) أسماء الإشارة: هذا، هذه، هؤلاء، ذلك، تلك. (ماعدا المثنى: هذان، هاتان → مُعرَبان)\n3) الأسماء الموصولة: الذي، التي، الذين، اللاتي. (ماعدا المثنى: اللذان، اللتان → مُعرَبان)\n4) أسماء الشرط: مَن، ما، مهما، متى، أينما... (ماعدا "أي" → مُعرَبة)\n5) أسماء الاستفهام: مَن، ما، ماذا، متى، كيف، أين. (ماعدا "أي" → مُعرَبة)\n6) بعض الظروف: حيث، أمسِ، الآن، إذْ، إذا.\n7) أسماء الأفعال: هيهاتَ، شتّانَ، آمينَ، صَهْ، مَهْ.\n8) الأعداد المركبة من 11 إلى 19 (ماعدا اثني عشر).'},
          {heading:'الحروف كلها مبنية', body:'كل الحروف مبنية بدون استثناء، ومالهاش محل من الإعراب.\nمثل: في، على، من، إلى، هل، لم، لن، قد، إنّ، الواو، الفاء.\nفي الإعراب بنقول: حرف جر مبني لا محل له من الإعراب.'},
          {heading:'إزاي تعرب المبني؟', body:'بنقول: مبني على (الحركة) في محل (الموقع الإعرابي).\nمثال: هذا طالبٌ → هذا: اسم إشارة مبني على السكون في محل رفع مبتدأ.\nمثال: رأيتُ هذا → هذا: اسم إشارة مبني على السكون في محل نصب مفعول به.'}
        ],
        quiz:[
          {q:'"هذا كتابٌ مفيدٌ" — إعراب (هذا):', options:['مبتدأ مرفوع بالضمة','اسم إشارة مبني على السكون في محل رفع مبتدأ','اسم مُعرَب مرفوع'], correct:1, explain:'أسماء الإشارة مبنية، فنقول مبني في محل رفع مبتدأ.'},
          {q:'أي الأسماء التالية مُعرَب وليس مبنيًا؟', options:['هؤلاء','هذان','الذي'], correct:1, explain:'المثنى من أسماء الإشارة والموصول مُعرَب (هذان، هاتان، اللذان، اللتان).'},
          {q:'الحروف في اللغة العربية:', options:['كلها مبنية','كلها معربة','بعضها معرب'], correct:0, explain:'كل الحروف مبنية ولا محل لها من الإعراب.'},
          {q:'"أيُّ الطلابِ نجح؟" — كلمة (أيُّ):', options:['مبنية','مُعرَبة','حرف'], correct:1, explain:'"أي" استثناء: مُعرَبة سواء كانت استفهامية أو شرطية.'}
        ]},

      {id:'p2-ar-2', unit:'الوحدة الأولى: انتمائي قوتي', title:'المعرب والمبني من الأفعال', meta:'النحو — الوحدة الأولى',
        sections:[
          {heading:'القاعدة العامة', body:'الأصل في الأفعال البناء، والمُعرَب منها هو المضارع فقط (بشروط).\n• الفعل الماضي: مبني دائمًا.\n• فعل الأمر: مبني دائمًا.\n• الفعل المضارع: مُعرَب إلا في حالتين.'},
          {heading:'بناء الفعل الماضي — ثلاث حالات', body:'1) مبني على الفتح: إذا لم يتصل به شيء، أو اتصلت به تاء التأنيث، أو ألف الاثنين.\n   كتَبَ — كتبَتْ — كتبَا.\n2) مبني على السكون: إذا اتصل به ضمير رفع متحرك (تاء الفاعل، نا الفاعلين، نون النسوة).\n   كتبْتُ — كتبْنا — كتبْنَ.\n3) مبني على الضم: إذا اتصلت به واو الجماعة.\n   كتبُوا.'},
          {heading:'بناء فعل الأمر', body:'1) مبني على السكون: إذا كان صحيح الآخر أو اتصلت به نون النسوة. اكتبْ — اكتبْنَ.\n2) مبني على حذف حرف العلة: إذا كان معتل الآخر. اسْعَ — ادْعُ — ارْمِ.\n3) مبني على حذف النون: إذا اتصلت به ألف الاثنين أو واو الجماعة أو ياء المخاطبة. اكتبَا — اكتبُوا — اكتبِي.\n4) مبني على الفتح: إذا اتصلت به نون التوكيد. اكتبَنَّ.'},
          {heading:'الفعل المضارع — متى يُبنى؟', body:'المضارع مُعرَب (مرفوع أو منصوب أو مجزوم) إلا في حالتين يُبنى فيهما:\n1) إذا اتصلت به نون النسوة → يُبنى على السكون.\n   مثال: الطالباتُ يكتبْنَ الدرس. (يكتبْنَ: مبني على السكون في محل رفع)\n2) إذا اتصلت به نون التوكيد (الثقيلة أو الخفيفة) → يُبنى على الفتح.\n   مثال: واللهِ لأجتهدَنَّ. (لأجتهدَنَّ: مبني على الفتح)'},
          {heading:'إعراب المضارع المُعرَب', body:'• مرفوع: إذا لم يسبقه ناصب ولا جازم. يكتبُ الطالبُ.\n• منصوب: بعد (أنْ، لن، كي، لام التعليل، حتى، فاء السببية). لن يكتبَ.\n• مجزوم: بعد (لم، لمّا، لام الأمر، لا الناهية) أو في جواب الشرط. لم يكتبْ.'}
        ],
        quiz:[
          {q:'"الطالباتُ يكتبْنَ الدرسَ" — إعراب (يكتبْنَ):', options:['مضارع مرفوع بالضمة','مضارع مبني على السكون في محل رفع','مضارع منصوب'], correct:1, explain:'اتصال نون النسوة بالمضارع يبنيه على السكون.'},
          {q:'"كتبُوا الدرسَ" — الفعل (كتبُوا) مبني على:', options:['الضم لاتصاله بواو الجماعة','الفتح','السكون'], correct:0, explain:'الماضي يُبنى على الضم عند اتصاله بواو الجماعة.'},
          {q:'"واللهِ لأجتهدَنَّ" — إعراب (لأجتهدَنَّ):', options:['مرفوع بالضمة','مبني على الفتح لاتصاله بنون التوكيد','مجزوم'], correct:1, explain:'نون التوكيد تبني المضارع على الفتح.'},
          {q:'"كتبْتُ الدرسَ" — الفعل مبني على:', options:['الفتح','السكون لاتصاله بضمير رفع متحرك','الضم'], correct:1, explain:'تاء الفاعل ضمير رفع متحرك، فيُبنى الماضي معها على السكون.'},
          {q:'فعل الأمر "ادْعُ" مبني على:', options:['السكون','حذف حرف العلة','حذف النون'], correct:1, explain:'الأمر من الفعل المعتل الآخر يُبنى على حذف حرف العلة.'}
        ]},

      {id:'p2-ar-3', unit:'الوحدة الثانية: بيئتي مسئوليتي', title:'الضمائر البارزة والمستترة', meta:'النحو — الوحدة الثانية: بيئتي مسئوليتي',
        sections:[
          {heading:'الضمير البارز', body:'هو الضمير اللي له صورة ظاهرة في الكلام (تقدر تشوفه مكتوب).\nوينقسم إلى:\n1) ضمير منفصل: يُنطق مستقلاً. (أنا، نحن، أنتَ، أنتِ، هو، هي، هم / إيّايَ، إيّاكَ، إيّاه)\n2) ضمير متصل: يتصل بآخر الكلمة. (التاء في كتبْتُ، نا، واو الجماعة، ألف الاثنين، ياء المخاطبة، الكاف، الهاء)'},
          {heading:'الضمير المستتر', body:'هو ضمير مالوش صورة ظاهرة، بس المعنى بيدل عليه، وبنقدّره في الذهن.\nمثال: محمدٌ يكتبُ الدرسَ → فاعل "يكتب" ضمير مستتر تقديره "هو".\nمثال: اكتبْ الدرسَ → فاعل "اكتب" ضمير مستتر وجوبًا تقديره "أنتَ".'},
          {heading:'مستتر وجوبًا ومستتر جوازًا', body:'• مستتر وجوبًا (مينفعش نحط مكانه اسم ظاهر): مع أفعال:\n  - المضارع المبدوء بالهمزة: أكتبُ → تقديره (أنا)\n  - المضارع المبدوء بالنون: نكتبُ → تقديره (نحن)\n  - المضارع المبدوء بالتاء للمخاطب: تكتبُ → تقديره (أنتَ)\n  - فعل الأمر: اكتبْ → تقديره (أنتَ)\n• مستتر جوازًا (ينفع نحط مكانه اسم ظاهر): مع الفعل المسند للغائب أو الغائبة:\n  - يكتبُ → تقديره (هو) — وينفع نقول: يكتبُ محمدٌ.\n  - تكتبُ (للغائبة) → تقديره (هي)'},
          {heading:'محل الضمير من الإعراب', body:'الضمير مبني دائمًا، وبنحدد محله حسب موقعه:\n• في محل رفع فاعل: كتبْتُ (التاء).\n• في محل نصب مفعول به: أكرمَني (الياء).\n• في محل جر بالإضافة أو بحرف الجر: كتابُه — عليه.'}
        ],
        quiz:[
          {q:'"أكتبُ الدرسَ" — الفاعل:', options:['ضمير مستتر وجوبًا تقديره أنا','ضمير بارز','اسم ظاهر'], correct:0, explain:'المضارع المبدوء بالهمزة فاعله مستتر وجوبًا تقديره "أنا".'},
          {q:'"محمدٌ يكتبُ" — الفاعل في (يكتب):', options:['مستتر وجوبًا','مستتر جوازًا تقديره هو','ضمير متصل'], correct:1, explain:'المسند للغائب فاعله مستتر جوازًا، لأنه ينفع يحل محله اسم ظاهر.'},
          {q:'"كتابُه مفيدٌ" — الهاء في (كتابُه):', options:['في محل رفع فاعل','في محل جر مضاف إليه','في محل نصب مفعول به'], correct:1, explain:'الضمير المتصل بالاسم يكون في محل جر بالإضافة.'},
          {q:'"إيّاكَ نعبدُ" — نوع الضمير (إيّاك):', options:['منفصل في محل نصب مفعول به','متصل في محل رفع','مستتر'], correct:0, explain:'"إيّا" ضمير نصب منفصل، ومحله نصب مفعول به مقدّم.'}
        ]},

      {id:'p2-ar-4', unit:'الوحدة الثانية: بيئتي مسئوليتي', title:'أسلوب الشرط: أدوات الشرط الجازمة', meta:'النحو — الوحدة الثانية',
        sections:[
          {heading:'أركان أسلوب الشرط', body:'أسلوب الشرط بيتكوّن من ثلاث أركان:\n1) أداة الشرط.\n2) فعل الشرط.\n3) جواب الشرط.\nمثال: مَن يجتهدْ ينجحْ.\n• مَن: أداة شرط جازمة.\n• يجتهدْ: فعل الشرط مجزوم.\n• ينجحْ: جواب الشرط وجزاؤه مجزوم.'},
          {heading:'أدوات الشرط الجازمة — احفظها', body:'إنْ — إذما (حرفان)\nمَن — ما — مهما — متى — أيّان — أين — أينما — أنّى — حيثما — كيفما — أيّ (أسماء)\nكلها مبنية ماعدا "أيّ" فهي مُعرَبة.'},
          {heading:'علامة جزم فعل الشرط وجوابه', body:'• السكون: لو صحيح الآخر. مَن يجتهدْ ينجحْ.\n• حذف حرف العلة: لو معتل الآخر. مَن يسعَ إلى الخير يلقَ خيرًا.\n• حذف النون: لو من الأفعال الخمسة. إنْ تجتهدوا تنجحوا.'},
          {heading:'متى يقترن جواب الشرط بالفاء؟ (سؤال مهم)', body:'بنربط الجواب بالفاء في الحالات دي:\n1) لو كان جملة اسمية: مَن يجتهدْ فهو ناجحٌ.\n2) لو كان فعلاً جامدًا: مَن يجتهدْ فنِعْمَ الطالبُ.\n3) لو كان فعلاً طلبيًا (أمر/نهي/استفهام): مَن يجتهدْ فأكرمْه.\n4) لو مسبوقًا بـ "ما" أو "لن" أو "قد" أو "السين/سوف": مَن يهملْ فلن ينجحَ.\nطريقة الحفظ: (اسمية — جامدة — طلبية — ما، لن، قد، السين وسوف).'},
          {heading:'ملاحظة عن إذا ولو', body:'"إذا" و"لو" أدوات شرط غير جازمة، بتربط بين جملتين من غير جزم.\nمثال: إذا اجتهدْتَ نجحْتَ.'}
        ],
        quiz:[
          {q:'"مَن يجتهدْ ينجحْ" — إعراب (ينجحْ):', options:['مرفوع بالضمة','جواب الشرط مجزوم بالسكون','منصوب'], correct:1, explain:'الأداة الجازمة تجزم فعل الشرط وجوابه.'},
          {q:'"إنْ تجتهدوا تنجحوا" — علامة جزم الفعلين:', options:['السكون','حذف النون','حذف حرف العلة'], correct:1, explain:'الأفعال الخمسة تُجزم بحذف النون.'},
          {q:'أي الجمل التالية يجب فيها اقتران الجواب بالفاء؟', options:['مَن يجتهدْ ينجحْ','مَن يجتهدْ فهو ناجحٌ','مَن يجتهدْ يتفوقْ'], correct:1, explain:'الجواب جملة اسمية، فيجب اقترانه بالفاء.'},
          {q:'الأداة المُعرَبة من بين أدوات الشرط الجازمة:', options:['مَن','مهما','أيّ'], correct:2, explain:'"أيّ" هي الوحيدة المُعرَبة، وباقي الأدوات مبنية.'}
        ]},

      {id:'p2-ar-5', unit:'الوحدة الأولى والثانية: الإملاء', title:'الألف اللينة في الأسماء والأفعال والحروف', meta:'الإملاء — الوحدة الأولى والثانية',
        sections:[
          {heading:'ما هي الألف اللينة؟', body:'هي ألف ساكنة مفتوح ما قبلها، وتأتي في آخر الكلمة، وتُكتب بصورتين:\n• ألف قائمة (ا) مثل: عصا، دعا.\n• ألف مقصورة (ى) مثل: فتى، سعى.'},
          {heading:'أولاً: الألف اللينة في الأسماء', body:'القاعدة: نرجع لأصل الألف.\n• لو أصلها واو → تُكتب ألفًا قائمة (ا). عصا (عَصَوان) — رِبا (رِبَوي).\n• لو أصلها ياء → تُكتب مقصورة (ى). فتى (فَتَيان) — هدى (هَدَيت).\nطريقة معرفة الأصل: ثنِّ الاسم أو اجمعه أو ردّه للمفرد.\nاستثناءات: في الأسماء الزائدة عن ثلاثة أحرف تُكتب مقصورة دائمًا (مستشفى، ذكرى)، إلا إذا سبقتها ياء فتُكتب قائمة (دنيا، هدايا، قضايا).\nوالأسماء الأعجمية تُكتب قائمة: أوروبا، فرنسا، أمريكا — إلا (موسى، عيسى، كسرى، بخارى).'},
          {heading:'ثانيًا: الألف اللينة في الأفعال', body:'• الفعل الثلاثي: نرجع لأصل الألف بالمضارع أو المصدر.\n  - أصلها واو → قائمة: دعا (يدعو)، سما (يسمو)، عفا (يعفو).\n  - أصلها ياء → مقصورة: سعى (يسعى)، رمى (يرمي)، قضى (يقضي).\n• الفعل الزائد عن ثلاثة أحرف: تُكتب مقصورة دائمًا: استدعى، ارتقى، أعطى.\n  إلا إذا سبقتها ياء فتُكتب قائمة: أحيا، استحيا.'},
          {heading:'ثالثًا: الألف اللينة في الحروف', body:'تُكتب قائمة (ا) في كل الحروف: ما، لا، إلا، كلا، خلا، عدا، حاشا، أمّا.\nإلا في أربعة حروف تُكتب مقصورة (ى): إلى — على — حتى — بلى.\nطريقة الحفظ: (إلى على حتى بلى) هي الاستثناء، وباقي الحروف بألف قائمة.'}
        ],
        quiz:[
          {q:'كلمة "عصا" كُتبت بألف قائمة لأن:', options:['أصل ألفها ياء','أصل ألفها واو (عَصَوان)','هي حرف'], correct:1, explain:'نثنيها فتصير "عصوان"، فأصل الألف واو وتُكتب قائمة.'},
          {q:'الكتابة الصحيحة للفعل من (يسعى):', options:['سعا','سعى','سعاء'], correct:1, explain:'أصل الألف ياء (يسعى)، فتُكتب مقصورة.'},
          {q:'أي الحروف التالية تُكتب بألف مقصورة؟', options:['ما','لا','على'], correct:2, explain:'الحروف المستثناة أربعة: إلى، على، حتى، بلى.'},
          {q:'كلمة "مستشفى" كُتبت مقصورة لأنها:', options:['اسم زائد عن ثلاثة أحرف','اسم أعجمي','حرف'], correct:0, explain:'الاسم الزائد عن ثلاثة أحرف تُكتب ألفه مقصورة ما لم تسبقها ياء.'},
          {q:'الكتابة الصحيحة:', options:['دنيى','دنيا','دنيي'], correct:1, explain:'سبقت الألفَ ياءٌ، فتُكتب قائمة: دنيا.'}
        ]}
    ]},
    english:{label:'اللغة الإنجليزية', icon:'globe', lessons:[]},
    math:{label:'الرياضيات', icon:'calc', lessons:[
      {id:'p2-math-1', unit:'الوحدة الثانية: الجبر', title:'المعادلة الخطية في متغير واحد', meta:'الجبر — الوحدة الثانية',
        sections:[
          {heading:'تعريف المعادلة الخطية', body:'هي معادلة من الدرجة الأولى في متغير واحد، بتاخد الصورة: ax + b = c، حيث a لا تساوي صفر.'},
          {heading:'خطوات الحل', body:'1) نجمع الحدود المتشابهة في كل طرف.\n2) ننقل الأعداد لطرف والمتغير للطرف التاني (مع تغيير الإشارة).\n3) نقسم الطرفين على معامل المتغير للحصول على قيمته.'},
          {heading:'مثال محلول', body:'حل المعادلة: 3x + 5 = 20\n3x = 20 - 5 = 15\nx = 15 ÷ 3 = 5'}
        ],
        quiz:[
          {q:'حل المعادلة: 2x + 4 = 12', options:['x = 4','x = 6','x = 8'], correct:0, explain:'2x = 12-4 = 8 ، إذن x = 8÷2 = 4.'},
          {q:'حل المعادلة: 5x - 3 = 17', options:['x = 3','x = 4','x = 5'], correct:1, explain:'5x = 17+3 = 20 ، إذن x = 20÷5 = 4.'}
        ]}
    ]},
    science:{label:'العلوم', icon:'flask', lessons:[]},
    social:{label:'الدراسات', icon:'map', lessons:[]}
  }},
  prep3:{ label:'الصف الثالث الإعدادي', subjects:{
    arabic:{label:'اللغة العربية', icon:'book', lessons:[
      {id:'p3-ar-1', unit:'الوحدة الأولى: آداب تحمي شبابنا', title:'أدب التعامل مع الوالدين', meta:'نص استماع — الدرس الأول',
        sections:[
          {heading:'الفكرة العامة', body:'النص بيتناول حق الوالدين العظيم على أبنائهم، وأدب الابن الصالح معاهما بالطاعة والاحترام والبر، باعتبار بر الوالدين من أسمى القيم الدينية والأخلاقية في مجتمعنا.'},
          {heading:'القيم المستفادة', body:'• بر الوالدين قرنه الله تعالى بعبادته في القرآن الكريم: ﴿وَقَضَىٰ رَبُّكَ أَلَّا تَعْبُدُوا إِلَّا إِيَّاهُ وَبِالْوَالِدَيْنِ إِحْسَانًا﴾.\n• طاعة الوالدين واجبة فيما لا يخالف شرع الله.\n• من أدب التعامل معهما: خفض الصوت، وعدم التأفف أو الجدال، والدعاء لهما دائمًا.\n• الإحسان للوالدين يكون في الكبر والصغر، وليس وقت الحاجة فقط.'},
          {heading:'ملحوظة مهمة للمذاكرة', body:'ده نص استماع، يعني بيتقال في الفصل شفهيًا وبيُختبر فيه الفهم مش الحفظ الحرفي. ركّز على استيعاب القيم والأفكار الرئيسية بدل حفظ نص بعينه.'}
        ],
        quiz:[
          {q:'بر الوالدين في القرآن الكريم قُرن بـ:', options:['الصلاة فقط','عبادة الله سبحانه وتعالى','الزكاة'], correct:1, explain:'"وقضى ربك ألا تعبدوا إلا إياه وبالوالدين إحسانًا" — قرن الله بر الوالدين بعبادته.'},
          {q:'من آداب التعامل مع الوالدين المذكورة في النص:', options:['رفع الصوت عند الغضب','خفض الصوت والتلطف','الجدال المستمر'], correct:1, explain:'من الأدب مع الوالدين خفض الصوت وعدم التأفف.'},
          {q:'هذا الدرس من نوع:', options:['نص قراءة','نص استماع','نص شعري'], correct:1, explain:'الدرس الأول في الوحدة نص استماع.'}
        ]},

      {id:'p3-ar-2', unit:'الوحدة الأولى: آداب تحمي شبابنا', title:'أغلى من الذهب — واسم الفاعل', meta:'نص قراءة + النحو — الدرس الثاني',
        sections:[
          {heading:'الفكرة العامة للنص', body:'يحكي النص قصة البطل المصري محمد رشوان، لاعب الجودو، الذي رفض في أوليمبياد 1984 أن يستغل أي ثغرة غير أخلاقية للفوز بالميدالية الذهبية، وفضّل الروح الرياضية والقيم على الفوز بأي ثمن. خسر المباراة وحصل على الفضية، لكنه كسب احترام العالم، وكُرّم دوليًا تقديرًا لأخلاقه الرياضية النبيلة. ومن هنا جاء عنوان النص "أغلى من الذهب" — لأن الشرف والأخلاق أغلى من أي ميدالية.'},
          {heading:'القيمة التربوية', body:'النجاح الحقيقي لا يُقاس بالفوز وحده، بل بالقيم والأخلاق التي يتمسك بها الإنسان حتى في لحظة المنافسة الحاسمة.'},
          {heading:'النحو: اسم الفاعل — تعريفه', body:'اسم مشتق يدل على مَن قام بالفعل أو اتصف به على وجه التجدد والحدوث (وليس الثبوت).'},
          {heading:'صياغة اسم الفاعل من الفعل الثلاثي', body:'على وزن (فاعِل): كتَبَ ← كاتِب — لعِبَ ← لاعِب — فهِمَ ← فاهِم.\nملحوظة: الفعل الأجوف (معتل الوسط) له صياغة خاصة: قال ← قائل — باع ← بائع — نام ← نائم.'},
          {heading:'صياغة اسم الفاعل من غير الثلاثي', body:'بإحلال ميم مضمومة محل حرف المضارعة، مع كسر ما قبل الآخر.\nأكرمَ ← يُكرِمُ ← مُكرِم — استخرجَ ← يستخرجُ ← مُستخرِج — انطلقَ ← ينطلقُ ← مُنطلِق.'},
          {heading:'عمل اسم الفاعل', body:'يعمل عمل فعله (يرفع فاعلاً وينصب مفعولاً به) بشرطين: أن يدل على الحال أو الاستقبال، وأن يعتمد على نفي أو استفهام أو يقع نعتًا أو حالًا أو خبرًا أو بعد مبتدأ.\nمثال: محمدٌ فاهمٌ الدرسَ. — فاهمٌ: اسم فاعل رفع ضميرًا مستترًا (هو) ونصب "الدرسَ" مفعولاً به.'}
        ],
        quiz:[
          {q:'البطل الذي يتحدث عنه نص "أغلى من الذهب":', options:['محمد صلاح','محمد رشوان','أحمد الجندي'], correct:1, explain:'النص عن لاعب الجودو محمد رشوان وموقفه الرياضي النبيل.'},
          {q:'اسم الفاعل من الفعل "قال":', options:['قائل','قاول','مقول'], correct:0, explain:'الفعل الأجوف "قال" اسم فاعله "قائل".'},
          {q:'اسم الفاعل من "استخرجَ":', options:['مُستخرَج','مُستخرِج','استخراج'], correct:1, explain:'بإحلال ميم مضمومة وكسر ما قبل الآخر يكون "مُستخرِج".'},
          {q:'"الطالبُ فاهمٌ الدرسَ" — إعراب "الدرسَ":', options:['مفعول به لاسم الفاعل منصوب','فاعل مرفوع','نعت منصوب'], correct:0, explain:'اسم الفاعل "فاهمٌ" عمل عمل فعله ونصب "الدرسَ" مفعولاً به.'}
        ]},

      {id:'p3-ar-3', unit:'الوحدة الأولى: آداب تحمي شبابنا', title:'الصداقة — واسم المفعول', meta:'نص قراءة + النحو — الدرس الثالث',
        sections:[
          {heading:'الفكرة العامة للنص', body:'مقال للدكتور شوقي ضيف (عالم لغوي وناقد أدبي مصري كبير، وعضو مجمع اللغة العربية) يتناول قيمة الصداقة الحقيقية وصفات الصديق الوفي، وأثر اختيار الأصدقاء الصالحين في حياة الإنسان.'},
          {heading:'القيم المستفادة', body:'• الصديق الحقيقي يقف بجانبك في وقت الشدة، لا الرخاء فقط.\n• "المرء على دين خليله" — لاختيار الأصدقاء أثر كبير على شخصية الإنسان وسلوكه.\n• أساس الصداقة الصادقة: الصدق والإخلاص والنصح.'},
          {heading:'النحو: اسم المفعول — تعريفه', body:'اسم مشتق يدل على مَن وقع عليه الفعل.'},
          {heading:'صياغة اسم المفعول من الثلاثي', body:'على وزن (مَفْعول): كتَبَ ← مكتوب — فهِمَ ← مفهوم.\nالفعل الأجوف: قال ← مقول (بحذف حرف العلة الأصلي وإبداله) — باع ← مبيع.'},
          {heading:'صياغة اسم المفعول من غير الثلاثي', body:'بإحلال ميم مضمومة محل حرف المضارعة، مع فتح ما قبل الآخر.\nأكرمَ ← يُكرِمُ ← مُكرَم — استخرجَ ← يستخرجُ ← مُستخرَج.'},
          {heading:'أهم فرق يلخبط الطلاب في الامتحان', body:'اسم الفاعل يُكسر ما قبل الآخر (مُستخرِج)، واسم المفعول يُفتح ما قبل الآخر (مُستخرَج).\nنفس الحروف بالظبط، والفرق بس في الحركة الأخيرة — ركّز عليها كويس جدًا.'},
          {heading:'عمل اسم المفعول', body:'يعمل عمل الفعل المبني للمجهول، فينوب عنه فاعله ويصبح نائب فاعل.\nمثال: الدرسُ مفهومٌ معناه. — مفهومٌ: اسم مفعول، و"معناه" نائب فاعل مرفوع.'}
        ],
        quiz:[
          {q:'كاتب نص "الصداقة":', options:['أحمد شوقي','د. شوقي ضيف','إبراهيم ناجي'], correct:1, explain:'النص مقال للدكتور شوقي ضيف.'},
          {q:'اسم المفعول من "استخرجَ":', options:['مُستخرِج','مُستخرَج','مستخرِجون'], correct:1, explain:'يُفتح ما قبل الآخر في اسم المفعول، بعكس اسم الفاعل.'},
          {q:'اسم المفعول من الفعل الأجوف "قال":', options:['مقوول','مقول','قائل'], correct:1, explain:'يُحذف حرف العلة الأصلي ويُستبدل، فيصير "مقول".'},
          {q:'"الدرسُ مفهومٌ معناه" — إعراب "معناه":', options:['نائب فاعل مرفوع لاسم المفعول','مفعول به','فاعل'], correct:0, explain:'اسم المفعول يعمل عمل المبني للمجهول، فيرفع نائب فاعل.'}
        ]},

      {id:'p3-ar-4', unit:'الوحدة الأولى: آداب تحمي شبابنا', title:'تحية للشباب — أحمد شوقي', meta:'نص شعري — الدرس الرابع',
        sections:[
          {heading:'عن الشاعر', body:'أحمد شوقي (1868 - 1932)، الملقّب بـ"أمير الشعراء"، من أعظم شعراء العربية الحديثة، وقد بايعه شعراء عصره بإمارة الشعر في حفل تكريم كبير سنة 1927.'},
          {heading:'الفكرة العامة للقصيدة', body:'القصيدة نداء وتحية من الشاعر إلى الشباب، يحثهم فيها على الجد والعمل والاعتزاز بالوطن، ويُبرز دورهم المحوري في بناء المستقبل والنهوض بالأمة.'},
          {heading:'وصية للمذاكرة', body:'النص الكامل للقصيدة موجود في كتابك المدرسي. لما تذاكرها ركّز على: معاني المفردات الصعبة، والبحر الشعري، ومواطن الجمال والصور البيانية — لأن الامتحان غالبًا بيسأل في المعنى والتذوق، مش في حفظ الأبيات بس.'}
        ],
        quiz:[
          {q:'لقب أحمد شوقي:', options:['أمير الشعراء','حافظ الشعراء','شاعر النيل'], correct:0, explain:'لُقّب أحمد شوقي بأمير الشعراء بعد مبايعة شعراء عصره له سنة 1927.'},
          {q:'موضوع قصيدة "تحية للشباب":', options:['وصف الطبيعة','حث الشباب على الجد وبناء المستقبل','الغزل'], correct:1, explain:'القصيدة نداء للشباب للعمل والجد واستشعار دورهم في بناء الوطن.'},
          {q:'يُعد أحمد شوقي من شعراء:', options:['العصر الجاهلي','العصر الحديث','العصر العباسي'], correct:1, explain:'أحمد شوقي من أبرز رواد الشعر العربي الحديث.'}
        ]},

      {id:'p3-ar-5', unit:'الوحدة الثانية: نحو تفكير سليم', title:'ثمرة القراءة', meta:'نص استماع — الدرس الأول',
        sections:[
          {heading:'الفكرة العامة', body:'النص بيتناول القيمة الحقيقية للقراءة، وإزاي القراءة الواعية بتبني عقل الإنسان وتوسّع مداركه وتنمّي تفكيره النقدي، وإزاي الأمم المتقدمة بنت نهضتها على أساس شعوب قارئة.'},
          {heading:'القيم المستفادة', body:'• القراءة غذاء العقل زي ما الطعام غذاء الجسم.\n• القراءة الواعية (مش بس السريعة) هي اللي بتبني تفكير سليم.\n• من ثمار القراءة: اتساع الأفق، وحسن التعبير، والقدرة على التمييز بين الصواب والخطأ.'},
          {heading:'ملحوظة للمذاكرة', body:'ده نص استماع، فالتركيز هنا على فهم الأفكار الرئيسية والقيم، مش حفظ نص بعينه.'}
        ],
        quiz:[
          {q:'موضوع النص الرئيسي:', options:['أهمية الرياضة','قيمة القراءة وأثرها على التفكير','تاريخ مصر'], correct:1, explain:'النص عن ثمرة القراءة وأثرها في بناء عقل الإنسان.'},
          {q:'من ثمار القراءة الواعية كما ورد في النص:', options:['اتساع الأفق وحسن التمييز','كثرة النوم','قلة التركيز'], correct:0},
          {q:'نوع هذا الدرس:', options:['نص قراءة','نص استماع','نص شعري'], correct:1}
        ]},

      {id:'p3-ar-6', unit:'الوحدة الثانية: نحو تفكير سليم', title:'أفضل النعم — وصيغ المبالغة', meta:'نص قراءة + النحو — الدرس الثاني',
        sections:[
          {heading:'الفكرة العامة للنص', body:'يتأمل النص في نِعَم الله الكثيرة على الإنسان، ويركّز بشكل خاص على نعمة عظيمة (العقل أو الصحة أو نعمة الهداية، بحسب ما ورد بالتفصيل في نص الكتاب) باعتبارها من أفضل ما وهبه الله للإنسان، ويدعو لشكرها وحسن استغلالها.\nملحوظة: النص الكامل والتفاصيل الدقيقة موجودة في كتابك — راجعها للتأكد من تحديد "أفضل نعمة" اللي ركّز عليها الكاتب بالظبط.'},
          {heading:'النحو: صيغ المبالغة — تعريفها', body:'صيغة مشتقة تدل على مَن اتصف بالفعل على سبيل الكثرة والمبالغة (أكتر من اسم الفاعل العادي في قوة الدلالة).'},
          {heading:'أشهر أوزان صيغ المبالغة — خمسة أوزان', body:'1) فَعّال: غفّار، كذّاب، رزّاق.\n2) مِفْعال: مِعطاء، مِقدام، مِهذار.\n3) فَعول: صبور، غفور، أكول.\n4) فَعِيل: رحيم، عليم، سميع.\n5) فَعِل: فَرِح، حَذِر، يَقِظ.'},
          {heading:'عملها في الجملة', body:'تعمل عمل اسم الفاعل تمامًا: ترفع فاعلاً وتنصب مفعولاً به، بنفس شروطه (أن تدل على الحال أو الاستقبال، وأن تعتمد على نفي أو استفهام، أو تقع خبرًا أو نعتًا أو حالًا أو بعد مبتدأ).\nمثال: اللهُ غفّارٌ الذنبَ. — غفّارٌ: صيغة مبالغة على وزن فَعّال، رفعت ضميرًا مستترًا (هو) ونصبت "الذنبَ" مفعولاً به.'}
        ],
        quiz:[
          {q:'كلمة "صبور" صيغة مبالغة على وزن:', options:['فَعّال','فَعول','مِفعال'], correct:1, explain:'صبور على وزن فَعول، وهو أحد أوزان المبالغة الخمسة.'},
          {q:'"اللهُ غفّارٌ الذنبَ" — إعراب "الذنبَ":', options:['فاعل مرفوع','مفعول به منصوب لصيغة المبالغة','نعت'], correct:1, explain:'صيغة المبالغة "غفّارٌ" عملت عمل اسم الفاعل ونصبت "الذنبَ" مفعولاً به.'},
          {q:'أي الكلمات التالية على وزن "مِفْعال"؟', options:['مِعطاء','رحيم','حَذِر'], correct:0, explain:'مِعطاء على وزن مِفعال، من أوزان صيغ المبالغة.'},
          {q:'صيغ المبالغة في عملها تشبه:', options:['اسم المفعول','اسم الفاعل','اسم المكان'], correct:1, explain:'تعمل عمل اسم الفاعل بنفس شروطه تمامًا.'}
        ]},

      {id:'p3-ar-7', unit:'الوحدة الثانية: نحو تفكير سليم', title:'خير جليس — واسم المكان', meta:'نص قراءة + النحو — الدرس الثالث',
        sections:[
          {heading:'الفكرة العامة للنص', body:'نص للدكتور أحمد زكي يدور حول القيمة العظيمة للكتاب باعتباره خير جليس ورفيق للإنسان، مستلهمًا المقولة العربية المشهورة "خير جليسٍ في الزمانِ كتابُ"، ويبرز دور الكتاب في تثقيف العقل ومؤانسة الإنسان في وحدته.'},
          {heading:'القيم المستفادة', body:'• الكتاب صديق وفيّ لا يمل ولا يخذل صاحبه.\n• القراءة وسيلة للترقي الفكري ومجالسة العظماء عبر كتبهم.'},
          {heading:'النحو: اسم المكان — تعريفه', body:'اسم مشتق يدل على مكان وقوع الفعل.'},
          {heading:'صياغته من الفعل الثلاثي — قاعدتان', body:'1) وزن (مَفْعَل) بفتح العين: إذا كان مضارع الفعل مفتوح العين أو مضمومها، أو كان الفعل مثالاً واويًا (أوله واو تُحذف في المضارع).\n   يذهبُ (مفتوح) ← مَذهَب — يكتُبُ (مضموم) ← مَكتَب — يَعِدُ (من وعد، مثال واوي) ← مَوعِد.\n2) وزن (مَفْعِل) بكسر العين: إذا كان مضارع الفعل مكسور العين.\n   يجلِسُ ← مَجلِس — يضرِبُ ← مَضرِب.'},
          {heading:'صياغته من غير الثلاثي', body:'على وزن اسم المفعول تمامًا: بإحلال ميم مضمومة محل حرف المضارعة وفتح ما قبل الآخر.\nاستخرجَ ← يستخرجُ ← مُستخرَج (المكان). انطلقَ ← يَنطلقُ ← مُنطلَق.'}
        ],
        quiz:[
          {q:'كاتب نص "خير جليس":', options:['أحمد شوقي','د. أحمد زكي','شوقي ضيف'], correct:1, explain:'النص للدكتور أحمد زكي.'},
          {q:'اسم المكان من الفعل "جلَسَ" (يجلِسُ):', options:['مَجلَس','مَجلِس','مُجالِس'], correct:1, explain:'مضارعه مكسور العين (يجلِس)، فاسم المكان على وزن مَفْعِل.'},
          {q:'اسم المكان من الفعل "كتَبَ" (يكتُبُ):', options:['مَكتِب','مَكتَب','مُكتَب'], correct:1, explain:'مضارعه مضموم العين (يكتُب)، فاسم المكان على وزن مَفْعَل.'},
          {q:'اسم المكان من "استخرجَ":', options:['مُستخرِج','مُستخرَج','مَخرَج'], correct:1, explain:'من غير الثلاثي يُصاغ على وزن اسم المفعول: مُستخرَج.'}
        ]},

      {id:'p3-ar-8', unit:'الوحدة الثانية: نحو تفكير سليم', title:'تاج الفضائل — الإمام علي بن أبي طالب', meta:'نص شعري — الدرس الرابع',
        sections:[
          {heading:'عن القصيدة وصاحبها', body:'القصيدة منسوبة إلى الإمام علي بن أبي طالب رضي الله عنه، ابن عم النبي ﷺ وزوج ابنته فاطمة، ورابع الخلفاء الراشدين، واشتُهر بالحكمة والفصاحة والزهد، وله حِكَم وأقوال مأثورة كثيرة في الأخلاق والفضائل.'},
          {heading:'الفكرة العامة', body:'تتناول القصيدة مجموعة من الفضائل والقيم الأخلاقية التي ينبغي للإنسان أن يتحلى بها، مثل الصدق والتواضع وطلب العلم وحسن الخُلق، بأسلوب حِكَمي مباشر ومؤثر.'},
          {heading:'وصية للمذاكرة', body:'راجع النص الكامل من كتابك المدرسي، وركّز أثناء المذاكرة على: معاني المفردات الصعبة، ومواطن الجمال في كل بيت، والقيمة الأخلاقية التي يدعو إليها.'}
        ],
        quiz:[
          {q:'قصيدة "تاج الفضائل" منسوبة إلى:', options:['أحمد شوقي','الإمام علي بن أبي طالب','إبراهيم ناجي'], correct:1, explain:'القصيدة منسوبة للإمام علي بن أبي طالب رضي الله عنه.'},
          {q:'الإمام علي بن أبي طالب هو:', options:['الخليفة الأول','رابع الخلفاء الراشدين','صحابي فقط بلا خلافة'], correct:1, explain:'هو رابع الخلفاء الراشدين رضي الله عنه.'},
          {q:'موضوع القصيدة بشكل عام:', options:['وصف الحروب','الفضائل والقيم الأخلاقية','الغزل'], correct:1, explain:'القصيدة تدعو إلى مجموعة من الفضائل والأخلاق الحميدة.'}
        ]},

      {id:'p3-ar-9', unit:'الوحدة الثالثة: أنا والمستقبل', title:'بناء المستقبل في عصر الآلة', meta:'نص استماع — الدرس الأول',
        sections:[
          {heading:'الفكرة العامة', body:'يتناول النص التحديات والفرص التي يواجهها جيل الشباب في عصر التكنولوجيا والآلة والذكاء الاصطناعي، وضرورة أن يُعدّ الشباب أنفسهم بالعلم والمهارات المناسبة لمواكبة هذا العصر وبناء مستقبلهم فيه.'},
          {heading:'القيم والأفكار المستفادة', body:'• العلم والتعلّم المستمر هما أساس مواكبة عصر الآلة والتكنولوجيا.\n• ينبغي أن يكون الإنسان صانعًا ومبدعًا في التكنولوجيا، لا مجرد مستهلك لها.\n• المهارات الإنسانية الخالصة (كالتفكير النقدي والإبداع والتواصل الإنساني) هي ما يميز الإنسان عن الآلة ويبقيه لا غنى عنه.'},
          {heading:'ملحوظة للمذاكرة', body:'ده نص استماع، فالتركيز هنا على فهم الأفكار والقيم الرئيسية، مش حفظ نص بعينه.'}
        ],
        quiz:[
          {q:'موضوع النص الرئيسي:', options:['تاريخ اختراع الآلات','تحديات وفرص بناء المستقبل في عصر التكنولوجيا','الرياضة والصحة'], correct:1, explain:'النص عن كيفية إعداد الشباب أنفسهم لمواكبة عصر الآلة والتكنولوجيا.'},
          {q:'من أهم عوامل مواكبة عصر الآلة كما ورد في النص:', options:['العلم والتعلم المستمر','الابتعاد الكامل عن التكنولوجيا','الاعتماد الكلي على الآلة بدل التفكير'], correct:0, explain:'العلم والتعلم المستمر هما أساس مواكبة العصر الحديث.'},
          {q:'نوع هذا الدرس:', options:['نص قراءة','نص استماع','نص شعري'], correct:1}
        ]},

      {id:'p3-ar-10', unit:'الوحدة الثالثة: أنا والمستقبل', title:'حرفتك بين يديك — واسم الزمان', meta:'نص قراءة + النحو — الدرس الثاني',
        sections:[
          {heading:'الفكرة العامة للنص', body:'يتناول النص أهمية تعلّم حرفة أو مهنة يعتمد عليها الإنسان في حياته، ويبرز قيمة العمل اليدوي والمهني إلى جانب التعليم الأكاديمي، ودور إتقان الحرفة في بناء الاستقلال الاقتصادي وتحقيق الذات.'},
          {heading:'القيم المستفادة', body:'• إتقان حرفة أو مهارة عملية ثروة حقيقية لا تقل عن الشهادة الدراسية.\n• العمل اليدوي شرف لا عيب فيه، والمجتمعات المتقدمة تحترم أصحاب الحرف.\n• الاعتماد على النفس واكتساب مهارة عملية يحقق الاستقلال والثقة بالنفس.'},
          {heading:'النحو: اسم الزمان — تعريفه', body:'اسم مشتق يدل على زمان وقوع الفعل.\nملحوظة مهمة: اسم الزمان واسم المكان لهما نفس الصيغة والوزن بالظبط، والفرق بينهما بيتحدد من السياق والمعنى في الجملة، مش من شكل الكلمة.'},
          {heading:'صياغته من الفعل الثلاثي', body:'نفس قاعدة اسم المكان بالضبط:\n1) وزن (مَفْعَل) بفتح العين: إذا كان مضارع الفعل مفتوح العين أو مضمومها، أو كان الفعل مثالاً واويًا.\n   غرَبَ (يغرُبُ) ← مَغرَب (وقت الغروب) — وعَدَ (يَعِدُ) ← مَوعِد (زمن الموعد).\n2) وزن (مَفْعِل) بكسر العين: إذا كان مضارع الفعل مكسور العين.\n   طلَعَ (يطلِعُ) ← مَطلِع (وقت الطلوع).'},
          {heading:'صياغته من غير الثلاثي', body:'على وزن اسم المفعول: بإحلال ميم مضمومة محل حرف المضارعة وفتح ما قبل الآخر.\nاستقبلَ (يستقبِلُ) ← مُستقبَل (بمعنى الزمن القادم) — انطلقَ ← مُنطلَق.'},
          {heading:'إزاي تفرّق بين اسم الزمان واسم المكان في الامتحان؟', body:'اقرأ الجملة كاملة: لو الكلمة بتدل على وقت (متى؟) فهي اسم زمان، ولو بتدل على مكان (أين؟) فهي اسم مكان.\nمثال: "وصلتُ في مَطلِع الفجر" (زمان) — "جلستُ في مَطلِع الجبل" (مكان، أي أول موضع منه).'}
        ],
        quiz:[
          {q:'"مَوعِدُنا غدًا صباحًا" — كلمة (مَوعِد) هنا:', options:['اسم زمان','اسم مكان','اسم آلة'], correct:0, explain:'تدل على وقت اللقاء، فهي اسم زمان.'},
          {q:'اسم الزمان من "طلَعَ" (يطلِعُ):', options:['مَطلَع','مَطلِع','مُطلِع'], correct:1, explain:'مضارعه مكسور العين (يطلِع)، فيُصاغ على وزن مَفْعِل.'},
          {q:'اسم الزمان واسم المكان يشتركان في:', options:['المعنى فقط','الصياغة والوزن','الإعراب دائمًا'], correct:1, explain:'لهما نفس الصيغة والوزن، ويُفرَّق بينهما بالمعنى والسياق.'},
          {q:'"استقبلَ" اسم الزمان منها:', options:['مُستقبِل','مُستقبَل','استقبال'], correct:1, explain:'من غير الثلاثي على وزن اسم المفعول: مُستقبَل.'}
        ]},

      {id:'p3-ar-11', unit:'الوحدة الثالثة: أنا والمستقبل', title:'مستقبل مصر في الزراعة — واسم الآلة', meta:'نص قراءة + النحو — الدرس الثالث',
        sections:[
          {heading:'الفكرة العامة للنص', body:'يتناول النص أهمية الزراعة في اقتصاد مصر ومستقبلها، ودور استصلاح الأراضي الصحراوية والمشروعات القومية الزراعية الحديثة في تحقيق الأمن الغذائي والنهوض الاقتصادي.'},
          {heading:'القيم المستفادة', body:'• الزراعة من أهم موارد الاقتصاد المصري منذ القدم.\n• استخدام العلم والتكنولوجيا الحديثة في الزراعة يزيد الإنتاج ويحقق الأمن الغذائي.\n• كل مواطن له دور في دعم مستقبل بلده الزراعي والاقتصادي.'},
          {heading:'النحو: اسم الآلة — تعريفه', body:'اسم مشتق يدل على الأداة التي يُستعان بها في القيام بالفعل.'},
          {heading:'أوزان اسم الآلة القياسية — ثلاثة أوزان', body:'1) مِفْعَل: مِبْرَد، مِصْعَد، مِقَصّ (أصلها مِقصَص).\n2) مِفْعَلة: مِلْعَقة، مِكْنَسة، مِغْرَفة.\n3) مِفْعال: مِفتاح، مِصباح، مِنشار.'},
          {heading:'أوزان حديثة لأدوات العصر', body:'كتير من أدوات العصر الحديث جت على وزن (فَعّالة) وهو أصلاً وزن مبالغة استُعير لاسم الآلة:\nسيّارة، غسّالة، ثلّاجة، طائرة، برّادة.\nوبعضها جاء بالنحت أو التعريب من لغات أخرى: تليفون، كمبيوتر، راديو.'},
          {heading:'إعراب اسم الآلة', body:'اسم الآلة ليس من المشتقات العاملة (بعكس اسم الفاعل والمفعول وصيغ المبالغة)، فهو يُعرب حسب موقعه العادي في الجملة فقط (فاعل، مفعول به، مبتدأ...) وليس له شروط عمل خاصة.'}
        ],
        quiz:[
          {q:'اسم الآلة "مِفتاح" على وزن:', options:['مِفْعَل','مِفْعال','مِفْعَلة'], correct:1, explain:'مِفتاح على وزن مِفعال، من الأوزان القياسية لاسم الآلة.'},
          {q:'كلمة "غسّالة" اسم آلة جاء على وزن:', options:['فَعّالة (مستعار من وزن المبالغة)','مِفْعَل','مَفْعول'], correct:0, explain:'كثير من أدوات العصر الحديث صيغت على وزن فَعّالة.'},
          {q:'اسم الآلة من حيث العمل النحوي:', options:['يعمل عمل فعله كاسم الفاعل','ليس من المشتقات العاملة، يُعرب حسب موقعه فقط','ينصب مفعولين'], correct:1, explain:'اسم الآلة لا يعمل عمل الفعل، بعكس اسم الفاعل والمفعول.'},
          {q:'"مِنشار" اسم آلة على وزن:', options:['مِفْعال','مِفْعَل','فَعّال'], correct:0, explain:'مِنشار على وزن مِفعال.'}
        ]},

      {id:'p3-ar-12', unit:'الوحدة الثالثة: أنا والمستقبل', title:'اصنع بيدك مجدك — معروف الرصافي', meta:'نص شعري — الدرس الرابع',
        sections:[
          {heading:'عن الشاعر', body:'معروف الرصافي (1875 - 1945)، شاعر عراقي كبير من أبرز رواد الشعر العربي الحديث، عُرف بشعره الاجتماعي والوطني والحكمي، ودعوته الدائمة للعمل والجد والإصلاح.'},
          {heading:'الفكرة العامة للقصيدة', body:'يدعو الشاعر في قصيدته الشباب إلى الاعتماد على النفس والعمل الجاد لبناء مجدهم ومستقبلهم بأيديهم، لا انتظار الفرج من الغير أو الاتكال على الحظ، مؤكدًا أن العزة والمجد ثمرة الكد والاجتهاد.'},
          {heading:'وصية للمذاكرة', body:'راجع النص الكامل من كتابك المدرسي، وركّز على: معاني المفردات الصعبة، ومواطن الجمال والصور البيانية، والقيمة الأخلاقية الأساسية (الاعتماد على النفس) التي تدور حولها القصيدة — لأنها الفكرة اللي بيتمحور حولها الامتحان غالبًا.'}
        ],
        quiz:[
          {q:'شاعر قصيدة "اصنع بيدك مجدك":', options:['أحمد شوقي','معروف الرصافي','إبراهيم ناجي'], correct:1, explain:'القصيدة لمعروف الرصافي، الشاعر العراقي الكبير.'},
          {q:'الفكرة الأساسية التي تدعو إليها القصيدة:', options:['انتظار الحظ والفرج','الاعتماد على النفس والعمل الجاد','الاتكال على الآخرين'], correct:1, explain:'القصيدة تحث على بناء المجد بالجهد الذاتي لا بالانتظار.'},
          {q:'معروف الرصافي شاعر من:', options:['مصر','العراق','سوريا'], correct:1, explain:'معروف الرصافي شاعر عراقي من أعلام الشعر العربي الحديث.'}
        ]}
    ]},
    english:{label:'اللغة الإنجليزية', icon:'globe', lessons:[]},
    math:{label:'الرياضيات', icon:'calc', lessons:[
      {id:'p3-math-1', unit:'الوحدة الأولى: الأعداد والعمليات عليها', title:'قوى القوى', meta:'1-1',
        sections:[
          {heading:'القانون الأساسي', body:'قوة مرفوعة لقوة: (aᵐ)ⁿ = aᵐ×ⁿ\nيعني لما يكون عندك أس على أس، بتضرب الأسين في بعض.\nمثال: (2³)² = 2³ˣ² = 2⁶ = 64.\nمثال: (x²)⁵ = x¹⁰.'},
          {heading:'مراجعة سريعة لباقي قوانين الأسس', body:'• ضرب أسس متشابهة الأساس: aᵐ × aⁿ = aᵐ⁺ⁿ\n• قسمة أسس متشابهة الأساس: aᵐ ÷ aⁿ = aᵐ⁻ⁿ (a≠0)\n• الأس صفر: a⁰ = 1 (a≠0)\n• الأس السالب: a⁻ⁿ = 1/aⁿ'},
          {heading:'القوة على حاصل ضرب أو خارج قسمة', body:'(a×b)ⁿ = aⁿ × bⁿ\n(a/b)ⁿ = aⁿ/bⁿ  (b≠0)\nمثال: (2x)³ = 2³ × x³ = 8x³.'},
          {heading:'مثال شامل محلول', body:'بسّط: (x³)² × (x²)⁴\n= x⁶ × x⁸  (طبّقنا قانون قوى القوى في الحدين)\n= x¹⁴  (جمعنا الأسس لأن الأساس واحد)'}
        ],
        quiz:[
          {q:'(3²)³ =', options:['3⁵','3⁶','3⁹'], correct:1, explain:'نضرب الأسين: 2×3=6، فالناتج 3⁶.'},
          {q:'(y⁴)⁵ =', options:['y⁹','y²⁰','y⁴⁵'], correct:1, explain:'نضرب الأسين: 4×5=20.'},
          {q:'(2x²)³ =', options:['2x⁶','8x⁶','6x⁶'], correct:1, explain:'(2)³ × (x²)³ = 8 × x⁶ = 8x⁶.'},
          {q:'بسّط: (a²)³ × (a³)²', options:['a⁵','a¹²','a³⁶'], correct:1, explain:'a⁶ × a⁶ = a¹².'}
        ]},

      {id:'p3-math-2', unit:'الوحدة الأولى: الأعداد والعمليات عليها', title:'المعادلات الأساسية', meta:'1-2',
        sections:[
          {heading:'حل المعادلة الخطية الأساسية', body:'الهدف: نعزل المتغيّر لوحده في طرف.\nالخطوات: 1) نجمع الحدود المتشابهة. 2) ننقل الأعداد لطرف والمتغيّر للطرف التاني (بتغيير الإشارة). 3) نقسم على معامل المتغيّر.\nمثال: 3x + 7 = 22 → 3x = 15 → x = 5.'},
          {heading:'معادلات فيها المتغيّر في الطرفين', body:'اجمع/اطرح المتغيّر من الطرفين الأول عشان يبقى في طرف واحد بس.\nمثال: 5x - 4 = 2x + 11 → 5x - 2x = 11 + 4 → 3x = 15 → x = 5.'},
          {heading:'معادلات بسيطة على الأسس (مرتبطة بالدرس اللي فات)', body:'لو الأساس واحد في الطرفين، تقدر تساوي بين الأسين مباشرة.\nمثال: حل: 2ˣ = 2⁵ → بما إن الأساس واحد (2)، إذن x = 5.\nمثال: حل: 3^(x+1) = 3⁴ → x + 1 = 4 → x = 3.'},
          {heading:'التحقق من الحل', body:'دايمًا عوّض بقيمة x اللي وصلتلها في المعادلة الأصلية للتأكد إن الطرفين بيتساووا.'}
        ],
        quiz:[
          {q:'حل: 4x - 3 = 17', options:['x = 4','x = 5','x = 6'], correct:1, explain:'4x = 20 → x = 5.'},
          {q:'حل: 6x + 2 = 3x + 14', options:['x = 3','x = 4','x = 6'], correct:1, explain:'3x = 12 → x = 4.'},
          {q:'حل: 5^(x) = 5³', options:['x = 3','x = 5','x = 15'], correct:0, explain:'الأساس متساوٍ (5)، إذن x = 3 مباشرة.'},
          {q:'حل: 2^(x-1) = 2⁵', options:['x = 4','x = 5','x = 6'], correct:2, explain:'x - 1 = 5 → x = 6.'}
        ]},

      {id:'p3-math-3', unit:'الوحدة الثانية: الجبر', title:'الدالة التربيعية', meta:'2-1',
        sections:[
          {heading:'تعريف الدالة التربيعية', body:'دالة من الدرجة الثانية، صورتها العامة: f(x) = ax² + bx + c، حيث a ≠ 0.\nشكلها البياني قطع مكافئ (Parabola).'},
          {heading:'اتجاه فتحة القطع المكافئ', body:'• لو a > 0: القطع المكافئ يفتح لأعلى (له نقطة صغرى).\n• لو a < 0: القطع المكافئ يفتح لأسفل (له نقطة عظمى).'},
          {heading:'رأس القطع المكافئ ومحور التماثل', body:'إحداثي x لرأس القطع المكافئ: x = -b/2a\nإحداثي y للرأس: نعوّض بقيمة x في الدالة: y = f(-b/2a)\nمحور التماثل: الخط الرأسي x = -b/2a.'},
          {heading:'نقاط التقاطع مع المحاور', body:'• مع محور y: عند x=0، فالنقطة (0, c).\n• مع محور x: نحل المعادلة ax²+bx+c=0 (هي جذور الدالة، وممكن تكون نقطتين أو نقطة أو لا توجد حسب المميز).'},
          {heading:'مثال محلول', body:'أوجد رأس الدالة: f(x) = x² - 4x + 3\nx = -(-4)/(2×1) = 2\ny = f(2) = 4 - 8 + 3 = -1\nإذن الرأس (2, -1)، والقطع يفتح لأعلى لأن a=1 موجب.'}
        ],
        quiz:[
          {q:'في الدالة f(x)=2x²-3x+1، اتجاه فتحة القطع المكافئ:', options:['لأعلى','لأسفل','لا يمكن التحديد'], correct:0, explain:'a=2 موجب، فالقطع يفتح لأعلى.'},
          {q:'إحداثي x لرأس الدالة f(x)=x²-6x+5:', options:['x=2','x=3','x=6'], correct:1, explain:'x = -(-6)/(2×1) = 3.'},
          {q:'نقطة تقاطع f(x)=x²+2x-8 مع محور y:', options:['(0,-8)','(0,2)','(0,8)'], correct:0, explain:'عند x=0، f(0)=-8.'},
          {q:'الصورة العامة للدالة التربيعية:', options:['f(x)=ax+b','f(x)=ax²+bx+c (a≠0)','f(x)=a/x'], correct:1}
        ]},

      {id:'p3-math-4', unit:'الوحدة الثانية: الجبر', title:'مجموعة الأصفار الحقيقية لدوال كثيرة الحدود', meta:'2-2',
        sections:[
          {heading:'تعريف الصفر الحقيقي للدالة', body:'هو قيمة x التي تجعل قيمة الدالة f(x) = 0. بيانيًا: هي نقاط تقاطع منحنى الدالة مع محور x.'},
          {heading:'إيجاد الأصفار بالتحليل', body:'حلّل كثيرة الحدود لعوامل، وساوِ كل عامل بالصفر.\nمثال: f(x) = x² - 5x + 6 = (x-2)(x-3)\nالأصفار: x=2 أو x=3.'},
          {heading:'القانون العام لحل المعادلة التربيعية', body:'لو ax²+bx+c=0 (a≠0): x = (-b ± √(b²-4ac)) / 2a\nيُستخدم لما يصعب التحليل المباشر.'},
          {heading:'المميّز Δ ونوع الجذور', body:'Δ = b² - 4ac\n• Δ > 0 ← جذران حقيقيان مختلفان (الدالة تقطع محور x في نقطتين).\n• Δ = 0 ← جذر حقيقي واحد مكرر (الدالة تمس محور x في نقطة واحدة).\n• Δ < 0 ← لا توجد جذور حقيقية (الدالة لا تقطع محور x إطلاقًا).'}
        ],
        quiz:[
          {q:'أصفار الدالة f(x)=(x-4)(x+1):', options:['x=4, x=-1','x=-4, x=1','x=4, x=1'], correct:0},
          {q:'لو Δ=0 في معادلة تربيعية، فإن:', options:['لا توجد جذور حقيقية','يوجد جذر حقيقي واحد مكرر','يوجد جذران مختلفان'], correct:1},
          {q:'مميّز المعادلة x²-4x+4=0:', options:['0','16','-16'], correct:0, explain:'Δ = (-4)²-4(1)(4) = 16-16 = 0.'},
          {q:'عدد نقاط تقاطع الدالة مع محور x لو Δ<0:', options:['نقطتان','نقطة واحدة','لا توجد'], correct:2}
        ]},

      {id:'p3-math-5', unit:'الوحدة الثانية: الجبر', title:'دوال الكسور الجبرية النسبية', meta:'2-3',
        sections:[
          {heading:'تعريف الكسر الجبري النسبي', body:'دالة على صورة كسر بسطه ومقامه كثيرتا حدود: f(x) = P(x)/Q(x)، بشرط Q(x) ≠ 0.'},
          {heading:'مجال الدالة', body:'مجال الدالة = كل الأعداد الحقيقية ما عدا القيم التي تجعل المقام يساوي صفرًا.\nمثال: f(x) = (x+1)/(x-3)  ← المجال: كل الأعداد الحقيقية ما عدا x=3.'},
          {heading:'اختزال الكسر لأبسط صورة', body:'حلّل البسط والمقام لعوامل، واحذف العوامل المشتركة بينهما.\nمثال: (x²-9)/(x-3) = ((x-3)(x+3))/(x-3) = x+3 ، بشرط x≠3.\nملحوظة مهمة: لازم نفضل ذاكرين شرط x≠3 حتى بعد الاختزال، لأنه جزء أساسي من مجال الدالة الأصلية.'}
        ],
        quiz:[
          {q:'مجال الدالة f(x) = 5/(x-2):', options:['كل الأعداد الحقيقية','كل الأعداد الحقيقية ما عدا 2','كل الأعداد الحقيقية ما عدا صفر'], correct:1},
          {q:'أبسط صورة لـ (x²-16)/(x-4):', options:['x+4، بشرط x≠4','x-4','x+4 بدون شروط'], correct:0, explain:'(x-4)(x+4)/(x-4) = x+4، ولازم نحتفظ بالشرط x≠4.'},
          {q:'المقام في الكسر الجبري لازم يكون:', options:['مساويًا للصفر','غير مساوٍ للصفر','عددًا صحيحًا فقط'], correct:1}
        ]},

      {id:'p3-math-6', unit:'الوحدة الثانية: الجبر', title:'المجال المشترك وتساوي دوال الكسور الجبرية النسبية', meta:'2-4',
        sections:[
          {heading:'المجال المشترك لدالتين', body:'هو تقاطع مجالي الدالتين، يعني كل قيم x المسموحة في الدالتين معًا في نفس الوقت.\nمثال: لو مجال f هو كل الأعداد ما عدا 2، ومجال g هو كل الأعداد ما عدا 3، فالمجال المشترك بينهما: كل الأعداد ما عدا 2 و3.'},
          {heading:'تساوي دالتين', body:'تتساوى دالتان f و g إذا تحقق الشرطان معًا:\n1) لهما نفس المجال المشترك.\n2) f(x) = g(x) لكل قيمة x في هذا المجال (بعد اختزال كل منهما لأبسط صورة).\nمثال: f(x)=(x²-4)/(x-2) و g(x)=x+2 ليستا متساويتين تمامًا؛ لأن مجال f يستثني x=2 بينما مجال g لا يستثنيها — فرغم تطابق الناتج بعد الاختزال، يختلف المجال.'}
        ],
        quiz:[
          {q:'الشرط الأول لتساوي دالتين:', options:['نفس المجال المشترك','نفس الشكل البياني فقط','نفس عدد الحدود'], correct:0},
          {q:'المجال المشترك لدالتين هو:', options:['اتحاد المجالين','تقاطع المجالين','مجموع المجالين'], correct:1},
          {q:'لو مجال f يستثني x=5 ومجال g يستثني x=1، فالمجال المشترك يستثني:', options:['x=5 فقط','x=1 فقط','x=5 و x=1'], correct:2}
        ]},

      {id:'p3-math-7', unit:'الوحدة الثانية: الجبر', title:'العمليات على الكسور الجبرية النسبية', meta:'2-5',
        sections:[
          {heading:'الجمع والطرح', body:'نوحّد المقام أولاً (بإيجاد أصغر مضاعف مشترك للمقامات)، ثم نجمع أو نطرح البسوط.\nمثال: 1/x + 2/(x+1) = ((x+1) + 2x) / (x(x+1)) = (3x+1)/(x(x+1))'},
          {heading:'الضرب', body:'نضرب البسط في البسط، والمقام في المقام، ويُفضّل التحليل والاختزال قبل الضرب لتسهيل الحل.\nمثال: (x/2) × (4/x²) = 4x/2x² = 2/x  (بشرط x≠0)'},
          {heading:'القسمة', body:'نضرب الكسر الأول في مقلوب الكسر الثاني.\nمثال: (x/3) ÷ (x²/6) = (x/3) × (6/x²) = 6x/3x² = 2/x  (بشرط x≠0)'},
          {heading:'تذكير مهم', body:'في كل عملية، حدد القيم الممنوعة لـ x (اللي بتخلي أي مقام = صفر) واكتبها كشرط مع إجابتك النهائية.'}
        ],
        quiz:[
          {q:'ناتج (2/x) × (x/6):', options:['1/3','2/6x','x²/6'], correct:0, explain:'2x/6x = 1/3 (بشرط x≠0).'},
          {q:'عند قسمة كسرين جبريين، نضرب الأول في:', options:['نفس الكسر الثاني','مقلوب الكسر الثاني','مقام الكسر الثاني فقط'], correct:1},
          {q:'قبل جمع كسرين جبريين مختلفي المقام، أول خطوة:', options:['نضرب المقامين في بعض مباشرة','نوحّد المقام بإيجاد أصغر مضاعف مشترك','نجمع البسوط مباشرة'], correct:1}
        ]},

      {id:'p3-math-8', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'تشابه المضلعات', meta:'3-1',
        sections:[
          {heading:'تعريف المضلعين المتشابهين', body:'مضلعان متشابهان إذا تحقق الشرطان معًا:\n1) زواياهما المتناظرة متساوية.\n2) أضلاعهما المتناظرة متناسبة (نسبها كلها متساوية).'},
          {heading:'نسبة التشابه', body:'هي النسبة الثابتة بين أطوال أي ضلعين متناظرين في المضلعين.\nمثال: لو ضلع في المضلع الأول = 6 سم، ونظيره في التاني = 3 سم، فنسبة التشابه = 6/3 = 2.'},
          {heading:'العلاقة بين المحيطين والمساحتين', body:'• نسبة المحيطين = نسبة التشابه نفسها.\n• نسبة المساحتين = مربع نسبة التشابه.\nمثال: لو نسبة التشابه 2، فنسبة المساحتين = 2² = 4.'}
        ],
        quiz:[
          {q:'مضلعان متشابهان نسبة التشابه بينهما 3، فنسبة مساحتيهما:', options:['3','6','9'], correct:2, explain:'نسبة المساحتين = مربع نسبة التشابه = 3²=9.'},
          {q:'شرط تشابه المضلعين:', options:['تساوي الأضلاع فقط','تساوي الزوايا وتناسب الأضلاع معًا','تساوي المساحة فقط'], correct:1},
          {q:'لو نسبة التشابه 1/2، فنسبة المحيطين:', options:['1/2','1/4','2'], correct:0, explain:'نسبة المحيطين = نسبة التشابه نفسها.'}
        ]},

      {id:'p3-math-9', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'تشابه المثلثات', meta:'3-2',
        sections:[
          {heading:'حالات تشابه المثلثات — ثلاث حالات', body:'1) حالة (ز.ز): تساوي زاويتين من المثلث الأول مع نظيرتيهما في الثاني.\n2) حالة (ض.ز.ض): تناسب ضلعين متناظرين مع تساوي الزاوية المحصورة بينهما.\n3) حالة (ض.ض.ض): تناسب الأضلاع الثلاثة المتناظرة كلها.'},
          {heading:'تطبيق: إيجاد طول مجهول', body:'لو مثلثان متشابهان وعرفنا نسبة التشابه، نقدر نوجد أي طول مجهول بعلاقة التناسب.\nمثال: مثلثان متشابهان، أضلاع الأول 4، 6، 8. الضلع المناظر لـ4 في الثاني طوله 6.\nنسبة التشابه = 6/4 = 3/2.\nإذن باقي الأضلاع في الثاني: 6×(3/2)=9 ، 8×(3/2)=12.'}
        ],
        quiz:[
          {q:'أسهل حالة لإثبات تشابه مثلثين هي:', options:['ز.ز','ض.ض.ض','ض.ز.ض'], correct:0, explain:'حالة ز.ز أبسط الحالات، فتساوي زاويتين كافٍ.'},
          {q:'مثلثان متشابهان بنسبة تشابه 2، ضلع في الأول طوله 5، فنظيره في الثاني:', options:['2.5','7','10'], correct:2, explain:'5×2=10.'},
          {q:'حالة ض.ز.ض تحتاج:', options:['تناسب ضلعين وتساوي الزاوية المحصورة بينهما','تساوي ثلاث زوايا','تناسب ثلاثة أضلاع'], correct:0}
        ]},

      {id:'p3-math-10', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'التمدد', meta:'3-3',
        sections:[
          {heading:'تعريف التمدد (Dilation)', body:'تحويل هندسي يُغيّر حجم الشكل (يكبّره أو يصغّره) حول نقطة ثابتة تسمى مركز التمدد، بمعامل تمدد k، مع الحفاظ على شكل الجسم (الشكل الناتج يشابه الأصلي).'},
          {heading:'معامل التمدد k', body:'• |k| > 1: تكبير.\n• 0 < |k| < 1: تصغير.\n• k سالب: مع انعكاس حول مركز التمدد.\n• |k| = 1: الشكل يبقى كما هو (تطابق).'},
          {heading:'إحداثيات النقطة بعد التمدد (مركزه نقطة الأصل)', body:'لو مركز التمدد نقطة الأصل (0,0)، فالنقطة (x,y) تتحول إلى (kx, ky).\nمثال: تمدد النقطة (3,4) بمعامل k=2 حول نقطة الأصل → (6,8).'}
        ],
        quiz:[
          {q:'تمدد بمعامل k=3 يعني:', options:['تصغير','تكبير','لا تغيير'], correct:1, explain:'|k|>1 فهو تكبير.'},
          {q:'صورة النقطة (2,5) بالتمدد حول نقطة الأصل بمعامل k=3:', options:['(5,8)','(6,15)','(2,15)'], correct:1, explain:'(2×3, 5×3) = (6,15).'},
          {q:'لو k=1/2، فالتمدد يكون:', options:['تكبير','تصغير','انعكاس فقط'], correct:1, explain:'0<|k|<1 فهو تصغير.'}
        ]},

      {id:'p3-math-11', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'النسب المثلثية للزوايا الحادة', meta:'3-4',
        sections:[
          {heading:'أضلاع المثلث القائم الزاوية', body:'بالنسبة لزاوية حادة معينة في المثلث القائم:\n• الوتر: الضلع المقابل للزاوية القائمة (أطول ضلع).\n• المقابل: الضلع المقابل للزاوية الحادة المدروسة.\n• المجاور: الضلع المجاور للزاوية الحادة (غير الوتر).'},
          {heading:'النسب المثلثية الثلاث الأساسية', body:'جا (الزاوية) = طول الضلع المقابل ÷ طول الوتر\nجتا (الزاوية) = طول الضلع المجاور ÷ طول الوتر\nظا (الزاوية) = طول الضلع المقابل ÷ طول الضلع المجاور'},
          {heading:'العلاقة بين النسب', body:'ظا (الزاوية) = جا(الزاوية) ÷ جتا(الزاوية)\nودي علاقة مهمة جدًا بتستخدم كتير في تبسيط المسائل.'}
        ],
        quiz:[
          {q:'جا الزاوية =', options:['المقابل ÷ المجاور','المقابل ÷ الوتر','المجاور ÷ الوتر'], correct:1},
          {q:'ظا الزاوية =', options:['جا ÷ جتا','جتا ÷ جا','جا × جتا'], correct:0},
          {q:'جتا الزاوية =', options:['المقابل ÷ الوتر','المجاور ÷ الوتر','المقابل ÷ المجاور'], correct:1}
        ]},

      {id:'p3-math-12', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'النسب المثلثية لبعض الزوايا الخاصة', meta:'3-5',
        sections:[
          {heading:'جدول القيم المشهور — احفظه غيبًا', body:'الزاوية 30°: جا=1/2 — جتا=√3/2 — ظا=1/√3 (=√3/3)\nالزاوية 45°: جا=√2/2 — جتا=√2/2 — ظا=1\nالزاوية 60°: جا=√3/2 — جتا=1/2 — ظا=√3'},
          {heading:'ملحوظة لتسهيل الحفظ', body:'لاحظ إن جا30°=جتا60° وجا60°=جتا30° — الزاويتان 30 و60 متكاملتان (مجموعهما 90°)، وجا الزاوية = جتا مكملتها دائمًا.\nوعند 45° تتساوى جا وجتا لأن الزاوية مكملة لنفسها.'},
          {heading:'مثال تطبيقي', body:'أوجد قيمة: جا60° × جتا30°\n= (√3/2) × (√3/2) = 3/4'}
        ],
        quiz:[
          {q:'قيمة جا30°:', options:['1/2','√3/2','1'], correct:0},
          {q:'قيمة ظا45°:', options:['0','1','√2'], correct:1},
          {q:'جا60° تساوي:', options:['جتا30°','جتا60°','ظا30°'], correct:0, explain:'الزاويتان 30 و60 متكاملتان، فجا إحداهما = جتا الأخرى.'},
          {q:'قيمة جتا60°:', options:['1/2','√3/2','1/√3'], correct:0}
        ]},

      {id:'p3-math-13', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'العلاقة بين ميلي المستقيمين المتوازيين والمتعامدين', meta:'3-6',
        sections:[
          {heading:'حساب ميل المستقيم', body:'ميل المستقيم المار بنقطتين (x₁,y₁) و(x₂,y₂):\nm = (y₂-y₁) / (x₂-x₁)'},
          {heading:'حالة التوازي', body:'مستقيمان متوازيان إذا وفقط إذا كان ميلاهما متساويين: m₁ = m₂'},
          {heading:'حالة التعامد', body:'مستقيمان متعامدان إذا وفقط إذا كان حاصل ضرب ميليهما = -1: m₁ × m₂ = -1\nبمعنى آخر: ميل أحدهما = المقلوب الضربي السالب لميل الآخر.'},
          {heading:'مثال محلول', body:'مستقيم ميله 2، أوجد ميل المستقيم العمودي عليه.\nm₂ = -1/2 (لأن 2 × (-1/2) = -1)'}
        ],
        quiz:[
          {q:'مستقيمان ميلاهما 3 و3، فهما:', options:['متوازيان','متعامدان','متقاطعان بزاوية 45°'], correct:0},
          {q:'مستقيم ميله 4، ميل المستقيم العمودي عليه:', options:['4','-4','-1/4'], correct:2, explain:'حاصل الضرب لازم يساوي -1: 4×(-1/4)=-1.'},
          {q:'شرط تعامد مستقيمين:', options:['m₁=m₂','m₁×m₂=-1','m₁+m₂=0'], correct:1},
          {q:'مستقيم ميله -2/3، ميل المستقيم العمودي عليه:', options:['2/3','-3/2','3/2'], correct:2}
        ]},

      {id:'p3-math-14', unit:'الوحدة الثالثة: التشابه وحساب المثلثات والإحداثيات', title:'معادلة الخط المستقيم', meta:'3-7',
        sections:[
          {heading:'الصورة الميلية (Slope-Intercept Form)', body:'y = mx + c\nحيث m الميل، و c هو الإحداثي y لنقطة تقاطع المستقيم مع محور y.'},
          {heading:'صورة النقطة والميل (Point-Slope Form)', body:'لو عارف ميل المستقيم m ونقطة عليه (x₁,y₁):\ny - y₁ = m(x - x₁)\nمفيدة جدًا لما تكون عارف نقطة وميل بس مش عارف نقطة تقاطع y.'},
          {heading:'الصورة العامة', body:'ax + by + c = 0'},
          {heading:'مثال محلول', body:'أوجد معادلة المستقيم المار بالنقطة (2,3) وميله 4.\ny - 3 = 4(x - 2)\ny - 3 = 4x - 8\ny = 4x - 5'}
        ],
        quiz:[
          {q:'معادلة مستقيم ميله 5 ويقطع محور y عند 2:', options:['y=5x+2','y=2x+5','y=5x-2'], correct:0},
          {q:'معادلة المستقيم المار بـ(1,4) وميله 3:', options:['y=3x+1','y=3x-1+4','y=3x+1... '], correct:1, explain:'y-4=3(x-1) → y=3x-3+4=3x+1.'},
          {q:'في الصورة y=mx+c، الرمز c يمثل:', options:['ميل المستقيم','نقطة تقاطع المستقيم مع محور y','نقطة تقاطع المستقيم مع محور x'], correct:1}
        ]},

      {id:'p3-math-15', unit:'الوحدة الرابعة: الإحصاء', title:'مقاييس التشتت', meta:'4-1',
        sections:[
          {heading:'ليه محتاجين مقاييس تشتت؟', body:'مقاييس النزعة المركزية (الوسط، الوسيط) بتوصف مركز البيانات بس، لكن مبتقولناش إذا كانت البيانات متجمعة حوالين الوسط أو متناثرة بعيد عنه. مقاييس التشتت بتقيس درجة التناثر ده.'},
          {heading:'المدى (Range)', body:'أبسط مقياس تشتت.\nالمدى = أكبر قيمة - أصغر قيمة\nعيبه: بيعتمد على قيمتين بس ومتأثر جدًا بالقيم الشاذة.'},
          {heading:'الانحراف المعياري (Standard Deviation)', body:'أدق وأشهر مقياس تشتت، بيقيس متوسط بُعد كل قيمة عن الوسط الحسابي.\nσ = √( Σ(x-x̄)² / n )\nخطوات الحساب: 1) احسب الوسط الحسابي x̄. 2) اطرح الوسط من كل قيمة وربّع الناتج. 3) اجمع كل المربعات واقسمها على عدد القيم n. 4) خذ الجذر التربيعي للناتج.'},
          {heading:'التباين (Variance)', body:'هو مربع الانحراف المعياري مباشرة: التباين = σ²\nيُستخدم كخطوة وسيطة في حساب الانحراف المعياري.'},
          {heading:'قاعدة عامة', body:'كل ما كان الانحراف المعياري أصغر، كل ما كانت البيانات متقاربة ومتجمعة حول الوسط. وكل ما كان أكبر، كل ما كانت البيانات متناثرة ومتباعدة.'}
        ],
        quiz:[
          {q:'المدى لمجموعة البيانات {4, 9, 2, 15, 7}:', options:['11','13','15'], correct:1, explain:'أكبر قيمة (15) - أصغر قيمة (2) = 13.'},
          {q:'التباين هو:', options:['جذر الانحراف المعياري','مربع الانحراف المعياري','نفس الانحراف المعياري'], correct:1},
          {q:'انحراف معياري صغير جدًا يعني:', options:['البيانات متناثرة جدًا','البيانات متقاربة حول الوسط','لا يوجد وسط حسابي'], correct:1},
          {q:'أول خطوة في حساب الانحراف المعياري:', options:['حساب المدى','حساب الوسط الحسابي','ترتيب البيانات تصاعديًا'], correct:1}
        ]}
    ]},
    science:{label:'العلوم', icon:'flask', lessons:[
      {id:'p3-sci-1', unit:'الوحدة الأولى: التفاعلات الكيميائية وآثارها البيئية', title:'أنواع التفاعلات الكيميائية', meta:'الدرس الأول',
        sections:[
          {heading:'إيه هو التفاعل الكيميائي؟', body:'عملية بيتكسّر فيها الروابط بين ذرات المواد المتفاعلة، وتتكوّن روابط جديدة، فتتحول المواد المتفاعلة (المتفاعلات) إلى مواد جديدة (نواتج) ليها خواص مختلفة تمامًا عن المواد الأصلية.'},
          {heading:'علامات حدوث تفاعل كيميائي', body:'• تغيّر اللون.\n• تصاعد غاز (فقاقيع).\n• تكوّن راسب (مادة صلبة جديدة).\n• تغيّر درجة الحرارة (التفاعل يطلق حرارة أو يمتصها).\n• انبعاث ضوء في بعض الأحيان.'},
          {heading:'أنواع التفاعلات الكيميائية — أربعة أنواع', body:'1) تفاعل الاتحاد (التركيب): مادتان أو أكتر بيتحدوا ليكوّنوا مادة واحدة جديدة.\n   مثال: 2H₂ + O₂ → 2H₂O (اتحاد الهيدروجين والأكسجين لتكوين الماء).\n2) تفاعل التحلل: مادة واحدة بتتفكك لمادتين أو أكتر أبسط منها (غالبًا بالحرارة).\n   مثال: تحلل كربونات الكالسيوم بالتسخين إلى أكسيد الكالسيوم وثاني أكسيد الكربون.\n3) تفاعل الإحلال الأحادي: عنصر نشط بيحل محل عنصر أقل نشاطًا في مركب.\n   مثال: الحديد يحل محل النحاس في محلول كبريتات النحاس.\n4) تفاعل الإحلال الثنائي (المزدوج): تبادل بين مركبين لتكوين مركبين جديدين، وغالبًا بيتكوّن راسب.\n   مثال: نترات الفضة + كلوريد الصوديوم → كلوريد الفضة (راسب) + نترات الصوديوم.'},
          {heading:'تصنيف حراري للتفاعلات', body:'• تفاعل طارد للحرارة: بيُطلق حرارة للوسط المحيط (زي الاحتراق).\n• تفاعل ماص للحرارة: بيمتص حرارة من الوسط المحيط (زي التحلل بالحرارة).'}
        ],
        quiz:[
          {q:'اتحاد الهيدروجين والأكسجين لتكوين الماء مثال على تفاعل:', options:['التحلل','الاتحاد','الإحلال الأحادي'], correct:1, explain:'مادتان اتحدوا ليكوّنوا مادة واحدة جديدة، فهو تفاعل اتحاد.'},
          {q:'تفاعل الحديد مع كبريتات النحاس ليحل محل النحاس هو تفاعل:', options:['إحلال أحادي','إحلال ثنائي','تحلل'], correct:0, explain:'عنصر واحد (الحديد) حل محل عنصر آخر (النحاس) في المركب.'},
          {q:'من علامات حدوث التفاعل الكيميائي:', options:['ثبات اللون دائمًا','تكوّن راسب أو تصاعد غاز','عدم تغير درجة الحرارة أبدًا'], correct:1},
          {q:'التفاعل الذي يُطلق حرارة للوسط المحيط يُسمى:', options:['ماصًا للحرارة','طاردًا للحرارة','متعادلًا'], correct:1}
        ]},

      {id:'p3-sci-2', unit:'الوحدة الأولى: التفاعلات الكيميائية وآثارها البيئية', title:'تفاعلات الاحتراق والتلوث البيئي', meta:'الدرس الثاني',
        sections:[
          {heading:'تعريف الاحتراق', body:'تفاعل كيميائي سريع بين مادة قابلة للاشتعال (وقود) والأكسجين، ينتج عنه حرارة وضوء، وهو من التفاعلات الطاردة للحرارة.'},
          {heading:'نوعا الاحتراق', body:'• الاحتراق الكامل: بوجود كمية كافية من الأكسجين، وينتج عنه ثاني أكسيد الكربون وبخار الماء فقط.\n• الاحتراق غير الكامل: عند نقص الأكسجين، وينتج عنه أول أكسيد الكربون (غاز سام) والسخام (الكربون الأسود)، وهو أخطر على البيئة والصحة.'},
          {heading:'مصادر التلوث الناتج عن الاحتراق', body:'احتراق الوقود الأحفوري (البنزين والسولار والفحم) في وسائل النقل والمصانع ومحطات توليد الكهرباء، وهو المصدر الأكبر لتلوث الهواء.'},
          {heading:'الآثار البيئية للاحتراق', body:'• انبعاث غازات ضارة: أول أكسيد الكربون، أكاسيد النيتروجين، أكاسيد الكبريت.\n• المطر الحمضي: نتيجة تفاعل أكاسيد الكبريت والنيتروجين مع بخار الماء في الجو.\n• تفاقم الاحتباس الحراري: بسبب زيادة ثاني أكسيد الكربون (أهم غازات الاحتباس الحراري).\n• أضرار صحية: أمراض الجهاز التنفسي والحساسية الصدرية.'},
          {heading:'طرق الحد من التلوث', body:'استخدام الطاقة المتجددة (الشمسية والرياح)، تركيب أجهزة تنقية العادم في السيارات والمصانع، التشجير، وترشيد استهلاك الوقود.'}
        ],
        quiz:[
          {q:'ناتج الاحتراق غير الكامل الخطير على الصحة:', options:['ثاني أكسيد الكربون','أول أكسيد الكربون','بخار الماء'], correct:1, explain:'الاحتراق غير الكامل (نقص الأكسجين) ينتج أول أكسيد الكربون السام.'},
          {q:'أهم غاز مسؤول عن ظاهرة الاحتباس الحراري:', options:['الأكسجين','ثاني أكسيد الكربون','النيتروجين'], correct:1},
          {q:'المطر الحمضي ينتج بشكل أساسي من:', options:['أكاسيد الكبريت والنيتروجين','بخار الماء النقي','الأكسجين'], correct:0},
          {q:'من طرق الحد من التلوث الناتج عن الاحتراق:', options:['زيادة استخدام الوقود الأحفوري','استخدام الطاقة المتجددة','إزالة الأشجار'], correct:1}
        ]},

      {id:'p3-sci-3', unit:'الوحدة الأولى: التفاعلات الكيميائية وآثارها البيئية', title:'التدخين ومخاطره', meta:'الدرس الثالث',
        sections:[
          {heading:'محتويات دخان السجائر', body:'يحتوي دخان السجائر على آلاف المواد الكيميائية الضارة، أهمها:\n• النيكوتين: مادة مسببة للإدمان، تؤثر على الجهاز العصبي وتزيد ضربات القلب وضغط الدم.\n• القطران: مادة لزجة مسرطنة تترسب في الرئتين.\n• أول أكسيد الكربون: يقلل قدرة كرات الدم الحمراء على حمل الأكسجين لأنسجة الجسم.'},
          {heading:'الأضرار الصحية للتدخين', body:'• أمراض الجهاز التنفسي: سرطان الرئة، الالتهاب الشعبي المزمن، انتفاخ الرئة.\n• أمراض القلب والأوعية الدموية: تصلب الشرايين، ارتفاع ضغط الدم، الجلطات.\n• إضعاف جهاز المناعة وزيادة التعرض للعدوى.\n• أضرار بالفم والأسنان واصفرارها.'},
          {heading:'التدخين السلبي', body:'استنشاق غير المدخنين (خصوصًا الأطفال والحوامل) لدخان السجائر المحيط بهم يعرضهم لمخاطر صحية مشابهة تقريبًا لمخاطر المدخن نفسه.'},
          {heading:'الوقاية والتوعية', body:'الوقاية من بداية عدم التدخين خير وسيلة، ونشر الوعي بمخاطره الصحية والاجتماعية والاقتصادية يحمي الفرد والمجتمع.'}
        ],
        quiz:[
          {q:'المادة المسببة للإدمان في دخان السجائر:', options:['القطران','النيكوتين','أول أكسيد الكربون'], correct:1},
          {q:'المادة المسرطنة في دخان السجائر:', options:['القطران','الأكسجين','بخار الماء'], correct:0},
          {q:'أول أكسيد الكربون في دخان السجائر يؤثر بشكل أساسي على:', options:['قدرة الدم على حمل الأكسجين','لون الأسنان فقط','حاسة الشم'], correct:0},
          {q:'التدخين السلبي يقصد به:', options:['تدخين السجائر الإلكترونية','استنشاق غير المدخن لدخان المدخنين','التدخين في الهواء الطلق'], correct:1}
        ]},

      {id:'p3-sci-4', unit:'الوحدة الثانية: الكهرباء والمغناطيسية', title:'التيار الكهربائي', meta:'الدرس الأول',
        sections:[
          {heading:'تعريف التيار الكهربائي', body:'معدل سريان الشحنات الكهربية (الإلكترونات) خلال موصل في وحدة الزمن. وحدة قياسه الأمبير (A)، ويُقاس بجهاز الأميتر.'},
          {heading:'شروط سريان التيار الكهربائي', body:'1) وجود مصدر للقوة الدافعة الكهربية (كالبطارية).\n2) وجود دائرة كهربية مغلقة متصلة بالكامل (موصلة).'},
          {heading:'نوعا التيار الكهربائي', body:'• التيار المستمر (DC): يسري في اتجاه واحد ثابت، ومصدره البطاريات والخلايا الشمسية.\n• التيار المتردد (AC): يتغير اتجاهه بصفة دورية ومنتظمة، وهو التيار المستخدم في شبكات الكهرباء المنزلية.'},
          {heading:'الموصلات والعوازل', body:'• الموصلات: مواد تسمح بمرور التيار الكهربي بسهولة لوجود إلكترونات حرة الحركة فيها، مثل: النحاس، الفضة، الألومنيوم (المعادن عمومًا).\n• العوازل: مواد لا تسمح بمرور التيار الكهربي، مثل: المطاط، البلاستيك، الزجاج، الخشب الجاف.'}
        ],
        quiz:[
          {q:'وحدة قياس شدة التيار الكهربائي:', options:['الفولت','الأمبير','الأوم'], correct:1},
          {q:'التيار الذي يتغير اتجاهه بصفة دورية يُسمى:', options:['مستمرًا','مترددًا','ثابتًا'], correct:1},
          {q:'من أمثلة المواد العازلة للكهرباء:', options:['النحاس','المطاط','الفضة'], correct:1},
          {q:'من شروط سريان التيار الكهربائي:', options:['دائرة كهربية مفتوحة','وجود مصدر للقوة الدافعة ودائرة مغلقة','عدم وجود موصلات'], correct:1}
        ]},

      {id:'p3-sci-5', unit:'الوحدة الثانية: الكهرباء والمغناطيسية', title:'الدائرة الكهربائية', meta:'الدرس الثاني',
        sections:[
          {heading:'مكونات الدائرة الكهربية', body:'• مصدر للتيار: كالبطارية، يوفر القوة الدافعة الكهربية.\n• موصلات: أسلاك توصيل من مادة موصلة كالنحاس.\n• حمل كهربي: كالمصباح أو أي جهاز يستهلك الطاقة الكهربية.\n• مفتاح: للتحكم في فتح وغلق الدائرة.'},
          {heading:'التوصيل على التوالي (Series)', body:'العناصر تُوصل الواحد بعد الآخر في مسار واحد فقط.\n• شدة التيار نفسها في كل نقطة من الدائرة.\n• لو انقطع أي جزء (زي احتراق مصباح)، يتوقف التيار في الدائرة كلها.'},
          {heading:'التوصيل على التوازي (Parallel)', body:'العناصر تُوصل في مسارات (فروع) متعددة جنبًا إلى جنب.\n• فرق الجهد ثابت وواحد على كل فرع.\n• لو انقطع فرع، تستمر باقي الفروع في العمل (زي توصيلات المنازل).'},
          {heading:'أجهزة القياس ورموزها', body:'• الأميتر: لقياس شدة التيار، يُوصل على التوالي في الدائرة.\n• الفولتميتر: لقياس فرق الجهد، يُوصل على التوازي مع العنصر المراد قياسه.'}
        ],
        quiz:[
          {q:'في التوصيل على التوالي، لو احترق مصباح واحد:', options:['تستمر باقي المصابيح في الإضاءة','تنطفئ كل المصابيح لأن الدائرة تنقطع','لا يتأثر شيء'], correct:1, explain:'التوصيل على التوالي مسار واحد، فانقطاعه يوقف التيار بالكامل.'},
          {q:'جهاز الأميتر يُوصل في الدائرة:', options:['على التوالي','على التوازي','لا يُوصل في الدائرة'], correct:0},
          {q:'توصيلات الكهرباء في المنازل غالبًا تكون على:', options:['التوالي','التوازي','لا توصيل'], correct:1, explain:'التوازي يسمح باستمرار عمل باقي الأجهزة لو تعطل جهاز واحد.'},
          {q:'الفولتميتر يقيس:', options:['شدة التيار','فرق الجهد','المقاومة'], correct:1}
        ]},

      {id:'p3-sci-6', unit:'الوحدة الثانية: الكهرباء والمغناطيسية', title:'القوة الكهربائية والمغناطيسية', meta:'الدرس الثالث',
        sections:[
          {heading:'القوة الكهربية بين الشحنات', body:'الشحنات المتشابهة (موجبة مع موجبة، أو سالبة مع سالبة) تتنافر، والشحنات المختلفة (موجبة مع سالبة) تتجاذب.\nتزداد قوة التجاذب أو التنافر كلما زادت مقدار الشحنتين، وتقل كلما زادت المسافة بينهما.'},
          {heading:'القوة المغناطيسية', body:'لكل مغناطيس قطبان: شمالي وجنوبي.\nالأقطاب المتشابهة تتنافر، والأقطاب المختلفة تتجاذب.\nتحيط بالمغناطيس منطقة تأثير تسمى المجال المغناطيسي.'},
          {heading:'الكهرومغناطيسية — العلاقة بين الكهرباء والمغناطيسية', body:'مرور تيار كهربي في سلك موصل يولّد حوله مجالًا مغناطيسيًا.\nلو لف السلك على شكل ملف حول قلب من الحديد، تتكوّن مغناطيسية أقوى بكثير، وده أساس المغناطيس الكهربي (Electromagnet).'},
          {heading:'تطبيقات الكهرومغناطيسية', body:'الجرس الكهربي، المحرك الكهربي (تحويل الطاقة الكهربية لحركية)، الرافعات الكهرومغناطيسية المستخدمة في رفع الخردة المعدنية.'}
        ],
        quiz:[
          {q:'شحنتان متشابهتان في النوع بينهما:', options:['تجاذب','تنافر','لا تأثير'], correct:1},
          {q:'مرور تيار كهربي في سلك موصل ينتج عنه:', options:['مجال مغناطيسي حول السلك','لا شيء','فقدان الشحنة'], correct:0, explain:'هذا أساس الكهرومغناطيسية.'},
          {q:'الأقطاب المغناطيسية المختلفة (شمالي وجنوبي):', options:['تتنافر','تتجاذب','لا تتأثر ببعضها'], correct:1},
          {q:'من تطبيقات الكهرومغناطيسية:', options:['الجرس الكهربي والمحرك الكهربي','التصوير الفوتوغرافي','قياس درجة الحرارة'], correct:0}
        ]},

      {id:'p3-sci-7', unit:'الوحدة الثالثة: تنوع الصفات في الكائنات الحية', title:'الوراثة وتنوع الصفات', meta:'الدرس الأول',
        sections:[
          {heading:'ما هي الوراثة؟', body:'انتقال الصفات من الآباء إلى الأبناء عبر الأجيال المتعاقبة، عن طريق المادة الوراثية (DNA) الموجودة على الكروموسومات داخل نواة الخلية.'},
          {heading:'الجينات', body:'وحدات المادة الوراثية المسؤولة عن ظهور الصفات المختلفة (كلون العين أو فصيلة الدم)، وتوجد مرتبة على الكروموسومات، ويرث الفرد نسخة من كل والد.'},
          {heading:'الصفات السائدة والمتنحية', body:'• الصفة السائدة: تظهر في الفرد حتى لو وُجد بجانبها جين متنحٍ (يكفي نسخة واحدة من الجين السائد لتظهر الصفة).\n• الصفة المتنحية: لا تظهر إلا إذا اجتمع جينان متنحيان معًا (نسخة من كل والد).'},
          {heading:'مصادر تنوع الصفات', body:'• الطفرات الوراثية: تغيرات مفاجئة في المادة الوراثية.\n• إعادة التوزيع الجيني أثناء التكاثر الجنسي: اختلاط جينات الأبوين بطرق متعددة.\n• العوامل البيئية: قد تؤثر في ظهور بعض الصفات.'}
        ],
        quiz:[
          {q:'المادة المسؤولة عن نقل الصفات الوراثية:', options:['DNA الموجود في الكروموسومات','السيتوبلازم','الغشاء الخلوي'], correct:0},
          {q:'الصفة التي تظهر في الفرد حتى بوجود جين متنحٍ معها تُسمى:', options:['متنحية','سائدة','مختلطة'], correct:1},
          {q:'الصفة المتنحية تظهر عندما:', options:['يجتمع جينان متنحيان من الأبوين','يوجد جين سائد واحد فقط','لا تظهر أبدًا'], correct:0},
          {q:'من مصادر تنوع الصفات بين الأفراد:', options:['الطفرات الوراثية','ثبات الجينات دائمًا','غياب التكاثر الجنسي'], correct:0}
        ]},

      {id:'p3-sci-8', unit:'الوحدة الثالثة: تنوع الصفات في الكائنات الحية', title:'الانتخاب الطبيعي والانتخاب الصناعي', meta:'الدرس الثاني',
        sections:[
          {heading:'الانتخاب الطبيعي (نظرية داروين)', body:'العملية التي تبقى فيها الكائنات الأصلح للتكيّف مع بيئتها على قيد الحياة وتتكاثر وتنقل صفاتها المفيدة للأجيال التالية، بينما تقل أو تنقرض الكائنات الأقل تكيّفًا، وذلك عبر فترات زمنية طويلة.'},
          {heading:'أمثلة على الانتخاب الطبيعي', body:'• تغيّر لون فراشات العث في إنجلترا أثناء الثورة الصناعية، حيث زاد انتشار اللون الداكن المموّه مع تلوث جذوع الأشجار بالسخام.\n• تطور مقاومة بعض أنواع البكتيريا للمضادات الحيوية بمرور الوقت.'},
          {heading:'الانتخاب الصناعي (الاصطناعي)', body:'تدخل الإنسان بشكل مقصود لاختيار وتربية الكائنات ذات الصفات المرغوبة (كإنتاجية أعلى للحليب أو مقاومة أكبر للأمراض)، وتربيتها عبر أجيال متتالية لتحسين السلالات في الزراعة وتربية الحيوان.'},
          {heading:'الفرق الجوهري بين النوعين', body:'الانتخاب الطبيعي تتحكم فيه عوامل البيئة بدون أي تدخل بشري، بينما الانتخاب الصناعي يتحكم فيه اختيار الإنسان المتعمد لتحقيق هدف معين.'}
        ],
        quiz:[
          {q:'العملية التي تبقي الكائنات الأصلح للبيئة على قيد الحياة تُسمى:', options:['الانتخاب الصناعي','الانتخاب الطبيعي','الطفرة'], correct:1},
          {q:'تربية الإنسان لسلالة أبقار عالية إنتاج اللبن مثال على:', options:['الانتخاب الطبيعي','الانتخاب الصناعي','الانقراض'], correct:1},
          {q:'الفرق الأساسي بين الانتخاب الطبيعي والصناعي هو:', options:['وجود تدخل الإنسان من عدمه','السرعة فقط','النوع فقط'], correct:0},
          {q:'تغيّر لون فراشات العث أثناء الثورة الصناعية مثال على:', options:['الانتخاب الصناعي','الانتخاب الطبيعي','التدخل البشري المباشر'], correct:1}
        ]},

      {id:'p3-sci-9', unit:'الوحدة الرابعة: تاريخ كوكب الأرض', title:'السجل الحفري', meta:'الدرس الأول',
        sections:[
          {heading:'تعريف الحفريات (المستحفرات)', body:'بقايا أو آثار كائنات حية عاشت في الماضي الجيولوجي البعيد، وتحجّرت أو حُفظت داخل الصخور الرسوبية عبر ملايين السنين.'},
          {heading:'كيف تتكوّن الحفريات؟', body:'غالبًا عند موت الكائن ودفنه سريعًا تحت طبقات من الرواسب (كالطين أو الرمل) قبل أن يتحلل بالكامل، ثم مع مرور الزمن تتصلب الرواسب المحيطة إلى صخر، وقد تُستبدل الأنسجة العضوية تدريجيًا بمعادن في عملية تُسمى التحجر.'},
          {heading:'أنواع حفظ الحفريات', body:'• التحجر الكامل: استبدال الأنسجة بمعادن.\n• الطبعات والقوالب: أثر شكل الكائن في الصخر بعد اختفاء جسمه.\n• الحفظ الكامل: في الكهرمان (الراتنج المتحجر) أو الجليد أو القار، وتحفظ حتى الأنسجة الطرية أحيانًا.'},
          {heading:'أهمية السجل الحفري', body:'• معرفة تاريخ الحياة على الأرض وتطور الكائنات عبر العصور المختلفة.\n• تحديد العمر النسبي لطبقات الصخور باستخدام الحفريات الدليلية.\n• فهم البيئات والمناخات القديمة التي عاشت فيها الكائنات.'}
        ],
        quiz:[
          {q:'الحفريات هي:', options:['كائنات حية معاصرة','بقايا أو آثار كائنات عاشت في الماضي الجيولوجي','صخور بركانية فقط'], correct:1},
          {q:'من شروط تكوّن الحفريات بشكل جيد:', options:['دفن الكائن سريعًا تحت الرواسب','بقاء الكائن مكشوفًا للهواء لفترة طويلة','ارتفاع درجة الحرارة الشديد فقط'], correct:0},
          {q:'حفظ حشرة كاملة داخل الكهرمان مثال على:', options:['التحجر الكامل','الطبعات والقوالب','الحفظ الكامل'], correct:2},
          {q:'من أهم استخدامات السجل الحفري:', options:['تحديد العمر النسبي للطبقات الصخرية','التنبؤ بالطقس اليومي','قياس شدة التيار الكهربي'], correct:0}
        ]},

      {id:'p3-sci-10', unit:'الوحدة الرابعة: تاريخ كوكب الأرض', title:'الأزمنة الجيولوجية', meta:'الدرس الثاني',
        sections:[
          {heading:'مقياس الزمن الجيولوجي', body:'قسّم العلماء عمر الأرض (المقدَّر بحوالي 4.6 مليار سنة) إلى وحدات زمنية كبرى (دهور وعصور)، بناءً على التغيرات الكبرى في طبقات الصخور وأنواع الحفريات الموجودة فيها.'},
          {heading:'الدهور الجيولوجية الكبرى (من الأقدم للأحدث)', body:'1) الدهر السحيق (ما قبل الكمبري): أقدم وأطول الدهور، وشهد ظهور أول أشكال الحياة البسيطة.\n2) دهر الحياة القديمة: ظهور الحياة البحرية المتنوعة والأسماك والنباتات والحشرات الأولى.\n3) دهر الحياة المتوسطة: يُعرف بعصر الديناصورات، وشهد أيضًا ظهور أولى الطيور والثدييات الصغيرة.\n4) دهر الحياة الحديثة: بعد انقراض الديناصورات، وشهد ازدهار الثدييات وظهور وتطور الإنسان.'},
          {heading:'كيف يحدد العلماء عمر الصخور؟', body:'• مبدأ تعاقب الطبقات: الطبقة الصخرية الأسفل أقدم من التي فوقها (في الأوضاع الطبيعية غير المضطربة).\n• التأريخ الإشعاعي: قياس معدل تحلل العناصر المشعة (كاليورانيوم أو الكربون-14) الموجودة في الصخر أو الحفرية لحساب عمرها بدقة.\n• الحفريات الدليلية: أنواع معينة من الكائنات عاشت فترة قصيرة وانتشرت على مساحات واسعة، فوجودها يدل على عمر محدد للطبقة.'},
          {heading:'أهمية دراسة الأزمنة الجيولوجية', body:'فهم كيفية تطور الحياة على الأرض عبر ملايين السنين، والمساعدة في التنقيب عن الموارد الطبيعية (كالبترول والفحم) المرتبطة بعصور جيولوجية معينة.'}
        ],
        quiz:[
          {q:'عصر الديناصورات ينتمي إلى:', options:['الدهر السحيق','دهر الحياة المتوسطة','دهر الحياة الحديثة'], correct:1},
          {q:'حسب مبدأ تعاقب الطبقات، الطبقة الصخرية السفلى تكون:', options:['أحدث من العلوية','أقدم من العلوية','لا علاقة بالعمر'], correct:1},
          {q:'من طرق تحديد عمر الصخور بدقة:', options:['التأريخ الإشعاعي','قياس درجة الحرارة الحالية','عد عدد الأشجار المحيطة'], correct:0},
          {q:'ظهور الإنسان وتطوره يرتبط بشكل أساسي بـ:', options:['الدهر السحيق','دهر الحياة القديمة','دهر الحياة الحديثة'], correct:2}
        ]}
    ]},
    social:{label:'الدراسات', icon:'map', lessons:[]}
  }}
};

/* ============================================================
   STATE + PERSISTENCE (localStorage — works once deployed online)
   ============================================================ */
let state = { grade:'prep3', subject:null, lesson:null };

function loadProgress(){
  try{ return JSON.parse(localStorage.getItem('abtal_progress')||'{}'); }catch(e){ return {}; }
}
function saveProgress(p){ localStorage.setItem('abtal_progress', JSON.stringify(p)); }
function markStudied(lessonId){
  const p = loadProgress(); p[lessonId] = p[lessonId]||{}; p[lessonId].studied = true; saveProgress(p);
}
function saveScore(lessonId, score, total){
  const p = loadProgress(); p[lessonId] = p[lessonId]||{};
  if(!p[lessonId].best || p[lessonId].best < score) p[lessonId].best = score;
  p[lessonId].total = total; saveProgress(p);
}

/* ============================================================
   NAV
   ============================================================ */
function switchTab(pageId, navId){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('nav.tabs button').forEach(b=>b.classList.remove('active'));
  document.getElementById(pageId).classList.add('active');
  document.getElementById(navId).classList.add('active');
  window.scrollTo(0,0);
}

function renderGradeTabs(){
  const row = document.getElementById('gradeRow');
  row.innerHTML='';
  Object.keys(CURRICULUM).forEach(gKey=>{
    const b = document.createElement('button');
    b.className = 'grade-btn' + (gKey===state.grade?' active':'');
    b.innerText = CURRICULUM[gKey].label;
    b.onclick = ()=>{ state.grade=gKey; state.subject=null; renderGradeTabs(); showSubjects(); };
    row.appendChild(b);
  });
}

function showSubjects(){
  document.getElementById('subjectsView').style.display='block';
  document.getElementById('lessonsView').style.display='none';
  document.getElementById('lessonDetailView').style.display='none';
  document.getElementById('gradeTitle').innerText = CURRICULUM[state.grade].label;
  const grid = document.getElementById('subjectGrid');
  grid.innerHTML='';
  const subjects = CURRICULUM[state.grade].subjects;
  const ICON_COLORS = { book:'#1e88e5', globe:'#2e7d32', calc:'#e07b1f', flask:'#7b4fc9', map:'#c0392b' };
  Object.keys(subjects).forEach(sKey=>{
    const s = subjects[sKey];
    const card = document.createElement('div');
    card.className='subject-card';
    const color = ICON_COLORS[s.icon] || 'var(--navy2)';
    card.innerHTML = `<div class="icon-circle" style="background:${color}">${ICONS[s.icon]}</div><h3>${s.label}</h3><div class="count">${s.lessons.length} درس متاح</div>`;
    card.onclick = ()=>{ state.subject=sKey; showLessons(); };
    grid.appendChild(card);
  });
}

function backToSubjects(){
  document.getElementById('subjectsView').style.display='block';
  document.getElementById('lessonsView').style.display='none';
  document.getElementById('lessonDetailView').style.display='none';
}

function showLessons(){
  document.getElementById('subjectsView').style.display='none';
  document.getElementById('lessonsView').style.display='block';
  document.getElementById('lessonDetailView').style.display='none';
  const subject = CURRICULUM[state.grade].subjects[state.subject];
  document.getElementById('subjectTitle').innerText = subject.label + ' — ' + CURRICULUM[state.grade].label;
  const list = document.getElementById('lessonList');
  list.innerHTML='';
  const progress = loadProgress();
  let currentUnit = null;
  if(subject.lessons.length===0){
    list.innerHTML = `<div class="empty-note">لسه مفيش دروس متاحة في المادة دي للصف ده. الموقع مبني بحيث يتضاف له محتوى بسهولة — لو محتاج تضيف درس جديد، اسأل المساعد الذكي يساعدك تجهزه.</div>`;
    return;
  }
  subject.lessons.forEach(lesson=>{
    const unitName = lesson.unit || 'دروس إضافية';
    if(unitName !== currentUnit){
      currentUnit = unitName;
      const head = document.createElement('div');
      head.className='unit-head';
      head.innerHTML = `<span>${unitName}</span>`;
      list.appendChild(head);
    }
    const row = document.createElement('div');
    row.className='lesson-row';
    const p = progress[lesson.id];
    row.innerHTML = `<div class="name">${lesson.title}${p&&p.studied?'<span class="done">تمت المذاكرة ✓</span>':''}</div>
      <button class="btn btn-ink">ذاكر الدرس</button>`;
    row.querySelector('button').onclick = ()=>openLesson(lesson);
    list.appendChild(row);
  });
}

function openLesson(lesson){
  state.lesson = lesson;
  document.getElementById('subjectsView').style.display='none';
  document.getElementById('lessonsView').style.display='none';
  const view = document.getElementById('lessonDetailView');
  view.style.display='block';
  markStudied(lesson.id);

  let html = `
    <button class="btn btn-ghost" style="margin-bottom:20px" onclick="showLessons()">⟵ رجوع للدروس</button>
    <div class="lesson-head">
      <div><h1>${lesson.title}</h1><div class="meta">${lesson.meta||''}</div></div>
    </div>
    <div class="listen-bar">
      <button class="icon-btn" onclick="readLesson()" title="استماع">🔊</button>
      <button class="icon-btn" onclick="stopReading()" title="إيقاف">⏹</button>
      <span>استمع للدرس بدل القراءة لو حابب تريّح عينيك</span>
    </div>`;

  if(lesson.quranText){
    html += `<div class="quran-box">${lesson.quranText}</div>`;
  }
  if(lesson.tafsir){
    html += `<div class="block"><h2>الشرح والتفسير</h2>`;
    lesson.tafsir.forEach(t=>{ html += `<div class="tafsir-card"><h4>${t.title}</h4><p>${t.body}</p></div>`; });
    html += `</div>`;
  }
  if(lesson.sections){
    html += `<div class="block"><h2>شرح الدرس</h2>`;
    lesson.sections.forEach(s=>{ html += `<div class="tafsir-card"><h4>${s.heading}</h4><p>${s.body.replace(/\n/g,'<br>')}</p></div>`; });
    html += `</div>`;
  }
  if(lesson.vocab){
    html += `<div class="block"><h2>المفردات</h2><table class="vocab"><thead><tr><th>الكلمة</th><th>المعنى</th><th>المضاد</th></tr></thead><tbody>`;
    lesson.vocab.forEach(v=>{ html += `<tr><td>${v.word}</td><td>${v.meaning}</td><td>${v.opp}</td></tr>`; });
    html += `</tbody></table></div>`;
  }
  if(lesson.balagha){
    html += `<div class="block"><h2>مواطن الجمال</h2><ul class="balagha">`;
    lesson.balagha.forEach(b=>{ html += `<li>${b}</li>`; });
    html += `</ul></div>`;
  }

  html += `<hr class="divider">
    <div id="quizArea">
      <h2 class="section-title">اختبر نفسك</h2>
      <div id="quizQuestions"></div>
      <button class="btn btn-red" onclick="checkQuiz()">تسليم الإجابات ومعرفة النتيجة</button>
      <div class="result-box" id="resultBox"><div>نتيجتك</div><div class="score" id="scoreText"></div><button class="btn btn-ink" onclick="showLessons()">رجوع للدروس</button></div>
    </div>`;

  view.innerHTML = html;
  renderQuiz(lesson.quiz);
}

/* ---------- quiz engine ---------- */
function renderQuiz(questions){
  const box = document.getElementById('quizQuestions');
  box.innerHTML='';
  questions.forEach((q,qi)=>{
    const qDiv = document.createElement('div');
    qDiv.className='quiz-q';
    let optsHtml='';
    q.options.forEach((opt,oi)=>{
      optsHtml += `<label class="opt" id="opt-${qi}-${oi}"><input type="radio" name="q${qi}" value="${oi}"> ${opt}</label>`;
    });
    qDiv.innerHTML = `<p class="qtext">${qi+1}. ${q.q}</p>${optsHtml}`;
    box.appendChild(qDiv);
  });
}
function checkQuiz(){
  const quiz = state.lesson.quiz;
  let score=0;
  quiz.forEach((q,qi)=>{
    const chosen = document.querySelector(`input[name="q${qi}"]:checked`);
    const correctLabel = document.getElementById(`opt-${qi}-${q.correct}`);
    correctLabel.classList.add('correct');
    if(chosen){
      const val = parseInt(chosen.value);
      if(val===q.correct) score++;
      else document.getElementById(`opt-${qi}-${val}`).classList.add('wrong');
    }
  });
  document.getElementById('resultBox').style.display='block';
  document.getElementById('scoreText').innerText = `${score} / ${quiz.length}`;
  saveScore(state.lesson.id, score, quiz.length);
}

/* ---------- text-to-speech (plain browser voice, honestly labelled) ---------- */
function collectLessonText(lesson){
  let t = lesson.title + '. ';
  if(lesson.quranText) t += lesson.quranText + '. ';
  if(lesson.tafsir) lesson.tafsir.forEach(x=> t += x.title + '. ' + x.body + ' ');
  if(lesson.sections) lesson.sections.forEach(x=> t += x.heading + '. ' + x.body + ' ');
  return t;
}
function readLesson(){
  if(!('speechSynthesis' in window)) return alert('متصفحك لا يدعم خاصية القراءة الصوتية.');
  window.speechSynthesis.cancel();
  const u = new SpeechSynthesisUtterance(collectLessonText(state.lesson));
  u.lang='ar-SA'; u.rate=0.92;
  window.speechSynthesis.speak(u);
}
function stopReading(){ if('speechSynthesis' in window) window.speechSynthesis.cancel(); }

/* ============================================================
   AI ASSISTANT — calls Gemini directly from the browser using
   a key the user provides and stores in localStorage.
   ============================================================ */
function getApiKey(){ return localStorage.getItem('abtal_gemini_key') || ''; }

function saveApiKey(){
  const val = document.getElementById('apiKeyInput').value.trim();
  if(!val) return;
  localStorage.setItem('abtal_gemini_key', val);
  document.getElementById('keyPanel').style.display='none';
  document.getElementById('chatShell').style.display='flex';
}
function showKeyPanel(){
  document.getElementById('keyPanel').style.display='block';
  document.getElementById('chatShell').style.display='none';
  document.getElementById('apiKeyInput').value = getApiKey();
}
(function initAiPanel(){
  if(getApiKey()){
    document.getElementById('keyPanel').style.display='none';
    document.getElementById('chatShell').style.display='flex';
  }
})();

function handleChatKey(e){
  if(e.key==='Enter' && !e.shiftKey){ e.preventDefault(); sendChat(); }
}

async function callGemini(key, msg){
  const body = {
    systemInstruction:{parts:[{text:'اسمك "أبطال AI"، وأنت المساعد الذكي الخاص بمنصة "أبطال الإعدادية" (من تصميم وتطوير إسلام المصري) لطلاب الصف الأول والثاني والثالث الإعدادي. لو سألك حد "مين أنت" أو "انت مين"، قدّم نفسك باسم "أبطال AI" وإنك مساعد المنصة، من غير ما تذكر اسم أي شركة تقنية خلف الكواليس. جاوب بالعربية الفصحى المبسطة (تقدر تستخدم لهجة مصرية خفيفة للتقريب). اشرح بالتفصيل، اعرب الجمل لما يُطلب منك، وحل المسائل خطوة بخطوة. خلي إجاباتك مناسبة لسن المرحلة الإعدادية، وركز على المحتوى التعليمي.'}]},
    contents:[{role:'user', parts:[{text:msg}]}]
  };
  return fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-3.5-flash:generateContent?key=${key}`,{
    method:'POST', headers:{'Content-Type':'application/json'}, body:JSON.stringify(body)
  });
}

async function sendChat(){
  const input = document.getElementById('chatInput');
  const msg = input.value.trim();
  if(!msg) return;
  const body = document.getElementById('chatBody');

  const userBubble = document.createElement('div');
  userBubble.className='bubble user';
  userBubble.innerText = msg;
  body.appendChild(userBubble);
  input.value='';
  body.scrollTop = body.scrollHeight;

  const loadingBubble = document.createElement('div');
  loadingBubble.className='bubble bot loading';
  loadingBubble.innerText='جاري كتابة الإجابة...';
  body.appendChild(loadingBubble);
  body.scrollTop = body.scrollHeight;

  const key = getApiKey();
  if(!key){
    loadingBubble.innerText = 'محتاج تفعّل المفتاح الأول من زرار الإعدادات ⚙';
    return;
  }

  const MAX_TRIES = 3;
  for(let attempt=1; attempt<=MAX_TRIES; attempt++){
    try{
      const resp = await callGemini(key, msg);

      if(resp.status === 503 || resp.status === 429){
        if(attempt < MAX_TRIES){
          loadingBubble.innerText = `السيرفر مزحوم شوية، بحاول تاني (محاولة ${attempt+1} من ${MAX_TRIES})...`;
          await new Promise(r => setTimeout(r, 1500 * attempt));
          continue;
        } else {
          loadingBubble.innerText = 'سيرفرات الذكاء الاصطناعي مزحومة جدًا دلوقتي. استنى دقيقة واحدة واضغط إرسال تاني — المشكلة مؤقتة من عندهم مش من عندك.';
          body.scrollTop = body.scrollHeight;
          return;
        }
      }

      let data;
      try{
        data = await resp.json();
      }catch(parseErr){
        loadingBubble.innerText = 'الخدمة ردّت برد غير متوقع (HTTP ' + resp.status + '). جرّب تاكد من المفتاح تاني.';
        body.scrollTop = body.scrollHeight;
        return;
      }
      if(data.candidates && data.candidates[0]){
        loadingBubble.classList.remove('loading');
        loadingBubble.innerText = data.candidates[0].content.parts[0].text;
      } else {
        loadingBubble.innerText = 'حصل خطأ من الخدمة (HTTP ' + resp.status + '): ' + (data.error ? data.error.message : 'تأكد من صحة المفتاح.');
      }
      body.scrollTop = body.scrollHeight;
      return;
    }catch(err){
      loadingBubble.innerText = 'تعذر الاتصال — السبب التقني: ' + (err && err.message ? err.message : String(err)) + '. لو الرسالة فيها "Failed to fetch" غالبًا فيه إضافة (Extension) أو جدار حماية بيمنع الاتصال بـ googleapis.com، أو الملف بيتفتح من مكان بيمنع الاتصال الخارجي.';
      body.scrollTop = body.scrollHeight;
      return;
    }
  }
}

/* ============================================================
   INIT
   ============================================================ */
renderGradeTabs();
showSubjects();
</script>
</body>
</html>
