<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>เกมแต่งกลอนสุภาพ ม.1</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Sarabun", sans-serif;
    }

    body {
      background: linear-gradient(135deg, #fff7ed, #fde68a);
      min-height: 100vh;
      padding: 20px;
      color: #3f3f46;
    }

    .container {
      max-width: 1200px;
      margin: auto;
      display: grid;
      grid-template-columns: 1fr 380px;
      gap: 24px;
    }

    .card {
      background: white;
      border-radius: 24px;
      padding: 24px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
    }

    h1 {
      color: #b45309;
      margin-bottom: 12px;
      font-size: 2.2rem;
    }

    h2 {
      color: #92400e;
      margin-bottom: 12px;
    }

    .subtitle {
      margin-bottom: 24px;
      line-height: 1.7;
    }

    .goal-box {
      background: #fef3c7;
      padding: 18px;
      border-radius: 18px;
      margin-bottom: 20px;
      border-left: 8px solid #f59e0b;
    }

    .poem-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      margin-top: 20px;
    }

    .line-box {
      background: #fafaf9;
      border: 2px dashed #d6d3d1;
      border-radius: 18px;
      padding: 18px;
      transition: 0.3s;
    }

    .line-box.correct {
      border-color: #22c55e;
      background: #f0fdf4;
    }

    .line-box.wrong {
      border-color: #ef4444;
      background: #fef2f2;
    }

    .line-title {
      font-weight: bold;
      margin-bottom: 10px;
      color: #78350f;
    }

    textarea {
      width: 100%;
      min-height: 90px;
      border-radius: 12px;
      border: 1px solid #d4d4d8;
      padding: 12px;
      resize: none;
      font-size: 1rem;
      margin-bottom: 10px;
    }

    .count {
      font-size: 0.95rem;
      color: #78716c;
    }

    .buttons {
      margin-top: 24px;
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    button {
      border: none;
      padding: 14px 22px;
      border-radius: 14px;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.2s;
      font-weight: bold;
    }

    .primary {
      background: #f59e0b;
      color: white;
    }

    .primary:hover {
      background: #d97706;
    }

    .secondary {
      background: #e7e5e4;
    }

    .secondary:hover {
      background: #d6d3d1;
    }

    .score-box {
      text-align: center;
      padding: 20px;
      background: linear-gradient(135deg, #fef3c7, #fde68a);
      border-radius: 20px;
      margin-bottom: 20px;
    }

    .score {
      font-size: 3rem;
      color: #b45309;
      font-weight: bold;
    }

    .rules ul {
      padding-left: 22px;
      line-height: 1.9;
    }

    .feedback {
      margin-top: 18px;
      padding: 16px;
      border-radius: 16px;
      background: #f5f5f4;
      line-height: 1.7;
      white-space: pre-line;
    }

    .example {
      margin-top: 20px;
      background: #fffbeb;
      padding: 16px;
      border-radius: 16px;
      line-height: 2;
    }

    .badge {
      display: inline-block;
      background: #f59e0b;
      color: white;
      padding: 6px 14px;
      border-radius: 999px;
      margin-bottom: 14px;
      font-size: 0.9rem;
    }

    .footer {
      margin-top: 20px;
      text-align: center;
      color: #78716c;
      font-size: 0.9rem;
    }

    @media (max-width: 900px) {
      .container {
        grid-template-columns: 1fr;
      }

      .poem-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <div class="container">

    <div class="card">
      <div class="badge">เกมการเรียนรู้ภาษาไทย ม.1</div>
      <h1>เกมแต่งกลอนสุภาพ</h1>

      <p class="subtitle">
        ฝึกแต่งคำประพันธ์ประเภท <strong>กลอนสุภาพ</strong>
        โดยเน้นการตรวจสอบข้อบังคับด้านฉันทลักษณ์
        เช่น จำนวนคำ สัมผัสนอก และรูปแบบกลอน
      </p>

      <div class="goal-box">
        <strong>ภารกิจ:</strong>
        แต่งกลอนสุภาพ 1 บท (4 วรรค)
        ให้ถูกต้องตามหลักฉันทลักษณ์
      </div>

      <div class="poem-grid">

        <div class="line-box" id="box1">
          <div class="line-title">วรรคที่ 1</div>
          <textarea id="line1" placeholder="พิมพ์วรรคที่ 1"></textarea>
          <div class="count" id="count1">จำนวนคำ: 0</div>
        </div>

        <div class="line-box" id="box2">
          <div class="line-title">วรรคที่ 2</div>
          <textarea id="line2" placeholder="พิมพ์วรรคที่ 2"></textarea>
          <div class="count" id="count2">จำนวนคำ: 0</div>
        </div>

        <div class="line-box" id="box3">
          <div class="line-title">วรรคที่ 3</div>
          <textarea id="line3" placeholder="พิมพ์วรรคที่ 3"></textarea>
          <div class="count" id="count3">จำนวนคำ: 0</div>
        </div>

        <div class="line-box" id="box4">
          <div class="line-title">วรรคที่ 4</div>
          <textarea id="line4" placeholder="พิมพ์วรรคที่ 4"></textarea>
          <div class="count" id="count4">จำนวนคำ: 0</div>
        </div>
      </div>

      <div class="buttons">
        <button class="primary" onclick="checkPoem()">ตรวจฉันทลักษณ์</button>
        <button class="secondary" onclick="resetGame()">เริ่มใหม่</button>
        <button class="secondary" onclick="fillExample()">ตัวอย่างกลอน</button>
      </div>

      <div class="feedback" id="feedback">
        ระบบจะตรวจสอบ:
        • จำนวนคำในแต่ละวรรค
        • การเชื่อมสัมผัสระหว่างวรรค
        • ความครบถ้วนของกลอนสุภาพ
      </div>
    </div>

    <div class="card">
      <div class="score-box">
        <div>คะแนนรวม</div>
        <div class="score" id="score">0</div>
        <div>/ 100 คะแนน</div>
      </div>

      <div class="rules">
        <h2>หลักการแต่งกลอนสุภาพ</h2>

        <ul>
          <li>1 บท มี 4 วรรค</li>
          <li>แต่ละวรรคควรมีประมาณ 7-9 คำ</li>
          <li>คำสุดท้ายของวรรคที่ 1 สัมผัสกับคำที่ 3 หรือ 5 ของวรรคที่ 2</li>
          <li>คำสุดท้ายของวรรคที่ 2 สัมผัสกับคำสุดท้ายของวรรคที่ 3</li>
          <li>คำสุดท้ายของวรรคที่ 3 สัมผัสกับคำที่ 3 หรือ 5 ของวรรคที่ 4</li>
        </ul>
      </div>

      <div class="example">
        <h2>ตัวอย่างกลอนสุภาพ</h2>
        ฟ้าอรุณอุ่นแสงแห่งความฝัน<br>
        เด็กมุ่งมั่นเรียนรู้สู่จุดหมาย<br>
        ใช้ความเพียรสร้างตนจนใจกาย<br>
        พร้อมก้าวไปด้วยหวังพลังดี
      </div>

      <div class="footer">
        วิชาภาษาไทย : การแต่งคำประพันธ์ ระดับชั้นมัธยมศึกษาปีที่ 1
      </div>
    </div>

  </div>

  <script>
    const textareas = document.querySelectorAll('textarea');

    textareas.forEach((textarea, index) => {
      textarea.addEventListener('input', () => {
        updateWordCount(index + 1);
      });
    });

    function getWords(text) {
      return text
        .trim()
        .split(/\s+/)
        .filter(word => word.length > 0);
    }

    function updateWordCount(lineNumber) {
      const text = document.getElementById(`line${lineNumber}`).value;
      const count = getWords(text).length;
      document.getElementById(`count${lineNumber}`).innerText = `จำนวนคำ: ${count}`;
    }

    function lastWord(text) {
      const words = getWords(text);
      return words[words.length - 1] || "";
    }

    function getWordAt(text, positions) {
      const words = getWords(text);

      for (let pos of positions) {
        if (words[pos]) return words[pos];
      }

      return "";
    }

    function checkRhyme(word1, word2) {
      if (!word1 || !word2) return false;

      const end1 = word1.slice(-2);
      const end2 = word2.slice(-2);

      return end1 === end2;
    }

    function checkPoem() {
      let score = 0;
      let feedback = "ผลการตรวจฉันทลักษณ์\n\n";

      const lines = [
        document.getElementById('line1').value,
        document.getElementById('line2').value,
        document.getElementById('line3').value,
        document.getElementById('line4').value
      ];

      document.querySelectorAll('.line-box').forEach(box => {
        box.classList.remove('correct', 'wrong');
      });

      // ตรวจจำนวนคำ
      lines.forEach((line, index) => {
        const words = getWords(line);
        const box = document.getElementById(`box${index + 1}`);

        if (words.length >= 7 && words.length <= 9) {
          score += 15;
          feedback += `✅ วรรคที่ ${index + 1} จำนวนคำเหมาะสม (${words.length} คำ)\n`;
          box.classList.add('correct');
        } else {
          feedback += `❌ วรรคที่ ${index + 1} ควรมี 7-9 คำ (ปัจจุบัน ${words.length} คำ)\n`;
          box.classList.add('wrong');
        }
      });

      // ตรวจสัมผัส
      const rhyme1 = checkRhyme(
        lastWord(lines[0]),
        getWordAt(lines[1], [2,4])
      );

      const rhyme2 = checkRhyme(
        lastWord(lines[1]),
        lastWord(lines[2])
      );

      const rhyme3 = checkRhyme(
        lastWord(lines[2]),
        getWordAt(lines[3], [2,4])
      );

      if (rhyme1) {
        score += 15;
        feedback += "\n✅ สัมผัสระหว่างวรรคที่ 1 และ 2 ถูกต้อง";
      } else {
        feedback += "\n❌ สัมผัสระหว่างวรรคที่ 1 และ 2 ยังไม่ถูกต้อง";
      }

      if (rhyme2) {
        score += 15;
        feedback += "\n✅ สัมผัสระหว่างวรรคที่ 2 และ 3 ถูกต้อง";
      } else {
        feedback += "\n❌ สัมผัสระหว่างวรรคที่ 2 และ 3 ยังไม่ถูกต้อง";
      }

      if (rhyme3) {
        score += 15;
        feedback += "\n✅ สัมผัสระหว่างวรรคที่ 3 และ 4 ถูกต้อง";
      } else {
        feedback += "\n❌ สัมผัสระหว่างวรรคที่ 3 และ 4 ยังไม่ถูกต้อง";
      }

      // โบนัส
      if (score >= 85) {
        feedback += "\n\n🏆 ยอดเยี่ยม! กลอนของคุณมีรูปแบบใกล้เคียงกลอนสุภาพมาก";
      } else if (score >= 60) {
        feedback += "\n\n🌟 ดีมาก! ลองปรับสัมผัสอีกเล็กน้อย";
      } else {
        feedback += "\n\n📘 ลองตรวจจำนวนคำและสัมผัสอีกครั้ง";
      }

      document.getElementById('score').innerText = score;
      document.getElementById('feedback').innerText = feedback;
    }

    function resetGame() {
      textareas.forEach((textarea, index) => {
        textarea.value = '';
        updateWordCount(index + 1);
      });

      document.getElementById('score').innerText = '0';

      document.querySelectorAll('.line-box').forEach(box => {
        box.classList.remove('correct', 'wrong');
      });

      document.getElementById('feedback').innerText = `ระบบจะตรวจสอบ:
• จำนวนคำในแต่ละวรรค
• การเชื่อมสัมผัสระหว่างวรรค
• ความครบถ้วนของกลอนสุภาพ`;
    }

    function fillExample() {
      document.getElementById('line1').value = 'ฟ้าอรุณอุ่นแสงแห่งความฝัน';
      document.getElementById('line2').value = 'เด็กมุ่งมั่นเรียนรู้สู่จุดหมาย';
      document.getElementById('line3').value = 'ใช้ความเพียรสร้างตนจนใจกาย';
      document.getElementById('line4').value = 'พร้อมก้าวไปด้วยหวังพลังดี';

      updateWordCount(1);
      updateWordCount(2);
      updateWordCount(3);
      updateWordCount(4);
    }
  </script>
</body>
</html>
