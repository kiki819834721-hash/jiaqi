# jiaqi<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>抹山集 · 生活补丁计划 | 活动玩法</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700;900&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }

:root {
  --green-50: #f0f7ed;
  --green-100: #dcecd4;
  --green-200: #b8d9a8;
  --green-300: #8dc078;
  --green-400: #6ba354;
  --green-500: #4c8636;
  --green-600: #3b6b2a;
  --green-700: #2e5522;
  --green-800: #26441c;
  --green-900: #1f3818;
  --warm: #faf6f0;
  --text: #2c2c2c;
  --text-light: #6b7280;
  --text-white: rgba(255,255,255,.85);
  --radius: 16px;
  --shadow: 0 2px 20px rgba(0,0,0,.06);
  --shadow-lg: 0 8px 40px rgba(0,0,0,.10);
}

body {
  font-family: 'Noto Sans SC', -apple-system, sans-serif;
  background: var(--warm);
  color: var(--text);
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
}

/* ── HERO ── */
.hero {
  position: relative;
  min-height: 100vh;
  background: linear-gradient(160deg, var(--green-900) 0%, var(--green-700) 40%, var(--green-600) 75%, var(--green-500) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 500px 400px at 15% 70%, rgba(141,192,120,.12) 0%, transparent 70%),
    radial-gradient(ellipse 600px 500px at 85% 25%, rgba(249,115,92,.08) 0%, transparent 60%);
  pointer-events: none;
}
.hero-grid {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(rgba(255,255,255,.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,.03) 1px, transparent 1px);
  background-size: 48px 48px;
  pointer-events: none;
}
.hero-content {
  position: relative;
  z-index: 1;
  text-align: center;
  padding: 2rem;
  max-width: 760px;
}
.hero-emoji { font-size: 3rem; margin-bottom: .8rem; display: block; }
.hero-badge {
  display: inline-block;
  background: rgba(255,255,255,.08);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255,255,255,.15);
  color: rgba(255,255,255,.7);
  font-size: .75rem;
  letter-spacing: .15em;
  padding: .35rem 1.2rem;
  border-radius: 999px;
  margin-bottom: 1.5rem;
  font-weight: 500;
}
.hero h1 {
  font-size: clamp(2.2rem, 5.5vw, 3.6rem);
  font-weight: 900;
  color: #fff;
  line-height: 1.2;
  margin-bottom: .3rem;
  letter-spacing: .04em;
}
.hero h1 em {
  font-style: normal;
  background: linear-gradient(135deg, var(--green-200), #ffe27a);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.hero-sub {
  font-size: clamp(1rem, 1.8vw, 1.2rem);
  color: rgba(255,255,255,.65);
  margin-top: .6rem;
  font-weight: 300;
  letter-spacing: .06em;
  line-height: 1.8;
}
.hero-meta {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: .6rem 1.5rem;
  margin-top: 2rem;
}
.hero-meta span {
  background: rgba(255,255,255,.07);
  border: 1px solid rgba(255,255,255,.12);
  border-radius: 999px;
  padding: .3rem 1rem;
  font-size: .82rem;
  color: rgba(255,255,255,.8);
}
.scroll-hint {
  position: absolute;
  bottom: 2.5rem;
  left: 50%;
  transform: translateX(-50%);
  color: rgba(255,255,255,.2);
  font-size: .7rem;
  letter-spacing: .12em;
  animation: bounce 2.5s ease-in-out infinite;
}
@keyframes bounce {
  0%, 100% { transform: translateX(-50%) translateY(0); }
  50% { transform: translateX(-50%) translateY(8px); }
}

/* ── SECTION ── */
.section {
  max-width: 840px;
  margin: 0 auto;
  padding: 4rem 1.5rem;
}
.section-wide {
  max-width: 960px;
}
.section-label {
  display: flex;
  align-items: center;
  gap: .5rem;
  font-size: .7rem;
  letter-spacing: .2em;
  color: var(--green-400);
  font-weight: 500;
  margin-bottom: .3rem;
}
.section-label::before {
  content: '';
  width: 18px;
  height: 2px;
  background: var(--green-300);
  border-radius: 1px;
  flex-shrink: 0;
}
.section h2 {
  font-size: clamp(1.5rem, 3vw, 2rem);
  font-weight: 700;
  color: var(--green-900);
  line-height: 1.3;
  margin-bottom: .4rem;
}
.section-lead {
  font-size: .95rem;
  color: var(--text-light);
  line-height: 1.8;
  margin-bottom: 2rem;
}
.section-alt {
  background: #fff;
}

/* ── PATCH GRID ── */
.patch-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 1.2rem;
}
.patch-card {
  background: #fff;
  border-radius: var(--radius);
  padding: 1.8rem 1.5rem;
  box-shadow: var(--shadow);
  transition: box-shadow .2s, transform .2s;
  border: 1px solid rgba(0,0,0,.04);
}
.patch-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}
.patch-card .badge {
  display: inline-flex;
  align-items: center;
  gap: .3rem;
  font-size: .68rem;
  font-weight: 600;
  letter-spacing: .06em;
  padding: .2rem .7rem;
  border-radius: 999px;
  margin-bottom: .6rem;
}
.patch-card .badge.taste { background: #fef3c7; color: #92400e; }
.patch-card .badge.life  { background: #e0f2fe; color: #075985; }
.patch-card .badge.body  { background: #fce7f3; color: #9d174d; }
.patch-card .badge.mood  { background: #ede9fe; color: #5b21b6; }

.patch-card .patch-icon {
  font-size: 2.2rem;
  margin-bottom: .3rem;
}
.patch-card h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--green-800);
  line-height: 1.3;
}
.patch-card .pain {
  font-size: .85rem;
  color: var(--text-light);
  margin-top: .15rem;
  margin-bottom: .6rem;
  line-height: 1.6;
}
.patch-card .solution {
  font-size: .85rem;
  color: var(--text);
  line-height: 1.7;
  padding: .6rem .8rem;
  background: var(--green-50);
  border-radius: 10px;
}
.patch-card .solution strong {
  color: var(--green-600);
}
.patch-card .how {
  margin-top: .7rem;
  font-size: .82rem;
  color: var(--green-500);
  font-weight: 500;
}
.patch-card .how::before {
  content: '▸ ';
}

/* ── HOW IT WORKS ── */
.steps {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
  margin: 1.5rem 0;
}
.step {
  background: #fff;
  border-radius: 14px;
  padding: 1.5rem 1rem;
  text-align: center;
  box-shadow: var(--shadow);
  border: 1px solid rgba(0,0,0,.04);
  position: relative;
}
.step .num {
  width: 32px;
  height: 32px;
  border-radius: 50%;
  background: var(--green-600);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: .85rem;
  font-weight: 700;
  margin: 0 auto .6rem;
}
.step .icon { font-size: 1.6rem; margin-bottom: .4rem; }
.step h4 { font-size: .9rem; font-weight: 700; color: var(--green-800); margin-bottom: .2rem; }
.step p { font-size: .78rem; color: var(--text-light); line-height: 1.5; }
.step-arrow {
  position: absolute;
  right: -.7rem;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1.1rem;
  color: var(--green-300);
}
@media (max-width: 840px) {
  .step-arrow { display: none; }
  .steps { gap: .8rem; }
}

/* ── REWARD ── */
.reward-box {
  background: linear-gradient(135deg, var(--green-900), var(--green-700));
  border-radius: var(--radius);
  padding: 2rem 2rem 1.8rem;
  color: #fff;
  text-align: center;
  margin-top: 1.5rem;
}
.reward-box .emoji { font-size: 2.4rem; margin-bottom: .5rem; display: block; }
.reward-box h3 { font-size: 1.15rem; font-weight: 700; margin-bottom: .3rem; }
.reward-box p { font-size: .88rem; color: rgba(255,255,255,.7); line-height: 1.7; }
.reward-box .tag-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: .4rem .6rem;
  margin-top: .8rem;
}
.reward-box .tag-list span {
  background: rgba(255,255,255,.1);
  border: 1px solid rgba(255,255,255,.12);
  border-radius: 999px;
  padding: .2rem .7rem;
  font-size: .78rem;
  color: rgba(255,255,255,.85);
}

/* ── TIMELINE ── */
.event-timeline {
  margin-top: 1.5rem;
}
.event-card {
  display: flex;
  gap: 1.2rem;
  padding: 1.2rem 0;
  border-bottom: 1px solid rgba(0,0,0,.05);
}
.event-card:last-child { border-bottom: none; }
.event-date {
  flex-shrink: 0;
  width: 88px;
  text-align: center;
}
.event-date .day {
  font-size: 1.6rem;
  font-weight: 900;
  color: var(--green-600);
  line-height: 1.1;
}
.event-date .month {
  font-size: .7rem;
  color: var(--text-light);
  letter-spacing: .05em;
  font-weight: 500;
}
.event-body { flex: 1; }
.event-body h4 { font-size: .95rem; font-weight: 700; color: var(--green-800); margin-bottom: .2rem; }
.event-body p { font-size: .85rem; color: var(--text-light); line-height: 1.6; }

/* ── CARD / STAMP ── */
.stamp-showcase {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(170px, 1fr));
  gap: 1rem;
  margin: 1.5rem 0;
}
.stamp-item {
  text-align: center;
  padding: 1.2rem .8rem;
  background: #fff;
  border-radius: 14px;
  box-shadow: var(--shadow);
  border: 1px solid rgba(0,0,0,.04);
}
.stamp-item .stamp-circle {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.6rem;
  margin: 0 auto .5rem;
}
.stamp-item .stamp-circle.taste { background: #fef3c7; }
.stamp-item .stamp-circle.life  { background: #e0f2fe; }
.stamp-item .stamp-circle.body  { background: #fce7f3; }
.stamp-item .stamp-circle.mood  { background: #ede9fe; }
.stamp-item h4 { font-size: .88rem; font-weight: 700; color: var(--green-800); }
.stamp-item p { font-size: .75rem; color: var(--text-light); margin-top: .15rem; }

/* ── SOCIAL ── */
.social-box {
  background: var(--green-50);
  border-radius: var(--radius);
  padding: 1.5rem;
  margin-top: 1.5rem;
  text-align: center;
}
.social-box h4 { font-size: 1rem; font-weight: 700; color: var(--green-700); margin-bottom: .3rem; }
.social-box p { font-size: .85rem; color: var(--text-light); line-height: 1.6; }
.social-box .hashtag {
  display: inline-block;
  margin-top: .5rem;
  padding: .3rem 1rem;
  background: var(--green-100);
  color: var(--green-600);
  border-radius: 999px;
  font-size: .85rem;
  font-weight: 500;
}

/* ── FAQ ── */
.faq-list { margin-top: 1rem; }
.faq-item {
  border: 1px solid rgba(0,0,0,.06);
  border-radius: 12px;
  margin-bottom: .6rem;
  overflow: hidden;
  background: #fff;
}
.faq-q {
  padding: 1rem 1.2rem;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
  font-size: .92rem;
  font-weight: 600;
  color: var(--green-800);
  user-select: none;
  transition: background .15s;
}
.faq-q:hover { background: var(--green-50); }
.faq-q .arrow {
  font-size: .7rem;
  color: var(--green-400);
  transition: transform .25s;
  flex-shrink: 0;
}
.faq-item.open .faq-q .arrow { transform: rotate(180deg); }
.faq-a {
  max-height: 0;
  overflow: hidden;
  transition: max-height .35s ease;
}
.faq-item.open .faq-a { max-height: 500px; }
.faq-a-inner {
  padding: 0 1.2rem 1rem;
  font-size: .85rem;
  color: var(--text-light);
  line-height: 1.7;
  border-top: 1px solid rgba(0,0,0,.04);
  padding-top: .8rem;
}

/* ── FOOTER ── */
.footer {
  text-align: center;
  padding: 2.5rem 1.5rem;
  background: var(--green-900);
  color: rgba(255,255,255,.4);
  font-size: .8rem;
  line-height: 1.8;
}
.footer strong {
  color: rgba(255,255,255,.7);
  font-weight: 500;
}

/* ── RESPONSIVE ── */
@media (max-width: 640px) {
  .section { padding: 2.5rem 1.2rem; }
  .patch-grid { grid-template-columns: 1fr; }
  .event-card { flex-direction: column; gap: .3rem; }
  .event-date { width: auto; text-align: left; display: flex; gap: .4rem; align-items: baseline; }
  .event-date .day { font-size: 1.2rem; }
  .steps { grid-template-columns: 1fr 1fr; }
  .stamp-showcase { grid-template-columns: 1fr 1fr; }
}
</style>
</head>
<body>

<!-- ═══ HERO ═══ -->
<section class="hero">
  <div class="hero-grid"></div>
  <div class="hero-content">
    <span class="hero-badge">2026 · 七月限定</span>
    <h1>抹山集·生活补丁计划</h1>
    <p class="hero-sub">
      生活总有那么些小缺憾——<br>
      我们用四种方式，把它补回来。
    </p>
    <div class="hero-meta">
      <span>📅 7月4日 — 7月31日</span>
      <span>📍 抹山集 · 贵阳部分门店</span>
      <span>🎫惊喜大礼包</span>
      <span>🎪 7月25日 主题活动日</span>
    </div>
  </div>
  <div class="scroll-hint">SCROLL ▼</div>
</section>

<!-- ═══ 活动说明 ═══ -->
<section class="section">
  <div class="section-label">ABOUT</div>
  <h2>来抹山集，给生活打一块补丁</h2>
  
</section>

<!-- ═══ 四大补丁 ═══ -->
<section class="section section-wide">
  <div class="section-label">PATCHES</div>
  <h2>四个补丁 · 四种治愈</h2>
  <p class="section-lead">每一种缺憾都值得被好好对待，每一块补丁都是重新喜欢生活的理由。</p>

  <div class="patch-grid">

    <!-- 味觉补丁 -->
    <div class="patch-card">
      <div class="patch-icon">😩</div>
      <div class="badge taste">味觉补丁</div>
      <h3>重油饭后的悔恨感<br>→ 一杯抹茶就够了</h3>
      <p class="pain">火锅烧烤吃得爽，吃完躺着后悔——肚子胀、嘴巴腻，整个人像被油糊住了。</p>
      <div class="solution">
        <strong>解决方案：</strong>来抹山集喝一杯清爽抹茶饮品。柚見抹茶冰的冰沙刺激、柚見冰柠的柠檬酸爽、抹茶云顶苹果的清甜、苹果茉莉的花果香——每一口都在帮你把"吃太多"的罪恶感冲淡。
      </div>
      
    </div>

    <!-- 生活补丁 -->
    <div class="patch-card">
      <div class="patch-icon">😐</div>
      <div class="badge life">生活补丁</div>
      <h3>无趣的日常<br>→ 盲盒与贴纸请查收</h3>
      <p class="pain">一样的通勤路，一样的工位，一样的晚饭——日子重复到让人记不清今天是周几。</p>
      <div class="solution">
        <strong>解决方案：</strong>购买线上团购并好评，可抽取100%惊喜盲盒。拆开的瞬间——可能是搞怪贴纸包、限定杯套、饮品买一送一券，甚至是免单券。我们还准备了贵州方言搞怪贴纸免费派送，"安逸""莽起""乖噜噜"——贴在手机壳上、电脑上、水杯上，让生活多一点不正经的可爱。
      </div>
      
    </div>

    <!-- 身体补丁 -->
    <div class="patch-card">
      <div class="patch-icon">🦵</div>
      <div class="badge body">身体补丁</div>
      <h3>逐渐消退的身体机能<br>→ 踩上滑板就好了</h3>
      <p class="pain">每天久坐八小时，腰疼肩膀硬，爬两层楼就喘。身体在无声地抗议——你听见了吗？</p>
      <div class="solution">
        <strong>解决方案：</strong>活动玩法不写，暂定。
      </div>
      
    </div>

    <!-- 情绪补丁 -->
    <div class="patch-card">
      <div class="patch-icon">🌧️</div>
      <div class="badge mood">情绪补丁</div>
      <h3>时常光顾的精神内耗<br>→ 交给一首歌吧</h3>
      <p class="pain">想太多、睡不好、白天没精神晚上睡不着。心里的那根弦一直绷着，找不到松下来的理由。</p>
      <div class="solution">
        <strong>解决方案：</strong>7月25日傍晚，我们在现场搭了一个素人音乐会。没有明星大咖，只有和你一样的普通人——他们唱自己的歌，唱你也许也听过的旋律。民谣、流行、原创……你只需要坐下来，吹着晚风，喝一口抹茶，让音乐把心里的褶皱熨平。
      </div>
      
    </div>

  </div>
 </section>
<section class="section" style="padding:1.5rem 1.5rem 0.5rem;">
  <!-- 大礼包 -->
  <div class="reward-box">
    <span class="emoji">🎁</span>
    <h3>品牌大礼包里有什么？</h3>
    <p>抹山集为你准备的夏日礼包——<br>有你爱喝的，有你想要的，还有一点小惊喜。</p>
    <div class="tag-list">
      <span>🥤 饮品免费券 × 3</span>
      <span>👜 限定帆布袋</span>
      <span>🧲 四款补丁冰箱贴套装</span>
      <span>🎨 搞怪贴纸包</span>
      <span>🎫 联名折扣券</span>
    </div>
    <p style="margin-top:.8rem;color:rgba(255,255,255,.5);font-size:.78rem;">* 大礼包数量有限，兑完即止</p>
  </div>
</section>

<!-- ═══ 时间线 ═══ -->
<section class="section">
  <div class="section-label">SCHEDULE</div>
  <h2>你的七月补丁日历</h2>
  <p class="section-lead">两件小事现在就能做，一件大事等7月25日。</p>

  <div class="event-timeline">
    <div class="event-card">
      <div class="event-date">
        <div class="day">7.4-7.10</div>
      </div>
      <div class="event-body">
        <h4>门店活动启动</h4>
        <p>贵阳抹山集花果园购物中心和青云市集门店同步上线「生活补丁计划」。到店核销团购并好评，可以兑换100%中奖盲盒。</p>
      </div>
    </div>
    <div class="event-card">
      <div class="event-date">
        <div class="day">7.18 — 7.19</div>
      </div>
      <div class="event-body">
        <h4>抹茶DIY</h4>
        <p>活动期间到店消费可体验抹茶点茶过程，快来diy专属于你的抹茶饮品吧。</p>
      </div>
    </div>
    <div class="event-card">
      <div class="event-date">
        <div class="day">7.25</div>
      </div>
      <div class="event-body">
        <h4>🎪 主题活动日 · 滑板 + 音乐会</h4>
        <p>下午滑板体验（14:00—18:00），晚间素人音乐会（18:30—21:00）。来现场一次集齐身体+情绪两枚印章，补丁计划圆满达成！</p>
      </div>
    </div>
    <div class="event-card">
      <div class="event-date">
        <div class="day">7.31</div>
      </div>
      <div class="event-body">
        <h4>活动收官</h4>
        <p>抹山集下回更精彩。</p>
      </div>
    </div>
  </div>
</section>

<!-- ═══ 社交互动 ═══ -->
<section class="section section-alt">
  <div class="section-label">SHARE</div>
  <h2>分享你的补丁进度</h2>
  <p class="section-lead">7月抹山集等你来探</p>

  <div class="social-box">
    <h4>社交分享激励</h4>
    <p>
      快把你的图文/视频发布到社交平台并带上话题，并私信我们，抹山集会随机抽取幸运用户，享受抹山集免单券，快快参与进来吧～
    </p>
    <div class="hashtag">#抹山集生活补丁计划#</div>
  </div>
</section>

<!-- ═══ 常见问题 ═══ -->
<section class="section">
  <div class="section-label">FAQ</div>
  <h2>你可能想问的</h2>
  <p class="section-lead">直接点问题看答案，不用翻来翻去。</p>

  <div class="faq-list">
    <div class="faq-item">
      <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">
        <span>活动是所有抹山集门店都能参与吗？</span>
        <span class="arrow">▼</span>
      </div>
      <div class="faq-a">
        <div class="faq-a-inner">以上门店活动只有花果园购物中心店和青云市集店能够参与。线下活动在花果园购物中心哦～</div>
      </div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">
        <span>线下活动需要报名后才能参与吗？</span>
        <span class="arrow">▼</span>
      </div>
      <div class="faq-a">
        <div class="faq-a-inner">线下活动无需报名，欢迎👏大家到现场参加。滑板体验名额有限，会根据现场情况进行调整。</div>
      </div>
    </div>
    
    <div class="faq-item">
      <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">
        <span>我不会滑板，也能玩吗？</span>
        <span class="arrow">▼</span>
      </div>
      <div class="faq-a">
        <div class="faq-a-inner">当然可以！滑板体验区专门设有新手友好时段，有教练从零教学。来试试，说不定就解锁了新爱好。</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══ FOOTER ═══ -->
<footer class="footer">
  <strong>抹山集 · 生活补丁计划</strong><br>
  2026年7月 · 贵阳全门店<br>
  更多信息请关注抹山集官方小红书 / 抖音 / 微信公众号
</footer>

<script>
// Auto-open first FAQ for better initial view
document.querySelector('.faq-item')?.classList.add('open');
</script>

</body>
</html>
