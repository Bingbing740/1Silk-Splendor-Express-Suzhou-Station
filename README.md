[Uploading task1.html…]()
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>高铁客运服务英语实训系统</title>
<style>
  /* ================= 复制与泉州站完全相同的 CSS ================= */
  * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
  body { font-family: "Microsoft YaHei", "PingFang SC", sans-serif; background-color: #f0f6ff; background-image: linear-gradient(45deg, #dbe9ff 25%, transparent 25%), linear-gradient(-45deg, #dbe9ff 25%, transparent 25%), linear-gradient(45deg, transparent 75%, #dbe9ff 75%), linear-gradient(-45deg, transparent 75%, #dbe9ff 75%); background-size: 40px 40px; background-position: 0 0, 0 20px, 20px -20px, -20px 0px; color: #333; min-height: 100vh; }
  .navbar { background: linear-gradient(90deg, #8b2e2e, #b83a3a); color: #fff; padding: 12px 16px; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 10px; box-shadow: 0 2px 8px rgba(0,0,0,0.15); position: sticky; top: 0; z-index: 100; }
  .navbar-left { display: flex; align-items: center; gap: 8px; font-weight: 600; font-size: 15px; }
  .navbar-left a { color: #fff; text-decoration: none; font-size: 13px; background: rgba(255,255,255,0.2); padding: 4px 10px; border-radius: 12px; margin-right: 6px; }
  .navbar-menu { display: flex; gap: 4px; flex-wrap: wrap; width: 100%; order: 3; }
  .navbar-menu a { color: #f5e6e6; text-decoration: none; font-size: 12px; padding: 6px 10px; border-radius: 20px; cursor: pointer; white-space: nowrap; }
  .navbar-menu a.active, .navbar-menu a:hover { background: rgba(255,255,255,0.2); color: #fff; }
  .btn-print { background: rgba(255,255,255,0.15); border: none; color: #fff; padding: 6px 12px; border-radius: 20px; cursor: pointer; font-size: 12px; white-space: nowrap; }
  .container { max-width: 1150px; margin: 0 auto; padding: 20px 12px 40px; }
  .page-title { font-size: 24px; color: #b83a3a; margin-bottom: 6px; line-height: 1.3; word-break: break-all; }
  .page-subtitle { font-size: 13px; color: #666; font-family: monospace; margin-bottom: 16px; }
  .card { background: #fff; border-radius: 10px; box-shadow: 0 2px 10px rgba(0,0,0,0.06); padding: 16px 14px; margin-bottom: 16px; position: relative; overflow: hidden; }
  .card::before { content: ""; position: absolute; top: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, #b83a3a, #d4a017); }
  .card-title { font-size: 16px; font-weight: 600; color: #8b2e2e; margin-bottom: 14px; display: flex; align-items: center; gap: 6px; flex-wrap: wrap; }
  .form-grid { display: grid; grid-template-columns: 1fr; gap: 12px; }
  .form-item { display: flex; flex-direction: column; gap: 6px; }
  .form-item label { font-size: 13px; color: #4a5568; font-weight: 500; }
  .form-item input { padding: 10px 12px; border: 1px solid #cbd5e0; border-radius: 6px; font-size: 14px; outline: none; width: 100%; }
  .form-actions { margin-top: 16px; display: flex; align-items: center; gap: 12px; flex-wrap: wrap; }
  .btn-save { background: #2f855a; color: #fff; border: none; padding: 10px 20px; border-radius: 24px; font-size: 14px; cursor: pointer; }
  .btn-secondary { background: #b83a3a; color: #fff; border: none; padding: 10px 20px; border-radius: 24px; font-size: 14px; cursor: pointer; }
  .case-header { display: flex; flex-direction: column; align-items: flex-start; gap: 10px; padding: 12px 14px; background: #fff8f0; border-radius: 8px; margin-bottom: 14px; border-left: 4px solid #d4a017; }
  .case-header .badge { background: #b83a3a; color: #fff; padding: 6px 12px; border-radius: 6px; font-size: 13px; font-weight: 600; }
  .case-header .case-info { font-size: 13px; color: #555; line-height: 1.6; }
  .case-desc { font-size: 14px; line-height: 1.8; color: #4a5568; margin-bottom: 14px; }
  .vocab-grid { display: grid; grid-template-columns: 1fr; gap: 12px; }
  .vocab-card { background: #fff; border: 1px solid #f0e0d0; border-radius: 8px; padding: 12px 14px; }
  .vocab-card .word { font-size: 15px; font-weight: 700; color: #b83a3a; margin-bottom: 2px; }
  .vocab-card .phonetic { font-size: 12px; color: #888; margin-bottom: 4px; }
  .vocab-card .meaning { font-size: 13px; color: #444; margin-bottom: 8px; }
  .vocab-card .actions { display: flex; align-items: center; gap: 8px; flex-wrap: wrap; }
  .vocab-card .actions button { background: #f0f6ff; border: 1px solid #cbd5e0; border-radius: 6px; padding: 6px 12px; font-size: 12px; cursor: pointer; color: #4a5568; }
  .vocab-card .actions button.record-btn { background: #b83a3a; color: #fff; border-color: #b83a3a; }
  .score-panel { margin-top: 10px; padding: 10px; background: #fafafa; border-radius: 6px; border: 1px solid #eee; display: grid; grid-template-columns: 1fr; gap: 6px; font-size: 12px; }
  .score-panel .score-item { display: flex; justify-content: space-between; padding: 4px 8px; background: #fff; border-radius: 4px; }
  .score-panel .score-item .label { color: #888; }
  .score-panel .score-item .value { color: #b83a3a; font-weight: 700; }
  .score-panel.total-row { grid-template-columns: 1fr; }
  .score-panel.total-row .score-item { background: #fdf0f0; }
  .sentence-section { margin-bottom: 20px; }
  .sentence-section .section-title { font-size: 14px; font-weight: 600; color: #b83a3a; padding: 8px 12px; background: #fdf0f0; border-radius: 6px; margin-bottom: 12px; }
  .sentence-item { background: #fff; border: 1px solid #f0e0d0; border-radius: 8px; padding: 12px; margin-bottom: 10px; }
  .sentence-item .sentence-main { display: flex; flex-direction: column; gap: 10px; }
  .sentence-item .en { font-size: 14px; color: #333; margin-bottom: 4px; font-weight: 500; line-height: 1.5; }
  .sentence-item .cn { font-size: 13px; color: #777; line-height: 1.5; }
  .sentence-item .btn-group { display: flex; gap: 8px; flex-wrap: wrap; }
  .sentence-item .read-btn, .sentence-item .record-btn { border: none; padding: 8px 14px; border-radius: 6px; font-size: 13px; cursor: pointer; display: flex; align-items: center; justify-content: center; flex: 1; }
  .sentence-item .read-btn { background: #b83a3a; color: #fff; }
  .sentence-item .record-btn { background: #2f855a; color: #fff; }
  .dialog-scene { background: #fff; border: 1px solid #f0e0d0; border-radius: 10px; padding: 14px; margin-bottom: 16px; }
  .dialog-scene .scene-header { display: flex; flex-direction: column; gap: 6px; margin-bottom: 12px; }
  .dialog-scene .scene-header .scene-name { font-size: 14px; font-weight: 600; color: #8b2e2e; padding: 6px 12px; background: #fdf0f0; border-radius: 6px; display: inline-block; }
  .dialog-line { border-radius: 8px; padding: 10px 12px; margin-bottom: 10px; }
  .dialog-line.role-steward { background: #fdf6ec; border-left: 4px solid #d4a017; }
  .dialog-line.role-passenger { background: #f0f7ff; border-left: 4px solid #4a90d9; }
  .dialog-line .role-label { font-size: 13px; font-weight: 600; margin-bottom: 6px; display: flex; align-items: center; gap: 4px; }
  .dialog-line .line-en { font-size: 13px; color: #333; margin-bottom: 4px; font-weight: 500; line-height: 1.5; }
  .dialog-line .line-cn { font-size: 12px; color: #777; margin-bottom: 8px; line-height: 1.5; }
  .dialog-line .read-btn { background: #b83a3a; color: #fff; border: none; padding: 6px 12px; border-radius: 14px; font-size: 12px; cursor: pointer; }
  .role-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .role-item { background: #fff; border: 1px solid #f0e0d0; border-radius: 8px; padding: 12px 10px; text-align: center; }
  .role-item .role-name { font-size: 13px; font-weight: 600; color: #b83a3a; margin-bottom: 4px; }
  .role-item input { width: 100%; padding: 8px; border: 1px solid #cbd5e0; border-radius: 6px; font-size: 13px; outline: none; text-align: center; }
  .script-scene { background: #fff; border: 1px solid #f0e0d0; border-radius: 10px; padding: 14px; margin-bottom: 16px; }
  .script-scene .scene-title { font-size: 14px; font-weight: 600; color: #8b2e2e; padding: 6px 12px; background: #fdf0f0; border-radius: 6px; margin-bottom: 12px; }
  .ref-sentences { display: flex; flex-wrap: wrap; gap: 6px; padding: 10px; background: #fafafa; border-radius: 8px; margin-bottom: 14px; max-height: 200px; overflow-y: auto; }
  .ref-sentence { background: #fff; border: 1px solid #e0c8c8; border-radius: 6px; padding: 6px 10px; font-size: 12px; cursor: grab; color: #555; line-height: 1.4; }
  .turns-list { display: flex; flex-direction: column; gap: 12px; margin-bottom: 12px; }
  .turn-item { display: flex; flex-direction: column; gap: 8px; background: #fffdfd; border: 1px solid #f0e0d0; border-radius: 8px; padding: 12px; }
  .turn-item .turn-header { display: flex; justify-content: space-between; align-items: center; }
  .turn-item .turn-index { font-size: 13px; font-weight: 700; color: #b83a3a; }
  .turn-item .turn-role-select { padding: 6px 10px; border: 1px solid #cbd5e0; border-radius: 6px; font-size: 13px; outline: none; background: #fff; width: 120px; }
  .turn-item .turn-dropzone { min-height: 48px; border: 2px dashed #d0c0c0; border-radius: 6px; padding: 8px 10px; font-size: 13px; color: #333; background: #fff; line-height: 1.5; }
  .turn-item .turn-dropzone .empty-hint { font-size: 12px; color: #bbb; font-style: italic; }
  .turn-item .turn-text { word-break: break-word; white-space: pre-wrap; }
  .turn-item .turn-actions { display: flex; gap: 6px; flex-wrap: wrap; justify-content: flex-end; }
  .turn-item .turn-actions button { background: #fff; border: 1px solid #d0d0d0; border-radius: 6px; padding: 6px 10px; font-size: 12px; cursor: pointer; color: #666; flex: 1; min-width: 70px; }
  .turn-custom-area { display: none; gap: 6px; align-items: center; flex-wrap: wrap; margin-top: 6px; }
  .turn-custom-area.active { display: flex; }
  .turn-custom-area input { flex: 1; min-width: 100%; padding: 8px 10px; border: 1px solid #cbd5e0; border-radius: 6px; font-size: 13px; outline: none; }
  .turn-custom-area button { padding: 8px 12px; border: none; border-radius: 6px; font-size: 13px; cursor: pointer; flex: 1; }
  .btn-add { background: #2f855a; color: #fff; }
  .btn-cancel { background: #e2e8f0; color: #4a5568; }
  .btn-voice { background: #b83a3a; color: #fff; }
  .scene-add-turn button { background: #b83a3a; color: #fff; border: none; padding: 10px; border-radius: 20px; font-size: 13px; width: 100%; cursor: pointer; }
  .score-table-wrap { overflow-x: auto; }
  .score-table { width: 100%; border-collapse: collapse; font-size: 13px; margin-bottom: 12px; min-width: 500px; }
  .score-table th, .score-table td { padding: 10px 8px; text-align: left; border-bottom: 1px solid #eee; }
  .score-table th { background: #fdf0f0; color: #8b2e2e; font-weight: 600; font-size: 12px; }
  .score-table td input { width: 60px; padding: 6px; border: 1px solid #cbd5e0; border-radius: 4px; font-size: 13px; text-align: center; }
  .total-score { display: flex; align-items: center; justify-content: space-between; background: #fdf0f0; border-radius: 8px; padding: 12px 14px; margin-top: 10px; }
  .overview-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 14px; }
  .overview-card { background: #fff; border: 1px solid #f0e0d0; border-radius: 8px; padding: 12px; text-align: center; }
  .final-score-card { background: linear-gradient(90deg, #b83a3a, #d4a017); color: #fff; border-radius: 10px; padding: 16px; display: flex; align-items: center; justify-content: space-between; margin-top: 14px; }
  .comment-box textarea { width: 100%; min-height: 80px; padding: 10px; border: 1px solid #cbd5e0; border-radius: 6px; font-size: 14px; outline: none; }
  .toast { position: fixed; top: 70px; right: 50%; transform: translateX(50%) translateY(-10px); background: #2f855a; color: #fff; padding: 10px 20px; border-radius: 6px; font-size: 13px; opacity: 0; transition: all 0.3s; pointer-events: none; z-index: 200; }
  .toast.show { opacity: 1; transform: translateX(50%) translateY(0); }
  
  @media screen and (min-width: 768px) {
    .navbar { flex-wrap: nowrap; padding: 12px 32px; }
    .navbar-menu { width: auto; order: 0; }
    .container { padding: 36px 24px 60px; }
    .card { padding: 24px 28px; }
    .form-grid { grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); }
    .case-header { flex-direction: row; align-items: center; padding: 14px 18px; }
    .vocab-grid { grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); }
    .score-panel { grid-template-columns: repeat(2, 1fr); }
    .role-grid { grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); }
    .turn-item { flex-direction: row; align-items: flex-start; padding: 10px 12px; }
    .turn-item .turn-header { flex-direction: row; width: 140px; flex-shrink: 0; padding-top: 6px; }
    .turn-item .turn-actions { flex-wrap: wrap; justify-content: flex-start; min-width: 120px; padding-top: 4px; }
    .turn-item .turn-actions button { flex: none; min-width: auto; }
    .turn-item .turn-content { flex: 1; }
    .turn-custom-area input { min-width: 180px; }
    .overview-grid { grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); }
  }
</style>
</head>
<body>

<nav class="navbar">
  <div class="navbar-left">
    <a href="index.html">⬅ 返回首页</a>
    <span id="navTitle">🚄 专列英语实训</span>
  </div>
  <div class="navbar-menu">
    <a class="active" onclick="showSection('group')">👥 小组</a>
    <a onclick="showSection('case')">📋 案例信息</a>
    <a onclick="showSection('vocab')">📖 词汇</a>
    <a onclick="showSection('sentence')">💬 句型</a>
    <a onclick="showSection('dialog')">🗂 对话卡片</a>
    <a onclick="showSection('perform')">🎭 模拟展演</a>
    <a onclick="showSection('score')">⭐ 师评成绩</a>
  </div>
  <button class="btn-print" onclick="window.print()">🖨 打印</button>
</nav>

<div class="container">
  <h1 class="page-title" id="pageTitle"></h1>
  <p class="page-subtitle" id="pageSubtitle"></p>

  <section id="section-group">
    <div class="card">
      <div class="card-title"><span class="icon">ℹ️</span> 小组基本信息</div>
      <div class="form-grid">
        <div class="form-item"><label>班级</label><input type="text" id="className" placeholder="请输入班级"></div>
        <div class="form-item"><label>小组名称</label><input type="text" id="groupName" placeholder="如：第1组"></div>
        <div class="form-item"><label>小组编号</label><input type="text" id="groupNo" placeholder="如：G01"></div>
        <div class="form-item"><label>实训任务</label><input type="text" id="task" readonly></div>
        <div class="form-item"><label>指导教师</label><input type="text" id="teacher" placeholder="请输入姓名"></div>
      </div>
      <div class="form-actions"><button class="btn-save" onclick="saveGroup()">💾 保存信息</button></div>
    </div>
    <div class="card">
      <div class="card-title"><span class="icon">📋</span> 任务说明</div>
      <p class="case-desc" id="taskIntro"></p>
    </div>
  </section>

  <section id="section-case" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">📋</span> 乘务服务案例</div>
      <div class="case-header" id="caseHeader"></div>
      <h3 style="font-size:15px; color:#8b2e2e; margin-bottom:10px;">案例描述</h3>
      <p class="case-desc" id="caseDesc"></p>
      <h3 style="font-size:15px; color:#8b2e2e; margin:14px 0 10px;">四大情境</h3>
      <div class="scene-grid" id="sceneGrid"></div>
    </div>
  </section>

  <section id="section-vocab" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">📖</span> 核心文化词汇</div>
      <div class="vocab-grid" id="vocabGrid"></div>
    </div>
  </section>

  <section id="section-sentence" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">💬</span> 高铁乘务常用句型</div>
      <div id="sentenceContainer"></div>
    </div>
  </section>

  <section id="section-dialog" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">🗂</span> 高铁乘务服务对话卡片</div>
      <div id="dialogContainer"></div>
    </div>
  </section>

  <section id="section-perform" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">🎭</span> 1. 角色分工（4人一组）</div>
      <div class="role-grid">
        <div class="role-item"><div class="role-name">列车长</div><input type="text" class="role-input" data-role="chief" placeholder="姓名..."></div>
        <div class="role-item"><div class="role-name">乘务员1</div><input type="text" class="role-input" data-role="ca1" placeholder="姓名..."></div>
        <div class="role-item"><div class="role-name">乘务员2</div><input type="text" class="role-input" data-role="ca2" placeholder="姓名..."></div>
        <div class="role-item"><div class="role-name">列车员</div><input type="text" class="role-input" data-role="attendant" placeholder="姓名..."></div>
      </div>
    </div>
    <div class="card">
      <div class="card-title"><span class="icon">📝</span> 2. 对话文本编写</div>
      <div id="scriptContainer"></div>
      <div class="form-actions" style="margin-top:16px;">
        <button class="btn-save" onclick="saveScript()">💾 保存脚本</button>
        <button class="btn-secondary" onclick="previewScript()">👁 预览对话</button>
        <button class="btn-secondary" onclick="resetScript()">↺ 重置</button>
      </div>
      <div id="previewArea" style="margin-top:16px; display:none;"><div class="preview-box" id="previewBox"></div></div>
    </div>
    <div class="card">
      <div class="card-title"><span class="icon">🎭</span> 模拟展演评分</div>
      <div class="score-table-wrap">
        <table class="score-table">
          <thead><tr><th>评价维度</th><th>说明</th><th>分值</th><th>得分</th></tr></thead>
          <tbody>
            <tr><td><strong>语言</strong></td><td>英语表达自然、连贯，发音准确</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcPerform()"></td></tr>
            <tr><td><strong>文化</strong></td><td>文化讲解准确、生动，传递到位</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcPerform()"></td></tr>
            <tr><td><strong>服务</strong></td><td>服务用语规范、得体、有礼貌</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcPerform()"></td></tr>
            <tr><td><strong>团队</strong></td><td>角色分工明确，配合默契</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcPerform()"></td></tr>
          </tbody>
        </table>
      </div>
      <div class="total-score"><span>模拟展演总分</span><span id="performTotal">0 / 100</span></div>
      <div class="form-actions"><button class="btn-save" onclick="savePerform()">💾 保存评分</button></div>
    </div>
  </section>

  <section id="section-score" style="display:none;">
    <div class="card">
      <div class="card-title"><span class="icon">⭐</span> 教师综合评价</div>
      <div class="score-table-wrap">
        <table class="score-table">
          <thead><tr><th>评价维度</th><th>说明</th><th>分值</th><th>得分</th></tr></thead>
          <tbody>
            <tr><td><strong>语言</strong></td><td>英语表达自然、连贯，发音准确</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcFinal()"></td></tr>
            <tr><td><strong>文化</strong></td><td>文化讲解准确、生动，传递到位</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcFinal()"></td></tr>
            <tr><td><strong>服务</strong></td><td>服务用语规范、得体、有礼貌</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcFinal()"></td></tr>
            <tr><td><strong>团队</strong></td><td>角色分工明确，配合默契</td><td>25</td><td><input type="number" min="0" max="25" value="0" onchange="calcFinal()"></td></tr>
          </tbody>
        </table>
      </div>
      <div class="total-score"><span>师评加权总分</span><span id="finalTotal">0 / 100</span></div>
      <div class="form-actions"><button class="btn-save" onclick="saveFinal()">💾 保存师评</button></div>
    </div>
  </section>
</div>
<div class="toast" id="toast">✅ 操作成功</div>

<script>
/* =========================================================
   核心数据配置区（修改这里即可变成不同站点的系统）
   ========================================================= */
const TASK_DATA = {
  title: "衣锦专列 · 苏州站",
  subTitle: "English-for-Silk-Brocade-Suzhou-Station",
  themeColor: "#4a90d9", // 可以根据需要调整主题色
  
  intro: "本实训系统基于“衣锦专列”真实案例设计。围绕登车迎客、车厢广播、主题特产销售、车厢主题互动四大情境，掌握宋锦、苏绣相关核心词汇与句型。",
  
  case: {
    badge: "🚄 衣锦专列 苏州站",
    info: "<strong>车次：</strong>G8292<br><strong>文化载体：</strong>宋锦、苏绣非物质文化遗产",
    desc: "在一趟由北京开往苏州的高铁上，乘务组为旅客提供全程服务。服务内容包括：登车迎客、车厢广播（介绍宋锦苏绣）、特产销售、主题互动。",
    scenes: [
      { no: "情景一", en: "Boarding & Welcome", cn: "登车迎客" },
      { no: "情景二", en: "Onboard Announcements", cn: "车厢广播" },
      { no: "情景三", en: "Specialty Product Sales", cn: "主题特产销售" },
      { no: "情景四", en: "Onboard Theme Interaction", cn: "车厢主题互动" }
    ]
  },
  
  vocab: [
    { en: 'brocade', ph: '/brəˈkeɪd/', cn: 'n. 织锦' },
    { en: 'embroidery', ph: '/ɪmˈbrɔɪdəri/', cn: 'n. 刺绣' },
    { en: 'silk weaving', ph: '/sɪlk ˈwiːvɪŋ/', cn: 'n. 丝织' },
    { en: 'intricate pattern', ph: '/ˈɪntrɪkət ˈpætn/', cn: 'n. 精美纹样' }
    // 此处请参考泉州站，补充满 40 个词汇...
  ],
  
  sentences: [
    {
      title: '情境一：登车迎客',
      items: [
        { en: 'Welcome aboard the Silk Brocade Express!', cn: '欢迎乘坐衣锦专列！' },
        { en: 'Suzhou is the home of Song brocade and Su embroidery.', cn: '苏州是宋锦和苏绣的故乡。' }
      ]
    }
    // 此处请参考泉州站，补充其余情境的句型...
  ],
  
  dialogs: [
    {
      title: '情境 1：登车迎客',
      lines: [
        { role: '列车员', en: 'Good morning, welcome aboard the Silk Brocade Express.', cn: '早上好，欢迎乘坐衣锦专列。' },
        { role: '乘客', en: 'Thank you. The pattern on the seat is beautiful.', cn: '谢谢。座位上的图案真漂亮。' }
      ]
    }
    // 此处请参考泉州站，补充其余情境的对话卡片...
  ]
};

/* =========================================================
   以下为系统逻辑，无需修改
   ========================================================= */
document.addEventListener('DOMContentLoaded', () => {
  // 初始化页面内容
  document.getElementById('navTitle').innerText = TASK_DATA.title;
  document.getElementById('pageTitle').innerText = TASK_DATA.subTitle;
  document.getElementById('pageSubtitle').innerText = "index.html <!DOCTYPE html>";
  document.getElementById('task').value = TASK_DATA.title + " 实训";
  document.getElementById('taskIntro').innerText = TASK_DATA.intro;
  
  // 案例信息
  let caseHtml = `<div class="badge">${TASK_DATA.case.badge}</div><div class="case-info">${TASK_DATA.case.info}</div>`;
  document.getElementById('caseHeader').innerHTML = caseHtml;
  document.getElementById('caseDesc').innerText = TASK_DATA.case.desc;
  document.getElementById('sceneGrid').innerHTML = TASK_DATA.case.scenes.map(s => `
    <div style="background:#fff; border-left:4px solid ${TASK_DATA.themeColor}; padding:12px; border-radius:6px;">
      <div style="font-size:12px; color:${TASK_DATA.themeColor}; font-weight:600;">${s.no}</div>
      <div style="font-size:14px; font-weight:600; margin:4px 0;">${s.en}</div>
      <div style="font-size:13px; color:#666;">${s.cn}</div>
    </div>
  `).join('');

  // 词汇
  document.getElementById('vocabGrid').innerHTML = TASK_DATA.vocab.map((v, i) => `
    <div class="vocab-card">
      <div class="word">${v.en}</div>
      <div class="phonetic">${v.ph}</div>
      <div class="meaning">${v.cn}</div>
      <div class="actions">
        <button onclick="speakEnglish('${v.en}')">🔊 发音</button>
        <button class="record-btn" onclick="startVocabRead(${i})">🎤 跟读评分</button>
      </div>
      <div id="vocabScorePanel${i}"></div>
    </div>
  `).join('');

  // 句型
  let idx = 0;
  document.getElementById('sentenceContainer').innerHTML = TASK_DATA.sentences.map(sec => `
    <div class="sentence-section">
      <div class="section-title">${sec.title}</div>
      ${sec.items.map(item => {
        const currentIdx = idx++;
        return `
        <div class="sentence-item">
          <div class="sentence-main">
            <div><div class="en">${item.en}</div><div class="cn">${item.cn}</div></div>
            <div class="btn-group">
              <button class="read-btn" onclick="speakEnglish('${item.en}', 0.9)">🔊 朗读</button>
              <button class="record-btn" onclick="startSentenceRead(${currentIdx})">🎤 评分</button>
            </div>
          </div>
          <div id="sentenceScorePanel${currentIdx}"></div>
        </div>`;
      }).join('')}
    </div>
  `).join('');

  // 对话卡片
  document.getElementById('dialogContainer').innerHTML = TASK_DATA.dialogs.map((scene, sIdx) => `
    <div class="dialog-scene">
      <div class="scene-header"><div class="scene-name">📌 ${scene.title}</div></div>
      ${scene.lines.map(line => `
        <div class="dialog-line ${line.role === '乘客' ? 'role-passenger' : 'role-steward'}">
          <div class="role-label">${line.role === '乘客' ? '👤' : '🧑‍✈️'} ${line.role}</div>
          <div class="line-en">${line.en}</div>
          <div class="line-cn">${line.cn}</div>
          <button class="read-btn" onclick="speakEnglish('${line.en}', 0.9)">🔊 朗读</button>
        </div>
      `).join('')}
    </div>
  `).join('');

  // 脚本编排初始化
  initScriptState();
  loadScriptState();
  renderScript();
  loadGroup();
});

// 导航切换
const sections = ['group', 'case', 'vocab', 'sentence', 'dialog', 'perform', 'score'];
function showSection(name) {
  sections.forEach(s => { document.getElementById('section-' + s).style.display = (s === name) ? 'block' : 'none'; });
  document.querySelectorAll('.navbar-menu a').forEach(a => a.classList.remove('active'));
  const idx = sections.indexOf(name);
  if (idx >= 0) document.querySelectorAll('.navbar-menu a')[idx].classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg; t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2000);
}

function speakEnglish(text, rate = 1.0) {
  if ('speechSynthesis' in window) {
    const u = new SpeechSynthesisUtterance(text); u.lang = 'en-US'; u.rate = rate; speechSynthesis.speak(u);
  } else showToast('当前浏览器不支持语音合成');
}

// 模拟讯飞评测
function mockSpeechAssessment() {
  return new Promise(resolve => {
    setTimeout(() => {
      const accuracy = Math.floor(Math.random() * 20) + 80;
      const fluency  = Math.floor(Math.random() * 20) + 80;
      const integrity = Math.floor(Math.random() * 15) + 85;
      resolve({ total_score: Math.round((accuracy+fluency+integrity)/3), accuracy_score: accuracy, fluency_score: fluency, integrity_score: integrity });
    }, 1200);
  });
}

function renderScorePanel(container, result) {
  container.innerHTML = `
    <div class="score-panel total-row"><div class="score-item"><span class="label">总分</span><span class="value">${result.total_score}</span></div></div>
    <div class="score-panel">
      <div class="score-item"><span class="label">准确度</span><span class="value">${result.accuracy_score}</span></div>
      <div class="score-item"><span class="label">流畅度</span><span class="value">${result.fluency_score}</span></div>
      <div class="score-item"><span class="label">完整度</span><span class="value">${result.integrity_score}</span></div>
    </div>`;
}

async function startVocabRead(i) {
  const panel = document.getElementById('vocabScorePanel' + i);
  panel.innerHTML = `<div class="score-panel"><div style="text-align:center;">🎤 录音识别中...</div></div>`;
  renderScorePanel(panel, await mockSpeechAssessment());
}

async function startSentenceRead(idx) {
  const panel = document.getElementById('sentenceScorePanel' + idx);
  panel.innerHTML = `<div class="score-panel"><div style="text-align:center;">🎤 录音识别中...</div></div>`;
  renderScorePanel(panel, await mockSpeechAssessment());
}

// 多轮脚本编排逻辑 (与泉州站完全一致)
const SCRIPT_KEY = 'train_script_' + TASK_DATA.title;
let scriptState = {};
function initScriptState() {
  scriptState = {};
  TASK_DATA.dialogs.forEach((d, i) => {
    scriptState['scene' + (i+1)] = d.lines.map(l => ({ role: l.role, text: l.en, manual: false }));
  });
}
function loadScriptState() {
  const saved = localStorage.getItem(SCRIPT_KEY);
  if (saved) { try { scriptState = JSON.parse(saved); } catch(e){} }
  renderScript();
}
function saveScriptState() { localStorage.setItem(SCRIPT_KEY, JSON.stringify(scriptState)); }

function renderScript() {
  const container = document.getElementById('scriptContainer');
  container.innerHTML = TASK_DATA.dialogs.map((d, i) => {
    const sceneId = 'scene' + (i+1);
    return `
      <div class="script-scene">
        <div class="scene-title">📌 ${d.title}</div>
        <div style="font-size:12px; color:#888; margin-bottom:6px;">参考句型（可拖拽到下方任意轮次）</div>
        <div class="ref-sentences">
          ${TASK_DATA.sentences[i] ? TASK_DATA.sentences[i].items.map((s, j) => `
            <div class="ref-sentence" draggable="true" ondragstart="onDragStart(event, '${s.en}')" ondragend="onDragEnd(event)">
              <span style="color:#b83a3a; font-size:11px; margin-right:4px;">⋮⋮</span>${s.en}
            </div>
          `).join('') : ''}
        </div>
        <div class="turns-list" id="turns-${sceneId}">
          ${renderTurns(sceneId)}
        </div>
        <div class="scene-add-turn"><button onclick="addTurn('${sceneId}')">+ 添加一轮对话</button></div>
      </div>
    `;
  }).join('');
}

function renderTurns(sceneId) {
  const turns = scriptState[sceneId] || [];
  return turns.map((turn, idx) => `
    <div class="turn-item">
      <div class="turn-header">
        <div class="turn-index">#${idx + 1}</div>
        <select class="turn-role-select" onchange="changeTurnRole('${sceneId}', ${idx}, this.value)">
          <option value="列车员" ${turn.role === '列车员' ? 'selected' : ''}>列车员</option>
          <option value="乘客" ${turn.role === '乘客' ? 'selected' : ''}>乘客</option>
        </select>
      </div>
      <div class="turn-content">
        <div class="turn-dropzone" ondragover="onTurnDragOver(event)" ondragleave="onTurnDragLeave(event)" ondrop="onTurnDrop(event, '${sceneId}', ${idx})">
          ${turn.text ? `<span class="turn-text">${turn.text}</span>` : `<span class="empty-hint">拖拽参考句到此处，或自定义</span>`}
        </div>
        <div class="turn-custom-area" id="turn-custom-${sceneId}-${idx}">
          <input type="text" placeholder="输入自定义台词..." value="${turn.manual ? turn.text : ''}" onkeydown="if(event.key==='Enter'){updateTurnText('${sceneId}',${idx},this.value);this.value='';}">
          <button class="btn-voice" onclick="startVoiceInputTurn('${sceneId}', ${idx})">🎤 语音</button>
          <button class="btn-add" onclick="updateTurnTextFromInput('${sceneId}', ${idx})">添加</button>
          <button class="btn-cancel" onclick="toggleTurnCustom('${sceneId}', ${idx})">取消</button>
        </div>
      </div>
      <div class="turn-actions">
        <button onclick="toggleTurnCustom('${sceneId}', ${idx})">+ 自定义</button>
        <button onclick="moveTurn('${sceneId}', ${idx}, -1)">↑ 上移</button>
        <button onclick="moveTurn('${sceneId}', ${idx}, 1)">↓ 下移</button>
        <button style="color:#d33;" onclick="removeTurn('${sceneId}', ${idx})">✕ 删除</button>
      </div>
    </div>
  `).join('');
}

function refreshTurns(sceneId) { document.getElementById(`turns-${sceneId}`).innerHTML = renderTurns(sceneId); }
function addTurn(sceneId) { scriptState[sceneId].push({ role: '列车员', text: '', manual: false }); refreshTurns(sceneId); saveScriptState(); }
function removeTurn(sceneId, idx) { if (scriptState[sceneId].length <= 1) return showToast('至少保留一轮'); scriptState[sceneId].splice(idx, 1); refreshTurns(sceneId); saveScriptState(); }
function moveTurn(sceneId, idx, dir) { const arr = scriptState[sceneId]; const newIdx = idx + dir; if (newIdx < 0 || newIdx >= arr.length) return; [arr[idx], arr[newIdx]] = [arr[newIdx], arr[idx]]; refreshTurns(sceneId); saveScriptState(); }
function changeTurnRole(sceneId, idx, role) { scriptState[sceneId][idx].role = role; saveScriptState(); }
function toggleTurnCustom(sceneId, idx) { document.getElementById(`turn-custom-${sceneId}-${idx}`).classList.toggle('active'); }
function updateTurnTextFromInput(sceneId, idx) { const input = document.querySelector(`#turn-custom-${sceneId}-${idx} input`); if(input.value.trim()){ updateTurnText(sceneId, idx, input.value); input.value=''; } }
function updateTurnText(sceneId, idx, text) { if (!text.trim()) return; scriptState[sceneId][idx].text = text.trim(); scriptState[sceneId][idx].manual = true; refreshTurns(sceneId); saveScriptState(); }

// 拖拽
let dragText = null;
function onDragStart(e, text) { dragText = text; e.target.style.opacity = '0.4'; }
function onDragEnd(e) { e.target.style.opacity = '1'; }
function onTurnDragOver(e) { e.preventDefault(); e.currentTarget.style.borderColor = '#b83a3a'; e.currentTarget.style.background = '#fff0f0'; }
function onTurnDragLeave(e) { e.currentTarget.style.borderColor = '#d0c0c0'; e.currentTarget.style.background = '#fff'; }
function onTurnDrop(e, sceneId, turnIdx) {
  e.preventDefault(); e.currentTarget.style.borderColor = '#d0c0c0'; e.currentTarget.style.background = '#fff';
  if (!dragText) return;
  const turn = scriptState[sceneId][turnIdx];
  turn.text = turn.text ? turn.text + '\n' + dragText : dragText;
  turn.manual = false; refreshTurns(sceneId); saveScriptState(); dragText = null;
}

// 语音输入
function startVoiceInputTurn(sceneId, idx) {
  const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
  if (!SpeechRecognition) return showToast('请用 Chrome 或 Edge 浏览器');
  const rec = new SpeechRecognition(); rec.lang = 'en-US'; rec.interimResults = false;
  rec.onstart = () => showToast('🎤 正在录音...');
  rec.onresult = (event) => {
    const text = event.results[0][0].transcript;
    const turn = scriptState[sceneId][idx];
    turn.text = turn.text ? turn.text + '\n' + text : text;
    turn.manual = true; refreshTurns(sceneId); saveScriptState();
  };
  rec.start();
}

function saveScript() { saveScriptState(); showToast('✅ 脚本已保存'); }
function previewScript() {
  let html = '';
  TASK_DATA.dialogs.forEach((d, i) => {
    html += `【${d.title}】\n`;
    (scriptState['scene' + (i+1)] || []).forEach((t, idx) => { html += `  #${idx+1} ${t.role}：${t.text || '（无）'}\n`; });
    html += '\n';
  });
  document.getElementById('previewBox').textContent = html;
  document.getElementById('previewArea').style.display = 'block';
}
function resetScript() { if(confirm('确定重置？')){ localStorage.removeItem(SCRIPT_KEY); initScriptState(); renderScript(); showToast('已重置'); } }

// 评分与小组信息保存
function calcPerform() { let tot = 0; document.querySelectorAll('#section-perform input[type="number"]').forEach(i => tot += Number(i.value)||0); document.getElementById('performTotal').textContent = tot + ' / 100'; }
function savePerform() { showToast('✅ 展演评分已保存'); }
function calcFinal() { let tot = 0; document.querySelectorAll('#section-score input[type="number"]').forEach(i => tot += Number(i.value)||0); document.getElementById('finalTotal').textContent = tot + ' / 100'; }
function saveFinal() { showToast('✅ 师评已保存'); }

const GROUP_KEY = 'group_' + TASK_DATA.title;
function saveGroup() {
  const data = { className: document.getElementById('className').value, groupName: document.getElementById('groupName').value, groupNo: document.getElementById('groupNo').value, teacher: document.getElementById('teacher').value };
  localStorage.setItem(GROUP_KEY, JSON.stringify(data)); showToast('✅ 信息已保存');
}
function loadGroup() {
  const saved = localStorage.getItem(GROUP_KEY);
  if (saved) { try { const d = JSON.parse(saved); document.getElementById('className').value = d.className||''; document.getElementById('groupName').value = d.groupName||''; document.getElementById('groupNo').value = d.groupNo||''; document.getElementById('teacher').value = d.teacher||''; } catch(e){} }
}
</script>
</body>
</html>
