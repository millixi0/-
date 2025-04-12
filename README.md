<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>إهداء لعيُونك!</title>
  <style>
    body {
      background-color: #3C5981;
      color: #3C5981;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
      margin: 0;
      overflow: hidden;
    }
    .page {
      background-color: white;
      width: 90%;
      height: 80%;
      margin: 5% auto;
      padding: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      border-radius: 20px;
      display: none;
      text-align: center;
      font-size: 18px;
      line-height: 2;
    }
    .page.active {
      display: block;
    }
    .next-btn {
      background-color: #3C5981;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 12px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    h1, .link {
      color: #3C5981;
    }
    .hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
    }
    .heart {
      position: absolute;
      width: 15px;
      height: 15px;
      background-color: #99A9C6;
      clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 50% 80%, 20% 100%, 0% 35%);
      animation: float 4s infinite ease-in-out;
      opacity: 0.6;
    }
    @keyframes float {
      0% { transform: translateY(100%); opacity: 0.6; }
      100% { transform: translateY(-100vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="hearts" id="hearts"></div>

<audio id="bgMusic" loop controls style="display:none;">
     <source src="https://docs.google.com/uc?export=download&id=1xo9JhDwWbEfel4cK7eaxsc5cxGAA1p8s" type="audio/mpeg">
   </audio>

  <div class="page active" id="page1">
    <h1>إهداء لعيُونك!</h1>
    <p>
      أهلًا يا نُور القلب، ويا عزيز الروح، إليكَ من فؤادِ امرأةٍ هامَت بك عشقاً، وسكنتْ تفاصيلك سُكناً لا يعقبه رحيل.
      مشاعرٌ جياشة، سالت من ينابيع الهوى، وتعالت من منابر الودّ والهيبة، سُطورٌ لا تُهدى لغيرك، ولا تُكتَب إلا لك،
      وفاءً لا يَعرف الزوال، ومحبّةً لا تعرف الفتور.
    </p>
    <button class="next-btn" onclick="showPage(2)">التالي</button>
  </div>

  <div class="page" id="page2">
    <h1 class="link">
      <a href="https://youtu.be/7ho1WFn79e0?si=2WpEvytlNlcyJSQa" target="_blank">
        همتُ بقلّبك لإهديهِ حرُوف وألحَان تليقُ بهِ
      </a>
    </h1>
    <p>
      يا من تجلّى الحُسن فيك واكتمل، بك تهيم الروحُ وتطمئنّ، وبك يُضاء الدربُ ويَسكن الوجع.
      رأيتُك، فنسيت الزهر والقمر، فأنتَ الجمالُ إذا نُطق، والفتنةُ إن تجسّدت.
    </p>
    <button class="next-btn" onclick="showPage(3)">التالي</button>
  </div>

  <div class="page" id="page3">
    <p>
      عندما أحببتك، أدركتُ أن الحياة ليست مجرّد عيشٍ وأيام، بل رسالةٌ كتبتها الأقدارُ باسمك.
      حين أحببتك، علمتُ أن الشمس لا تُشرق إلا مرةً، وأنت إشراقتها.
      أنتَ دهشةُ العُمر، وأمنيةُ القلبِ، ولستَ عابراً كالبشر.
      حين أحببتك، أدركتُ قوانين الجاذبية، وفهمتُ بكاء شعراءِ العشق، وتنهيداتِ المجانين بالهوى.
      معك.. كل التفاصيل الصغيرة، اصبَحت بحجم الكون.
    </p>
    <button class="next-btn" onclick="showPage(4)">التالي</button>
  </div>

  <div class="page" id="page4">
    <p>مِن نبضِ أُنثاكَ التِي تهِيمُ بكَ</p>
    <p>17/4/2003 - 17/4/2025</p>
    <p style="font-size: 14px; margin-top: 30px;">جُودتك</p>
  </div>

  <script>
    let currentPage = 1;
    function showPage(pageNum) {
      document.querySelector(`#page${currentPage}`).classList.remove('active');
      document.querySelector(`#page${pageNum}`).classList.add('active');
      currentPage = pageNum;
    }

    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (3 + Math.random() * 2) + 's';
      document.getElementById('hearts').appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }
    setInterval(createHeart, 300);
  </script>
<script>
     document.addEventListener('click', function() {
       const music = document.getElementById('bgMusic');
       music.play().catch(e => alert('الرجاء الضغط على السماح لتشغيل الصوت'));
     }, {once: true});
   </script>
</body>
</html>
