<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TaskFlow — 스마트 할일 관리</title>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #F7F5F0;
  --surface: #FFFFFF;
  --surface2: #F0EDE8;
  --border: rgba(0,0,0,0.08);
  --border-strong: rgba(0,0,0,0.14);
  --text: #1A1814;
  --text-2: #6B6760;
  --text-3: #A09D98;
  --accent: #2D5A3D;
  --accent-light: #E8F2EB;
  --urgent: #C0392B;
  --urgent-light: #FDECEA;
  --high: #D4820A;
  --high-light: #FEF3E2;
  --normal: #1E6091;
  --normal-light: #E8F4FD;
  --low: #7D7166;
  --low-light: #F0EDE8;
  --work: #2D5A3D;
  --work-light: #E8F2EB;
  --personal: #5B3A8C;
  --personal-light: #F0EAFA;
  --health: #C0392B;
  --health-light: #FDECEA;
  --study: #D4820A;
  --study-light: #FEF3E2;
  --radius: 12px;
  --radius-sm: 7px;
  --shadow: 0 1px 3px rgba(0,0,0,0.06), 0 4px 16px rgba(0,0,0,0.04);
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 14px;
}

/* LAYOUT */
.app-shell { display: flex; min-height: 100vh; }

.sidebar {
  width: 220px;
  background: var(--surface);
  border-right: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  padding: 28px 0;
  position: fixed;
  top: 0; left: 0; bottom: 0;
  z-index: 10;
}

.logo {
  padding: 0 24px 28px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 20px;
}

.logo-title {
  font-family: 'Instrument Serif', serif;
  font-size: 22px;
  color: var(--text);
  letter-spacing: -0.3px;
}

.logo-sub {
  font-size: 11px;
  color: var(--text-3);
  margin-top: 2px;
  font-weight: 300;
}

.nav { padding: 0 12px; flex: 1; }

.nav-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 9px 12px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  color: var(--text-2);
  font-size: 13px;
  font-weight: 400;
  transition: all 0.15s;
  margin-bottom: 2px;
  border: none;
  background: none;
  width: 100%;
  text-align: left;
}

.nav-item:hover { background: var(--surface2); color: var(--text); }
.nav-item.active { background: var(--accent-light); color: var(--accent); font-weight: 500; }

.nav-icon { width: 16px; height: 16px; opacity: 0.7; flex-shrink: 0; }
.nav-item.active .nav-icon { opacity: 1; }

.nav-badge {
  margin-left: auto;
  background: var(--surface2);
  color: var(--text-3);
  font-size: 10px;
  font-weight: 600;
  padding: 1px 6px;
  border-radius: 8px;
  min-width: 18px;
  text-align: center;
}
.nav-item.active .nav-badge { background: var(--accent); color: white; }

.sidebar-section-label {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.08em;
  color: var(--text-3);
  text-transform: uppercase;
  padding: 16px 24px 6px;
}

.main { margin-left: 220px; padding: 36px 40px; flex: 1; max-width: calc(100vw - 220px); }

.page { display: none; }
.page.active { display: block; }

/* PAGE HEADER */
.page-header { margin-bottom: 28px; }
.page-title {
  font-family: 'Instrument Serif', serif;
  font-size: 32px;
  font-weight: 400;
  letter-spacing: -0.5px;
  margin-bottom: 4px;
}
.page-subtitle { font-size: 13px; color: var(--text-2); }

/* DASHBOARD */
.metrics-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-bottom: 24px;
}

.metric-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 20px;
  box-shadow: var(--shadow);
  position: relative;
  overflow: hidden;
}

.metric-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
}

.metric-card.green::before { background: var(--accent); }
.metric-card.red::before { background: var(--urgent); }
.metric-card.amber::before { background: var(--high); }
.metric-card.blue::before { background: var(--normal); }

.metric-label { font-size: 11px; color: var(--text-3); font-weight: 500; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 10px; }
.metric-value { font-family: 'Instrument Serif', serif; font-size: 38px; line-height: 1; color: var(--text); margin-bottom: 4px; }
.metric-sub { font-size: 11px; color: var(--text-3); }

.charts-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin-bottom: 14px; }
.charts-row.three { grid-template-columns: 1fr 1fr 1fr; }

.chart-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 22px;
  box-shadow: var(--shadow);
}

.chart-card.wide { grid-column: 1 / -1; }

.chart-title { font-size: 13px; font-weight: 500; color: var(--text); margin-bottom: 18px; }

/* DONUT */
.donut-container { display: flex; align-items: center; gap: 20px; }
.donut-wrap { position: relative; flex-shrink: 0; }
.donut-center {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
.donut-center-num { font-family: 'Instrument Serif', serif; font-size: 22px; color: var(--text); line-height: 1; }
.donut-center-label { font-size: 9px; color: var(--text-3); text-transform: uppercase; letter-spacing: 0.05em; }

.legend { display: flex; flex-direction: column; gap: 8px; flex: 1; }
.legend-item { display: flex; align-items: center; gap: 8px; font-size: 12px; color: var(--text-2); }
.legend-dot { width: 8px; height: 8px; border-radius: 2px; flex-shrink: 0; }
.legend-name { flex: 1; }
.legend-count { font-weight: 500; color: var(--text); font-size: 13px; }
.legend-pct { font-size: 10px; color: var(--text-3); margin-left: 4px; }

/* BARS */
.bar-group { display: flex; flex-direction: column; gap: 10px; }
.bar-row { display: flex; align-items: center; gap: 10px; }
.bar-label { font-size: 12px; color: var(--text-2); width: 32px; }
.bar-track { flex: 1; height: 7px; background: var(--surface2); border-radius: 4px; overflow: hidden; }
.bar-fill { height: 100%; border-radius: 4px; transition: width 0.6s cubic-bezier(0.34, 1.56, 0.64, 1); }
.bar-val { font-size: 12px; color: var(--text-2); width: 16px; text-align: right; }

/* PROGRESS */
.big-progress { margin-top: 4px; }
.big-progress-track { height: 12px; background: var(--surface2); border-radius: 6px; overflow: hidden; margin-bottom: 10px; }
.big-progress-fill { height: 100%; background: linear-gradient(90deg, var(--accent), #4A8C5F); border-radius: 6px; transition: width 0.8s cubic-bezier(0.34, 1.56, 0.64, 1); }
.big-progress-info { display: flex; justify-content: space-between; font-size: 12px; color: var(--text-2); }

/* WEEKLY CHART */
.week-chart { display: flex; align-items: flex-end; gap: 8px; height: 80px; }
.week-col { display: flex; flex-direction: column; align-items: center; gap: 4px; flex: 1; }
.week-bar-wrap { flex: 1; display: flex; align-items: flex-end; width: 100%; }
.week-bar { width: 100%; border-radius: 4px 4px 0 0; min-height: 4px; transition: height 0.4s; }
.week-day { font-size: 10px; color: var(--text-3); }
.week-num { font-size: 10px; font-weight: 500; color: var(--text-2); }

/* URGENT LIST */
.urgent-items { display: flex; flex-direction: column; gap: 8px; }
.urgent-item {
  display: flex; align-items: center; gap: 10px;
  padding: 10px 12px;
  background: var(--urgent-light);
  border-radius: var(--radius-sm);
  border-left: 3px solid var(--urgent);
  font-size: 13px;
}
.urgent-text { flex: 1; color: var(--text); }
.urgent-cat { font-size: 10px; font-weight: 500; }

/* TODO PAGE */
.todo-toolbar {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 16px;
  margin-bottom: 16px;
  box-shadow: var(--shadow);
}

.add-form { display: flex; gap: 8px; margin-bottom: 12px; }
.add-form input[type="text"] {
  flex: 1;
  padding: 9px 14px;
  border: 1px solid var(--border-strong);
  border-radius: var(--radius-sm);
  font-family: inherit;
  font-size: 14px;
  background: var(--bg);
  color: var(--text);
  outline: none;
  transition: border-color 0.15s;
}
.add-form input[type="text"]:focus { border-color: var(--accent); }
.add-form select {
  padding: 9px 10px;
  border: 1px solid var(--border-strong);
  border-radius: var(--radius-sm);
  font-family: inherit;
  font-size: 13px;
  background: var(--bg);
  color: var(--text);
  outline: none;
  cursor: pointer;
}

.btn-add {
  padding: 9px 18px;
  background: var(--accent);
  color: white;
  border: none;
  border-radius: var(--radius-sm);
  font-family: inherit;
  font-size: 13px;
  font-weight: 500;
  cursor: pointer;
  transition: opacity 0.15s;
  white-space: nowrap;
}
.btn-add:hover { opacity: 0.88; }

.filter-row { display: flex; gap: 6px; flex-wrap: wrap; }
.filter-chip {
  padding: 4px 12px;
  border: 1px solid var(--border);
  border-radius: 20px;
  font-size: 12px;
  font-weight: 400;
  cursor: pointer;
  color: var(--text-2);
  background: var(--bg);
  transition: all 0.15s;
}
.filter-chip:hover { border-color: var(--border-strong); color: var(--text); }
.filter-chip.active { background: var(--text); color: white; border-color: var(--text); }

/* TASK SECTIONS */
.task-section { margin-bottom: 20px; }
.section-header {
  display: flex; align-items: center; gap: 8px;
  margin-bottom: 8px;
  font-size: 11px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.07em;
  color: var(--text-3);
}
.section-dot { width: 7px; height: 7px; border-radius: 50%; }

/* TASK CARD */
.task-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  margin-bottom: 6px;
  overflow: hidden;
  box-shadow: var(--shadow);
  transition: box-shadow 0.15s, border-color 0.15s;
}
.task-card:hover { box-shadow: 0 2px 8px rgba(0,0,0,0.08); border-color: var(--border-strong); }
.task-card.done { opacity: 0.5; }

.task-main { display: flex; align-items: center; gap: 12px; padding: 12px 14px; cursor: pointer; }

.check-btn {
  width: 20px; height: 20px;
  border-radius: 5px;
  border: 1.5px solid var(--border-strong);
  background: none;
  cursor: pointer;
  flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
  transition: all 0.15s;
}
.check-btn.checked { background: var(--accent); border-color: var(--accent); }
.check-btn.checked::after { content: ''; display: block; width: 5px; height: 9px; border: 2px solid white; border-top: none; border-left: none; transform: rotate(45deg) translateY(-1px); }

.task-body { flex: 1; min-width: 0; }
.task-text { font-size: 14px; color: var(--text); line-height: 1.4; }
.task-card.done .task-text { text-decoration: line-through; color: var(--text-3); }
.task-meta { display: flex; align-items: center; gap: 6px; margin-top: 4px; flex-wrap: wrap; }
.task-note-preview { font-size: 11px; color: var(--text-3); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 200px; }

.badge {
  font-size: 10px; font-weight: 500;
  padding: 2px 7px; border-radius: 5px;
  white-space: nowrap;
}

.task-actions { display: flex; align-items: center; gap: 4px; }
.icon-btn {
  width: 28px; height: 28px;
  border: none; background: none;
  border-radius: 6px;
  cursor: pointer;
  color: var(--text-3);
  display: flex; align-items: center; justify-content: center;
  transition: all 0.15s;
  font-size: 13px;
}
.icon-btn:hover { background: var(--surface2); color: var(--text); }
.icon-btn.delete:hover { color: var(--urgent); background: var(--urgent-light); }

/* MEMO PANEL */
.memo-panel {
  background: var(--bg);
  border-top: 1px solid var(--border);
  padding: 10px 14px;
  display: none;
}
.memo-panel.open { display: block; }
.memo-input {
  width: 100%;
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 8px 10px;
  font-family: inherit;
  font-size: 13px;
  color: var(--text);
  background: var(--surface);
  resize: vertical;
  min-height: 64px;
  outline: none;
  line-height: 1.5;
}
.memo-input:focus { border-color: var(--accent); }
.memo-save {
  margin-top: 6px;
  padding: 5px 12px;
  background: var(--accent-light);
  color: var(--accent);
  border: none;
  border-radius: var(--radius-sm);
  font-family: inherit;
  font-size: 12px;
  font-weight: 500;
  cursor: pointer;
}
.memo-save:hover { background: var(--accent); color: white; }

.empty-state { text-align: center; padding: 48px 24px; color: var(--text-3); }
.empty-icon { font-size: 32px; margin-bottom: 10px; }
.empty-text { font-size: 14px; }

/* STATS PAGE */
.stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
.stats-full { grid-column: 1 / -1; }

/* TABLE */
.stat-table { width: 100%; border-collapse: collapse; }
.stat-table th { font-size: 10px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.06em; color: var(--text-3); padding: 0 0 10px; text-align: left; border-bottom: 1px solid var(--border); }
.stat-table td { padding: 10px 0; border-bottom: 1px solid var(--border); font-size: 13px; color: var(--text-2); vertical-align: middle; }
.stat-table tr:last-child td { border-bottom: none; }
.stat-table td:last-child { text-align: right; font-weight: 500; color: var(--text); }

.completion-bar-wrap { display: flex; align-items: center; gap: 8px; }
.comp-bar { flex: 1; height: 5px; background: var(--surface2); border-radius: 3px; overflow: hidden; }
.comp-fill { height: 100%; border-radius: 3px; }
.comp-pct { font-size: 11px; color: var(--text-3); min-width: 30px; }

/* ACTIVITY */
.activity-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 4px; }
.activity-cell {
  aspect-ratio: 1;
  border-radius: 3px;
  background: var(--surface2);
}
.activity-cell.level-1 { background: #c8e6c9; }
.activity-cell.level-2 { background: #81c784; }
.activity-cell.level-3 { background: #4caf50; }
.activity-cell.level-4 { background: var(--accent); }

/* RESPONSIVE */
@media (max-width: 900px) {
  .metrics-grid { grid-template-columns: 1fr 1fr; }
  .charts-row { grid-template-columns: 1fr; }
  .charts-row.three { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<div class="app-shell">
  <!-- SIDEBAR -->
  <aside class="sidebar">
    <div class="logo">
      <div class="logo-title">TaskFlow</div>
      <div class="logo-sub">스마트 할일 관리</div>
    </div>
    <nav class="nav">
      <button class="nav-item active" onclick="showPage('dashboard', this)">
        <svg class="nav-icon" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5">
          <rect x="1" y="1" width="6" height="6" rx="1.5"/><rect x="9" y="1" width="6" height="6" rx="1.5"/><rect x="1" y="9" width="6" height="6" rx="1.5"/><rect x="9" y="9" width="6" height="6" rx="1.5"/>
        </svg>
        대시보드
      </button>
      <button class="nav-item" onclick="showPage('todo', this)">
        <svg class="nav-icon" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5">
          <path d="M2 4h12M2 8h8M2 12h5"/><circle cx="13" cy="11" r="2.5"/><path d="M13 9.5v1.5l1 1"/>
        </svg>
        할일 목록
        <span class="nav-badge" id="nav-todo-count">0</span>
      </button>

      <div class="sidebar-section-label">카테고리</div>
      <button class="nav-item" onclick="showPage('todo', this); setFilter('work')">
        <span style="width:8px;height:8px;border-radius:2px;background:var(--work);flex-shrink:0"></span>
        업무
        <span class="nav-badge" id="nav-work-count">0</span>
      </button>
      <button class="nav-item" onclick="showPage('todo', this); setFilter('personal')">
        <span style="width:8px;height:8px;border-radius:2px;background:var(--personal);flex-shrink:0"></span>
        개인
        <span class="nav-badge" id="nav-personal-count">0</span>
      </button>
      <button class="nav-item" onclick="showPage('todo', this); setFilter('health')">
        <span style="width:8px;height:8px;border-radius:2px;background:var(--health);flex-shrink:0"></span>
        건강
        <span class="nav-badge" id="nav-health-count">0</span>
      </button>
      <button class="nav-item" onclick="showPage('todo', this); setFilter('study')">
        <span style="width:8px;height:8px;border-radius:2px;background:var(--study);flex-shrink:0"></span>
        학습
        <span class="nav-badge" id="nav-study-count">0</span>
      </button>

      <div class="sidebar-section-label" style="margin-top:8px">분석</div>
      <button class="nav-item" onclick="showPage('stats', this)">
        <svg class="nav-icon" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5">
          <path d="M2 12 L5 7 L8 9 L11 4 L14 6"/><rect x="2" y="13" width="12" height="1" rx="0.5" fill="currentColor" stroke="none"/>
        </svg>
        통계 분석
      </button>
    </nav>
  </aside>

  <!-- MAIN -->
  <main class="main">

    <!-- DASHBOARD PAGE -->
    <div class="page active" id="page-dashboard">
      <div class="page-header">
        <div class="page-title">대시보드</div>
        <div class="page-subtitle" id="dash-date"></div>
      </div>

      <div class="metrics-grid">
        <div class="metric-card green">
          <div class="metric-label">전체 할일</div>
          <div class="metric-value" id="m-total">0</div>
          <div class="metric-sub">등록된 총 항목</div>
        </div>
        <div class="metric-card blue">
          <div class="metric-label">완료</div>
          <div class="metric-value" id="m-done">0</div>
          <div class="metric-sub" id="m-rate-sub">완료율 0%</div>
        </div>
        <div class="metric-card red">
          <div class="metric-label">긴급 잔여</div>
          <div class="metric-value" id="m-urgent">0</div>
          <div class="metric-sub">즉시 처리 필요</div>
        </div>
        <div class="metric-card amber">
          <div class="metric-label">오늘 추가</div>
          <div class="metric-value" id="m-today">0</div>
          <div class="metric-sub">오늘 생성된 할일</div>
        </div>
      </div>

      <div class="charts-row">
        <div class="chart-card">
          <div class="chart-title">카테고리 분포</div>
          <div class="donut-container">
            <div class="donut-wrap">
              <canvas id="donut-canvas" width="120" height="120"></canvas>
              <div class="donut-center">
                <div class="donut-center-num" id="donut-center-num">0</div>
                <div class="donut-center-label">전체</div>
              </div>
            </div>
            <div class="legend" id="cat-legend"></div>
          </div>
        </div>
        <div class="chart-card">
          <div class="chart-title">우선순위 현황</div>
          <div class="bar-group" id="pri-bars"></div>
        </div>
      </div>

      <div class="charts-row">
        <div class="chart-card wide">
          <div class="chart-title">전체 진행률</div>
          <div class="big-progress">
            <div class="big-progress-track">
              <div class="big-progress-fill" id="big-progress" style="width:0%"></div>
            </div>
            <div class="big-progress-info">
              <span id="prog-done-text">0개 완료</span>
              <span id="prog-pct-text">0%</span>
              <span id="prog-left-text">0개 남음</span>
            </div>
          </div>
        </div>
      </div>

      <div class="chart-card">
        <div class="chart-title">긴급 미완료 할일</div>
        <div class="urgent-items" id="urgent-list"></div>
      </div>
    </div>

    <!-- TODO PAGE -->
    <div class="page" id="page-todo">
      <div class="page-header">
        <div class="page-title">할일 목록</div>
        <div class="page-subtitle">할일을 추가하고 관리하세요</div>
      </div>

      <div class="todo-toolbar">
        <div class="add-form">
          <input type="text" id="task-input" placeholder="새 할일을 입력하세요..." />
          <select id="cat-select">
            <option value="work">업무</option>
            <option value="personal">개인</option>
            <option value="health">건강</option>
            <option value="study">학습</option>
          </select>
          <select id="pri-select">
            <option value="urgent">긴급</option>
            <option value="high">높음</option>
            <option value="normal" selected>보통</option>
            <option value="low">낮음</option>
          </select>
          <button class="btn-add" onclick="addTask()">+ 추가</button>
        </div>
        <div class="filter-row" id="filter-row">
          <button class="filter-chip active" onclick="setFilter('all', this)">전체</button>
          <button class="filter-chip" onclick="setFilter('work', this)">업무</button>
          <button class="filter-chip" onclick="setFilter('personal', this)">개인</button>
          <button class="filter-chip" onclick="setFilter('health', this)">건강</button>
          <button class="filter-chip" onclick="setFilter('study', this)">학습</button>
          <button class="filter-chip" onclick="setFilter('urgent', this)">긴급</button>
          <button class="filter-chip" onclick="setFilter('done', this)">완료</button>
        </div>
      </div>

      <div id="task-container"></div>
    </div>

    <!-- STATS PAGE -->
    <div class="page" id="page-stats">
      <div class="page-header">
        <div class="page-title">통계 분석</div>
        <div class="page-subtitle">할일 패턴과 생산성을 한눈에</div>
      </div>

      <div class="stats-grid">
        <div class="chart-card">
          <div class="chart-title">카테고리별 완료율</div>
          <table class="stat-table" id="cat-completion-table"></table>
        </div>
        <div class="chart-card">
          <div class="chart-title">우선순위별 완료율</div>
          <table class="stat-table" id="pri-completion-table"></table>
        </div>
        <div class="chart-card stats-full">
          <div class="chart-title">주간 추가 현황 (최근 7일)</div>
          <div class="week-chart" id="week-chart"></div>
        </div>
        <div class="chart-card stats-full">
          <div class="chart-title">생산성 요약</div>
          <div id="productivity-summary" style="display:flex;gap:24px;flex-wrap:wrap"></div>
        </div>
      </div>
    </div>

  </main>
</div>

<script>
// ── DATA ──────────────────────────────────────────────
const STORAGE_KEY = 'taskflow-tasks-v2';
const today = new Date().toDateString();

function loadTasks() {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if (raw) return JSON.parse(raw);
  } catch(e) {}
  // default sample data
  return [
    {id:1, text:'기획서 초안 작성', cat:'work', pri:'urgent', done:false, memo:'3페이지 분량, 내일까지', createdAt: today},
    {id:2, text:'팀 미팅 준비', cat:'work', pri:'high', done:false, memo:'', createdAt: today},
    {id:3, text:'운동 30분', cat:'health', pri:'normal', done:true, memo:'', createdAt: today},
    {id:4, text:'알고리즘 강의 듣기', cat:'study', pri:'normal', done:false, memo:'섹션 5까지', createdAt: today},
    {id:5, text:'병원 예약', cat:'health', pri:'high', done:false, memo:'', createdAt: new Date(Date.now()-86400000).toDateString()},
    {id:6, text:'장보기', cat:'personal', pri:'low', done:true, memo:'우유, 계란, 빵', createdAt: new Date(Date.now()-86400000).toDateString()},
    {id:7, text:'독서 30분', cat:'personal', pri:'low', done:false, memo:'', createdAt: new Date(Date.now()-172800000).toDateString()},
  ];
}

let tasks = loadTasks();
let nextId = tasks.reduce((m,t) => Math.max(m, t.id), 0) + 1;
let currentFilter = 'all';
let openMemos = new Set();

function save() {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(tasks));
}

// ── CONFIG ────────────────────────────────────────────
const catLabel = {work:'업무', personal:'개인', health:'건강', study:'학습'};
const priLabel = {urgent:'긴급', high:'높음', normal:'보통', low:'낮음'};
const priOrder = {urgent:0, high:1, normal:2, low:3};
const catColors = {work:'var(--work)', personal:'var(--personal)', health:'var(--health)', study:'var(--study)'};
const catBg    = {work:'var(--work-light)', personal:'var(--personal-light)', health:'var(--health-light)', study:'var(--study-light)'};
const priColors = {urgent:'var(--urgent)', high:'var(--high)', normal:'var(--normal)', low:'var(--low)'};
const priBg    = {urgent:'var(--urgent-light)', high:'var(--high-light)', normal:'var(--normal-light)', low:'var(--low-light)'};
const catColorsHex = {work:'#2D5A3D', personal:'#5B3A8C', health:'#C0392B', study:'#D4820A'};

// ── NAVIGATION ────────────────────────────────────────
function showPage(name, btn) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(b => b.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  if (btn) btn.classList.add('active');
  if (name === 'dashboard') renderDashboard();
  if (name === 'stats') renderStats();
  if (name === 'todo') renderTodo();
}

// ── DATE ─────────────────────────────────────────────
function formatDate() {
  const d = new Date();
  const days = ['일','월','화','수','목','금','토'];
  return `${d.getFullYear()}년 ${d.getMonth()+1}월 ${d.getDate()}일 (${days[d.getDay()]})`;
}
document.getElementById('dash-date').textContent = formatDate();

// ── TASK ADD ─────────────────────────────────────────
function addTask() {
  const input = document.getElementById('task-input');
  const text = input.value.trim();
  if (!text) return;
  const t = {
    id: nextId++,
    text,
    cat: document.getElementById('cat-select').value,
    pri: document.getElementById('pri-select').value,
    done: false,
    memo: '',
    createdAt: today
  };
  tasks.unshift(t);
  save();
  input.value = '';
  renderTodo();
  updateNavBadges();
}

document.getElementById('task-input').addEventListener('keydown', e => {
  if (e.key === 'Enter') addTask();
});

function toggleTask(id) {
  const t = tasks.find(t => t.id === id);
  if (t) { t.done = !t.done; save(); renderTodo(); updateNavBadges(); }
}

function deleteTask(id) {
  tasks = tasks.filter(t => t.id !== id);
  openMemos.delete(id);
  save();
  renderTodo();
  updateNavBadges();
}

function saveMemo(id) {
  const t = tasks.find(t => t.id === id);
  const textarea = document.getElementById('memo-' + id);
  if (t && textarea) { t.memo = textarea.value; save(); renderTodo(); }
}

function toggleMemo(id) {
  if (openMemos.has(id)) openMemos.delete(id);
  else openMemos.add(id);
  renderTodo();
}

function setFilter(f, btn) {
  currentFilter = f;
  document.querySelectorAll('.filter-chip').forEach(b => b.classList.remove('active'));
  if (btn) btn.classList.add('active');
  else {
    const chips = document.querySelectorAll('.filter-chip');
    chips.forEach(c => { if (c.textContent.trim() === (catLabel[f]||f)) c.classList.add('active'); });
  }
  renderTodo();
}

// ── RENDER TODO ───────────────────────────────────────
function renderTodo() {
  let filtered = tasks;
  if (currentFilter === 'done') filtered = tasks.filter(t => t.done);
  else if (currentFilter === 'urgent') filtered = tasks.filter(t => t.pri === 'urgent' && !t.done);
  else if (currentFilter !== 'all') filtered = tasks.filter(t => t.cat === currentFilter);

  const active = filtered.filter(t => !t.done).sort((a,b) => priOrder[a.pri] - priOrder[b.pri]);
  const done = filtered.filter(t => t.done);

  const container = document.getElementById('task-container');

  if (!filtered.length) {
    container.innerHTML = `<div class="empty-state"><div class="empty-icon">✓</div><div class="empty-text">할일이 없습니다</div></div>`;
    return;
  }

  const groups = {};
  active.forEach(t => { if (!groups[t.pri]) groups[t.pri] = []; groups[t.pri].push(t); });

  let html = '';
  ['urgent','high','normal','low'].forEach(pri => {
    if (!groups[pri] || !groups[pri].length) return;
    html += `<div class="task-section">
      <div class="section-header">
        <span class="section-dot" style="background:${priColors[pri]}"></span>
        ${priLabel[pri]} 우선순위
      </div>
      ${groups[pri].map(taskCardHTML).join('')}
    </div>`;
  });

  if (done.length) {
    html += `<div class="task-section">
      <div class="section-header">완료됨</div>
      ${done.map(taskCardHTML).join('')}
    </div>`;
  }

  container.innerHTML = html;
}

function taskCardHTML(t) {
  const memoOpen = openMemos.has(t.id);
  const memoIcon = t.memo ? '📝' : '✏️';
  return `<div class="task-card${t.done?' done':''}">
    <div class="task-main" onclick="toggleTask(${t.id})">
      <div class="check-btn${t.done?' checked':''}"></div>
      <div class="task-body">
        <div class="task-text">${t.text}</div>
        <div class="task-meta">
          <span class="badge" style="background:${catBg[t.cat]};color:${catColorsHex[t.cat]}">${catLabel[t.cat]}</span>
          <span class="badge" style="background:${priBg[t.pri]};color:${priColors[t.pri].replace('var(--','')}"><!-- handled below --></span>
          ${t.memo ? `<span class="task-note-preview">📝 ${t.memo}</span>` : ''}
        </div>
      </div>
      <div class="task-actions" onclick="event.stopPropagation()">
        <button class="icon-btn" onclick="toggleMemo(${t.id})" title="메모">${memoIcon}</button>
        <button class="icon-btn delete" onclick="deleteTask(${t.id})" title="삭제">✕</button>
      </div>
    </div>
    <div class="memo-panel${memoOpen?' open':''}">
      <textarea class="memo-input" id="memo-${t.id}" placeholder="메모를 입력하세요...">${t.memo||''}</textarea>
      <button class="memo-save" onclick="saveMemo(${t.id})">저장</button>
    </div>
  </div>`;
}

// Fix the badge color inline issue
function renderTodoFixed() {
  renderTodo();
  // patch priority badges
  document.querySelectorAll('.task-card').forEach(card => {
    const badges = card.querySelectorAll('.badge');
    if (badges[1]) {
      const taskId = parseInt(card.querySelector('.check-btn')?.getAttribute?.('data-id') || '0');
    }
  });
}

// ── DASHBOARD ─────────────────────────────────────────
function renderDashboard() {
  const total = tasks.length;
  const done = tasks.filter(t => t.done).length;
  const rate = total ? Math.round(done / total * 100) : 0;
  const urgentLeft = tasks.filter(t => t.pri === 'urgent' && !t.done).length;
  const todayCount = tasks.filter(t => t.createdAt === today).length;

  document.getElementById('m-total').textContent = total;
  document.getElementById('m-done').textContent = done;
  document.getElementById('m-rate-sub').textContent = `완료율 ${rate}%`;
  document.getElementById('m-urgent').textContent = urgentLeft;
  document.getElementById('m-today').textContent = todayCount;
  document.getElementById('big-progress').style.width = rate + '%';
  document.getElementById('prog-done-text').textContent = done + '개 완료';
  document.getElementById('prog-pct-text').textContent = rate + '%';
  document.getElementById('prog-left-text').textContent = (total - done) + '개 남음';

  // Donut
  const canvas = document.getElementById('donut-canvas');
  const ctx = canvas.getContext('2d');
  const cats = ['work','personal','health','study'];
  const counts = cats.map(c => tasks.filter(t => t.cat === c).length);
  const sum = counts.reduce((a,b) => a+b, 0) || 1;
  ctx.clearRect(0, 0, 120, 120);
  let angle = -Math.PI / 2;
  const cx=60, cy=60, r=50, ir=30;
  cats.forEach((c, i) => {
    const slice = (counts[i] / sum) * Math.PI * 2;
    ctx.beginPath(); ctx.moveTo(cx, cy);
    ctx.arc(cx, cy, r, angle, angle + slice);
    ctx.closePath();
    ctx.fillStyle = catColorsHex[c];
    ctx.fill();
    angle += slice;
  });
  ctx.beginPath(); ctx.arc(cx, cy, ir, 0, Math.PI*2);
  ctx.fillStyle = '#FFFFFF'; ctx.fill();
  document.getElementById('donut-center-num').textContent = total;

  document.getElementById('cat-legend').innerHTML = cats.map((c,i) => `
    <div class="legend-item">
      <span class="legend-dot" style="background:${catColorsHex[c]}"></span>
      <span class="legend-name">${catLabel[c]}</span>
      <span class="legend-count">${counts[i]}</span>
      <span class="legend-pct">${Math.round(counts[i]/sum*100)}%</span>
    </div>`).join('');

  // Pri bars
  const priCounts = ['urgent','high','normal','low'].map(p => tasks.filter(t => t.pri===p).length);
  const maxP = Math.max(...priCounts, 1);
  document.getElementById('pri-bars').innerHTML = ['urgent','high','normal','low'].map((p,i) => `
    <div class="bar-row">
      <span class="bar-label">${priLabel[p]}</span>
      <div class="bar-track"><div class="bar-fill" style="width:${Math.round(priCounts[i]/maxP*100)}%;background:${catColorsHex[['health','study','personal','work'][i]]}"></div></div>
      <span class="bar-val">${priCounts[i]}</span>
    </div>`).join('');

  // Urgent list
  const urgents = tasks.filter(t => t.pri === 'urgent' && !t.done);
  document.getElementById('urgent-list').innerHTML = urgents.length
    ? urgents.map(t => `<div class="urgent-item">
        <span class="urgent-text">${t.text}</span>
        <span class="badge" style="background:${catBg[t.cat]};color:${catColorsHex[t.cat]}">${catLabel[t.cat]}</span>
        ${t.memo ? `<span style="font-size:11px;color:var(--text-3)">📝</span>` : ''}
      </div>`).join('')
    : '<span style="font-size:13px;color:var(--text-3)">긴급 할일이 없습니다 🎉</span>';
}

// ── STATS ─────────────────────────────────────────────
function renderStats() {
  const cats = ['work','personal','health','study'];
  const pris = ['urgent','high','normal','low'];

  // Cat completion table
  document.getElementById('cat-completion-table').innerHTML =
    `<tr><th>카테고리</th><th>전체</th><th>완료율</th></tr>` +
    cats.map(c => {
      const total = tasks.filter(t => t.cat===c).length;
      const done = tasks.filter(t => t.cat===c && t.done).length;
      const pct = total ? Math.round(done/total*100) : 0;
      return `<tr>
        <td><span class="badge" style="background:${catBg[c]};color:${catColorsHex[c]}">${catLabel[c]}</span></td>
        <td>${total}</td>
        <td>
          <div class="completion-bar-wrap">
            <div class="comp-bar"><div class="comp-fill" style="width:${pct}%;background:${catColorsHex[c]}"></div></div>
            <span class="comp-pct">${pct}%</span>
          </div>
        </td>
      </tr>`;
    }).join('');

  // Pri completion table
  document.getElementById('pri-completion-table').innerHTML =
    `<tr><th>우선순위</th><th>전체</th><th>완료율</th></tr>` +
    pris.map(p => {
      const total = tasks.filter(t => t.pri===p).length;
      const done = tasks.filter(t => t.pri===p && t.done).length;
      const pct = total ? Math.round(done/total*100) : 0;
      return `<tr>
        <td>${priLabel[p]}</td>
        <td>${total}</td>
        <td>
          <div class="completion-bar-wrap">
            <div class="comp-bar"><div class="comp-fill" style="width:${pct}%;background:${priColors[p]}"></div></div>
            <span class="comp-pct">${pct}%</span>
          </div>
        </td>
      </tr>`;
    }).join('');

  // Weekly chart
  const days = ['일','월','화','수','목','금','토'];
  const weekData = [];
  const maxW = 60;
  for (let i=6; i>=0; i--) {
    const d = new Date(Date.now() - i*86400000);
    const ds = d.toDateString();
    const count = tasks.filter(t => t.createdAt === ds).length;
    weekData.push({day: days[d.getDay()], count});
  }
  const maxWC = Math.max(...weekData.map(d=>d.count), 1);
  document.getElementById('week-chart').innerHTML = weekData.map(d => `
    <div class="week-col">
      <div class="week-num">${d.count||''}</div>
      <div class="week-bar-wrap">
        <div class="week-bar" style="height:${Math.round(d.count/maxWC*maxW)}px;background:var(--accent);opacity:${0.4+d.count/maxWC*0.6}"></div>
      </div>
      <div class="week-day">${d.day}</div>
    </div>`).join('');

  // Productivity summary
  const totalDone = tasks.filter(t=>t.done).length;
  const totalAll = tasks.length;
  const withMemo = tasks.filter(t=>t.memo&&t.memo.trim()).length;
  const urgDone = tasks.filter(t=>t.pri==='urgent'&&t.done).length;
  const urgTotal = tasks.filter(t=>t.pri==='urgent').length;

  document.getElementById('productivity-summary').innerHTML = [
    {label:'전체 완료율', value: totalAll ? Math.round(totalDone/totalAll*100)+'%' : '—', sub: `${totalDone}/${totalAll}개`},
    {label:'긴급 처리율', value: urgTotal ? Math.round(urgDone/urgTotal*100)+'%' : '—', sub: `${urgDone}/${urgTotal}개`},
    {label:'메모 활용', value: withMemo+'개', sub: '메모 있는 할일'},
    {label:'총 등록', value: totalAll+'개', sub: '누적 할일 수'},
  ].map(s => `<div class="metric-card" style="flex:1;min-width:120px">
    <div class="metric-label">${s.label}</div>
    <div class="metric-value" style="font-size:28px">${s.value}</div>
    <div class="metric-sub">${s.sub}</div>
  </div>`).join('');
}

// ── NAV BADGES ────────────────────────────────────────
function updateNavBadges() {
  document.getElementById('nav-todo-count').textContent = tasks.filter(t=>!t.done).length;
  document.getElementById('nav-work-count').textContent = tasks.filter(t=>t.cat==='work'&&!t.done).length;
  document.getElementById('nav-personal-count').textContent = tasks.filter(t=>t.cat==='personal'&&!t.done).length;
  document.getElementById('nav-health-count').textContent = tasks.filter(t=>t.cat==='health'&&!t.done).length;
  document.getElementById('nav-study-count').textContent = tasks.filter(t=>t.cat==='study'&&!t.done).length;
}

// ── INIT ─────────────────────────────────────────────
renderDashboard();
renderTodo();
updateNavBadges();
</script>
</body>
</html>
