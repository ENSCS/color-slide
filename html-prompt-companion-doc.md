# Prompt: เอกสาร HTML ขนาด A4 ประกอบสไลด์ (เนื้อหาเต็ม อ่านเข้าใจได้ในตัวเอง)

วิธีใช้: แนบไฟล์สไลด์ .pptx และ PDF ที่ export จากสไลด์ชุดเดียวกัน แล้ววางทั้งบล็อกด้านล่าง
(ข้อความในวงเล็บ `[...]` แก้ได้ ถ้าไม่แก้ให้ลบบรรทัดนั้นทิ้ง)

ผลที่ได้คือไฟล์ .html ไฟล์เดียว เปิดในเบราว์เซอร์จะเห็นเป็นหน้ากระดาษ A4 เรียงกัน
ต้องการ PDF ให้เปิดด้วย Chrome แล้วสั่งพิมพ์ เลือก Save as PDF

```text
ช่วยสร้างเอกสาร HTML ขนาดหน้า A4 จากสไลด์ที่แนบมา (.pptx และ PDF ของสไลด์ชุดเดียวกัน)
[ผู้อ่าน: ...]
[ชื่อวิชาหรือชุดเอกสาร สำหรับหัวกระดาษ: ...]
[บทที่: ... ถ้าเป็นเอกสารเดี่ยวให้ลบบรรทัดนี้]

ไม่ต้องถามกลับ ถ้ามีจุดที่ไม่ชัดให้ตัดสินใจเอง แล้วบอกสั้นๆ ตอนส่งไฟล์

เป้าหมาย: สไลด์เป็นสื่อประกอบการบรรยาย เนื้อหาจึงไม่ครบในตัว เอกสารนี้ต้องเติมให้ครบ
ผู้อ่านอ่านเองแล้วเข้าใจได้ โดยไม่ต้องฟังบรรยายและไม่ต้องเปิดสไลด์

1. เนื้อหา
   - ครอบคลุมทุกหัวข้อในสไลด์ ตามลำดับเดิม ใช้คำศัพท์ สัญลักษณ์ และตัวอย่างชุดเดียวกับสไลด์
   - ขยายข้อความสั้นในสไลด์เป็นคำอธิบายเต็ม: บอกว่าคืออะไร ทำไม ทำงานอย่างไร
     เชื่อมแต่ละหัวข้อให้ต่อเนื่อง และอธิบายขั้นตอนของตัวอย่างทีละขั้น
   - เติมได้เฉพาะคำอธิบายที่ช่วยให้เข้าใจสิ่งที่สไลด์สอน ไม่เพิ่มหัวข้อใหม่ที่สไลด์ไม่มี
     ไม่ใส่ตัวเลขหรือข้อเท็จจริงที่ไม่แน่ใจ
   - ภาษาไทยทางการกึ่งวิชาการแบบตำรา เข้าใจง่าย ตรงประเด็น
   - ไม่อ้างถึงสไลด์ ("ดังสไลด์ที่ 5") ให้อ้างหัวข้อ รูป หรือตารางในเอกสารแทน
   - เลขยกกำลังและตัวห้อย (เช่น x², H₂O, m², a₁, a₂, …, aₙ) ใช้ <sup> และ <sub> เสมอ
     ไม่ใช้เครื่องหมาย ^ และไม่พิมพ์ตัวเลขขนาดปกติต่อท้ายแทนตัวห้อย

2. โครงเอกสาร
   - ลำดับ: บทนำ → วัตถุประสงค์การเรียนรู้ → คำศัพท์สำคัญ (ตาราง) → เนื้อหา → สรุป
     ถ้าสไลด์มีกิจกรรม โจทย์ฝึก หรือแบบทดสอบ ให้ใส่ต่อจากสรุป
     และรวมเฉลยทั้งหมดไว้หัวข้อสุดท้าย "เฉลยท้ายบท" ขึ้นหน้าใหม่ ไม่วางเฉลยต่อท้ายโจทย์
   - หัวข้อที่ไม่มีเลข: บทนำ, วัตถุประสงค์การเรียนรู้, คำศัพท์สำคัญ, สรุป, เฉลยท้ายบท
   - หัวข้อเนื้อหามีเลข 2 ระดับ จัดตามหมวดของสไลด์ เริ่มนับที่เนื้อหาเรื่องแรกเสมอ
   - ถ้าระบุเลขบท (เอกสารเป็นบทหนึ่งของชุด): หัวข้อเป็น N.1, N.1.1
     รูปเป็น "รูปที่ N.k" ตารางเป็น "ตารางที่ N.k" และใส่เลขบทใน data-chapter
   - ถ้าไม่ระบุ (เอกสารเดี่ยว): ไม่มีคำว่า "บทที่" ทุกที่ หัวข้อเป็น 1., 1.1
     รูปเป็น "รูปที่ k" ตารางเป็น "ตารางที่ k" data-chapter เว้นว่าง ห้ามตั้งเลขบทขึ้นเอง
   - โจทย์ที่ให้ผู้อ่านเขียนตอบ ทำเป็นพื้นที่ว่างหรือตารางเปล่าในเอกสาร ไม่ใช้รูปจากสไลด์
   - ไม่มีหน้าปกและสารบัญ

3. รูปแบบไฟล์
   - ส่งเป็นไฟล์ .html ไฟล์เดียว รูปทุกรูปฝังในไฟล์ ไม่มีไฟล์ประกอบ
   - ใช้ "โครงไฟล์" ท้าย prompt นี้ตามตัวอักษร ทั้ง CSS และสคริปต์แบ่งหน้า
     แก้ได้เฉพาะ: ค่าสีใน :root, <title>, data-series, data-title, data-chapter
     และเนื้อหาใน <main id="doc"> เพิ่ม CSS ได้เมื่อเนื้อหาต้องใช้องค์ประกอบที่โครงไฟล์ไม่มี
   - ค่าสีใน :root ใช้ชุดเดียวกับสไลด์ที่แนบ: อ่านสีหลัก สีหลักเข้ม สีเน้น สีตัวอักษร
     และสีพื้นจางจากไฟล์ .pptx (--accent-text คือสีเน้นเฉดเข้มที่อ่านบนพื้นขาวได้ชัด)
   - สคริปต์จะแบ่งเนื้อหาลงหน้า A4 และใส่หัวกระดาษ ท้ายกระดาษ เลขหน้าให้เอง
     จึงห้ามแบ่งหน้าเอง ห้ามเขียนหัวกระดาษ ท้ายกระดาษ หรือเลขหน้าลงในเนื้อหา
   - เนื้อหาทุกชิ้นต้องเป็นลูกโดยตรงของ <main id="doc"> เรียงต่อกัน ไม่ซ้อนใน div หรือ section อื่น
     และแต่ละชิ้นต้องสั้นกว่าหนึ่งหน้า ใช้ได้เฉพาะองค์ประกอบต่อไปนี้
       <h1>ชื่อเรื่อง</h1>  ถ้ามีเลขบท: <h1><small>บทที่ N</small>ชื่อเรื่อง</h1>
       <h2>หัวข้อระดับ 1</h2>   <h3>หัวข้อระดับ 2</h3>
       <p>ย่อหน้า</p>  (เยื้องบรรทัดแรกและชิดซ้ายให้เอง)   <p class="flush">ย่อหน้าไม่เยื้อง</p>
       <ul>, <ol>  รายการ
       <div class="note"><p>…</p></div>  กล่องข้อสังเกต (class="note accent" = พื้นจางสีเน้น)
       <figure><img src="data:…" style="width:…mm" alt="…"><figcaption><b>รูปที่ k</b> คำบรรยาย</figcaption></figure>
       <div class="tbl"><p class="tcap"><b>ตารางที่ k</b> ชื่อตาราง</p><table><thead>…</thead><tbody>…</tbody></table></div>
       <div class="choices"><p>ก. …</p><p>ข. …</p></div>  ตัวเลือกของแบบทดสอบ
       <div class="blank" style="height:…mm"></div>  พื้นที่ว่างให้เขียนตอบ
     เพิ่ม class="new-page" ที่ชิ้นซึ่งต้องขึ้นหน้าใหม่ (เช่น <h2 class="new-page">เฉลยท้ายบท</h2>)
     เพิ่ม class="keep-next" ที่ย่อหน้าซึ่งต้องอยู่หน้าเดียวกับชิ้นถัดไป (เช่น คำถามกับตัวเลือก)

4. ตาราง
   - ตารางในสไลด์ให้สร้างเป็นตาราง HTML จริง ไม่ทำเป็นรูป แถวแรกอยู่ใน <thead>
   - ความกว้างพอดีเนื้อหา (ไม่กำหนด width) โครงไฟล์จัดกึ่งกลางหน้าให้เอง
   - การจัดแนวกำหนดเป็นรายคอลัมน์ ทุกเซลล์ในคอลัมน์เดียวกันจัดแนวเดียวกันเสมอ:
     คอลัมน์ตัวเลข หรือคำสั้นทุกแถว ใส่ class="c" ทุกเซลล์ (จัดกึ่งกลาง)
     คอลัมน์ที่มีข้อความยาวหรือประโยคแม้เพียงแถวเดียว ไม่ใส่ class (ชิดซ้ายทั้งคอลัมน์)
   - คำบรรยายอยู่เหนือตาราง (<p class="tcap">) นับต่อเนื่องทั้งเอกสาร แยกจากเลขรูป
     และเนื้อหาต้องกล่าวถึงตารางทุกตาราง เลขตารางและเลขรูปเริ่มนับที่ส่วนเนื้อหา
     ตารางคำศัพท์สำคัญและตารางในเฉลยท้ายบท ไม่มีเลขและไม่มีคำบรรยาย

5. รูป: นำมาจากสไลด์โดยตรง ไม่วาดใหม่ และไม่จับภาพทั้งสไลด์
   - ภาพประกอบที่ฝังเป็นรูปชิ้นใหญ่ใน .pptx ให้ดึงไฟล์รูปนั้นมาฝังเป็น <img> แบบ data URI
   - ส่วนที่ประกอบจากรูปร่างหลายชิ้น (การ์ด แผนภาพ ลูกศร) ให้แปลงหน้านั้นของ PDF เป็น SVG
     แล้วตัดด้วยการตั้งค่า viewBox ให้เท่ากรอบของการ์ดหรือกลุ่มรูปร่าง ซึ่งอ่านพิกัดจาก .pptx
     (ไม่ใช้ clip-path ครอบ เพราะจะเกิดเส้นขอบบางๆ ตอนพิมพ์เป็น PDF)
   - ลบชั้นเงาของการ์ดออกจาก SVG เพราะทำให้เกิดเส้นขอบดำตอนพิมพ์ ชั้นเงาคือภาพบิตแมปขนาดใหญ่
     ที่เป็นสีเดียวทั้งภาพและใช้คู่กับ mask (ไอคอนเป็นบิตแมปขนาดเล็ก ต้องเก็บไว้)
     แล้วลบ mask และบิตแมปที่ไม่ถูกใช้ ตัวอักษรที่อยู่นอกกรอบตัด และเส้นร่างตัวอักษรที่ไม่ได้ใช้ เพื่อลดขนาดไฟล์
   - ฝัง SVG เป็น <img src="data:image/svg+xml;base64,…"> เท่านั้น ห้ามวาง <svg> ลงในหน้าตรงๆ
     เพราะ id ภายในของแต่ละรูปจะชนกัน
   - ถ้าไฟล์ HTML รวมใหญ่เกินประมาณ 15 MB ให้เปลี่ยนรูปที่ใหญ่ที่สุดเป็น PNG กว้าง 1600 พิกเซล
   - ถ้าไม่มี PDF ให้ติดตั้งฟอนต์ Sarabun แล้วแปลง .pptx เป็น PDF เองก่อนตัด
     ถ้าติดตั้งฟอนต์ไม่ได้ ให้หยุดแล้วขอ PDF ห้ามใช้ภาพที่ฟอนต์ถูกแทน
   - กรอบตัดครอบเนื้อหาของรูปให้ครบ ไม่ตัดขาด และไม่รวมป้ายหมวด หัวข้อสไลด์
     แถบสรุปล่าง เลขหน้า
   - สไลด์ที่มีการ์ดซ้าย–ขวา เลือกเฉพาะด้านที่เป็นภาพ ด้านที่เป็นข้อความให้เขียนเป็นเนื้อหา
   - การ์ดในสไลด์ เลือกวิธีนำเสนอตามลักษณะเนื้อหา อย่างใดอย่างหนึ่ง ไม่ทำซ้ำสองแบบ:
     • เน้นให้เห็นภาพรวม หรือเป็นลำดับขั้น → ตัดทั้งกลุ่มการ์ดมาเป็นรูป
       (รวมลูกศรระหว่างการ์ด ไม่รวมแถบสรุปล่าง) แล้วอธิบายขยายในเนื้อหา
     • รายละเอียดเยอะ หรือต้องเทียบหลายหัวข้อ → ทำเป็นตาราง
       และเติมรายละเอียดได้มากกว่าที่การ์ดมี
   - ไม่นำมาเป็นรูป: หน้าเปิด หน้าปิด แผนที่คำศัพท์ แบบทดสอบ และไม่ใส่รูปที่ซ้ำกับตารางในเอกสาร
   - วางรูปหลังย่อหน้าที่กล่าวถึงรูปนั้น กำหนดความกว้างเป็น mm ตามสัดส่วนของรูป
     (กลุ่มการ์ดเต็มแถวประมาณ 150–160mm ภาพประกอบเดี่ยวไม่สูงเกินราวครึ่งหน้า)
     คำบรรยายใต้รูปตามรูปแบบเลขรูปในข้อ 2 นับต่อเนื่องทั้งเอกสาร และเนื้อหาต้องกล่าวถึงรูปทุกรูป

ก่อนส่ง เปิดไฟล์ด้วยเบราว์เซอร์แบบไม่มีหน้าจอ (Chrome/Chromium) รอให้สคริปต์แบ่งหน้าเสร็จ แล้วตรวจว่า
- document.body.dataset.overflow เป็น "0" (ไม่มีหน้าใดเนื้อหาล้น) ถ้าไม่ใช่ ให้ย่อหรือแบ่งชิ้นที่ล้น
- พิมพ์เป็น PDF แล้วเปิดดูทุกหน้า: รูปไม่ขาดและไม่ซ้ำ ฟอนต์ในรูปถูกต้อง ไม่มีเส้นหรือขอบดำรอบรูป
  ตารางไม่ล้นขอบ เลขรูปและเลขตารางเรียงถูก หัวข้อไม่ตกอยู่ท้ายหน้าโดยไม่มีเนื้อหาตาม
  และเฉลยขึ้นหน้าใหม่
ส่งไฟล์ .html ที่ดาวน์โหลดได้จริง พร้อมบอกจำนวนหน้า จำนวนรูป (เวกเตอร์กี่รูป) จำนวนตาราง
ขนาดไฟล์ และสไลด์ที่ไม่ได้นำมาเป็นรูป

โครงไฟล์ (ใช้ตามนี้):

<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ชื่อเรื่อง</title>
<link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@400;700&display=swap" rel="stylesheet">
<style>
:root{ --primary:#0088CC; --primary-dark:#0A6AA1; --accent:#FFB100; --accent-text:#A36B00;
  --ink:#1C2B39; --ink2:#5B6B76; --tint:#EAF6FD; --accent-tint:#FFF1CC; --line:#CFE8F5; }
@page{size:A4;margin:0}
*{box-sizing:border-box}
html{-webkit-print-color-adjust:exact;print-color-adjust:exact}
body{margin:0;background:#E6E9EC;color:var(--ink);font-family:'Sarabun',sans-serif;font-size:11.5pt;line-height:1.8}
.page{width:210mm;height:297mm;margin:8mm auto;padding:10mm 23mm;background:#fff;box-shadow:0 2px 14px rgba(0,0,0,.18);display:flex;flex-direction:column;overflow:hidden}
.page+.page{break-before:page}
.page-head{flex:none;height:13mm;display:flex;justify-content:space-between;gap:8mm;font-size:9pt;color:var(--ink2)}
.page-body{flex:1;min-height:0;overflow:hidden}
.page-foot{flex:none;height:13mm;display:flex;align-items:flex-end;justify-content:center;font-size:9pt;color:var(--ink2)}
.page.overflow{outline:3px solid red}
@media print{body{background:none}.page{margin:0;box-shadow:none}.page.overflow{outline:none}}

h1{font-size:22pt;line-height:1.3;margin:0 0 5mm;padding-bottom:2mm;border-bottom:2pt solid var(--primary)}
h1 small{display:block;font-size:13pt;font-weight:700;color:var(--primary)}
h2{font-size:18pt;line-height:1.3;margin:6mm 0 3mm;padding:1mm 0 1mm 3.5mm;border-left:4pt solid var(--accent)}
h3{font-size:14pt;line-height:1.35;margin:4mm 0 1.5mm;color:var(--primary)}
.page-body>:first-child{margin-top:0}
p{margin:0 0 2.5mm;text-indent:12.7mm;text-align:left}
p.flush{text-indent:0}
ul,ol{margin:0 0 2.5mm;padding-left:12mm}
li{margin-bottom:.8mm}
.choices{margin:0 0 3mm 10mm}
.choices p{text-indent:0;margin:0 0 .8mm}
.note{margin:3mm 0 4mm;padding:3mm 5mm;border-radius:2mm;background:var(--tint)}
.note.accent{background:var(--accent-tint)}
.note p{text-indent:0;margin:0}
.blank{margin:2mm 0 4mm;border:1pt dashed var(--ink2);border-radius:2mm}
figure{margin:3mm 0 4mm;text-align:center}
figure img{display:block;margin:0 auto;max-width:100%;height:auto}
figcaption,.tcap{font-size:10.5pt;text-align:center;text-indent:0}
figcaption{margin-top:1.5mm}
.tbl{margin:3mm 0 4mm}
.tcap{margin:0 0 1.5mm}
table{border-collapse:collapse;margin:0 auto;font-size:10.5pt;line-height:1.4}
th,td{border:.75pt solid var(--line);padding:1.2mm 3mm;text-align:left;vertical-align:middle}
th{background:var(--primary);color:#fff;text-align:center;white-space:nowrap}
tbody td:first-child{background:var(--tint);font-weight:700}
td.c{text-align:center;white-space:nowrap}
sup,sub{line-height:0}
</style>
</head>
<body>
<main id="doc" data-series="ชื่อวิชาหรือชุดเอกสาร" data-title="ชื่อเรื่อง" data-chapter="">
<!-- เนื้อหาทั้งหมดวางที่นี่ ทีละชิ้นเรียงต่อกัน -->
</main>
<script>
/* แบ่งเนื้อหาใน #doc ลงหน้า A4 อัตโนมัติ พร้อมหัวกระดาษ ท้ายกระดาษ และเลขหน้า */
(async function(){
  const doc=document.getElementById('doc'), meta=doc.dataset;
  if(document.fonts&&document.fonts.ready) await document.fonts.ready;
  await Promise.all([...document.images].map(i=>i.complete?0:new Promise(r=>{i.onload=i.onerror=r})));
  let body,n=0;
  const newPage=()=>{
    n++; const pg=document.createElement('section'); pg.className='page';
    pg.innerHTML='<header class="page-head"><span></span><span></span></header><div class="page-body"></div><footer class="page-foot"></footer>';
    pg.querySelector('.page-head').children[0].textContent=meta.series||'';
    pg.querySelector('.page-head').children[1].textContent=meta.title||'';
    pg.querySelector('.page-foot').textContent=(meta.chapter?meta.chapter+' – ':'')+n;
    document.body.insertBefore(pg,doc); body=pg.querySelector('.page-body');
  };
  const over=()=>body.scrollHeight>body.clientHeight+1;
  const sticky=el=>el&&(/^H[1-6]$/.test(el.tagName)||el.classList.contains('keep-next'));
  /* ตัดรายการหรือตารางยาวออกเป็นสองส่วน คืนส่วนที่เหลือ หรือ null ถ้าตัดไม่ได้ */
  const split=el=>{
    let box=null,min=1;
    if(el.tagName==='UL'||el.tagName==='OL') box=el;
    else if(el.classList.contains('tbl')&&el.querySelectorAll('tbody tr').length>12){box=el.querySelector('tbody');min=3;}
    if(!box||box.children.length<=min) return null;
    const rest=el.cloneNode(true), rbox=(box===el)?rest:rest.querySelector('tbody');
    if(box!==el){ /* ตรึงความกว้างคอลัมน์ให้สองส่วนเท่ากัน */
      const a=el.querySelectorAll('thead th'), b=rest.querySelectorAll('thead th');
      a.forEach((th,i)=>{const w=th.getBoundingClientRect().width+'px';th.style.width=w;if(b[i])b[i].style.width=w;});
      const cap=rest.querySelector('.tcap'); if(cap&&!/\(ต่อ\)$/.test(cap.textContent)) cap.append(' (ต่อ)');
    }
    rbox.innerHTML='';
    while(over()&&box.children.length>min) rbox.prepend(box.lastElementChild);
    if(over()||!rbox.children.length){ while(rbox.firstElementChild) box.append(rbox.firstElementChild); return null; }
    if(el.tagName==='OL') rest.start=(el.start||1)+box.children.length;
    return rest;
  };
  const place=el=>{
    if(el.classList.contains('new-page')&&body.children.length) newPage();
    body.appendChild(el);
    if(!over()) return;
    const rest=split(el);
    if(rest){ newPage(); place(rest); return; }
    const carry=[el]; let prev=el.previousElementSibling;
    while(sticky(prev)){ carry.unshift(prev); prev=prev.previousElementSibling; }
    if(carry.length===body.children.length){ body.parentNode.classList.add('overflow'); return; }
    newPage(); carry.forEach(c=>body.appendChild(c));
    if(over()){ const r=split(el); if(r){ newPage(); place(r); } else body.parentNode.classList.add('overflow'); }
  };
  newPage();
  [...doc.children].forEach(place);
  doc.remove();
  document.querySelectorAll('.page-body').forEach(b=>{ if(b.scrollWidth>b.clientWidth+1) b.parentNode.classList.add('overflow'); });
  document.body.dataset.pages=n;
  document.body.dataset.overflow=document.querySelectorAll('.page.overflow').length;
})();
</script>
</body>
</html>
```
