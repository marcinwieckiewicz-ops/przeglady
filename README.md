<!doctype html><html lang="pl"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover"><meta name="mobile-web-app-capable" content="yes"><meta name="apple-mobile-web-app-capable" content="yes"><style>[hidden]{display:none!important}body{margin:0}img{max-width:100%}</style></head><body>
<title>Protokół kontroli okresowej</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap">
<style>
:root{
  --bg:#eef0ec;--panel:#ffffff;--panel2:#f7f8f5;--ink:#17212b;--muted:#5b6670;--line:#d5d9d2;
  --accent:#2f5597;--accent-ink:#ffffff;--accent-soft:#e4eaf5;
  --ok:#2e7d4f;--zad:#2f7f9b;--dst:#a86e12;--zla:#c0392b;--nd:#7a838b;
  --danger-soft:#fbe9e7;--warn-soft:#fdf3dc;
  --sans:"IBM Plex Sans",system-ui,-apple-system,"Segoe UI",Arial,sans-serif;
  --mono:"IBM Plex Mono",ui-monospace,Menlo,Consolas,monospace;
}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){
  color-scheme:dark;--bg:#11161b;--panel:#1a2027;--panel2:#161b21;--ink:#e6eaee;--muted:#9aa5ae;--line:#2e3740;
  --accent:#8fb0e8;--accent-ink:#0f1720;--accent-soft:#1f2b3d;--ok:#5cbf85;--zad:#5fb3d0;--dst:#e0a64a;--zla:#ef7a6d;--nd:#98a2ab;
  --danger-soft:#3a1f1c;--warn-soft:#352a14;}}
:root[data-theme="dark"]{
  color-scheme:dark;--bg:#11161b;--panel:#1a2027;--panel2:#161b21;--ink:#e6eaee;--muted:#9aa5ae;--line:#2e3740;
  --accent:#8fb0e8;--accent-ink:#0f1720;--accent-soft:#1f2b3d;--ok:#5cbf85;--zad:#5fb3d0;--dst:#e0a64a;--zla:#ef7a6d;--nd:#98a2ab;
  --danger-soft:#3a1f1c;--warn-soft:#352a14;}
*{box-sizing:border-box}
html,body{background:var(--bg)}
body{color:var(--ink);font-family:var(--sans);font-size:15px;line-height:1.45}
button,input,select,textarea{font:inherit;color:inherit}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}

.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:20;background:var(--panel);border-bottom:1px solid var(--line);padding-inline:16px}
.top-in{max-width:1280px;margin:0 auto;display:flex;align-items:center;gap:12px;padding-block:10px;flex-wrap:wrap}
.brand{display:flex;flex-direction:column;min-width:0;flex:1 1 220px}
.brand small{font-size:11px;letter-spacing:.08em;text-transform:uppercase;color:var(--muted)}
.brand b{font-size:16px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.actions{display:flex;gap:8px;flex-wrap:wrap}
.btn{border:1px solid var(--line);background:var(--panel);border-radius:6px;padding:7px 12px;cursor:pointer;font-size:14px;display:inline-flex;align-items:center;gap:6px;white-space:nowrap}
.btn:hover{border-color:var(--accent)}
.btn.pri{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.btn.sm{padding:4px 9px;font-size:13px}
.btn.ghost{border-color:transparent;background:transparent;color:var(--muted)}
.btn.ghost:hover{color:var(--zla)}
.btn.warn{border-color:var(--zla);color:var(--zla)}

.wrap{max-width:1280px;margin:0 auto;padding-inline:16px;padding-block:16px 60px;display:grid;grid-template-columns:270px minmax(0,1fr);gap:20px;align-items:start}
nav.cats{position:sticky;top:calc(env(safe-area-inset-top,0px) + 76px);display:flex;flex-direction:column;gap:2px;max-height:calc(100vh - 100px);overflow:auto}
.cat{display:grid;grid-template-columns:26px 1fr auto;gap:8px;align-items:center;text-align:left;border:0;background:transparent;border-radius:6px;padding:8px 10px;cursor:pointer}
.cat:hover{background:var(--panel)}
.cat.on{background:var(--panel);box-shadow:inset 3px 0 0 var(--accent)}
.cat .k{font-family:var(--mono);font-size:12px;color:var(--muted)}
.cat .t{font-size:14px;line-height:1.25}
.cat .t small{display:block;font-size:11.5px;color:var(--muted)}
.cnt{font-family:var(--mono);font-size:11px;color:var(--muted);white-space:nowrap}
.cnt .f{color:var(--zla);font-weight:500}
.navsep{font-size:11px;letter-spacing:.08em;text-transform:uppercase;color:var(--muted);padding:12px 10px 4px}

main{min-width:0}
.phead{display:flex;flex-wrap:wrap;align-items:flex-end;justify-content:space-between;gap:8px 16px;margin-bottom:14px}
.phead h1{font-size:22px;margin:0;text-wrap:balance;font-weight:600}
.law{font-family:var(--mono);font-size:12px;color:var(--muted)}
.card{background:var(--panel);border:1px solid var(--line);border-radius:8px;padding:16px;margin-bottom:14px}
.card h2{font-size:16px;margin:0 0 4px;font-weight:600;display:flex;gap:10px;align-items:baseline;flex-wrap:wrap}
.card h2 .n{font-family:var(--mono);font-size:13px;color:var(--accent)}
.hint{font-size:13px;color:var(--muted);margin:4px 0 10px}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:12px}
.fld{display:flex;flex-direction:column;gap:4px;min-width:0}
.fld.w2{grid-column:span 2}
.fld.full{grid-column:1/-1}
.fld label,.lbl{font-size:12px;color:var(--muted);letter-spacing:.02em}
input[type=text],input[type=date],input[type=number],select,textarea{width:100%;border:1px solid var(--line);background:var(--panel2);border-radius:6px;padding:8px 10px;min-width:0}
textarea{min-height:64px;resize:vertical}
input:focus,select:focus,textarea:focus{border-color:var(--accent);outline:none;background:var(--panel)}
.chk{display:flex;gap:8px;align-items:flex-start;cursor:pointer;font-size:14px}
.chk input{margin-top:3px;accent-color:var(--accent);width:16px;height:16px;flex:none}
.chips{display:flex;flex-wrap:wrap;gap:6px}
.chipc{border:1px solid var(--line);background:var(--panel2);border-radius:99px;padding:5px 12px;cursor:pointer;font-size:13.5px}
.chipc.on{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.alert{border-radius:6px;padding:10px 12px;font-size:14px;margin:10px 0 0}
.alert.red{background:var(--danger-soft);border:1px solid var(--zla)}
.alert.amb{background:var(--warn-soft);border:1px solid var(--dst)}
.alert.blue{background:var(--accent-soft);border:1px solid var(--accent)}

/* elementy */
.sec-top{display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap;align-items:center}
.el{border-top:1px solid var(--line);padding:10px 0}
.el:first-of-type{border-top:0}
.el-row{display:grid;grid-template-columns:minmax(150px,1fr) auto;gap:8px 12px;align-items:center}
.el-name{font-weight:500;display:flex;gap:6px;align-items:center;min-width:0}
.el-name .ref{font-family:var(--mono);font-size:11.5px;color:var(--zla);white-space:nowrap}
.rates{display:flex;flex-wrap:wrap;gap:4px}
.rt{border:1px solid var(--line);background:var(--panel2);border-radius:5px;padding:4px 8px;font-size:12.5px;cursor:pointer;line-height:1.2}
.rt[data-v=dobra].on{background:var(--ok);border-color:var(--ok);color:#fff}
.rt[data-v=zadow].on{background:var(--zad);border-color:var(--zad);color:#fff}
.rt[data-v=dost].on{background:var(--dst);border-color:var(--dst);color:#fff}
.rt[data-v=zla].on{background:var(--zla);border-color:var(--zla);color:#fff}
.rt[data-v=nd].on{background:var(--nd);border-color:var(--nd);color:#fff}
.el-more{display:grid;grid-template-columns:1fr 1fr 110px;gap:8px;margin-top:8px}
.el-more .fld.sug{grid-column:1/-1}
.el-more[hidden]{display:none}
.tog{border:0;background:none;color:var(--accent);cursor:pointer;font-size:12.5px;padding:0}
.pil{display:flex;gap:3px}
.pil button{width:30px;border:1px solid var(--line);background:var(--panel2);border-radius:5px;padding:6px 0;cursor:pointer;font-family:var(--mono);font-size:12.5px}
.pil button.on{background:var(--ink);color:var(--panel);border-color:var(--ink)}
.pil button.on[data-p="1"]{background:var(--zla);border-color:var(--zla);color:#fff}
.addrow{display:flex;gap:8px;margin-top:10px;flex-wrap:wrap}
.addrow input{flex:1 1 200px}

/* tabele w aplikacji */
.tw{overflow-x:auto}
table.t{border-collapse:collapse;width:100%;font-size:13.5px}
table.t th{font-size:11.5px;text-transform:uppercase;letter-spacing:.05em;color:var(--muted);text-align:left;font-weight:500;padding:6px 6px;border-bottom:1px solid var(--line)}
table.t td{padding:6px;border-bottom:1px solid var(--line);vertical-align:top}
table.t td.num{font-family:var(--mono);white-space:nowrap;font-size:12.5px}
.p1{color:var(--zla);font-weight:600}
.inst{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:4px 16px}
.inst .it{display:flex;justify-content:space-between;align-items:center;gap:8px;padding:5px 0;border-bottom:1px dashed var(--line);font-size:14px}
.yn{display:flex;border:1px solid var(--line);border-radius:5px;overflow:hidden;flex:none}
.yn button{border:0;background:var(--panel2);padding:3px 10px;cursor:pointer;font-size:12.5px}
.yn button.on{background:var(--accent);color:var(--accent-ink)}
.fph{grid-column:1/-1;display:flex;flex-direction:column;gap:6px;margin-top:4px}
.fph-list{display:flex;flex-wrap:wrap;gap:8px}
.fph-it{position:relative;width:96px;height:72px;border-radius:6px;overflow:hidden;border:1px solid var(--line)}
.fph-it img{width:100%;height:100%;object-fit:cover;display:block}
.fph-del{position:absolute;top:2px;right:2px;width:24px;height:24px;border-radius:50%;border:0;background:rgba(0,0,0,.6);color:#fff;cursor:pointer;font-size:12px;line-height:24px;padding:0}
.fph-btns{display:flex;gap:8px;flex-wrap:wrap}
.fph-btns label{position:relative;cursor:pointer}
.vh{position:absolute;width:1px;height:1px;opacity:0;overflow:hidden;clip:rect(0 0 0 0)}
.fph-btns label:focus-within{outline:2px solid var(--accent);outline-offset:2px}
.fi{border-top:1px solid var(--line);padding:12px 0;display:flex;flex-direction:column;gap:6px}
.fi:first-of-type{border-top:0}
.fi-h{display:flex;gap:10px;align-items:baseline;flex-wrap:wrap}
.fi-no{font-family:var(--mono);font-size:13px;color:var(--accent)}
.fi-p{font-family:var(--mono);font-size:12px;color:var(--muted);margin-left:auto}
.fi-p.p1{color:var(--zla)}
.fi-z{font-size:14px;color:var(--muted)}
.mbar{display:none}
.photos{display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:10px}
.ph{border:1px solid var(--line);border-radius:6px;overflow:hidden;background:var(--panel2);display:flex;flex-direction:column}
.ph img{aspect-ratio:4/3;object-fit:cover;width:100%;display:block}
.ph .pc{padding:6px;display:flex;gap:4px;align-items:center}
.ph .pc input{padding:4px 6px;font-size:13px}
.stat{display:flex;gap:18px;flex-wrap:wrap;font-size:13px;color:var(--muted);margin:8px 0 0}
.stat b{font-family:var(--mono);color:var(--ink);font-weight:500}
.cover{max-width:320px;border-radius:6px;border:1px solid var(--line);display:block;margin-top:8px}

/* podgląd dokumentu */
.sheet-wrap{overflow-x:auto;background:var(--panel2);border:1px solid var(--line);border-radius:8px;padding:16px}
.sheet{background:#fff;color:#000;width:100%;max-width:794px;min-width:560px;margin:0 auto;padding:40px 44px;box-shadow:0 1px 4px rgba(0,0,0,.18)}

.toast{position:fixed;left:50%;bottom:calc(20px + env(safe-area-inset-bottom,0px));transform:translateX(-50%);background:var(--ink);color:var(--panel);padding:10px 16px;border-radius:6px;font-size:14px;z-index:50;max-width:calc(100% - 32px)}
.modal-bg{position:fixed;inset:0;background:rgba(10,15,20,.45);z-index:40;display:flex;align-items:center;justify-content:center;padding:16px}
.modal{background:var(--panel);border-radius:8px;padding:18px;max-width:440px;width:100%;border:1px solid var(--line)}
.modal h3{margin:0 0 6px;font-size:17px}
.modal .row{display:flex;gap:8px;justify-content:flex-end;margin-top:14px;flex-wrap:wrap}
.menu{position:relative}
.menu-pop{position:absolute;right:0;top:calc(100% + 6px);background:var(--panel);border:1px solid var(--line);border-radius:8px;padding:6px;min-width:260px;z-index:30;box-shadow:0 8px 24px rgba(0,0,0,.14);display:flex;flex-direction:column}
.menu-pop[hidden]{display:none}
.menu-pop button{text-align:left;border:0;background:none;padding:9px 10px;border-radius:5px;cursor:pointer;font-size:14px}
.menu-pop button:hover{background:var(--accent-soft)}
.menu-pop button small{display:block;color:var(--muted);font-size:12px}

@media (max-width:900px){
  .top{position:static}
  .wrap{grid-template-columns:1fr;gap:12px;padding-block:10px 60px}
  nav.cats{position:sticky;top:env(safe-area-inset-top,0px);z-index:10;flex-direction:row;overflow-x:auto;max-height:none;background:var(--bg);padding-block:6px;margin-inline:-16px;padding-inline:16px;scrollbar-width:none}
  .cat{grid-template-columns:auto auto;border:1px solid var(--line);background:var(--panel);white-space:nowrap;padding:6px 10px}
  .cat .t small,.cat .cnt,.navsep{display:none}
  .cat.on{box-shadow:none;border-color:var(--accent);background:var(--accent-soft)}
  .brand small{display:none}
}
@media (max-width:900px){
  body{padding-bottom:calc(72px + env(safe-area-inset-bottom,0px))}
  nav.cats{display:none!important}
  .mbar{display:flex;gap:8px;position:fixed;left:0;right:0;bottom:0;z-index:25;background:var(--panel);border-top:1px solid var(--line);padding:10px 16px calc(10px + env(safe-area-inset-bottom,0px))}
  .mbar select{flex:1;font-size:16px;padding:10px}
  .mbar .btn{padding:10px 16px;font-size:18px}
  input[type=text],input[type=date],input[type=number],select,textarea{font-size:16px}
  .rates{display:grid;grid-template-columns:repeat(3,1fr);gap:6px}
  .rt{padding:10px 4px;font-size:13.5px;text-align:center}
  .pil button{width:44px;padding:10px 0}
  .tog{font-size:14.5px;padding:6px 0}
  .fph-btns .btn{padding:10px 14px;font-size:15px}
  .fph-it{width:31%;height:auto;aspect-ratio:4/3}
  .chk{font-size:15px}
  .chk input{width:20px;height:20px}
  .top-in{padding-block:8px;gap:8px}
  .actions .btn{padding:8px 10px}
  #bPrev{display:none}
  .addrow.noprint{display:none}
  .toast{bottom:calc(84px + env(safe-area-inset-bottom,0px))}
}
@media (max-width:600px){
  .el-row{grid-template-columns:1fr}
  .el-more{grid-template-columns:1fr}
  .fld.w2{grid-column:auto}
  .phead h1{font-size:19px}
  .sheet{padding:24px 20px}
}
@media (prefers-reduced-motion:reduce){*{transition:none!important}}
@media print{
  .top,nav.cats,.phead,.noprint{display:none!important}
  body,html{background:#fff}
  .wrap{display:block;padding:0}
  .sheet-wrap{border:0;padding:0;background:#fff;overflow:visible}
  .sheet{box-shadow:none;padding:0;max-width:none;min-width:0}
  main > *:not(.printable){display:none!important}
}
</style>

<div class="top">
  <div class="top-in">
    <div class="brand"><small>Kontrola okresowa obiektu budowlanego</small><b id="hdrTitle">Protokół</b></div>
    <div class="actions">
      <button class="btn" id="bPrev" type="button">Podgląd protokołu</button>
      <div class="menu">
        <button class="btn pri" id="bExp" type="button" aria-haspopup="true">Pobierz ▾</button>
        <div class="menu-pop" id="expMenu" hidden>
          <button type="button" data-act="docx">Word (.docx)<small>Do edycji i druku, z nagłówkiem i numeracją stron</small></button>
          <button type="button" data-act="html">Dokument HTML<small>Otwórz w przeglądarce i wydrukuj do PDF</small></button>
          <button type="button" data-act="print" id="bPrint" hidden>Drukuj / zapisz jako PDF<small>Okno drukowania przeglądarki</small></button>
          <button type="button" data-act="json">Zapisz projekt (.json)<small>Do wczytania i dalszej edycji</small></button>
        </div>
      </div>
      <div class="menu">
        <button class="btn" id="bMore" type="button" aria-haspopup="true">Więcej ▾</button>
        <div class="menu-pop" id="moreMenu" hidden>
          <button type="button" data-act="load">Wczytaj projekt (.json)<small>Otwórz zapisany wcześniej protokół</small></button>
          <button type="button" data-act="next">Następna kontrola na podstawie tej<small>Zalecenia przechodzą do „Sprawdzenia zaleceń”, oceny są czyszczone</small></button>
          <button type="button" data-act="new">Nowy, pusty protokół<small>Zaczyna od zera</small></button>
        </div>
      </div>
      <input type="file" id="fileJson" accept=".json,application/json" hidden>
    </div>
  </div>
</div>

<div class="wrap">
  <nav class="cats" id="nav" aria-label="Kategorie"></nav>
  <main id="main"></main>
</div>

<div class="mbar" id="mbar"><button type="button" class="btn" id="mPrev" aria-label="Poprzednia kategoria">←</button><select id="mSel" aria-label="Kategoria"></select><button type="button" class="btn pri" id="mNext" aria-label="Następna kategoria">→</button></div>
<script>
"use strict";
/* ============================================================
   KATALOG
   ============================================================ */
const RATES=[["dobra","Dobra"],["zadow","Zadowalająca"],["dost","Dostateczna"],["zla","Zła"],["nd","Nie dotyczy"]];
const RATE_LBL=Object.fromEntries(RATES);
const RATE_ORDER={dobra:1,zadow:2,dost:3,zla:4};
const PIL=[
  [1,"bezzwłocznie","W czasie lub bezpośrednio po kontroli – bezpośrednie zagrożenie życia lub zdrowia ludzi, bezpieczeństwa mienia bądź środowiska, w szczególności katastrofą budowlaną, pożarem, wybuchem, porażeniem prądem elektrycznym albo zatruciem gazem."],
  [2,"miesiąc","Możliwość wystąpienia potencjalnego zagrożenia konstrukcji budynku i bezpieczeństwa użytkowania."],
  [3,"trzy miesiące","Możliwość pogłębiania się uszkodzeń i zagrożenia konstrukcji oraz bezpieczeństwa użytkowania w dłuższej perspektywie."],
  [4,"sześć miesięcy","Elementy i instalacje niepowodujące potencjalnych zagrożeń dla konstrukcji, ale mające wpływ na dalsze bezpieczne użytkowanie."],
  [5,"do następnej kontroli okresowej","Uszkodzenia niepowodujące zagrożeń dla konstrukcji, ludzi i środowiska, mające wpływ na postępujące zużycie elementu lub estetykę obiektu."]
];

const CH=[
 {id:"D",name:"Elementy budowlane",sub:"narażone na wpływy atmosferyczne i czynniki użytkowe",law:"art. 62 ust. 1 pkt 1 lit. a",
  title:"KONTROLA STANU TECHNICZNEGO ELEMENTÓW BUDYNKU, BUDOWLI I INSTALACJI NARAŻONYCH NA SZKODLIWE WPŁYWY ATMOSFERYCZNE I NISZCZĄCE DZIAŁANIA CZYNNIKÓW WYSTĘPUJĄCYCH PODCZAS UŻYTKOWANIA OBIEKTU",
  secs:[
   {id:"D1",name:"Elementy konstrukcji budynku",els:["Konstrukcja nośna budynku","Fundamenty","Izolacje przeciwwilgociowe","Ściany zewnętrzne","Ściany wewnętrzne nośne","Stropy","Schody","Balustrady"]},
   {id:"D2",name:"Zewnętrzne warstwy przegród zewnętrznych",els:["Elewacje","Cokół","Stolarka okienna","Stolarka drzwiowa zewnętrzna","Stolarka bramowa","Gzymsy","Attyki","Filary","Balkony, loggie","Daszki nad wejściami"]},
   {id:"D3",name:"Wewnętrzne warstwy przegród",els:["Ściany wewnętrzne działowe","Sufity","Posadzki","Stolarka drzwiowa wewnętrzna"]},
   {id:"D4",name:"Pokrycie dachowe, elementy dachowe, odprowadzenie wód opadowych",els:["Pokrycie dachowe","Obróbki blacharskie","Rynny i rury spustowe","Wpusty dachowe","Kominy i podstawy dachowe","Świetliki i klapy dymowe","Wyłazy i drabiny dachowe","Zabezpieczenia przed upadkiem z wysokości","Panele fotowoltaiczne na dachu"]},
   {id:"D5",name:"Elementy i urządzenia zamocowane do ścian i dachu budynku",els:["Szyldy, reklamy","Jednostki zewnętrzne klimatyzacji","Anteny, maszty","Konstrukcje wsporcze urządzeń","Oprawy oświetleniowe, kamery"]},
   {id:"D6",name:"Elementy zagospodarowania terenu i estetyki budynku oraz jego otoczenia",els:["Elementy utwardzenia terenu","Opaska wokół budynku","Teren biologicznie czynny","Ogrodzenie, bramy wjazdowe","Miejsce gromadzenia odpadów","Oświetlenie terenu","Estetyka obiektu i otoczenia"]}
 ]},
 {id:"E",name:"Instalacje ochrony środowiska",sub:"wod.-kan., c.o., wentylacja, klimatyzacja",law:"art. 62 ust. 1 pkt 1 lit. b",
  title:"KONTROLA STANU TECHNICZNEGO INSTALACJI I URZĄDZEŃ SŁUŻĄCYCH OCHRONIE ŚRODOWISKA",
  secs:[
   {id:"E1",name:"Zewnętrzna instalacja kanalizacji sanitarnej",els:["Studzienki kanalizacji sanitarnej","Przyłącze kanalizacji sanitarnej","Bezodpływowy zbiornik na ścieki","Przydomowa oczyszczalnia ścieków","Zawory burzowe","Separatory tłuszczu","Separatory substancji ropopochodnych"]},
   {id:"E2",name:"Zewnętrzna instalacja kanalizacji deszczowej",els:["Studzienki kanalizacji deszczowej","Przyłącze kanalizacji deszczowej","Wpusty uliczne, odwodnienia liniowe","Zbiorniki retencyjne / rozsączające"]},
   {id:"E3",name:"Zewnętrzna instalacja wodociągowa",els:["Przyłącze wodociągowe","Studnia / zestaw wodomierzowy","Zawory odcinające, zasuwy","Przejścia przez przegrody budowlane"]},
   {id:"E4",name:"Wewnętrzna instalacja kanalizacji sanitarnej",els:["Piony i poziomy","Podejścia pod przybory","Wpusty podłogowe","Urządzenia sanitarne, biała armatura"]},
   {id:"E5",name:"Wewnętrzna instalacja wodociągowa",els:["Przewody instalacji wodociągowej","Izolacje przewodów wodociągowych","Armatura zabezpieczająca","Zawory antyskażeniowe","Podgrzewacze wody","Stacja uzdatniania wody"]},
   {id:"E6",name:"Instalacja centralnego ogrzewania i źródło ciepła",els:["Źródło ciepła / węzeł cieplny","Przewody grzewcze w budynku","Izolacje przewodów grzewczych","Ogrzewanie grzejnikowe","Armatura zabezpieczająca"]},
   {id:"E7",name:"Instalacja wentylacji",els:["Kanały wentylacyjne wewnątrz budynku","Wywietrzaki dachowe","Wentylatory dachowe","Czerpnie i wyrzutnie powietrza","Anemostaty i kratki wentylacyjne","Centrala wentylacyjna","Odciągi miejscowe","Sprawność wentylacji"]},
   {id:"E8",name:"Instalacja klimatyzacji i urządzenia chłodnicze",els:["Agregaty chłodnicze","Jednostki wewnętrzne","Przewody chłodnicze","Kontrola szczelności (F-gazy)"]}
 ]},
 {id:"F",name:"Gaz i przewody kominowe",sub:"z odniesieniem do e-protokołu",law:"art. 62 ust. 1 pkt 1 lit. c",
  title:"KONTROLA INSTALACJI GAZOWYCH ORAZ PRZEWODÓW KOMINOWYCH",
  secs:[
   {id:"F1",name:"Instalacja gazowa",gas:true,els:["Kurek główny, szafka gazowa","Gazomierz","Przewody instalacji gazowej","Urządzenia gazowe","Szczelność instalacji","Wentylacja pomieszczeń z urządzeniami gazowymi"]},
   {id:"F2",name:"Przewody kominowe dymowe, spalinowe i wentylacyjne",chim:true,els:["Przewody kominowe dymowe","Przewody kominowe spalinowe","Czopuchy / podejścia do przewodów kominowych","Przewody kominowe wentylacyjne grawitacyjne","Przewody kominowe wentylacyjne o ciągu wymuszonym","Kominy wolnostojące"]}
 ]},
 {id:"G",name:"Elektryka i odgromowa",sub:"pełne badanie w kontroli 5-letniej",law:"art. 62 ust. 1 pkt 2",
  title:"KONTROLA INSTALACJI ELEKTRYCZNEJ I PIORUNOCHRONNEJ",
  secs:[
   {id:"G1",name:"Instalacja elektryczna",el:true,els:["Złącze kablowe","Rozdzielnica główna","Rozdzielnice piętrowe / obiektowe","Przewody i osprzęt","Przeciwpożarowy wyłącznik prądu","Pomiary instalacji elektrycznej","Instalacja fotowoltaiczna – falownik, zabezpieczenia"]},
   {id:"G2",name:"Instalacja piorunochronna",els:["Instalacja odgromowa – zwody i przewody","Złącza kontrolne","Uziemienia – pomiary rezystancji"]}
 ]},
 {id:"H",name:"Ppoż. i urządzenia techniczne",sub:"sprawdzenie dokumentów i stanu",law:"przepisy ppoż. i dozoru technicznego",
  title:"ZABEZPIECZENIA PRZECIWPOŻAROWE I URZĄDZENIA TECHNICZNE",
  secs:[
   {id:"H1",name:"Zabezpieczenia przeciwpożarowe budynku",els:["Hydranty zewnętrzne","Hydranty wewnętrzne","Zawory hydrantowe, zasuwy","Protokół z przeglądu hydrantów","Gaśnice / podręczny sprzęt ppoż.","Drogi ewakuacyjne","Oznakowanie ewakuacyjne","Oświetlenie awaryjne i ewakuacyjne","Drzwi i bramy przeciwpożarowe","Instalacja tryskaczowa / SSP / oddymianie"]},
   {id:"H2",name:"Urządzenia techniczne",els:["Dźwigi, platformy (decyzja UDT)","Bramy i drzwi automatyczne – serwis","Urządzenia ciśnieniowe (UDT)"]}
 ]}
];
const ALLSECS=[];CH.forEach(c=>c.secs.forEach(s=>{s.ch=c.id;ALLSECS.push(s)}));

const FIND={
"Pokrycie dachowe":[["Pęcherze, pęknięcia i nieszczelności papy","Naprawić pokrycie w miejscach uszkodzeń",4],["Brak części kapturków kominków wentylacyjnych papowych","Uzupełnić kapturki",4],["Zastoiny wody i lodu w korytach dachowych","Wyprowadzić spadki lub zamontować kable grzewcze; na bieżąco usuwać lód",5],["Przecieki przez pokrycie dachu","Zlokalizować i zlikwidować przecieki",2]],
"Elewacje":[["Zarysowany tynk na elewacji","Zabezpieczyć przed dalszą destrukcją i penetracją wody",5],["Zniszczenie systemowej dylatacji elewacyjnej","Uzupełnić / wymienić dylatację",4],["Nieprawidłowe zabezpieczenie przejść instalacyjnych przez ścianę","Uporządkować i wykonać szczelne przejścia instalacyjne z obróbkami blacharskimi",5],["Zabrudzenia, wykwity, korozja biologiczna","Oczyścić i zabezpieczyć elewację",5]],
"Cokół":[["Brak zabezpieczenia strefy cokołowej elewacji","Uzupełnić izolację i warstwę fakturową",5]],
"Stolarka okienna":[["Punktowa korozja stolarki stalowej i drobne nieszczelności","Oczyścić, zabezpieczyć antykorozyjnie i uszczelnić",5],["Uszkodzone okucia","Wyregulować / wymienić okucia",5]],
"Stolarka bramowa":[["Brak udokumentowanego serwisu bram","Zapewnić regularny serwis bram wg DTR",5]],
"Ściany wewnętrzne działowe":[["Uszkodzenie mechaniczne ściany z płyty warstwowej – odchylenie od pionu","Naprawić / wymienić, doprowadzając ścianę do pionu i stabilnego usytuowania",1]],
"Sufity":[["Uszkodzenia i zamoczenia części płyt sufitowych","Wymienić uszkodzone i uzupełnić brakujące płyty sufitowe",5]],
"Posadzki":[["Miejscowe spękania posadzek gresowych","Naprawić uszkodzone fragmenty posadzki",5]],
"Anteny, maszty":[["Luźne / zdemontowane anteny na dachu","Usunąć z powierzchni dachu",1]],
"Wyłazy i drabiny dachowe":[["Znacząca korozja elementów drabiny wyłazowej","Oczyścić i zabezpieczyć skorodowane elementy",5]],
"Świetliki i klapy dymowe":[["Korozja obrzeży świetlików","Oczyścić i zabezpieczyć przed dalszą destrukcją",4]],
"Wpusty dachowe":[["Brak siatek / koszy ochronnych na wpustach dachowych","Oczyścić rury spustowe, zamontować kosze ochronne na wpustach",5]],
"Rynny i rury spustowe":[["Zanieczyszczone rynny i rury spustowe","Oczyścić i udrożnić",5],["Uszkodzone mocowania rynien i rur spustowych","Uzupełnić mocowania",4]],
"Kominy i podstawy dachowe":[["Skorodowane cylindryczne wywietrzaki dachowe","Oczyścić, odrdzewić, zabezpieczyć farbą podkładową i nawierzchniową lub wymienić",4],["Uszkodzony wywietrzak dachowy","Wymienić podstawę dachową wraz z wywietrzakiem",1]],
"Wywietrzaki dachowe":[["Skorodowane wywietrzaki dachowe","Oczyścić, odrdzewić i zabezpieczyć lub wymienić",4]],
"Jednostki zewnętrzne klimatyzacji":[["Nieprawidłowe mocowanie / przejścia instalacyjne","Poprawić mocowanie i uszczelnić przejścia",5]],
"Wpusty podłogowe":[["Uszkodzony wpust podłogowy","Zamontować kratkę wpustową lub wymienić wpust",4]],
"Urządzenia sanitarne, biała armatura":[["Nieczynny przybór, ślady długotrwałych przecieków na podejściu","Naprawić / wymienić przybór i odcinek przewodu kanalizacyjnego",5]],
"Izolacje przewodów grzewczych":[["Uszkodzona izolacja przewodów grzewczych","Zdemontować uszkodzone powłoki, wymienić izolację w miejscach uszkodzonych",5]],
"Odciągi miejscowe":[["Brak podłączenia odciągu miejscowego spalin do kanału wywiewnego","Wykonać podłączenie odciągu spalin do kanału wywiewnego",1],["Uszkodzony przewód odciągu miejscowego","Wymienić przewód elastyczny, podłączyć do króćca",4]],
"Anemostaty i kratki wentylacyjne":[["Zanieczyszczone kratki wentylacyjne, odpadające powłoki","Wyczyścić kratki wraz z kanałem, odnowić powłoki",5],["Brak kratki wentylacyjnej wywiewnej","Zamontować kratkę wywiewną i połączyć trwale z przewodem",5],["Uszkodzony przewód wentylacyjny typu FLEX","Zdemontować uszkodzony przewód, zamontować kratkę wywiewną na kanale",5]],
"Sprawność wentylacji":[["Brak ciągu wentylacji wywiewnej","Udrożnić kanały wentylacyjne lub wykonać nową wentylację wywiewną",5],["Brak wentylacji w pomieszczeniu","Wykonać co najmniej wentylację grawitacyjną lub mechaniczną wywiewną",5]],
"Wentylatory dachowe":[["Korozja obudów wentylatorów","Przeprowadzić konserwację i malowanie",5]],
"Protokół z przeglądu hydrantów":[["Brak przeglądu jednego z hydrantów","Wykonać przegląd hydrantu potwierdzony protokołem",2]],
"Hydranty wewnętrzne":[["Brak aktualnego przeglądu hydrantów wewnętrznych","Wykonać przegląd i badanie węży",2]],
"Gaśnice / podręczny sprzęt ppoż.":[["Brak aktualnego przeglądu gaśnic","Wykonać przegląd gaśnic",2]],
"Oświetlenie awaryjne i ewakuacyjne":[["Brak protokołu z przeglądu oświetlenia awaryjnego","Wykonać przegląd i test oświetlenia awaryjnego",3]],
"Drogi ewakuacyjne":[["Zastawione drogi ewakuacyjne","Usunąć przeszkody z dróg ewakuacyjnych",1]],
"Instalacja odgromowa – zwody i przewody":[["Oderwane podstawy mocujące instalację odgromową","Przytwierdzić / wymienić uszkodzone podstawy",2]],
"Rozdzielnica główna":[["Brak zabezpieczenia wejścia do pomieszczenia rozdzielni głównej","Zabezpieczyć wejście do rozdzielni przed osobami nieuprawnionymi",1]],
"Pomiary instalacji elektrycznej":[["Brak aktualnych pomiarów (starszych niż 5 lat)","Wykonać pomiary skuteczności ochrony przeciwporażeniowej i rezystancji izolacji",2]],
"Uziemienia – pomiary rezystancji":[["Brak aktualnych pomiarów rezystancji uziemień","Wykonać pomiary instalacji piorunochronnej",2]],
"Kontrola szczelności (F-gazy)":[["Brak wpisu kontroli szczelności w CRO","Wykonać kontrolę szczelności i wpis do Centralnego Rejestru Operatorów",3]],
"Szczelność instalacji":[["Wyczuwalny zapach gazu / nieszczelność","Odciąć dopływ gazu, usunąć nieszczelność, wykonać próbę szczelności",1]]
};
const FIND_GEN=[["Brak bieżącej konserwacji","Przeprowadzić prace konserwacyjne",5],["Korozja elementów stalowych","Oczyścić i zabezpieczyć antykorozyjnie",5],["Uszkodzenie mechaniczne elementu","Naprawić / wymienić uszkodzony element",4],["Zanieczyszczenie elementu","Oczyścić",5],["Brak protokołu z serwisu wg DTR","Przedstawić protokół z serwisu urządzenia",4]];
const ZAL_SUG=["Przeprowadzić prace konserwacyjne","Przeprowadzić konserwację","Oczyścić i zabezpieczyć antykorozyjnie","Naprawić / wymienić uszkodzony element","Wykonać przegląd potwierdzony protokołem","Na bieżąco kontrolować stan elementu"];

const INST=["Instalacja zimnej wody (z.w.)","Instalacja ciepłej wody (c.w.)","Instalacja centralnego ogrzewania","Kocioł na paliwo stałe","Kocioł na olej opałowy","Kocioł na paliwo gazowe","Pompa ciepła","Kocioł elektryczny","Węzeł cieplny","Kanalizacja sanitarna","Kanalizacja deszczowa","Przewody dymowe","Przewody spalinowe","Przewody wentylacji grawitacyjnej","Instalacja wentylacji mechanicznej","Urządzenia klimatyzacji freonowej","Urządzenia chłodnicze","Separator tłuszczu","Separator ropopochodnych","Hydranty wewnętrzne","Hydranty zewnętrzne","Instalacja tryskaczowa","Instalacja zraszaczowa","Instalacja gazowa","Instalacja elektryczna","Instalacja odgromowa","Fotowoltaika","Dźwigi / platformy","System sygnalizacji pożarowej (SSP)"];

const OPIS=[["fundamenty","Fundamenty",["Płyta żelbetowa – brak oznak nadmiernego osiadania","Ławy żelbetowe","Stopy fundamentowe żelbetowe"]],["szkielet","Szkielet nośny",["Konstrukcja budynku stalowa","Konstrukcja żelbetowa szkieletowa","Konstrukcja murowana","Konstrukcja drewniana"]],["sciany","Ściany",["Z płyt warstwowych i murowane – stan dobry","Murowane z bloczków silikatowych","Żelbetowe"]],["stropy","Stropy",["Budynek parterowy","Żelbetowe monolityczne","Gęstożebrowe","Stalowe z blachą trapezową"]],["posadzki","Podłogi i posadzki",["Gres / beton zacierany","Płytki ceramiczne","Wykładzina PCV","Żywica epoksydowa"]],["schody","Klatka schodowa",["Schody na antresolę stalowe – stan dobry","Schody żelbetowe","Brak"]],["dach","Dach",["Płaski, pokryty papą termozgrzewalną","Płaski, pokryty membraną PVC","Blacha trapezowa","Stropodach wentylowany"]],["elewacje","Elewacje",["Ocieplenie styropianem i tynk cienkowarstwowy","Płyta warstwowa","Elewacja wentylowana","Tynk tradycyjny"]],["okna","Stolarka okienna",["Stalowa, aluminiowa, PCV","PCV","Aluminiowa"]],["drzwi","Stolarka drzwiowa",["Stalowa, aluminiowa","Aluminiowa przeszklona","Drewniana"]]];

const METODY=[
 ["snieg","Usuwać śnieg i lód z dachu na bieżąco, nie dopuszczając do obciążenia przekraczającego wartość projektową (orientacyjnie 50 kg/m²); prace prowadzić tak, aby nie uszkodzić pokrycia."],
 ["rynny","Czyścić rynny, wpusty dachowe i rury spustowe co najmniej dwa razy w roku (wiosną i jesienią) oraz po intensywnych opadach."],
 ["dachpo","Po silnych wiatrach, intensywnych opadach i wyładowaniach atmosferycznych sprawdzać stan pokrycia, obróbek i elementów zamocowanych do dachu (art. 61 pkt 2)."],
 ["koroz","Odnawiać powłoki antykorozyjne elementów stalowych (drabiny, wywietrzaki, balustrady, obróbki) w miarę ich zużycia."],
 ["elew","Utrzymywać szczelność przejść instalacyjnych i dylatacji elewacji; nie dopuszczać do zawilgacania strefy cokołowej."],
 ["went","Utrzymywać drożność kanałów i kratek wentylacyjnych; nie zasłaniać kratek i nie wyłączać wentylacji w pomieszczeniach."],
 ["dtr","Urządzenia (klimatyzacja, wentylacja, bramy, separatory) serwisować zgodnie z dokumentacją techniczno-ruchową producenta."],
 ["sep","Separatory opróżniać i czyścić w terminach wynikających z instrukcji eksploatacji i pozwolenia wodnoprawnego; przechowywać dokumenty odbioru odpadów."],
 ["ruch","Nie dopuszczać do ruchu pieszego po dachu poza wyznaczonymi ciągami komunikacyjnymi."],
 ["kob","Prowadzić książkę obiektu budowlanego (c-KOB) i dokonywać w niej wpisów o kontrolach, remontach i przebudowach."]
];

const ROLES=[["bud","elementów obiektu budowlanego"],["san","instalacji wod.-kan., c.o. i wentylacji"],["gaz","instalacji gazowej"],["kom","przewodów kominowych"],["el","instalacji elektrycznej i piorunochronnej"]];

const PRZYD=[
 ["tak","Obiekt nadaje się do dalszej bezpiecznej eksploatacji zgodnie z przeznaczeniem."],
 ["warunek","Obiekt nadaje się do dalszej eksploatacji pod warunkiem wykonania zaleceń w terminach określonych w protokole."],
 ["czesc","Obiekt nadaje się do eksploatacji w ograniczonym zakresie – do czasu usunięcia nieprawidłowości należy wyłączyć z użytkowania:"],
 ["nie","Obiekt nie nadaje się do eksploatacji – stan techniczny zagraża życiu lub zdrowiu ludzi, bezpieczeństwu mienia lub środowiska."]
];
const OGOLNA=[["dobra","Dobra"],["zadow","Zadowalająca"],["dost","Dostateczna"],["zla","Zła"],["awar","Awaryjna"]];

/* ============================================================
   STAN
   ============================================================ */
const KEY="protokol-kontroli-v1";
function blank(){
  return {
    meta:{nr:"",nazwa:"",ulica:"",kod:"",miejscowosc:"",woj:"",dzialka:"",funkcja:"",wlasciciel:"",wlAdres:"",uczestnicy:"",rok:"",kob:"",
      pCalk:"",pUzyt:"",pZab:"",kub:"",pDach:"",kPodz:"",kNad:"",
      rodzaj:{roczna:true,polroczna:false,piecio:false,dorazna:false},dorPowod:"",
      zakres:{a:true,b:true,c:true},data:"",dataOpr:"",nastepna:"",nast5:"",
      pogoda:"",temp:"",metodyK:{ogl:true,pom:false,dok:true,foto:true},ograniczenia:"",cover:""},
    opis:{},inst:{},osoby:[{imie:"",upr:"",nr:"",izba:"",rola:"bud"}],
    docs:{poprz:"",kob:true,dokt:false,pomEl:false,kom:false,hydr:false,ppoz:false,inne:""},
    prev:[],prevOgolnie:"",
    el:{},custom:{},sec:{},extra:[],
    gasNone:false,chim:{nr:"",data:"",kto:""},elec:{dataEl:"",nrEl:"",dataOdg:""},
    metody:{},metodyInne:"",
    concl:{ogolna:"",przyd:"",czesc:"",uwagi:"",pinb:"",pinbData:"",pinbSent:false},
    zal:{crub:false,inne:""},photos:[]
  };
}
let S;
function fresh(){const b=blank();INST.forEach(k=>b.inst[k]="");return b}
function load(){try{const r=localStorage.getItem(KEY);if(r){const o=JSON.parse(r);if(o&&o.meta&&o.meta.nr==="2024/11/2/Piaseczno")return fresh();return migrate(o)}}catch(e){}return fresh()}
function migrate(o){const b=blank();const out=Object.assign(b,o);out.meta=Object.assign(blank().meta,o.meta||{});out.concl=Object.assign(blank().concl,o.concl||{});out.docs=Object.assign(blank().docs,o.docs||{});return out}
let saveT,saveWarned=false;
function save(){clearTimeout(saveT);saveT=setTimeout(()=>{try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){if(!saveWarned){saveWarned=true;toast("Automatyczny zapis w przeglądarce niedostępny lub pełny (np. przez zdjęcia). Zapisz projekt do pliku .json.")}}},400);refreshCounts()}
S=load();

/* ============================================================
   NARZĘDZIA
   ============================================================ */
const $=s=>document.querySelector(s);
const esc=v=>String(v==null?"":v).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));
function fmtD(iso){if(!iso)return"";const [y,m,d]=iso.split("-");return d&&m&&y?`${d}.${m}.${y} r.`:iso}
function addMonths(iso,n){const d=new Date(iso+"T12:00:00");if(isNaN(d))return"";d.setMonth(d.getMonth()+n);return d.toISOString().slice(0,10)}
function toast(msg){const t=document.createElement("div");t.className="toast";t.textContent=msg;document.body.appendChild(t);setTimeout(()=>t.remove(),3800)}
function confirmBox(title,text,okLbl,cb){const bg=document.createElement("div");bg.className="modal-bg";bg.innerHTML=`<div class="modal" role="dialog" aria-modal="true"><h3>${esc(title)}</h3><div class="hint">${esc(text)}</div><div class="row"><button class="btn" type="button" data-x>Anuluj</button><button class="btn pri" type="button" data-ok>${esc(okLbl)}</button></div></div>`;document.body.appendChild(bg);bg.querySelector("[data-x]").onclick=()=>bg.remove();bg.querySelector("[data-ok]").onclick=()=>{bg.remove();cb()};bg.addEventListener("click",e=>{if(e.target===bg)bg.remove()});bg.querySelector("[data-ok]").focus()}
const elId=(sec,name)=>sec+"|"+name;
function secEls(sec){return sec.els.concat((S.custom[sec.id]||[]))}
function getEl(id){return S.el[id]||(S.el[id]={oc:"",find:"",zal:"",pil:0})}
function secInc(sec){const x=S.sec[sec.id];if(x&&typeof x.inc==="boolean")return x.inc;if(sec.gas)return true;return true}
function secObj(id){return S.sec[id]||(S.sec[id]={inc:true,opis:""})}
function chIncluded(ch){ if(ch.id==="F"&&!S.meta.zakres.c)return false; if(ch.id==="E"&&!S.meta.zakres.b)return false; if(ch.id==="D"&&!S.meta.zakres.a)return false; return ch.secs.some(s=>secInc(s))}

function nextControl(){
  if(S.meta.nastepna)return S.meta.nastepna;
  const d=S.meta.data;if(!d)return"";
  if(S.meta.rodzaj.polroczna){const y=+d.slice(0,4);const c=[`${y}-05-31`,`${y}-11-30`,`${y+1}-05-31`,`${y+1}-11-30`];return c.find(x=>x>d)}
  return addMonths(d,12);
}
function deadline(p){const d=S.meta.data;if(!p)return"";if(p===1)return"bezzwłocznie";if(!d)return PIL[p-1][1];if(p===5){const n=nextControl();return n?"do "+fmtD(n):"do następnej kontroli"}return "do "+fmtD(addMonths(d,{2:1,3:3,4:6}[p]))}
function needsHalfYear(){return (+S.meta.pZab||0)>2000||(+S.meta.pDach||0)>1000}

/* Numeracja rozdziałów i nieprawidłowości */
function structure(){
  const chaps=[];let n=4;
  CH.forEach(c=>{if(chIncluded(c)){n++;chaps.push({ch:c,num:n})}});
  const findNum=n+1;
  const findings=[];let k=0;const refs={};
  chaps.forEach(({ch})=>ch.secs.forEach(sec=>{if(!secInc(sec))return;if(sec.gas&&S.gasNone)return;secEls(sec).forEach(name=>{const id=elId(sec.id,name);const e=S.el[id];if(e&&e.oc&&e.oc!=="nd"&&e.find&&e.find.trim()){k++;const no=`${findNum}.${k}`;refs[id]=no;findings.push({no,el:name,sec:sec.name,find:e.find,zal:e.zal,pil:e.pil,id,photos:e.photos||[]})}})}));
  S.extra.forEach((x,i)=>{if((x.find||"").trim()){k++;findings.push({no:`${findNum}.${k}`,el:x.gdzie||"",find:x.find,zal:x.zal,pil:+x.pil||0,extra:i,photos:x.photos||[]})}});
  return {chaps,findNum,findings,refs,metNum:findNum+1,conNum:findNum+2,terNum:findNum+3};
}

/* ============================================================
   NAWIGACJA
   ============================================================ */
const NAV=[
 {id:"A",k:"A",name:"Dane obiektu i kontroli",sub:"rodzaj, zakres, osoby"},
 {id:"B",k:"B",name:"Opis techniczny",sub:"parametry, konstrukcja, instalacje"},
 {id:"C",k:"C",name:"Poprzednie kontrole",sub:"art. 62 ust. 1a"},
 {sep:"Ocena elementów"},
 ...CH.map(c=>({id:c.id,k:c.id,name:c.name,sub:c.law,ch:c})),
 {sep:"Wyniki"},
 {id:"I",k:"I",name:"Nieprawidłowości",sub:"lista zbiorcza z terminami"},
 {id:"J",k:"J",name:"Wnioski i przydatność",sub:"ocena, eksploatacja, PINB"},
 {id:"K",k:"K",name:"Podpisy i załączniki",sub:"zdjęcia, dokumenty"},
 {id:"P",k:"▤",name:"Podgląd protokołu",sub:"wersja do druku"}
];
let cur="A";
try{const h=location.hash.slice(1);if(NAV.some(n=>n.id===h))cur=h}catch(e){}
function chStats(c){let tot=0,done=0,f=0;c.secs.forEach(s=>{if(!secInc(s))return;secEls(s).forEach(n=>{tot++;const e=S.el[elId(s.id,n)];if(e&&e.oc){done++;if(e.find&&e.oc!=="nd")f++}})});return{tot,done,f}}
function renderNav(){
  const st=structure();
  $("#nav").innerHTML=NAV.map(n=>{
    if(n.sep)return`<div class="navsep">${esc(n.sep)}</div>`;
    let cnt="";
    if(n.ch){const s=chStats(n.ch);cnt=`<span class="cnt">${s.done}/${s.tot}${s.f?` · <span class="f">${s.f}!</span>`:""}</span>`}
    if(n.id==="I")cnt=`<span class="cnt">${st.findings.length?`<span class="f">${st.findings.length}</span>`:"0"}</span>`;
    return`<button type="button" class="cat${cur===n.id?" on":""}" data-nav="${n.id}"><span class="k">${esc(n.k)}</span><span class="t">${esc(n.name)}<small>${esc(n.sub)}</small></span>${cnt}</button>`}).join("");
  $("#hdrTitle").textContent=S.meta.nr?`Protokół nr ${S.meta.nr}`:"Nowy protokół";
}
function refreshCounts(){renderNav();renderMbar()}
function renderMbar(){const sel=document.getElementById("mSel");if(!sel)return;const st=structure();const ids=NAV.filter(x=>x.id);
  sel.innerHTML=ids.map(n=>{let c="";if(n.ch){const s=chStats(n.ch);c=` (${s.done}/${s.tot}${s.f?", usterki: "+s.f:""})`}if(n.id==="I")c=` (${st.findings.length})`;return`<option value="${n.id}"${n.id===cur?" selected":""}>${esc(n.k==="▤"?"":n.k+". ")}${esc(n.name)}${esc(c)}</option>`}).join("");
  const i=ids.findIndex(x=>x.id===cur);document.getElementById("mPrev").disabled=i<=0;document.getElementById("mNext").disabled=i>=ids.length-1}
$("#nav").addEventListener("click",e=>{const b=e.target.closest("[data-nav]");if(!b)return;go(b.dataset.nav)});
function go(id){cur=id;try{history.replaceState(null,"","#"+id)}catch(e){}render();window.scrollTo({top:0});const on=$("#nav .on");if(on&&on.scrollIntoView)on.scrollIntoView({block:"nearest",inline:"center"})}

/* ============================================================
   WIDOKI
   ============================================================ */
function F(path,label,opt={}){ // pole tekstowe
  const v=getPath(path);const cls=opt.cls?` ${opt.cls}`:"";const id="f_"+path.replace(/[^a-z0-9]/gi,"_");
  const list=opt.list?` list="${opt.list}"`:"";
  let inp;
  if(opt.area)inp=`<textarea id="${id}" data-b="${path}" placeholder="${esc(opt.ph||"")}">${esc(v)}</textarea>`;
  else inp=`<input id="${id}" type="${opt.type||"text"}" data-b="${path}" value="${esc(v)}" placeholder="${esc(opt.ph||"")}"${list}${opt.type==="number"?' inputmode="decimal"':""}>`;
  return`<div class="fld${cls}"><label for="${id}">${esc(label)}</label>${inp}${opt.after||""}</div>`;
}
function C(path,label){const v=!!getPath(path);const id="c_"+path.replace(/[^a-z0-9]/gi,"_");return`<label class="chk" for="${id}"><input id="${id}" type="checkbox" data-b="${path}"${v?" checked":""}><span>${label}</span></label>`}
function getPath(p){return p.split(".").reduce((o,k)=>o==null?undefined:o[k],S)??""}
function setPath(p,v){const ks=p.split(".");let o=S;for(let i=0;i<ks.length-1;i++){if(o[ks[i]]==null)o[ks[i]]={};o=o[ks[i]]}o[ks[ks.length-1]]=v}
function datalists(){return`<datalist id="dl-zal">${ZAL_SUG.map(z=>`<option value="${esc(z)}">`).join("")}</datalist><datalist id="dl-fun"><option value="Budynek mieszkalny wielorodzinny"><option value="Biurowy / usługowy"><option value="Handlowo-usługowy"><option value="Hala produkcyjno-magazynowa"><option value="Budynek użyteczności publicznej"><option value="Budynek gospodarczy"></datalist>`}

function vA(){
  const m=S.meta;
  const rodz=[["roczna","Roczna","art. 62 ust. 1 pkt 1"],["polroczna","Półroczna (2× w roku)","art. 62 ust. 1 pkt 3"],["piecio","Pięcioletnia","art. 62 ust. 1 pkt 2"],["dorazna","Doraźna","art. 62 ust. 1 pkt 4"]];
  let warn="";
  if(needsHalfYear()&&!m.rodzaj.polroczna)warn=`<div class="alert amb">Powierzchnia zabudowy powyżej 2000 m² lub dachu powyżej 1000 m² – obiekt podlega kontroli dwa razy w roku, w terminach do 31 maja i do 30 listopada (art. 62 ust. 1 pkt 3).</div>`;
  if(!needsHalfYear()&&(m.pZab||m.pDach))warn=`<div class="alert blue">Powierzchnia zabudowy nie przekracza 2000 m², a dachu 1000 m² – wystarczy kontrola roczna.</div>`;
  return`<div class="phead"><h1>Dane obiektu i kontroli</h1><span class="law">art. 62a ust. 2 pkt 1–5</span></div>
  <div class="card"><h2>Protokół</h2><div class="grid">
   ${F("meta.nr","Numer protokołu",{ph:"np. 2026/10/1/Miejscowość"})}
   ${F("meta.data","Data przeprowadzenia kontroli",{type:"date"})}
   ${F("meta.dataOpr","Data opracowania protokołu",{type:"date"})}
  </div></div>
  <div class="card"><h2>Rodzaj kontroli</h2><div class="hint">Można zaznaczyć kilka – np. kontrola pięcioletnia obejmuje też zakres roczny.</div>
   <div class="chips">${rodz.map(([k,l,a])=>`<button type="button" class="chipc${m.rodzaj[k]?" on":""}" data-rodz="${k}" title="${a}">${l}</button>`).join("")}</div>
   ${m.rodzaj.dorazna?`<div class="grid" style="margin-top:10px">${F("meta.dorPowod","Okoliczność kontroli doraźnej (art. 61 pkt 2)",{cls:"full",ph:"np. silny wiatr w dniu …, intensywne opady śniegu",list:"dl-dor"})}</div><datalist id="dl-dor"><option value="Silne wiatry"><option value="Intensywne opady atmosferyczne"><option value="Wyładowania atmosferyczne"><option value="Wstrząsy sejsmiczne"><option value="Powódź / pożar"></datalist>`:""}
   ${warn}
   <div class="lbl" style="margin-top:14px">Zakres kontroli rocznej</div>
   <div style="display:grid;gap:6px;margin-top:6px">
    ${C("meta.zakres.a","Elementy budynku, budowli i instalacji narażone na szkodliwe wpływy atmosferyczne i niszczące działania czynników występujących podczas użytkowania obiektu")}
    ${C("meta.zakres.b","Instalacje i urządzenia służące ochronie środowiska")}
    ${C("meta.zakres.c","Instalacje gazowe oraz przewody kominowe")}
   </div></div>
  <div class="card"><h2>Obiekt</h2><div class="grid">
   ${F("meta.nazwa","Nazwa obiektu budowlanego",{cls:"w2"})}
   ${F("meta.funkcja","Funkcja / sposób użytkowania",{list:"dl-fun"})}
   ${F("meta.ulica","Ulica, nr")}${F("meta.kod","Kod pocztowy")}${F("meta.miejscowosc","Miejscowość")}${F("meta.woj","Województwo")}
   ${F("meta.dzialka","Nr działki ewidencyjnej, obręb",{ph:"np. 123/4, obr. 0012"})}
   ${F("meta.kob","Nr książki obiektu (c-KOB)",{ph:"opcjonalnie"})}
  </div></div>
  <div class="card"><h2>Właściciel lub zarządca</h2><div class="grid">
   ${F("meta.wlasciciel","Nazwa / imię i nazwisko",{cls:"w2"})}
   ${F("meta.wlAdres","Adres właściciela lub zarządcy")}
   ${F("meta.uczestnicy","Osoby obecne przy kontroli ze strony właściciela",{cls:"full",ph:"imię, nazwisko, funkcja"})}
  </div></div>
  <div class="card"><h2>Osoby dokonujące kontroli</h2><div class="hint">Dane trafiają do nagłówka protokołu i do podpisów – wpisujesz je tylko raz.</div>
   ${S.osoby.map((o,i)=>`<div class="grid" style="border-top:${i?"1px solid var(--line)":"0"};padding-top:${i?"12px":"0"};margin-top:${i?"12px":"0"}">
     ${F(`osoby.${i}.imie`,"Imię i nazwisko")}
     ${F(`osoby.${i}.nr`,"Nr uprawnień budowlanych")}
     ${F(`osoby.${i}.izba`,"Nr członkowski izby (opcjonalnie)")}
     <div class="fld"><label for="rola${i}">Podpisuje w zakresie</label><select id="rola${i}" data-b="osoby.${i}.rola">${ROLES.map(([k,l])=>`<option value="${k}"${o.rola===k?" selected":""}>${esc(l)}</option>`).join("")}</select></div>
     ${F(`osoby.${i}.upr`,"Zakres uprawnień",{cls:"full",list:"dl-upr"})}
     <div class="fld full" style="align-items:flex-end">${S.osoby.length>1?`<button type="button" class="btn ghost sm" data-delos="${i}">Usuń osobę</button>`:""}</div>
   </div>`).join("")}
   <datalist id="dl-upr"><option value="Uprawnienia budowlane do kierowania robotami budowlanymi bez ograniczeń w specjalności konstrukcyjno-budowlanej"><option value="Uprawnienia budowlane do projektowania i kierowania robotami budowlanymi bez ograniczeń w specjalności konstrukcyjno-budowlanej"><option value="Uprawnienia budowlane bez ograniczeń w specjalności instalacyjnej w zakresie sieci, instalacji i urządzeń cieplnych, wentylacyjnych, gazowych, wodociągowych i kanalizacyjnych"><option value="Uprawnienia budowlane bez ograniczeń w specjalności instalacyjnej w zakresie sieci, instalacji i urządzeń elektrycznych i elektroenergetycznych"><option value="Mistrz w zawodzie kominiarz"></datalist>
   <div class="addrow"><button type="button" class="btn sm" data-addos>+ Dodaj osobę</button></div>
  </div>
  <div class="card"><h2>Warunki i metody kontroli</h2><div class="grid">
   ${F("meta.pogoda","Warunki atmosferyczne",{list:"dl-pog"})}${F("meta.temp","Temperatura powietrza [°C]",{type:"number"})}
  </div><datalist id="dl-pog"><option value="Słonecznie, bez opadów"><option value="Pochmurno, bez opadów"><option value="Opady deszczu"><option value="Pokrywa śnieżna na dachu"></datalist>
   <div class="lbl" style="margin-top:12px">Metody</div>
   <div style="display:grid;gap:6px;margin-top:6px;grid-template-columns:repeat(auto-fill,minmax(230px,1fr))">
    ${C("meta.metodyK.ogl","Oględziny (ocena wizualna)")}${C("meta.metodyK.dok","Analiza dokumentacji")}${C("meta.metodyK.pom","Pomiary i badania")}${C("meta.metodyK.foto","Dokumentacja fotograficzna")}
   </div>
   <div class="grid" style="margin-top:12px">${F("meta.ograniczenia","Elementy niedostępne / wyłączone z kontroli",{cls:"full",area:true,ph:"np. dach nieobjęty oględzinami z powodu oblodzenia; pomieszczenia najemcy zamknięte"})}</div>
  </div>
  <div class="card"><h2>Zdjęcie na stronę tytułową</h2>
   <input type="file" accept="image/*" id="coverIn" data-cover>
   ${S.meta.cover?`<img class="cover" src="${S.meta.cover}" alt="Zdjęcie obiektu"><button type="button" class="btn ghost sm" data-delcover>Usuń zdjęcie</button>`:""}
  </div>`;
}

function vB(){
  const m=S.meta;
  return`<div class="phead"><h1>Opis techniczny obiektu</h1><span class="law">rozdział 2 protokołu</span></div>
  <div class="card"><h2>Parametry obiektu</h2><div class="grid">
   ${F("meta.rok","Rok zakończenia budowy")}${F("meta.pZab","Powierzchnia zabudowy [m²]",{type:"number"})}${F("meta.pDach","Powierzchnia dachu [m²]",{type:"number"})}
   ${F("meta.pCalk","Powierzchnia całkowita [m²]",{type:"number"})}${F("meta.pUzyt","Powierzchnia użytkowa [m²]",{type:"number"})}${F("meta.kub","Kubatura [m³]",{type:"number"})}
   ${F("meta.kPodz","Kondygnacje podziemne")}${F("meta.kNad","Kondygnacje nadziemne")}
  </div></div>
  <div class="card"><h2>Konstrukcja i wykończenie</h2><div class="hint">Wybierz z listy albo wpisz własny opis.</div><div class="grid">
   ${OPIS.map(([k,l,sug])=>F("opis."+k,l,{list:"dl-op-"+k})+`<datalist id="dl-op-${k}">${sug.map(x=>`<option value="${esc(x)}">`).join("")}</datalist>`).join("")}
  </div></div>
  <div class="card"><h2>Podstawowe instalacje w obiekcie</h2><div class="hint">Instalacje oznaczone „NIE” możesz potem pominąć w ocenie.</div>
   <div class="inst">${INST.concat(Object.keys(S.inst).filter(k=>!INST.includes(k))).map(k=>{const v=S.inst[k]||"";return`<div class="it"><span>${esc(k)}</span><span class="yn"><button type="button" data-inst="${esc(k)}" data-v="T" class="${v==="T"?"on":""}">TAK</button><button type="button" data-inst="${esc(k)}" data-v="N" class="${v==="N"?"on":""}">NIE</button></span></div>`}).join("")}</div>
   <div class="addrow"><input type="text" id="instNew" placeholder="Inna instalacja…"><button type="button" class="btn sm" data-addinst>+ Dodaj</button></div>
  </div>`;
}

function vC(){
  const st={tak:"Wykonano",czesc:"Wykonano częściowo",nie:"Nie wykonano",stale:"Zalecenie stałe"};
  return`<div class="phead"><h1>Sprawdzenie zaleceń z poprzednich kontroli</h1><span class="law">art. 62 ust. 1a · art. 62a ust. 2 pkt 9</span></div>
  <div class="card"><h2>Dokumenty, z którymi się zapoznano</h2><div class="grid">
   ${F("docs.poprz","Protokoły z poprzednich kontroli",{cls:"full",area:true})}</div>
   <div style="display:grid;gap:6px;margin-top:10px;grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
    ${C("docs.kob","Książka obiektu budowlanego (KOB / c-KOB)")}${C("docs.dokt","Dokumentacja techniczna / powykonawcza")}${C("docs.pomEl","Protokoły pomiarów elektrycznych")}${C("docs.kom","E-protokół z kontroli przewodów kominowych")}${C("docs.hydr","Protokół z przeglądu hydrantów")}${C("docs.ppoz","Protokoły przeglądów urządzeń ppoż.")}
   </div>
   <div class="grid" style="margin-top:10px">${F("docs.inne","Inne dokumenty",{cls:"full"})}</div>
  </div>
  <div class="card"><h2>Zalecenia z poprzedniej kontroli</h2>
   <div class="tw"><table class="t"><thead><tr><th style="min-width:130px">Element</th><th style="min-width:180px">Zalecenie</th><th style="min-width:150px">Stopień wykonania</th><th style="min-width:150px">Uwagi</th><th></th></tr></thead><tbody>
   ${S.prev.map((p,i)=>`<tr><td><input type="text" data-b="prev.${i}.el" value="${esc(p.el)}" aria-label="Element"></td><td><textarea data-b="prev.${i}.zal" aria-label="Zalecenie" style="min-height:40px">${esc(p.zal)}</textarea></td><td><select data-b="prev.${i}.st" aria-label="Stopień wykonania"><option value=""></option>${Object.entries(st).map(([k,l])=>`<option value="${k}"${p.st===k?" selected":""}>${l}</option>`).join("")}</select></td><td><input type="text" data-b="prev.${i}.uw" value="${esc(p.uw)}" aria-label="Uwagi"></td><td><button type="button" class="btn ghost sm" data-delprev="${i}" aria-label="Usuń">✕</button></td></tr>`).join("")}
   </tbody></table></div>
   <div class="addrow"><button type="button" class="btn sm" data-addprev>+ Dodaj zalecenie</button></div>
   ${S.prev.length?`<div class="alert blue">${esc(prevSummary())}</div>`:`<div class="hint">Brak zaleceń – np. pierwsza kontrola. Po wczytaniu poprzedniego protokołu użyj „Więcej → Następna kontrola na podstawie tej”.</div>`}
  </div>`;
}
function prevSummary(){const a=S.prev.filter(p=>p.st&&p.st!=="stale");if(!S.prev.length)return"Nie dotyczy – brak zaleceń z poprzedniej kontroli.";if(!a.length)return"Zalecenia z poprzedniej kontroli mają charakter stały i należy je nadal przestrzegać.";if(a.every(p=>p.st==="tak"))return"Zalecenia uwzględnione w poprzednim protokole kontroli zostały wykonane.";if(a.every(p=>p.st==="nie"))return"Zalecenia uwzględnione w poprzednim protokole kontroli nie zostały wykonane – zakres niewykonanych zaleceń podano w tabeli.";return"Zalecenia uwzględnione w poprzednim protokole kontroli zostały wykonane częściowo – zakres niewykonanych zaleceń podano w tabeli."}

function vCh(ch){
  const st=structure();const chap=st.chaps.find(x=>x.ch===ch);
  let off="";
  if(!chIncluded(ch))off=`<div class="alert amb">Ta kategoria nie trafi do protokołu – ${ch.id==="D"||ch.id==="E"||ch.id==="F"?"odznaczono ją w zakresie kontroli (zakładka A) albo ":""}wyłączono wszystkie jej sekcje.</div>`;
  let extra="";
  if(ch.id==="G")extra=`<div class="card"><h2>Pomiary</h2><div class="hint">Badanie instalacji elektrycznej i piorunochronnej (stan połączeń, osprzętu, zabezpieczeń, ochrona przeciwporażeniowa, rezystancja izolacji, uziemienia) jest obowiązkowe co najmniej raz na 5 lat.</div><div class="grid">${F("elec.dataEl","Data ostatnich pomiarów instalacji elektrycznej",{type:"date"})}${F("elec.nrEl","Nr protokołu pomiarów")}${F("elec.dataOdg","Data ostatnich pomiarów instalacji odgromowej",{type:"date"})}${F("meta.nast5","Termin następnej kontroli 5-letniej",{type:"date"})}</div>${oldMeasure()}</div>`;
  return`<div class="phead"><h1>${esc(ch.name)}</h1><span class="law">${esc(ch.law)}${chap?` · rozdział ${chap.num}`:""}</span></div>${off}${extra}
  ${ch.secs.map((sec,si)=>vSec(sec,chap?`${chap.num}.${si+1}`:"",st)).join("")}`;
}
function oldMeasure(){const d=S.elec.dataEl,k=S.meta.data;if(!d||!k)return"";const lim=addMonths(d,60);if(lim<k)return`<div class="alert red">Pomiary instalacji elektrycznej są starsze niż 5 lat (ważne do ${fmtD(lim)}). Dodaj zalecenie przy „Pomiary instalacji elektrycznej”.</div>`;return`<div class="alert blue">Pomiary ważne do ${fmtD(lim)}.</div>`}
function vSec(sec,num,st){
  const so=secObj(sec.id);const inc=secInc(sec);
  let top="";
  if(sec.gas)top=`<div style="margin:8px 0">${C("gasNone","Obiekt nie jest wyposażony w instalację gazową")}</div>`;
  if(sec.chim)top=`<div class="alert blue" style="margin-bottom:10px">Protokół z kontroli przewodów kominowych sporządza się w formie elektronicznej (e-protokół) w systemie centralnej ewidencji emisyjności budynków (art. 62a ust. 5). Poniższa ocena jest odniesieniem do e-protokołu.</div><div class="grid" style="margin-bottom:8px">${F("chim.nr","Nr e-protokołu")}${F("chim.data","Data kontroli kominiarskiej",{type:"date"})}${F("chim.kto","Wykonawca (mistrz kominiarski / osoba uprawniona)")}</div>`;
  const hideEls=sec.gas&&S.gasNone;
  return`<section class="card" id="sec-${sec.id}"><div class="sec-top"><h2><span class="n">${esc(num)}</span>${esc(sec.name)}</h2>
   <label class="chk"><input type="checkbox" data-secinc="${sec.id}"${inc?" checked":""}><span>W protokole</span></label></div>
   ${inc?`${top}${hideEls?"":`<div class="fld" style="margin:6px 0 4px"><label for="op_${sec.id}">Opis</label><input type="text" id="op_${sec.id}" data-b="sec.${sec.id}.opis" value="${esc(so.opis||"")}" placeholder="Krótki opis konstrukcji lub instalacji"></div>
   <div class="hint">Elementy bez oceny nie trafiają do protokołu. Opis nieprawidłowości automatycznie trafia do zbiorczej listy z numerem punktu.</div>
   ${secEls(sec).map(n=>vEl(sec,n,st)).join("")}
   <div class="addrow"><input type="text" id="new_${sec.id}" placeholder="Dodaj własny element…"><button type="button" class="btn sm" data-addel="${sec.id}">+ Dodaj</button></div>`}`:""}
  </section>`;
}
function phArr(key){if(key.startsWith("el:")){const e=getEl(key.slice(3));return e.photos||(e.photos=[])}const x=S.extra[+key.slice(3)];if(!x)return[];return x.photos||(x.photos=[])}
function photoBox(key,arr,lbl){arr=arr||[];return`<div class="fph"><div class="lbl">${esc(lbl||"Zdjęcia nieprawidłowości")} <span style="opacity:.75">– opcjonalnie, można opisać bez zdjęcia</span></div>
 ${arr.length?`<div class="fph-list">${arr.map((p,i)=>`<div class="fph-it"><img src="${p.src}" alt="Zdjęcie ${i+1}"><button type="button" class="fph-del" data-delfph="${esc(key)}|${i}" aria-label="Usuń zdjęcie ${i+1}">✕</button></div>`).join("")}</div>`:""}
 <div class="fph-btns"><label class="btn sm">Zrób zdjęcie<input class="vh" type="file" accept="image/*" capture="environment" data-fph="${esc(key)}"></label><label class="btn sm">Dodaj z galerii<input class="vh" type="file" accept="image/*" multiple data-fph="${esc(key)}"></label></div></div>`}
function vEl(sec,name,st){
  const id=elId(sec.id,name);const e=S.el[id]||{};const open=!!(e.find||e.zal||(e.photos&&e.photos.length)||(e.oc&&e.oc!=="dobra"&&e.oc!=="nd"));
  const sug=(FIND[name]||[]).concat(FIND_GEN);
  const custom=(S.custom[sec.id]||[]).includes(name);
  const ref=st.refs[id];
  return`<div class="el" data-el="${esc(id)}">
   <div class="el-row"><div class="el-name">${esc(name)}${ref?`<span class="ref">pkt ${ref}</span>`:""}${custom?`<button type="button" class="btn ghost sm" data-delel="${esc(id)}" aria-label="Usuń element">✕</button>`:""}</div>
    <div class="rates">${RATES.map(([k,l])=>`<button type="button" class="rt${e.oc===k?" on":""}" data-rate="${k}" data-v="${k}">${l}</button>`).join("")}</div></div>
   <button type="button" class="tog" data-tog>${open?"Ukryj szczegóły":"+ Nieprawidłowość / zalecenie"}</button>
   <div class="el-more"${open?"":" hidden"}>
    <div class="fld sug"><label>Typowe usterki – wybór wypełnia pola</label><select data-sug><option value="">Wybierz…</option>${sug.map((s,i)=>`<option value="${i}">${esc(s[0])}</option>`).join("")}</select></div>
    <div class="fld"><label>Stwierdzona nieprawidłowość</label><textarea data-ef="find" placeholder="Puste = brak nieprawidłowości">${esc(e.find||"")}</textarea></div>
    <div class="fld"><label>Zalecenie / uwagi</label><textarea data-ef="zal" list="dl-zal">${esc(e.zal||"")}</textarea></div>
    <div class="fld"><label>Pilność</label><div class="pil">${[1,2,3,4,5].map(p=>`<button type="button" data-p="${p}" class="${e.pil===p?"on":""}" title="${PIL[p-1][1]}">${p}°</button>`).join("")}</div></div>
    ${photoBox("el:"+id,e.photos)}
   </div></div>`;
}

function vI(){
  const st=structure();
  return`<div class="phead"><h1>Nieprawidłowości stwierdzone w trakcie kontroli</h1><span class="law">art. 62a ust. 2 pkt 6–7, ust. 3 · rozdział ${st.findNum}</span></div>
  <div class="card"><h2>Lista zbiorcza</h2><div class="hint">Lista buduje się sama z ocen elementów. Termin wykonania wynika z pilności i daty kontroli (art. 62a ust. 3 wymaga terminu).</div>
   ${st.findings.filter(f=>f.id).length?st.findings.filter(f=>f.id).map(f=>`<div class="fi">
     <div class="fi-h"><span class="fi-no">${f.no}</span><b>${esc(f.el)}</b><span class="fi-p ${f.pil===1?"p1":""}">${f.pil?f.pil+"° · "+esc(deadline(f.pil)):"bez pilności"}</span></div>
     <div class="fi-t">${esc(f.find)}</div>${f.zal?`<div class="fi-z">Zalecenie: ${esc(f.zal)}</div>`:""}
     ${photoBox("el:"+f.id,f.photos)}
     <button type="button" class="tog" data-goel="${esc(f.id)}">Edytuj opis w kategorii →</button></div>`).join(""):`<div class="hint">Brak nieprawidłowości przy ocenianych elementach. Opisz je przy elemencie w kategoriach D–H albo dodaj poniżej.</div>`}
   <div class="stat">${[1,2,3,4,5].map(p=>`<span>${p}°: <b>${st.findings.filter(f=>f.pil===p).length}</b></span>`).join("")}<span>bez pilności: <b>${st.findings.filter(f=>!f.pil).length}</b></span></div>
  </div>
  <div class="card"><h2>Nieprawidłowości spoza listy elementów</h2>
   ${S.extra.map((x,i)=>`<div class="grid" style="border-top:${i?"1px solid var(--line)":"0"};padding-top:${i?"10px":"0"};margin-top:${i?"10px":"0"}">${F(`extra.${i}.gdzie`,"Element / miejsce")}${F(`extra.${i}.find`,"Nieprawidłowość",{cls:"w2"})}${F(`extra.${i}.zal`,"Zalecenie",{cls:"w2",list:"dl-zal"})}<div class="fld"><label for="xp${i}">Pilność</label><select id="xp${i}" data-b="extra.${i}.pil"><option value="0">—</option>${[1,2,3,4,5].map(p=>`<option value="${p}"${+x.pil===p?" selected":""}>${p}° – ${PIL[p-1][1]}</option>`).join("")}</select></div><div class="fld full">${photoBox("ex:"+i,x.photos)}</div><div class="fld" style="justify-content:flex-end"><button type="button" class="btn ghost sm" data-delextra="${i}">Usuń nieprawidłowość</button></div></div>`).join("")}
   <div class="addrow"><button type="button" class="btn sm" data-addextra>+ Dodaj nieprawidłowość</button></div>
  </div>
  <div class="card"><h2>Stopnie pilności</h2><div class="tw"><table class="t"><tbody>${PIL.map(p=>`<tr><td class="num">${p[0]}°</td><td><b style="font-weight:500">${p[1]}</b><div class="hint" style="margin:2px 0 0">${esc(p[2])}</div></td></tr>`).join("")}</tbody></table></div></div>`;
}

function worst(){let w=0;Object.values(S.el).forEach(e=>{if(e&&RATE_ORDER[e.oc])w=Math.max(w,RATE_ORDER[e.oc])});return w}
function vJ(){
  const st=structure();const p1=st.findings.filter(f=>f.pil===1);const c=S.concl;const w=worst();
  const sugO=["","dobra","zadow","dost","zla"][w]||"";
  const sugP=p1.length?"warunek":(st.findings.length?"warunek":"tak");
  return`<div class="phead"><h1>Wnioski i przydatność do użytkowania</h1><span class="law">art. 62a ust. 2 pkt 8 · art. 70</span></div>
  <div class="card"><h2>Metody i środki użytkowania elementów narażonych na szkodliwe wpływy</h2><div class="hint">Obowiązkowy element protokołu (art. 62a ust. 2 pkt 8) – nie było go w dotychczasowym wzorze.</div>
   <div style="display:grid;gap:8px">${METODY.map(([k,t])=>C("metody."+k,esc(t))).join("")}</div>
   <div class="grid" style="margin-top:10px">${F("metodyInne","Inne zalecenia eksploatacyjne",{cls:"full",area:true})}</div></div>
  <div class="card"><h2>Ogólna ocena stanu technicznego</h2>
   <div class="chips">${OGOLNA.map(([k,l])=>`<button type="button" class="chipc${c.ogolna===k?" on":""}" data-ogol="${k}">${l}</button>`).join("")}</div>
   ${sugO&&!c.ogolna?`<div class="hint" style="margin-top:8px">Najniższa ocena elementu: ${RATE_LBL[sugO]}.</div>`:""}</div>
  <div class="card"><h2>Czy obiekt nadaje się do eksploatacji?</h2>
   <div style="display:grid;gap:8px">${PRZYD.map(([k,t])=>`<label class="chk"><input type="radio" name="przyd" data-przyd="${k}"${c.przyd===k?" checked":""}><span>${esc(t)}</span></label>`).join("")}</div>
   ${c.przyd==="czesc"?`<div class="grid" style="margin-top:10px">${F("concl.czesc","Części / pomieszczenia wyłączone z użytkowania",{cls:"full"})}</div>`:""}
   ${!c.przyd?`<div class="hint" style="margin-top:8px">Podpowiedź na podstawie listy: „${esc(PRZYD.find(x=>x[0]===sugP)[1])}”</div>`:""}
   <div class="grid" style="margin-top:10px">${F("concl.uwagi","Uwagi końcowe",{cls:"full",area:true})}</div></div>
  <div class="card"><h2>Zawiadomienie organu nadzoru budowlanego</h2>
   ${p1.length?`<div class="alert red">Stwierdzono ${p1.length} ${p1.length===1?"nieprawidłowość":"nieprawidłowości"} o pilności 1° (pkt ${p1.map(f=>f.no).join(", ")}). Zgodnie z art. 70 ust. 1–2 właściciel lub zarządca usuwa je w czasie lub bezpośrednio po kontroli, a kontrolujący bezzwłocznie przesyła kopię protokołu do właściwego organu.</div>`:`<div class="hint">Brak nieprawidłowości 1° – zawiadomienie organu nie jest wymagane.</div>`}
   <div class="grid" style="margin-top:10px">${F("concl.pinb","Właściwy organ",{cls:"w2",ph:"Powiatowy Inspektorat Nadzoru Budowlanego w …"})}${F("concl.pinbData","Data przesłania kopii",{type:"date"})}</div>
   <div style="margin-top:8px">${C("concl.pinbSent","Kopię protokołu przesłano do organu")}</div></div>
  <div class="card"><h2>Terminy kolejnych kontroli</h2><div class="grid">
   ${F("meta.nastepna","Następna kontrola okresowa (puste = wyliczona)",{type:"date",after:`<span class="hint" style="margin:0">Wyliczono: ${esc(fmtD(nextControl())||"—")}</span>`})}
   ${F("meta.nast5","Następna kontrola 5-letnia",{type:"date"})}</div></div>`;
}

function vK(){
  return`<div class="phead"><h1>Podpisy, załączniki i dokumentacja</h1><span class="law">art. 62a ust. 2 pkt 2, ust. 4–4a</span></div>
  <div class="card"><h2>Podpisy</h2><div class="hint">Bloki podpisów tworzą się z listy osób w zakładce A.</div>
   <div class="tw"><table class="t"><tbody>${S.osoby.map(o=>`<tr><td>${esc((ROLES.find(r=>r[0]===o.rola)||["",""])[1])}</td><td>${esc(o.imie)||"<i>brak</i>"}</td><td class="num">${esc(o.nr)}</td></tr>`).join("")}</tbody></table></div>
   <div class="addrow"><button type="button" class="btn sm" data-nav2="A">Edytuj osoby</button></div></div>
  <div class="card"><h2>Załączniki</h2>
   ${C("zal.crub","Osoby kontrolujące są wpisane do centralnego rejestru osób posiadających uprawnienia budowlane – kopie decyzji i zaświadczeń nie są wymagane (art. 62a ust. 4a)")}
   <div class="hint" style="margin-top:8px">Lista automatyczna: ${esc(attachments().join("; ")||"brak")}.</div>
   <div class="grid">${F("zal.inne","Inne załączniki (każdy w osobnej linii)",{cls:"full",area:true,ph:"np. Protokół pomiarów elektrycznych nr …"})}</div></div>
  <div class="card"><h2>Dokumentacja fotograficzna</h2><div class="hint">Zdjęcia są pomniejszane do rozmiaru dokumentu. Możesz je zrobić telefonem.</div>
   <input type="file" accept="image/*" multiple id="phIn" data-photos>
   <div class="photos" style="margin-top:10px">${S.photos.map((p,i)=>`<div class="ph"><img src="${p.src}" alt="Fot. ${i+1}"><div class="pc"><span class="num" style="font-family:var(--mono);font-size:12px">${i+1}.</span><input type="text" data-b="photos.${i}.opis" value="${esc(p.opis)}" placeholder="Opis / pkt" aria-label="Opis zdjęcia ${i+1}"><button type="button" class="btn ghost sm" data-delph="${i}" aria-label="Usuń zdjęcie">✕</button></div></div>`).join("")}</div></div>`;
}
function attachments(){
  const out=[];if(!S.zal.crub){const br={bud:"konstrukcyjno-budowlana",san:"instalacyjna sanitarna",gaz:"instalacyjna gazowa",el:"instalacyjna elektryczna",kom:"kominiarska"};
   const seen=new Set();S.osoby.forEach(o=>{if(!o.imie||seen.has(o.rola))return;seen.add(o.rola);if(o.rola==="kom")return;out.push(`Decyzja o nadaniu uprawnień budowlanych – branża ${br[o.rola]}`);out.push(`Zaświadczenie o przynależności do właściwej izby inżynierów budownictwa – branża ${br[o.rola]}`)})}
  (S.zal.inne||"").split("\n").map(x=>x.trim()).filter(Boolean).forEach(x=>out.push(x));
  if(S.photos.length)out.push(`Dokumentacja fotograficzna (${S.photos.length} fot.)`);
  return out;
}

function vP(){
  const standalone=!inFrame;
  return`<div class="phead"><h1>Podgląd protokołu</h1><span class="law">tak wygląda dokument do druku</span></div>
  <div class="card noprint"><div class="hint" style="margin:0">Pobierz → <b>Word (.docx)</b> daje dokument z nagłówkiem „KONTROLA OKRESOWA OBIEKTU BUDOWLANEGO” i stopką „strona X/Y”, jak w dotychczasowym wzorze. ${standalone?"Możesz też wydrukować bezpośrednio z przeglądarki.":"Z pliku Word zapiszesz też PDF."}</div></div>
  <div class="sheet-wrap printable"><div class="sheet">${protocolHTML(true)}</div></div>`;
}

/* ============================================================
   RENDER + ZDARZENIA
   ============================================================ */
function render(){
  renderNav();renderMbar();
  const n=NAV.find(x=>x.id===cur)||NAV[0];
  let h="";
  if(cur==="A")h=vA();else if(cur==="B")h=vB();else if(cur==="C")h=vC();else if(n.ch)h=vCh(n.ch);else if(cur==="I")h=vI();else if(cur==="J")h=vJ();else if(cur==="K")h=vK();else if(cur==="P")h=vP();
  const nav=NAV.filter(x=>x.id);const i=nav.findIndex(x=>x.id===cur);
  const prev=nav[i-1],next=nav[i+1];
  h+=`<div class="addrow noprint" style="justify-content:space-between">${prev?`<button type="button" class="btn" data-nav2="${prev.id}">← ${esc(prev.name)}</button>`:"<span></span>"}${next?`<button type="button" class="btn pri" data-nav2="${next.id}">${esc(next.name)} →</button>`:""}</div>`;
  $("#main").innerHTML=datalists()+h;
}
const main=$("#main");
main.addEventListener("input",e=>{
  const t=e.target;
  if(t.dataset.b){let v=t.type==="checkbox"?t.checked:t.value;setPath(t.dataset.b,v);save();
    if(t.type==="checkbox"&&(t.dataset.b==="gasNone"||t.dataset.b.startsWith("meta.zakres")))render();
    if(t.dataset.b==="meta.nr")renderNav();
    if(t.dataset.b.startsWith("extra.")&&t.tagName==="SELECT")save();
    return}
  if(t.dataset.ef){const box=t.closest("[data-el]");const e2=getEl(box.dataset.el);e2[t.dataset.ef]=t.value;save();updRef(box);return}
});
main.addEventListener("change",e=>{
  const t=e.target;
  if(t.dataset.b&&(t.type==="checkbox"||t.tagName==="SELECT")){if(t.dataset.b.startsWith("meta.zakres")||t.dataset.b==="gasNone"||t.dataset.b.startsWith("zal.")||t.dataset.b.startsWith("elec.")||t.dataset.b==="meta.data")render();return}
  if(t.dataset.b==="meta.pZab"||t.dataset.b==="meta.pDach"||t.dataset.b==="meta.data"||t.dataset.b==="meta.nastepna"||t.dataset.b==="elec.dataEl"){render();return}
  if(t.dataset.secinc){secObj(t.dataset.secinc).inc=t.checked;save();render();return}
  if(t.dataset.przyd){S.concl.przyd=t.dataset.przyd;save();render();return}
  if(t.dataset.sug!==undefined){const box=t.closest("[data-el]");const id=box.dataset.el;const name=id.split("|").slice(1).join("|");const sug=(FIND[name]||[]).concat(FIND_GEN)[+t.value];if(!sug)return;const e2=getEl(id);e2.find=sug[0];e2.zal=sug[1];e2.pil=sug[2];if(!e2.oc||e2.oc==="dobra"||e2.oc==="nd")e2.oc=sug[2]<=2?"zla":"dost";save();rerenderEl(box);return}
  if(t.dataset.fph){const key=t.dataset.fph;const box=t.closest("[data-el]");Promise.all([...t.files].map(f=>readImg(f,1100))).then(a=>{const arr=phArr(key);a.forEach(src=>src&&arr.push({src}));save();if(box&&cur!=="I")rerenderEl(box);else render();toast(a.length===1?"Dodano zdjęcie":"Dodano zdjęcia: "+a.length)});return}
  if(t.dataset.cover!==undefined){readImg(t.files[0],1400).then(src=>{S.meta.cover=src;save();render()});return}
  if(t.dataset.photos!==undefined){Promise.all([...t.files].map(f=>readImg(f,1280))).then(a=>{a.forEach(src=>src&&S.photos.push({src,opis:""}));save();render()});return}
});
main.addEventListener("click",e=>{
  const t=e.target.closest("button");if(!t)return;
  const box=t.closest("[data-el]");
  if(t.dataset.rate&&box){const e2=getEl(box.dataset.el);e2.oc=e2.oc===t.dataset.rate?"":t.dataset.rate;save();rerenderEl(box);return}
  if(t.dataset.p&&box){const e2=getEl(box.dataset.el);const p=+t.dataset.p;e2.pil=e2.pil===p?0:p;save();rerenderEl(box);return}
  if(t.dataset.tog!==undefined&&box){const m=box.querySelector(".el-more");m.hidden=!m.hidden;t.textContent=m.hidden?"+ Nieprawidłowość / zalecenie":"Ukryj szczegóły";return}
  if(t.dataset.nav2){go(t.dataset.nav2);return}
  if(t.dataset.rodz){S.meta.rodzaj[t.dataset.rodz]=!S.meta.rodzaj[t.dataset.rodz];if(!Object.values(S.meta.rodzaj).some(Boolean))S.meta.rodzaj.roczna=true;save();render();return}
  if(t.dataset.inst){S.inst[t.dataset.inst]=S.inst[t.dataset.inst]===t.dataset.v?"":t.dataset.v;save();t.parentNode.querySelectorAll("button").forEach(b=>b.classList.toggle("on",S.inst[t.dataset.inst]===b.dataset.v));return}
  if(t.dataset.addinst!==undefined){const v=$("#instNew").value.trim();if(v){S.inst[v]="T";save();render()}return}
  if(t.dataset.addos!==undefined){S.osoby.push({imie:"",upr:"",nr:"",izba:"",rola:"san"});save();render();return}
  if(t.dataset.delos){S.osoby.splice(+t.dataset.delos,1);save();render();return}
  if(t.dataset.addprev!==undefined){S.prev.push({el:"",zal:"",st:"",uw:""});save();render();return}
  if(t.dataset.delprev){S.prev.splice(+t.dataset.delprev,1);save();render();return}
  if(t.dataset.addel){const inp=$("#new_"+t.dataset.addel);const v=inp.value.trim();if(!v)return;(S.custom[t.dataset.addel]||(S.custom[t.dataset.addel]=[])).push(v);save();render();setTimeout(()=>{const s=$("#sec-"+t.dataset.addel);s&&s.scrollIntoView({block:"end"})},0);return}
  if(t.dataset.delel){const [sid,...nm]=t.dataset.delel.split("|");const name=nm.join("|");S.custom[sid]=(S.custom[sid]||[]).filter(x=>x!==name);delete S.el[t.dataset.delel];save();render();return}
  if(t.dataset.addextra!==undefined){S.extra.push({gdzie:"",find:"",zal:"",pil:0,photos:[]});save();render();return}
  if(t.dataset.delextra){S.extra.splice(+t.dataset.delextra,1);save();render();return}
  if(t.dataset.ogol){S.concl.ogolna=S.concl.ogolna===t.dataset.ogol?"":t.dataset.ogol;save();render();return}
  if(t.dataset.delfph){const v=t.dataset.delfph;const k=v.lastIndexOf("|");const arr=phArr(v.slice(0,k));arr.splice(+v.slice(k+1),1);save();const box=t.closest("[data-el]");if(box&&cur!=="I")rerenderEl(box);else render();return}
  if(t.dataset.goel){const id=t.dataset.goel;const sec=ALLSECS.find(x=>x.id===id.split("|")[0]);go(sec.ch);setTimeout(()=>{const b=[...document.querySelectorAll("[data-el]")].find(x=>x.dataset.el===id);if(b){const m=b.querySelector(".el-more");m.hidden=false;b.querySelector("[data-tog]").textContent="Ukryj szczegóły";b.scrollIntoView({block:"center"})}},30);return}
  if(t.dataset.delph){S.photos.splice(+t.dataset.delph,1);save();render();return}
  if(t.dataset.delcover!==undefined){S.meta.cover="";save();render();return}
});
function rerenderEl(box){const id=box.dataset.el;const sid=id.split("|")[0];const sec=ALLSECS.find(s=>s.id===sid);const name=id.split("|").slice(1).join("|");const wasOpen=!box.querySelector(".el-more").hidden;const tmp=document.createElement("div");tmp.innerHTML=vEl(sec,name,structure());const nb=tmp.firstElementChild;if(wasOpen){nb.querySelector(".el-more").hidden=false;nb.querySelector("[data-tog]").textContent="Ukryj szczegóły"}box.replaceWith(nb);refreshAllRefs()}
function updRef(){refreshAllRefs()}
function refreshAllRefs(){const st=structure();document.querySelectorAll("[data-el]").forEach(b=>{const r=st.refs[b.dataset.el];let s=b.querySelector(".ref");if(r){if(!s){s=document.createElement("span");s.className="ref";b.querySelector(".el-name").insertBefore(s,b.querySelector(".el-name").children[0]||null)}s.textContent="pkt "+r}else if(s)s.remove()})}
function readImg(file,max){return new Promise(res=>{if(!file)return res("");const fr=new FileReader();fr.onload=()=>{const img=new Image();img.onload=()=>{const k=Math.min(1,max/Math.max(img.width,img.height));const c=document.createElement("canvas");c.width=Math.round(img.width*k);c.height=Math.round(img.height*k);c.getContext("2d").drawImage(img,0,0,c.width,c.height);res(c.toDataURL("image/jpeg",.78))};img.onerror=()=>res("");img.src=fr.result};fr.onerror=()=>res("");fr.readAsDataURL(file)})}

/* ============================================================
   DOKUMENT (styl oryginalnego protokołu)
   ============================================================ */
const DOC_CSS=`.pk{font-family:Arial,Helvetica,sans-serif;font-size:10pt;color:#000;line-height:1.3}
.pk .hdr{border:1px solid #000;text-align:center;font-family:'Times New Roman',serif;font-size:9pt;padding:2px;margin-bottom:18pt}
.pk h1{text-align:center;font-size:13pt;font-weight:bold;margin:24pt 0 18pt}
.pk h2{font-size:11pt;font-weight:bold;margin:16pt 0 6pt;text-transform:uppercase}
.pk h3{font-size:10pt;font-weight:bold;margin:10pt 0 3pt}
.pk p{margin:3pt 0}
.pk table{border-collapse:collapse;width:100%;margin:4pt 0 8pt}
.pk td,.pk th{border:1px solid #000;padding:2pt 4pt;font-size:9pt;vertical-align:top;text-align:left}
.pk th{background:#d9d9d9;font-weight:bold}
.pk .v{color:#2f5597}
.pk .b{font-weight:bold}
.pk .s{text-decoration:line-through;font-weight:normal}
.pk .c{text-align:center}
.pk .sm{font-size:8pt}
.pk .it{font-style:italic}
.pk .sig td{border:0;padding:3pt 0}
.pk .cover img{max-width:100%;width:420px;display:block;margin:12pt auto}
.pk .fot td{border:0;text-align:center;width:50%}
.pk .fot img{width:300px;max-width:100%}
.pk .fp img{width:46%;max-width:300px;margin:4pt 2% 2pt 0;vertical-align:top}
.pk .law{font-size:9pt}`;
function ph(){return'<span class="v">---</span>'}
function v(x){return x&&String(x).trim()?`<span class="v">${esc(x)}</span>`:ph()}
function protocolHTML(){
  const m=S.meta,st=structure();
  const adres=[m.ulica,[m.kod,m.miejscowosc].filter(Boolean).join(" ")].filter(Boolean).join(", ");
  const rodzLaw={roczna:"roczna – art. 62 ust. 1 pkt 1",polroczna:"półroczna – art. 62 ust. 1 pkt 3",piecio:"5-letnia – art. 62 ust. 1 pkt 2",dorazna:"doraźna – art. 62 ust. 1 pkt 4"};
  const rodz=Object.keys(rodzLaw).filter(k=>m.rodzaj[k]).map(k=>rodzLaw[k]);
  const pZ=+m.pZab||0;
  let rodzTxt=rodz.map(r=>"Kontrola "+r).join("<br>");
  if(m.rodzaj.dorazna&&m.dorPowod)rodzTxt+=` (${esc(m.dorPowod)})`;
  const zakr=[["a","Elementy budynku, budowli i instalacji narażone na szkodliwe wpływy atmosferyczne i niszczące działania czynników występujących podczas użytkowania obiektu"],["b","Instalacje i urządzenia służące ochronie środowiska"],["c",S.gasNone?"Przewody kominowe (obiekt bez instalacji gazowej)":"Instalacje gazowe oraz przewody kominowe"]].filter(z=>m.zakres[z[0]]);
  if(m.rodzaj.piecio)zakr.push(["x","Stan techniczny i przydatność do użytkowania obiektu, estetyka obiektu i jego otoczenia; badanie instalacji elektrycznej i piorunochronnej"]);
  const osoby=S.osoby.filter(o=>o.imie).map(o=>`<span class="v">${esc(o.imie)}</span><br><span class="sm it">${esc(o.upr)}${o.nr?`<br>Nr uprawnień: ${esc(o.nr)}`:""}${o.izba?`; nr członkowski izby: ${esc(o.izba)}`:""}</span>`).join("<br><br>");
  const met=[["ogl","oględziny"],["dok","analiza dokumentacji"],["pom","pomiary i badania"],["foto","dokumentacja fotograficzna"]].filter(x=>m.metodyK[x[0]]).map(x=>x[1]).join(", ");
  let h=`<div class="pk"><div class="hdr">KONTROLA OKRESOWA OBIEKTU BUDOWLANEGO</div>
  <h1>PROTOKÓŁ NR ${esc(m.nr||"……")}<br>Z OKRESOWEJ KONTROLI STANU TECHNICZNEGO OBIEKTU BUDOWLANEGO</h1>
  ${m.cover?`<div class="cover"><img src="${m.cover}" alt=""></div>`:""}
  <table><tr><th colspan="2" class="c" style="font-size:11pt">INFORMACJA O OBIEKCIE I KONTROLI</th></tr>
  <tr><td class="it" style="width:32%">Nazwa obiektu budowlanego:</td><td class="b">${v(m.nazwa)}</td></tr>
  <tr><td class="it">Adres obiektu:</td><td class="b">${v(adres.toUpperCase())}${m.dzialka?`<br><span class="sm">dz. ew. ${esc(m.dzialka)}</span>`:""}</td></tr>
  <tr><td class="it">Funkcja obiektu:</td><td class="b">${v((m.funkcja||"").toUpperCase())}</td></tr>
  <tr><td class="it">Właściciel lub zarządca obiektu:</td><td class="b">${v(m.wlasciciel)}${m.wlAdres?`<br><span class="sm" style="font-weight:normal">${esc(m.wlAdres)}</span>`:""}</td></tr>
  <tr><td class="it">Rodzaj kontroli i podstawa prawna:</td><td><span class="v">${rodzTxt}</span><br><span class="sm">powierzchnia zabudowy ${pZ?(pZ>2000?"&gt;":"&lt;")+" 2000 m²":"—"}; ustawa z dnia 7 lipca 1994 r. – Prawo budowlane</span></td></tr>
  <tr><td class="it">Zakres kontroli:</td><td><ol style="margin:0;padding-left:16pt">${zakr.map(z=>`<li>${esc(z[1])}</li>`).join("")}</ol></td></tr>
  <tr><td class="it">Osoby dokonujące kontroli:</td><td>${osoby||ph()}</td></tr>
  ${m.uczestnicy?`<tr><td class="it">Osoby obecne przy kontroli:</td><td>${v(m.uczestnicy)}</td></tr>`:""}
  <tr><td class="it">Data przeprowadzenia kontroli:</td><td>${v(fmtD(m.data))}</td></tr>
  <tr><td class="it">Warunki atmosferyczne:</td><td>${v([m.pogoda,m.temp!==""?m.temp+" °C":""].filter(Boolean).join(", "))}</td></tr>
  <tr><td class="it">Metody kontroli:</td><td>${v(met)}</td></tr>
  ${m.ograniczenia?`<tr><td class="it">Elementy niedostępne / wyłączone z kontroli:</td><td>${v(m.ograniczenia)}</td></tr>`:""}
  </table>`;
  // 1
  h+=`<h2>1. Podstawa prawna</h2><p class="law">Art. 62 ust. 1 i art. 62a ustawy z dnia 7 lipca 1994 r. – Prawo budowlane (tekst jednolity z późniejszymi zmianami).</p>`;
  // 2
  const par=[["Powierzchnia całkowita",m.pCalk,"m²"],["Powierzchnia użytkowa",m.pUzyt,"m²"],["Powierzchnia zabudowy",m.pZab,"m²"],["Kubatura",m.kub,"m³"],["Powierzchnia dachu",m.pDach,"m²"],["Liczba kondygnacji podziemnych",m.kPodz,""],["Liczba kondygnacji nadziemnych",m.kNad,""]];
  h+=`<h2>2. Informacje ogólne o obiekcie</h2>
  <table><tr><th colspan="2">Lokalizacja i sposób użytkowania</th></tr>
  <tr><td style="width:40%">Województwo</td><td>${v(m.woj)}</td></tr>
  ${m.dzialka?`<tr><td>Działka ewidencyjna, obręb</td><td>${v(m.dzialka)}</td></tr>`:""}
  ${m.kob?`<tr><td>Nr książki obiektu budowlanego (c-KOB)</td><td>${v(m.kob)}</td></tr>`:""}
  <tr><td>Rok zakończenia budowy</td><td>${v(m.rok)}</td></tr></table>
  <table><tr><th colspan="2">Parametry obiektu</th></tr>${par.map(p=>`<tr><td style="width:40%">${p[0]}</td><td>${p[1]!==""&&p[1]!=null?`<span class="v">${esc(Number(p[1])&&p[2]?Number(p[1]).toLocaleString("pl-PL"):p[1])}</span>${p[2]?` [${p[2]}]`:""}`:ph()}</td></tr>`).join("")}</table>
  <table><tr><th colspan="2">Opis techniczny obiektu</th></tr>${OPIS.map(([k,l])=>`<tr><td style="width:40%">${l}</td><td>${v(S.opis[k])}</td></tr>`).join("")}</table>
  <table><tr><th colspan="2">Podstawowe instalacje w obiekcie</th></tr>${Object.keys(S.inst).filter(k=>S.inst[k]).sort((a,b)=>{const ia=INST.indexOf(a),ib=INST.indexOf(b);return (ia<0?99:ia)-(ib<0?99:ib)}).map(k=>`<tr><td style="width:60%">${esc(k)}</td><td>${S.inst[k]==="T"?'<span class="b">TAK</span> / <span class="s">NIE</span>':'<span class="s">TAK</span> / <span class="b">NIE</span>'}</td></tr>`).join("")}</table>`;
  // 3
  h+=`<h2>3. Kryteria oceny technicznej</h2>
  <table><tr><th style="width:18%">Ocena</th><th style="width:16%">Zużycie elementu</th><th>Kryteria oceny</th></tr>
  <tr><td class="b">Dobra</td><td>0% – 15%</td><td>Element dobrze utrzymany, konserwowany, nie wykazuje zużycia i uszkodzeń. Cechy i właściwości wbudowanych materiałów odpowiadają wymaganiom normowym.</td></tr>
  <tr><td class="b">Zadowalająca</td><td>16% – 30%</td><td>Element utrzymany należycie. Celowy jest remont bieżący polegający na drobnych naprawach, uzupełnieniach, konserwacji, impregnacji.</td></tr>
  <tr><td class="b">Dostateczna</td><td>31% – 50%</td><td>Niewielkie uszkodzenia i ubytki niezagrażające bezpieczeństwu użytkowania. Celowy jest częściowy remont.</td></tr>
  <tr><td class="b">Zła</td><td>powyżej 50%</td><td>Znaczne uszkodzenia i ubytki; właściwości materiałów obniżone. Wymagany kompleksowy remont kapitalny lub wymiana.</td></tr></table>
  <table><tr><th style="width:12%">Pilność napraw</th><th style="width:20%">Termin</th><th>Uzasadnienie</th></tr>${PIL.map(p=>`<tr><td class="b c">${p[0]}°</td><td>${p[1]}</td><td>${p[2]}</td></tr>`).join("")}</table>`;
  // 4
  const stL={tak:"wykonano",czesc:"wykonano częściowo",nie:"nie wykonano",stale:"zalecenie stałe – należy nadal przestrzegać"};
  const docs=[S.docs.kob&&"książka obiektu budowlanego",S.docs.dokt&&"dokumentacja techniczna / powykonawcza",S.docs.pomEl&&"protokoły pomiarów elektrycznych",S.docs.kom&&"e-protokół z kontroli przewodów kominowych",S.docs.hydr&&"protokół z przeglądu hydrantów",S.docs.ppoz&&"protokoły przeglądów urządzeń ppoż.",S.docs.inne].filter(Boolean);
  h+=`<h2>4. Sprawdzenie zaleceń z poprzednich kontroli</h2><p>Przed rozpoczęciem kontroli zapoznano się z:</p>
  <p>– protokołami z poprzednich kontroli: ${v(S.docs.poprz||"brak")}</p><p>– innymi dokumentami mającymi znaczenie dla oceny stanu technicznego: ${v(docs.join(", ")||"brak")}</p>
  <p class="b">${esc(prevSummary())}</p>
  ${S.prev.length?`<table><tr><th>Element, urządzenie, instalacja</th><th>Zalecenia</th><th>Stopień wykonania zaleceń</th><th>Uwagi</th></tr>${S.prev.map(p=>`<tr><td>${v(p.el)}</td><td>${v(p.zal)}</td><td>${v(stL[p.st]||"")}</td><td>${v(p.uw)}</td></tr>`).join("")}</table>`:""}`;
  // rozdziały elementów
  st.chaps.forEach(({ch,num})=>{
    h+=`<h2>${num}. ${esc(ch.title)}</h2><p class="law">(${esc(ch.law)} ustawy Prawo budowlane)</p>`;
    let si=0;
    ch.secs.forEach(sec=>{
      if(!secInc(sec))return;si++;
      const so=secObj(sec.id);
      h+=`<h3>${num}.${si}. ${esc(sec.name)}</h3>`;
      if(sec.gas&&S.gasNone){h+=`<p>Przedmiotowy obiekt nie jest wyposażony w instalację gazową.</p>`;return}
      if(sec.chim)h+=`<p class="sm">Protokół z kontroli przewodów kominowych sporządza się w formie dokumentu elektronicznego w systemie teleinformatycznym centralnej ewidencji emisyjności budynków (art. 62a ust. 5 ustawy Prawo budowlane). E-protokół stanowi jedyne potwierdzenie wykonania kontroli przewodów kominowych; poniższa ocena jest odniesieniem do niego.${S.chim.nr||S.chim.data?` E-protokół nr ${v(S.chim.nr)} z dnia ${v(fmtD(S.chim.data))}${S.chim.kto?`, wykonawca: ${v(S.chim.kto)}`:""}.`:""}</p>`;
      if(sec.id==="G1"&&(S.elec.dataEl||S.elec.nrEl))h+=`<p>Ostatnie pomiary instalacji elektrycznej: ${v(fmtD(S.elec.dataEl))}${S.elec.nrEl?`, protokół nr ${v(S.elec.nrEl)}`:""}.</p>`;
      if(sec.id==="G2"&&S.elec.dataOdg)h+=`<p>Ostatnie pomiary instalacji piorunochronnej: ${v(fmtD(S.elec.dataOdg))}.</p>`;
      if(so.opis)h+=`<p>${esc(so.opis)}</p>`;
      const rows=secEls(sec).map(n=>({n,e:S.el[elId(sec.id,n)],id:elId(sec.id,n)})).filter(r=>r.e&&r.e.oc);
      if(!rows.length){h+=`<p class="it">Nie oceniano.</p>`;return}
      h+=`<table><tr><th style="width:28%">${sec.ch==="D"?"Elementy budynku":"Element instalacji / urządzenie"}</th><th style="width:15%">Ocena stanu techn.</th><th>Zalecenia / uwagi</th><th style="width:11%">Stopień pilności</th></tr>`+
      rows.map(({n,e,id})=>{if(e.oc==="nd")return`<tr><td>${esc(n)}</td><td class="v">Nie dotyczy</td><td>---</td><td>---</td></tr>`;
        const ref=st.refs[id];const z=ref?`Uwagi wg pkt ${ref}`:(e.zal||"---");
        return`<tr><td>${esc(n)}</td><td class="v">${RATE_LBL[e.oc]}</td><td class="v">${esc(z)}</td><td class="v c">${e.pil?e.pil+"°":"---"}</td></tr>`}).join("")+`</table>`;
    });
  });
  // nieprawidłowości
  h+=`<h2>${st.findNum}. Nieprawidłowości stwierdzone w trakcie kontroli</h2>`;
  h+=st.findings.length?`<table><tr><th style="width:8%">Nr</th><th>Ustalenia dokonane w trakcie kontroli, w tym wskazane nieprawidłowości</th><th>Zalecenia</th><th style="width:11%">Stopień pilności</th><th style="width:15%">Termin wykonania</th></tr>${st.findings.map(f=>`<tr><td>${f.no}</td><td class="v">${f.el?`<b>${esc(f.el)}</b> – `:""}${esc(f.find)}</td><td class="v">${esc(f.zal)}</td><td class="v c">${f.pil?f.pil+"°":"---"}</td><td class="v">${esc(deadline(f.pil))}</td></tr>${f.photos&&f.photos.length?`<tr><td></td><td colspan="4" class="fp">${f.photos.map(p=>`<img src="${p.src}" data-cm="7" alt="">`).join(" ")}<p class="sm">${f.photos.map((p,j)=>`Fot. ${f.no}/${j+1}`).join(", ")}</p></td></tr>`:""}`).join("")}</table>`:`<p>W trakcie kontroli nie stwierdzono nieprawidłowości.</p>`;
  // metody
  const mt=METODY.filter(x=>S.metody[x[0]]).map(x=>x[1]);(S.metodyInne||"").split("\n").map(x=>x.trim()).filter(Boolean).forEach(x=>mt.push(x));
  h+=`<h2>${st.metNum}. Metody i środki użytkowania elementów narażonych na szkodliwe wpływy</h2><p class="law">(art. 62a ust. 2 pkt 8 ustawy Prawo budowlane)</p>${mt.length?`<ul style="margin:3pt 0;padding-left:16pt">${mt.map(x=>`<li>${esc(x)}</li>`).join("")}</ul>`:"<p>---</p>"}`;
  // wnioski
  const c=S.concl;const p1=st.findings.filter(f=>f.pil===1);
  h+=`<h2>${st.conNum}. Wnioski końcowe i ocena przydatności do użytkowania</h2>
  <table><tr><td style="width:40%">Ogólna ocena stanu technicznego obiektu</td><td>${OGOLNA.map(([k,l])=>c.ogolna===k?`<span class="b v">${l}</span>`:`<span class="s">${l}</span>`).join(" / ")}</td></tr>
  <tr><td>Przydatność obiektu do użytkowania</td><td>${PRZYD.map(([k,t])=>`<div style="margin:2pt 0">${c.przyd===k?"☒":"☐"} ${c.przyd===k?`<span class="v b">${esc(t)}${k==="czesc"&&c.czesc?" "+esc(c.czesc):""}</span>`:`<span class="sm">${esc(t)}</span>`}</div>`).join("")}</td></tr>
  <tr><td>Nieprawidłowości wymagające usunięcia bezzwłocznie (1°)</td><td>${p1.length?`<span class="v">TAK – pkt ${p1.map(f=>f.no).join(", ")}</span>`:'<span class="v">NIE</span>'}</td></tr>
  ${p1.length?`<tr><td>Zawiadomienie organu (art. 70 ust. 2)</td><td>${c.pinbSent?`Kopię protokołu przesłano do: ${v(c.pinb)}${c.pinbData?` dnia ${v(fmtD(c.pinbData))}`:""}`:`Kopia protokołu zostanie bezzwłocznie przesłana do: ${v(c.pinb||"właściwego organu nadzoru budowlanego")}`}</td></tr>`:""}
  ${c.uwagi?`<tr><td>Uwagi</td><td>${v(c.uwagi)}</td></tr>`:""}</table>
  ${p1.length?`<p class="sm">Zgodnie z art. 70 ust. 1 ustawy Prawo budowlane właściciel, zarządca lub użytkownik obiektu, na których spoczywają obowiązki w zakresie napraw, są obowiązani w czasie lub bezpośrednio po przeprowadzonej kontroli usunąć stwierdzone uszkodzenia oraz uzupełnić braki, które mogłyby spowodować zagrożenie życia lub zdrowia ludzi, bezpieczeństwa mienia bądź środowiska. Wykonanie tego obowiązku potwierdza się w protokole, a osoba dokonująca kontroli bezzwłocznie przesyła kopię protokołu do właściwego organu (art. 70 ust. 2).</p>`:""}`;
  // terminy
  h+=`<h2>${st.terNum}. Terminy kontroli</h2>
  <table><tr><th>Data przeprowadzonej kontroli</th><th>Data następnej kontroli</th>${m.nast5?"<th>Następna kontrola 5-letnia</th>":""}<th>Data opracowania protokołu</th></tr>
  <tr><td class="v">${esc(fmtD(m.data))||"---"}</td><td class="v">${esc(fmtD(nextControl()))||"---"}</td>${m.nast5?`<td class="v">${esc(fmtD(m.nast5))}</td>`:""}<td class="v">${esc(fmtD(m.dataOpr))||"---"}</td></tr></table>
  <p class="sm">${m.rodzaj.polroczna?"Obiekt o powierzchni zabudowy przekraczającej 2000 m² lub powierzchni dachu przekraczającej 1000 m² – kontrola co najmniej dwa razy w roku, w terminach do 31 maja i do 30 listopada (art. 62 ust. 1 pkt 3).":"Kontrola okresowa co najmniej raz w roku (art. 62 ust. 1 pkt 1)"+(needsHalfYear()?"; uwaga: parametry obiektu wskazują na obowiązek kontroli dwa razy w roku (art. 62 ust. 1 pkt 3).":"; obiekt nie przekracza 2000 m² powierzchni zabudowy.")} Protokół należy dołączyć do książki obiektu budowlanego (c-KOB).</p>`;
  // podpisy
  h+=`<p style="margin-top:14pt">Oświadczamy, iż ustalenia zawarte w protokole są zgodne ze stanem faktycznym.</p><p class="b">Dokonujący kontroli stanu technicznego:</p>
  <table class="sig">${S.osoby.filter(o=>o.imie).map(o=>`<tr><td style="width:50%;padding-top:14pt"><span class="b">${esc((ROLES.find(r=>r[0]===o.rola)||["",""])[1])}</span><br><span class="v">${esc(o.imie)}</span>${o.nr?`<br><span class="sm">nr uprawnień: ${esc(o.nr)}</span>`:""}</td><td style="padding-top:34pt" class="c">..........................................................................<br><span class="sm">(czytelny podpis oraz pieczątka)</span></td></tr>`).join("")}
  ${m.zakres.c&&!S.osoby.some(o=>o.rola==="kom"&&o.imie)?`<tr><td colspan="2" class="sm" style="padding-top:10pt">Przewody kominowe – wg odrębnego e-protokołu${S.chim.nr?` nr ${esc(S.chim.nr)}`:""}.</td></tr>`:""}</table>`;
  const att=attachments();
  h+=`<p class="b" style="margin-top:12pt">Wykaz załączników:</p>${att.length?`<ul style="margin:3pt 0;padding-left:16pt">${att.map(a=>`<li>${esc(a)}</li>`).join("")}</ul>`:"<p>brak</p>"}${S.zal.crub?`<p class="sm">Osoby dokonujące kontroli są wpisane do centralnego rejestru osób posiadających uprawnienia budowlane – kopie decyzji i zaświadczeń nie są dołączane (art. 62a ust. 4a).</p>`:""}`;
  if(S.photos.length){h+=`<h2 style="page-break-before:always">Dokumentacja fotograficzna</h2><table class="fot">`;for(let i=0;i<S.photos.length;i+=2){h+="<tr>"+[0,1].map(j=>{const p=S.photos[i+j];return p?`<td><img src="${p.src}" alt=""><br><span class="sm">Fot. ${i+j+1}${p.opis?" – "+esc(p.opis):""}</span></td>`:"<td></td>"}).join("")+"</tr>"}h+="</table>"}
  return h+"</div>";
}

/* ============================================================
   EKSPORT
   ============================================================ */
const inFrame=(()=>{try{return window.self!==window.top}catch(e){return true}})();
if(!inFrame)$("#bPrint").hidden=false;
function fname(ext){const n=(S.meta.nr||"protokol").replace(/[\\/:*?"<>|]+/g,"_");return`Protokol_${n}.${ext}`}
async function saveFile(name,data,mime){
  let d=null;
  if(window.claude&&typeof window.claude.use==="function"){try{d=await window.claude.use("downloads")}catch(e){d=null}}
  if(d){try{await d.save({filename:name,data});toast("Zapisano plik "+name)}catch(e){if(e&&e.code==="declined")return;toast("Nie udało się zapisać pliku ("+((e&&e.code)||"błąd")+").")}return}
  try{const blob=data instanceof Blob?data:new Blob([data],{type:mime});const a=document.createElement("a");a.href=URL.createObjectURL(blob);a.download=name;document.body.appendChild(a);a.click();setTimeout(()=>{URL.revokeObjectURL(a.href);a.remove()},1500);toast("Pobieranie: "+name)}catch(e){toast("Pobieranie niedostępne w tym widoku.")}
}
function standaloneHTML(){return`<!doctype html><html lang="pl"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>Protokół ${esc(S.meta.nr)}</title><style>@page{size:A4;margin:18mm 15mm 18mm 20mm}body{margin:0;padding:24px;background:#fff}.pk{max-width:780px;margin:0 auto}@media print{body{padding:0}}${DOC_CSS}</style></head><body>${protocolHTML()}</body></html>`}
/* --- minimalny ZIP + DOCX (altChunk MHT) --- */
const CRC=(()=>{const t=new Uint32Array(256);for(let n=0;n<256;n++){let c=n;for(let k=0;k<8;k++)c=c&1?0xEDB88320^(c>>>1):c>>>1;t[n]=c>>>0}return t})();
function crc32(u){let c=0xFFFFFFFF;for(let i=0;i<u.length;i++)c=CRC[(c^u[i])&255]^(c>>>8);return(c^0xFFFFFFFF)>>>0}
function zip(files){const enc=new TextEncoder();const parts=[];const cd=[];let off=0;
  files.forEach(f=>{const name=enc.encode(f.name);const data=typeof f.data==="string"?enc.encode(f.data):f.data;const crc=crc32(data);
    const h=new DataView(new ArrayBuffer(30));h.setUint32(0,0x04034b50,true);h.setUint16(4,20,true);h.setUint16(6,0x0800,true);h.setUint16(8,0,true);h.setUint16(10,0,true);h.setUint16(12,0x21,true);h.setUint32(14,crc,true);h.setUint32(18,data.length,true);h.setUint32(22,data.length,true);h.setUint16(26,name.length,true);h.setUint16(28,0,true);
    parts.push(new Uint8Array(h.buffer),name,data);
    const c=new DataView(new ArrayBuffer(46));c.setUint32(0,0x02014b50,true);c.setUint16(4,20,true);c.setUint16(6,20,true);c.setUint16(8,0x0800,true);c.setUint16(10,0,true);c.setUint16(12,0,true);c.setUint16(14,0x21,true);c.setUint32(16,crc,true);c.setUint32(20,data.length,true);c.setUint32(24,data.length,true);c.setUint16(28,name.length,true);c.setUint32(42,off,true);
    cd.push(new Uint8Array(c.buffer),name);off+=30+name.length+data.length});
  const cdSize=cd.reduce((s,a)=>s+a.length,0);const e=new DataView(new ArrayBuffer(22));e.setUint32(0,0x06054b50,true);e.setUint16(8,files.length,true);e.setUint16(10,files.length,true);e.setUint32(12,cdSize,true);e.setUint32(16,off,true);
  return new Blob([...parts,...cd,new Uint8Array(e.buffer)],{type:"application/vnd.openxmlformats-officedocument.wordprocessingml.document"})}
/* --- natywny DOCX (WordprocessingML) budowany z HTML protokołu --- */
const TW=9922; // szerokość obszaru tekstu w twipach
const xe=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
function imgSize(src){return new Promise(r=>{const i=new Image();i.onload=()=>r([i.naturalWidth,i.naturalHeight]);i.onerror=()=>r([800,600]);i.src=src})}
function stOf(el,st){const s=Object.assign({},st);const c=el.classList||{contains:()=>false};const t=el.tagName;
  if(t==="B"||t==="STRONG"||t==="TH"||c.contains("b"))s.b=true;
  if(t==="I"||c.contains("it"))s.i=true;
  if(c.contains("s")){s.strike=true;s.b=false}
  if(c.contains("v"))s.color="2F5597";
  if(c.contains("sm")||c.contains("law"))s.sz=16;
  if(c.contains("c"))s.center=true;
  return s}
function rPr(s){return`<w:rPr><w:rFonts w:ascii="Arial" w:hAnsi="Arial" w:cs="Arial"/>${s.b?"<w:b/>":""}${s.i?"<w:i/>":""}${s.strike?"<w:strike/>":""}${s.caps?"<w:caps/>":""}${s.color?`<w:color w:val="${s.color}"/>`:""}<w:sz w:val="${s.sz||20}"/><w:szCs w:val="${s.sz||20}"/></w:rPr>`}
function runsOf(node,st,ctx){let out=[];
  node.childNodes.forEach(n=>{
    if(n.nodeType===3){const t=n.textContent.replace(/\s+/g," ");if(t)out.push(`<w:r>${rPr(st)}<w:t xml:space="preserve">${xe(t)}</w:t></w:r>`);return}
    if(n.nodeType!==1)return;
    if(n.tagName==="BR"){out.push(`<w:r>${rPr(st)}<w:br/></w:r>`);return}
    if(n.tagName==="IMG"){out.push(imgRun(n,ctx));return}
    out=out.concat(runsOf(n,stOf(n,st),ctx))});
  return out}
function imgRun(img,ctx){const src=img.getAttribute("src")||"";const m=src.match(/^data:image\/(jpeg|png|gif);base64,(.+)$/);if(!m)return"";
  const i=ctx.imgs.length+1;const ext=m[1]==="jpeg"?"jpg":m[1];const [w,h]=ctx.sizes[src]||[800,600];
  const maxW=+img.getAttribute("data-cm")||(img.closest(".cover")?15:8);const cx=Math.round(maxW*360000);const cy=Math.round(cx*h/w);
  ctx.imgs.push({name:`image${i}.${ext}`,data:m[2],rid:`rImg${i}`});
  return`<w:r><w:drawing><wp:inline distT="0" distB="0" distL="0" distR="0"><wp:extent cx="${cx}" cy="${cy}"/><wp:docPr id="${i}" name="Obraz ${i}"/><a:graphic xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"><a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/picture"><pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"><pic:nvPicPr><pic:cNvPr id="${i}" name="image${i}.${ext}"/><pic:cNvPicPr/></pic:nvPicPr><pic:blipFill><a:blip r:embed="rImg${i}"/><a:stretch><a:fillRect/></a:stretch></pic:blipFill><pic:spPr><a:xfrm><a:off x="0" y="0"/><a:ext cx="${cx}" cy="${cy}"/></a:xfrm><a:prstGeom prst="rect"><a:avLst/></a:prstGeom></pic:spPr></pic:pic></a:graphicData></a:graphic></wp:inline></w:drawing></w:r>`}
function para(runs,o={}){const sp=`<w:spacing w:before="${o.before||0}" w:after="${o.after==null?60:o.after}"/>`;
  return`<w:p><w:pPr>${o.pb?"<w:pageBreakBefore/>":""}${o.keep?"<w:keepNext/>":""}${sp}${o.ind?`<w:ind w:left="${o.ind}" w:hanging="${o.hang||0}"/>`:""}${o.center?'<w:jc w:val="center"/>':""}</w:pPr>${runs.join("")}</w:p>`}
function blocks(node,st,ctx,inCell){const out=[];let cur=[];
  const flush=()=>{if(cur.length){out.push(para(cur,{center:st.center,after:inCell?0:60}));cur=[]}};
  node.childNodes.forEach(n=>{
    if(n.nodeType===3){const t=n.textContent.replace(/\s+/g," ");if(t.trim()||cur.length)cur=cur.concat(runsOf({childNodes:[n]},st,ctx));return}
    if(n.nodeType!==1)return;const t=n.tagName;
    if(["SPAN","B","I","STRONG","BR","IMG"].includes(t)){cur=cur.concat(t==="BR"?[`<w:r><w:br/></w:r>`]:t==="IMG"?[imgRun(n,ctx)]:runsOf(n,stOf(n,st),ctx));return}
    flush();const s=stOf(n,st);
    if(t==="H1"){out.push(para(runsOf(n,Object.assign(s,{b:true,sz:26}),ctx),{center:true,before:360,after:280}));return}
    if(t==="H2"){out.push(para(runsOf(n,Object.assign(s,{b:true,sz:22,caps:true}),ctx),{before:280,after:100,keep:true,pb:/page-break-before/.test(n.getAttribute("style")||"")}));return}
    if(t==="H3"){out.push(para(runsOf(n,Object.assign(s,{b:true}),ctx),{before:180,after:60,keep:true}));return}
    if(t==="P"){out.push(para(runsOf(n,s,ctx),{center:s.center,after:inCell?0:60,before:/margin-top/.test(n.getAttribute("style")||"")?200:0}));return}
    if(t==="UL"||t==="OL"){[...n.children].forEach((li,k)=>{out.push(para([`<w:r>${rPr(s)}<w:t xml:space="preserve">${t==="OL"?(k+1)+".":"–"}\t</w:t></w:r>`].concat(runsOf(li,stOf(li,s),ctx)),{ind:360,hang:360,after:inCell?0:40}))});return}
    if(t==="TABLE"){out.push(table(n,s,ctx));if(!inCell)out.push(para([],{after:60}));return}
    if(t==="DIV"){if(n.classList.contains("hdr"))return;if(n.classList.contains("cover")){out.push(para(runsOf(n,s,ctx),{center:true,after:200}));return}out.push(...blocks(n,s,ctx,inCell));return}
    out.push(...blocks(n,s,ctx,inCell))});
  flush();return out}
function table(tb,st,ctx){
  const rows=[...tb.querySelectorAll(":scope > tbody > tr, :scope > tr")];
  const nCols=Math.max(...rows.map(r=>[...r.children].reduce((a,c)=>a+(+c.getAttribute("colspan")||1),0)));
  const full=rows.find(r=>r.children.length===nCols)||rows[0];
  let pct=[...full.children].map(c=>{const m=(c.getAttribute("style")||"").match(/width:(\d+)%/);return m?+m[1]:0});
  const fixed=pct.reduce((a,b)=>a+b,0),free=pct.filter(x=>!x).length;pct=pct.map(x=>x||Math.max(5,(100-fixed)/Math.max(1,free)));
  const cols=pct.map(p=>Math.round(TW*p/100));
  const noB=tb.classList.contains("sig")||tb.classList.contains("fot");
  const bd=noB?'<w:tblBorders><w:top w:val="nil"/><w:left w:val="nil"/><w:bottom w:val="nil"/><w:right w:val="nil"/><w:insideH w:val="nil"/><w:insideV w:val="nil"/></w:tblBorders>':'<w:tblBorders><w:top w:val="single" w:sz="4" w:color="000000"/><w:left w:val="single" w:sz="4" w:color="000000"/><w:bottom w:val="single" w:sz="4" w:color="000000"/><w:right w:val="single" w:sz="4" w:color="000000"/><w:insideH w:val="single" w:sz="4" w:color="000000"/><w:insideV w:val="single" w:sz="4" w:color="000000"/></w:tblBorders>';
  let x=`<w:tbl><w:tblPr><w:tblW w:w="${TW}" w:type="dxa"/>${bd}<w:tblLayout w:type="fixed"/><w:tblCellMar><w:top w:w="28" w:type="dxa"/><w:left w:w="70" w:type="dxa"/><w:bottom w:w="28" w:type="dxa"/><w:right w:w="70" w:type="dxa"/></w:tblCellMar></w:tblPr><w:tblGrid>${cols.map(c=>`<w:gridCol w:w="${c}"/>`).join("")}</w:tblGrid>`;
  rows.forEach((r,ri)=>{let ci=0;const isHead=[...r.children].every(c=>c.tagName==="TH");
    x+=`<w:tr><w:trPr><w:cantSplit/>${isHead&&ri===0?"<w:tblHeader/>":""}</w:trPr>`;
    [...r.children].forEach(c=>{const span=+c.getAttribute("colspan")||1;const w=cols.slice(ci,ci+span).reduce((a,b)=>a+b,0);ci+=span;
      const s=stOf(c,Object.assign({},st,{sz:18}));
      const ps=blocks(c,s,ctx,true);
      const fs=(c.getAttribute("style")||"").match(/font-size:(\d+)pt/);if(fs)s.sz=+fs[1]*2;
      x+=`<w:tc><w:tcPr><w:tcW w:w="${w}" w:type="dxa"/>${span>1?`<w:gridSpan w:val="${span}"/>`:""}${c.tagName==="TH"?'<w:shd w:val="clear" w:color="auto" w:fill="D9D9D9"/>':""}</w:tcPr>${ps.length?ps.join(""):para([],{after:0})}</w:tc>`});
    x+="</w:tr>"});
  return x+"</w:tbl>"}
async function buildDocx(){
  const html=protocolHTML();const dom=new DOMParser().parseFromString(html,"text/html");const root=dom.querySelector(".pk");
  const sizes={};for(const im of root.querySelectorAll("img")){const s=im.getAttribute("src");if(s&&!sizes[s])sizes[s]=await imgSize(s)}
  const ctx={imgs:[],sizes};
  const body=blocks(root,{sz:20},ctx,false).join("");
  const W='xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"';
  const box='<w:pBdr><w:top w:val="single" w:sz="4" w:space="1" w:color="000000"/><w:left w:val="single" w:sz="4" w:space="4" w:color="000000"/><w:bottom w:val="single" w:sz="4" w:space="1" w:color="000000"/><w:right w:val="single" w:sz="4" w:space="4" w:color="000000"/></w:pBdr><w:jc w:val="center"/>';
  const rp='<w:rPr><w:rFonts w:ascii="Times New Roman" w:hAnsi="Times New Roman" w:cs="Times New Roman"/><w:sz w:val="18"/></w:rPr>';
  const run=t=>`<w:r>${rp}<w:t xml:space="preserve">${t}</w:t></w:r>`;
  const fld=f=>`<w:r>${rp}<w:fldChar w:fldCharType="begin"/></w:r><w:r>${rp}<w:instrText xml:space="preserve"> ${f} </w:instrText></w:r><w:r>${rp}<w:fldChar w:fldCharType="separate"/></w:r>${run("1")}<w:r>${rp}<w:fldChar w:fldCharType="end"/></w:r>`;
  const b64=s=>{const bin=atob(s);const u=new Uint8Array(bin.length);for(let i=0;i<bin.length;i++)u[i]=bin.charCodeAt(i);return u};
  const files=[
   {name:"[Content_Types].xml",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Types xmlns="http://schemas.openxmlformats.org/package/2006/content-types"><Default Extension="rels" ContentType="application/vnd.openxmlformats-package.relationships+xml"/><Default Extension="xml" ContentType="application/xml"/><Default Extension="jpg" ContentType="image/jpeg"/><Default Extension="png" ContentType="image/png"/><Default Extension="gif" ContentType="image/gif"/><Override PartName="/word/document.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/><Override PartName="/word/styles.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.styles+xml"/><Override PartName="/word/header1.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.header+xml"/><Override PartName="/word/footer1.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.footer+xml"/></Types>`},
   {name:"_rels/.rels",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"><Relationship Id="R1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target="word/document.xml"/></Relationships>`},
   {name:"word/_rels/document.xml.rels",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships"><Relationship Id="rSt" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/styles" Target="styles.xml"/><Relationship Id="rIdH" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/header" Target="header1.xml"/><Relationship Id="rIdF" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/footer" Target="footer1.xml"/>${ctx.imgs.map(im=>`<Relationship Id="${im.rid}" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/image" Target="media/${im.name}"/>`).join("")}</Relationships>`},
   {name:"word/styles.xml",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:styles ${W}><w:docDefaults><w:rPrDefault><w:rPr><w:rFonts w:ascii="Arial" w:hAnsi="Arial" w:cs="Arial" w:eastAsia="Arial"/><w:sz w:val="20"/><w:lang w:val="pl-PL"/></w:rPr></w:rPrDefault><w:pPrDefault><w:pPr><w:spacing w:after="60" w:line="240" w:lineRule="auto"/></w:pPr></w:pPrDefault></w:docDefaults><w:style w:type="paragraph" w:default="1" w:styleId="Normal"><w:name w:val="Normal"/></w:style></w:styles>`},
   {name:"word/document.xml",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:document ${W}><w:body>${body}<w:sectPr><w:headerReference w:type="default" r:id="rIdH"/><w:footerReference w:type="default" r:id="rIdF"/><w:pgSz w:w="11906" w:h="16838"/><w:pgMar w:top="1134" w:right="850" w:bottom="1134" w:left="1134" w:header="567" w:footer="567" w:gutter="0"/></w:sectPr></w:body></w:document>`},
   {name:"word/header1.xml",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:hdr ${W}><w:p><w:pPr>${box}</w:pPr>${run("KONTROLA OKRESOWA OBIEKTU BUDOWLANEGO")}</w:p></w:hdr>`},
   {name:"word/footer1.xml",data:`<?xml version="1.0" encoding="UTF-8" standalone="yes"?><w:ftr ${W}><w:p><w:pPr>${box}</w:pPr>${run("strona ")}${fld("PAGE")}${run("/")}${fld("NUMPAGES")}</w:p></w:ftr>`}
  ].concat(ctx.imgs.map(im=>({name:"word/media/"+im.name,data:b64(im.data)})));
  return zip(files);
}
function doExport(act){
  if(act==="docx")return buildDocx().then(b=>saveFile(fname("docx"),b)).catch(()=>toast("Nie udało się zbudować pliku Word."));
  if(act==="html")return saveFile(fname("html"),standaloneHTML(),"text/html");
  if(act==="json")return saveFile(fname("json"),JSON.stringify(S,null,1),"application/json");
  if(act==="print"){go("P");setTimeout(()=>window.print(),200)}
}
function closeMenus(){$("#expMenu").hidden=true;$("#moreMenu").hidden=true}
$("#bExp").onclick=e=>{e.stopPropagation();const h=$("#expMenu").hidden;closeMenus();$("#expMenu").hidden=!h};
$("#bMore").onclick=e=>{e.stopPropagation();const h=$("#moreMenu").hidden;closeMenus();$("#moreMenu").hidden=!h};
$("#bPrev").onclick=()=>go("P");
$("#mSel").addEventListener("change",e=>go(e.target.value));
$("#mPrev").onclick=()=>{const ids=NAV.filter(x=>x.id);const i=ids.findIndex(x=>x.id===cur);if(i>0)go(ids[i-1].id)};
$("#mNext").onclick=()=>{const ids=NAV.filter(x=>x.id);const i=ids.findIndex(x=>x.id===cur);if(i<ids.length-1)go(ids[i+1].id)};
document.addEventListener("click",e=>{if(!e.target.closest(".menu"))closeMenus()});
document.addEventListener("keydown",e=>{if(e.key==="Escape")closeMenus()});
$("#expMenu").addEventListener("click",e=>{const b=e.target.closest("[data-act]");if(!b)return;closeMenus();doExport(b.dataset.act)});
$("#moreMenu").addEventListener("click",e=>{const b=e.target.closest("[data-act]");if(!b)return;closeMenus();const a=b.dataset.act;
  if(a==="load")$("#fileJson").click();
  if(a==="new")confirmBox("Nowy protokół","Bieżące dane zostaną wyczyszczone. Jeśli chcesz je zachować, najpierw zapisz projekt (.json).","Wyczyść",()=>{S=fresh();save();go("A")});
  if(a==="next")confirmBox("Następna kontrola","Nieprawidłowości z tego protokołu staną się zaleceniami do sprawdzenia, oceny i zdjęcia zostaną wyczyszczone, a data kontroli ustawiona na termin następnej kontroli. Dane obiektu i osób pozostają.","Utwórz",()=>{
    const st=structure();const prevNr=S.meta.nr,prevD=S.meta.data;
    S.prev=st.findings.map(f=>({el:f.el,zal:f.zal||f.find,st:"",uw:""}));
    if(S.metody.snieg)S.prev.push({el:"Dach budynku",zal:"Na bieżąco usuwać śnieg i lód z dachu",st:"stale",uw:""});
    S.docs.poprz=`Protokół nr ${prevNr||"…"}${prevD?" z dnia "+fmtD(prevD):""}`;
    const nd=nextControl();S.meta.data=nd||"";S.meta.dataOpr="";S.meta.nastepna="";S.meta.nr="";S.meta.pogoda="";S.meta.temp="";
    Object.values(S.el).forEach(e=>{e.oc="";e.find="";e.zal="";e.pil=0;e.photos=[]});S.extra=[];S.photos=[];S.concl=Object.assign(blank().concl,{pinb:S.concl.pinb});S.chim={nr:"",data:"",kto:""};
    save();go("C");toast("Utworzono nową kontrolę – sprawdź zalecenia z poprzedniej.")})});
$("#fileJson").addEventListener("change",e=>{const f=e.target.files[0];if(!f)return;const fr=new FileReader();fr.onload=()=>{try{S=migrate(JSON.parse(fr.result));save();go("A");toast("Wczytano projekt "+f.name)}catch(err){toast("To nie jest poprawny plik projektu (.json).")}e.target.value=""};fr.readAsText(f)});

(function(){const st=document.createElement("style");st.textContent=DOC_CSS;document.head.appendChild(st)})();
render();
try{const on=document.querySelector("#nav .on");if(on&&cur!=="A")on.scrollIntoView({block:"nearest",inline:"center"})}catch(e){}
</script>
</body></html>
