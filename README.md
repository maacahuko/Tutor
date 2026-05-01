# Tutor
A website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tutor Uko — Time Master Quiz</title>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;600;800&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --navy:#0a1931; --gold:#f5a623; --teal:#00bcd4;
  --green:#43a047; --red:#e53935; --purple:#7c3aed;
  --bg1:#e8f4fd; --bg2:#fff8e1; --bg3:#e8f5e9;
  --white:#ffffff; --card:#ffffff;
  --shadow:0 10px 40px rgba(10,25,49,0.13);
}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'Nunito',sans-serif;background:linear-gradient(135deg,var(--bg1) 0%,var(--bg2) 50%,var(--bg3) 100%);min-height:100vh;overflow-x:hidden;}

/* ── TUTOR UKO LOGO WATERMARK (sidebar) ── */
.logo-sidebar{
  position:fixed;left:0;top:0;bottom:0;width:110px;
  background:var(--navy);
  display:flex;flex-direction:column;align-items:center;justify-content:center;gap:18px;
  z-index:5;
  box-shadow:4px 0 24px rgba(10,25,49,0.18);
}
.logo-sidebar svg{width:68px;height:68px;}
.logo-sidebar .brand-text{
  writing-mode:vertical-rl;text-orientation:mixed;
  transform:rotate(180deg);
  font-family:'Baloo 2',cursive;font-weight:800;font-size:1.1rem;
  color:var(--gold);letter-spacing:3px;text-transform:uppercase;
}
.logo-sidebar .tagline{
  writing-mode:vertical-rl;text-orientation:mixed;
  transform:rotate(180deg);
  font-size:0.62rem;color:rgba(255,255,255,0.55);
  letter-spacing:2px;text-transform:uppercase;margin-top:4px;
}
.logo-sidebar .divider{width:40px;height:2px;background:var(--gold);opacity:0.4;border-radius:2px;}

/* ── WATERMARK behind quiz ── */
.watermark{
  position:fixed;right:20px;bottom:20px;
  opacity:0.06;pointer-events:none;z-index:1;
  font-family:'Baloo 2',cursive;font-size:7rem;font-weight:800;
  color:var(--navy);line-height:1;text-align:right;
}

/* ── MAIN LAYOUT ── */
.page-wrap{margin-left:110px;padding:30px 30px 60px;max-width:820px;position:relative;z-index:10;}

/* ── HEADER ── */
header{text-align:center;padding-bottom:10px;}
.header-badge{
  display:inline-flex;align-items:center;gap:12px;
  background:var(--navy);color:var(--gold);
  font-family:'Baloo 2',cursive;font-size:2rem;font-weight:800;
  padding:12px 36px;border-radius:60px;
  box-shadow:0 6px 0 rgba(10,25,49,0.5),var(--shadow);
  animation:popIn .7s cubic-bezier(.34,1.56,.64,1) both;
}
.header-badge .ico{font-size:2rem;animation:tickTock 1s ease-in-out infinite alternate;display:inline-block;}
.subtitle{margin-top:10px;font-size:.95rem;color:var(--navy);font-weight:700;opacity:.7;}

/* progress */
.prog-wrap{max-width:580px;margin:18px auto 4px;background:rgba(255,255,255,.6);border-radius:20px;height:16px;overflow:hidden;box-shadow:inset 0 2px 6px rgba(0,0,0,.1);}
.prog-fill{height:100%;background:linear-gradient(90deg,var(--teal),var(--purple));border-radius:20px;transition:width .5s cubic-bezier(.34,1.56,.64,1);}
.prog-label{text-align:center;font-size:.82rem;color:var(--navy);font-weight:800;margin-top:4px;opacity:.7;}

/* section badge */
.section-badge{
  display:inline-block;margin:14px auto 0;
  background:var(--teal);color:#fff;
  font-size:.78rem;font-weight:800;letter-spacing:1.5px;text-transform:uppercase;
  padding:4px 16px;border-radius:20px;
}

/* ── CARD ── */
main{max-width:720px;margin:20px auto 0;}
.q-card{
  background:var(--card);border-radius:26px;
  box-shadow:var(--shadow),0 2px 0 #dce0ff;
  padding:32px 36px 36px;
  animation:cardIn .5s cubic-bezier(.34,1.56,.64,1) both;
  position:relative;overflow:hidden;
}
.q-card::before{content:'';position:absolute;top:0;left:0;right:0;height:5px;background:linear-gradient(90deg,var(--teal),var(--purple),var(--gold));border-radius:26px 26px 0 0;}
.q-num{font-family:'Baloo 2',cursive;font-size:.82rem;font-wei…
