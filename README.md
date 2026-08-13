[index.html](https://github.com/user-attachments/files/31047885/index.html)
<!doctype html>
<html lang="ja">
<meta charset="utf-8">
<title>医療安全総研 | 病院の医療安全に、もう一人の専門家を。</title>
<meta name="description" content="医療安全総研（株式会社医療安全総研）は、管理者と現場の双方を年間で支える医療安全の伴走支援パートナーです。判断・報告の助言から有事の初動対応、RCA・体制づくりまで、現役の医療安全専門医が実務レベルで支援します。">
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
  :root {
    /* brand palette — navy(信頼/管理者) × teal(現場) × crimson(有事) */
    --navy:       #17284a;
    --navy-2:     #223a66;
    --navy-soft:  #e7ecf4;
    --teal:       #0f7d72;
    --teal-deep:  #0a5f56;
    --teal-soft:  #e2efec;
    --crimson:    #b23b3b;
    --crimson-soft:#f6e9e6;

    --ground:   #f7f8f9;
    --surface:  #ffffff;
    --surface-2:#eef1f4;
    --ink:      #0f151d;
    --ink-soft: #161c24;
    --ink-faint:#3a414c;
    --line:     #d3d9e1;

    --focus: var(--teal);
    --maxw: 1160px;
    --gut: clamp(20px, 5vw, 68px);

    --sans: "Hiragino Kaku Gothic ProN", "Hiragino Sans", "Yu Gothic",
            "YuGothic", "Noto Sans JP", Meiryo, system-ui, sans-serif;
    --serif: "Hiragino Mincho ProN", "Hiragino Mincho Pro", "Yu Mincho",
             "YuMincho", "Noto Serif JP", "MS PMincho", serif;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --navy:#0f1b33; --navy-2:#2c4675; --navy-soft:#1b2b48;
      --teal:#41b3a5; --teal-deep:#63c9bc; --teal-soft:#12332f;
      --crimson:#d97a72; --crimson-soft:#33201e;
      --ground:#0c1524; --surface:#12213a; --surface-2:#182a48;
      --ink:#eef2f9; --ink-soft:#c3ccdb; --ink-faint:#93a0b5; --line:#2b3d60;
    }
  }
  :root[data-theme="light"]{
    --navy:#17284a; --navy-2:#223a66; --navy-soft:#e7ecf4;
    --teal:#0f7d72; --teal-deep:#0a5f56; --teal-soft:#e2efec;
    --crimson:#b23b3b; --crimson-soft:#f6e9e6;
    --ground:#f7f8f9; --surface:#ffffff; --surface-2:#eef1f4;
    --ink:#0f151d; --ink-soft:#161c24; --ink-faint:#3a414c; --line:#d3d9e1;
  }
  :root[data-theme="dark"]{
    --navy:#0f1b33; --navy-2:#2c4675; --navy-soft:#1b2b48;
    --teal:#41b3a5; --teal-deep:#63c9bc; --teal-soft:#12332f;
    --crimson:#d97a72; --crimson-soft:#33201e;
    --ground:#0c1524; --surface:#12213a; --surface-2:#182a48;
    --ink:#eef2f9; --ink-soft:#c3ccdb; --ink-faint:#93a0b5; --line:#2b3d60;
  }

  * { box-sizing: border-box; }
  html { scroll-behavior: smooth; scroll-padding-top: 76px; }
  @media (prefers-reduced-motion: reduce){ html{scroll-behavior:auto;} *{animation:none!important;transition:none!important;} }

  body {
    margin:0; background:var(--ground); color:var(--ink);
    font-family:var(--sans); font-size:18px; line-height:1.95;
    -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    /* 日本語：文節単位で改行（lang=ja が必須）。熟語・単語が途中で割れない */
    word-break: auto-phrase;
    overflow-wrap: anywhere;
    line-break: strict;
  }
  .wrap{ max-width:var(--maxw); margin:0 auto; padding-inline:var(--gut); }
  a{ color:var(--teal-deep); text-underline-offset:3px; }
  a:focus-visible, button:focus-visible{ outline:2px solid var(--focus); outline-offset:3px; border-radius:3px; }

  h1,h2,h3{ text-wrap:balance; }

  /* 主要テキストも auto-phrase で統一（文節単位で改行） */
  h1,h2,h3,h4,p,li,
  .lede,.sub,.ptag,.role,.q,.intro,.at,.tt,.msg,.form-note,.eyebrow,
  .co-table .v,.prof-table .v,.g-head p,.notice-body p,.answer p,
  .stance p,.stance h3,.card p,.acts li,.plan li,.step .st,.pstep p,
  .li-t span,.hero-meta .m span,.g-photo .lab b,.g-photo .lab span{
    line-break: strict;
    word-break: auto-phrase;
  }
  p,li,.lede,.intro,.msg{ text-wrap: pretty; }

  /* ── header ── */
  header{
    position:sticky; top:0; z-index:60;
    background:color-mix(in srgb, var(--ground) 90%, transparent);
    backdrop-filter:saturate(1.4) blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav{ display:flex; align-items:center; justify-content:space-between; gap:20px; height:66px; }
  .brand{ display:flex; align-items:center; gap:11px; text-decoration:none; color:var(--ink); }
  .brand .logo{
    width:34px; height:34px; border-radius:8px; flex:none;
    background:linear-gradient(145deg, var(--navy), var(--navy-2));
    display:grid; place-items:center; color:#fff; position:relative;
  }
  .brand .logo svg{ width:19px; height:19px; }
  .brand .logo::after{ content:""; position:absolute; right:-2px; bottom:-2px; width:11px; height:11px; border-radius:50%; background:var(--teal); border:2px solid var(--ground); }
  .brand .txt{ display:flex; flex-direction:column; line-height:1.15; }
  .brand .jp{ font-family:var(--serif); font-weight:600; font-size:17.5px; letter-spacing:.06em; }
  .brand .en{ font-size:9px; letter-spacing:.24em; color:var(--ink-faint); text-transform:uppercase; }
  .nav-links{ display:flex; gap:22px; align-items:center; }
  .nav-links a{ color:var(--ink-soft); text-decoration:none; font-size:15px; letter-spacing:.02em; transition:color .2s; white-space:nowrap; }
  .nav-links a:hover{ color:var(--teal); }
  .nav-cta{ font-size:13.5px; padding:9px 18px; border-radius:999px; background:var(--navy); color:#fff !important; text-decoration:none; white-space:nowrap; transition:background .2s; }
  .nav-cta:hover{ background:var(--navy-2); }
  .theme-btn{ background:transparent; border:1px solid var(--line); color:var(--ink-soft); width:34px; height:34px; border-radius:999px; cursor:pointer; display:grid; place-items:center; transition:border-color .2s,color .2s; flex:none; }
  .theme-btn:hover{ border-color:var(--teal); color:var(--teal); }
  .theme-btn svg{ width:16px; height:16px; }
  @media (max-width:960px){
    .hamburger{ display:block; }
    .nav-links{ position:absolute; top:66px; left:0; right:0; background:var(--ground); border-bottom:1px solid var(--line); flex-direction:column; align-items:stretch; gap:0; padding:6px 20px 18px; display:none; box-shadow:0 24px 34px -22px rgba(0,0,0,.35); }
    .nav-links.open{ display:flex; }
    .nav-links a{ padding:14px 4px; border-bottom:1px solid var(--line); font-size:16.5px; }
    .nav-links a.nav-cta{ border:none; background:var(--navy); color:#fff !important; border-radius:999px; text-align:center; margin-top:14px; padding:14px; }
    .nav-links .theme-btn{ align-self:flex-start; margin-top:14px; }
  }

  /* ── buttons ── */
  .btn{ display:inline-flex; align-items:center; gap:9px; padding:14px 28px; border-radius:999px; font-size:15px; text-decoration:none; font-weight:600; letter-spacing:.02em; transition:transform .15s, background .2s, border-color .2s, color .2s; cursor:pointer; border:none; }
  .btn .arw{ font-size:16px; line-height:1; }
  .btn-primary{ background:var(--teal); color:#fff; }
  .btn-primary:hover{ background:var(--teal-deep); transform:translateY(-1px); }
  .btn-navy{ background:var(--navy); color:#fff; }
  .btn-navy:hover{ background:var(--navy-2); transform:translateY(-1px); }
  .btn-ghost{ background:transparent; color:var(--ink); border:1.5px solid var(--line); }
  .btn-ghost:hover{ border-color:var(--teal); color:var(--teal); }
  .btn-light{ background:#fff; color:var(--navy); }
  .btn-light:hover{ transform:translateY(-1px); }

  /* ── section frame ── */
  section{ padding:clamp(60px,9vw,110px) 0; }
  .alt{ background:var(--surface-2); }
  .sec-head{ max-width:44em; margin-bottom:clamp(38px,6vw,58px); }
  .kicker{ display:flex; align-items:center; gap:12px; font-size:12px; letter-spacing:.18em; text-transform:uppercase; color:var(--teal-deep); margin-bottom:16px; font-weight:600; }
  .kicker .no{ font-family:var(--serif); font-size:13px; color:var(--ink-faint); letter-spacing:.05em; }
  .kicker::after{ content:""; height:1px; flex:1; background:var(--line); max-width:70px; }
  h2{ font-family:var(--serif); font-weight:600; font-size:clamp(26px,4.2vw,40px); line-height:1.42; letter-spacing:.02em; margin:0 0 16px; }
  .sec-head p{ color:var(--ink-soft); margin:0; font-size:17.5px; }

  /* ── hero ── */
  .hero{ position:relative; overflow:hidden; background:var(--navy); color:#eef2f8; padding:clamp(76px,13vw,150px) 0 clamp(64px,10vw,120px); }
  .hero::before{ content:""; position:absolute; inset:0; background:
      radial-gradient(48% 60% at 84% 12%, rgba(15,125,114,.34) 0%, transparent 62%),
      radial-gradient(40% 50% at 8% 100%, rgba(34,58,102,.55) 0%, transparent 60%); }
  .hero .wrap{ position:relative; z-index:1; }
  .hero .eyebrow{ display:inline-flex; align-items:center; gap:11px; font-size:12.5px; letter-spacing:.2em; text-transform:uppercase; color:#7fd3c8; margin-bottom:26px; }
  .hero .eyebrow::before{ content:""; width:30px; height:1.5px; background:var(--teal); }
  .hero h1{ font-family:var(--serif); font-weight:600; font-size:clamp(28px,5vw,48px); line-height:1.32; letter-spacing:.02em; margin:0 0 26px; max-width:16em; }
  .hero h1 .l{ white-space:nowrap; }
  .hero h1 .hl{ color:#5ec9bb; }
  .hero .lede{ font-size:clamp(15.5px,2.1vw,19px); color:#c6d0e0; max-width:33em; margin:0 0 40px; }
  .hero-actions{ display:flex; flex-wrap:wrap; gap:14px; }
  .hero-meta{ display:flex; flex-wrap:wrap; gap:26px; margin-top:52px; padding-top:30px; border-top:1px solid rgba(255,255,255,.14); }
  .hero-meta .m{ display:flex; flex-direction:column; }
  .hero-meta .m b{ font-family:var(--serif); font-size:clamp(22px,3vw,30px); color:#fff; font-weight:600; line-height:1.2; }
  .hero-meta .m span{ font-size:12.5px; color:#9fb0c7; letter-spacing:.03em; margin-top:4px; }

  /* ── problem / two stances ── */
  .stances{ display:grid; grid-template-columns:1fr 1fr; gap:22px; }
  @media (max-width:820px){ .stances{ grid-template-columns:1fr; } }
  .stance{ border-radius:16px; padding:34px 32px; border:1px solid var(--line); background:var(--surface); position:relative; overflow:hidden; }
  .stance::before{ content:""; position:absolute; left:0; top:0; bottom:0; width:5px; }
  .stance.mng::before{ background:var(--navy-2); }
  .stance.fld::before{ background:var(--teal); }
  .stance .tag{ display:inline-block; font-size:12.5px; letter-spacing:.08em; font-weight:600; padding:5px 13px; border-radius:999px; margin-bottom:16px; }
  .stance.mng .tag{ background:var(--navy-soft); color:var(--navy-2); }
  .stance.fld .tag{ background:var(--teal-soft); color:var(--teal-deep); }
  .stance h3{ font-family:var(--serif); font-size:21px; font-weight:600; margin:0 0 12px; line-height:1.5; }
  .stance p{ margin:0 0 16px; color:var(--ink-soft); font-size:15.5px; }
  .stance .q{ font-size:16.5px; color:var(--ink); font-weight:600; border-top:1px dashed var(--line); padding-top:16px; margin:0; }

  .answer{ margin-top:30px; background:var(--navy); color:#eef2f8; border-radius:16px; padding:clamp(28px,4vw,42px); }
  .answer .lbl{ font-size:12.5px; letter-spacing:.14em; text-transform:uppercase; color:#7fd3c8; font-weight:600; margin-bottom:12px; }
  .answer p{ margin:0; font-size:clamp(16px,2.4vw,20px); line-height:1.85; }
  .answer .hl{ color:#5ec9bb; font-weight:600; }

  /* ── services ── */
  .svc-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:22px; }
  @media (max-width:900px){ .svc-grid{ grid-template-columns:1fr; } }
  .svc{ background:var(--surface); border:1px solid var(--line); border-radius:16px; padding:34px 30px; display:flex; flex-direction:column; gap:14px; transition:transform .2s, box-shadow .2s, border-color .2s; }
  .svc:hover{ transform:translateY(-3px); border-color:var(--teal); box-shadow:0 16px 40px -24px rgba(23,40,74,.55); }
  .svc .no{ font-family:var(--serif); font-size:13px; letter-spacing:.1em; color:var(--ink-faint); }
  .svc .ico{ width:48px; height:48px; border-radius:12px; display:grid; place-items:center; }
  .svc.a .ico{ background:var(--navy-soft); color:var(--navy-2); }
  .svc.b .ico{ background:var(--teal-soft); color:var(--teal-deep); }
  .svc.c .ico{ background:var(--crimson-soft); color:var(--crimson); }
  .svc .ico svg{ width:25px; height:25px; }
  .svc h3{ font-family:var(--serif); font-size:21px; font-weight:600; margin:0; }
  .svc .sub{ font-size:14px; color:var(--teal-deep); font-weight:600; margin:-8px 0 0; }
  .svc p{ margin:0; color:var(--ink-soft); font-size:15.5px; }
  .svc ul{ margin:4px 0 0; padding:0; list-style:none; display:grid; gap:9px; }
  .svc li{ font-size:15px; color:var(--ink-soft); padding-left:22px; position:relative; }
  .svc li::before{ content:""; position:absolute; left:2px; top:9px; width:8px; height:8px; border-radius:2px; background:var(--teal); opacity:.6; }

  /* support by role */
  .roles{ display:grid; grid-template-columns:1fr 1fr; gap:0; margin-top:34px; border:1px solid var(--line); border-radius:16px; overflow:hidden; background:var(--surface); }
  @media (max-width:820px){ .roles{ grid-template-columns:1fr; } }
  .role-col{ padding:32px 30px; }
  .role-col:first-child{ border-right:1px solid var(--line); }
  @media (max-width:820px){ .role-col:first-child{ border-right:none; border-bottom:1px solid var(--line); } }
  .role-col h4{ display:flex; align-items:center; gap:10px; margin:0 0 20px; font-family:var(--serif); font-size:18px; font-weight:600; }
  .role-col h4 .dot{ width:11px; height:11px; border-radius:3px; }
  .role-col.mng h4 .dot{ background:var(--navy-2); }
  .role-col.fld h4 .dot{ background:var(--teal); }
  .role-col .grp{ font-size:12px; letter-spacing:.08em; color:var(--ink-faint); font-weight:600; margin:16px 0 8px; }
  .role-col ul{ margin:0; padding:0; list-style:none; display:grid; gap:9px; }
  .role-col li{ font-size:15px; color:var(--ink-soft); padding-left:20px; position:relative; }
  .role-col li::before{ content:"✓"; position:absolute; left:0; top:0; color:var(--teal); font-size:12px; font-weight:700; }

  /* サービス詳細（相談パートナーシップ） */
  .svc-detail{ margin-top:22px; background:var(--surface); border:1px solid var(--line); border-left:5px solid var(--crimson); border-radius:16px; padding:clamp(26px,4vw,40px); display:grid; grid-template-columns:1fr 1fr; gap:clamp(24px,4vw,46px); align-items:start; }
  @media (max-width:820px){ .svc-detail{ grid-template-columns:1fr; gap:24px; } }
  .svc-detail .sd-tag{ font-size:12.5px; font-weight:700; letter-spacing:.06em; color:var(--crimson); }
  .svc-detail h3{ font-family:var(--serif); font-size:clamp(20px,2.7vw,25px); font-weight:600; margin:12px 0; }
  .svc-detail .sd-head p{ margin:0; color:var(--ink-soft); font-size:15.5px; }
  .svc-detail .sd-head b{ color:var(--crimson); font-weight:700; }
  .sd-list{ display:grid; gap:15px; }
  .sd-item{ padding-left:28px; position:relative; }
  .sd-item::before{ content:""; position:absolute; left:2px; top:7px; width:12px; height:12px; border-radius:3px; background:var(--crimson-soft); border:2px solid var(--crimson); }
  .sd-item b{ display:block; font-size:15.5px; color:var(--ink); font-weight:600; margin-bottom:3px; }
  .sd-item span{ font-size:14px; color:var(--ink-soft); line-height:1.7; }

  /* 制度改正 notice band */
  .notice{ margin-top:34px; background:var(--navy); color:#eef2f8; border-radius:16px; padding:clamp(28px,4vw,42px); display:grid; grid-template-columns:auto 1fr; gap:28px; align-items:start; }
  @media (max-width:720px){ .notice{ grid-template-columns:1fr; gap:16px; } }
  .notice-tag{ background:var(--teal); color:#fff; font-size:13px; font-weight:700; letter-spacing:.04em; padding:9px 16px; border-radius:999px; white-space:nowrap; align-self:start; }
  .notice-body h3{ font-family:var(--serif); font-size:clamp(20px,2.7vw,26px); font-weight:600; margin:0 0 14px; color:#fff; line-height:1.5; }
  .notice-body p{ margin:0; font-size:16.5px; color:#d3dbe8; line-height:1.95; }
  .notice-body b{ color:#7fd3c8; font-weight:600; }

  /* ── pricing ── */
  .price-wrap{ overflow-x:auto; }
  .price-grid{ display:grid; grid-template-columns:repeat(2, minmax(280px,1fr)); gap:22px; }
  @media (max-width:760px){ .price-grid{ grid-template-columns:1fr; } }
  .plan{ border:1px solid var(--line); border-radius:18px; background:var(--surface); padding:34px 32px; display:flex; flex-direction:column; position:relative; }
  .plan.feature{ border-color:var(--teal); box-shadow:0 18px 44px -26px rgba(15,125,114,.5); }
  .plan .badge{ position:absolute; top:-13px; left:32px; background:var(--teal); color:#fff; font-size:12px; font-weight:700; letter-spacing:.04em; padding:6px 14px; border-radius:999px; }
  .plan .pname{ font-family:var(--serif); font-size:22px; font-weight:600; margin:0 0 4px; }
  .plan .ptag{ font-size:13.5px; color:var(--teal-deep); font-weight:600; margin:0 0 22px; min-height:2.6em; }
  .plan .price{ display:flex; align-items:baseline; gap:6px; margin-bottom:4px; }
  .plan .price b{ font-family:var(--serif); font-size:38px; font-weight:600; color:var(--ink); letter-spacing:.01em; font-variant-numeric:tabular-nums; }
  .plan .price .yen{ font-size:18px; color:var(--ink); }
  .plan .price .per{ font-size:13px; color:var(--ink-faint); }
  .plan .tax{ font-size:12px; color:var(--ink-faint); margin:0 0 24px; }
  .plan ul{ margin:0 0 26px; padding:22px 0 0; list-style:none; display:grid; gap:12px; border-top:1px solid var(--line); }
  .plan li{ font-size:15px; color:var(--ink-soft); padding-left:26px; position:relative; line-height:1.65; }
  .plan li b{ color:var(--ink); font-weight:600; }
  .plan li::before{ content:""; position:absolute; left:0; top:6px; width:15px; height:15px; border-radius:50%; background:var(--teal-soft); }
  .plan li::after{ content:"✓"; position:absolute; left:3.5px; top:4px; font-size:10px; font-weight:700; color:var(--teal-deep); }
  .plan li.no{ color:var(--ink-faint); }
  .plan li.no::before{ background:var(--surface-2); }
  .plan li.no::after{ content:"—"; color:var(--ink-faint); left:2.5px; }
  .plan .btn{ margin-top:auto; justify-content:center; }
  .price-notes{ margin-top:26px; display:grid; gap:8px; }
  .price-notes p{ margin:0; font-size:14px; color:var(--ink-faint); padding-left:18px; position:relative; }
  .price-notes p::before{ content:"※"; position:absolute; left:0; top:0; }
  .opt-band{ margin-top:24px; display:flex; flex-wrap:wrap; align-items:center; justify-content:space-between; gap:18px; background:var(--crimson-soft); border:1px solid color-mix(in srgb,var(--crimson) 35%, transparent); border-radius:14px; padding:22px 26px; }
  .opt-band .ob-t{ font-weight:600; color:var(--ink); font-size:15.5px; }
  .opt-band .ob-t small{ display:block; font-weight:400; color:var(--ink-soft); font-size:13px; margin-top:4px; }
  .opt-band .ob-tag{ font-size:12px; font-weight:700; letter-spacing:.06em; color:var(--crimson); background:var(--surface); border:1px solid color-mix(in srgb,var(--crimson) 40%, transparent); padding:6px 13px; border-radius:999px; white-space:nowrap; }

  /* スポットプラン */
  .spot-plan{ margin-top:24px; border:1px solid var(--line); border-radius:18px; background:var(--surface); padding:clamp(28px,4vw,40px); }
  .spot-plan .pname{ font-family:var(--serif); font-size:23px; font-weight:600; margin:0 0 4px; }
  .spot-plan .ptag{ font-size:14px; color:var(--teal-deep); font-weight:600; margin:0 0 14px; }
  .spot-plan .sp-head p{ margin:0 0 26px; color:var(--ink-soft); font-size:16px; max-width:52em; }
  .sp-grid{ display:grid; grid-template-columns:1fr 1fr; gap:clamp(22px,3vw,40px); align-items:start; }
  @media (max-width:820px){ .sp-grid{ grid-template-columns:1fr; } }
  .sp-emg{ background:var(--crimson-soft); border:1px solid color-mix(in srgb,var(--crimson) 30%, transparent); border-radius:14px; padding:24px 26px; }
  .sp-emg-tag{ display:inline-block; font-size:12px; font-weight:700; letter-spacing:.06em; color:#fff; background:var(--crimson); padding:6px 14px; border-radius:999px; margin-bottom:14px; }
  .sp-emg h4{ font-family:var(--serif); font-size:20px; font-weight:600; margin:0 0 8px; }
  .sp-emg > p{ margin:0 0 16px; font-size:15px; color:var(--ink-soft); }
  .sp-emg ul, .sp-other ul{ margin:0; padding:0; list-style:none; display:grid; gap:10px; }
  .sp-emg li{ font-size:15px; color:var(--ink-soft); padding-left:22px; position:relative; }
  .sp-emg li::before{ content:""; position:absolute; left:2px; top:9px; width:8px; height:8px; border-radius:2px; background:var(--crimson); }
  .sp-other{ padding-top:4px; }
  .sp-other h4{ font-family:var(--serif); font-size:18px; font-weight:600; margin:0 0 14px; }
  .sp-other li{ font-size:15px; color:var(--ink-soft); padding-left:22px; position:relative; }
  .sp-other li::before{ content:""; position:absolute; left:2px; top:9px; width:8px; height:8px; border-radius:2px; background:var(--teal); opacity:.6; }

  /* プラン欄：3つの提供形態をラベル分け */
  .plan-block{ margin-top:46px; }
  .plan-block:first-of-type{ margin-top:0; }
  .plan-block .svc-detail, .plan-block .spot-plan{ margin-top:0; }
  .pb-label{ display:flex; align-items:center; gap:12px; font-family:var(--serif); font-size:21px; font-weight:600; margin-bottom:20px; }
  .pb-no{ font-family:var(--sans); font-size:12px; letter-spacing:.07em; color:var(--teal-deep); font-weight:700; background:var(--teal-soft); padding:6px 12px; border-radius:999px; }
  .pb-no.pb-emg{ color:var(--crimson); background:var(--crimson-soft); }
  .pb-cta{ margin-top:22px; }

  /* 団体・グループ一括契約の帯 */
  .group-band{ margin-top:30px; display:flex; align-items:center; gap:22px; flex-wrap:wrap; background:var(--teal-soft); border:1px solid color-mix(in srgb,var(--teal) 40%, transparent); border-radius:16px; padding:26px 30px; }
  .group-band .gb-ico{ width:54px; height:54px; border-radius:14px; background:var(--teal); color:#fff; display:grid; place-items:center; flex:none; }
  .group-band .gb-ico svg{ width:27px; height:27px; }
  .group-band .gb-text{ flex:1; min-width:230px; }
  .group-band .gb-text b{ display:block; font-family:var(--serif); font-size:19px; color:var(--ink); margin-bottom:5px; }
  .group-band .gb-text span{ font-size:15px; color:var(--ink-soft); }
  .group-band .btn{ white-space:nowrap; }

  /* ── comparison ── */
  .cmp{ overflow-x:auto; border:1px solid var(--line); border-radius:16px; }
  table.cmp-t{ border-collapse:collapse; width:100%; min-width:560px; background:var(--surface); font-size:15.5px; }
  table.cmp-t th, table.cmp-t td{ padding:15px 20px; text-align:left; border-bottom:1px solid var(--line); }
  table.cmp-t thead th{ background:var(--surface-2); font-size:12.5px; letter-spacing:.04em; color:var(--ink-soft); font-weight:600; }
  table.cmp-t thead th:last-child{ background:var(--navy); color:#fff; }
  table.cmp-t td:first-child{ font-weight:600; color:var(--ink); width:150px; }
  table.cmp-t td.old{ color:var(--ink-faint); }
  table.cmp-t td.new{ color:var(--teal-deep); font-weight:600; }
  table.cmp-t tr:last-child td{ border-bottom:none; }

  /* ── emergency flow ── */
  .flow{ display:grid; grid-template-columns:repeat(6,1fr); gap:12px; margin-top:8px; }
  @media (max-width:900px){ .flow{ grid-template-columns:repeat(3,1fr); } }
  @media (max-width:520px){ .flow{ grid-template-columns:repeat(2,1fr); } }
  .step{ background:var(--surface); border:1px solid var(--line); border-radius:12px; padding:20px 16px; text-align:center; position:relative; }
  .step .n{ width:30px; height:30px; border-radius:50%; background:var(--crimson); color:#fff; display:grid; place-items:center; font-size:13px; font-weight:700; margin:0 auto 12px; font-family:var(--serif); }
  .step .st{ font-size:14.5px; font-weight:600; color:var(--ink); line-height:1.5; }

  /* ── profile ── */
  .prof-grid{ display:grid; grid-template-columns:270px 1fr; gap:clamp(28px,5vw,58px); align-items:start; }
  @media (max-width:760px){ .prof-grid{ grid-template-columns:1fr; } }
  .prof-photo{ aspect-ratio:4/5; border-radius:18px; border:1px solid var(--line); background:linear-gradient(155deg, var(--navy-soft), var(--teal-soft)); display:grid; place-items:center; color:var(--navy-2); position:relative; overflow:hidden; }
  .prof-photo .initial{ font-family:var(--serif); font-size:92px; opacity:.45; }
  .prof-photo .ph-note{ position:absolute; bottom:14px; left:0; right:0; text-align:center; font-size:11px; letter-spacing:.08em; color:var(--ink-faint); }
  .prof-body h3{ font-family:var(--serif); font-size:26px; font-weight:600; margin:0 0 2px; }
  .prof-body h3 small{ font-size:14px; color:var(--ink-faint); font-weight:400; margin-left:10px; }
  .prof-body .role{ color:var(--teal-deep); font-size:15px; font-weight:600; margin:0 0 20px; }
  .prof-body p{ color:var(--ink-soft); margin:0 0 16px; font-size:16px; }
  .prof-table{ display:grid; gap:0; margin:22px 0; border:1px solid var(--line); border-radius:12px; overflow:hidden; }
  .prof-table .r{ display:grid; grid-template-columns:110px 1fr; }
  .prof-table .r:not(:last-child){ border-bottom:1px solid var(--line); }
  .prof-table .k{ background:var(--surface-2); padding:13px 16px; font-size:14px; font-weight:600; color:var(--ink); }
  .prof-table .v{ padding:13px 16px; font-size:15px; color:var(--ink-soft); }
  .msg{ background:var(--navy-soft); border-radius:12px; padding:22px 24px; font-size:15.5px; color:var(--ink); border-left:4px solid var(--navy-2); }
  .team{ margin-top:22px; }
  .team .tt{ font-size:13px; color:var(--ink-faint); margin-bottom:12px; }
  .chips{ display:flex; flex-wrap:wrap; gap:9px; }
  .chips span{ font-size:14px; color:var(--ink-soft); background:var(--surface); border:1px solid var(--line); padding:7px 15px; border-radius:999px; }

  .acts{ margin-top:26px; }
  .acts .at{ font-size:14px; color:var(--ink); font-weight:600; margin-bottom:12px; display:flex; align-items:center; gap:10px; }
  .acts .at::before{ content:""; width:4px; height:16px; border-radius:2px; background:var(--teal); }
  .acts ul{ list-style:none; margin:0; padding:0; border:1px solid var(--line); border-radius:12px; overflow:hidden; }
  .acts li{ display:flex; justify-content:space-between; align-items:baseline; gap:18px; padding:13px 18px; font-size:15px; color:var(--ink-soft); background:var(--surface); }
  .acts li:not(:last-child){ border-bottom:1px solid var(--line); }
  .acts li .yr{ color:var(--teal-deep); font-size:13.5px; font-weight:600; white-space:nowrap; font-variant-numeric:tabular-nums; }
  @media (max-width:520px){ .acts li{ flex-direction:column; gap:2px; } }

  /* ── process steps ── */
  .proc{ display:grid; grid-template-columns:repeat(5,1fr); gap:14px; counter-reset:s; }
  @media (max-width:900px){ .proc{ grid-template-columns:repeat(2,1fr); } }
  @media (max-width:520px){ .proc{ grid-template-columns:1fr; } }
  .pstep{ background:var(--surface); border:1px solid var(--line); border-radius:14px; padding:26px 22px; position:relative; }
  .pstep .pn{ font-family:var(--serif); font-size:13.5px; letter-spacing:.1em; color:var(--teal-deep); font-weight:600; margin-bottom:10px; }
  .pstep h4{ margin:0 0 8px; font-size:16.5px; font-weight:600; color:var(--ink); }
  .pstep p{ margin:0; font-size:14.5px; color:var(--ink-soft); line-height:1.7; }

  /* ── company ── */
  .co-table{ border:1px solid var(--line); border-radius:14px; overflow:hidden; }
  .co-table .r{ display:grid; grid-template-columns:180px 1fr; }
  @media (max-width:640px){ .co-table .r{ grid-template-columns:120px 1fr; } }
  .co-table .r:not(:last-child){ border-bottom:1px solid var(--line); }
  .co-table .k{ background:var(--navy); color:#eef2f8; padding:16px 20px; font-size:15px; font-weight:600; }
  .co-table .v{ background:var(--surface); padding:16px 20px; font-size:15.5px; color:var(--ink-soft); }
  .co-table .v .ph{ color:var(--crimson); border-bottom:1px dashed var(--crimson); }

  /* ── contact + line ── */
  .contact{ background:var(--navy); color:#eef2f8; }
  .contact .kicker{ color:#7fd3c8; }
  .contact .kicker::after{ background:rgba(255,255,255,.2); }
  .contact h2{ color:#fff; }
  .contact-grid{ display:grid; grid-template-columns:1fr 1fr; gap:clamp(28px,5vw,56px); align-items:stretch; }
  @media (max-width:840px){ .contact-grid{ grid-template-columns:1fr; } }
  .contact .intro{ color:#c6d0e0; max-width:30em; font-size:15.5px; }
  .cc{ background:rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.15); border-radius:16px; padding:32px; }
  .cc .field{ margin-bottom:22px; }
  .cc .lbl{ font-size:11.5px; letter-spacing:.12em; text-transform:uppercase; color:#7fd3c8; margin-bottom:6px; font-weight:600; }
  .cc .val{ font-size:17px; color:#fff; }
  .cc .val a{ color:inherit; }
  .cc .ph{ color:#e6a89f; border-bottom:1px dashed #e6a89f; }
  .line-box{ margin-top:14px; background:rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.15); border-radius:16px; padding:26px 28px; display:flex; gap:20px; align-items:center; flex-wrap:wrap; }
  .line-box .li-ico{ width:52px; height:52px; border-radius:14px; background:#06c755; display:grid; place-items:center; color:#fff; font-weight:800; font-size:13px; flex:none; letter-spacing:.02em; }
  .line-box .li-t{ flex:1; min-width:180px; }
  .line-box .li-t b{ display:block; color:#fff; font-size:17px; margin-bottom:3px; }
  .line-box .li-t span{ color:#c6d0e0; font-size:14px; }

  /* ── footer ── */
  footer{ background:var(--ground); border-top:1px solid var(--line); padding:48px 0 60px; }
  .foot{ display:flex; flex-wrap:wrap; justify-content:space-between; gap:26px; align-items:flex-start; }
  .foot .lead{ max-width:24em; }
  .foot .lead p{ color:var(--ink-faint); font-size:14px; margin:12px 0 0; }
  .foot-links{ display:flex; gap:24px; flex-wrap:wrap; }
  .foot-links a{ color:var(--ink-soft); text-decoration:none; font-size:15px; }
  .foot-links a:hover{ color:var(--teal); }
  .copy{ color:var(--ink-faint); font-size:13.5px; margin-top:30px; padding-top:22px; border-top:1px solid var(--line); }

  .reveal{ opacity:0; transform:translateY(18px); transition:opacity .7s ease, transform .7s ease; }
  .reveal.in{ opacity:1; transform:none; }

  /* ── hamburger / mobile menu ── */
  .hamburger{ display:none; background:transparent; border:1px solid rgba(255,255,255,0); border-color:var(--line); border-radius:10px; width:44px; height:40px; cursor:pointer; padding:0; flex:none; }
  .hamburger span{ display:block; width:22px; height:2px; background:var(--ink); margin:5px auto; border-radius:2px; transition:.25s; }
  .hamburger.open span:nth-child(1){ transform:translateY(7px) rotate(45deg); }
  .hamburger.open span:nth-child(2){ opacity:0; }
  .hamburger.open span:nth-child(3){ transform:translateY(-7px) rotate(-45deg); }
  @media (max-width:960px){ .hamburger{ display:block; } }

  /* ── hero two-column + photo ── */
  .hero-grid{ display:grid; grid-template-columns:1.12fr .88fr; gap:clamp(30px,5vw,60px); align-items:center; }
  @media (max-width:900px){ .hero-grid{ grid-template-columns:1fr; gap:34px; } }
  .photo-frame{ position:relative; border-radius:20px; overflow:hidden; border:1px solid rgba(255,255,255,.2); background:linear-gradient(160deg, rgba(63,176,162,.24), rgba(34,58,102,.55)); aspect-ratio:4/3; display:grid; place-items:center; box-shadow:0 30px 60px -30px rgba(0,0,0,.5); }
  .photo-frame img{ width:100%; height:100%; object-fit:cover; display:block; }
  .photo-frame .ph-in{ text-align:center; color:#cfe0ec; padding:24px; }
  .photo-frame .ph-in svg{ width:54px; height:54px; opacity:.65; margin-bottom:12px; }
  .photo-frame .ph-in b{ display:block; font-size:14px; letter-spacing:.05em; margin-bottom:4px; color:#eaf2f7; }
  .photo-frame .ph-in span{ font-size:12px; color:#9fb6c9; }

  /* ── gallery strip ── */
  .gallery{ padding:clamp(46px,7vw,72px) 0; }
  .gallery .g-head{ text-align:center; max-width:40em; margin:0 auto 30px; }
  .gallery .g-head h3{ font-family:var(--serif); font-size:clamp(20px,2.8vw,26px); font-weight:600; margin:0 0 8px; }
  .gallery .g-head p{ margin:0; color:var(--ink-soft); font-size:16px; }
  .g-strip{ display:grid; grid-template-columns:repeat(3,1fr); gap:18px; }
  @media (max-width:760px){ .g-strip{ grid-template-columns:1fr; } }
  .g-photo{ border-radius:16px; overflow:hidden; border:1px solid var(--line); aspect-ratio:3/2; background:linear-gradient(160deg,var(--navy-soft),var(--teal-soft)); display:grid; place-items:center; text-align:center; }
  .g-photo img{ width:100%; height:100%; object-fit:cover; display:block; }
  .g-photo .lab{ padding:18px; color:var(--navy-2); }
  .g-photo .lab svg{ width:34px; height:34px; opacity:.55; margin-bottom:8px; }
  .g-photo .lab b{ display:block; font-size:14.5px; color:var(--ink); }
  .g-photo .lab span{ font-size:12.5px; color:var(--ink-faint); }

  /* ── contact form ── */
  .form{ display:grid; gap:16px; }
  .form .row{ display:grid; gap:16px; grid-template-columns:1fr 1fr; }
  @media (max-width:520px){ .form .row{ grid-template-columns:1fr; } }
  .form .fld label{ display:block; font-size:13.5px; font-weight:600; color:#eaf2f7; margin-bottom:7px; }
  .form .fld label .req{ color:#e6a89f; margin-left:5px; font-size:11.5px; }
  .form input, .form select, .form textarea{ width:100%; font-family:inherit; font-size:16px; color:#fff; background:rgba(255,255,255,.09); border:1px solid rgba(255,255,255,.22); border-radius:10px; padding:12px 14px; }
  .form textarea{ min-height:104px; resize:vertical; }
  .form input::placeholder, .form textarea::placeholder{ color:#90a3b8; }
  .form input:focus, .form select:focus, .form textarea:focus{ outline:2px solid var(--teal); outline-offset:1px; border-color:var(--teal); }
  .form select{ appearance:none; background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath fill='%23cfe0ec' d='M1 1l5 5 5-5'/%3E%3C/svg%3E"); background-repeat:no-repeat; background-position:right 14px center; padding-right:36px; }
  .form select option{ color:#111; }
  .form .btn{ width:100%; justify-content:center; margin-top:2px; }
  .form-note{ font-size:12.5px; color:#9fb6c9; margin:0; }
  .cc-details{ display:grid; gap:20px; margin-top:26px; }
</style>

<header>
  <div class="wrap nav">
    <a class="brand" href="#top" aria-label="医療安全総研 トップへ">
      <span class="logo"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 3l7 3v5c0 4.5-3 8-7 10-4-2-7-5.5-7-10V6l7-3z"/><path d="M9.5 12l1.8 1.8L15 10"/></svg></span>
      <span class="txt"><span class="jp">医療安全総研</span><span class="en">Patient Safety Partnership</span></span>
    </a>
    <button class="hamburger" id="hamburger" aria-label="メニューを開く" aria-expanded="false" aria-controls="navlinks">
      <span></span><span></span><span></span>
    </button>
    <nav class="nav-links" id="navlinks">
      <a href="#about">考え方</a>
      <a href="#service">サービス</a>
      <a href="#price">プラン</a>
      <a href="#emergency">有事対応</a>
      <a href="#profile">代表</a>
      <a href="#company">会社概要</a>
      <button class="theme-btn" id="theme" aria-label="配色を切り替え">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M21 12.8A9 9 0 1111.2 3a7 7 0 009.8 9.8z"/></svg>
      </button>
      <a href="#contact" class="nav-cta">無料相談</a>
    </nav>
  </div>
</header>

<main id="top">
  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div class="hero-grid">
        <div class="hero-text">
          <span class="eyebrow">Patient Safety Partnership</span>
          <h1><span class="l">病院の医療安全に、</span><br><span class="l"><span class="hl">もう一人の専門家</span>を。</span></h1>
          <p class="lede">
            日本の医療事故を、限りなくゼロに近づける社会へ。医療安全総研は、管理者の「判断」と現場の「対応」——
            その双方に年間を通じて伴走し、医療安全を「個人の頑張り」から「組織の仕組み」へと変えていく専門家集団です。
          </p>
          <div class="hero-actions">
            <a href="#contact" class="btn btn-primary">初回無料相談を申し込む <span class="arw">→</span></a>
            <a href="#service" class="btn btn-ghost" style="color:#eef2f8;border-color:rgba(255,255,255,.3)">サービスを見る</a>
          </div>
        </div>
        <div class="hero-visual">
          <!-- 写真差し替え枠：<img src="hero.jpg" alt="..."> に置き換え -->
          <div class="photo-frame">
            <div class="ph-in">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87M16 3.13a4 4 0 010 7.75"/></svg>
              <b>写真をここに（トップ画像）</b>
              <span>代表・スタッフ・現場の写真を掲載予定</span>
            </div>
          </div>
        </div>
      </div>
      <div class="hero-meta">
        <div class="m"><b>初回相談 0円</b><span>まずは話を聞くだけでも</span></div>
        <div class="m"><b>全国対応</b><span>オンライン中心・現地訪問も</span></div>
        <div class="m"><b>現役の専門医</b><span>特定機能病院の実務家が支援</span></div>
      </div>
    </div>
  </section>

  <!-- PHILOSOPHY / TWO STANCES -->
  <section id="about">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">01</span>私たちの考え</div>
        <h2>重大事故は、めったに起こりません。<br>だからこそ、その一度の初動が信用を左右します。</h2>
        <p>医療安全は、特定の誰かの努力だけで守れるものではありません。重大な事故が起きたとき、その対応の質を左右するのは——管理者の「判断力」と、現場の「対応力」。その両方が、同時に機能する必要があります。</p>
      </div>

      <div class="stances">
        <div class="stance mng reveal">
          <span class="tag">管理者の方へ</span>
          <h3>最終責任を負う立場として、判断の備えはできていますか。</h3>
          <p>重大事故は頻発せず「経験で学ぶ」機会がほぼありません。初めての事案に、即興の判断で対応せざるを得ない——。院内に相談相手を持ちにくく、顧問弁護士は法的助言はできても、医療安全の実務判断までは踏み込めません。</p>
          <p class="q">事故が起きたとき、管理者として動けますか？</p>
        </div>
        <div class="stance fld reveal">
          <span class="tag">医療安全担当者の方へ</span>
          <h3>孤立して抱え込むのではなく、相談できる専門家はいますか。</h3>
          <p>「何をすればいいか分からない」——これは個人の能力ではなく、構造的な課題です。担当者が変わるたびに体制がリセットされ、研修は形だけ、集めたインシデントも分析に活かしきれない。現場の負担は増え続けています。</p>
          <p class="q">何をすればよいか分からない時、相談できますか？</p>
        </div>
      </div>

      <div class="answer reveal">
        <div class="lbl">私たちの答え</div>
        <p>答えは、シンプルです。管理者と現場、その<span class="hl">双方に、私たちが伴走します</span>。医療安全を「個人の頑張り」ではなく<span class="hl">「仕組み」へ</span>。医療事故該当性の判断助言を、医療安全を専門とする医師のアドバイスとともに提供し、質の高い安全な医療を届ける医療機関へと機能させる。それが、医療安全総研の伴走支援です。</p>
      </div>
    </div>
  </section>

  <!-- GALLERY (写真差し替え枠) -->
  <section class="gallery">
    <div class="wrap">
      <div class="g-head">
        <h3>現場に、一番近い医療安全を専門とする医師。</h3>
      </div>
      <div class="g-strip">
        <div class="g-photo">
          <!-- 写真差し替え枠：<img src="photo1.jpg" alt="研修の様子"> に置き換え -->
          <div class="lab">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M2 3h20v14H2zM8 21h8M12 17v4"/></svg>
            <b>研修・講演の様子</b><span>写真をここに</span>
          </div>
        </div>
        <div class="g-photo">
          <!-- 写真差し替え枠：<img src="photo2.jpg" alt="現場での対話"> に置き換え -->
          <div class="lab">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg>
            <b>現場での対話・伴走</b><span>写真をここに</span>
          </div>
        </div>
        <div class="g-photo">
          <!-- 写真差し替え枠：<img src="photo3.jpg" alt="チーム"> に置き換え -->
          <div class="lab">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/></svg>
            <b>代表・チームの紹介</b><span>写真をここに</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICE -->
  <section id="service" class="alt">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">02</span>サービス</div>
        <h2>管理者と現場、双方を支える3つの関わり方。</h2>
        <p>年間を通じて伴走する「安全文化醸成」を軸に、いざという時の「有事対応」、そして必要な部分だけを頼める「スポット支援」。貴院の状況に合わせて組み合わせられます。</p>
      </div>

      <div class="svc-grid">
        <article class="svc a reveal">
          <div class="no">SERVICE 01</div>
          <div class="ico"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M20 6L9 17l-5-5"/><circle cx="12" cy="12" r="10" opacity=".25"/></svg></div>
          <h3>年間伴走支援</h3>
          <p class="sub">病院全体の医療安全文化の醸成</p>
          <p>1年を通じて貴院に伴走する基本サービス。平時の備え・有事の対応力・組織への定着を循環させ、担当者が代わっても機能し続ける「仕組み」をつくります。</p>
          <ul>
            <li>オンライン講義・責任者交流会</li>
            <li>定例ミーティング／現地訪問</li>
            <li>委員会・事例検討への助言</li>
            <li>経営層向け 医療安全レポート</li>
          </ul>
        </article>

        <article class="svc c reveal">
          <div class="no">SERVICE 02</div>
          <div class="ico"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 3l8 4v5c0 5-3.5 8-8 9-4.5-1-8-4-8-9V7l8-4z"/><path d="M12 8v5M12 16h.01"/></svg></div>
          <h3>相談パートナーシップ</h3>
          <p class="sub">何かあったときに相談できる窓口（主に有事対応）</p>
          <p>「誰に相談するか」を、事故が起きる前に決めておく。管理者・担当者が判断に迷う場面で、適時に相談できるメール／ホットライン窓口を確保します（相談料は別途）。</p>
          <ul>
            <li>有事対応（初動〜再発防止）の伴走</li>
            <li>M&amp;Mカンファレンス支援</li>
            <li>事故性・報告要否の判断相談</li>
            <li>緊急時に相談できるホットライン</li>
          </ul>
        </article>

        <article class="svc b reveal">
          <div class="no">SERVICE 03</div>
          <div class="ico"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><rect x="4" y="4" width="16" height="16" rx="2"/><path d="M8 9h8M8 13h8M8 17h5"/></svg></div>
          <h3>スポット支援</h3>
          <p class="sub">「ここだけ」の個別支援</p>
          <p>年間契約でなくても、必要なテーマだけを個別に。研修・RCA実務支援・マニュアル整備・院内教育動画の作成など、貴院の「今の課題」にピンポイントで対応します。</p>
          <ul>
            <li>各種研修・教育の実施</li>
            <li>RCA（根本原因分析）実務支援</li>
            <li>マニュアル・手順書の作成支援</li>
            <li>院内教育用動画の作成</li>
          </ul>
        </article>
      </div>

      <!-- support by role -->
      <div class="roles reveal">
        <div class="role-col mng">
          <h4><span class="dot"></span>管理者へのサポート</h4>
          <ul>
            <li>重大事案発生時の初動対応支援・判断助言</li>
            <li>院内事故調査の運営助言</li>
            <li>死亡時の事故性判定（医療起因性・予期性）の相談</li>
            <li>過失かもしれない事例発生時の判断サポート・助言</li>
            <li>法令・通知・診療報酬改定への対応（指針・マニュアル改定の指導）</li>
            <li>A類型・B類型の判断・報告に関する相談</li>
            <li>実際の業務運用の確認・点検</li>
            <li>緊急時の助言・相談</li>
            <li>経営層との対面でのディスカッション</li>
            <li>経営層向け 医療安全レポート</li>
          </ul>
        </div>
        <div class="role-col fld">
          <h4><span class="dot"></span>現場担当者へのサポート</h4>
          <div class="grp">学ぶ・つながる</div>
          <ul>
            <li>年4回のオンライン講義</li>
            <li>月1回のオンライン交流会（他施設担当者との情報交換）</li>
          </ul>
          <div class="grp">日常業務の支援</div>
          <ul>
            <li>マニュアル・手順書作成支援</li>
            <li>インシデントレポートの集積・分析支援</li>
            <li>院内周知・ニュースレター作成の支援</li>
            <li>事例について適宜メール相談</li>
          </ul>
          <div class="grp">事例検討・事故対応</div>
          <ul>
            <li>委員会・事例検討への助言／M&Mカンファレンスの支援</li>
            <li>原因究明・再発防止策の検討（RCA実務支援含む）</li>
          </ul>
        </div>
      </div>

      <!-- 制度改正 notice -->
      <div class="notice reveal">
        <div class="notice-tag">2026年度 制度改正への対応</div>
        <div class="notice-body">
          <h3>法令・通知・診療報酬改定に、まとめて対応します。</h3>
          <p>令和8年4月の医療法施行規則改正と2026年度診療報酬改定により、入院施設のあるすべての医療機関で「医療安全管理者の配置」「記録の整備」「医療事故判断プロセス（<b>A類型・B類型</b>）の指針への追加」などが求められます。「何を・いつまでに」を整理し、<b>指針・マニュアルの改定指導</b>から<b>実際の業務運用の確認</b>、<b>A類型・B類型の判断・報告の相談</b>まで、現役の実務家がタイムリーに伴走します。</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <section id="price">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">03</span>プラン</div>
        <h2>3つの関わり方と、料金プラン。</h2>
        <p>「年間伴走支援」「相談パートナーシップ」「スポット支援」の3つ。年間伴走支援はベーシック／プレミアムの2プラン、相談パートナーシップとスポット支援は必要に応じてご利用いただけます（内容に応じて別途お見積もり）。</p>
      </div>

      <!-- 01 年間伴走支援 -->
      <div class="plan-block">
        <div class="pb-label"><span class="pb-no">SERVICE 01</span>年間伴走支援</div>
        <div class="price-grid">
        <div class="plan feature reveal">
          <span class="badge">★ 最も選ばれているプラン</span>
          <div class="pname">ベーシック</div>
          <div class="ptag">判断・報告を支える実務パートナー</div>
          <ul>
            <li>オンラインセミナー・事例共有・<b>交流会</b></li>
            <li>現地訪問 <b>年2回</b></li>
            <li>定例オンラインMTG <b>年4回</b>（うち2回対面）</li>
            <li>事例検討助言／メール相談</li>
            <li>管理者との対面ディスカッション（現地訪問時）</li>
            <li>経営層レポート（年次）</li>
            <li class="no">院内教育動画の作成</li>
            <li>事故・有事対応：メール対応（オプション）</li>
          </ul>
          <a href="#contact" class="btn btn-primary">このプランを相談する</a>
        </div>

        <div class="plan reveal">
          <div class="pname">プレミアム</div>
          <div class="ptag">医療安全文化を醸成する外部医療安全担当者</div>
          <ul>
            <li>ベーシックの内容をすべて含む</li>
            <li>現地訪問 <b>年4回</b></li>
            <li>定例MTG <b>月1回</b>（委員会参加・うち4回対面）</li>
            <li>院内教育動画の作成 <b>年2本</b></li>
            <li>M&Mカンファレンス <b>事例ごとの運営支援</b></li>
            <li>チャット・メール相談の優先対応</li>
            <li>事故・有事対応：<b>ホットライン（初動対応）</b></li>
          </ul>
          <a href="#contact" class="btn btn-navy">このプランを相談する</a>
        </div>
      </div>
      </div>

      <!-- 02 相談パートナーシップ（有事対応） -->
      <div class="plan-block">
        <div class="pb-label"><span class="pb-no pb-emg">SERVICE 02</span>相談パートナーシップ（有事対応）</div>
        <div class="svc-detail reveal">
          <div class="sd-head">
            <span class="sd-tag">有事対応</span>
            <h3>「何かあったとき」に、すぐ相談できる関係を。</h3>
            <p>管理者・担当者が判断に迷う場面で、適時に相談できるパートナーシップです。主に<b>有事対応</b>の場面で力を発揮します（相談料は別途）。「誰に相談するか」を、事故が起きる前に決めておく仕組みです。</p>
          </div>
          <div class="sd-list">
            <div class="sd-item"><b>初動対応・ホットライン相談</b><span>発生直後の判断・記録の整え方を支援します。</span></div>
            <div class="sd-item"><b>事故性・報告要否の判断支援</b><span>医療起因性・予期性、センター報告該当性の判断。</span></div>
            <div class="sd-item"><b>院内事故調査の運営助言・RCA実務支援</b><span>委員会組成・進行、根本原因分析まで。</span></div>
            <div class="sd-item"><b>家族・遺族への説明支援／職員のケア</b><span>説明シナリオ・記録の整備、第二の被害者対応。</span></div>
            <div class="sd-item"><b>行政・警察・公表対応の助言／再発防止</b><span>再発防止策の策定・フォローまで支援します。</span></div>
            <div class="sd-item"><b>M&amp;Mカンファレンス支援</b><span>事例検討会の運営と、専門家視点での助言。</span></div>
          </div>
        </div>
        <div class="pb-cta"><a href="#contact" class="btn btn-navy">このプランを相談する <span class="arw">→</span></a></div>
      </div>

      <!-- 03 スポット支援 -->
      <div class="plan-block">
        <div class="pb-label"><span class="pb-no">SERVICE 03</span>スポット支援</div>
      <div class="spot-plan reveal">
        <div class="sp-head">
          <div class="ptag">必要な「ここだけ」を、単発で。</div>
          <p>年間契約でなくても大丈夫。「マニュアルのこの部分を相談したい」「単発で教育セミナーを開きたい」など、貴院の“今の課題”に必要な支援だけを、単発（スポット）でご利用いただけます。内容に応じて別途お見積もり。</p>
        </div>
        <div class="sp-grid">
          <div class="sp-other">
            <h4>よくあるご依頼</h4>
            <ul>
              <li>マニュアル・手順書の内容相談／作成支援</li>
              <li>単発の教育セミナー・院内研修の実施</li>
              <li>RCA（根本原因分析）の単発サポート</li>
              <li>院内教育用動画の作成</li>
            </ul>
          </div>
          <div class="sp-other">
            <h4>その他のご相談</h4>
            <ul>
              <li>M&amp;Mカンファレンスの単発支援</li>
              <li>制度改正（A/B類型）対応の相談</li>
              <li>インシデントの分析・改善の相談</li>
              <li>院内周知・ニュースレター作成の支援</li>
            </ul>
          </div>
        </div>
      </div>
        <div class="pb-cta"><a href="#contact" class="btn btn-navy">このプランを相談する <span class="arw">→</span></a></div>
      </div>

      <!-- 団体・グループ一括契約 -->
      <div class="group-band reveal">
        <div class="gb-ico"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M3 21h18M6 21V8l6-4 6 4v13M9 21v-4h6v4M9 12h.01M15 12h.01M12 12h.01"/></svg></div>
        <div class="gb-text">
          <b>団体・グループ医療機関の一括契約に対応します</b>
          <span>複数法人・複数施設（グループ病院・医療法人・関連施設など）での一括契約が可能です。規模やニーズに応じて、内容と料金を別途お見積もりします。</span>
        </div>
        <a href="#contact" class="btn btn-navy">まとめて相談する <span class="arw">→</span></a>
      </div>

      <div class="price-notes">
        <p>定例ミーティングは、現地訪問時は現地で、それ以外はオンラインで参加します。プレミアムは院内の医療安全委員会に外部アドバイザーとして参加します（原則 月1回）。</p>
        <p>医療事故対応は初動対応が重要であり、対応内容により結果が大きく変わる場合があります。詳細・お見積りはお問い合わせください。</p>
      </div>
    </div>
  </section>

  <!-- DIFFERENTIATION -->
  <section class="alt">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">04</span>従来との違い</div>
        <h2>年間を通じた“伴走”が、医療安全を病院文化に変える。</h2>
        <p>単発の研修やスポットのコンサルでは、医療安全の文化は根づきません。「平時の備え」「有事の対応力」「組織への定着」——この3つを年間契約で循環させます。</p>
      </div>
      <div class="cmp reveal">
        <table class="cmp-t">
          <thead>
            <tr><th>観点</th><th>従来の医療安全</th><th>医療安全総研の伴走支援</th></tr>
          </thead>
          <tbody>
            <tr><td>提供形態</td><td class="old">単発研修</td><td class="new">継続伴走型</td></tr>
            <tr><td>連携範囲</td><td class="old">院内完結</td><td class="new">他院横断の交流会</td></tr>
            <tr><td>体制の性質</td><td class="old">属人的（担当者依存）</td><td class="new">仕組み化</td></tr>
            <tr><td>事故後対応</td><td class="old">定型化していない</td><td class="new">標準化された手順</td></tr>
            <tr><td>運用実態</td><td class="old">形だけの運用</td><td class="new">実務で機能する体制</td></tr>
            <tr><td>緊急時の相談先</td><td class="old">相談先がない</td><td class="new">緊急時ホットライン</td></tr>
            <tr><td>制度対応</td><td class="old">改定への対応が後追い</td><td class="new">現役の実務家が最新制度にタイムリー対応</td></tr>
            <tr><td>事故分析の深さ</td><td class="old">手順の確認にとどまりがち</td><td class="new">医師が診療の中身まで踏み込む</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- EMERGENCY -->
  <section id="emergency">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">05</span>有事対応（オプション）</div>
        <h2>医療事故対応は、「初動」がすべてを左右します。</h2>
        <p>最初の1週間の判断と記録が、その後の調査・説明・法的責任のすべてに影響します。発生直後の初動から、実務レベルで伴走します。</p>
      </div>
      <div class="flow reveal">
        <div class="step"><div class="n">1</div><div class="st">発生・検知</div></div>
        <div class="step"><div class="n">2</div><div class="st">初動相談<br>（ホットライン）</div></div>
        <div class="step"><div class="n">3</div><div class="st">事実確認・<br>方針決定</div></div>
        <div class="step"><div class="n">4</div><div class="st">院内調査・<br>RCA</div></div>
        <div class="step"><div class="n">5</div><div class="st">家族・<br>遺族説明</div></div>
        <div class="step"><div class="n">6</div><div class="st">再発防止策・<br>実装</div></div>
      </div>
      <div class="roles reveal" style="grid-template-columns:1fr;">
        <div class="role-col fld">
          <h4><span class="dot" style="background:var(--crimson)"></span>提供する有事対応の内容</h4>
          <ul style="grid-template-columns:1fr 1fr; display:grid; gap:8px 30px;">
            <li>発生直後の初動対応支援・ホットライン相談</li>
            <li>事故性・報告要否（医療起因性・予期性）の判断支援</li>
            <li>院内事故調査の運営助言（委員会組成・進行・外部委員選定）</li>
            <li>RCA（根本原因分析）の実務支援</li>
            <li>家族・遺族への説明支援（シナリオ・記録の整備）</li>
            <li>当事者職員のケア（第二の被害者対応）</li>
            <li>行政・警察・公表対応の助言</li>
            <li>再発防止策の策定・フォローまで支援</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- PROFILE -->
  <section id="profile" class="alt">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">06</span>代表プロフィール</div>
        <h2>“医師”という、もう一人の専門家。</h2>
      </div>
      <div class="prof-grid">
        <div class="reveal">
          <div class="prof-photo">
            <span class="initial">平</span>
            <span class="ph-note">写真は後で差し替え可</span>
          </div>
        </div>
        <div class="prof-body reveal">
          <h3>平松 真理子<small>ひらまつ まりこ</small></h3>
          <p class="role">医療安全総研 代表取締役／医師・最高質安全管理責任者（CQSO）</p>
          <p>
            現役の特定機能病院で、医療安全管理者・医師として医療安全実務の第一線に立つ。制度改定・診療報酬改定・行政通知などの最新動向にタイムリーに対応し、複数の医療機関への支援実績を持つ。医療事故対応・RCA・体制構築の実務経験を軸に、「正しいけれど動かない」を「実際に動く」へと変える支援を行う。
          </p>
          <div class="prof-table">
            <div class="r"><div class="k">現職</div><div class="v">慶應義塾大学病院 医療安全管理部 専任講師・医療安全管理者（専従）・医師</div></div>
            <div class="r"><div class="k">兼務</div><div class="v">名古屋大学医学部附属病院 患者安全推進部 招へい教員</div></div>
            <div class="r"><div class="k">資格</div><div class="v">医師・医学博士／耳鼻咽喉科専門医／頭頸部外科専門医／最高質安全管理責任者（CQSO）</div></div>
            <div class="r"><div class="k">専門領域</div><div class="v">患者安全（医療安全）・医療の質／医療事故対応・RCA・院内体制構築・医療安全教育</div></div>
          </div>
          <div class="msg">
            医療安全の現場で培った実務経験をもとに、貴院の実情に即した現実的な支援を行います。管理者と現場、その両方が同じ方向を向ける環境づくりに、私たちが少しでもお役に立てれば幸いです。
          </div>

          <div class="acts">
            <div class="at">主な活動・講師歴</div>
            <ul>
              <li><span>医療の質・安全学会　代議員</span><span class="yr">2022年〜現在</span></li>
              <li><span>日本病院会　医療安全管理者講習 アドバンストコース 講師</span><span class="yr">2021年〜現在</span></li>
              <li><span>東海北陸厚生局　医療安全ワークショップ 企画・講師</span><span class="yr">2021年〜現在</span></li>
              <li><span>日本助産師会　医療法に基づく医療安全関連研修システム構築プロジェクトチーム メンバー</span><span class="yr">2026年〜現在</span></li>
              <li><span>都内公的病院の医療安全講師（定期）</span><span class="yr">2024年〜現在</span></li>
              <li><span>愛知県看護協会　医療安全管理者養成研修会 講師</span><span class="yr">2021〜2024年</span></li>
            </ul>
          </div>

          <div class="team">
            <div class="tt">代表に加え、各分野の実務専門家がアドバイザリーボードとして、貴院の規模・診療領域・課題に応じて伴走します。</div>
            <div class="chips">
              <span>医師</span><span>看護師</span><span>弁護士</span><span>薬剤師</span>
              <span>臨床工学技士</span><span>事務</span><span>システムエンジニア</span><span>経営コンサルタント</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section id="process">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">07</span>ご導入の流れ</div>
        <h2>お問い合わせから、サービス開始まで。</h2>
        <p>まずは「話を聞くだけ」でも構いません。初回相談は無料です。</p>
      </div>
      <div class="proc reveal">
        <div class="pstep"><div class="pn">STEP 1</div><h4>お問い合わせ・無料相談</h4><p>約60分／オンライン・対面。まずはお気軽にご相談ください。</p></div>
        <div class="pstep"><div class="pn">STEP 2</div><h4>プラン提案・お見積もり</h4><p>課題に応じたご提案と、お見積もりをお出しします。</p></div>
        <div class="pstep"><div class="pn">STEP 3</div><h4>ご契約</h4><p>プラン確定後、契約を締結します。</p></div>
        <div class="pstep"><div class="pn">STEP 4</div><h4>キックオフ</h4><p>体制・課題のヒアリングを行います。</p></div>
        <div class="pstep"><div class="pn">STEP 5</div><h4>サービス開始</h4><p>年間を通じた伴走支援を開始します。</p></div>
      </div>
    </div>
  </section>

  <!-- COMPANY -->
  <section id="company" class="alt">
    <div class="wrap">
      <div class="sec-head">
        <div class="kicker"><span class="no">08</span>会社概要</div>
        <h2>会社概要</h2>
      </div>
      <div class="co-table reveal">
        <div class="r"><div class="k">会社名</div><div class="v">医療安全総研（株式会社医療安全総研）</div></div>
        <div class="r"><div class="k">代表</div><div class="v">代表取締役　平松 真理子</div></div>
        <div class="r"><div class="k">設立</div><div class="v">2026年8月</div></div>
        <div class="r"><div class="k">所在地</div><div class="v">東京都墨田区</div></div>
        <div class="r"><div class="k">資格者</div><div class="v">医師・看護師・弁護士・薬剤師・臨床工学技士・医療安全管理者ほか／各分野の実務専門家がチームを構成</div></div>
        <div class="r"><div class="k">対応エリア</div><div class="v">全国対応（オンライン中心。現地訪問はご契約プランに応じて実施）</div></div>
        <div class="r"><div class="k">対象</div><div class="v">病院・診療所・有床診療所などの医療機関（特定機能病院／一般病院／療養型・ケアミックス等、規模を問わず）。医療安全対策加算の取得・未取得いずれも対応可能。</div></div>
        <div class="r"><div class="k">サービス</div><div class="v">医療安全 年間伴走支援／有事対応支援（オプション）／オンライン講義・責任者交流会／院内事故調査・RCA実務支援／マニュアル整備・院内教育動画作成 ほか</div></div>
        <div class="r"><div class="k">Web</div><div class="v">https://www.patient-safety.org/</div></div>
        <div class="r"><div class="k">連絡先</div><div class="v"><a href="mailto:ma.7.ri.6.ko@gmail.com" data-email>ma.7.ri.6.ko@gmail.com</a></div></div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="contact">
    <div class="wrap">
      <div class="contact-grid">
        <div>
          <div class="kicker"><span class="no">09</span>お問い合わせ</div>
          <h2>初回相談は無料です。<br>まずは、お気軽に。</h2>
          <p class="intro">
            院内研修、講演、伴走支援、有事対応、教材づくりなどのご依頼・ご相談を承っています。
            「話を聞くだけ」でも構いません。下のフォームからお気軽にどうぞ。秘密は厳守します。
          </p>
          <div class="cc-details">
            <div class="cc reveal">
              <div class="field">
                <div class="lbl">Email</div>
                <div class="val"><a href="mailto:ma.7.ri.6.ko@gmail.com" data-email>ma.7.ri.6.ko@gmail.com</a></div>
              </div>
              <div class="field">
                <div class="lbl">公式サイト</div>
                <div class="val"><a href="https://www.patient-safety.org/">www.patient-safety.org</a></div>
              </div>
            </div>
            <div class="line-box reveal">
              <span class="li-ico">LINE</span>
              <div class="li-t">
                <b>公式LINE 無料登録</b>
                <span>医療安全の最新情報・有害事象の事例・実務資料を無料でお届け</span>
              </div>
              <a href="https://lin.ee/PrjoYeo" data-line class="btn btn-light" style="white-space:nowrap;">友だち登録</a>
            </div>
          </div>
        </div>
        <div>
          <div class="cc reveal">
            <form method="POST" class="form" id="contactForm">
              <input type="hidden" name="_subject" value="医療安全総研HP からお問い合わせがありました">
              <input type="hidden" name="_template" value="table">
              <input type="text" name="_honey" style="display:none !important" tabindex="-1" autocomplete="off" aria-hidden="true">
              <div class="fld">
                <label for="f-org">医療機関・施設名 <span class="req">必須</span></label>
                <input id="f-org" name="施設名" required placeholder="〇〇病院">
              </div>
              <div class="row">
                <div class="fld">
                  <label for="f-name">お名前 <span class="req">必須</span></label>
                  <input id="f-name" name="お名前" required placeholder="山田 太郎">
                </div>
                <div class="fld">
                  <label for="f-mail">メールアドレス <span class="req">必須</span></label>
                  <input id="f-mail" type="email" name="メール" required placeholder="mail@example.com">
                </div>
              </div>
              <div class="row">
                <div class="fld">
                  <label for="f-tel">電話番号（任意）</label>
                  <input id="f-tel" name="電話番号" placeholder="03-1234-5678">
                </div>
                <div class="fld">
                  <label for="f-type">ご相談内容 <span class="req">必須</span></label>
                  <select id="f-type" name="ご相談内容" required>
                    <option value="" disabled selected>選択してください</option>
                    <option>年間伴走支援について</option>
                    <option>相談パートナーシップについて</option>
                    <option>有事対応について</option>
                    <option>研修・講演のご依頼</option>
                    <option>制度改正（A/B類型）対応の相談</option>
                    <option>その他</option>
                  </select>
                </div>
              </div>
              <div class="fld">
                <label for="f-msg">メッセージ <span class="req">必須</span></label>
                <textarea id="f-msg" name="メッセージ" required placeholder="ご相談内容をご記入ください。「話を聞くだけ」でも構いません。"></textarea>
              </div>
              <button type="submit" class="btn btn-primary">この内容で送信する <span class="arw">→</span></button>
              <p class="form-note">送信いただいた内容は担当者のメールに届きます。秘密厳守。通常2〜3営業日以内にご返信します。</p>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">
    <div class="foot">
      <div class="lead">
        <a class="brand" href="#top" style="display:inline-flex">
          <span class="logo"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 3l7 3v5c0 4.5-3 8-7 10-4-2-7-5.5-7-10V6l7-3z"/><path d="M9.5 12l1.8 1.8L15 10"/></svg></span>
          <span class="txt"><span class="jp">医療安全総研</span><span class="en">Patient Safety Partnership</span></span>
        </a>
        <p>病院の医療安全に、“医師”というもう一人の専門家を。管理者の判断と現場の実務、その双方に、私たちが伴走します。</p>
      </div>
      <nav class="foot-links">
        <a href="#about">考え方</a>
        <a href="#service">サービス</a>
        <a href="#price">プラン</a>
        <a href="#emergency">有事対応</a>
        <a href="#company">会社概要</a>
        <a href="#contact">お問い合わせ</a>
        <a href="https://www.patient-safety.org/">公式サイト</a>
        <a href="https://lin.ee/PrjoYeo" data-line>公式LINE</a>
      </nav>
    </div>
    <div class="copy">© 2026 医療安全総研（株式会社医療安全総研） ｜ Patient Safety Partnership ｜ www.patient-safety.org</div>
  </div>
</footer>

<script>
  (function(){
    var root=document.documentElement, btn=document.getElementById('theme');
    btn&&btn.addEventListener('click',function(){
      var cur=root.getAttribute('data-theme');
      if(!cur){ cur=matchMedia('(prefers-color-scheme: dark)').matches?'dark':'light'; }
      root.setAttribute('data-theme', cur==='dark'?'light':'dark');
    });
  })();
  (function(){
    var ham=document.getElementById('hamburger'), menu=document.getElementById('navlinks');
    if(!ham||!menu) return;
    function toggle(open){
      var willOpen = open===undefined ? !menu.classList.contains('open') : open;
      menu.classList.toggle('open', willOpen);
      ham.classList.toggle('open', willOpen);
      ham.setAttribute('aria-expanded', willOpen?'true':'false');
    }
    ham.addEventListener('click', function(){ toggle(); });
    menu.addEventListener('click', function(e){ if(e.target.tagName==='A'){ toggle(false); } });
  })();
  (function(){
    var form=document.getElementById('contactForm');
    if(!form) return;
    form.addEventListener('submit', async function(e){
      e.preventDefault();
      var btn=form.querySelector('button[type=submit]');
      var orig=btn.innerHTML; btn.disabled=true; btn.textContent='送信中…';
      var payload=Object.fromEntries(new FormData(form).entries());
      try{
        var res=await fetch('https://formsubmit.co/ajax/ma.7.ri.6.ko@gmail.com',{
          method:'POST',
          headers:{'Content-Type':'application/json','Accept':'application/json'},
          body:JSON.stringify(payload)
        });
        var json=await res.json();
        if(json.success===true||json.success==='true'){ window.location.href='/thanks.html'; }
        else { throw new Error(json.message||'error'); }
      }catch(err){
        btn.disabled=false; btn.innerHTML=orig;
        alert('申し訳ありません、送信に失敗しました。お手数ですが時間をおいて再度お試しいただくか、メール（ma.7.ri.6.ko@gmail.com）でご連絡ください。');
      }
    });
  })();
  (function(){
    if(matchMedia('(prefers-reduced-motion: reduce)').matches){
      document.querySelectorAll('.reveal').forEach(function(e){e.classList.add('in');}); return;
    }
    var io=new IntersectionObserver(function(es){
      es.forEach(function(e){ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target);} });
    },{threshold:.12});
    document.querySelectorAll('.reveal').forEach(function(e){ io.observe(e); });
  })();
</script>
</html>
