<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>أصالة | موقع عربي أصيل</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800&family=Amiri:wght@400;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --brown: #3b2418;
      --dark: #1d120d;
      --gold: #c59a55;
      --gold-light: #e4c27a;
      --cream: #f5ead7;
      --sand: #d9bd8b;
    }

    body {
      background:
        radial-gradient(circle at top, #4b3020 0%, #21140e 45%, #120b08 100%);
      color: var(--cream);
      font-family: "Cairo", sans-serif;
      min-height: 100vh;
    }

    /* زخرفة الخلفية */
    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: .08;
      background-image:
        linear-gradient(30deg, #fff 12%, transparent 12.5%, transparent 87%, #fff 87.5%),
        linear-gradient(150deg, #fff 12%, transparent 12.5%, transparent 87%, #fff 87.5%);
      background-size: 45px 45px;
    }

    nav {
      position: sticky;
      top: 0;
      z-index: 10;

      display: flex;
      justify-content: space-between;
      align-items: center;

      padding: 18px 8%;
      background: rgba(20, 12, 8, .88);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(197,154,85,.25);
    }

    .logo {
      font-family: "Amiri", serif;
      font-size: 30px;
      color: var(--gold-light);
      font-weight: bold;
    }

    nav ul {
      display: flex;
      gap: 30px;
      list-style: none;
    }

    nav a {
      color: #eee;
      text-decoration: none;
      transition: .3s;
      font-weight: 600;
    }

    nav a:hover {
      color: var(--gold-light);
    }

    .hero {
      min-height: 82vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 60px 20px;
    }

    .hero-content {
      max-width: 850px;
    }

    .ornament {
      color: var(--gold);
      font-size: 28px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-family: "Amiri", serif;
      font-size: clamp(55px, 9vw, 105px);
      line-height: 1;
      color: var(--gold-light);
      text-shadow: 0 8px 30px rgba(0,0,0,.5);
    }

    .hero h2 {
      font-size: 25px;
      margin-top: 20px;
      color: #fff;
    }

    .hero p {
      margin: 20px auto;
      max-width: 650px;
      color: #d7c8b3;
      line-height: 2;
      font-size: 17px;
    }

    .buttons {
      margin-top: 30px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 13px 28px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: bold;
      transition: .3s;
    }

    .primary {
      background: linear-gradient(135deg, var(--gold), var(--gold-light));
      color: #24140b;
    }

    .secondary {
      border: 1px solid var(--gold);
      color: var(--gold-light);
    }

    .btn:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 25px rgba(0,0,0,.35);
    }

    section {
      padding: 80px 8%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 45px;
    }

    .section-title h2 {
      font-family: "Amiri", serif;
      font-size: 45px;
      color: var(--gold-light);
    }

    .section-title p {
      color: #bfae99;
      margin-top: 8px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 22px;
      max-width: 1100px;
      margin: auto;
    }

    .card {
      background: rgba(255,255,255,.045);
      border: 1px solid rgba(197,154,85,.22);
      border-radius: 22px;
      padding: 35px 25px;
      text-align: center;
      transition: .35s;
      backdrop-filter: blur(8px);
    }

    .card:hover {
      transform: translateY(-8px);
      border-color: var(--gold);
      background: rgba(197,154,85,.08);
    }

    .icon {
      font-size: 45px;
      margin-bottom: 18px;
    }

    .card h3 {
      color: var(--gold-light);
      font-family: "Amiri", serif;
      font-size: 27px;
      margin-bottom: 10px;
    }

    .card p {
      color: #cbbda9;
      line-height: 1.9;
    }

    .quote {
      max-width: 900px;
      margin: auto;
      text-align: center;
      border-top: 1px solid rgba(197,154,85,.35);
      border-bottom: 1px solid rgba(197,154,85,.35);
      padding: 45px 20px;
    }

    .quote p {
      font-family: "Amiri", serif;
      font-size: 32px;
      line-height: 1.8;
      color: var(--cream);
    }

    footer {
      text-align: center;
      padding: 35px 20px;
      border-top: 1px solid rgba(197,154,85,.2);
      color: #a9957d;
      background: rgba(0,0,0,.2);
    }

    footer span {
      color: var(--gold);
    }

    @media (max-width: 650px) {
      nav {
        padding: 15px 5%;
      }

      nav ul {
        gap: 12px;
        font-size: 13px;
      }

      .hero {
        min-height: 75vh;
      }

      .hero h1 {
        font-size: 65px;
      }

      .hero h2 {
        font-size: 20px;
      }

      section {
        padding: 60px 5%;
      }

      .section-title h2 {
        font-size: 38px;
      }
    }
  </style>
</head>

<body>

  <!-- القائمة -->
  <nav>
    <div class="logo">أصالة</div>

    <ul>
      <li><a href="#home">الرئيسية</a></li>
      <li><a href="#about">عن الموقع</a></li>
      <li><a href="#heritage">تراثنا</a></li>
    </ul>
  </nav>


  <!-- الواجهة الرئيسية -->
  <header class="hero" id="home">

    <div class="hero-content">

      <div class="ornament">✦ ــــــــــ ✦</div>

      <h1>أصالة</h1>

      <h2>حكاية وطن... وإرث أجداد</h2>

      <p>
        هنا تبدأ الحكاية من عبق الماضي،
        حيث القهوة والمجالس والكرم،
        وحيث تحمل كل قطعة من تراثنا قصة
        تستحق أن تُروى.
      </p>

      <div class="buttons">
        <a href="#heritage" class="btn primary">
          اكتشف تراثنا
        </a>

        <a href="#about" class="btn secondary">
          اعرف المزيد
        </a>
      </div>

    </div>

  </header>


  <!-- عن الموقع -->
  <section id="about">

    <div class="section-title">
      <h2>عن أصالة</h2>
      <p>الماضي حاضرٌ في تفاصيلنا</p>
    </div>

    <div class="quote">

      <p>
        "من لا يعرف ماضيه، لا يعرف قيمة حاضره،
        فالتراث ليس مجرد ذكريات، بل هو هوية."
      </p>

    </div>

  </section>


  <!-- التراث -->
  <section id="heritage">

    <div class="section-title">
      <h2>من تراثنا</h2>
      <p>تفاصيل صغيرة صنعت ذاكرة كبيرة</p>
    </div>

    <div class="cards">

      <div class="card">
        <div class="icon">☕</div>
        <h3>القهوة العربية</h3>
        <p>
          رمز للكرم والضيافة، ارتبطت بالمجالس
          وأصبحت جزءاً أصيلاً من ثقافتنا.
        </p>
      </div>

      <div class="card">
        <div class="icon">🏕️</div>
        <h3>المجلس</h3>
        <p>
          مكان يجتمع فيه الأهل والضيوف،
          وتُروى فيه الحكايات وتُحفظ الذكريات.
        </p>
      </div>

      <div class="card">
        <div class="icon">🐪</div>
        <h3>الإبل</h3>
        <p>
          رفيقة الإنسان في الجزيرة العربية،
          ولها مكانة كبيرة في تاريخ المنطقة.
        </p>
      </div>

      <div class="card">
        <div class="icon">🗡️</div>
        <h3>الفروسية</h3>
        <p>
          ارتبطت بالشجاعة والمهارة،
          وكانت من أبرز مظاهر حياة العرب قديماً.
        </p>
      </div>

    </div>

  </section>


  <!-- اقتباس -->
  <section>

    <div class="quote">

      <div class="ornament">✦</div>

      <p>
        أصالتنا ليست شيئاً نتركه خلفنا،
        بل شيء نحمله معنا أينما ذهبنا.
      </p>

      <div class="ornament">✦</div>

    </div>

  </section>


  <!-- التذييل -->
  <footer>

    صُنع بحب من <span>فزاع</span> © 2026

  </footer>


  <script>

    // حركة بسيطة عند الضغط على روابط القائمة
    document.querySelectorAll('a[href^="#"]').forEach(link => {

      link.addEventListener("click", function(e) {

        e.preventDefault();

        const target = document.querySelector(
          this.getAttribute("href")
        );

        if (target) {
          target.scrollIntoView({
            behavior: "smooth"
          });
        }

      });

    });

  </script>

</body>
</html>