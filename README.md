<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1"/>
  <title>وظفني | سيرة ذاتية عربية وإنجليزية + خطاب توظيف</title>
  <meta name="description" content="وظفني: منصّة بسيطة لصناعة سيرة ذاتية عربية وإنجليزية متوافقة مع أنظمة التتبع (ATS) وخطاب توظيف مخصص لشركة معيّنة، مع ثلاث باقات مناسبة.">
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header class="site-header">
    <div class="container nav">
      <a class="brand" href="#home" aria-label="وظفني - الرئيسية">
        <span class="logo" aria-hidden="true"></span>
        <strong>وظفني</strong>
      </a>
      <nav class="menu" aria-label="التنقل الرئيسي">
        <a href="#cv">السيرة الذاتية</a>
        <a href="#cover">خطاب التوظيف</a>
        <a href="#pricing">الباقات</a>
        <a class="btn ghost" href="#start">ابدأ الآن</a>
      </nav>
    </div>
  </header>

  <main id="home">
    <!-- Hero -->
    <section class="hero container">
      <div class="hero-text">
        <h1>أنشئ سيرتك وخطابك — بصيغة صديقة لـ <span class="underline">ATS</span></h1>
        <p class="muted">نماذج عربية وإنجليزية واضحة، قابلة للنسخ أو التنزيل كملف TXT، مع نصائح كلمات مفتاحية.</p>
        <div class="hero-cta">
          <a class="btn primary" href="#start">ابدأ مجانًا</a>
          <a class="btn" href="#pricing">شاهد الباقات</a>
        </div>
        <div class="badges">
          <span>⚡ فوري</span><span>📝 عربي / English</span><span>🎯 خطاب موجّه</span><span>✔️ صديق لـ ATS</span>
        </div>
      </div>
      <div class="hero-card card">
        <div class="switcher" role="tablist" aria-label="لغة المعاينة">
          <button id="tab-ar" class="active" aria-selected="true">العربية</button>
          <button id="tab-en" aria-selected="false">English</button>
        </div>
        <pre id="cv-preview" class="preview" aria-live="polite"></pre>
        <p class="hint">معاينة نص سيرة بسيط وواضح لتجاوز فلاتر ATS.</p>
      </div>
    </section>

    <!-- CV Builder -->
    <section id="cv" class="container section">
      <h2>السيرة الذاتية (ATS)</h2>
      <div class="grid two">
        <div class="card">
          <h3>بيانات السيرة</h3>
          <form id="cv-form" novalidate>
            <div class="grid two">
              <label>الاسم الكامل
                <input name="fullName" required placeholder="مثال: أحمد محمد العتيبي">
              </label>
              <label>المسمى الوظيفي
                <input name="title" required placeholder="مثال: مطوّر واجهات">
              </label>
            </div>
            <div class="grid two">
              <label>البريد الإلكتروني
                <input type="email" name="email" required placeholder="you@email.com">
              </label>
              <label>الجوال
                <input name="phone" placeholder="05xxxxxxxx">
              </label>
            </div>
            <div class="grid two">
              <label>الموقع (مدينة - دولة)
                <input name="location" placeholder="الرياض - السعودية">
              </label>
              <label>اللغة
                <select name="cvLang">
                  <option value="ar">العربية</option>
                  <option value="en">English</option>
                  <option value="both">عربي + English</option>
                </select>
              </label>
            </div>
            <label>روابط (LinkedIn / GitHub / موقع شخصي) — افصل بينها بـ فاصلة
              <input name="links" placeholder="linkedin.com/in/..., github.com/..., yoursite.me">
            </label>
            <label>ملخص مهني مختصر
              <textarea name="summary" rows="3" placeholder="3–4 أسطر تبرز الخبرات والإنجازات القابلة للقياس"></textarea>
            </label>
            <label>الخبرات (عنصر في كل سطر) — الصيغة المقترحة:
              <span class="hint">شركة | الدور | المدة (2022–2024) | 2–3 إنجازات قابلة للقياس</span>
              <textarea name="experience" rows="5" placeholder="شركة س | مطوّر واجهات | 2023–2024 | خفّضت زمن التحميل 35%"></textarea>
            </label>
            <label>التعليم (عنصر في كل سطر)
              <textarea name="education" rows="3" placeholder="بكالوريوس علوم حاسب | جامعة الملك سعود | 2021"></textarea>
            </label>
            <label>المهارات (افصل بفواصل)
              <input name="skills" placeholder="JavaScript, React, HTML, CSS, Git">
            </label>

            <div class="actions">
              <button type="submit" class="btn primary">توليد السيرة</button>
              <button type="button" id="copy-cv" class="btn">نسخ</button>
              <button type="button" id="download-cv" class="btn ghost">تنزيل TXT</button>
              <span class="hint">نصيحة: استخدم كلمات من الوصف الوظيفي لزيادة التوافق مع ATS.</span>
            </div>
          </form>
        </div>

        <div class="card">
          <h3>نص السيرة الناتج</h3>
          <textarea id="output-cv" rows="18" readonly placeholder="سيظهر النص هنا..."></textarea>
        </div>
      </div>
    </section>

    <!-- Cover Letter -->
    <section id="cover" class="container section">
      <h2>خطاب التوظيف</h2>
      <div class="grid two">
        <div class="card">
          <h3>إعداد الخطاب</h3>
          <form id="cl-form" novalidate>
            <div class="grid two">
              <label>اسم الشركة
                <input name="company" required placeholder="مثال: شركة نمو التقنية">
              </label>
              <label>المسمى/القسم
                <input name="role" placeholder="مثال: أخصائي تسويق رقمي">
              </label>
            </div>
            <div class="grid two">
              <label>اللغة
                <select name="clLang">
                  <option value="ar">العربية</option>
                  <option value="en">English</option>
                </select>
              </label>
              <label>النبرة
                <select name="tone">
                  <option value="formal">رسمية</option>
                  <option value="friendly">ودّية</option>
                </select>
              </label>
            </div>
            <label>لماذا أنت مناسب؟ (نقاط سريعة كل نقطة بسطر)
              <textarea name="why" rows="4" placeholder="قيادة فرق، تحسين مؤشرات الأداء، إنجازات قابلة للقياس"></textarea>
            </label>
            <div class="actions">
              <button type="submit" class="btn primary">توليد الخطاب</button>
              <button type="button" id="copy-cl" class="btn">نسخ</button>
              <button type="button" id="download-cl" class="btn ghost">تنزيل TXT</button>
            </div>
          </form>
        </div>

        <div class="card">
          <h3>نص الخطاب الناتج</h3>
          <textarea id="output-cl" rows="18" readonly placeholder="سيظهر الخطاب هنا..."></textarea>
        </div>
      </div>
    </section>

    <!-- Pricing -->
    <section id="pricing" class="container section">
      <h2>الباقات</h2>
      <p class="muted center">أسعار رمزية — غيّرها كما تريد من الكود.</p>
      <div class="grid three">
        <div class="card price-card">
          <div class="ribbon">الأوفر</div>
          <h3>الأساسية</h3>
          <p>سيرة واحدة (عربي أو English) + تنزيل TXT</p>
          <div class="price">19 ر.س</div>
          <a class="btn full" href="#start">اختر</a>
        </div>
        <div class="card price-card">
          <h3>الاحترافية</h3>
          <p>سيرتان (عربي + English) + خطاب عام</p>
          <div class="price">39 ر.س</div>
          <a class="btn full" href="#start">اختر</a>
        </div>
        <div class="card price-card">
          <h3>البريميوم</h3>
          <p>سيرتان + خطاب مخصص لشركة + نصائح كلمات مفتاحية</p>
          <div class="price">69 ر.س</div>
          <a class="btn full" href="#start">اختر</a>
        </div>
      </div>
    </section>

    <!-- Start anchor -->
    <section id="start" class="container section small-gap">
      <div class="card center">
        <h3>جاهز تبدأ؟</h3>
        <p class="muted">املأ النموذج في قسم السيرة أو الخطاب، وانسخ أو نزّل الملف فورًا.</p>
        <a class="btn primary" href="#cv">ابدأ بصناعة السيرة</a>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-wrap">
      <span>© <span id="year"></span> وظفني</span>
      <div class="chips">
        <span class="chip">سياسة الخصوصية</span>
        <span class="chip">الشروط</span>
        <a class="chip" href="#cv">السيرة</a>
      </div>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
:root{
  --bg:#0f1115; --bg2:#12141b; --card:#171a23; --text:#e8eaf2; --muted:#aab0c0;
  --acc:#4ade80; --acc2:#60a5fa; --ring:#22d3ee; --line:rgba(255,255,255,.08);
}
@media (prefers-color-scheme: light){
  :root{ --bg:#f8fafc; --bg2:#eef2f7; --card:#ffffff; --text:#111827; --muted:#6b7280; --acc:#10b981; --acc2:#2563eb; --ring:#06b6d4; --line:rgba(0,0,0,.08); }
}
*{box-sizing:border-box}
html,body{height:100%}
body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,"Noto Naskh Arabic",Tahoma,Arial,sans-serif;background:linear-gradient(180deg,var(--bg),var(--bg2));color:var(--text);line-height:1.65}
a{color:inherit;text-decoration:none}
.container{max-width:1100px;margin:auto;padding:20px}
.site-header{position:sticky;top:0;background:rgba(10,12,18,.65);backdrop-filter:blur(10px);border-bottom:1px solid var(--line);z-index:10}
.nav{display:flex;align-items:center;justify-content:space-between;gap:12px}
.brand{display:flex;align-items:center;gap:10px;font-weight:800}
.logo{width:36px;height:36px;border-radius:10px;background:
  radial-gradient(45% 50% at 70% 30%, var(--acc2), transparent 60%),
  linear-gradient(135deg, var(--acc), var(--acc2));box-shadow:0 8px 30px rgba(0,0,0,.25)}
.menu{display:flex;gap:12px;align-items:center}
.btn{display:inline-flex;gap:8px;align-items:center;justify-content:center;padding:10px 14px;border-radius:12px;border:1px solid var(--line);background:linear-gradient(180deg,rgba(255,255,255,.06),rgba(255,255,255,.02));cursor:pointer}
.btn.primary{border-color:transparent;background:linear-gradient(135deg,var(--acc),var(--acc2));color:#fff}
.btn.ghost{background:transparent;border:1px solid var(--ring);color:var(--text)}
.btn.full{width:100%}
.muted{color:var(--muted)}
.center{text-align:center}
.chips{display:flex;gap:8px;flex-wrap:wrap}
.chip{font-size:12px;padding:6px 10px;border-radius:10px;background:rgba(255,255,255,.06);border:1px solid var(--line)}
.section{padding:34px 0}
.small-gap{padding:20px 0}
.card{background:linear-gradient(180deg,var(--card),rgba(255,255,255,.02));border:1px solid var(--line);border-radius:16px;padding:18px;box-shadow:0 10px 36px rgba(0,0,0,.18)}
.grid.two{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.grid.three{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.hero{display:grid;grid-template-columns:1.1fr .9fr;gap:28px;align-items:center;padding:36px 0}
.hero h1{font-size:clamp(26px,3.8vw,40px);margin:0 0 8px}
.hero-cta{display:flex;gap:10px;flex-wrap:wrap;margin-top:10px}
.badges{display:flex;gap:8px;flex-wrap:wrap;margin-top:8px}
.switcher{display:flex;gap:8px;padding:4px;border:1px solid var(--line);border-radius:12px}
.switcher button{flex:1;border:0;background:transparent;padding:8px 10px;border-radius:8px;cursor:pointer;color:var(--muted)}
.switcher button.active{background:rgba(255,255,255,.08);color:var(--text);border:1px solid var(--line)}
.preview{background:#fff;color:#111;border-radius:12px;padding:14px;min-height:220px;max-height:320px;overflow:auto;font-family:ui-monospace,Consolas,monospace}
label{display:block;font-weight:600;margin:8px 0 4px}
input,select,textarea{width:100%;background:rgba(255,255,255,.06);border:1px solid var(--line);border-radius:10px;color:var(--text);padding:10px 12px;font-size:15px}
input:focus,select:focus,textarea:focus{outline:2px solid var(--ring);border-color:transparent}
textarea{resize:vertical}
.actions{display:flex;flex-wrap:wrap;gap:10px;align-items:center;margin-top:8px}
.hint{font-size:12px;color:var(--muted)}
.price-card{position:relative}
.ribbon{position:absolute;inset-inline-start:-8px;top:-8px;background:var(--acc2);color:#fff;padding:6px 10px;border-radius:8px;font-size:12px}
.site-footer{padding:26px 0;color:var(--muted);border-top:1px solid var(--line);margin-top:20px}
.footer-wrap{display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap}
@media (max-width:1000px){.hero{grid-template-columns:1fr}.grid.two{grid-template-columns:1fr}.grid.three{grid-template-columns:1fr}}
