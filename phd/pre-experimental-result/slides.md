---
theme: default
title: Paper 1 Proposal - Cross-Scenario Operator State Detection
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade
colorSchema: dark
fonts:
  sans: 'Inter'
  serif: 'Inter'
  mono: 'JetBrains Mono'
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[600px] h-[600px] bg-cyan-500/10 rounded-full blur-[140px] anim-breathe-slow"></div>
  <div class="absolute bottom-[-15%] right-[-10%] w-[650px] h-[650px] bg-fuchsia-500/10 rounded-full blur-[140px] anim-breathe-slow-2"></div>
  <div class="absolute top-[40%] left-[55%] w-[400px] h-[400px] bg-blue-600/8 rounded-full blur-[120px]"></div>
</div>
<div class="absolute inset-0 opacity-25 pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full anim-eeg-flow" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,200 Q80,200 130,180 T230,200 Q280,100 330,200 T430,200 Q480,260 530,200 T630,200 Q680,140 730,200 T830,200 Q880,220 930,200 T1030,200 Q1080,170 1130,200 T1230,200 Q1280,100 1330,200 T1430,200 Q1480,260 1530,200 T1630,200 Q1680,200 1730,180 T1830,200 Q1880,100 1930,200 T2030,200 Q2080,260 2130,200 T2230,200 Q2280,140 2330,200 T2430,200 Q2480,220 2530,200 T2630,200 Q2680,170 2730,200 T2830,200 Q2880,100 2930,200 T3030,200 Q3080,260 3130,200 L3200,200" fill="none" stroke="#22d3ee" stroke-width="1.2" opacity="0.7"/>
    <path d="M0,720 Q70,720 130,700 T230,720 Q280,660 330,720 T430,720 Q480,760 530,720 T630,720 Q680,680 730,720 T830,720 Q880,740 930,720 T1030,720 Q1080,670 1130,720 T1230,720 Q1280,780 1330,720 T1430,720 Q1480,700 1530,720 T1630,720 Q1680,720 1730,700 T1830,720 Q1880,660 1930,720 T2030,720 Q2080,760 2130,720 T2230,720 Q2280,680 2330,720 T2430,720 Q2480,740 2530,720 T2630,720 Q2680,670 2730,720 T2830,720 Q2880,780 2930,720 T3030,720 Q3080,700 3130,720 L3200,720" fill="none" stroke="#a855f7" stroke-width="1.2" opacity="0.6"/>
  </svg>
</div>
<div class="absolute inset-0 opacity-15 pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full anim-eeg-flow-slow" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q150,420 300,450 T600,450 Q750,380 900,450 T1200,450 Q1350,500 1500,450 T1800,450 Q1950,400 2100,450 T2400,450 Q2550,500 2700,450 T3000,450 L3200,450" fill="none" stroke="#67e8f9" stroke-width="0.8"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[18%] left-[8%] w-1 h-1 bg-cyan-400 rounded-full anim-pulse-1"></div>
  <div class="absolute top-[25%] left-[12%] w-1 h-1 bg-cyan-400 rounded-full anim-pulse-2"></div>
  <div class="absolute top-[70%] left-[6%] w-1.5 h-1.5 bg-fuchsia-400 rounded-full anim-pulse-3"></div>
  <div class="absolute top-[22%] right-[30%] w-1 h-1 bg-cyan-300 rounded-full anim-pulse-2"></div>
  <div class="absolute top-[60%] right-[30%] w-1.5 h-1.5 bg-fuchsia-400 rounded-full anim-pulse-1"></div>
  <div class="absolute top-[85%] left-[45%] w-1 h-1 bg-fuchsia-300 rounded-full anim-pulse-2"></div>
  <div class="absolute top-[15%] left-[35%] w-1 h-1 bg-cyan-300 rounded-full anim-pulse-3"></div>
  <div class="absolute top-[50%] left-[4%] w-1 h-1 bg-fuchsia-300 rounded-full anim-pulse-1"></div>
</div>
<div class="absolute top-16 right-20 w-16 h-16 opacity-35 anim-crosshair">
  <div class="absolute inset-0 border border-cyan-400 rounded-full anim-ring-pulse"></div>
  <div class="absolute inset-[20%] border border-cyan-400 rounded-full anim-ring-pulse-delay"></div>
  <div class="absolute inset-[40%] border border-cyan-300 rounded-full"></div>
  <div class="absolute top-1/2 left-0 w-full h-px bg-cyan-400"></div>
  <div class="absolute left-1/2 top-0 h-full w-px bg-cyan-400"></div>
  <div class="absolute top-1/2 left-1/2 w-1.5 h-1.5 bg-cyan-300 rounded-full anim-dot-blink" style="transform: translate(-50%, -50%);"></div>
</div>
<div class="absolute top-[28%] right-[7%] anim-fade-in-delay-3">
  <div class="anim-drift-x-1">
    <div class="flex flex-col items-center">
      <svg viewBox="0 0 140 140" width="72" height="72" style="filter: drop-shadow(0 0 10px rgba(34,211,238,0.55));">
        <ellipse cx="70" cy="130" rx="24" ry="3" fill="#22d3ee" opacity="0.25" class="send-uav-shadow"/>
        <g class="send-uav-hover">
          <line x1="70" y1="70" x2="28" y2="28" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="112" y2="28" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="28" y2="112" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="112" y2="112" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
          <circle cx="28" cy="28" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 28px 28px;" class="send-rotor-cw">
            <line x1="14" y1="28" x2="42" y2="28" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="28" cy="28" r="3" fill="#22d3ee"/>
          <circle cx="112" cy="28" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 112px 28px;" class="send-rotor-ccw">
            <line x1="98" y1="28" x2="126" y2="28" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="112" cy="28" r="3" fill="#22d3ee"/>
          <circle cx="28" cy="112" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 28px 112px;" class="send-rotor-ccw">
            <line x1="14" y1="112" x2="42" y2="112" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="28" cy="112" r="3" fill="#22d3ee"/>
          <circle cx="112" cy="112" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 112px 112px;" class="send-rotor-cw">
            <line x1="98" y1="112" x2="126" y2="112" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="112" cy="112" r="3" fill="#22d3ee"/>
          <circle cx="70" cy="70" r="12" fill="#000" stroke="#22d3ee" stroke-width="2"/>
          <circle cx="70" cy="70" r="5" fill="#22d3ee" class="send-beacon"/>
        </g>
      </svg>
      <div class="text-[9px] uppercase tracking-[0.3em] text-cyan-400/80 font-mono mt-2">UAV-1</div>
    </div>
  </div>
</div>
<div class="absolute top-[46%] right-[14%] anim-fade-in-delay-3b">
  <div class="anim-drift-x-2">
    <div class="flex flex-col items-center">
      <svg viewBox="0 0 140 140" width="60" height="60" style="filter: drop-shadow(0 0 10px rgba(56,189,248,0.55));">
        <ellipse cx="70" cy="130" rx="24" ry="3" fill="#38bdf8" opacity="0.25" class="send-uav-shadow"/>
        <g class="send-uav-hover" style="animation-delay: -1.5s;">
          <line x1="70" y1="70" x2="28" y2="28" stroke="#38bdf8" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="112" y2="28" stroke="#38bdf8" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="28" y2="112" stroke="#38bdf8" stroke-width="3" stroke-linecap="round"/>
          <line x1="70" y1="70" x2="112" y2="112" stroke="#38bdf8" stroke-width="3" stroke-linecap="round"/>
          <circle cx="28" cy="28" r="14" fill="rgba(56,189,248,0.06)" stroke="#38bdf8" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 28px 28px;" class="send-rotor-ccw">
            <line x1="14" y1="28" x2="42" y2="28" stroke="#38bdf8" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="28" cy="28" r="3" fill="#38bdf8"/>
          <circle cx="112" cy="28" r="14" fill="rgba(56,189,248,0.06)" stroke="#38bdf8" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 112px 28px;" class="send-rotor-cw">
            <line x1="98" y1="28" x2="126" y2="28" stroke="#38bdf8" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="112" cy="28" r="3" fill="#38bdf8"/>
          <circle cx="28" cy="112" r="14" fill="rgba(56,189,248,0.06)" stroke="#38bdf8" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 28px 112px;" class="send-rotor-cw">
            <line x1="14" y1="112" x2="42" y2="112" stroke="#38bdf8" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="28" cy="112" r="3" fill="#38bdf8"/>
          <circle cx="112" cy="112" r="14" fill="rgba(56,189,248,0.06)" stroke="#38bdf8" stroke-width="0.8" opacity="0.5"/>
          <g style="transform-origin: 112px 112px;" class="send-rotor-ccw">
            <line x1="98" y1="112" x2="126" y2="112" stroke="#38bdf8" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
          </g>
          <circle cx="112" cy="112" r="3" fill="#38bdf8"/>
          <circle cx="70" cy="70" r="12" fill="#000" stroke="#38bdf8" stroke-width="2"/>
          <circle cx="70" cy="70" r="5" fill="#38bdf8" class="send-beacon"/>
        </g>
      </svg>
      <div class="text-[9px] uppercase tracking-[0.3em] text-sky-400/80 font-mono mt-2">UAV-2</div>
    </div>
  </div>
</div>
<div class="absolute top-[67%] right-[6%] anim-fade-in-delay-3">
  <div class="anim-drift-x-3">
    <div class="flex flex-col items-center">
      <svg viewBox="0 0 140 140" width="88" height="88" style="filter: drop-shadow(0 0 10px rgba(232,121,249,0.55));">
        <line x1="5" y1="120" x2="135" y2="120" stroke="#e879f9" stroke-width="1" opacity="0.35" stroke-dasharray="6 3" class="send-ground-scroll"/>
        <g class="send-ugv-bob">
          <path d="M 95 75 L 125 68 L 125 82 L 95 79 Z" fill="#e879f9" opacity="0.15" class="send-headlight"/>
          <path d="M 30 90 L 30 72 L 42 62 L 98 62 L 110 72 L 110 90 Z" fill="#000" stroke="#e879f9" stroke-width="2"/>
          <rect x="52" y="46" width="32" height="16" rx="1" fill="#000" stroke="#e879f9" stroke-width="2"/>
          <circle cx="68" cy="54" r="3" fill="#e879f9" class="send-camera-pulse"/>
          <line x1="85" y1="46" x2="96" y2="24" stroke="#e879f9" stroke-width="1.5"/>
          <circle cx="96" cy="24" r="2.5" fill="#e879f9" class="send-antenna-pulse"/>
          <path d="M 96 24 Q 104 18 108 24" fill="none" stroke="#e879f9" stroke-width="1" class="send-signal-a"/>
          <path d="M 96 24 Q 108 12 116 24" fill="none" stroke="#e879f9" stroke-width="1" class="send-signal-b"/>
          <circle cx="108" cy="78" r="2" fill="#e879f9"/>
          <line x1="42" y1="70" x2="45" y2="62" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
          <line x1="98" y1="62" x2="95" y2="70" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
          <g style="transform-origin: 95px 95px;" class="send-wheel-spin">
            <circle cx="95" cy="95" r="13" fill="#000" stroke="#e879f9" stroke-width="2"/>
            <circle cx="95" cy="95" r="5" fill="#e879f9"/>
            <line x1="95" y1="82" x2="95" y2="108" stroke="#e879f9" stroke-width="1.5"/>
            <line x1="82" y1="95" x2="108" y2="95" stroke="#e879f9" stroke-width="1.5"/>
            <line x1="86" y1="86" x2="104" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
            <line x1="104" y1="86" x2="86" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
          </g>
          <g style="transform-origin: 45px 95px;" class="send-wheel-spin">
            <circle cx="45" cy="95" r="13" fill="#000" stroke="#e879f9" stroke-width="2"/>
            <circle cx="45" cy="95" r="5" fill="#e879f9"/>
            <line x1="45" y1="82" x2="45" y2="108" stroke="#e879f9" stroke-width="1.5"/>
            <line x1="32" y1="95" x2="58" y2="95" stroke="#e879f9" stroke-width="1.5"/>
            <line x1="36" y1="86" x2="54" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
            <line x1="54" y1="86" x2="36" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
          </g>
        </g>
      </svg>
      <div class="text-[9px] uppercase tracking-[0.3em] text-fuchsia-400/80 font-mono mt-2">UGV</div>
    </div>
  </div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-cyan-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent anim-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col py-6 px-16">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-4 anim-fade-in">
      <div class="relative anim-logo-glow">
        <div class="absolute -inset-1 rounded-xl bg-gradient-to-br from-cyan-400/30 via-sky-400/20 to-fuchsia-400/30 blur-md"></div>
        <div class="relative w-16 h-16 rounded-xl p-[1.5px] bg-gradient-to-br from-cyan-400 via-sky-500 to-fuchsia-500">
          <div class="relative w-full h-full rounded-[10px] bg-slate-950 flex items-center justify-center overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-br from-cyan-500/10 to-fuchsia-500/10"></div>
            <div class="absolute top-1 left-1 w-1.5 h-1.5 border-l border-t border-cyan-400/60"></div>
            <div class="absolute top-1 right-1 w-1.5 h-1.5 border-r border-t border-cyan-400/60"></div>
            <div class="absolute bottom-1 left-1 w-1.5 h-1.5 border-l border-b border-fuchsia-400/60"></div>
            <div class="absolute bottom-1 right-1 w-1.5 h-1.5 border-r border-b border-fuchsia-400/60"></div>
            <img src="/logo.svg" class="relative w-10 h-10 object-contain" alt="BIT Logo" />
          </div>
        </div>
      </div>
      <div class="flex flex-col justify-center leading-tight">
        <div class="text-[10px] uppercase tracking-[0.3em] text-slate-300 font-mono">Beijing Institute of Technology</div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-slate-600 font-mono mt-1">School of Mechanical Engineering</div>
      </div>
    </div>
    <div class="flex items-center gap-3 anim-fade-in-delay mr-24">
      <div class="w-2 h-2 bg-cyan-400 rounded-full anim-pulse-strong"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono">Paper 01 · Proposal</div>
    </div>
  </div>
  <div class="mt-10 max-w-[75%]">
    <div class="flex items-center gap-3 mb-5 anim-slide-in">
      <div class="h-px w-8 bg-cyan-400 opacity-60"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono opacity-80">Human Factors · Brain-Computer Interface · Teleoperation</div>
    </div>
    <h1 class="!text-[2.7rem] !leading-[1.1] !font-bold !mb-3 tracking-tight anim-slide-in-delay">
      <span class="text-white">Cross-Scenario </span><span class="bg-gradient-to-r from-cyan-300 via-sky-300 to-fuchsia-300 bg-clip-text text-transparent">Operator State Detection</span>
    </h1>
    <h2 class="!text-[1.45rem] !leading-snug !font-light !text-slate-200 !mb-8 !mt-0 tracking-wide anim-slide-in-delay-2">for Unmanned Vehicle Teleoperation</h2>
    <div class="flex items-stretch gap-5 mb-2 anim-slide-in-delay-3">
      <div class="w-[3px] bg-gradient-to-b from-cyan-400 via-sky-400 to-fuchsia-400 rounded-full"></div>
      <div class="text-[1.05rem] text-slate-300 font-light leading-relaxed">
        A hybrid <span class="text-cyan-300 font-medium">handcrafted–deep feature fusion</span> of
        <span class="px-1.5 py-0.5 rounded bg-cyan-500/10 border border-cyan-500 text-cyan-200 font-mono text-sm">EEG</span>
        and
        <span class="px-1.5 py-0.5 rounded bg-fuchsia-500/10 border border-fuchsia-500 text-fuchsia-200 font-mono text-sm">Eye-Gaze</span>,
        transferring from controlled lab to multiple applied scenarios.
      </div>
    </div>
  </div>
  <div class="flex-1"></div>
  <div class="flex items-end justify-between anim-fade-in-delay-2">
    <div class="flex items-end gap-5">
      <div class="w-[3px] h-16 bg-gradient-to-b from-cyan-400 to-transparent rounded-full"></div>
      <div>
        <div class="text-[10px] uppercase tracking-[0.35em] text-slate-500 mb-2 font-mono">Presenter</div>
        <div class="relative inline-block">
          <span class="electric-name">Dedik Romahadi</span>
          <span class="electric-spark electric-spark-1"></span>
          <span class="electric-spark electric-spark-2"></span>
          <span class="electric-spark electric-spark-3"></span>
        </div>
        <div class="flex items-center gap-3 mt-1.5 text-xs text-slate-400">
          <span>Beijing Institute of Technology</span><span class="text-slate-700">·</span><span class="font-mono text-slate-500">ID 3820222028</span>
        </div>
      </div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-green-400 rounded-full anim-pulse-strong"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Session Active</div>
    </div>
  </div>
</div>

<style>
:root { --slidev-slide-bg: #000000; }
.slidev-layout { background: #000000 !important; }
@keyframes eegFlow { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.anim-eeg-flow { animation: eegFlow 20s linear infinite; }
.anim-eeg-flow-slow { animation: eegFlow 35s linear infinite; }
@keyframes breatheSlow { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.anim-breathe-slow { animation: breatheSlow 8s ease-in-out infinite; }
.anim-breathe-slow-2 { animation: breatheSlow 10s ease-in-out infinite; animation-delay: -4s; }
@keyframes dotPulse { 0%, 100% { opacity: 0.3; transform: scale(1); } 50% { opacity: 1; transform: scale(1.5); } }
.anim-pulse-1 { animation: dotPulse 2.5s ease-in-out infinite; }
.anim-pulse-2 { animation: dotPulse 3.2s ease-in-out infinite; animation-delay: -1s; }
.anim-pulse-3 { animation: dotPulse 4s ease-in-out infinite; animation-delay: -2s; }
@keyframes strongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.anim-pulse-strong { animation: strongPulse 1.8s ease-in-out infinite; }
@keyframes ringPulse { 0% { transform: scale(1); opacity: 0.8; } 100% { transform: scale(1.4); opacity: 0; } }
.anim-ring-pulse { animation: ringPulse 2.5s ease-out infinite; }
.anim-ring-pulse-delay { animation: ringPulse 2.5s ease-out infinite; animation-delay: -1.25s; }
@keyframes crosshairFloat { 0%, 100% { transform: rotate(0deg); } 50% { transform: rotate(90deg); } }
.anim-crosshair { animation: crosshairFloat 12s ease-in-out infinite; }
@keyframes dotBlink { 0%, 100% { opacity: 1; } 50% { opacity: 0.3; } }
.anim-dot-blink { animation: dotBlink 1.5s ease-in-out infinite; }
@keyframes logoGlow { 0%, 100% { filter: drop-shadow(0 0 8px rgba(34, 211, 238, 0.3)); } 50% { filter: drop-shadow(0 0 16px rgba(168, 85, 247, 0.4)); } }
.anim-logo-glow { animation: logoGlow 4s ease-in-out infinite; }
@keyframes scanLine { 0% { top: -5%; } 100% { top: 105%; } }
.anim-scan-line { animation: scanLine 6s linear infinite; }
@keyframes driftX1 { 0%, 100% { transform: translateX(0); } 50% { transform: translateX(-18px); } }
@keyframes driftX2 { 0%, 100% { transform: translateX(0); } 50% { transform: translateX(20px); } }
@keyframes driftX3 { 0%, 100% { transform: translateX(0); } 50% { transform: translateX(-14px); } }
.anim-drift-x-1 { animation: driftX1 6s ease-in-out infinite; }
.anim-drift-x-2 { animation: driftX2 8s ease-in-out infinite; animation-delay: -2s; }
.anim-drift-x-3 { animation: driftX3 7s ease-in-out infinite; animation-delay: -1s; }
@keyframes hover1 { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-6px); } }
@keyframes hover2 { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-4px); } }
.anim-hover-1 { animation: hover1 3s ease-in-out infinite; }
.anim-hover-2 { animation: hover2 2.5s ease-in-out infinite; animation-delay: -0.8s; }
@keyframes shadowPulse { 0%, 100% { transform: scaleX(1); opacity: 0.4; } 50% { transform: scaleX(0.6); opacity: 0.2; } }
.anim-shadow-1 { animation: shadowPulse 3s ease-in-out infinite; }
.anim-shadow-2 { animation: shadowPulse 2.5s ease-in-out infinite; animation-delay: -0.8s; }
@keyframes rotorPulse { 0%, 100% { opacity: 0.9; } 50% { opacity: 0.25; } }
.anim-rotor-pulse-1 { animation: rotorPulse 0.35s linear infinite; }
.anim-rotor-pulse-2 { animation: rotorPulse 0.35s linear infinite; animation-delay: -0.08s; }
.anim-rotor-pulse-3 { animation: rotorPulse 0.35s linear infinite; animation-delay: -0.17s; }
.anim-rotor-pulse-4 { animation: rotorPulse 0.35s linear infinite; animation-delay: -0.25s; }
@keyframes signalRing { 0% { transform: scale(0.6); opacity: 0.8; } 100% { transform: scale(1.6); opacity: 0; } }
.anim-signal-1 { animation: signalRing 3s ease-out infinite; }
.anim-signal-2 { animation: signalRing 3s ease-out infinite; animation-delay: -1.5s; }
.anim-signal-3 { animation: signalRing 3.5s ease-out infinite; animation-delay: -1s; }
@keyframes ugvRock { 0%, 100% { transform: translateY(0) rotate(0deg); } 25% { transform: translateY(-0.5px) rotate(0.8deg); } 75% { transform: translateY(-0.5px) rotate(-0.8deg); } }
.anim-ugv-rock { animation: ugvRock 2.5s ease-in-out infinite; }
@keyframes sensorBlink { 0%, 100% { opacity: 1; } 50% { opacity: 0.3; } }
.anim-sensor-blink { animation: sensorBlink 1s ease-in-out infinite; }
@keyframes scanCone { 0%, 100% { opacity: 0; } 50% { opacity: 1; } }
.anim-scan-cone { animation: scanCone 2s ease-in-out infinite; }
@keyframes wheelPulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }
.anim-wheel-pulse-1 { animation: wheelPulse 0.8s ease-in-out infinite; }
.anim-wheel-pulse-2 { animation: wheelPulse 0.8s ease-in-out infinite; animation-delay: -0.4s; }
@keyframes fadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes slideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.anim-fade-in { animation: fadeIn 0.8s ease-out both; }
.anim-fade-in-delay { animation: fadeIn 0.8s ease-out 0.2s both; }
.anim-fade-in-delay-2 { animation: fadeIn 0.8s ease-out 1.2s both; }
.anim-fade-in-delay-3 { animation: fadeIn 1s ease-out 1.4s both; }
.anim-fade-in-delay-3b { animation: fadeIn 1s ease-out 1.7s both; }
.anim-slide-in { animation: slideIn 0.8s ease-out 0.4s both; }
.anim-slide-in-delay { animation: slideIn 0.8s ease-out 0.6s both; }
.anim-slide-in-delay-2 { animation: slideIn 0.8s ease-out 0.8s both; }
.anim-slide-in-delay-3 { animation: slideIn 0.8s ease-out 1s both; }

/* ========== ELECTRIC NAME EFFECT ========== */
.electric-name {
  display: inline-block;
  font-size: 1.35rem;
  font-weight: 600;
  line-height: 1.1;
  background: linear-gradient(90deg, #67e8f9 0%, #ffffff 25%, #e879f9 50%, #ffffff 75%, #67e8f9 100%);
  background-size: 200% 100%;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: electricShimmer 3s linear infinite, electricGlow 2s ease-in-out infinite;
  position: relative;
}
@keyframes electricShimmer {
  0%   { background-position: 200% 50%; }
  100% { background-position: -200% 50%; }
}
@keyframes electricGlow {
  0%, 100% {
    filter: drop-shadow(0 0 4px rgba(103, 232, 249, 0.8))
            drop-shadow(0 0 8px rgba(56, 189, 248, 0.5))
            drop-shadow(0 0 12px rgba(168, 85, 247, 0.3));
  }
  50% {
    filter: drop-shadow(0 0 6px rgba(232, 121, 249, 0.9))
            drop-shadow(0 0 14px rgba(103, 232, 249, 0.6))
            drop-shadow(0 0 20px rgba(56, 189, 248, 0.4));
  }
}
.electric-spark {
  position: absolute;
  width: 2px;
  height: 2px;
  background: #ffffff;
  border-radius: 50%;
  box-shadow: 0 0 6px 2px rgba(103, 232, 249, 0.9),
              0 0 12px 4px rgba(56, 189, 248, 0.5);
  pointer-events: none;
  opacity: 0;
}
.electric-spark-1 {
  top: 10%;
  left: 20%;
  animation: sparkJump1 2.5s ease-in-out infinite;
}
.electric-spark-2 {
  top: 80%;
  left: 55%;
  animation: sparkJump2 3s ease-in-out infinite;
  animation-delay: -0.8s;
}
.electric-spark-3 {
  top: 30%;
  left: 85%;
  animation: sparkJump3 2.8s ease-in-out infinite;
  animation-delay: -1.5s;
}
@keyframes sparkJump1 {
  0%, 100% { opacity: 0; transform: translate(0, 0) scale(0.5); }
  10% { opacity: 1; transform: translate(0, 0) scale(1); }
  50% { opacity: 1; transform: translate(40px, -8px) scale(0.8); }
  90% { opacity: 0.3; transform: translate(80px, 4px) scale(0.4); }
}
@keyframes sparkJump2 {
  0%, 100% { opacity: 0; transform: translate(0, 0) scale(0.5); }
  15% { opacity: 1; transform: translate(0, 0) scale(1); }
  50% { opacity: 1; transform: translate(-30px, 6px) scale(0.7); }
  85% { opacity: 0.2; transform: translate(-60px, -4px) scale(0.3); }
}
@keyframes sparkJump3 {
  0%, 100% { opacity: 0; transform: translate(0, 0) scale(0.5); }
  20% { opacity: 1; transform: translate(0, 0) scale(1); }
  55% { opacity: 1; transform: translate(20px, -10px) scale(0.8); }
  90% { opacity: 0.3; transform: translate(40px, 6px) scale(0.4); }
}
/* ========== NEW UAV / UGV ANIMATIONS (from closing slide) ========== */
@keyframes sendUavHover {
  0%, 100% { transform: translate(0, 0); }
  25% { transform: translate(-3px, -4px); }
  50% { transform: translate(0, -7px); }
  75% { transform: translate(3px, -4px); }
}
.send-uav-hover { animation: sendUavHover 4s ease-in-out infinite; }
@keyframes sendUavShadow {
  0%, 100% { opacity: 0.25; transform: scale(1); }
  50% { opacity: 0.1; transform: scale(0.75); }
}
.send-uav-shadow { animation: sendUavShadow 4s ease-in-out infinite; transform-origin: center; transform-box: fill-box; }
@keyframes sendRotorCw { to { transform: rotate(360deg); } }
.send-rotor-cw { animation: sendRotorCw 0.12s linear infinite; }
@keyframes sendRotorCcw { to { transform: rotate(-360deg); } }
.send-rotor-ccw { animation: sendRotorCcw 0.12s linear infinite; }
@keyframes sendBeacon {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.25; }
}
.send-beacon { animation: sendBeacon 0.9s ease-in-out infinite; }
@keyframes sendUgvBob {
  0%, 100% { transform: translate(0, 0) rotate(0deg); }
  20% { transform: translate(0, -1.5px) rotate(-0.6deg); }
  40% { transform: translate(0, 0) rotate(0deg); }
  60% { transform: translate(0, -2px) rotate(0.8deg); }
  80% { transform: translate(0, -0.5px) rotate(-0.3deg); }
}
.send-ugv-bob { animation: sendUgvBob 1.2s ease-in-out infinite; transform-origin: 70px 95px; transform-box: fill-box; }
@keyframes sendWheelSpin { to { transform: rotate(-720deg); } }
.send-wheel-spin { animation: sendWheelSpin 0.8s linear infinite; }
@keyframes sendGroundScroll { from { stroke-dashoffset: 0; } to { stroke-dashoffset: -18; } }
.send-ground-scroll { animation: sendGroundScroll 0.5s linear infinite; }
@keyframes sendAntennaPulse {
  0%, 100% { opacity: 1; r: 2.5; }
  50% { opacity: 0.4; r: 1.5; }
}
.send-antenna-pulse { animation: sendAntennaPulse 1s ease-in-out infinite; }
@keyframes sendCameraPulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.35; }
}
.send-camera-pulse { animation: sendCameraPulse 1.3s ease-in-out infinite; }
@keyframes sendSignalWave {
  0% { opacity: 0; }
  40% { opacity: 0.8; }
  100% { opacity: 0; }
}
.send-signal-a { animation: sendSignalWave 1.2s ease-in-out infinite; }
.send-signal-b { animation: sendSignalWave 1.2s ease-in-out infinite; animation-delay: -0.4s; }
@keyframes sendHeadlight {
  0%, 100% { opacity: 0.15; }
  50% { opacity: 0.4; }
}
.send-headlight { animation: sendHeadlight 1.5s ease-in-out infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-cyan-500/10 rounded-full blur-[140px] s2-breathe-1"></div>
  <div class="absolute bottom-[-15%] right-[-10%] w-[550px] h-[550px] bg-fuchsia-500/10 rounded-full blur-[140px] s2-breathe-2"></div>
</div>
<div class="absolute inset-0 opacity-[0.12] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s2-eeg" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q150,420 300,450 T600,450 Q750,380 900,450 T1200,450 Q1350,500 1500,450 T1800,450 Q1950,400 2100,450 T2400,450 Q2550,500 2700,450 T3000,450 L3200,450" fill="none" stroke="#22d3ee" stroke-width="0.8"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[15%] left-[75%] w-1 h-1 bg-cyan-400 rounded-full s2-float-1"></div>
  <div class="absolute top-[35%] left-[82%] w-1 h-1 bg-fuchsia-400 rounded-full s2-float-2"></div>
  <div class="absolute top-[60%] left-[78%] w-1.5 h-1.5 bg-cyan-300 rounded-full s2-float-3"></div>
  <div class="absolute top-[80%] left-[85%] w-1 h-1 bg-fuchsia-300 rounded-full s2-float-1"></div>
  <div class="absolute top-[25%] left-[8%] w-1 h-1 bg-cyan-400 rounded-full s2-float-2"></div>
  <div class="absolute top-[70%] left-[6%] w-1 h-1 bg-fuchsia-400 rounded-full s2-float-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-cyan-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent s2-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col py-6 px-16">
  <div class="flex items-center justify-between mb-2 s2-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-cyan-400 rounded-full s2-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono">Slide 02 · Outline</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="mb-5 s2-slide-in">
    <div class="flex items-center gap-3 mb-2">
      <div class="h-px w-8 bg-cyan-400 opacity-60"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono opacity-80">Presentation Agenda</div>
    </div>
    <h1 class="!text-[2.2rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
      <span class="text-white">Table of </span><span class="bg-gradient-to-r from-cyan-300 via-sky-300 to-fuchsia-300 bg-clip-text text-transparent">Contents</span>
    </h1>
  </div>
  <div class="flex-1 flex items-center justify-center">
    <div class="relative max-w-4xl w-full">
      <div class="absolute left-[26px] top-[26px] bottom-[26px] w-[2px] bg-gradient-to-b from-cyan-400/60 via-sky-400/60 to-fuchsia-400/60 s2-line-grow origin-top"></div>
      <div class="relative flex items-start gap-6 mb-4 s2-step-1">
        <div class="relative flex-shrink-0">
          <div class="absolute inset-0 rounded-full bg-cyan-400/30 blur-md s2-node-glow-1"></div>
          <div class="relative w-[54px] h-[54px] rounded-full p-[2px] bg-gradient-to-br from-cyan-400 to-sky-500">
            <div class="w-full h-full rounded-full bg-slate-950 flex items-center justify-center relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-br from-cyan-500/20 to-transparent"></div>
              <span class="relative text-cyan-300 font-bold text-lg font-mono">01</span>
            </div>
          </div>
        </div>
        <div class="flex-1 pt-1">
          <div class="flex items-center gap-2 mb-0.5">
            <h2 class="!text-[1.4rem] !font-bold !text-white !m-0 tracking-tight">Experimental Setup</h2>
            <svg class="w-4 h-4 text-cyan-400 s2-icon-float" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
              <path d="M9 3h6M10 3v6L4 20a1 1 0 0 0 1 1h14a1 1 0 0 0 1-1l-6-11V3"/>
              <path d="M7 15h10"/>
            </svg>
          </div>
          <p class="!text-xs !text-slate-400 !m-0 !leading-relaxed font-light max-w-xl">Cross-scenario paradigm design, hardware configuration, and data acquisition protocol.</p>
          <div class="mt-1.5 h-[1.5px] w-16 bg-gradient-to-r from-cyan-400 to-transparent"></div>
        </div>
        <div class="text-[9px] font-mono text-slate-600 tracking-[0.2em] pt-3">P. 03</div>
      </div>
      <div class="relative flex items-start gap-6 mb-4 s2-step-2">
        <div class="relative flex-shrink-0">
          <div class="absolute inset-0 rounded-full bg-sky-400/30 blur-md s2-node-glow-2"></div>
          <div class="relative w-[54px] h-[54px] rounded-full p-[2px] bg-gradient-to-br from-sky-400 to-blue-500">
            <div class="w-full h-full rounded-full bg-slate-950 flex items-center justify-center relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-br from-sky-500/20 to-transparent"></div>
              <span class="relative text-sky-300 font-bold text-lg font-mono">02</span>
            </div>
          </div>
        </div>
        <div class="flex-1 pt-1">
          <div class="flex items-center gap-2 mb-0.5">
            <h2 class="!text-[1.4rem] !font-bold !text-white !m-0 tracking-tight">Methodology</h2>
            <svg class="w-4 h-4 text-sky-400 s2-icon-float-2" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
              <circle cx="12" cy="12" r="2"/>
              <circle cx="4" cy="6" r="1.5"/>
              <circle cx="20" cy="6" r="1.5"/>
              <circle cx="4" cy="18" r="1.5"/>
              <circle cx="20" cy="18" r="1.5"/>
              <path d="M5.5 7l5 4M18.5 7l-5 4M5.5 17l5-4M18.5 17l-5-4"/>
            </svg>
          </div>
          <p class="!text-xs !text-slate-400 !m-0 !leading-relaxed font-light max-w-xl">Handcrafted–deep feature fusion, EEG + Eye-Gaze processing pipeline, and transfer learning strategy.</p>
          <div class="mt-1.5 h-[1.5px] w-16 bg-gradient-to-r from-sky-400 to-transparent"></div>
        </div>
        <div class="text-[9px] font-mono text-slate-600 tracking-[0.2em] pt-3">P. 08</div>
      </div>
      <div class="relative flex items-start gap-6 mb-4 s2-step-3">
        <div class="relative flex-shrink-0">
          <div class="absolute inset-0 rounded-full bg-purple-400/30 blur-md s2-node-glow-3"></div>
          <div class="relative w-[54px] h-[54px] rounded-full p-[2px] bg-gradient-to-br from-purple-400 to-fuchsia-500">
            <div class="w-full h-full rounded-full bg-slate-950 flex items-center justify-center relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-br from-purple-500/20 to-transparent"></div>
              <span class="relative text-purple-300 font-bold text-lg font-mono">03</span>
            </div>
          </div>
        </div>
        <div class="flex-1 pt-1">
          <div class="flex items-center gap-2 mb-0.5">
            <h2 class="!text-[1.4rem] !font-bold !text-white !m-0 tracking-tight">Experimental Results</h2>
            <svg class="w-4 h-4 text-purple-400 s2-icon-float" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
              <path d="M3 3v18h18"/>
              <path d="M7 15l4-6 4 3 5-7"/>
              <circle cx="7" cy="15" r="1" fill="currentColor"/>
              <circle cx="11" cy="9" r="1" fill="currentColor"/>
              <circle cx="15" cy="12" r="1" fill="currentColor"/>
              <circle cx="20" cy="5" r="1" fill="currentColor"/>
            </svg>
          </div>
          <p class="!text-xs !text-slate-400 !m-0 !leading-relaxed font-light max-w-xl">Preliminary findings, classification performance, and cross-scenario transfer accuracy.</p>
          <div class="mt-1.5 h-[1.5px] w-16 bg-gradient-to-r from-purple-400 to-transparent"></div>
        </div>
        <div class="text-[9px] font-mono text-slate-600 tracking-[0.2em] pt-3">P. 14</div>
      </div>
      <div class="relative flex items-start gap-6 s2-step-4">
        <div class="relative flex-shrink-0">
          <div class="absolute inset-0 rounded-full bg-fuchsia-400/30 blur-md s2-node-glow-4"></div>
          <div class="relative w-[54px] h-[54px] rounded-full p-[2px] bg-gradient-to-br from-fuchsia-400 to-pink-500">
            <div class="w-full h-full rounded-full bg-slate-950 flex items-center justify-center relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-br from-fuchsia-500/20 to-transparent"></div>
              <span class="relative text-fuchsia-300 font-bold text-lg font-mono">04</span>
            </div>
          </div>
        </div>
        <div class="flex-1 pt-1">
          <div class="flex items-center gap-2 mb-0.5">
            <h2 class="!text-[1.4rem] !font-bold !text-white !m-0 tracking-tight">Summary</h2>
            <svg class="w-4 h-4 text-fuchsia-400 s2-icon-float-2" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
              <path d="M4 21V4h12l-2 4 2 4H4"/>
              <path d="M4 21V12"/>
            </svg>
          </div>
          <p class="!text-xs !text-slate-400 !m-0 !leading-relaxed font-light max-w-xl">Key contributions, research implications, and future directions.</p>
          <div class="mt-1.5 h-[1.5px] w-16 bg-gradient-to-r from-fuchsia-400 to-transparent"></div>
        </div>
        <div class="text-[9px] font-mono text-slate-600 tracking-[0.2em] pt-3">P. 20</div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between s2-fade-in-last mt-2">
    <div class="flex items-center gap-3">
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">4 Sections · ~25 min</div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-green-400 rounded-full s2-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Ready to Begin</div>
    </div>
  </div>
</div>

<style>
@keyframes s2EegFlow { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.s2-eeg { animation: s2EegFlow 25s linear infinite; }
@keyframes s2Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s2-breathe-1 { animation: s2Breathe 8s ease-in-out infinite; }
.s2-breathe-2 { animation: s2Breathe 10s ease-in-out infinite; animation-delay: -4s; }
@keyframes s2Float1 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-10px, -8px); opacity: 1; } }
@keyframes s2Float2 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(8px, -10px); opacity: 1; } }
@keyframes s2Float3 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-6px, 10px); opacity: 1; } }
.s2-float-1 { animation: s2Float1 4s ease-in-out infinite; }
.s2-float-2 { animation: s2Float2 5s ease-in-out infinite; animation-delay: -1s; }
.s2-float-3 { animation: s2Float3 4.5s ease-in-out infinite; animation-delay: -2s; }
@keyframes s2StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.s2-strong-pulse { animation: s2StrongPulse 1.8s ease-in-out infinite; }
@keyframes s2ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s2-scan-line { animation: s2ScanLine 6s linear infinite; }
@keyframes s2LineGrow { from { transform: scaleY(0); } to { transform: scaleY(1); } }
.s2-line-grow { animation: s2LineGrow 2s cubic-bezier(0.65, 0, 0.35, 1) 0.8s both; }
@keyframes s2NodeGlow { 0%, 100% { opacity: 0.4; transform: scale(1); } 50% { opacity: 0.9; transform: scale(1.15); } }
.s2-node-glow-1 { animation: s2NodeGlow 3s ease-in-out infinite; }
.s2-node-glow-2 { animation: s2NodeGlow 3s ease-in-out infinite; animation-delay: -0.75s; }
.s2-node-glow-3 { animation: s2NodeGlow 3s ease-in-out infinite; animation-delay: -1.5s; }
.s2-node-glow-4 { animation: s2NodeGlow 3s ease-in-out infinite; animation-delay: -2.25s; }
@keyframes s2IconFloat { 0%, 100% { transform: translateY(0) rotate(0deg); } 50% { transform: translateY(-3px) rotate(-3deg); } }
@keyframes s2IconFloat2 { 0%, 100% { transform: translateY(0) rotate(0deg); } 50% { transform: translateY(-3px) rotate(3deg); } }
.s2-icon-float { animation: s2IconFloat 3s ease-in-out infinite; }
.s2-icon-float-2 { animation: s2IconFloat2 3.5s ease-in-out infinite; }
@keyframes s2StepIn { from { opacity: 0; transform: translateX(-30px); filter: blur(4px); } to { opacity: 1; transform: translateX(0); filter: blur(0); } }
.s2-step-1 { animation: s2StepIn 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.0s both; }
.s2-step-2 { animation: s2StepIn 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.4s both; }
.s2-step-3 { animation: s2StepIn 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.8s both; }
.s2-step-4 { animation: s2StepIn 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 2.2s both; }
@keyframes s2FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s2SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s2-fade-in { animation: s2FadeIn 0.8s ease-out both; }
.s2-slide-in { animation: s2SlideIn 0.8s ease-out 0.3s both; }
.s2-fade-in-last { animation: s2FadeIn 0.8s ease-out 2.8s both; }
</style>


---
transition: fade
---

<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-20%] left-[20%] w-[800px] h-[800px] bg-cyan-500/15 rounded-full blur-[160px] s3-breathe"></div>
  <div class="absolute bottom-[-20%] right-[10%] w-[700px] h-[700px] bg-sky-500/12 rounded-full blur-[160px] s3-breathe-2"></div>
</div>
<div class="absolute inset-0 opacity-[0.18] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s3-eeg" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q150,420 300,450 T600,450 Q750,380 900,450 T1200,450 Q1350,500 1500,450 T1800,450 Q1950,400 2100,450 T2400,450 Q2550,500 2700,450 T3000,450 L3200,450" fill="none" stroke="#22d3ee" stroke-width="0.8"/>
  </svg>
</div>
<div class="absolute inset-0 opacity-[0.12] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s3-eeg-2" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,250 Q80,250 130,230 T230,250 Q280,150 330,250 T430,250 Q480,310 530,250 T630,250 Q680,190 730,250 T830,250 Q880,270 930,250 T1030,250 Q1080,220 1130,250 T1230,250 Q1280,150 1330,250 T1430,250 Q1480,310 1530,250 T1630,250 L3200,250" fill="none" stroke="#67e8f9" stroke-width="1"/>
    <path d="M0,650 Q100,650 160,630 T260,650 Q310,710 360,650 T460,650 Q510,590 560,650 T660,650 Q710,670 760,650 T860,650 L3200,650" fill="none" stroke="#a855f7" stroke-width="1"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[15%] left-[10%] w-1 h-1 bg-cyan-400 rounded-full s3-particle-1"></div>
  <div class="absolute top-[25%] left-[85%] w-1.5 h-1.5 bg-cyan-300 rounded-full s3-particle-2"></div>
  <div class="absolute top-[75%] left-[12%] w-1 h-1 bg-sky-400 rounded-full s3-particle-3"></div>
  <div class="absolute top-[80%] left-[88%] w-1.5 h-1.5 bg-cyan-400 rounded-full s3-particle-1"></div>
  <div class="absolute top-[40%] left-[5%] w-1 h-1 bg-sky-300 rounded-full s3-particle-2"></div>
  <div class="absolute top-[55%] left-[92%] w-1 h-1 bg-cyan-300 rounded-full s3-particle-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-60"></div>
<div class="absolute top-6 left-6 w-8 h-8 border-l-2 border-t-2 border-cyan-400 opacity-60 s3-bracket-1"></div>
<div class="absolute top-6 right-6 w-8 h-8 border-r-2 border-t-2 border-cyan-400 opacity-60 s3-bracket-1"></div>
<div class="absolute bottom-6 left-6 w-8 h-8 border-l-2 border-b-2 border-cyan-400 opacity-60 s3-bracket-2"></div>
<div class="absolute bottom-6 right-6 w-8 h-8 border-r-2 border-b-2 border-cyan-400 opacity-60 s3-bracket-2"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-15">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent s3-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col">
  <div class="flex items-center justify-between px-16 py-4 s3-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-cyan-400 rounded-full s3-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono">Section Transition</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex-1 flex items-center justify-center px-16">
    <div class="relative w-full max-w-5xl">
      <div class="relative flex items-center justify-center mb-3 s3-number-wrap">
        <div class="absolute w-[180px] h-[180px] rounded-full bg-cyan-500/10 blur-3xl s3-aura"></div>
        <div class="absolute w-[120px] h-[120px] rounded-full border border-cyan-400/20 s3-ring-1"></div>
        <div class="absolute w-[155px] h-[155px] rounded-full border border-cyan-400/15 s3-ring-2"></div>
        <div class="absolute w-[190px] h-[190px] rounded-full border border-cyan-400/10 s3-ring-3"></div>
        <div class="relative z-10 flex items-baseline gap-1">
          <span class="text-[5.5rem] font-black leading-none tracking-tighter bg-gradient-to-b from-cyan-300 via-sky-400 to-blue-600 bg-clip-text text-transparent s3-number-glow">01</span>
          <span class="text-[1.1rem] font-light text-slate-600 font-mono tracking-wider">/ 04</span>
        </div>
      </div>
      <div class="text-center s3-label-wrap">
        <div class="flex items-center justify-center gap-4 mb-2">
          <div class="h-px w-12 bg-gradient-to-r from-transparent to-cyan-400"></div>
          <div class="text-[10px] uppercase tracking-[0.5em] text-cyan-400 font-mono">Section One</div>
          <div class="h-px w-12 bg-gradient-to-l from-transparent to-cyan-400"></div>
        </div>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight s3-title">
          <span class="bg-gradient-to-r from-white via-cyan-100 to-white bg-clip-text text-transparent">EXPERIMENTAL</span>
        </h1>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight mt-1 s3-title-2">
          <span class="bg-gradient-to-r from-cyan-300 via-sky-300 to-cyan-300 bg-clip-text text-transparent">SETUP</span>
        </h1>
        <div class="mt-4 max-w-2xl mx-auto s3-subtitle">
          <p class="!text-xs !text-slate-400 !m-0 font-light tracking-wide leading-relaxed">
            Cross-scenario paradigm design · Hardware configuration · Data acquisition protocol
          </p>
        </div>
      </div>
      <div class="flex items-center justify-center gap-2 mt-4 s3-dots">
        <div class="w-8 h-[2px] bg-cyan-400 rounded-full"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between px-16 py-4 s3-fade-in-last">
    <div class="flex items-center gap-3">
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Paper 01 · Proposal</div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-cyan-400 rounded-full s3-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Entering Section</div>
    </div>
  </div>
</div>

<style>
@keyframes s3Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.1); } }
.s3-breathe { animation: s3Breathe 10s ease-in-out infinite; }
.s3-breathe-2 { animation: s3Breathe 12s ease-in-out infinite; animation-delay: -5s; }
@keyframes s3EegFlow { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.s3-eeg { animation: s3EegFlow 30s linear infinite; }
.s3-eeg-2 { animation: s3EegFlow 22s linear infinite; }
@keyframes s3Particle1 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-12px, -10px); opacity: 1; } }
@keyframes s3Particle2 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(10px, -12px); opacity: 1; } }
@keyframes s3Particle3 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-8px, 12px); opacity: 1; } }
.s3-particle-1 { animation: s3Particle1 5s ease-in-out infinite; }
.s3-particle-2 { animation: s3Particle2 6s ease-in-out infinite; animation-delay: -1.5s; }
.s3-particle-3 { animation: s3Particle3 5.5s ease-in-out infinite; animation-delay: -2.5s; }
@keyframes s3StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 14px currentColor; } }
.s3-strong-pulse { animation: s3StrongPulse 1.8s ease-in-out infinite; }
@keyframes s3ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s3-scan-line { animation: s3ScanLine 5s linear infinite; }
@keyframes s3BracketPulse1 { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.08); } }
.s3-bracket-1 { animation: s3BracketPulse1 4s ease-in-out infinite; transform-origin: top left; }
.s3-bracket-2 { animation: s3BracketPulse1 4s ease-in-out infinite; animation-delay: -2s; transform-origin: bottom right; }
@keyframes s3Aura { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.15); } }
.s3-aura { animation: s3Aura 4s ease-in-out infinite; }
@keyframes s3RingRotate1 { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
@keyframes s3RingRotate2 { from { transform: rotate(0deg); } to { transform: rotate(-360deg); } }
@keyframes s3RingPulse { 0%, 100% { opacity: 0.4; } 50% { opacity: 0.9; } }
.s3-ring-1 { animation: s3RingRotate1 40s linear infinite, s3RingPulse 3s ease-in-out infinite; }
.s3-ring-2 { animation: s3RingRotate2 60s linear infinite, s3RingPulse 3s ease-in-out infinite; animation-delay: -1s; }
.s3-ring-3 { animation: s3RingRotate1 80s linear infinite, s3RingPulse 3s ease-in-out infinite; animation-delay: -2s; }
@keyframes s3NumberGlow {
  0%, 100% { filter: drop-shadow(0 0 20px rgba(34, 211, 238, 0.4)) drop-shadow(0 0 40px rgba(56, 189, 248, 0.2)); }
  50% { filter: drop-shadow(0 0 30px rgba(103, 232, 249, 0.6)) drop-shadow(0 0 60px rgba(34, 211, 238, 0.3)); }
}
.s3-number-glow { animation: s3NumberGlow 3s ease-in-out infinite; }
@keyframes s3NumberIn {
  from { opacity: 0; transform: scale(0.6); filter: blur(20px); }
  to { opacity: 1; transform: scale(1); filter: blur(0); }
}
.s3-number-wrap { animation: s3NumberIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) 0.3s both; }
@keyframes s3FadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
.s3-label-wrap { animation: s3FadeUp 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.0s both; }
@keyframes s3TitleIn {
  from { opacity: 0; transform: translateY(20px); letter-spacing: 0.5em; filter: blur(8px); }
  to { opacity: 1; transform: translateY(0); letter-spacing: -0.025em; filter: blur(0); }
}
.s3-title { animation: s3TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.2s both; }
.s3-title-2 { animation: s3TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.5s both; }
@keyframes s3SubIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
.s3-subtitle { animation: s3SubIn 0.8s ease-out 2.0s both; }
.s3-dots { animation: s3SubIn 0.8s ease-out 2.3s both; }
@keyframes s3FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
.s3-fade-in { animation: s3FadeIn 0.8s ease-out both; }
.s3-fade-in-last { animation: s3FadeIn 0.8s ease-out 2.5s both; }
</style>

---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s4-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[550px] h-[550px] bg-cyan-500/8 rounded-full blur-[140px] s4-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[20%] w-[500px] h-[500px] bg-amber-500/6 rounded-full blur-[140px] s4-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-cyan-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent s4-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col py-4 px-10">
  <div class="flex items-center justify-between mb-2 s4-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-cyan-400 rounded-full s4-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono">Slide 04 · Experimental Setup</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="mb-3 s4-slide-in">
    <div class="flex items-center gap-2 mb-1.5">
      <div class="h-[2px] w-12 bg-cyan-400 rounded-full s4-bar-pulse-1"></div>
      <div class="h-[2px] w-20 bg-sky-400 rounded-full s4-bar-pulse-2"></div>
      <div class="h-[2px] w-8 bg-fuchsia-400 rounded-full s4-bar-pulse-3"></div>
      <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/40 via-cyan-400/20 to-transparent ml-1"></div>
      <div class="w-1 h-1 rounded-full bg-cyan-400 s4-strong-pulse"></div>
    </div>
    <h1 class="!text-[1.7rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
      <span class="text-white">Data Acquisition </span><span class="bg-gradient-to-r from-cyan-300 via-sky-300 to-fuchsia-300 bg-clip-text text-transparent">Setup</span>
    </h1>
  </div>
  <div class="grid grid-cols-[1fr_24px_1fr_24px_1fr_24px_1fr] gap-x-2 mb-1 s4-header-fade items-center">
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-400 font-mono text-center">Source</div>
    <div></div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-400 font-mono text-center">Device / Software</div>
    <div></div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-400 font-mono text-center">Stream · Rate</div>
    <div></div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-400 font-mono text-center">Synchronization</div>
  </div>
  <div class="flex-1 relative">
    <div class="absolute inset-0 pointer-events-none">
      <div class="absolute top-0 bottom-0 right-0 w-[23%] border border-cyan-400/20 rounded-2xl s4-matlab-frame"></div>
    </div>
    <div class="relative h-full grid grid-cols-[1fr_24px_1fr_24px_1fr_24px_1fr] gap-x-2 gap-y-3 items-center py-2">
      <div class="s4-card-1 relative neon-card-pink">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-fuchsia-300 s4-icon-eeg" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <path d="M12 22 A12 12 0 0 1 36 22 L36 28 A12 12 0 0 1 12 28 Z"/>
              <circle cx="17" cy="20" r="1.5" fill="currentColor"/>
              <circle cx="24" cy="18" r="1.5" fill="currentColor"/>
              <circle cx="31" cy="20" r="1.5" fill="currentColor"/>
              <circle cx="15" cy="26" r="1.5" fill="currentColor"/>
              <circle cx="33" cy="26" r="1.5" fill="currentColor"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Subject</div>
            <div class="text-[0.7rem] text-fuchsia-200/70 mt-0.5">Wearing EEG cap</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-1 flex items-center justify-center">
        <svg class="w-full h-4 text-fuchsia-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-pink"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-pink"/>
        </svg>
      </div>
      <div class="s4-card-2 relative neon-card-pink">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-fuchsia-300 s4-icon-amp" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <line x1="18" y1="6" x2="18" y2="14" stroke-linecap="round"/>
              <line x1="30" y1="6" x2="30" y2="14" stroke-linecap="round"/>
              <circle cx="18" cy="6" r="1.2" fill="currentColor"/>
              <circle cx="30" cy="6" r="1.2" fill="currentColor"/>
              <rect x="12" y="14" width="24" height="26" rx="3"/>
              <circle cx="24" cy="26" r="2.5" fill="currentColor"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Neuracle</div>
            <div class="text-[0.7rem] text-fuchsia-200/70 mt-0.5">Wireless EEG amplifier</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-2 flex items-center justify-center">
        <svg class="w-full h-4 text-fuchsia-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-pink"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-pink"/>
        </svg>
      </div>
      <div class="s4-card-3 relative neon-card-pink">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-12 h-7 s4-icon-wave-wrap" viewBox="0 0 72 30" fill="none" stroke-width="1.8">
              <defs>
                <clipPath id="s4WaveClip">
                  <rect x="0" y="0" width="72" height="30"/>
                </clipPath>
              </defs>
              <line x1="0" y1="15" x2="72" y2="15" stroke="#e879f9" stroke-width="0.5" opacity="0.2"/>
              <g clip-path="url(#s4WaveClip)" stroke="#f0abfc" fill="none" stroke-linecap="round">
                <path class="s4-eeg-signal" d="M-72,15 Q-66,5 -60,15 T-48,15 Q-42,4 -36,15 T-24,15 Q-18,25 -12,15 T0,15 Q6,5 12,15 T24,15 Q30,4 36,15 T48,15 Q54,25 60,15 T72,15 Q78,5 84,15 T96,15 Q102,4 108,15 T120,15 Q126,25 132,15 T144,15"/>
              </g>
              <circle cx="68" cy="15" r="1.8" fill="#f0abfc" class="s4-eeg-dot"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Raw EEG</div>
            <div class="text-[0.7rem] text-fuchsia-200/70 mt-0.5 font-mono">1000 Hz · TCP/IP</div>
          </div>
        </div>
      </div>
      <div class="s4-dash-pink-1 flex items-center justify-center pr-1">
        <svg class="w-full h-12" viewBox="0 0 32 60" fill="none" preserveAspectRatio="none">
          <circle cx="4" cy="8" r="2" fill="#e879f9" class="s4-travel-pink-slow"/>
          <path d="M4 8 Q20 20 28 50" stroke="#e879f9" stroke-width="1" stroke-dasharray="3 3" fill="none" opacity="0.5"/>
          <path d="M24 46 L30 51 L27 45" stroke="#e879f9" stroke-width="1.5" stroke-linecap="round" fill="none" opacity="0.8"/>
        </svg>
      </div>
      <div class="s4-matlab row-span-3 flex items-center justify-center px-2">
        <div class="relative w-full neon-card-cyan">
          <div class="neon-card-inner-lg">
            <div class="flex justify-center mb-2">
              <svg class="w-11 h-11 text-cyan-200 s4-icon-sync" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
                <circle cx="14" cy="14" r="2.5" fill="currentColor"/>
                <circle cx="14" cy="24" r="2.5" fill="currentColor"/>
                <circle cx="14" cy="34" r="2.5" fill="currentColor"/>
                <circle cx="34" cy="24" r="3" fill="currentColor"/>
                <line x1="16" y1="14" x2="32" y2="24" stroke-linecap="round"/>
                <line x1="16" y1="24" x2="32" y2="24" stroke-linecap="round"/>
                <line x1="16" y1="34" x2="32" y2="24" stroke-linecap="round"/>
                <path d="M34 24 L44 24 M40 20 L44 24 L40 28" stroke-linecap="round"/>
              </svg>
            </div>
            <div class="text-center">
              <div class="text-[1.1rem] font-bold text-white leading-tight">MATLAB</div>
              <div class="text-[0.7rem] text-cyan-200/70 mt-1">Time alignment</div>
            </div>
          </div>
        </div>
      </div>
      <div class="s4-card-4 relative neon-card-cyan-light">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-11 h-6 text-cyan-300" viewBox="0 0 56 28" fill="none" stroke="currentColor" stroke-width="1.8">
              <rect x="4" y="6" width="48" height="16" rx="8"/>
              <circle cx="18" cy="14" r="3.5" fill="#0a0f1e" stroke="#67e8f9" stroke-width="1"/>
              <circle cx="38" cy="14" r="3.5" fill="#0a0f1e" stroke="#67e8f9" stroke-width="1"/>
              <circle class="s4-tracker-pupil-l" cx="18" cy="14" r="1.8" fill="#67e8f9" stroke="none"/>
              <circle class="s4-tracker-pupil-r" cx="38" cy="14" r="1.8" fill="#67e8f9" stroke="none"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Tobii Tracker</div>
            <div class="text-[0.7rem] text-cyan-200/70 mt-0.5">Screen-mounted</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-3 flex items-center justify-center">
        <svg class="w-full h-4 text-cyan-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-cyan"/>
        </svg>
      </div>
      <div class="s4-card-5 relative neon-card-cyan-light">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-cyan-300 s4-icon-monitor-wrap" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <defs>
                <clipPath id="s4MonitorScreen">
                  <rect x="9" y="11" width="30" height="20" rx="1"/>
                </clipPath>
              </defs>
              <rect x="8" y="10" width="32" height="22" rx="2"/>
              <line x1="18" y1="36" x2="30" y2="36" stroke-linecap="round"/>
              <line x1="24" y1="32" x2="24" y2="36" stroke-linecap="round"/>
              <circle cx="33" cy="15" r="1.2" fill="currentColor"/>
              <rect x="9" y="11" width="30" height="20" rx="1" fill="#67e8f9" class="s4-monitor-flash"/>
              <g clip-path="url(#s4MonitorScreen)">
                <circle cx="14" cy="16" r="1.5" fill="#67e8f9" class="s4-monitor-cursor" stroke="none"/>
              </g>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">CrossSceneSAR</div>
            <div class="text-[0.7rem] text-cyan-200/70 mt-0.5">Experiment software</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-4 flex items-center justify-center">
        <svg class="w-full h-4 text-cyan-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-cyan"/>
        </svg>
      </div>
      <div class="s4-card-6 relative neon-card-cyan-light">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-cyan-300 s4-icon-eye" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <path d="M6 24 Q24 10 42 24 Q24 38 6 24 Z"/>
              <circle cx="24" cy="24" r="5" fill="currentColor" fill-opacity="0.2"/>
              <circle cx="24" cy="24" r="2.5" fill="currentColor"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Gaze Data</div>
            <div class="text-[0.7rem] text-cyan-200/70 mt-0.5 font-mono">90 Hz · LSL</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-cyan-matlab flex items-center justify-center pr-1">
        <svg class="w-full h-4 text-cyan-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-cyan"/>
        </svg>
      </div>
      <div class="s4-card-7 relative neon-card-amber">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-amber-300 s4-icon-operator" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <circle cx="24" cy="16" r="5"/>
              <path d="M14 34 Q14 24 24 24 Q34 24 34 34 L34 38 L14 38 Z"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Operator</div>
            <div class="text-[0.7rem] text-amber-200/70 mt-0.5">Task responses</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-5 flex items-center justify-center">
        <svg class="w-full h-4 text-amber-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-amber"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-amber"/>
        </svg>
      </div>
      <div class="s4-card-8 relative neon-card-amber">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-amber-300 s4-icon-clipboard" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <rect x="12" y="10" width="24" height="32" rx="2"/>
              <rect x="18" y="6" width="12" height="6" rx="1"/>
              <line x1="18" y1="22" x2="30" y2="22" stroke-linecap="round"/>
              <line x1="18" y1="28" x2="30" y2="28" stroke-linecap="round"/>
              <line x1="18" y1="34" x2="26" y2="34" stroke-linecap="round"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">CrossSceneSAR</div>
            <div class="text-[0.7rem] text-amber-200/70 mt-0.5">Trial event logger</div>
          </div>
        </div>
      </div>
      <div class="s4-arrow-6 flex items-center justify-center">
        <svg class="w-full h-4 text-amber-400" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s4-dash-amber"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          <circle cx="4" cy="4" r="1.5" fill="currentColor" class="s4-travel-amber"/>
        </svg>
      </div>
      <div class="s4-card-9 relative neon-card-amber">
        <div class="neon-card-inner">
          <div class="flex justify-center mb-1">
            <svg class="w-9 h-9 text-amber-300 s4-icon-flag" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8">
              <line x1="14" y1="6" x2="14" y2="42" stroke-linecap="round"/>
              <path d="M14 10 L34 10 L30 17 L34 24 L14 24 Z" fill="currentColor" fill-opacity="0.3"/>
            </svg>
          </div>
          <div class="text-center">
            <div class="text-[0.95rem] font-bold text-white leading-tight">Event Marker</div>
            <div class="text-[0.7rem] text-amber-200/70 mt-0.5 font-mono">Async · LSL</div>
          </div>
        </div>
      </div>
      <div class="s4-dash-amber-1 flex items-center justify-center pr-1">
        <svg class="w-full h-12" viewBox="0 0 32 60" fill="none" preserveAspectRatio="none">
          <circle cx="4" cy="52" r="2" fill="#fbbf24" class="s4-travel-amber-slow"/>
          <path d="M4 52 Q20 40 28 10" stroke="#fbbf24" stroke-width="1" stroke-dasharray="3 3" fill="none" opacity="0.5"/>
          <path d="M24 14 L30 9 L27 15" stroke="#fbbf24" stroke-width="1.5" stroke-linecap="round" fill="none" opacity="0.8"/>
        </svg>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between mt-2 s4-fade-in-last">
    <div class="flex items-center gap-3">
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">3 Streams · Synchronized</div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-green-400 rounded-full s4-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Pipeline Active</div>
    </div>
  </div>
</div>

<style>
/* ============ NEON CARD STYLES ============ */
.neon-card-pink {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.65), 0 0 18px rgba(232, 121, 249, 0.35), inset 0 0 12px rgba(232, 121, 249, 0.08);
  animation: s4NeonGlowPink 3s ease-in-out infinite;
}
.neon-card-cyan-light {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.65), 0 0 18px rgba(103, 232, 249, 0.35), inset 0 0 12px rgba(103, 232, 249, 0.08);
  animation: s4NeonGlowCyan 3s ease-in-out infinite;
  animation-delay: -1s;
}
.neon-card-amber {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.65), 0 0 18px rgba(251, 191, 36, 0.35), inset 0 0 12px rgba(251, 191, 36, 0.08);
  animation: s4NeonGlowAmber 3s ease-in-out infinite;
  animation-delay: -2s;
}
.neon-card-cyan {
  border-radius: 16px;
  box-shadow: 0 0 0 1.5px rgba(165, 243, 252, 0.7), 0 0 25px rgba(103, 232, 249, 0.4), inset 0 0 16px rgba(103, 232, 249, 0.1);
  animation: s4NeonGlowMatlab 3s ease-in-out infinite;
}
.neon-card-inner {
  background: #0a0f1e;
  border-radius: 12px;
  padding: 10px 12px;
}
.neon-card-inner-lg {
  background: #0a0f1e;
  border-radius: 14px;
  padding: 18px 14px;
}
@keyframes s4NeonGlowPink {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.6), 0 0 15px rgba(232, 121, 249, 0.3), inset 0 0 12px rgba(232, 121, 249, 0.08); }
  50% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.9), 0 0 28px rgba(232, 121, 249, 0.55), inset 0 0 16px rgba(232, 121, 249, 0.15); }
}
@keyframes s4NeonGlowCyan {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.6), 0 0 15px rgba(103, 232, 249, 0.3), inset 0 0 12px rgba(103, 232, 249, 0.08); }
  50% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.9), 0 0 28px rgba(103, 232, 249, 0.55), inset 0 0 16px rgba(103, 232, 249, 0.15); }
}
@keyframes s4NeonGlowAmber {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.6), 0 0 15px rgba(251, 191, 36, 0.3), inset 0 0 12px rgba(251, 191, 36, 0.08); }
  50% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.9), 0 0 28px rgba(251, 191, 36, 0.55), inset 0 0 16px rgba(251, 191, 36, 0.15); }
}
@keyframes s4NeonGlowMatlab {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(165, 243, 252, 0.7), 0 0 22px rgba(103, 232, 249, 0.4), inset 0 0 16px rgba(103, 232, 249, 0.1); }
  50% { box-shadow: 0 0 0 1.5px rgba(165, 243, 252, 1), 0 0 40px rgba(103, 232, 249, 0.7), inset 0 0 22px rgba(103, 232, 249, 0.2); }
}
/* ============ MATLAB FRAME ============ */
@keyframes s4MatlabFrame { 0%, 100% { opacity: 0.25; } 50% { opacity: 0.45; } }
.s4-matlab-frame { animation: s4MatlabFrame 4s ease-in-out infinite; }
/* ============ BACKGROUND ============ */
@keyframes s4Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s4-breathe-1 { animation: s4Breathe 8s ease-in-out infinite; }
.s4-breathe-2 { animation: s4Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s4-breathe-3 { animation: s4Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s4ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s4-scan-line { animation: s4ScanLine 6s linear infinite; }
@keyframes s4StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.s4-strong-pulse { animation: s4StrongPulse 1.8s ease-in-out infinite; }
/* ============ ICON ANIMATIONS ============ */
/* SUBJECT EEG (electrodes) - electrodes berkedip bergiliran seperti sinyal masuk */
@keyframes s4EegNodes { 0%, 100% { opacity: 0.7; transform: scale(1); } 50% { opacity: 1; transform: scale(1.15); filter: drop-shadow(0 0 12px currentColor); } }
.s4-icon-eeg { animation: s4EegNodes 1.6s ease-in-out infinite; transform-origin: center; filter: drop-shadow(0 0 4px currentColor); }
.s4-icon-eeg circle:nth-child(2) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 0s; transform-origin: 14px 18px; }
.s4-icon-eeg circle:nth-child(3) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 0.2s; transform-origin: 24px 14px; }
.s4-icon-eeg circle:nth-child(4) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 0.4s; transform-origin: 34px 18px; }
.s4-icon-eeg circle:nth-child(5) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 0.6s; transform-origin: 12px 26px; }
.s4-icon-eeg circle:nth-child(6) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 0.8s; transform-origin: 36px 26px; }
.s4-icon-eeg circle:nth-child(7) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 1.0s; transform-origin: 18px 34px; }
.s4-icon-eeg circle:nth-child(8) { animation: s4EegNodes 1.6s ease-in-out infinite; animation-delay: 1.2s; transform-origin: 30px 34px; }

/* AMPLIFIER - LED merah/hijau berkedip seperti device aktif + antena memancarkan sinyal */
@keyframes s4AmpLed { 0%, 100% { opacity: 0.4; transform: scale(0.8); filter: drop-shadow(0 0 2px currentColor); } 50% { opacity: 1; transform: scale(1.4); filter: drop-shadow(0 0 10px currentColor); } }
.s4-icon-amp circle { animation: s4AmpLed 0.8s ease-in-out infinite; transform-origin: 24px 26px; }
@keyframes s4AmpAntenna { 0%, 100% { transform: translateY(0); opacity: 0.8; } 50% { transform: translateY(-1px); opacity: 1; filter: drop-shadow(0 0 6px currentColor); } }
.s4-icon-amp line { animation: s4AmpAntenna 1s ease-in-out infinite; transform-origin: bottom; }
.s4-icon-amp { filter: drop-shadow(0 0 4px currentColor); }

/* RAW EEG - sinyal terus mengalir kontinyu seperti realtime monitoring */
@keyframes s4EegSignalFlow {
  0% { transform: translateX(0); }
  100% { transform: translateX(-72px); }
}
.s4-eeg-signal { animation: s4EegSignalFlow 1.4s linear infinite; }
@keyframes s4EegDot { 0%, 100% { opacity: 0.6; r: 1.5; filter: drop-shadow(0 0 4px currentColor); } 50% { opacity: 1; r: 2.5; filter: drop-shadow(0 0 12px currentColor); } }
.s4-eeg-dot { animation: s4EegDot 0.4s ease-in-out infinite; }
.s4-icon-wave-wrap { filter: drop-shadow(0 0 5px #f0abfc); }

/* TOBII TRACKER - mata melirik kiri-kanan dengan jelas */
@keyframes s4TrackerLookLR {
  0%, 100% { transform: translateX(0); }
  20% { transform: translateX(-2.5px); }
  40% { transform: translateX(0); }
  60% { transform: translateX(2.5px); }
  80% { transform: translateX(0); }
}
.s4-tracker-pupil-l, .s4-tracker-pupil-r { animation: s4TrackerLookLR 3s ease-in-out infinite; }
@keyframes s4TrackerBlink {
  0%, 92%, 100% { transform: scaleY(1); }
  96% { transform: scaleY(0.05); }
}

/* MONITOR (CrossSceneSAR Experiment) - layar berkedip + cursor bergerak di area layar */
@keyframes s4MonitorFlash {
  0%, 100% { opacity: 0; }
  85% { opacity: 0; }
  87% { opacity: 0.18; }
  89% { opacity: 0; }
  92% { opacity: 0.25; }
  94% { opacity: 0; }
}
.s4-monitor-flash { animation: s4MonitorFlash 3s linear infinite; }
@keyframes s4MonitorCursor {
  0% { transform: translate(0, 0); }
  18% { transform: translate(0, 0); }
  22% { transform: translate(14px, 0); }
  40% { transform: translate(14px, 0); }
  44% { transform: translate(14px, 8px); }
  62% { transform: translate(14px, 8px); }
  66% { transform: translate(0, 8px); }
  84% { transform: translate(0, 8px); }
  88% { transform: translate(0, 0); }
  100% { transform: translate(0, 0); }
}
.s4-monitor-cursor { animation: s4MonitorCursor 4s steps(1, end) infinite; filter: drop-shadow(0 0 4px #67e8f9); }
.s4-icon-monitor-wrap { filter: drop-shadow(0 0 5px currentColor); }

/* GAZE EYE - eye darting + occasional blink */
@keyframes s4EyePupil {
  0%, 100% { transform: translateX(0); }
  20% { transform: translateX(-2px); }
  40% { transform: translateX(2px); }
  60% { transform: translateX(-1.5px); }
  80% { transform: translateX(1.5px); }
}
.s4-icon-eye circle:last-child { animation: s4EyePupil 2.5s ease-in-out infinite; transform-origin: 24px 24px; }
@keyframes s4EyeBlink {
  0%, 88%, 100% { transform: scaleY(1); }
  94% { transform: scaleY(0.08); }
}
.s4-icon-eye { animation: s4EyeBlink 4s ease-in-out infinite; transform-origin: center; transform-box: fill-box; filter: drop-shadow(0 0 5px currentColor); }

/* OPERATOR (person icon) - breathing dengan slight head tilt */
@keyframes s4OperatorBreath {
  0%, 100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-1.5px) scale(1.04); }
}
.s4-icon-operator { animation: s4OperatorBreath 2.2s ease-in-out infinite; transform-origin: center; transform-box: fill-box; filter: drop-shadow(0 0 4px currentColor); }
@keyframes s4OperatorHead {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(-5deg); }
  75% { transform: rotate(5deg); }
}
.s4-icon-operator circle { animation: s4OperatorHead 4s ease-in-out infinite; transform-origin: 24px 16px; }

/* CLIPBOARD - writing motion + paper lines blink */
@keyframes s4ClipboardWrite {
  0%, 100% { transform: rotate(-3deg) translateY(0); }
  25% { transform: rotate(0deg) translateY(-1px); }
  50% { transform: rotate(3deg) translateY(0); }
  75% { transform: rotate(0deg) translateY(-1px); }
}
.s4-icon-clipboard { animation: s4ClipboardWrite 2.5s ease-in-out infinite; transform-origin: center; transform-box: fill-box; filter: drop-shadow(0 0 4px currentColor); }
@keyframes s4ClipboardLines {
  0%, 50%, 100% { opacity: 1; }
  60% { opacity: 0.3; }
  70% { opacity: 1; }
}
.s4-icon-clipboard line { animation: s4ClipboardLines 2s ease-in-out infinite; }
.s4-icon-clipboard line:nth-of-type(2) { animation-delay: 0.1s; }
.s4-icon-clipboard line:nth-of-type(3) { animation-delay: 0.2s; }

/* FLAG (Event Marker) - bendera berkibar dramatis */
@keyframes s4FlagWave {
  0%, 100% { transform: skewX(-5deg) scaleX(1); }
  25% { transform: skewX(5deg) scaleX(1.05); }
  50% { transform: skewX(-3deg) scaleX(0.95); }
  75% { transform: skewX(7deg) scaleX(1.05); }
}
.s4-icon-flag path { animation: s4FlagWave 1.5s ease-in-out infinite; transform-origin: left center; transform-box: fill-box; }
.s4-icon-flag { filter: drop-shadow(0 0 5px currentColor); }

/* MATLAB SYNC HUB - ikon sync rotating + nodes pulsing in sequence */
@keyframes s4SyncRotate { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
.s4-icon-sync { animation: s4SyncRotate 8s linear infinite; transform-origin: center; transform-box: fill-box; filter: drop-shadow(0 0 6px currentColor); }
@keyframes s4SyncNode {
  0%, 100% { opacity: 0.5; transform: scale(0.85); filter: drop-shadow(0 0 2px currentColor); }
  50% { opacity: 1; transform: scale(1.3); filter: drop-shadow(0 0 10px currentColor); }
}
.s4-icon-sync circle:nth-child(1) { animation: s4SyncNode 1.2s ease-in-out infinite; animation-delay: 0s; transform-origin: 14px 14px; }
.s4-icon-sync circle:nth-child(2) { animation: s4SyncNode 1.2s ease-in-out infinite; animation-delay: 0.3s; transform-origin: 14px 24px; }
.s4-icon-sync circle:nth-child(3) { animation: s4SyncNode 1.2s ease-in-out infinite; animation-delay: 0.6s; transform-origin: 14px 34px; }
.s4-icon-sync circle:nth-child(4) { animation: s4SyncNode 1.2s ease-in-out infinite; animation-delay: 0.9s; transform-origin: 34px 24px; }
/* ============ ARROWS - DASH MARCHING ============ */
@keyframes s4DashMarch { to { stroke-dashoffset: -8; } }
.s4-dash-pink { animation: s4DashMarch 0.6s linear infinite; }
.s4-dash-cyan { animation: s4DashMarch 0.6s linear infinite; }
.s4-dash-amber { animation: s4DashMarch 0.6s linear infinite; }
/* ============ ARROWS - TRAVELING PACKET ============ */
@keyframes s4TravelRight {
  0% { transform: translateX(0); opacity: 0; }
  15% { opacity: 1; }
  85% { opacity: 1; }
  100% { transform: translateX(14px); opacity: 0; }
}
.s4-travel-pink { animation: s4TravelRight 1.5s ease-in-out infinite; filter: drop-shadow(0 0 3px currentColor); }
.s4-travel-cyan { animation: s4TravelRight 1.5s ease-in-out infinite; filter: drop-shadow(0 0 3px currentColor); animation-delay: -0.3s; }
.s4-travel-amber { animation: s4TravelRight 1.5s ease-in-out infinite; filter: drop-shadow(0 0 3px currentColor); animation-delay: -0.6s; }
/* Diagonal arrows (Pink top-right to MATLAB, Amber bottom-right to MATLAB) */
@keyframes s4TravelDiagPink {
  0% { transform: translate(0, 0); opacity: 0; }
  15% { opacity: 1; }
  85% { opacity: 1; }
  100% { transform: translate(22px, 42px); opacity: 0; }
}
.s4-travel-pink-slow { animation: s4TravelDiagPink 2.2s ease-in-out infinite; filter: drop-shadow(0 0 4px currentColor); }
@keyframes s4TravelDiagAmber {
  0% { transform: translate(0, 0); opacity: 0; }
  15% { opacity: 1; }
  85% { opacity: 1; }
  100% { transform: translate(22px, -42px); opacity: 0; }
}
.s4-travel-amber-slow { animation: s4TravelDiagAmber 2.2s ease-in-out infinite; filter: drop-shadow(0 0 4px currentColor); }
/* ============ ENTRY ANIMATIONS ============ */
@keyframes s4CardIn { from { opacity: 0; transform: translateY(20px) scale(0.95); filter: blur(4px); } to { opacity: 1; transform: translateY(0) scale(1); filter: blur(0); } }
.s4-card-1 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.6s both; }
.s4-card-2 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.75s both; }
.s4-card-3 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.9s both; }
.s4-card-4 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.7s both; }
.s4-card-5 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.85s both; }
.s4-card-6 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.0s both; }
.s4-card-7 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.8s both; }
.s4-card-8 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.95s both; }
.s4-card-9 { animation: s4CardIn 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.1s both; }
.s4-matlab { animation: s4CardIn 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.3s both; }
@keyframes s4ArrowIn { from { opacity: 0; } to { opacity: 1; } }
.s4-arrow-1, .s4-arrow-2 { animation: s4ArrowIn 0.4s ease-out 1.15s both; }
.s4-arrow-3, .s4-arrow-4 { animation: s4ArrowIn 0.4s ease-out 1.25s both; }
.s4-arrow-5, .s4-arrow-6 { animation: s4ArrowIn 0.4s ease-out 1.35s both; }
.s4-arrow-cyan-matlab { animation: s4ArrowIn 0.4s ease-out 1.4s both; }
.s4-dash-pink-1 { animation: s4ArrowIn 0.4s ease-out 1.4s both; }
.s4-dash-amber-1 { animation: s4ArrowIn 0.4s ease-out 1.4s both; }
@keyframes s4FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s4SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s4-fade-in { animation: s4FadeIn 0.8s ease-out both; }
.s4-slide-in { animation: s4SlideIn 0.8s ease-out 0.3s both; }
.s4-header-fade { animation: s4FadeIn 0.6s ease-out 0.5s both; }
.s4-fade-in-last { animation: s4FadeIn 0.8s ease-out 1.6s both; }
@keyframes sBarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s4-bar-pulse-1 { animation: sBarPulse 2.4s ease-in-out infinite; color: #67e8f9; transform-origin: left; }
.s4-bar-pulse-2 { animation: sBarPulse 2.4s ease-in-out infinite; color: #7dd3fc; animation-delay: -0.8s; transform-origin: left; }
.s4-bar-pulse-3 { animation: sBarPulse 2.4s ease-in-out infinite; color: #e879f9; animation-delay: -1.6s; transform-origin: left; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s5-breathe-1"></div>
  <div class="absolute bottom-[-10%] right-[-10%] w-[550px] h-[550px] bg-fuchsia-500/10 rounded-full blur-[140px] s5-breathe-2"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-fuchsia-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-fuchsia-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-fuchsia-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-fuchsia-300 to-transparent s5-scan-line"></div>
</div>
<div class="absolute top-3 left-10 right-10 flex items-center justify-between z-10 s5-fade-in">
  <div class="flex items-center gap-3">
    <div class="w-2 h-2 bg-fuchsia-400 rounded-full s5-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #e879f9; font-family: 'JetBrains Mono', monospace;">Slide 05 · Scenario 01</div>
  </div>
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Dedik Romahadi · BIT</div>
</div>
<div class="absolute top-12 left-10 right-10 z-10 s5-slide-in">
  <div class="flex items-center gap-3 mb-1">
    <div class="h-px w-8 bg-fuchsia-400 opacity-60"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #e879f9; opacity: 0.8; font-family: 'JetBrains Mono', monospace;">Scenario One · Baseline Task</div>
  </div>
  <div class="flex items-end justify-between">
    <h1 style="font-size: 1.5rem; line-height: 1.1; font-weight: 700; margin: 0; letter-spacing: -0.025em;">
      <span style="color: white;">Psychomotor </span><span class="bg-gradient-to-r from-fuchsia-300 via-pink-300 to-fuchsia-300 bg-clip-text text-transparent">Vigilance Task</span>
    </h1>
    <div class="flex items-center gap-4" style="font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase; color: #94a3b8; font-family: 'JetBrains Mono', monospace;">
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-full"></div>Trials · 200</div>
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-full"></div>ISI · 2-10 s</div>
    </div>
  </div>
</div>
<div class="absolute z-10 s5-video-wrap" style="top: 120px; left: 50%; transform: translateX(-50%); width: 700px; height: 394px;">
  <div class="absolute rounded-2xl bg-gradient-to-r from-fuchsia-500/30 via-pink-500/20 to-fuchsia-500/30 blur-xl s5-video-glow" style="inset: -4px;"></div>
  <div class="relative rounded-2xl overflow-hidden s5-video-frame" style="width: 100%; height: 100%;">
    <div class="relative" style="width: 100%; height: 100%; background: #0f172a;">
      <video autoplay muted loop playsinline style="position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover;">
        <source src="/scenario1-pvt.mp4" type="video/mp4"/>
      </video>
      <div class="absolute top-3 left-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-fuchsia-400/40">
        <div class="w-1.5 h-1.5 bg-red-500 rounded-full s5-rec-pulse"></div>
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">REC · PVT</div>
      </div>
      <div class="absolute top-3 right-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-fuchsia-400/40">
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: #f0abfc; font-family: 'JetBrains Mono', monospace;">01 / 03</div>
      </div>
      <div class="absolute bottom-3 left-3 right-3 flex items-center justify-between">
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-fuchsia-400/30">
          <svg class="w-3 h-3 text-fuchsia-300" viewBox="0 0 12 12" fill="currentColor"><circle cx="6" cy="6" r="2.5"/></svg>
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">Visual Stimulus · Button Response</div>
        </div>
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-fuchsia-400/30">
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">1920 × 1080</div>
        </div>
      </div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 right-10 flex items-center justify-between z-10 s5-fade-in-last">
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Reaction Time · Lapses · Response Accuracy</div>
  <div class="flex items-center gap-3">
    <div class="w-1.5 h-1.5 bg-green-400 rounded-full s5-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Recording</div>
  </div>
</div>

<style>
@keyframes s5Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s5-breathe-1 { animation: s5Breathe 8s ease-in-out infinite; }
.s5-breathe-2 { animation: s5Breathe 10s ease-in-out infinite; animation-delay: -3s; }
@keyframes s5ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s5-scan-line { animation: s5ScanLine 6s linear infinite; }
@keyframes s5StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.s5-strong-pulse { animation: s5StrongPulse 1.8s ease-in-out infinite; }
.s5-video-frame { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.7), 0 0 40px rgba(232, 121, 249, 0.3), inset 0 0 20px rgba(232, 121, 249, 0.08); animation: s5FrameGlow 4s ease-in-out infinite; }
@keyframes s5FrameGlow { 0%, 100% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.6), 0 0 30px rgba(232, 121, 249, 0.25), inset 0 0 20px rgba(232, 121, 249, 0.08); } 50% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 1), 0 0 55px rgba(232, 121, 249, 0.5), inset 0 0 30px rgba(232, 121, 249, 0.15); } }
@keyframes s5VideoGlow { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
.s5-video-glow { animation: s5VideoGlow 4s ease-in-out infinite; }
@keyframes s5VideoScan { 0% { top: 0%; } 100% { top: 100%; } }
.s5-video-scan { animation: s5VideoScan 3s linear infinite; }
@keyframes s5PlayPulse { 0%, 100% { transform: scale(1); opacity: 0.9; filter: drop-shadow(0 0 10px currentColor); } 50% { transform: scale(1.08); opacity: 1; filter: drop-shadow(0 0 20px currentColor); } }
.s5-play-icon { animation: s5PlayPulse 2s ease-in-out infinite; }
@keyframes s5CirclePulse { 0%, 100% { transform: scale(1); opacity: 0.6; } 50% { transform: scale(1.15); opacity: 0.2; } }
.s5-circle-pulse { animation: s5CirclePulse 2s ease-in-out infinite; transform-origin: center; transform-box: fill-box; }
@keyframes s5Dots { 0%, 80%, 100% { opacity: 0.3; transform: scale(0.8); } 40% { opacity: 1; transform: scale(1.3); } }
.s5-dot-1 { animation: s5Dots 1.2s ease-in-out infinite; }
.s5-dot-2 { animation: s5Dots 1.2s ease-in-out infinite; animation-delay: 0.2s; }
.s5-dot-3 { animation: s5Dots 1.2s ease-in-out infinite; animation-delay: 0.4s; }
@keyframes s5RecPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 8px rgba(239, 68, 68, 0.8); } 50% { opacity: 0.4; box-shadow: 0 0 4px rgba(239, 68, 68, 0.4); } }
.s5-rec-pulse { animation: s5RecPulse 1s ease-in-out infinite; }
@keyframes s5VideoIn { from { opacity: 0; transform: translateX(-50%) scale(0.95); filter: blur(6px); } to { opacity: 1; transform: translateX(-50%) scale(1); filter: blur(0); } }
.s5-video-wrap { animation: s5VideoIn 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.6s both; }
@keyframes s5FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s5SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s5-fade-in { animation: s5FadeIn 0.8s ease-out both; }
.s5-slide-in { animation: s5SlideIn 0.8s ease-out 0.3s both; }
.s5-fade-in-last { animation: s5FadeIn 0.8s ease-out 1.4s both; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-cyan-500/10 rounded-full blur-[140px] s6-breathe-1"></div>
  <div class="absolute bottom-[-10%] right-[-10%] w-[550px] h-[550px] bg-sky-500/10 rounded-full blur-[140px] s6-breathe-2"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-cyan-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-cyan-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent s6-scan-line"></div>
</div>
<div class="absolute top-3 left-10 right-10 flex items-center justify-between z-10 s6-fade-in">
  <div class="flex items-center gap-3">
    <div class="w-2 h-2 bg-cyan-400 rounded-full s6-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #22d3ee; font-family: 'JetBrains Mono', monospace;">Slide 06 · Scenario 02</div>
  </div>
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Dedik Romahadi · BIT</div>
</div>
<div class="absolute top-12 left-10 right-10 z-10 s6-slide-in">
  <div class="flex items-center gap-3 mb-1">
    <div class="h-px w-8 bg-cyan-400 opacity-60"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #22d3ee; opacity: 0.8; font-family: 'JetBrains Mono', monospace;">Scenario Two · Aerial Operation</div>
  </div>
  <div class="flex items-end justify-between">
    <h1 style="font-size: 1.5rem; line-height: 1.1; font-weight: 700; margin: 0; letter-spacing: -0.025em;">
      <span style="color: white;">UAV </span><span class="bg-gradient-to-r from-cyan-300 via-sky-300 to-cyan-300 bg-clip-text text-transparent">Sea-Survivor Search</span>
    </h1>
    <div class="flex items-center gap-4" style="font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase; color: #94a3b8; font-family: 'JetBrains Mono', monospace;">
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-full"></div>Trials · 200</div>
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-full"></div>Targets · Multi</div>
    </div>
  </div>
</div>
<div class="absolute z-10 s6-video-wrap" style="top: 120px; left: 50%; transform: translateX(-50%); width: 700px; height: 394px;">
  <div class="absolute rounded-2xl bg-gradient-to-r from-cyan-500/30 via-sky-500/20 to-cyan-500/30 blur-xl s6-video-glow" style="inset: -4px;"></div>
  <div class="relative rounded-2xl overflow-hidden s6-video-frame" style="width: 100%; height: 100%;">
    <div class="relative" style="width: 100%; height: 100%; background: #0f172a;">
      <video autoplay muted loop playsinline style="position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover;">
        <source src="/scenario2-uav.mp4" type="video/mp4"/>
      </video>
      <div class="absolute top-3 left-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-cyan-400/40">
        <div class="w-1.5 h-1.5 bg-red-500 rounded-full s6-rec-pulse"></div>
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">LIVE · UAV</div>
      </div>
      <div class="absolute top-3 right-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-cyan-400/40">
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: #67e8f9; font-family: 'JetBrains Mono', monospace;">02 / 03</div>
      </div>
      <div class="absolute bottom-3 left-3 right-3 flex items-center justify-between">
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-cyan-400/30">
          <svg class="w-3 h-3 text-cyan-300" viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M2 6 L6 2 L10 6 M6 2 L6 10"/></svg>
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">Altitude · 150m · Search Grid Active</div>
        </div>
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-cyan-400/30">
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">Open Sea</div>
        </div>
      </div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 right-10 flex items-center justify-between z-10 s6-fade-in-last">
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Target Detection · Navigation · Dual-Task Load</div>
  <div class="flex items-center gap-3">
    <div class="w-1.5 h-1.5 bg-green-400 rounded-full s6-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Recording</div>
  </div>
</div>

<style>
@keyframes s6Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s6-breathe-1 { animation: s6Breathe 8s ease-in-out infinite; }
.s6-breathe-2 { animation: s6Breathe 10s ease-in-out infinite; animation-delay: -3s; }
@keyframes s6ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s6-scan-line { animation: s6ScanLine 6s linear infinite; }
@keyframes s6StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.s6-strong-pulse { animation: s6StrongPulse 1.8s ease-in-out infinite; }
.s6-video-frame { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.7), 0 0 40px rgba(103, 232, 249, 0.3), inset 0 0 20px rgba(103, 232, 249, 0.08); animation: s6FrameGlow 4s ease-in-out infinite; }
@keyframes s6FrameGlow { 0%, 100% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.6), 0 0 30px rgba(103, 232, 249, 0.25), inset 0 0 20px rgba(103, 232, 249, 0.08); } 50% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 1), 0 0 55px rgba(103, 232, 249, 0.5), inset 0 0 30px rgba(103, 232, 249, 0.15); } }
@keyframes s6VideoGlow { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
.s6-video-glow { animation: s6VideoGlow 4s ease-in-out infinite; }
@keyframes s6VideoScan { 0% { top: 0%; } 100% { top: 100%; } }
.s6-video-scan { animation: s6VideoScan 3s linear infinite; }
@keyframes s6PlayPulse { 0%, 100% { transform: scale(1); opacity: 0.9; filter: drop-shadow(0 0 10px currentColor); } 50% { transform: scale(1.08); opacity: 1; filter: drop-shadow(0 0 20px currentColor); } }
.s6-play-icon { animation: s6PlayPulse 2s ease-in-out infinite; }
@keyframes s6CirclePulse { 0%, 100% { transform: scale(1); opacity: 0.6; } 50% { transform: scale(1.15); opacity: 0.2; } }
.s6-circle-pulse { animation: s6CirclePulse 2s ease-in-out infinite; transform-origin: center; transform-box: fill-box; }
@keyframes s6Dots { 0%, 80%, 100% { opacity: 0.3; transform: scale(0.8); } 40% { opacity: 1; transform: scale(1.3); } }
.s6-dot-1 { animation: s6Dots 1.2s ease-in-out infinite; }
.s6-dot-2 { animation: s6Dots 1.2s ease-in-out infinite; animation-delay: 0.2s; }
.s6-dot-3 { animation: s6Dots 1.2s ease-in-out infinite; animation-delay: 0.4s; }
@keyframes s6RecPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 8px rgba(239, 68, 68, 0.8); } 50% { opacity: 0.4; box-shadow: 0 0 4px rgba(239, 68, 68, 0.4); } }
.s6-rec-pulse { animation: s6RecPulse 1s ease-in-out infinite; }
@keyframes s6VideoIn { from { opacity: 0; transform: translateX(-50%) scale(0.95); filter: blur(6px); } to { opacity: 1; transform: translateX(-50%) scale(1); filter: blur(0); } }
.s6-video-wrap { animation: s6VideoIn 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.6s both; }
@keyframes s6FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s6SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s6-fade-in { animation: s6FadeIn 0.8s ease-out both; }
.s6-slide-in { animation: s6SlideIn 0.8s ease-out 0.3s both; }
.s6-fade-in-last { animation: s6FadeIn 0.8s ease-out 1.4s both; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-amber-500/10 rounded-full blur-[140px] s7-breathe-1"></div>
  <div class="absolute bottom-[-10%] right-[-10%] w-[550px] h-[550px] bg-orange-500/10 rounded-full blur-[140px] s7-breathe-2"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-amber-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-amber-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-amber-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-amber-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-amber-300 to-transparent s7-scan-line"></div>
</div>
<div class="absolute top-3 left-10 right-10 flex items-center justify-between z-10 s7-fade-in">
  <div class="flex items-center gap-3">
    <div class="w-2 h-2 bg-amber-400 rounded-full s7-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #fbbf24; font-family: 'JetBrains Mono', monospace;">Slide 07 · Scenario 03</div>
  </div>
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Dedik Romahadi · BIT</div>
</div>
<div class="absolute top-12 left-10 right-10 z-10 s7-slide-in">
  <div class="flex items-center gap-3 mb-1">
    <div class="h-px w-8 bg-amber-400 opacity-60"></div>
    <div style="font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: #fbbf24; opacity: 0.8; font-family: 'JetBrains Mono', monospace;">Scenario Three · Ground Operation</div>
  </div>
  <div class="flex items-end justify-between">
    <h1 style="font-size: 1.5rem; line-height: 1.1; font-weight: 700; margin: 0; letter-spacing: -0.025em;">
      <span style="color: white;">UGV </span><span class="bg-gradient-to-r from-amber-300 via-orange-300 to-amber-300 bg-clip-text text-transparent">Fire-Environment Search</span>
    </h1>
    <div class="flex items-center gap-4" style="font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase; color: #94a3b8; font-family: 'JetBrains Mono', monospace;">
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-amber-400 rounded-full"></div>Trials · 200</div>
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-amber-400 rounded-full"></div>Obstacles · High</div>
    </div>
  </div>
</div>
<div class="absolute z-10 s7-video-wrap" style="top: 120px; left: 50%; transform: translateX(-50%); width: 700px; height: 394px;">
  <div class="absolute rounded-2xl bg-gradient-to-r from-amber-500/30 via-orange-500/20 to-amber-500/30 blur-xl s7-video-glow" style="inset: -4px;"></div>
  <div class="relative rounded-2xl overflow-hidden s7-video-frame" style="width: 100%; height: 100%;">
    <div class="relative" style="width: 100%; height: 100%; background: #0f172a;">
      <video autoplay muted loop playsinline style="position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover;">
        <source src="/scenario3-ugv.mp4" type="video/mp4"/>
      </video>
      <div class="absolute top-3 left-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-amber-400/40">
        <div class="w-1.5 h-1.5 bg-red-500 rounded-full s7-rec-pulse"></div>
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">LIVE · UGV</div>
      </div>
      <div class="absolute top-3 right-3 flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-amber-400/40">
        <div style="font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: #fcd34d; font-family: 'JetBrains Mono', monospace;">03 / 03</div>
      </div>
      <div class="absolute bottom-3 left-3 right-3 flex items-center justify-between">
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-amber-400/30">
          <svg class="w-3 h-3 text-amber-300" viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M6 1 L10 4 L10 11 L2 11 L2 4 Z"/><circle cx="6" cy="7" r="1.5" fill="currentColor"/></svg>
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">Thermal · Obstacle Detect · Navigation</div>
        </div>
        <div class="flex items-center gap-2 bg-black/60 backdrop-blur rounded-full px-3 py-1 border border-amber-400/30">
          <div style="font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; color: white; font-family: 'JetBrains Mono', monospace;">Hazard Zone</div>
        </div>
      </div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 right-10 flex items-center justify-between z-10 s7-fade-in-last">
  <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Obstacle Avoidance · Target Detection · High-Stress Environment</div>
  <div class="flex items-center gap-3">
    <div class="w-1.5 h-1.5 bg-green-400 rounded-full s7-strong-pulse"></div>
    <div style="font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: #64748b; font-family: 'JetBrains Mono', monospace;">Recording</div>
  </div>
</div>

<style>
@keyframes s7Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s7-breathe-1 { animation: s7Breathe 8s ease-in-out infinite; }
.s7-breathe-2 { animation: s7Breathe 10s ease-in-out infinite; animation-delay: -3s; }
@keyframes s7ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s7-scan-line { animation: s7ScanLine 6s linear infinite; }
@keyframes s7StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 12px currentColor; } }
.s7-strong-pulse { animation: s7StrongPulse 1.8s ease-in-out infinite; }
.s7-video-frame { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.7), 0 0 40px rgba(251, 191, 36, 0.3), inset 0 0 20px rgba(251, 191, 36, 0.08); animation: s7FrameGlow 4s ease-in-out infinite; }
@keyframes s7FrameGlow { 0%, 100% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.6), 0 0 30px rgba(251, 191, 36, 0.25), inset 0 0 20px rgba(251, 191, 36, 0.08); } 50% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 1), 0 0 55px rgba(251, 191, 36, 0.5), inset 0 0 30px rgba(251, 191, 36, 0.15); } }
@keyframes s7VideoGlow { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
.s7-video-glow { animation: s7VideoGlow 4s ease-in-out infinite; }
@keyframes s7VideoScan { 0% { top: 0%; } 100% { top: 100%; } }
.s7-video-scan { animation: s7VideoScan 3s linear infinite; }
@keyframes s7PlayPulse { 0%, 100% { transform: scale(1); opacity: 0.9; filter: drop-shadow(0 0 10px currentColor); } 50% { transform: scale(1.08); opacity: 1; filter: drop-shadow(0 0 20px currentColor); } }
.s7-play-icon { animation: s7PlayPulse 2s ease-in-out infinite; }
@keyframes s7CirclePulse { 0%, 100% { transform: scale(1); opacity: 0.6; } 50% { transform: scale(1.15); opacity: 0.2; } }
.s7-circle-pulse { animation: s7CirclePulse 2s ease-in-out infinite; transform-origin: center; transform-box: fill-box; }
@keyframes s7Dots { 0%, 80%, 100% { opacity: 0.3; transform: scale(0.8); } 40% { opacity: 1; transform: scale(1.3); } }
.s7-dot-1 { animation: s7Dots 1.2s ease-in-out infinite; }
.s7-dot-2 { animation: s7Dots 1.2s ease-in-out infinite; animation-delay: 0.2s; }
.s7-dot-3 { animation: s7Dots 1.2s ease-in-out infinite; animation-delay: 0.4s; }
@keyframes s7RecPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 8px rgba(239, 68, 68, 0.8); } 50% { opacity: 0.4; box-shadow: 0 0 4px rgba(239, 68, 68, 0.4); } }
.s7-rec-pulse { animation: s7RecPulse 1s ease-in-out infinite; }
@keyframes s7VideoIn { from { opacity: 0; transform: translateX(-50%) scale(0.95); filter: blur(6px); } to { opacity: 1; transform: translateX(-50%) scale(1); filter: blur(0); } }
.s7-video-wrap { animation: s7VideoIn 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.6s both; }
@keyframes s7FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s7SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s7-fade-in { animation: s7FadeIn 0.8s ease-out both; }
.s7-slide-in { animation: s7SlideIn 0.8s ease-out 0.3s both; }
.s7-fade-in-last { animation: s7FadeIn 0.8s ease-out 1.4s both; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[450px] h-[450px] bg-fuchsia-500/8 rounded-full blur-[140px] s8-breathe-1"></div>
  <div class="absolute top-[30%] left-[40%] w-[450px] h-[450px] bg-cyan-500/8 rounded-full blur-[140px] s8-breathe-2"></div>
  <div class="absolute bottom-[-10%] right-[-5%] w-[500px] h-[500px] bg-amber-500/10 rounded-full blur-[140px] s8-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-cyan-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-cyan-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-cyan-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-cyan-300 to-transparent s8-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col pt-0 pb-2 px-10">
  <div class="flex items-center justify-between s8-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-cyan-400 rounded-full s8-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-cyan-400 font-mono">Slide 08 · Experimental Setup</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="s8-slide-in flex items-end justify-between mt-1 mb-3">
    <div>
      <div class="flex items-center gap-2 mb-1.5">
        <div class="h-[2px] w-12 bg-green-400 rounded-full s8-bar-pulse-1"></div>
        <div class="h-[2px] w-20 bg-cyan-400 rounded-full s8-bar-pulse-2"></div>
        <div class="h-[2px] w-8 bg-amber-400 rounded-full s8-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/40 via-cyan-400/20 to-transparent ml-1"></div>
        <div class="w-1 h-1 rounded-full bg-cyan-400 s8-strong-pulse"></div>
      </div>
      <h1 class="!text-[1.7rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Trial-Level </span><span class="bg-gradient-to-r from-green-300 via-cyan-300 to-amber-300 bg-clip-text text-transparent">Vigilance Labels</span>
      </h1>
    </div>
    <div class="flex items-center gap-5 text-[10px] uppercase tracking-[0.2em] text-slate-400 font-mono">
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-green-400 rounded-full s8-strong-pulse"></div>Alert</div>
      <div class="flex items-center gap-2"><div class="w-1.5 h-1.5 bg-amber-500 rounded-full s8-strong-pulse"></div>Unguarded</div>
    </div>
  </div>
  <div class="flex-1 grid grid-cols-3 gap-4 items-stretch">
    <div class="s8-col-1 relative neon-card-fuchsia">
      <div class="neon-card-inner-col">
        <div class="flex items-center justify-center mb-3 pb-3 border-b border-fuchsia-400/20">
          <div class="flex items-center gap-3">
            <svg class="w-9 h-9 s8-icon-pvt-wrap" viewBox="0 0 40 40" fill="none">
              <circle cx="20" cy="20" r="17" stroke="#f0abfc" stroke-width="1.5" opacity="0.4"/>
              <circle cx="20" cy="20" r="13" stroke="#f0abfc" stroke-width="1.5" opacity="0.6"/>
              <circle cx="20" cy="20" r="9" stroke="#f0abfc" stroke-width="1.5" opacity="0.8"/>
              <circle class="s8-pvt-stimulus" cx="20" cy="20" r="5" fill="#e879f9"/>
              <circle class="s8-pvt-ring" cx="20" cy="20" r="3" fill="none" stroke="#f0abfc" stroke-width="1.5"/>
              <line x1="20" y1="2" x2="20" y2="7" stroke="#f0abfc" stroke-width="1.5" stroke-linecap="round" opacity="0.6"/>
              <line x1="20" y1="33" x2="20" y2="38" stroke="#f0abfc" stroke-width="1.5" stroke-linecap="round" opacity="0.6"/>
              <line x1="2" y1="20" x2="7" y2="20" stroke="#f0abfc" stroke-width="1.5" stroke-linecap="round" opacity="0.6"/>
              <line x1="33" y1="20" x2="38" y2="20" stroke="#f0abfc" stroke-width="1.5" stroke-linecap="round" opacity="0.6"/>
            </svg>
            <div class="text-[1.6rem] font-black text-fuchsia-300 tracking-wider">PVT</div>
          </div>
        </div>
        <div class="mb-3">
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-green-500/15 border border-green-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-green-300">ALERT</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-green-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">Only when both conditions met:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">STIMULUS and RESPONSE both exist</div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Reaction Time <span class="font-mono text-green-300">≤ 700 ms</span></div>
            </div>
          </div>
        </div>
        <div>
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-amber-500/15 border border-amber-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-amber-300">UNGUARDED</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-amber-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">If any condition occurs:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Trial contains a <span class="font-mono text-amber-300">FALSE START</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Either STIMULUS or RESPONSE missing</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="s8-col-2 relative neon-card-amber-soft">
      <div class="neon-card-inner-col">
        <div class="flex items-center justify-center mb-3 pb-3 border-b border-amber-400/20">
          <div class="flex items-center gap-3">
            <svg class="w-11 h-9 s8-icon-ugv-wrap" viewBox="0 0 48 40" fill="none">
              <rect class="s8-ugv-track-outer" x="3" y="22" width="42" height="11" rx="5.5" stroke="#fcd34d" stroke-width="1.5" fill="#0a0805"/>
              <circle cx="9" cy="27.5" r="2" fill="#fcd34d" opacity="0.7"/>
              <circle cx="17" cy="27.5" r="2" fill="#fcd34d" opacity="0.7"/>
              <circle cx="24" cy="27.5" r="2" fill="#fcd34d" opacity="0.7"/>
              <circle cx="31" cy="27.5" r="2" fill="#fcd34d" opacity="0.7"/>
              <circle cx="39" cy="27.5" r="2" fill="#fcd34d" opacity="0.7"/>
              <line class="s8-ugv-track-line" x1="3" y1="33" x2="45" y2="33" stroke="#fcd34d" stroke-width="0.8" stroke-dasharray="3 2"/>
              <line class="s8-ugv-track-line" x1="3" y1="22" x2="45" y2="22" stroke="#fcd34d" stroke-width="0.8" stroke-dasharray="3 2"/>
              <rect x="8" y="11" width="32" height="11" rx="1.5" stroke="#fcd34d" stroke-width="1.5" fill="#1a1006"/>
              <rect x="14" y="14" width="20" height="5" rx="0.5" fill="#fcd34d" opacity="0.25"/>
              <rect x="18" y="5" width="12" height="6" rx="1" stroke="#fcd34d" stroke-width="1.5" fill="#1a1006"/>
              <line class="s8-ugv-antenna" x1="36" y1="11" x2="42" y2="3" stroke="#fcd34d" stroke-width="1.3" stroke-linecap="round"/>
              <circle class="s8-ugv-antenna-tip" cx="42" cy="3" r="1.3" fill="#fcd34d"/>
              <line x1="14" y1="5" x2="22" y2="0" stroke="#fcd34d" stroke-width="1.5" stroke-linecap="round"/>
              <circle class="s8-ugv-headlight-l" cx="40" cy="14" r="1.3" fill="#fcd34d"/>
              <circle class="s8-ugv-headlight-r" cx="40" cy="19" r="1.3" fill="#fcd34d"/>
            </svg>
            <div class="text-[1.6rem] font-black text-amber-300 tracking-wider">UGV</div>
          </div>
        </div>
        <div class="mb-3">
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-green-500/15 border border-green-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-green-300">ALERT</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-green-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">Only when ALL conditions satisfied:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">No <span class="font-mono text-green-300">FALSE START</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">No <span class="font-mono text-green-300">COLLISION</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Both Stimulus and Response exist</div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Reaction Time <span class="font-mono text-green-300">≤ 1 s</span></div>
            </div>
          </div>
        </div>
        <div>
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-amber-500/15 border border-amber-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-amber-300">UNGUARDED</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-amber-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">If ANY condition occurs:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Trial contains <span class="font-mono text-amber-300">FALSE START</span> or <span class="font-mono text-amber-300">COLLISION</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Missing Stimulus or Response</div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Reaction Time <span class="font-mono text-amber-300">&gt; 1 s</span></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="s8-col-3 relative neon-card-cyan-soft">
      <div class="neon-card-inner-col">
        <div class="flex items-center justify-center mb-3 pb-3 border-b border-cyan-400/20">
          <div class="flex items-center gap-3">
            <svg class="w-10 h-9 s8-icon-uav-wrap" viewBox="0 0 44 40" fill="none">
              <line x1="13" y1="13" x2="31" y2="27" stroke="#67e8f9" stroke-width="1.8" stroke-linecap="round"/>
              <line x1="31" y1="13" x2="13" y2="27" stroke="#67e8f9" stroke-width="1.8" stroke-linecap="round"/>
              <rect x="17" y="16" width="10" height="8" rx="2" fill="#0a0f1e" stroke="#67e8f9" stroke-width="1.5"/>
              <circle cx="22" cy="20" r="1.5" fill="#67e8f9"/>
              <ellipse class="s8-uav-prop-1" cx="13" cy="13" rx="6" ry="1.2" fill="#67e8f9" opacity="0.5"/>
              <ellipse class="s8-uav-prop-1" cx="13" cy="13" rx="1.2" ry="6" fill="#67e8f9" opacity="0.5"/>
              <circle cx="13" cy="13" r="1.5" fill="#67e8f9"/>
              <ellipse class="s8-uav-prop-2" cx="31" cy="13" rx="6" ry="1.2" fill="#67e8f9" opacity="0.5"/>
              <ellipse class="s8-uav-prop-2" cx="31" cy="13" rx="1.2" ry="6" fill="#67e8f9" opacity="0.5"/>
              <circle cx="31" cy="13" r="1.5" fill="#67e8f9"/>
              <ellipse class="s8-uav-prop-3" cx="13" cy="27" rx="6" ry="1.2" fill="#67e8f9" opacity="0.5"/>
              <ellipse class="s8-uav-prop-3" cx="13" cy="27" rx="1.2" ry="6" fill="#67e8f9" opacity="0.5"/>
              <circle cx="13" cy="27" r="1.5" fill="#67e8f9"/>
              <ellipse class="s8-uav-prop-4" cx="31" cy="27" rx="6" ry="1.2" fill="#67e8f9" opacity="0.5"/>
              <ellipse class="s8-uav-prop-4" cx="31" cy="27" rx="1.2" ry="6" fill="#67e8f9" opacity="0.5"/>
              <circle cx="31" cy="27" r="1.5" fill="#67e8f9"/>
              <ellipse class="s8-uav-shadow" cx="22" cy="36" rx="10" ry="1.5" fill="#67e8f9" opacity="0.15"/>
            </svg>
            <div class="text-[1.6rem] font-black text-cyan-300 tracking-wider">UAV</div>
          </div>
        </div>
        <div class="mb-3">
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-green-500/15 border border-green-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-green-300">ALERT</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-green-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">Only when ALL conditions satisfied:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">No <span class="font-mono text-green-300">FALSE START</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Deviation duration <span class="font-mono text-green-300">≤ 2 s</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Reaction Time <span class="font-mono text-green-300">≤ 1 s</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-green-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Total trial duration <span class="font-mono text-green-300">≤ 20 s</span></div>
            </div>
          </div>
        </div>
        <div>
          <div class="flex items-center gap-2 mb-2">
            <div class="px-2 py-0.5 rounded-md bg-amber-500/15 border border-amber-400/40">
              <div class="text-[10px] uppercase tracking-[0.2em] font-mono font-bold text-amber-300">UNGUARDED</div>
            </div>
            <div class="flex-1 h-px bg-gradient-to-r from-amber-400/30 to-transparent"></div>
          </div>
          <div class="text-[0.7rem] text-slate-400 italic mb-1.5">If ANY condition occurs:</div>
          <div class="space-y-1">
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Trial contains <span class="font-mono text-amber-300">FALSE START</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Deviation phase missing or <span class="font-mono text-amber-300">&gt; 2 s</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Stimulus or Response missing</div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Reaction Time <span class="font-mono text-amber-300">&gt; 1 s</span></div>
            </div>
            <div class="flex items-start gap-2">
              <div class="w-1 h-1 rounded-full bg-amber-400 mt-1.5 flex-shrink-0"></div>
              <div class="text-[0.78rem] text-slate-200 leading-snug">Total trial duration <span class="font-mono text-amber-300">&gt; 20 s</span></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between mt-1 s8-fade-in-last">
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Per-Trial Binary Classification · Cross-Scenario Comparable</div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-green-400 rounded-full s8-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Labels Ready</div>
    </div>
  </div>
</div>

<style>
.neon-card-fuchsia {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.6), 0 0 18px rgba(232, 121, 249, 0.3), inset 0 0 12px rgba(232, 121, 249, 0.06);
  animation: s8GlowFuchsia 3.5s ease-in-out infinite;
}
.neon-card-amber-soft {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.6), 0 0 18px rgba(251, 191, 36, 0.3), inset 0 0 12px rgba(251, 191, 36, 0.06);
  animation: s8GlowAmber 3.5s ease-in-out infinite;
  animation-delay: -1.2s;
}
.neon-card-cyan-soft {
  border-radius: 14px;
  box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.6), 0 0 18px rgba(103, 232, 249, 0.3), inset 0 0 12px rgba(103, 232, 249, 0.06);
  animation: s8GlowCyan 3.5s ease-in-out infinite;
  animation-delay: -2.4s;
}
.neon-card-inner-col {
  background: #0a0f1e;
  border-radius: 12px;
  padding: 14px 14px;
  height: 100%;
  display: flex;
  flex-direction: column;
}
@keyframes s8GlowFuchsia {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.5), 0 0 14px rgba(232, 121, 249, 0.2), inset 0 0 12px rgba(232, 121, 249, 0.05); }
  50% { box-shadow: 0 0 0 1.5px rgba(232, 121, 249, 0.85), 0 0 26px rgba(232, 121, 249, 0.45), inset 0 0 16px rgba(232, 121, 249, 0.12); }
}
@keyframes s8GlowAmber {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.5), 0 0 14px rgba(251, 191, 36, 0.2), inset 0 0 12px rgba(251, 191, 36, 0.05); }
  50% { box-shadow: 0 0 0 1.5px rgba(251, 191, 36, 0.85), 0 0 26px rgba(251, 191, 36, 0.45), inset 0 0 16px rgba(251, 191, 36, 0.12); }
}
@keyframes s8GlowCyan {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.5), 0 0 14px rgba(103, 232, 249, 0.2), inset 0 0 12px rgba(103, 232, 249, 0.05); }
  50% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.85), 0 0 26px rgba(103, 232, 249, 0.45), inset 0 0 16px rgba(103, 232, 249, 0.12); }
}
@keyframes s8Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s8-breathe-1 { animation: s8Breathe 8s ease-in-out infinite; }
.s8-breathe-2 { animation: s8Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s8-breathe-3 { animation: s8Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s8ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s8-scan-line { animation: s8ScanLine 6s linear infinite; }
@keyframes s8StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.6; box-shadow: 0 0 12px currentColor; } }
.s8-strong-pulse { animation: s8StrongPulse 1.8s ease-in-out infinite; }
/* ============ ICON ANIMATIONS ============ */
/* PVT Bullseye - target stimulus berkedip + ring expanding seperti reaction */
.s8-icon-pvt-wrap { filter: drop-shadow(0 0 6px #e879f9); }
@keyframes s8PvtStimulus {
  0%, 60%, 100% { opacity: 1; transform: scale(1); filter: drop-shadow(0 0 8px #e879f9); }
  30% { opacity: 0.3; transform: scale(0.85); filter: drop-shadow(0 0 2px #e879f9); }
  35% { opacity: 1; transform: scale(1.15); filter: drop-shadow(0 0 14px #e879f9); }
}
.s8-pvt-stimulus { animation: s8PvtStimulus 1.5s ease-in-out infinite; transform-origin: 20px 20px; transform-box: fill-box; }
@keyframes s8PvtRing {
  0% { opacity: 1; transform: scale(1); }
  100% { opacity: 0; transform: scale(3); }
}
.s8-pvt-ring { animation: s8PvtRing 1.5s ease-out infinite; transform-origin: 20px 20px; transform-box: fill-box; }

/* UGV - track conveyor moving + antenna swaying + dual headlights */
.s8-icon-ugv-wrap { filter: drop-shadow(0 0 6px #fcd34d); }
@keyframes s8UgvTrackMarch { to { stroke-dashoffset: -10; } }
.s8-ugv-track-line { animation: s8UgvTrackMarch 0.8s linear infinite; }
@keyframes s8UgvAntenna {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(-6deg); }
  75% { transform: rotate(6deg); }
}
.s8-ugv-antenna { animation: s8UgvAntenna 2.5s ease-in-out infinite; transform-origin: 36px 11px; transform-box: fill-box; }
.s8-ugv-antenna-tip { animation: s8UgvAntenna 2.5s ease-in-out infinite; transform-origin: 36px 11px; transform-box: fill-box; }
@keyframes s8UgvHeadlight {
  0%, 100% { opacity: 0.4; transform: scale(1); filter: drop-shadow(0 0 3px #fcd34d); }
  50% { opacity: 1; transform: scale(1.5); filter: drop-shadow(0 0 12px #fcd34d); }
}
.s8-ugv-headlight-l { animation: s8UgvHeadlight 1.2s ease-in-out infinite; transform-origin: 40px 14px; transform-box: fill-box; }
.s8-ugv-headlight-r { animation: s8UgvHeadlight 1.2s ease-in-out infinite; transform-origin: 40px 19px; transform-box: fill-box; animation-delay: -0.6s; }

/* UAV - 4 propellers berputar + body floating + shadow pulsing */
.s8-icon-uav-wrap { animation: s8UavFloat 2.2s ease-in-out infinite; filter: drop-shadow(0 0 6px #67e8f9); }
@keyframes s8UavFloat {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-2px); }
}
@keyframes s8UavPropSpin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
.s8-uav-prop-1 { animation: s8UavPropSpin 0.15s linear infinite; transform-origin: 13px 13px; transform-box: fill-box; }
.s8-uav-prop-2 { animation: s8UavPropSpin 0.15s linear infinite; transform-origin: 31px 13px; transform-box: fill-box; animation-delay: -0.04s; }
.s8-uav-prop-3 { animation: s8UavPropSpin 0.15s linear infinite; transform-origin: 13px 27px; transform-box: fill-box; animation-delay: -0.08s; }
.s8-uav-prop-4 { animation: s8UavPropSpin 0.15s linear infinite; transform-origin: 31px 27px; transform-box: fill-box; animation-delay: -0.02s; }
@keyframes s8UavShadow {
  0%, 100% { opacity: 0.15; transform: scaleX(1); }
  50% { opacity: 0.08; transform: scaleX(0.85); }
}
.s8-uav-shadow { animation: s8UavShadow 2.2s ease-in-out infinite; transform-origin: 22px 36px; transform-box: fill-box; }
@keyframes s8ColIn { from { opacity: 0; transform: translateY(20px) scale(0.96); filter: blur(4px); } to { opacity: 1; transform: translateY(0) scale(1); filter: blur(0); } }
.s8-col-1 { animation: s8ColIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.5s both; }
.s8-col-2 { animation: s8ColIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.7s both; }
.s8-col-3 { animation: s8ColIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.9s both; }
@keyframes s8FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s8SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s8-fade-in { animation: s8FadeIn 0.8s ease-out both; }
.s8-slide-in { animation: s8SlideIn 0.8s ease-out 0.3s both; }
.s8-fade-in-last { animation: s8FadeIn 0.8s ease-out 1.4s both; }
@keyframes sBarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s8-bar-pulse-1 { animation: sBarPulse 2.4s ease-in-out infinite; color: #4ade80; transform-origin: left; }
.s8-bar-pulse-2 { animation: sBarPulse 2.4s ease-in-out infinite; color: #67e8f9; animation-delay: -0.8s; transform-origin: left; }
.s8-bar-pulse-3 { animation: sBarPulse 2.4s ease-in-out infinite; color: #fbbf24; animation-delay: -1.6s; transform-origin: left; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-20%] left-[20%] w-[800px] h-[800px] bg-violet-500/15 rounded-full blur-[160px] s9-breathe"></div>
  <div class="absolute bottom-[-20%] right-[10%] w-[700px] h-[700px] bg-purple-500/12 rounded-full blur-[160px] s9-breathe-2"></div>
</div>
<div class="absolute inset-0 opacity-[0.18] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s9-eeg" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q150,420 300,450 T600,450 Q750,380 900,450 T1200,450 Q1350,500 1500,450 T1800,450 Q1950,400 2100,450 T2400,450 Q2550,500 2700,450 T3000,450 L3200,450" fill="none" stroke="#a78bfa" stroke-width="0.8"/>
  </svg>
</div>
<div class="absolute inset-0 opacity-[0.12] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s9-eeg-2" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,250 Q80,250 130,230 T230,250 Q280,150 330,250 T430,250 Q480,310 530,250 T630,250 Q680,190 730,250 T830,250 Q880,270 930,250 T1030,250 Q1080,220 1130,250 T1230,250 Q1280,150 1330,250 T1430,250 Q1480,310 1530,250 T1630,250 L3200,250" fill="none" stroke="#c4b5fd" stroke-width="1"/>
    <path d="M0,650 Q100,650 160,630 T260,650 Q310,710 360,650 T460,650 Q510,590 560,650 T660,650 Q710,670 760,650 T860,650 L3200,650" fill="none" stroke="#e879f9" stroke-width="1"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[15%] left-[10%] w-1 h-1 bg-violet-400 rounded-full s9-particle-1"></div>
  <div class="absolute top-[25%] left-[85%] w-1.5 h-1.5 bg-purple-300 rounded-full s9-particle-2"></div>
  <div class="absolute top-[75%] left-[12%] w-1 h-1 bg-violet-400 rounded-full s9-particle-3"></div>
  <div class="absolute top-[80%] left-[88%] w-1.5 h-1.5 bg-purple-400 rounded-full s9-particle-1"></div>
  <div class="absolute top-[40%] left-[5%] w-1 h-1 bg-violet-300 rounded-full s9-particle-2"></div>
  <div class="absolute top-[55%] left-[92%] w-1 h-1 bg-purple-300 rounded-full s9-particle-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-60"></div>
<div class="absolute top-6 left-6 w-8 h-8 border-l-2 border-t-2 border-violet-400 opacity-60 s9-bracket-1"></div>
<div class="absolute top-6 right-6 w-8 h-8 border-r-2 border-t-2 border-violet-400 opacity-60 s9-bracket-1"></div>
<div class="absolute bottom-6 left-6 w-8 h-8 border-l-2 border-b-2 border-violet-400 opacity-60 s9-bracket-2"></div>
<div class="absolute bottom-6 right-6 w-8 h-8 border-r-2 border-b-2 border-violet-400 opacity-60 s9-bracket-2"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-15">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s9-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col">
  <div class="flex items-center justify-between px-16 py-4 s9-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s9-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Section Transition</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex-1 flex items-center justify-center px-16">
    <div class="relative w-full max-w-5xl">
      <div class="relative flex items-center justify-center mb-3 s9-number-wrap">
        <div class="absolute w-[180px] h-[180px] rounded-full bg-violet-500/10 blur-3xl s9-aura"></div>
        <div class="absolute w-[120px] h-[120px] rounded-full border border-violet-400/20 s9-ring-1"></div>
        <div class="absolute w-[155px] h-[155px] rounded-full border border-violet-400/15 s9-ring-2"></div>
        <div class="absolute w-[190px] h-[190px] rounded-full border border-violet-400/10 s9-ring-3"></div>
        <div class="relative z-10 flex items-baseline gap-1">
          <span class="text-[5.5rem] font-black leading-none tracking-tighter bg-gradient-to-b from-violet-300 via-purple-400 to-violet-700 bg-clip-text text-transparent s9-number-glow">02</span>
          <span class="text-[1.1rem] font-light text-slate-600 font-mono tracking-wider">/ 04</span>
        </div>
      </div>
      <div class="text-center s9-label-wrap">
        <div class="flex items-center justify-center gap-4 mb-2">
          <div class="h-px w-12 bg-gradient-to-r from-transparent to-violet-400"></div>
          <div class="text-[10px] uppercase tracking-[0.5em] text-violet-400 font-mono">Section Two</div>
          <div class="h-px w-12 bg-gradient-to-l from-transparent to-violet-400"></div>
        </div>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight s9-title">
          <span class="bg-gradient-to-r from-white via-violet-100 to-white bg-clip-text text-transparent">PROPOSED</span>
        </h1>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight mt-1 s9-title-2">
          <span class="bg-gradient-to-r from-violet-300 via-purple-300 to-violet-300 bg-clip-text text-transparent">METHODOLOGY</span>
        </h1>
        <div class="mt-4 max-w-2xl mx-auto s9-subtitle">
          <p class="!text-xs !text-slate-400 !m-0 font-light tracking-wide leading-relaxed">
            Hybrid handcrafted–deep feature fusion · Cross-scenario decoding pipeline · Domain adaptation
          </p>
        </div>
      </div>
      <div class="flex items-center justify-center gap-2 mt-4 s9-dots">
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-8 h-[2px] bg-violet-400 rounded-full"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between px-16 py-4 s9-fade-in-last">
    <div class="flex items-center gap-3">
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Paper 01 · Proposal</div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-violet-400 rounded-full s9-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Entering Section</div>
    </div>
  </div>
</div>

<style>
@keyframes s9Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.1); } }
.s9-breathe { animation: s9Breathe 10s ease-in-out infinite; }
.s9-breathe-2 { animation: s9Breathe 12s ease-in-out infinite; animation-delay: -5s; }
@keyframes s9EegFlow { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.s9-eeg { animation: s9EegFlow 30s linear infinite; }
.s9-eeg-2 { animation: s9EegFlow 22s linear infinite; }
@keyframes s9Particle1 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-12px, -10px); opacity: 1; } }
@keyframes s9Particle2 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(10px, -12px); opacity: 1; } }
@keyframes s9Particle3 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-8px, 12px); opacity: 1; } }
.s9-particle-1 { animation: s9Particle1 5s ease-in-out infinite; }
.s9-particle-2 { animation: s9Particle2 6s ease-in-out infinite; animation-delay: -1.5s; }
.s9-particle-3 { animation: s9Particle3 5.5s ease-in-out infinite; animation-delay: -2.5s; }
@keyframes s9StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 14px currentColor; } }
.s9-strong-pulse { animation: s9StrongPulse 1.8s ease-in-out infinite; }
@keyframes s9ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s9-scan-line { animation: s9ScanLine 5s linear infinite; }
@keyframes s9BracketPulse1 { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.08); } }
.s9-bracket-1 { animation: s9BracketPulse1 4s ease-in-out infinite; transform-origin: top left; }
.s9-bracket-2 { animation: s9BracketPulse1 4s ease-in-out infinite; animation-delay: -2s; transform-origin: bottom right; }
@keyframes s9Aura { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.15); } }
.s9-aura { animation: s9Aura 4s ease-in-out infinite; }
@keyframes s9RingRotate1 { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
@keyframes s9RingRotate2 { from { transform: rotate(0deg); } to { transform: rotate(-360deg); } }
@keyframes s9RingPulse { 0%, 100% { opacity: 0.4; } 50% { opacity: 0.9; } }
.s9-ring-1 { animation: s9RingRotate1 40s linear infinite, s9RingPulse 3s ease-in-out infinite; }
.s9-ring-2 { animation: s9RingRotate2 60s linear infinite, s9RingPulse 3s ease-in-out infinite; animation-delay: -1s; }
.s9-ring-3 { animation: s9RingRotate1 80s linear infinite, s9RingPulse 3s ease-in-out infinite; animation-delay: -2s; }
@keyframes s9NumberGlow {
  0%, 100% { filter: drop-shadow(0 0 20px rgba(167, 139, 250, 0.4)) drop-shadow(0 0 40px rgba(168, 85, 247, 0.2)); }
  50% { filter: drop-shadow(0 0 30px rgba(196, 181, 253, 0.6)) drop-shadow(0 0 60px rgba(167, 139, 250, 0.3)); }
}
.s9-number-glow { animation: s9NumberGlow 3s ease-in-out infinite; }
@keyframes s9NumberIn {
  from { opacity: 0; transform: scale(0.6); filter: blur(20px); }
  to { opacity: 1; transform: scale(1); filter: blur(0); }
}
.s9-number-wrap { animation: s9NumberIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) 0.3s both; }
@keyframes s9FadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
.s9-label-wrap { animation: s9FadeUp 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.0s both; }
@keyframes s9TitleIn {
  from { opacity: 0; transform: translateY(20px); letter-spacing: 0.5em; filter: blur(8px); }
  to { opacity: 1; transform: translateY(0); letter-spacing: -0.025em; filter: blur(0); }
}
.s9-title { animation: s9TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.2s both; }
.s9-title-2 { animation: s9TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.5s both; }
@keyframes s9SubIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
.s9-subtitle { animation: s9SubIn 0.8s ease-out 2.0s both; }
.s9-dots { animation: s9SubIn 0.8s ease-out 2.3s both; }
@keyframes s9FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
.s9-fade-in { animation: s9FadeIn 0.8s ease-out both; }
.s9-fade-in-last { animation: s9FadeIn 0.8s ease-out 2.5s both; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-orange-500/8 rounded-full blur-[140px] s10-breathe-1"></div>
  <div class="absolute top-[35%] right-[-10%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s10-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[20%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s10-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s10-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col pt-2 pb-2 px-10">
  <div class="flex items-center justify-between s10-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s10-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 10 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="s10-slide-in flex items-end justify-between mt-1 mb-3">
    <div class="flex-1">
      <div class="flex items-center gap-2 mb-1.5">
        <div class="h-[2px] w-12 bg-orange-400 rounded-full s10-bar-pulse-1"></div>
        <div class="h-[2px] w-20 bg-cyan-400 rounded-full s10-bar-pulse-2"></div>
        <div class="h-[2px] w-8 bg-amber-400 rounded-full s10-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/40 via-violet-400/20 to-transparent ml-1"></div>
        <div class="w-1 h-1 rounded-full bg-violet-400 s10-strong-pulse"></div>
      </div>
      <h1 class="!text-[1.7rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">EEG </span><span class="bg-gradient-to-r from-orange-300 via-cyan-300 to-amber-300 bg-clip-text text-transparent">Preprocessing Pipeline</span>
      </h1>
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-3 justify-around">
    <div class="s10-stage-1 relative">
      <div class="flex items-center gap-3 mb-1.5">
        <div class="relative w-7 h-7 rounded-full border-2 border-orange-400 flex items-center justify-center s10-stage-num">
          <div class="text-[10px] font-mono font-bold text-orange-300">01</div>
        </div>
        <div class="text-[11px] uppercase tracking-[0.35em] font-mono font-bold text-orange-300">Step &amp; Spike Correction</div>
        <div class="flex-1 h-px bg-gradient-to-r from-orange-400/50 via-orange-400/20 to-transparent"></div>
      </div>
      <div class="relative">
        <div class="flex items-center justify-between gap-1.5 px-2 relative">
          <div class="s10-node-orange flex flex-col items-center justify-center px-2 py-1.5 min-w-[88px] h-[52px]">
            <div class="text-[0.78rem] font-bold text-white leading-tight">Raw EEG</div>
            <div class="text-[0.6rem] text-orange-200/70 font-mono mt-0.5">nCh × nSamples</div>
          </div>
          <svg class="w-5 h-3 text-orange-400 flex-shrink-0" viewBox="0 0 20 8" fill="none">
            <line x1="0" y1="4" x2="14" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-orange"/>
            <path d="M12 1 L18 4 L12 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="s10-node-orange flex flex-col items-center justify-center px-2 py-1.5 min-w-[88px] h-[52px]">
            <div class="text-[0.78rem] font-bold text-white leading-tight">MAD threshold</div>
            <div class="text-[0.6rem] text-orange-200/70 font-mono mt-0.5">20 × MAD</div>
          </div>
          <svg class="w-5 h-3 text-orange-400 flex-shrink-0" viewBox="0 0 20 8" fill="none">
            <line x1="0" y1="4" x2="14" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-orange"/>
            <path d="M12 1 L18 4 L12 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="relative flex-shrink-0" style="width: 80px; height: 60px;">
            <svg class="absolute inset-0 w-full h-full" viewBox="0 0 80 60" fill="none">
              <polygon points="40,4 76,30 40,56 4,30" fill="#0a0f1e" stroke="#fb923c" stroke-width="1.6" class="s10-diamond-orange"/>
            </svg>
            <div class="absolute inset-0 flex flex-col items-center justify-center">
              <div class="text-[0.7rem] font-bold text-white leading-none">Step</div>
              <div class="text-[0.7rem] font-bold text-white leading-none">detected?</div>
            </div>
            <div id="s10-anchor-step" class="absolute" style="top: 50%; left: 50%; width: 0; height: 0;"></div>
            <svg class="absolute" style="top: -22px; left: 40px; width: 274px; height: 28px; overflow: visible; z-index: 20;" viewBox="0 0 286 28" fill="none">
              <path d="M 1 28 L 1 6 L 285 6 L 285 24" stroke="#fb923c" stroke-width="1.3" stroke-dasharray="3 3" fill="none" class="s10-bypass-orange-1"/>
              <path d="M 281 20 L 285 26 L 289 20" stroke="#fb923c" stroke-width="1.3" stroke-linecap="round" fill="none"/>
              <text x="143" y="2" font-family="'JetBrains Mono', monospace" font-size="3.5" fill="#fdba74" text-anchor="middle" font-weight="bold">No</text>
            </svg>
          </div>
          <div class="relative flex-shrink-0">
            <svg class="w-5 h-3 text-orange-400" viewBox="0 0 20 8" fill="none">
              <line x1="0" y1="4" x2="14" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-orange"/>
              <path d="M12 1 L18 4 L12 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
            </svg>
            <div class="absolute -top-3 left-1/2 -translate-x-1/2 text-[0.75rem] font-mono font-bold text-orange-300">Yes</div>
          </div>
          <div class="s10-node-orange flex flex-col items-center justify-center px-2 py-1.5 min-w-[88px] h-[52px]">
            <div class="text-[0.78rem] font-bold text-white leading-tight">Step correction</div>
            <div class="text-[0.6rem] text-orange-200/70 font-mono mt-0.5">Median shift</div>
          </div>
          <svg class="w-5 h-3 text-orange-400 flex-shrink-0" viewBox="0 0 20 8" fill="none">
            <line x1="0" y1="4" x2="14" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-orange"/>
            <path d="M12 1 L18 4 L12 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="relative flex-shrink-0" style="width: 80px; height: 60px;">
            <svg class="absolute inset-0 w-full h-full" viewBox="0 0 80 60" fill="none">
              <polygon points="40,4 76,30 40,56 4,30" fill="#0a0f1e" stroke="#fb923c" stroke-width="1.6" class="s10-diamond-orange"/>
            </svg>
            <div class="absolute inset-0 flex flex-col items-center justify-center">
              <div class="text-[0.7rem] font-bold text-white leading-none">Spike</div>
              <div class="text-[0.7rem] font-bold text-white leading-none">≤ 2%?</div>
            </div>
            <svg class="absolute" style="top: 56px; right: 40px; width: 540px; height: 60px; overflow: visible;" viewBox="0 0 540 60" fill="none">
              <path d="M 540 0 L 540 30 L 1 30 L 1 60" stroke="#fb923c" stroke-width="1.3" stroke-dasharray="3 3" fill="none" class="s10-bypass-orange-2"/>
              <path d="M -3 56 L 1 62 L 5 56" stroke="#fb923c" stroke-width="1.3" stroke-linecap="round" fill="none"/>
              <text x="270" y="26" font-family="'JetBrains Mono', monospace" font-size="3.5" fill="#fdba74" text-anchor="middle" font-weight="bold">No</text>
            </svg>
          </div>
          <div class="relative flex-shrink-0">
            <svg class="w-5 h-3 text-orange-400" viewBox="0 0 20 8" fill="none">
              <line x1="0" y1="4" x2="14" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-orange"/>
              <path d="M12 1 L18 4 L12 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
            </svg>
            <div class="absolute -top-3 left-1/2 -translate-x-1/2 text-[0.75rem] font-mono font-bold text-orange-300">Yes</div>
          </div>
          <div class="relative flex-shrink-0">
            <div class="s10-node-orange flex flex-col items-center justify-center px-2 py-1.5 min-w-[88px] h-[52px]">
              <div class="text-[0.78rem] font-bold text-white leading-tight">Pchip</div>
              <div class="text-[0.6rem] text-orange-200/70 font-mono mt-0.5">Interpolation</div>
            </div>
            <svg class="absolute" style="top: 52px; right: 0; width: 200px; height: 36px; overflow: visible; pointer-events: none; z-index: 10;" viewBox="0 0 200 36" fill="none">
              <path d="M 156 0 L 156 30 L 1 30" stroke="#fb923c" stroke-width="1.3" stroke-dasharray="3 3" fill="none" class="s10-pchip-down"/>
            </svg>
          </div>
        </div>
      </div>
    </div>
    <div class="s10-stage-2 relative">
      <div class="flex items-center gap-3 mb-1.5">
        <div class="relative w-7 h-7 rounded-full border-2 border-cyan-400 flex items-center justify-center s10-stage-num">
          <div class="text-[10px] font-mono font-bold text-cyan-300">02</div>
        </div>
        <div class="text-[11px] uppercase tracking-[0.35em] font-mono font-bold text-cyan-300">Signal Preprocessing</div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/50 via-cyan-400/20 to-transparent"></div>
      </div>
      <div class="flex items-center justify-between gap-2 px-2">
        <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-white leading-tight">Detrend</div>
          <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5">Linear</div>
        </div>
        <svg class="w-6 h-3 text-cyan-400 flex-shrink-0" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
        </svg>
        <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-white leading-tight">Notch filter</div>
          <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5">50 Hz · Q = 35</div>
        </div>
        <svg class="w-6 h-3 text-cyan-400 flex-shrink-0" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
        </svg>
        <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-white leading-tight">CAR</div>
          <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5">Avg reference</div>
        </div>
        <svg class="w-6 h-3 text-cyan-400 flex-shrink-0" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
        </svg>
        <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-white leading-tight">Bandpass</div>
          <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5 text-center">0.5–80 Hz · Butter n=4</div>
        </div>
        <svg class="w-6 h-3 text-cyan-400 flex-shrink-0" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
        </svg>
        <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-white leading-tight">Downsample</div>
          <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5">1000 → 500 Hz</div>
        </div>
        <svg class="w-6 h-3 text-cyan-400 flex-shrink-0" viewBox="0 0 24 8" fill="none">
          <line x1="0" y1="4" x2="18" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="2 2" class="s10-dash-cyan"/>
          <path d="M16 1 L22 4 L16 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
        </svg>
        <div class="relative flex-shrink-0">
          <div class="s10-node-cyan flex flex-col items-center justify-center px-2 py-1.5 min-w-[100px] h-[52px]">
            <div class="text-[0.8rem] font-bold text-white leading-tight">Baseline</div>
            <div class="text-[0.6rem] text-cyan-200/60 font-mono mt-0.5">First 0.5 s</div>
          </div>
          <svg class="absolute" style="top: 52px; right: 50px; width: 425px; height: 60px; overflow: visible; pointer-events: none; z-index: 10;" viewBox="0 0 425 60" fill="none">
            <path d="M 425 0 L 425 30 L 1 30 L 1 60" stroke="#67e8f9" stroke-width="1.3" stroke-dasharray="3 3" fill="none" class="s10-baseline-down"/>
            <path d="M -3 56 L 1 62 L 5 56" stroke="#67e8f9" stroke-width="1.3" stroke-linecap="round" fill="none"/>
          </svg>
        </div>
      </div>
    </div>
    <div class="s10-stage-3 relative">
      <div class="flex items-center gap-3 mb-1.5">
        <div class="relative w-7 h-7 rounded-full border-2 border-amber-400 flex items-center justify-center s10-stage-num">
          <div class="text-[10px] font-mono font-bold text-amber-300">03</div>
        </div>
        <div class="text-[11px] uppercase tracking-[0.35em] font-mono font-bold text-amber-300">Segment Validation</div>
        <div class="flex-1 h-px bg-gradient-to-r from-amber-400/50 via-amber-400/20 to-transparent"></div>
      </div>
      <div class="flex items-center justify-center gap-3 px-2">
        <div class="flex flex-col items-center">
          <svg class="w-9 h-9 text-rose-400 s10-trash-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
            <path d="M3 6 H21" stroke-linecap="round"/>
            <path d="M5 6 V20 Q5 22 7 22 H17 Q19 22 19 20 V6" stroke-linecap="round"/>
            <path d="M9 6 V4 Q9 2 11 2 H13 Q15 2 15 4 V6" stroke-linecap="round"/>
            <line x1="10" y1="11" x2="10" y2="18" stroke-linecap="round"/>
            <line x1="14" y1="11" x2="14" y2="18" stroke-linecap="round"/>
          </svg>
          <div class="text-[0.65rem] uppercase tracking-[0.2em] text-rose-300 font-mono mt-0.5">Discard</div>
        </div>
        <div class="relative flex-shrink-0">
          <svg class="w-12 h-3 text-rose-400" viewBox="0 0 48 8" fill="none">
            <line x1="2" y1="4" x2="44" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="3 2" class="s10-dash-rose"/>
            <path d="M6 1 L2 4 L6 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="absolute -top-3 left-1/2 -translate-x-1/2 text-[0.75rem] font-mono font-bold text-rose-300">No</div>
        </div>
        <div class="relative flex-shrink-0" style="width: 110px; height: 70px;">
          <svg class="absolute inset-0 w-full h-full" viewBox="0 0 110 70" fill="none">
            <polygon points="55,4 106,35 55,66 4,35" fill="#0a0f1e" stroke="#fbbf24" stroke-width="1.8" class="s10-diamond-amber"/>
          </svg>
          <div class="absolute inset-0 flex items-center justify-center">
            <div class="text-[0.65rem] font-bold text-white">Length ≥ 100?</div>
          </div>
        </div>
        <div class="relative flex-shrink-0">
          <svg class="w-12 h-3 text-emerald-400" viewBox="0 0 48 8" fill="none">
            <line x1="0" y1="4" x2="42" y2="4" stroke="currentColor" stroke-width="1.5" stroke-dasharray="3 2" class="s10-dash-emerald"/>
            <path d="M40 1 L46 4 L40 7" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="absolute -top-3 left-1/2 -translate-x-1/2 text-[0.75rem] font-mono font-bold text-emerald-300">Yes</div>
        </div>
        <div class="s10-feature-out relative flex flex-col items-center justify-center px-3 py-1.5 min-w-[150px] h-[52px]">
          <div class="text-[0.8rem] font-bold text-emerald-200 leading-tight uppercase tracking-wider">Feature Extraction</div>
          <div class="text-[0.6rem] text-emerald-200/60 font-mono mt-0.5">Next stage →</div>
        </div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between mt-2 s10-fade-in-last">
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">3 Stages · Artifact-free · Quality-assured</div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s10-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Pipeline Ready</div>
    </div>
  </div>
</div>

<style>
.s10-node-orange {
  border-radius: 8px;
  background: #0a0f1e;
  box-shadow: 0 0 0 1.5px rgba(251, 146, 60, 0.7), 0 0 12px rgba(251, 146, 60, 0.25), inset 0 0 8px rgba(251, 146, 60, 0.05);
  animation: s10NodeGlowOrange 3s ease-in-out infinite;
}
.s10-node-cyan {
  border-radius: 8px;
  background: #0a0f1e;
  box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.7), 0 0 12px rgba(103, 232, 249, 0.25), inset 0 0 8px rgba(103, 232, 249, 0.05);
  animation: s10NodeGlowCyan 3s ease-in-out infinite;
  animation-delay: -1s;
}
.s10-feature-out {
  border-radius: 8px;
  background: #0a0f1e;
  box-shadow: 0 0 0 2px rgba(52, 211, 153, 0.85), 0 0 18px rgba(52, 211, 153, 0.4), inset 0 0 10px rgba(52, 211, 153, 0.1);
  animation: s10NodeGlowEmerald 2.5s ease-in-out infinite;
}
@keyframes s10NodeGlowOrange {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(251, 146, 60, 0.6), 0 0 10px rgba(251, 146, 60, 0.2), inset 0 0 8px rgba(251, 146, 60, 0.05); }
  50% { box-shadow: 0 0 0 1.5px rgba(251, 146, 60, 0.95), 0 0 22px rgba(251, 146, 60, 0.5), inset 0 0 12px rgba(251, 146, 60, 0.12); }
}
@keyframes s10NodeGlowCyan {
  0%, 100% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.6), 0 0 10px rgba(103, 232, 249, 0.2), inset 0 0 8px rgba(103, 232, 249, 0.05); }
  50% { box-shadow: 0 0 0 1.5px rgba(103, 232, 249, 0.95), 0 0 22px rgba(103, 232, 249, 0.5), inset 0 0 12px rgba(103, 232, 249, 0.12); }
}
@keyframes s10NodeGlowEmerald {
  0%, 100% { box-shadow: 0 0 0 2px rgba(52, 211, 153, 0.7), 0 0 14px rgba(52, 211, 153, 0.3), inset 0 0 10px rgba(52, 211, 153, 0.08); }
  50% { box-shadow: 0 0 0 2px rgba(52, 211, 153, 1), 0 0 28px rgba(52, 211, 153, 0.6), inset 0 0 14px rgba(52, 211, 153, 0.18); }
}
@keyframes s10DiamondGlowOrange {
  0%, 100% { filter: drop-shadow(0 0 4px rgba(251, 146, 60, 0.4)); }
  50% { filter: drop-shadow(0 0 12px rgba(251, 146, 60, 0.85)); }
}
.s10-diamond-orange { animation: s10DiamondGlowOrange 3s ease-in-out infinite; }
@keyframes s10DiamondGlowAmber {
  0%, 100% { filter: drop-shadow(0 0 5px rgba(251, 191, 36, 0.4)); }
  50% { filter: drop-shadow(0 0 14px rgba(251, 191, 36, 0.85)); }
}
.s10-diamond-amber { animation: s10DiamondGlowAmber 2.8s ease-in-out infinite; }
@keyframes s10BypassMarch { to { stroke-dashoffset: -12; } }
.s10-bypass-orange-1, .s10-bypass-orange-2 { animation: s10BypassMarch 0.8s linear infinite; }
.s10-pchip-down { animation: s10BypassMarch 0.8s linear infinite; }
.s10-baseline-down { animation: s10BypassMarch 0.8s linear infinite; }
@keyframes s10StageNum {
  0%, 100% { box-shadow: 0 0 0 0 currentColor, 0 0 8px rgba(255,255,255,0.1); }
  50% { box-shadow: 0 0 0 3px rgba(255,255,255,0.05), 0 0 16px currentColor; }
}
.s10-stage-num { animation: s10StageNum 2.5s ease-in-out infinite; }
@keyframes s10Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s10-breathe-1 { animation: s10Breathe 8s ease-in-out infinite; }
.s10-breathe-2 { animation: s10Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s10-breathe-3 { animation: s10Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s10ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s10-scan-line { animation: s10ScanLine 6s linear infinite; }
@keyframes s10StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.6; box-shadow: 0 0 12px currentColor; } }
.s10-strong-pulse { animation: s10StrongPulse 1.8s ease-in-out infinite; }
@keyframes s10DashMarch { to { stroke-dashoffset: -8; } }
.s10-dash-orange { animation: s10DashMarch 0.6s linear infinite; }
.s10-dash-cyan { animation: s10DashMarch 0.6s linear infinite; animation-delay: -0.2s; }
.s10-dash-rose { animation: s10DashMarch 0.6s linear infinite; }
.s10-dash-emerald { animation: s10DashMarch 0.6s linear infinite; animation-delay: -0.3s; }
@keyframes s10TrashShake {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(-6deg); }
  75% { transform: rotate(6deg); }
}
.s10-trash-icon { animation: s10TrashShake 1.5s ease-in-out infinite; transform-origin: center; transform-box: fill-box; filter: drop-shadow(0 0 6px currentColor); }
@keyframes s10StageIn { from { opacity: 0; transform: translateY(15px); filter: blur(4px); } to { opacity: 1; transform: translateY(0); filter: blur(0); } }
.s10-stage-1 { animation: s10StageIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.5s both; }
.s10-stage-2 { animation: s10StageIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.8s both; }
.s10-stage-3 { animation: s10StageIn 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.1s both; }
@keyframes s10FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes s10SlideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }
.s10-fade-in { animation: s10FadeIn 0.8s ease-out both; }
.s10-slide-in { animation: s10SlideIn 0.8s ease-out 0.3s both; }
.s10-fade-in-last { animation: s10FadeIn 0.8s ease-out 1.6s both; }
@keyframes s10BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s10-bar-pulse-1 { animation: s10BarPulse 2.4s ease-in-out infinite; color: #fb923c; transform-origin: left; }
.s10-bar-pulse-2 { animation: s10BarPulse 2.4s ease-in-out infinite; color: #67e8f9; animation-delay: -0.8s; transform-origin: left; }
.s10-bar-pulse-3 { animation: s10BarPulse 2.4s ease-in-out infinite; color: #fbbf24; animation-delay: -1.6s; transform-origin: left; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px]"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px]"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px]"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="relative z-10 h-full flex flex-col pt-2 pb-2 px-6">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 11 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-1 mb-1.5">
    <div>
      <div class="flex items-center gap-2 mb-1.5">
        <div class="h-[2px] w-12 bg-cyan-400 rounded-full s11-bar-pulse-1"></div>
        <div class="h-[2px] w-20 bg-fuchsia-400 rounded-full s11-bar-pulse-2"></div>
        <div class="h-[2px] w-8 bg-emerald-400 rounded-full s11-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/40 via-violet-400/20 to-transparent ml-1"></div>
        <div class="w-1 h-1 rounded-full bg-violet-400 s11-pipeline-dot"></div>
      </div>
      <h1 class="!text-[1.4rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Nonlinear </span><span class="bg-gradient-to-r from-cyan-300 via-fuchsia-300 to-emerald-300 bg-clip-text text-transparent">Feature Extraction</span>
      </h1>
    </div>
    <div class="text-[10px] uppercase tracking-[0.25em] text-slate-400 font-mono">
      1 Segment EEG + Gaze → Feature Vector [1 × 292]
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-1.5 min-h-0">
    <div class="border border-cyan-400/40 rounded-lg p-2 bg-slate-900/30">
      <div class="flex items-center justify-between mb-1.5">
        <div class="text-[9px] uppercase tracking-[0.3em] font-mono font-bold text-cyan-300">▸ Pipeline · Input Signals → 5-Band Filter → Feature Matrix → Feature Vector</div>
        <div class="flex items-center gap-2">
          <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s11-pipeline-dot"></div>
          <div class="text-[9px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold">Live Pipeline</div>
        </div>
      </div>
      <div class="grid grid-cols-12 gap-1.5 items-stretch">
        <div class="col-span-2 flex flex-col">
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/30 flex-1">
            <div class="text-[10px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center mb-1">Input Signals</div>
            <svg viewBox="0 0 140 245" class="w-full" preserveAspectRatio="xMidYMid meet">
              <defs>
                <clipPath id="s11-eeg-clip">
                  <rect x="22" y="0" width="116" height="180"/>
                </clipPath>
                <clipPath id="s11-gaze-clip">
                  <rect x="32" y="190" width="106" height="55"/>
                </clipPath>
              </defs>
              <g clip-path="url(#s11-eeg-clip)">
                <g class="s11-signal-flow">
                  <path d="M22,14 c0.75,-1.5 3,-1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0 s4.5,-1.5 6,0 s4.5,1.5 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,36 c1.0,-2 3,-2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0 s4.5,-2 6,0 s4.5,2 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,58 c1.75,-3.5 3,-3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0 s4.5,-3.5 6,0 s4.5,3.5 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,80 c0.9,-1.8 3,-1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0 s4.5,-1.8 6,0 s4.5,1.8 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,102 c1.25,-2.5 3,-2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0 s4.5,-2.5 6,0 s4.5,2.5 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,124 c0.6,-1.2 3,-1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0 s4.5,-1.2 6,0 s4.5,1.2 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,146 c1.4,-2.8 3,-2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0 s4.5,-2.8 6,0 s4.5,2.8 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                  <path d="M22,168 c1.5,-3 3,-3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0 s4.5,-3 6,0 s4.5,3 6,0" stroke="#67e8f9" stroke-width="1" fill="none"/>
                </g>
              </g>
              <text x="2" y="14" font-size="4.5" font-family="monospace" fill="#67e8f9">Fp1</text>
              <text x="2" y="36" font-size="4.5" font-family="monospace" fill="#67e8f9">Fp2</text>
              <text x="2" y="58" font-size="4.5" font-family="monospace" fill="#67e8f9">F3</text>
              <text x="2" y="80" font-size="4.5" font-family="monospace" fill="#67e8f9">F4</text>
              <text x="2" y="102" font-size="4.5" font-family="monospace" fill="#67e8f9">C3</text>
              <text x="2" y="124" font-size="4.5" font-family="monospace" fill="#67e8f9">C4</text>
              <text x="2" y="146" font-size="4.5" font-family="monospace" fill="#67e8f9">O1</text>
              <text x="2" y="168" font-size="4.5" font-family="monospace" fill="#67e8f9">O2</text>
              <line x1="2" y1="184" x2="138" y2="184" stroke="#f9a8d4" stroke-width="0.6" stroke-dasharray="2 2" opacity="0.6"/>
              <text x="2" y="212" font-size="4.5" font-family="monospace" fill="#f9a8d4">GazeX</text>
              <text x="2" y="240" font-size="4.5" font-family="monospace" fill="#f9a8d4">GazeY</text>
              <g clip-path="url(#s11-gaze-clip)">
                <g class="s11-gaze-flow">
                  <path d="M40,210 L48,210 L48,200 L60,200 L60,213 L72,213 L72,204 L84,204 L84,211 L96,211 L96,201 L108,201 L108,209 L120,209 L120,202 L132,202 L132,212 L144,212 L144,200 L156,200 L156,213 L168,213 L168,204 L180,204 L180,211 L192,211 L192,201 L204,201 L204,209 L216,209 L216,202 L228,202 L228,212 L240,212 L240,200 L252,200" stroke="#f9a8d4" stroke-width="1" fill="none"/>
                  <path d="M40,236 L50,236 L50,228 L62,228 L62,240 L74,240 L74,231 L86,231 L86,238 L98,238 L98,229 L110,229 L110,237 L122,237 L122,230 L134,230 L134,238 L146,238 L146,228 L158,228 L158,240 L170,240 L170,231 L182,231 L182,238 L194,238 L194,229 L206,229 L206,237 L218,237 L218,230 L230,230 L230,238 L242,238 L242,228 L254,228" stroke="#f9a8d4" stroke-width="1" fill="none"/>
                </g>
              </g>
            </svg>
            <div class="text-[8px] text-slate-400 font-mono text-center mt-0.5">← T Samples →</div>
          </div>
        </div>
        <div class="col-span-1 flex flex-col items-center justify-center">
          <div class="border border-orange-400 rounded-md px-1 py-1.5 bg-orange-950/40 text-center s11-pulse-orange">
            <div class="text-[8px] font-bold text-orange-300 leading-tight">BAND</div>
            <div class="text-[8px] font-bold text-orange-300 leading-tight">FILTER</div>
            <div class="text-[8px] text-orange-200/70 mt-0.5">FIR1</div>
            <div class="text-[8px] text-orange-200/70">filtfilt</div>
            <div class="text-[8px] text-orange-200/70">5 Bands</div>
          </div>
          <svg class="w-full h-3 mt-1" viewBox="0 0 50 8" fill="none" preserveAspectRatio="none">
            <line x1="0" y1="4" x2="44" y2="4" stroke="#fb923c" stroke-width="1" stroke-dasharray="2 2" class="s11-arrow-flow-orange"/>
            <path d="M42 1 L48 4 L42 7" stroke="#fb923c" stroke-width="1" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="text-[7.5px] text-orange-300/70 font-mono mt-0.5">EEG Only</div>
        </div>
        <div class="col-span-2 flex flex-col gap-1">
          <div class="border border-purple-400/60 rounded-md p-1.5 bg-purple-950/20">
            <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-purple-300 text-center mb-1">5 Band-Filtered (EEG)</div>
            <div class="space-y-0.5">
              <div class="border border-purple-500/70 rounded px-1 py-0.5 bg-purple-950/60 text-center"><div class="text-[8px] font-mono font-bold text-purple-200">Delta [1–3 Hz]</div></div>
              <div class="border border-violet-500/70 rounded px-1 py-0.5 bg-violet-950/60 text-center"><div class="text-[8px] font-mono font-bold text-violet-200">Theta [4–7 Hz]</div></div>
              <div class="border border-orange-500/70 rounded px-1 py-0.5 bg-orange-950/60 text-center"><div class="text-[8px] font-mono font-bold text-orange-200">Alpha [8–13 Hz]</div></div>
              <div class="border border-yellow-500/70 rounded px-1 py-0.5 bg-yellow-950/60 text-center"><div class="text-[8px] font-mono font-bold text-yellow-200">Beta [14–30 Hz]</div></div>
              <div class="border border-pink-500/70 rounded px-1 py-0.5 bg-pink-950/60 text-center"><div class="text-[8px] font-mono font-bold text-pink-200">Gamma [31–80 Hz]</div></div>
            </div>
          </div>
          <div class="border border-pink-400/60 rounded-md p-1 bg-pink-950/20">
            <div class="text-[8px] uppercase tracking-wider font-mono font-bold text-pink-300 text-center mb-0.5">Gaze · Mean-Center Only</div>
            <div class="space-y-0.5">
              <div class="border border-pink-500/70 rounded px-1 py-0.5 bg-pink-950/60 text-center"><div class="text-[8px] font-mono font-bold text-pink-200">Raw GazeX</div></div>
              <div class="border border-pink-500/70 rounded px-1 py-0.5 bg-pink-950/60 text-center"><div class="text-[8px] font-mono font-bold text-pink-200">Raw GazeY</div></div>
            </div>
          </div>
        </div>
        <div class="col-span-1 flex flex-col items-center justify-center">
          <div class="border border-yellow-400 rounded-md px-1 py-1.5 bg-yellow-950/40 text-center s11-pulse-yellow">
            <div class="text-[7.5px] font-bold text-yellow-300 leading-tight">7 FEATURES</div>
            <div class="text-[8px] text-yellow-200/70 mt-0.5">Per Band</div>
            <div class="text-[8px] text-yellow-200/70">Per Channel</div>
            <div class="text-[8px] text-yellow-200/70">(Scalar)</div>
          </div>
          <svg class="w-full h-3 mt-1" viewBox="0 0 50 8" fill="none" preserveAspectRatio="none">
            <line x1="0" y1="4" x2="44" y2="4" stroke="#facc15" stroke-width="1" stroke-dasharray="2 2" class="s11-arrow-flow-yellow"/>
            <path d="M42 1 L48 4 L42 7" stroke="#facc15" stroke-width="1" stroke-linecap="round" fill="none"/>
          </svg>
          <div class="text-[7.5px] text-pink-300/70 font-mono mt-0.5 text-center">6 Feats<br/>(No RelEn)</div>
        </div>
        <div class="col-span-3 flex flex-col gap-1">
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20">
            <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center mb-1">Feature Matrix (7 × Bands)</div>
            <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 text-[9px] font-mono mb-0.5">
              <div></div>
              <div class="text-center text-purple-300 font-bold">δ</div>
              <div class="text-center text-violet-300 font-bold">θ</div>
              <div class="text-center text-orange-300 font-bold">α</div>
              <div class="text-center text-yellow-300 font-bold">β</div>
              <div class="text-center text-pink-300 font-bold">γ</div>
            </div>
            <div class="space-y-0.5">
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">RelEn</div><div class="h-2 bg-cyan-400/70 rounded-sm s11-cell-d0"></div><div class="h-2 bg-cyan-400/60 rounded-sm s11-cell-d1"></div><div class="h-2 bg-cyan-400/80 rounded-sm s11-cell-d2"></div><div class="h-2 bg-cyan-400/50 rounded-sm s11-cell-d3"></div><div class="h-2 bg-cyan-400/70 rounded-sm s11-cell-d4"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">DE</div><div class="h-2 bg-purple-400/60 rounded-sm s11-cell-d5"></div><div class="h-2 bg-purple-400/80 rounded-sm s11-cell-d6"></div><div class="h-2 bg-purple-400/50 rounded-sm s11-cell-d7"></div><div class="h-2 bg-purple-400/70 rounded-sm s11-cell-d8"></div><div class="h-2 bg-purple-400/60 rounded-sm s11-cell-d9"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">HM</div><div class="h-2 bg-orange-400/60 rounded-sm s11-cell-d10"></div><div class="h-2 bg-orange-400/50 rounded-sm s11-cell-d11"></div><div class="h-2 bg-orange-400/80 rounded-sm s11-cell-d0"></div><div class="h-2 bg-orange-400/60 rounded-sm s11-cell-d1"></div><div class="h-2 bg-orange-400/70 rounded-sm s11-cell-d2"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">N2D</div><div class="h-2 bg-yellow-400/60 rounded-sm s11-cell-d3"></div><div class="h-2 bg-yellow-400/70 rounded-sm s11-cell-d4"></div><div class="h-2 bg-yellow-400/50 rounded-sm s11-cell-d5"></div><div class="h-2 bg-yellow-400/80 rounded-sm s11-cell-d6"></div><div class="h-2 bg-yellow-400/60 rounded-sm s11-cell-d7"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">D1</div><div class="h-2 bg-pink-400/70 rounded-sm s11-cell-d8"></div><div class="h-2 bg-pink-400/60 rounded-sm s11-cell-d9"></div><div class="h-2 bg-pink-400/80 rounded-sm s11-cell-d10"></div><div class="h-2 bg-pink-400/50 rounded-sm s11-cell-d11"></div><div class="h-2 bg-pink-400/70 rounded-sm s11-cell-d0"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">RE</div><div class="h-2 bg-rose-400/60 rounded-sm s11-cell-d1"></div><div class="h-2 bg-rose-400/70 rounded-sm s11-cell-d2"></div><div class="h-2 bg-rose-400/50 rounded-sm s11-cell-d3"></div><div class="h-2 bg-rose-400/80 rounded-sm s11-cell-d4"></div><div class="h-2 bg-rose-400/60 rounded-sm s11-cell-d5"></div></div>
              <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center"><div class="text-[8px] font-mono text-cyan-200 text-right pr-1">LRSSV</div><div class="h-2 bg-fuchsia-400/70 rounded-sm s11-cell-d6"></div><div class="h-2 bg-fuchsia-400/60 rounded-sm s11-cell-d7"></div><div class="h-2 bg-fuchsia-400/80 rounded-sm s11-cell-d8"></div><div class="h-2 bg-fuchsia-400/50 rounded-sm s11-cell-d9"></div><div class="h-2 bg-fuchsia-400/70 rounded-sm s11-cell-d10"></div></div>
            </div>
            <div class="text-[8px] text-slate-400 font-mono text-center mt-1">× 8 Channels (EEG)</div>
          </div>
          <div class="border border-pink-400/60 rounded-md p-1 bg-pink-950/20">
            <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center text-[9px] font-mono">
              <div></div>
              <div class="text-center text-pink-300/80 font-bold">DE</div>
              <div class="text-center text-pink-300/80 font-bold">HM</div>
              <div class="text-center text-pink-300/80 font-bold">N2D</div>
              <div class="text-center text-pink-300/80 font-bold">D1</div>
              <div class="text-center text-pink-300/80 font-bold">RE</div>
              <div class="text-center text-pink-300/80 font-bold">LRSSV</div>
            </div>
            <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center mt-0.5">
              <div class="text-[8px] font-mono text-pink-200 text-right pr-1">GazeX</div>
              <div class="h-1.5 bg-pink-400/70 rounded-sm s11-cell-d11"></div><div class="h-1.5 bg-pink-400/60 rounded-sm s11-cell-d0"></div><div class="h-1.5 bg-pink-400/80 rounded-sm s11-cell-d1"></div><div class="h-1.5 bg-pink-400/50 rounded-sm s11-cell-d2"></div><div class="h-1.5 bg-pink-400/70 rounded-sm s11-cell-d3"></div><div class="h-1.5 bg-pink-400/60 rounded-sm s11-cell-d4"></div>
            </div>
            <div class="grid grid-cols-[40px_1fr_1fr_1fr_1fr_1fr_1fr] gap-0.5 items-center mt-0.5">
              <div class="text-[8px] font-mono text-pink-200 text-right pr-1">GazeY</div>
              <div class="h-1.5 bg-pink-400/60 rounded-sm s11-cell-d5"></div><div class="h-1.5 bg-pink-400/70 rounded-sm s11-cell-d6"></div><div class="h-1.5 bg-pink-400/50 rounded-sm s11-cell-d7"></div><div class="h-1.5 bg-pink-400/80 rounded-sm s11-cell-d8"></div><div class="h-1.5 bg-pink-400/60 rounded-sm s11-cell-d9"></div><div class="h-1.5 bg-pink-400/70 rounded-sm s11-cell-d10"></div>
            </div>
            <div class="text-[8px] text-slate-400 font-mono text-center mt-0.5">6 Features × 2 Gaze Ch (No RelEnergy)</div>
          </div>
        </div>
        <div class="col-span-3">
          <div class="border-2 border-emerald-400/70 rounded-md p-1.5 bg-emerald-950/20 h-full s11-feature-vector-glow">
            <div class="text-[10px] uppercase tracking-wider font-mono font-bold text-emerald-300 text-center mb-1">Feature Vector</div>
            <div class="border border-cyan-400/50 rounded p-1 bg-cyan-950/30 mb-1">
              <div class="text-[8px] font-mono font-bold text-cyan-300">EEG Block</div>
              <div class="text-[8px] font-mono text-cyan-100">7 Feat × 5 Bands × 8 Ch = 280 Scalars</div>
            </div>
            <div class="border border-pink-400/50 rounded p-1 bg-pink-950/30 mb-1">
              <div class="text-[8px] font-mono font-bold text-pink-300">GAZE Block</div>
              <div class="text-[8px] font-mono text-pink-100">6 Feat × 2 Ch = 12 Scalars</div>
            </div>
            <div class="text-center text-emerald-300 font-bold text-xs leading-none my-0.5">+</div>
            <div class="border-2 border-yellow-400/60 rounded p-1 bg-yellow-950/30">
              <div class="text-[8px] font-mono font-bold text-yellow-300">Feature Vector</div>
              <div class="text-[8px] font-mono text-yellow-100">[ 1 × (280 + 12) ] = [ 1 × 292 ]</div>
              <div class="text-[7.5px] font-mono text-yellow-200/60 mt-0.5">+ Feature Names Labels</div>
            </div>
            <div class="text-[8px] font-mono text-slate-400 mt-1 text-center">NaN / Inf → 0</div>
            <div class="text-[8px] font-mono text-slate-400 text-center">General : 1 × (7·5·C<sub>eeg</sub> + 6·C<sub>gaze</sub>)</div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-violet-400/40 rounded-lg p-2 bg-slate-900/30" style="padding-bottom: 20px; margin-bottom: 30px;">
      <div class="text-[9px] uppercase tracking-[0.3em] font-mono font-bold text-violet-300 mb-1">▸ Mathematical Description · 7 Feature Formulas</div>
      <div class="grid grid-cols-7 gap-1">
        <div class="border border-cyan-400/60 rounded-md p-1 bg-cyan-950/20 relative s11-formula-1">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-cyan-500 border border-cyan-300 flex items-center justify-center text-[7px] font-bold text-white">1</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center leading-tight">F1 · EEG Only</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">RelEnergy</div>
          <div class="text-[6.5px] text-cyan-200/70 text-center leading-tight mt-0.5">Band Energy / Total Energy</div>
          <div class="text-center mt-0.5 text-[8px] text-cyan-100 font-serif italic">Σx²<sub>b</sub> / ΣΣx²<sub>b'</sub></div>
        </div>
        <div class="border border-purple-400/60 rounded-md p-1 bg-purple-950/20 relative s11-formula-2">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-purple-500 border border-purple-300 flex items-center justify-center text-[7px] font-bold text-white">2</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-purple-300 text-center leading-tight">Feature 2</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">DE</div>
          <div class="text-[6.5px] text-purple-200/70 text-center leading-tight mt-0.5">Differential Entropy</div>
          <div class="text-center mt-0.5 text-[8px] text-purple-100 font-serif italic">½ log(2πe σ²)</div>
        </div>
        <div class="border border-fuchsia-400/60 rounded-md p-1 bg-fuchsia-950/20 relative s11-formula-3">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-fuchsia-500 border border-fuchsia-300 flex items-center justify-center text-[7px] font-bold text-white">3</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-fuchsia-300 text-center leading-tight">Feature 3</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">HM</div>
          <div class="text-[6.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">Hjorth Mobility</div>
          <div class="text-center mt-0.5 text-[8px] text-fuchsia-100 font-serif italic">√(Var(ẋ)/Var(x))</div>
        </div>
        <div class="border border-orange-400/60 rounded-md p-1 bg-orange-950/20 relative s11-formula-4">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-orange-500 border border-orange-300 flex items-center justify-center text-[7px] font-bold text-white">4</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-orange-300 text-center leading-tight">Feature 4</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">N2D</div>
          <div class="text-[8px] text-orange-200/70 text-center leading-tight mt-0.5">Norm. 2nd Derivative</div>
          <div class="text-center mt-0.5 text-[8px] text-orange-100 font-serif italic">Σ|ẍ|/Σ|x|</div>
        </div>
        <div class="border border-yellow-400/60 rounded-md p-1 bg-yellow-950/20 relative s11-formula-5">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-yellow-500 border border-yellow-300 flex items-center justify-center text-[7px] font-bold text-white">5</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-yellow-300 text-center leading-tight">Feature 5</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">D1 (RMS)</div>
          <div class="text-[8px] text-yellow-200/70 text-center leading-tight mt-0.5">1st Derivative RMS</div>
          <div class="text-center mt-0.5 text-[8px] text-yellow-100 font-serif italic">√(1/T·Σẋ²)</div>
        </div>
        <div class="border border-rose-400/60 rounded-md p-1 bg-rose-950/20 relative s11-formula-6">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-rose-500 border border-rose-300 flex items-center justify-center text-[7px] font-bold text-white">6</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-rose-300 text-center leading-tight">Feature 6</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">RE</div>
          <div class="text-[6.5px] text-rose-200/70 text-center leading-tight mt-0.5">Renyi Entropy</div>
          <div class="text-center mt-0.5 text-[8px] text-rose-100 font-serif italic">1/(1−α) log Σpᵢ<sup>α</sup></div>
        </div>
        <div class="border border-pink-400/60 rounded-md p-1 bg-pink-950/20 relative s11-formula-7">
          <div class="absolute -top-1.5 -left-1.5 w-4 h-4 rounded-full bg-pink-500 border border-pink-300 flex items-center justify-center text-[7px] font-bold text-white">7</div>
          <div class="text-[7px] uppercase tracking-wider font-mono font-bold text-pink-300 text-center leading-tight">Feature 7</div>
          <div class="text-[9px] font-bold text-white text-center mt-0.5">LRSSV</div>
          <div class="text-[6.5px] text-pink-200/70 text-center leading-tight mt-0.5">Log Ratio Sum-of-Sq</div>
          <div class="text-center mt-0.5 text-[8px] text-pink-100 font-serif italic">log(Σx²/Σ(Δx)²)</div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: 4px;">
    <div class="flex items-center gap-2 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>EEG</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-pink-400 rounded-sm"></div>Gaze</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-purple-400 rounded-sm"></div>δ/θ</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>α</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>β</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-sm"></div>γ</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Vector</div>
    </div>
  </div>
</div>

<style>
@keyframes s11SignalFlow {
  0% { transform: translateX(0); }
  100% { transform: translateX(-96px); }
}
.s11-signal-flow {
  animation: s11SignalFlow 6s linear infinite;
}
@keyframes s11GazeFlow {
  0% { transform: translateX(0); }
  100% { transform: translateX(-96px); }
}
.s11-gaze-flow {
  animation: s11GazeFlow 5s linear infinite;
}
@keyframes s11PulseOrange {
  0%, 100% { box-shadow: 0 0 0 0 rgba(251,146,60,0), inset 0 0 6px rgba(251,146,60,0.1); border-color: rgba(251,146,60,0.6); }
  50% { box-shadow: 0 0 12px rgba(251,146,60,0.5), inset 0 0 12px rgba(251,146,60,0.2); border-color: rgba(251,146,60,1); }
}
.s11-pulse-orange { animation: s11PulseOrange 2.4s ease-in-out infinite; }
@keyframes s11PulseYellow {
  0%, 100% { box-shadow: 0 0 0 0 rgba(250,204,21,0), inset 0 0 6px rgba(250,204,21,0.1); border-color: rgba(250,204,21,0.6); }
  50% { box-shadow: 0 0 12px rgba(250,204,21,0.5), inset 0 0 12px rgba(250,204,21,0.2); border-color: rgba(250,204,21,1); }
}
.s11-pulse-yellow { animation: s11PulseYellow 2.4s ease-in-out infinite; animation-delay: -1.2s; }
@keyframes s11ArrowFlow {
  to { stroke-dashoffset: -8; }
}
.s11-arrow-flow-orange { animation: s11ArrowFlow 0.6s linear infinite; }
.s11-arrow-flow-yellow { animation: s11ArrowFlow 0.6s linear infinite; animation-delay: -0.3s; }
@keyframes s11VectorGlow {
  0%, 100% { box-shadow: 0 0 8px rgba(52,211,153,0.2), inset 0 0 8px rgba(52,211,153,0.05); border-color: rgba(52,211,153,0.5); }
  50% { box-shadow: 0 0 22px rgba(52,211,153,0.6), inset 0 0 14px rgba(52,211,153,0.18); border-color: rgba(52,211,153,1); }
}
.s11-feature-vector-glow { animation: s11VectorGlow 2.8s ease-in-out infinite; }
@keyframes s11PipelineDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399; }
  50% { opacity: 0.5; box-shadow: 0 0 12px #34d399; }
}
.s11-pipeline-dot { animation: s11PipelineDot 1.6s ease-in-out infinite; }
@keyframes s11CellFlicker {
  0%, 90%, 100% { filter: brightness(1) saturate(1); transform: scaleY(1); }
  92% { filter: brightness(2.2) saturate(1.5) drop-shadow(0 0 3px currentColor); transform: scaleY(1.4); }
  94% { filter: brightness(1) saturate(1); transform: scaleY(1); }
  96% { filter: brightness(2) saturate(1.5) drop-shadow(0 0 3px currentColor); transform: scaleY(1.3); }
}
[class*="s11-cell-d"] { animation: s11CellFlicker 3s ease-in-out infinite; transform-origin: center; }
.s11-cell-d0 { animation-delay: 0s; }
.s11-cell-d1 { animation-delay: 0.4s; }
.s11-cell-d2 { animation-delay: 1.7s; }
.s11-cell-d3 { animation-delay: 2.3s; }
.s11-cell-d4 { animation-delay: 0.9s; }
.s11-cell-d5 { animation-delay: 2.8s; }
.s11-cell-d6 { animation-delay: 1.2s; }
.s11-cell-d7 { animation-delay: 0.2s; }
.s11-cell-d8 { animation-delay: 2.0s; }
.s11-cell-d9 { animation-delay: 0.7s; }
.s11-cell-d10 { animation-delay: 2.5s; }
.s11-cell-d11 { animation-delay: 1.5s; }
@keyframes s11FormulaActivate {
  0%, 80%, 100% { 
    box-shadow: inset 0 0 0 1px transparent;
    filter: brightness(1) saturate(1);
    border-color: currentColor;
    transform: scale(1);
  }
  88%, 92% { 
    box-shadow: 
      0 0 20px currentColor,
      0 0 35px currentColor,
      inset 0 0 16px rgba(255,255,255,0.25),
      inset 0 0 0 2px currentColor;
    filter: brightness(1.8) saturate(1.6);
    transform: scale(1.03);
  }
}
[class*="s11-formula-"] { animation: s11FormulaActivate 4.9s ease-in-out infinite; }
.s11-formula-1 { animation-delay: 0s; color: #67e8f9; }
.s11-formula-2 { animation-delay: 0.7s; color: #c084fc; }
.s11-formula-3 { animation-delay: 1.4s; color: #e879f9; }
.s11-formula-4 { animation-delay: 2.1s; color: #fb923c; }
.s11-formula-5 { animation-delay: 2.8s; color: #facc15; }
.s11-formula-6 { animation-delay: 3.5s; color: #fb7185; }
.s11-formula-7 { animation-delay: 4.2s; color: #f9a8d4; }
@keyframes sBarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s11-bar-pulse-1 { animation: sBarPulse 2.4s ease-in-out infinite; color: #67e8f9; transform-origin: left; }
.s11-bar-pulse-2 { animation: sBarPulse 2.4s ease-in-out infinite; color: #e879f9; animation-delay: -0.8s; transform-origin: left; }
.s11-bar-pulse-3 { animation: sBarPulse 2.4s ease-in-out infinite; color: #34d399; animation-delay: -1.6s; transform-origin: left; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s12-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s12-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s12-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s12-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col pt-2 px-6" style="padding-bottom: 16px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s12-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 12 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-1 mb-2">
    <div>
      <div class="flex items-center gap-2 mb-1.5">
        <div class="h-[2px] w-12 bg-cyan-400 rounded-full s12-bar-pulse-1"></div>
        <div class="h-[2px] w-20 bg-fuchsia-400 rounded-full s12-bar-pulse-2"></div>
        <div class="h-[2px] w-8 bg-emerald-400 rounded-full s12-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/40 via-violet-400/20 to-transparent ml-1"></div>
        <div class="w-1 h-1 rounded-full bg-violet-400 s12-pulse"></div>
      </div>
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">EEG + Gaze → </span><span class="bg-gradient-to-r from-cyan-300 via-fuchsia-300 to-emerald-300 bg-clip-text text-transparent">Spectrogram Pipeline</span>
      </h1>
    </div>
    <div class="flex items-center gap-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Preprocessing → DL Input · SqueezeNet &amp; ShuffleNet</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s12-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s12-blink-text">Live Pipeline</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-0.5 min-h-0">
    <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden s12-row-1">
      <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0 border-b border-cyan-400/30 flex items-center gap-2">
        <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Row 1 · Segmentation &amp; Windowing</div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-cyan-400/70">[ C × N<sub>w</sub> × M windowed frames ]</div>
      </div>
      <div class="p-1.5 grid grid-cols-[1fr_auto_1fr_auto_1fr_auto_1fr] gap-1.5 items-stretch">
        <div class="s12-step s12-step-cyan s12-step-1 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">1</div>
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 text-center tracking-wider">Step 1</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Clean Segments</div>
          <div class="text-[7.5px] text-cyan-200/70 text-center leading-tight mt-0.5">EEG + Gaze post-preprocessing<br/>C channels × T samples</div>
          <div class="text-center mt-1 text-[9px] text-cyan-100 font-serif italic">x<sup>c</sup>(n), c ∈ 1..C<sub>tot</sub></div>
        </div>
        <div class="s12-arrow s12-arrow-cyan flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-cyan s12-step-2 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">2</div>
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 text-center tracking-wider">Step 2</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Epoch Windowing</div>
          <div class="text-[7.5px] text-cyan-200/70 text-center leading-tight mt-0.5">Sliding window segmentation<br/>stride = N<sub>win</sub>(1 − overlap)</div>
          <div class="text-center mt-1 text-[9px] text-cyan-100 font-serif italic">N<sub>win</sub> = W<sub>s</sub> · f<sub>s</sub></div>
        </div>
        <div class="s12-arrow s12-arrow-cyan flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-cyan s12-step-3 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">3</div>
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 text-center tracking-wider">Step 3</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Framing</div>
          <div class="text-[7.5px] text-cyan-200/70 text-center leading-tight mt-0.5">Split epoch → overlapping frames<br/>m = frame index, H = hop size</div>
          <div class="text-center mt-1 text-[9px] text-cyan-100 font-serif italic">x<sup>c</sup><sub>m</sub>(n) = x<sup>c</sup>(n + mH)</div>
        </div>
        <div class="s12-arrow s12-arrow-cyan flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-cyan s12-step-4 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">4</div>
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 text-center tracking-wider">Step 4</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Hann Window</div>
          <div class="text-[7.5px] text-cyan-200/70 text-center leading-tight mt-0.5">Reduce spectral leakage<br/>y_m = x_m · w(n)</div>
          <div class="text-center mt-1 text-[9px] text-cyan-100 font-serif italic">w(n) = ½(1 − cos 2πn/N<sub>w</sub>−1)</div>
        </div>
      </div>
    </div>
    <div class="flex items-center justify-end pr-3 -my-1">
      <div class="flex items-center gap-2">
        <div class="px-2 py-0.5 rounded bg-orange-500/20 border border-orange-400/60 text-[8px] font-mono font-bold text-orange-300 s12-transition-tag">→ STFT</div>
        <svg viewBox="0 0 12 24" class="w-3 h-6"><path d="M6 0 L6 18" stroke="#fb923c" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M2 16 L6 22 L10 16" stroke="#fb923c" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg>
      </div>
    </div>
    <div class="border border-fuchsia-400/40 rounded-lg bg-slate-900/30 overflow-hidden s12-row-2">
      <div class="bg-gradient-to-r from-fuchsia-500/20 via-fuchsia-500/5 to-transparent px-2 py-0 border-b border-fuchsia-400/30 flex items-center gap-2">
        <div class="text-[10px] font-mono font-bold text-fuchsia-300">▸ Row 2 · STFT Transformation ( FFT → Power Spectrum → Log Scale )</div>
        <div class="flex-1 h-px bg-gradient-to-r from-fuchsia-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-fuchsia-400/70">[ C × F<sub>band</sub> × M log-spectrogram tensor ]</div>
      </div>
      <div class="p-1.5 grid grid-cols-[1fr_auto_1fr_auto_1fr_auto_1fr] gap-1.5 items-stretch">
        <div class="s12-step s12-step-fuchsia s12-step-8 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">8</div>
          <div class="text-[8px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider">Step 8</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Freq Band Select</div>
          <div class="text-[7.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">Filter frequency range<br/>EEG neural bands</div>
          <div class="text-center mt-1 text-[9px] text-fuchsia-100 font-serif italic">f ∈ [0.5, 80] Hz</div>
        </div>
        <div class="s12-arrow s12-arrow-fuchsia flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M24 6 L6 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash-rev"/><path d="M8 2 L2 6 L8 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-fuchsia s12-step-7 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">7</div>
          <div class="text-[8px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider">Step 7</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Log Scaling</div>
          <div class="text-[7.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">Dynamic range compression<br/>to decibel scale (dB)</div>
          <div class="text-center mt-1 text-[9px] text-fuchsia-100 font-serif italic">L<sup>c</sup> = 10 log<sub>10</sub>(P<sup>c</sup> + ε)</div>
        </div>
        <div class="s12-arrow s12-arrow-fuchsia flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M24 6 L6 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash-rev"/><path d="M8 2 L2 6 L8 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-fuchsia s12-step-6 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">6</div>
          <div class="text-[8px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider">Step 6</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Power Spectrum</div>
          <div class="text-[7.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">Squared FFT magnitude<br/>energy per time-freq bin</div>
          <div class="text-center mt-1 text-[9px] text-fuchsia-100 font-serif italic">P<sup>c</sup>(m,k) = |S<sup>c</sup>(m,k)|²</div>
        </div>
        <div class="s12-arrow s12-arrow-fuchsia flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M24 6 L6 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash-rev"/><path d="M8 2 L2 6 L8 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-fuchsia s12-step-5 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">5</div>
          <div class="text-[8px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider">Step 5</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">FFT Per Frame</div>
          <div class="text-[7.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">DFT per windowed frame<br/>time → frequency domain</div>
          <div class="text-center mt-1 text-[9px] text-fuchsia-100 font-serif italic">S<sup>c</sup><sub>m,k</sub> = Σ y<sup>c</sup><sub>m</sub> e<sup>−j2πkn/N</sup></div>
        </div>
      </div>
    </div>
    <div class="flex items-center justify-start pl-3 -my-1">
      <div class="flex items-center gap-2">
        <svg viewBox="0 0 12 24" class="w-3 h-6"><path d="M6 0 L6 18" stroke="#fb923c" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M2 16 L6 22 L10 16" stroke="#fb923c" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg>
        <div class="px-2 py-0.5 rounded bg-orange-500/20 border border-orange-400/60 text-[8px] font-mono font-bold text-orange-300 s12-transition-tag">C×F×M →</div>
      </div>
    </div>
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden s12-row-3">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0 border-b border-emerald-400/30 flex items-center gap-2">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Row 3 · Normalization &amp; Deep Learning Input</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">CNN Forward → Feature Vector f ∈ ℝ<sup>d</sup></div>
      </div>
      <div class="p-1.5 grid grid-cols-[1fr_auto_1fr_auto_1fr_auto_1fr] gap-1.5 items-stretch">
        <div class="s12-step s12-step-emerald s12-step-9 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">9</div>
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider">Step 9</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Channel Stacking</div>
          <div class="text-[7.5px] text-emerald-200/70 text-center leading-tight mt-0.5">Stack spectrograms all channels<br/>EEG + Gaze → 2D Image</div>
          <div class="text-center mt-1 text-[9px] text-emerald-100 font-serif italic"><strong>X</strong> ∈ ℝ<sup>C×F×M</sup></div>
        </div>
        <div class="s12-arrow s12-arrow-emerald flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-emerald s12-step-10 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">10</div>
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider">Step 10</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Normalization</div>
          <div class="text-[7.5px] text-emerald-200/70 text-center leading-tight mt-0.5">Z-score per segment<br/>stabilize DL input distribution</div>
          <div class="text-center mt-1 text-[9px] text-emerald-100 font-serif italic">X̂ = (X − μ<sub>X</sub>) / σ<sub>X</sub></div>
        </div>
        <div class="s12-arrow s12-arrow-emerald flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-emerald s12-step-11 relative rounded-md py-2 px-1.5">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">11</div>
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider">Step 11</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Resize + Colormap</div>
          <div class="text-[7.5px] text-emerald-200/70 text-center leading-tight mt-0.5">Convert → RGB 224×224<br/>Jet colormap</div>
          <div class="text-center mt-1 text-[9px] text-emerald-100 font-serif italic"><strong>I</strong> ∈ ℝ<sup>224×224×3</sup></div>
        </div>
        <div class="s12-arrow s12-arrow-emerald flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s12-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="s12-step s12-step-emerald s12-step-12 relative rounded-md p-1.5 s12-final-pop">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s12-badge">12</div>
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider">Step 12</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">DL Feature Extract</div>
          <div class="text-[7.5px] text-emerald-200/70 text-center leading-tight mt-0.5">CNN forward pass<br/>SqueezeNet + ShuffleNet</div>
          <div class="text-center mt-1 text-[9px] text-emerald-100 font-serif italic"><strong>f</strong> = CNN(X̂) ∈ ℝ<sup>d</sup></div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: 4px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Row 1: Segmentation &amp; Windowing</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-sm"></div>Row 2: STFT Transformation</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Row 3: Normalization &amp; DL Input</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-yellow-400"></div>Flow</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-orange-400"></div>Transition</div>
    </div>
  </div>
</div>

<style>
.s12-step {
  background: rgba(10, 15, 30, 0.7);
  border: 1.5px solid;
  position: relative;
  transition: all 0.3s ease;
}
.s12-step-cyan { border-color: rgba(103, 232, 249, 0.55); box-shadow: 0 0 8px rgba(103, 232, 249, 0.15), inset 0 0 6px rgba(103, 232, 249, 0.05); }
.s12-step-fuchsia { border-color: rgba(232, 121, 249, 0.55); box-shadow: 0 0 8px rgba(232, 121, 249, 0.15), inset 0 0 6px rgba(232, 121, 249, 0.05); }
.s12-step-emerald { border-color: rgba(52, 211, 153, 0.55); box-shadow: 0 0 8px rgba(52, 211, 153, 0.15), inset 0 0 6px rgba(52, 211, 153, 0.05); }
@keyframes s12StepActivate {
  0%, 80%, 100% { 
    transform: scale(1);
    filter: brightness(1) saturate(1);
  }
  88%, 92% { 
    transform: scale(1.03);
    filter: brightness(1.6) saturate(1.5);
  }
}
@keyframes s12StepActivateCyan {
  0%, 80%, 100% { box-shadow: 0 0 8px rgba(103, 232, 249, 0.15), inset 0 0 6px rgba(103, 232, 249, 0.05); border-color: rgba(103, 232, 249, 0.55); }
  88%, 92% { box-shadow: 0 0 22px #67e8f9, 0 0 36px rgba(103, 232, 249, 0.6), inset 0 0 14px rgba(103, 232, 249, 0.25); border-color: #67e8f9; }
}
@keyframes s12StepActivateFuchsia {
  0%, 80%, 100% { box-shadow: 0 0 8px rgba(232, 121, 249, 0.15), inset 0 0 6px rgba(232, 121, 249, 0.05); border-color: rgba(232, 121, 249, 0.55); }
  88%, 92% { box-shadow: 0 0 22px #e879f9, 0 0 36px rgba(232, 121, 249, 0.6), inset 0 0 14px rgba(232, 121, 249, 0.25); border-color: #e879f9; }
}
@keyframes s12StepActivateEmerald {
  0%, 80%, 100% { box-shadow: 0 0 8px rgba(52, 211, 153, 0.15), inset 0 0 6px rgba(52, 211, 153, 0.05); border-color: rgba(52, 211, 153, 0.55); }
  88%, 92% { box-shadow: 0 0 22px #34d399, 0 0 36px rgba(52, 211, 153, 0.6), inset 0 0 14px rgba(52, 211, 153, 0.25); border-color: #34d399; }
}
.s12-step-cyan { animation: s12StepActivateCyan 8.4s ease-in-out infinite, s12StepActivate 8.4s ease-in-out infinite; }
.s12-step-fuchsia { animation: s12StepActivateFuchsia 8.4s ease-in-out infinite, s12StepActivate 8.4s ease-in-out infinite; }
.s12-step-emerald { animation: s12StepActivateEmerald 8.4s ease-in-out infinite, s12StepActivate 8.4s ease-in-out infinite; }
.s12-step-1 { animation-delay: 0s, 0s; }
.s12-step-2 { animation-delay: 0.7s, 0.7s; }
.s12-step-3 { animation-delay: 1.4s, 1.4s; }
.s12-step-4 { animation-delay: 2.1s, 2.1s; }
.s12-step-5 { animation-delay: 2.8s, 2.8s; }
.s12-step-6 { animation-delay: 3.5s, 3.5s; }
.s12-step-7 { animation-delay: 4.2s, 4.2s; }
.s12-step-8 { animation-delay: 4.9s, 4.9s; }
.s12-step-9 { animation-delay: 5.6s, 5.6s; }
.s12-step-10 { animation-delay: 6.3s, 6.3s; }
.s12-step-11 { animation-delay: 7.0s, 7.0s; }
.s12-step-12 { animation-delay: 7.7s, 7.7s; }
@keyframes s12BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s12-badge { animation: s12BadgePulse 2s ease-in-out infinite; }
@keyframes s12DashMarch { to { stroke-dashoffset: -10; } }
.s12-dash { animation: s12DashMarch 0.6s linear infinite; }
.s12-dash-rev { animation: s12DashMarch 0.6s linear infinite reverse; }
@keyframes s12TransitionGlow {
  0%, 100% { box-shadow: 0 0 4px rgba(251,146,60,0.3); transform: scale(1); }
  50% { box-shadow: 0 0 14px rgba(251,146,60,0.8); transform: scale(1.05); }
}
.s12-transition-tag { animation: s12TransitionGlow 1.8s ease-in-out infinite; }
@keyframes s12RowGlow {
  0%, 100% { box-shadow: inset 0 0 0 transparent; }
  50% { box-shadow: inset 0 0 30px rgba(255,255,255,0.03); }
}
.s12-row-1 { animation: s12RowGlow 4s ease-in-out infinite; }
.s12-row-2 { animation: s12RowGlow 4s ease-in-out infinite; animation-delay: -1.3s; }
.s12-row-3 { animation: s12RowGlow 4s ease-in-out infinite; animation-delay: -2.6s; }
@keyframes s12FinalPop {
  0%, 100% { box-shadow: 0 0 12px rgba(52,211,153,0.3); }
  50% { box-shadow: 0 0 24px rgba(52,211,153,0.7), 0 0 40px rgba(52,211,153,0.4); }
}
.s12-final-pop { animation: s12FinalPop 2.5s ease-in-out infinite, s12StepActivate 8.4s ease-in-out infinite, s12StepActivateEmerald 8.4s ease-in-out infinite; }
@keyframes s12Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s12-pulse { animation: s12Pulse 1.6s ease-in-out infinite; }
@keyframes s12PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s12-pulse-strong { animation: s12PulseStrong 0.9s ease-in-out infinite; }
@keyframes s12BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s12-blink-text { animation: s12BlinkText 0.9s steps(2, end) infinite; }
@keyframes s12Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
.s12-breathe-1 { animation: s12Breathe 8s ease-in-out infinite; }
.s12-breathe-2 { animation: s12Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s12-breathe-3 { animation: s12Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s12ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s12-scan-line { animation: s12ScanLine 6s linear infinite; }
@keyframes sBarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s12-bar-pulse-1 { animation: sBarPulse 2.4s ease-in-out infinite; color: #67e8f9; transform-origin: left; }
.s12-bar-pulse-2 { animation: sBarPulse 2.4s ease-in-out infinite; color: #e879f9; animation-delay: -0.8s; transform-origin: left; }
.s12-bar-pulse-3 { animation: sBarPulse 2.4s ease-in-out infinite; color: #34d399; animation-delay: -1.6s; transform-origin: left; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s13-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s13-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s13-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s13-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s13-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 13 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Spectrogram </span><span class="bg-gradient-to-r from-cyan-300 via-fuchsia-300 to-emerald-300 bg-clip-text text-transparent">Formation</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-cyan-400 rounded-full s13-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-fuchsia-400 rounded-full s13-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-emerald-400 rounded-full s13-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-violet-400 rounded-full s13-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">STFT → Power → dB → V-Stack → Norm [0,1]</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s13-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s13-blink-text">Live Pipeline</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-0.5 min-h-0">
    <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Visual · Input Signals → Per-Channel STFT → Stacked Spectrogram Image</div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-cyan-400/70">[ C × N<sub>win</sub> samples ] → [ C × n<sub>fp</sub> × n<sub>time</sub> ] → [ (n<sub>fp</sub>·C) × n<sub>time</sub> ]</div>
      </div>
      <div class="p-2 grid grid-cols-[3fr_auto_3fr_auto_3fr] gap-2 items-stretch flex-1 min-h-0">
        <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/30 flex flex-col min-h-0 overflow-hidden">
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center mb-1 flex-shrink-0">Input Signals</div>
          <svg viewBox="0 0 220 180" class="w-full flex-1 min-h-0" preserveAspectRatio="none">
            <defs>
              <clipPath id="s13-eeg-clip"><rect x="28" y="0" width="186" height="130"/></clipPath>
              <clipPath id="s13-gaze-clip"><rect x="28" y="142" width="186" height="38"/></clipPath>
            </defs>
            <g clip-path="url(#s13-eeg-clip)">
              <g class="s13-signal-flow"><path d="M28,10.0 L29,9.2 L30,8.7 L31,8.5 L32,8.7 L33,9.2 L34,10.0 L35,10.8 L36,11.3 L37,11.5 L38,11.3 L39,10.8 L40,10.0 L41,9.2 L42,8.7 L43,8.5 L44,8.7 L45,9.2 L46,10.0 L47,10.7 L48,11.3 L49,11.5 L50,11.3 L51,10.8 L52,10.0 L53,9.2 L54,8.7 L55,8.5 L56,8.7 L57,9.2 L58,10.0 L59,10.7 L60,11.3 L61,11.5 L62,11.3 L63,10.8 L64,10.0 L65,9.3 L66,8.7 L67,8.5 L68,8.7 L69,9.2 L70,10.0 L71,10.7 L72,11.3 L73,11.5 L74,11.3 L75,10.8 L76,10.0 L77,9.3 L78,8.7 L79,8.5 L80,8.7 L81,9.2 L82,10.0 L83,10.8 L84,11.3 L85,11.5 L86,11.3 L87,10.8 L88,10.0 L89,9.3 L90,8.7 L91,8.5 L92,8.7 L93,9.2 L94,10.0 L95,10.7 L96,11.3 L97,11.5 L98,11.3 L99,10.7 L100,10.0 L101,9.3 L102,8.7 L103,8.5 L104,8.7 L105,9.2 L106,10.0 L107,10.7 L108,11.3 L109,11.5 L110,11.3 L111,10.7 L112,10.0 L113,9.2 L114,8.7 L115,8.5 L116,8.7 L117,9.2 L118,10.0 L119,10.7 L120,11.3 L121,11.5 L122,11.3 L123,10.7 L124,10.0 L125,9.3 L126,8.7 L127,8.5 L128,8.7 L129,9.2 L130,10.0 L131,10.7 L132,11.3 L133,11.5 L134,11.3 L135,10.8 L136,10.0 L137,9.3 L138,8.7 L139,8.5 L140,8.7 L141,9.2 L142,10.0 L143,10.8 L144,11.3 L145,11.5 L146,11.3 L147,10.8 L148,10.0 L149,9.2 L150,8.7 L151,8.5 L152,8.7 L153,9.2 L154,10.0 L155,10.8 L156,11.3 L157,11.5 L158,11.3 L159,10.7 L160,10.0 L161,9.3 L162,8.7 L163,8.5 L164,8.7 L165,9.3 L166,10.0 L167,10.7 L168,11.3 L169,11.5 L170,11.3 L171,10.8 L172,10.0 L173,9.2 L174,8.7 L175,8.5 L176,8.7 L177,9.2 L178,10.0 L179,10.7 L180,11.3 L181,11.5 L182,11.3 L183,10.7 L184,10.0 L185,9.3 L186,8.7 L187,8.5 L188,8.7 L189,9.2 L190,10.0 L191,10.7 L192,11.3 L193,11.5 L194,11.3 L195,10.7 L196,10.0 L197,9.2 L198,8.7 L199,8.5 L200,8.7 L201,9.2 L202,10.0 L203,10.7 L204,11.3 L205,11.5 L206,11.3 L207,10.8 L208,10.0 L209,9.3 L210,8.7 L211,8.5 L212,8.7 L213,9.2 L214,10.0 L215,10.8 L216,11.3 L217,11.5 L218,11.3 L219,10.8 L220,10.0 L221,9.3 L222,8.7 L223,8.5 L224,8.7 L225,9.2 L226,10.0 L227,10.8 L228,11.3 L229,11.5 L230,11.3 L231,10.8 L232,10.0 L233,9.3 L234,8.7 L235,8.5 L236,8.7 L237,9.3 L238,10.0 L239,10.7 L240,11.3 L241,11.5 L242,11.3 L243,10.8 L244,10.0 L245,9.3 L246,8.7 L247,8.5 L248,8.7 L249,9.2 L250,10.0 L251,10.8 L252,11.3 L253,11.5 L254,11.3 L255,10.8 L256,10.0 L257,9.3 L258,8.7 L259,8.5 L260,8.7 L261,9.3 L262,10.0 L263,10.7 L264,11.3 L265,11.5 L266,11.3 L267,10.8 L268,10.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,26.0 L29,25.0 L30,24.3 L31,24.0 L32,24.3 L33,25.0 L34,26.0 L35,27.0 L36,27.7 L37,28.0 L38,27.7 L39,27.0 L40,26.0 L41,25.0 L42,24.3 L43,24.0 L44,24.3 L45,25.0 L46,26.0 L47,27.0 L48,27.7 L49,28.0 L50,27.7 L51,27.0 L52,26.0 L53,25.0 L54,24.3 L55,24.0 L56,24.3 L57,25.0 L58,26.0 L59,27.0 L60,27.7 L61,28.0 L62,27.7 L63,27.0 L64,26.0 L65,25.0 L66,24.3 L67,24.0 L68,24.3 L69,25.0 L70,26.0 L71,27.0 L72,27.7 L73,28.0 L74,27.7 L75,27.0 L76,26.0 L77,25.0 L78,24.3 L79,24.0 L80,24.3 L81,25.0 L82,26.0 L83,27.0 L84,27.7 L85,28.0 L86,27.7 L87,27.0 L88,26.0 L89,25.0 L90,24.3 L91,24.0 L92,24.3 L93,25.0 L94,26.0 L95,27.0 L96,27.7 L97,28.0 L98,27.7 L99,27.0 L100,26.0 L101,25.0 L102,24.3 L103,24.0 L104,24.3 L105,25.0 L106,26.0 L107,27.0 L108,27.7 L109,28.0 L110,27.7 L111,27.0 L112,26.0 L113,25.0 L114,24.3 L115,24.0 L116,24.3 L117,25.0 L118,26.0 L119,27.0 L120,27.7 L121,28.0 L122,27.7 L123,27.0 L124,26.0 L125,25.0 L126,24.3 L127,24.0 L128,24.3 L129,25.0 L130,26.0 L131,27.0 L132,27.7 L133,28.0 L134,27.7 L135,27.0 L136,26.0 L137,25.0 L138,24.3 L139,24.0 L140,24.3 L141,25.0 L142,26.0 L143,27.0 L144,27.7 L145,28.0 L146,27.7 L147,27.0 L148,26.0 L149,25.0 L150,24.3 L151,24.0 L152,24.3 L153,25.0 L154,26.0 L155,27.0 L156,27.7 L157,28.0 L158,27.7 L159,27.0 L160,26.0 L161,25.0 L162,24.3 L163,24.0 L164,24.3 L165,25.0 L166,26.0 L167,27.0 L168,27.7 L169,28.0 L170,27.7 L171,27.0 L172,26.0 L173,25.0 L174,24.3 L175,24.0 L176,24.3 L177,25.0 L178,26.0 L179,27.0 L180,27.7 L181,28.0 L182,27.7 L183,27.0 L184,26.0 L185,25.0 L186,24.3 L187,24.0 L188,24.3 L189,25.0 L190,26.0 L191,27.0 L192,27.7 L193,28.0 L194,27.7 L195,27.0 L196,26.0 L197,25.0 L198,24.3 L199,24.0 L200,24.3 L201,25.0 L202,26.0 L203,27.0 L204,27.7 L205,28.0 L206,27.7 L207,27.0 L208,26.0 L209,25.0 L210,24.3 L211,24.0 L212,24.3 L213,25.0 L214,26.0 L215,27.0 L216,27.7 L217,28.0 L218,27.7 L219,27.0 L220,26.0 L221,25.0 L222,24.3 L223,24.0 L224,24.3 L225,25.0 L226,26.0 L227,27.0 L228,27.7 L229,28.0 L230,27.7 L231,27.0 L232,26.0 L233,25.0 L234,24.3 L235,24.0 L236,24.3 L237,25.0 L238,26.0 L239,27.0 L240,27.7 L241,28.0 L242,27.7 L243,27.0 L244,26.0 L245,25.0 L246,24.3 L247,24.0 L248,24.3 L249,25.0 L250,26.0 L251,27.0 L252,27.7 L253,28.0 L254,27.7 L255,27.0 L256,26.0 L257,25.0 L258,24.3 L259,24.0 L260,24.3 L261,25.0 L262,26.0 L263,27.0 L264,27.7 L265,28.0 L266,27.7 L267,27.0 L268,26.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,42.0 L29,40.2 L30,39.0 L31,38.5 L32,39.0 L33,40.2 L34,42.0 L35,43.8 L36,45.0 L37,45.5 L38,45.0 L39,43.8 L40,42.0 L41,40.2 L42,39.0 L43,38.5 L44,39.0 L45,40.2 L46,42.0 L47,43.8 L48,45.0 L49,45.5 L50,45.0 L51,43.8 L52,42.0 L53,40.2 L54,39.0 L55,38.5 L56,39.0 L57,40.2 L58,42.0 L59,43.7 L60,45.0 L61,45.5 L62,45.0 L63,43.8 L64,42.0 L65,40.3 L66,39.0 L67,38.5 L68,39.0 L69,40.2 L70,42.0 L71,43.7 L72,45.0 L73,45.5 L74,45.0 L75,43.8 L76,42.0 L77,40.3 L78,39.0 L79,38.5 L80,39.0 L81,40.2 L82,42.0 L83,43.8 L84,45.0 L85,45.5 L86,45.0 L87,43.8 L88,42.0 L89,40.3 L90,39.0 L91,38.5 L92,39.0 L93,40.2 L94,42.0 L95,43.7 L96,45.0 L97,45.5 L98,45.0 L99,43.7 L100,42.0 L101,40.3 L102,39.0 L103,38.5 L104,39.0 L105,40.2 L106,42.0 L107,43.7 L108,45.0 L109,45.5 L110,45.0 L111,43.7 L112,42.0 L113,40.2 L114,39.0 L115,38.5 L116,39.0 L117,40.2 L118,42.0 L119,43.7 L120,45.0 L121,45.5 L122,45.0 L123,43.7 L124,42.0 L125,40.3 L126,39.0 L127,38.5 L128,39.0 L129,40.2 L130,42.0 L131,43.7 L132,45.0 L133,45.5 L134,45.0 L135,43.8 L136,42.0 L137,40.3 L138,39.0 L139,38.5 L140,39.0 L141,40.2 L142,42.0 L143,43.8 L144,45.0 L145,45.5 L146,45.0 L147,43.8 L148,42.0 L149,40.2 L150,39.0 L151,38.5 L152,39.0 L153,40.2 L154,42.0 L155,43.8 L156,45.0 L157,45.5 L158,45.0 L159,43.7 L160,42.0 L161,40.3 L162,39.0 L163,38.5 L164,39.0 L165,40.3 L166,42.0 L167,43.7 L168,45.0 L169,45.5 L170,45.0 L171,43.8 L172,42.0 L173,40.2 L174,39.0 L175,38.5 L176,39.0 L177,40.2 L178,42.0 L179,43.7 L180,45.0 L181,45.5 L182,45.0 L183,43.8 L184,42.0 L185,40.3 L186,39.0 L187,38.5 L188,39.0 L189,40.2 L190,42.0 L191,43.7 L192,45.0 L193,45.5 L194,45.0 L195,43.7 L196,42.0 L197,40.2 L198,39.0 L199,38.5 L200,39.0 L201,40.2 L202,42.0 L203,43.7 L204,45.0 L205,45.5 L206,45.0 L207,43.8 L208,42.0 L209,40.3 L210,39.0 L211,38.5 L212,39.0 L213,40.2 L214,42.0 L215,43.8 L216,45.0 L217,45.5 L218,45.0 L219,43.8 L220,42.0 L221,40.2 L222,39.0 L223,38.5 L224,39.0 L225,40.2 L226,42.0 L227,43.8 L228,45.0 L229,45.5 L230,45.0 L231,43.8 L232,42.0 L233,40.3 L234,39.0 L235,38.5 L236,39.0 L237,40.3 L238,42.0 L239,43.7 L240,45.0 L241,45.5 L242,45.0 L243,43.8 L244,42.0 L245,40.3 L246,39.0 L247,38.5 L248,39.0 L249,40.2 L250,42.0 L251,43.8 L252,45.0 L253,45.5 L254,45.0 L255,43.8 L256,42.0 L257,40.3 L258,39.0 L259,38.5 L260,39.0 L261,40.3 L262,42.0 L263,43.7 L264,45.0 L265,45.5 L266,45.0 L267,43.8 L268,42.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,58.0 L29,57.1 L30,56.4 L31,56.2 L32,56.4 L33,57.1 L34,58.0 L35,58.9 L36,59.6 L37,59.8 L38,59.6 L39,58.9 L40,58.0 L41,57.1 L42,56.4 L43,56.2 L44,56.4 L45,57.1 L46,58.0 L47,58.9 L48,59.6 L49,59.8 L50,59.6 L51,58.9 L52,58.0 L53,57.1 L54,56.4 L55,56.2 L56,56.4 L57,57.1 L58,58.0 L59,58.9 L60,59.6 L61,59.8 L62,59.6 L63,58.9 L64,58.0 L65,57.1 L66,56.4 L67,56.2 L68,56.4 L69,57.1 L70,58.0 L71,58.9 L72,59.6 L73,59.8 L74,59.6 L75,58.9 L76,58.0 L77,57.1 L78,56.4 L79,56.2 L80,56.4 L81,57.1 L82,58.0 L83,58.9 L84,59.6 L85,59.8 L86,59.6 L87,58.9 L88,58.0 L89,57.1 L90,56.4 L91,56.2 L92,56.4 L93,57.1 L94,58.0 L95,58.9 L96,59.6 L97,59.8 L98,59.6 L99,58.9 L100,58.0 L101,57.1 L102,56.4 L103,56.2 L104,56.4 L105,57.1 L106,58.0 L107,58.9 L108,59.6 L109,59.8 L110,59.6 L111,58.9 L112,58.0 L113,57.1 L114,56.4 L115,56.2 L116,56.4 L117,57.1 L118,58.0 L119,58.9 L120,59.6 L121,59.8 L122,59.6 L123,58.9 L124,58.0 L125,57.1 L126,56.4 L127,56.2 L128,56.4 L129,57.1 L130,58.0 L131,58.9 L132,59.6 L133,59.8 L134,59.6 L135,58.9 L136,58.0 L137,57.1 L138,56.4 L139,56.2 L140,56.4 L141,57.1 L142,58.0 L143,58.9 L144,59.6 L145,59.8 L146,59.6 L147,58.9 L148,58.0 L149,57.1 L150,56.4 L151,56.2 L152,56.4 L153,57.1 L154,58.0 L155,58.9 L156,59.6 L157,59.8 L158,59.6 L159,58.9 L160,58.0 L161,57.1 L162,56.4 L163,56.2 L164,56.4 L165,57.1 L166,58.0 L167,58.9 L168,59.6 L169,59.8 L170,59.6 L171,58.9 L172,58.0 L173,57.1 L174,56.4 L175,56.2 L176,56.4 L177,57.1 L178,58.0 L179,58.9 L180,59.6 L181,59.8 L182,59.6 L183,58.9 L184,58.0 L185,57.1 L186,56.4 L187,56.2 L188,56.4 L189,57.1 L190,58.0 L191,58.9 L192,59.6 L193,59.8 L194,59.6 L195,58.9 L196,58.0 L197,57.1 L198,56.4 L199,56.2 L200,56.4 L201,57.1 L202,58.0 L203,58.9 L204,59.6 L205,59.8 L206,59.6 L207,58.9 L208,58.0 L209,57.1 L210,56.4 L211,56.2 L212,56.4 L213,57.1 L214,58.0 L215,58.9 L216,59.6 L217,59.8 L218,59.6 L219,58.9 L220,58.0 L221,57.1 L222,56.4 L223,56.2 L224,56.4 L225,57.1 L226,58.0 L227,58.9 L228,59.6 L229,59.8 L230,59.6 L231,58.9 L232,58.0 L233,57.1 L234,56.4 L235,56.2 L236,56.4 L237,57.1 L238,58.0 L239,58.9 L240,59.6 L241,59.8 L242,59.6 L243,58.9 L244,58.0 L245,57.1 L246,56.4 L247,56.2 L248,56.4 L249,57.1 L250,58.0 L251,58.9 L252,59.6 L253,59.8 L254,59.6 L255,58.9 L256,58.0 L257,57.1 L258,56.4 L259,56.2 L260,56.4 L261,57.1 L262,58.0 L263,58.9 L264,59.6 L265,59.8 L266,59.6 L267,58.9 L268,58.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,74.0 L29,72.8 L30,71.8 L31,71.5 L32,71.8 L33,72.8 L34,74.0 L35,75.2 L36,76.2 L37,76.5 L38,76.2 L39,75.2 L40,74.0 L41,72.8 L42,71.8 L43,71.5 L44,71.8 L45,72.8 L46,74.0 L47,75.2 L48,76.2 L49,76.5 L50,76.2 L51,75.2 L52,74.0 L53,72.8 L54,71.8 L55,71.5 L56,71.8 L57,72.8 L58,74.0 L59,75.2 L60,76.2 L61,76.5 L62,76.2 L63,75.2 L64,74.0 L65,72.8 L66,71.8 L67,71.5 L68,71.8 L69,72.7 L70,74.0 L71,75.2 L72,76.2 L73,76.5 L74,76.2 L75,75.2 L76,74.0 L77,72.8 L78,71.8 L79,71.5 L80,71.8 L81,72.8 L82,74.0 L83,75.2 L84,76.2 L85,76.5 L86,76.2 L87,75.2 L88,74.0 L89,72.8 L90,71.8 L91,71.5 L92,71.8 L93,72.8 L94,74.0 L95,75.2 L96,76.2 L97,76.5 L98,76.2 L99,75.2 L100,74.0 L101,72.8 L102,71.8 L103,71.5 L104,71.8 L105,72.8 L106,74.0 L107,75.2 L108,76.2 L109,76.5 L110,76.2 L111,75.2 L112,74.0 L113,72.8 L114,71.8 L115,71.5 L116,71.8 L117,72.8 L118,74.0 L119,75.2 L120,76.2 L121,76.5 L122,76.2 L123,75.2 L124,74.0 L125,72.8 L126,71.8 L127,71.5 L128,71.8 L129,72.8 L130,74.0 L131,75.2 L132,76.2 L133,76.5 L134,76.2 L135,75.3 L136,74.0 L137,72.8 L138,71.8 L139,71.5 L140,71.8 L141,72.8 L142,74.0 L143,75.3 L144,76.2 L145,76.5 L146,76.2 L147,75.3 L148,74.0 L149,72.8 L150,71.8 L151,71.5 L152,71.8 L153,72.8 L154,74.0 L155,75.3 L156,76.2 L157,76.5 L158,76.2 L159,75.2 L160,74.0 L161,72.8 L162,71.8 L163,71.5 L164,71.8 L165,72.8 L166,74.0 L167,75.2 L168,76.2 L169,76.5 L170,76.2 L171,75.3 L172,74.0 L173,72.8 L174,71.8 L175,71.5 L176,71.8 L177,72.8 L178,74.0 L179,75.2 L180,76.2 L181,76.5 L182,76.2 L183,75.2 L184,74.0 L185,72.8 L186,71.8 L187,71.5 L188,71.8 L189,72.7 L190,74.0 L191,75.2 L192,76.2 L193,76.5 L194,76.2 L195,75.2 L196,74.0 L197,72.8 L198,71.8 L199,71.5 L200,71.8 L201,72.8 L202,74.0 L203,75.2 L204,76.2 L205,76.5 L206,76.2 L207,75.2 L208,74.0 L209,72.8 L210,71.8 L211,71.5 L212,71.8 L213,72.7 L214,74.0 L215,75.3 L216,76.2 L217,76.5 L218,76.2 L219,75.3 L220,74.0 L221,72.8 L222,71.8 L223,71.5 L224,71.8 L225,72.7 L226,74.0 L227,75.2 L228,76.2 L229,76.5 L230,76.2 L231,75.2 L232,74.0 L233,72.8 L234,71.8 L235,71.5 L236,71.8 L237,72.8 L238,74.0 L239,75.2 L240,76.2 L241,76.5 L242,76.2 L243,75.3 L244,74.0 L245,72.8 L246,71.8 L247,71.5 L248,71.8 L249,72.7 L250,74.0 L251,75.2 L252,76.2 L253,76.5 L254,76.2 L255,75.3 L256,74.0 L257,72.8 L258,71.8 L259,71.5 L260,71.8 L261,72.8 L262,74.0 L263,75.2 L264,76.2 L265,76.5 L266,76.2 L267,75.3 L268,74.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,90.0 L29,89.4 L30,89.0 L31,88.8 L32,89.0 L33,89.4 L34,90.0 L35,90.6 L36,91.0 L37,91.2 L38,91.0 L39,90.6 L40,90.0 L41,89.4 L42,89.0 L43,88.8 L44,89.0 L45,89.4 L46,90.0 L47,90.6 L48,91.0 L49,91.2 L50,91.0 L51,90.6 L52,90.0 L53,89.4 L54,89.0 L55,88.8 L56,89.0 L57,89.4 L58,90.0 L59,90.6 L60,91.0 L61,91.2 L62,91.0 L63,90.6 L64,90.0 L65,89.4 L66,89.0 L67,88.8 L68,89.0 L69,89.4 L70,90.0 L71,90.6 L72,91.0 L73,91.2 L74,91.0 L75,90.6 L76,90.0 L77,89.4 L78,89.0 L79,88.8 L80,89.0 L81,89.4 L82,90.0 L83,90.6 L84,91.0 L85,91.2 L86,91.0 L87,90.6 L88,90.0 L89,89.4 L90,89.0 L91,88.8 L92,89.0 L93,89.4 L94,90.0 L95,90.6 L96,91.0 L97,91.2 L98,91.0 L99,90.6 L100,90.0 L101,89.4 L102,89.0 L103,88.8 L104,89.0 L105,89.4 L106,90.0 L107,90.6 L108,91.0 L109,91.2 L110,91.0 L111,90.6 L112,90.0 L113,89.4 L114,89.0 L115,88.8 L116,89.0 L117,89.4 L118,90.0 L119,90.6 L120,91.0 L121,91.2 L122,91.0 L123,90.6 L124,90.0 L125,89.4 L126,89.0 L127,88.8 L128,89.0 L129,89.4 L130,90.0 L131,90.6 L132,91.0 L133,91.2 L134,91.0 L135,90.6 L136,90.0 L137,89.4 L138,89.0 L139,88.8 L140,89.0 L141,89.4 L142,90.0 L143,90.6 L144,91.0 L145,91.2 L146,91.0 L147,90.6 L148,90.0 L149,89.4 L150,89.0 L151,88.8 L152,89.0 L153,89.4 L154,90.0 L155,90.6 L156,91.0 L157,91.2 L158,91.0 L159,90.6 L160,90.0 L161,89.4 L162,89.0 L163,88.8 L164,89.0 L165,89.4 L166,90.0 L167,90.6 L168,91.0 L169,91.2 L170,91.0 L171,90.6 L172,90.0 L173,89.4 L174,89.0 L175,88.8 L176,89.0 L177,89.4 L178,90.0 L179,90.6 L180,91.0 L181,91.2 L182,91.0 L183,90.6 L184,90.0 L185,89.4 L186,89.0 L187,88.8 L188,89.0 L189,89.4 L190,90.0 L191,90.6 L192,91.0 L193,91.2 L194,91.0 L195,90.6 L196,90.0 L197,89.4 L198,89.0 L199,88.8 L200,89.0 L201,89.4 L202,90.0 L203,90.6 L204,91.0 L205,91.2 L206,91.0 L207,90.6 L208,90.0 L209,89.4 L210,89.0 L211,88.8 L212,89.0 L213,89.4 L214,90.0 L215,90.6 L216,91.0 L217,91.2 L218,91.0 L219,90.6 L220,90.0 L221,89.4 L222,89.0 L223,88.8 L224,89.0 L225,89.4 L226,90.0 L227,90.6 L228,91.0 L229,91.2 L230,91.0 L231,90.6 L232,90.0 L233,89.4 L234,89.0 L235,88.8 L236,89.0 L237,89.4 L238,90.0 L239,90.6 L240,91.0 L241,91.2 L242,91.0 L243,90.6 L244,90.0 L245,89.4 L246,89.0 L247,88.8 L248,89.0 L249,89.4 L250,90.0 L251,90.6 L252,91.0 L253,91.2 L254,91.0 L255,90.6 L256,90.0 L257,89.4 L258,89.0 L259,88.8 L260,89.0 L261,89.4 L262,90.0 L263,90.6 L264,91.0 L265,91.2 L266,91.0 L267,90.6 L268,90.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,106.0 L29,104.6 L30,103.6 L31,103.2 L32,103.6 L33,104.6 L34,106.0 L35,107.4 L36,108.4 L37,108.8 L38,108.4 L39,107.4 L40,106.0 L41,104.6 L42,103.6 L43,103.2 L44,103.6 L45,104.6 L46,106.0 L47,107.4 L48,108.4 L49,108.8 L50,108.4 L51,107.4 L52,106.0 L53,104.6 L54,103.6 L55,103.2 L56,103.6 L57,104.6 L58,106.0 L59,107.4 L60,108.4 L61,108.8 L62,108.4 L63,107.4 L64,106.0 L65,104.6 L66,103.6 L67,103.2 L68,103.6 L69,104.6 L70,106.0 L71,107.4 L72,108.4 L73,108.8 L74,108.4 L75,107.4 L76,106.0 L77,104.6 L78,103.6 L79,103.2 L80,103.6 L81,104.6 L82,106.0 L83,107.4 L84,108.4 L85,108.8 L86,108.4 L87,107.4 L88,106.0 L89,104.6 L90,103.6 L91,103.2 L92,103.6 L93,104.6 L94,106.0 L95,107.4 L96,108.4 L97,108.8 L98,108.4 L99,107.4 L100,106.0 L101,104.6 L102,103.6 L103,103.2 L104,103.6 L105,104.6 L106,106.0 L107,107.4 L108,108.4 L109,108.8 L110,108.4 L111,107.4 L112,106.0 L113,104.6 L114,103.6 L115,103.2 L116,103.6 L117,104.6 L118,106.0 L119,107.4 L120,108.4 L121,108.8 L122,108.4 L123,107.4 L124,106.0 L125,104.6 L126,103.6 L127,103.2 L128,103.6 L129,104.6 L130,106.0 L131,107.4 L132,108.4 L133,108.8 L134,108.4 L135,107.4 L136,106.0 L137,104.6 L138,103.6 L139,103.2 L140,103.6 L141,104.6 L142,106.0 L143,107.4 L144,108.4 L145,108.8 L146,108.4 L147,107.4 L148,106.0 L149,104.6 L150,103.6 L151,103.2 L152,103.6 L153,104.6 L154,106.0 L155,107.4 L156,108.4 L157,108.8 L158,108.4 L159,107.4 L160,106.0 L161,104.6 L162,103.6 L163,103.2 L164,103.6 L165,104.6 L166,106.0 L167,107.4 L168,108.4 L169,108.8 L170,108.4 L171,107.4 L172,106.0 L173,104.6 L174,103.6 L175,103.2 L176,103.6 L177,104.6 L178,106.0 L179,107.4 L180,108.4 L181,108.8 L182,108.4 L183,107.4 L184,106.0 L185,104.6 L186,103.6 L187,103.2 L188,103.6 L189,104.6 L190,106.0 L191,107.4 L192,108.4 L193,108.8 L194,108.4 L195,107.4 L196,106.0 L197,104.6 L198,103.6 L199,103.2 L200,103.6 L201,104.6 L202,106.0 L203,107.4 L204,108.4 L205,108.8 L206,108.4 L207,107.4 L208,106.0 L209,104.6 L210,103.6 L211,103.2 L212,103.6 L213,104.6 L214,106.0 L215,107.4 L216,108.4 L217,108.8 L218,108.4 L219,107.4 L220,106.0 L221,104.6 L222,103.6 L223,103.2 L224,103.6 L225,104.6 L226,106.0 L227,107.4 L228,108.4 L229,108.8 L230,108.4 L231,107.4 L232,106.0 L233,104.6 L234,103.6 L235,103.2 L236,103.6 L237,104.6 L238,106.0 L239,107.4 L240,108.4 L241,108.8 L242,108.4 L243,107.4 L244,106.0 L245,104.6 L246,103.6 L247,103.2 L248,103.6 L249,104.6 L250,106.0 L251,107.4 L252,108.4 L253,108.8 L254,108.4 L255,107.4 L256,106.0 L257,104.6 L258,103.6 L259,103.2 L260,103.6 L261,104.6 L262,106.0 L263,107.4 L264,108.4 L265,108.8 L266,108.4 L267,107.4 L268,106.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/><path d="M28,122.0 L29,120.5 L30,119.4 L31,119.0 L32,119.4 L33,120.5 L34,122.0 L35,123.5 L36,124.6 L37,125.0 L38,124.6 L39,123.5 L40,122.0 L41,120.5 L42,119.4 L43,119.0 L44,119.4 L45,120.5 L46,122.0 L47,123.5 L48,124.6 L49,125.0 L50,124.6 L51,123.5 L52,122.0 L53,120.5 L54,119.4 L55,119.0 L56,119.4 L57,120.5 L58,122.0 L59,123.5 L60,124.6 L61,125.0 L62,124.6 L63,123.5 L64,122.0 L65,120.5 L66,119.4 L67,119.0 L68,119.4 L69,120.5 L70,122.0 L71,123.5 L72,124.6 L73,125.0 L74,124.6 L75,123.5 L76,122.0 L77,120.5 L78,119.4 L79,119.0 L80,119.4 L81,120.5 L82,122.0 L83,123.5 L84,124.6 L85,125.0 L86,124.6 L87,123.5 L88,122.0 L89,120.5 L90,119.4 L91,119.0 L92,119.4 L93,120.5 L94,122.0 L95,123.5 L96,124.6 L97,125.0 L98,124.6 L99,123.5 L100,122.0 L101,120.5 L102,119.4 L103,119.0 L104,119.4 L105,120.5 L106,122.0 L107,123.5 L108,124.6 L109,125.0 L110,124.6 L111,123.5 L112,122.0 L113,120.5 L114,119.4 L115,119.0 L116,119.4 L117,120.5 L118,122.0 L119,123.5 L120,124.6 L121,125.0 L122,124.6 L123,123.5 L124,122.0 L125,120.5 L126,119.4 L127,119.0 L128,119.4 L129,120.5 L130,122.0 L131,123.5 L132,124.6 L133,125.0 L134,124.6 L135,123.5 L136,122.0 L137,120.5 L138,119.4 L139,119.0 L140,119.4 L141,120.5 L142,122.0 L143,123.5 L144,124.6 L145,125.0 L146,124.6 L147,123.5 L148,122.0 L149,120.5 L150,119.4 L151,119.0 L152,119.4 L153,120.5 L154,122.0 L155,123.5 L156,124.6 L157,125.0 L158,124.6 L159,123.5 L160,122.0 L161,120.5 L162,119.4 L163,119.0 L164,119.4 L165,120.5 L166,122.0 L167,123.5 L168,124.6 L169,125.0 L170,124.6 L171,123.5 L172,122.0 L173,120.5 L174,119.4 L175,119.0 L176,119.4 L177,120.5 L178,122.0 L179,123.5 L180,124.6 L181,125.0 L182,124.6 L183,123.5 L184,122.0 L185,120.5 L186,119.4 L187,119.0 L188,119.4 L189,120.5 L190,122.0 L191,123.5 L192,124.6 L193,125.0 L194,124.6 L195,123.5 L196,122.0 L197,120.5 L198,119.4 L199,119.0 L200,119.4 L201,120.5 L202,122.0 L203,123.5 L204,124.6 L205,125.0 L206,124.6 L207,123.5 L208,122.0 L209,120.5 L210,119.4 L211,119.0 L212,119.4 L213,120.5 L214,122.0 L215,123.5 L216,124.6 L217,125.0 L218,124.6 L219,123.5 L220,122.0 L221,120.5 L222,119.4 L223,119.0 L224,119.4 L225,120.5 L226,122.0 L227,123.5 L228,124.6 L229,125.0 L230,124.6 L231,123.5 L232,122.0 L233,120.5 L234,119.4 L235,119.0 L236,119.4 L237,120.5 L238,122.0 L239,123.5 L240,124.6 L241,125.0 L242,124.6 L243,123.5 L244,122.0 L245,120.5 L246,119.4 L247,119.0 L248,119.4 L249,120.5 L250,122.0 L251,123.5 L252,124.6 L253,125.0 L254,124.6 L255,123.5 L256,122.0 L257,120.5 L258,119.4 L259,119.0 L260,119.4 L261,120.5 L262,122.0 L263,123.5 L264,124.6 L265,125.0 L266,124.6 L267,123.5 L268,122.0" stroke="#67e8f9" stroke-width="0.9" fill="none"/></g>
            </g>
            <text x="2" y="10" font-size="3.2" font-family="monospace" fill="#67e8f9">Fp1</text>
            <text x="2" y="26" font-size="3.2" font-family="monospace" fill="#67e8f9">Fp2</text>
            <text x="2" y="42" font-size="3.2" font-family="monospace" fill="#67e8f9">F3</text>
            <text x="2" y="58" font-size="3.2" font-family="monospace" fill="#67e8f9">F4</text>
            <text x="2" y="74" font-size="3.2" font-family="monospace" fill="#67e8f9">C3</text>
            <text x="2" y="90" font-size="3.2" font-family="monospace" fill="#67e8f9">C4</text>
            <text x="2" y="106" font-size="3.2" font-family="monospace" fill="#67e8f9">O1</text>
            <text x="2" y="122" font-size="3.2" font-family="monospace" fill="#67e8f9">O2</text>
            <line x1="2" y1="135" x2="218" y2="135" stroke="#f9a8d4" stroke-width="0.6" stroke-dasharray="2 2" opacity="0.6"/>
            <text x="2" y="155" font-size="3.2" font-family="monospace" fill="#f9a8d4">GazeX</text>
            <text x="2" y="172" font-size="3.2" font-family="monospace" fill="#f9a8d4">GazeY</text>
            <g clip-path="url(#s13-gaze-clip)">
              <g class="s13-gaze-flow"><path d="M28,155 L28,150 L38,150 L38,160 L48,160 L48,150 L58,150 L58,160 L68,160 L68,150 L78,150 L78,160 L88,160 L88,150 L98,150 L98,160 L108,160 L108,150 L118,150 L118,160 L128,160 L128,150 L138,150 L138,160 L148,160 L148,150 L158,150 L158,160 L168,160 L168,150 L178,150 L178,160 L188,160 L188,150 L198,150 L198,160 L208,160 L208,150 L218,150 L218,160 L228,160 L228,150 L238,150 L238,160 L248,160 L248,150 L258,150 L258,160 L268,160" stroke="#f9a8d4" stroke-width="0.9" fill="none"/><path d="M28,172 L28,167 L40,167 L40,177 L52,177 L52,167 L64,167 L64,177 L76,177 L76,167 L88,167 L88,177 L100,177 L100,167 L112,167 L112,177 L124,177 L124,167 L136,167 L136,177 L148,177 L148,167 L160,167 L160,177 L172,177 L172,167 L184,167 L184,177 L196,177 L196,167 L208,167 L208,177 L220,177 L220,167 L232,167 L232,177 L244,177 L244,167 L256,167 L256,177 L268,177" stroke="#f9a8d4" stroke-width="0.9" fill="none"/></g>
            </g>
          </svg>
          <div class="text-[8px] text-slate-400 font-mono text-center mt-0.5 flex-shrink-0">← time (T samples) →</div>
        </div>
        <div class="flex flex-col items-center justify-center gap-1 min-h-0">
          <div class="border-2 border-purple-400 rounded-md px-2 py-2 bg-purple-950/40 text-center flex-shrink-0">
            <div class="text-[10px] font-bold text-purple-200 leading-tight">STFT</div>
            <div class="text-[9px] text-purple-200/80 font-mono leading-tight mt-0.5">spectrogram()</div>
            <div class="text-[9px] text-purple-200/80 font-mono leading-tight">hann · |S|² · dB</div>
          </div>
          <svg viewBox="0 0 60 12" class="w-12 h-3 flex-shrink-0"><path d="M0 6 L52 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s13-dash"/><path d="M50 2 L56 6 L50 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg>
          <div class="text-[8.5px] text-slate-300/80 font-mono text-center flex-shrink-0">per channel<br/>k = 1..C</div>
        </div>
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 flex flex-col min-h-0 overflow-hidden">
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-fuchsia-300 text-center mb-1 flex-shrink-0">Per-Ch Spectrograms</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0">
            <div class="flex-[8] rounded-sm overflow-hidden relative s13-spec-row min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 25%, #06b6d4 50%, #fbbf24 75%, #ef4444 100%);">
              <div class="absolute inset-0 s13-spec-bands"></div>
              <div class="absolute inset-0 s13-spec-noise"></div>
            </div>
            <div class="h-[2px] bg-pink-400/80 flex-shrink-0 s13-divider-glow"></div>
            <div class="flex-[2] rounded-sm overflow-hidden relative s13-spec-row min-h-0" style="background: linear-gradient(to right, #18181b 0%, #831843 35%, #db2777 70%, #f9a8d4 100%); animation-delay: -1.2s;">
              <div class="absolute inset-0 s13-spec-bands-pink"></div>
              <div class="absolute inset-0 s13-spec-noise"></div>
            </div>
          </div>
          <div class="text-[8px] text-slate-400 font-mono text-center mt-0.5 flex-shrink-0">← time (M frames) →</div>
        </div>
        <div class="flex flex-col items-center justify-center gap-1 min-h-0">
          <div class="border-2 border-emerald-400 rounded-md px-2 py-2 bg-emerald-950/40 text-center flex-shrink-0">
            <div class="text-[10px] font-bold text-emerald-200 leading-tight">V-STACK</div>
            <div class="text-[9px] text-emerald-200/80 font-mono leading-tight mt-0.5">concat ch</div>
            <div class="text-[9px] text-emerald-200/80 font-mono leading-tight">norm [0,1]</div>
          </div>
          <svg viewBox="0 0 60 12" class="w-12 h-3 flex-shrink-0"><path d="M0 6 L52 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s13-dash"/><path d="M50 2 L56 6 L50 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg>
          <div class="text-[8.5px] text-slate-300/80 font-mono text-center flex-shrink-0">freq × ch ↑</div>
        </div>
        <div class="grid grid-cols-[1fr_auto] gap-1.5 items-stretch min-h-0">
          <div class="border-2 border-emerald-400/70 rounded-md p-1.5 bg-emerald-950/20 flex flex-col min-h-0 overflow-hidden">
            <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-emerald-300 text-center mb-1 flex-shrink-0">Stacked Output</div>
            <div class="flex-1 flex flex-col gap-[1px] rounded-sm overflow-hidden relative min-h-0">
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 25%, #06b6d4 50%, #fbbf24 75%, #ef4444 100%);"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 30%, #06b6d4 55%, #fbbf24 80%, #ef4444 100%); animation-delay: -0.2s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 20%, #06b6d4 45%, #fbbf24 70%, #ef4444 100%); animation-delay: -0.4s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 35%, #06b6d4 60%, #fbbf24 85%, #ef4444 100%); animation-delay: -0.6s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 25%, #06b6d4 50%, #fbbf24 75%, #ef4444 100%); animation-delay: -0.8s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 28%, #06b6d4 52%, #fbbf24 78%, #ef4444 100%); animation-delay: -1.0s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 22%, #06b6d4 48%, #fbbf24 72%, #ef4444 100%); animation-delay: -1.2s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 32%, #06b6d4 58%, #fbbf24 82%, #ef4444 100%); animation-delay: -1.4s;"></div>
              <div class="h-[2px] bg-yellow-300 my-0.5 flex-shrink-0"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #18181b 0%, #831843 35%, #db2777 70%, #f9a8d4 100%); animation-delay: -1.6s;"></div>
              <div class="flex-1 s13-stack-shimmer min-h-0" style="background: linear-gradient(to right, #18181b 0%, #831843 30%, #db2777 65%, #f9a8d4 100%); animation-delay: -1.8s;"></div>
            </div>
            <div class="text-[8px] text-slate-400 font-mono text-center mt-0.5 flex-shrink-0">← time →</div>
          </div>
          <div class="flex flex-col justify-center gap-2 text-[8px] font-mono">
            <div class="flex items-center gap-1">
              <div class="text-cyan-300 text-[9px] font-bold">}</div>
              <div>
                <div class="text-cyan-300 font-bold">EEG.img</div>
                <div class="text-[9px] text-cyan-200/70 leading-tight">(n_fp×8, n_time)</div>
                <div class="text-[9px] text-cyan-200/70 leading-tight">single [0, 1]</div>
              </div>
            </div>
            <div class="flex items-center gap-1">
              <div class="text-pink-300 text-[9px] font-bold">}</div>
              <div>
                <div class="text-pink-300 font-bold">Gaze.img</div>
                <div class="text-[9px] text-pink-200/70 leading-tight">(n_fp×2, n_time)</div>
                <div class="text-[9px] text-pink-200/70 leading-tight">single [0, 1]</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex items-center justify-center gap-3 -my-0.5">
      <div class="flex items-center gap-1.5">
        <div class="px-2 py-0.5 rounded bg-orange-500/20 border border-orange-400/60 text-[8px] font-mono font-bold text-orange-300 s13-transition-tag">→ STFT</div>
      </div>
      <div class="text-[7.5px] font-mono text-slate-500">|</div>
      <div class="flex items-center gap-1.5">
        <div class="px-2 py-0.5 rounded bg-orange-500/20 border border-orange-400/60 text-[8px] font-mono font-bold text-orange-300 s13-transition-tag">STACK →</div>
      </div>
    </div>
    <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1.3]">
      <div class="bg-gradient-to-r from-violet-500/20 via-violet-500/5 to-transparent px-2 py-0.5 border-b border-violet-400/30">
        <div class="text-[10px] font-mono font-bold text-violet-300">▸ Mathematical Description · 4 Sub-Steps</div>
      </div>
      <div class="p-2 grid grid-cols-[1fr_auto_1fr_auto_1fr_auto_1fr] gap-1.5 items-stretch">
        <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 relative s13-formula-1">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s13-badge">A</div>
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 text-center tracking-wider">Step A</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Hann Window</div>
          <div class="text-[7.5px] text-cyan-200/70 text-center leading-tight mt-0.5">Reduce spectral leakage<br/>applied per frame</div>
          <div class="text-center mt-1 text-[9px] text-cyan-100 font-serif italic">w(n) = ½(1 − cos 2πn/N<sub>w</sub>−1)</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s13-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-purple-400/60 rounded-md p-1.5 bg-purple-950/20 relative s13-formula-2">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-purple-500 border border-purple-200 flex items-center justify-center text-[8px] font-bold text-white s13-badge">B</div>
          <div class="text-[8px] uppercase font-mono font-bold text-purple-300 text-center tracking-wider">Step B</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">FFT Per Frame</div>
          <div class="text-[7.5px] text-purple-200/70 text-center leading-tight mt-0.5">DFT of windowed frame<br/>time → frequency domain</div>
          <div class="text-center mt-1 text-[9px] text-purple-100 font-serif italic">S<sup>c</sup><sub>m,k</sub> = Σ x<sup>c</sup><sub>m</sub> · w · e<sup>−j2πkn/N</sup></div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s13-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 relative s13-formula-3">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s13-badge">C</div>
          <div class="text-[8px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider">Step C</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Power + dB</div>
          <div class="text-[7.5px] text-fuchsia-200/70 text-center leading-tight mt-0.5">Squared magnitude<br/>log compression (decibel)</div>
          <div class="text-center mt-1 text-[9px] text-fuchsia-100 font-serif italic">L<sup>c</sup> = 10 log<sub>10</sub>(|S<sup>c</sup>|² + ε)</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s13-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s13-formula-4">
          <div class="absolute -top-1.5 -left-1.5 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s13-badge">D</div>
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider">Step D</div>
          <div class="text-[10px] font-bold text-white text-center mt-0.5">Stack + Normalize</div>
          <div class="text-[7.5px] text-emerald-200/70 text-center leading-tight mt-0.5">Concat C channels vertically<br/>min-max scale to [0, 1]</div>
          <div class="text-center mt-1 text-[9px] text-emerald-100 font-serif italic">X̂ = (X − X<sub>min</sub>) / (X<sub>max</sub> − X<sub>min</sub>)</div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>EEG Signal</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-pink-400 rounded-sm"></div>Gaze Signal</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-sm"></div>Spectrogram (freq↑)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Stacked (time→)</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-yellow-400"></div>Data Flow</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-orange-400"></div>Transition</div>
    </div>
  </div>
</div>

<style>
@keyframes s13SignalFlow { 0% { transform: translate3d(0,0,0); } 100% { transform: translate3d(-12px,0,0); } }
.s13-signal-flow { animation: s13SignalFlow 1.2s linear infinite; will-change: transform; }
@keyframes s13GazeFlow { 0% { transform: translate3d(0,0,0); } 100% { transform: translate3d(-24px,0,0); } }
.s13-gaze-flow { animation: s13GazeFlow 1.6s linear infinite; will-change: transform; }
@keyframes s13PulsePurple {
  0%, 100% { box-shadow: 0 0 8px rgba(168,85,247,0.3), inset 0 0 6px rgba(168,85,247,0.1); border-color: rgba(192,132,252,0.7); }
  50% { box-shadow: 0 0 22px #a855f7, 0 0 36px rgba(168,85,247,0.6), inset 0 0 14px rgba(192,132,252,0.3); border-color: #c084fc; }
}
.s13-pulse-purple { animation: s13PulsePurple 2.4s ease-in-out infinite; }
@keyframes s13PulseEmerald {
  0%, 100% { box-shadow: 0 0 8px rgba(52,211,153,0.3), inset 0 0 6px rgba(52,211,153,0.1); border-color: rgba(110,231,183,0.7); }
  50% { box-shadow: 0 0 22px #10b981, 0 0 36px rgba(52,211,153,0.6), inset 0 0 14px rgba(110,231,183,0.3); border-color: #34d399; }
}
.s13-pulse-emerald { animation: s13PulseEmerald 2.4s ease-in-out infinite; animation-delay: -1.2s; }
@keyframes s13DashMarch { to { stroke-dashoffset: -10; } }
.s13-dash { animation: s13DashMarch 0.6s linear infinite; }
@keyframes s13SpecRow {
  0%, 100% { filter: brightness(1) saturate(1.2); }
  50% { filter: brightness(1.3) saturate(1.6); }
}
.s13-spec-row { animation: s13SpecRow 2s ease-in-out infinite; }
@keyframes s13SpecBands {
  0% { background-position: 0px 0; }
  100% { background-position: -60px 0; }
}
@keyframes s13SpecBandsPink {
  0% { background-position: 0px 0; }
  100% { background-position: -50px 0; }
}
.s13-spec-bands {
  background: repeating-linear-gradient(90deg,
    rgba(255,255,255,0) 0px,
    rgba(255,255,255,0) 6px,
    rgba(255,255,255,0.18) 7px,
    rgba(255,255,255,0) 9px,
    rgba(0,0,0,0.25) 14px,
    rgba(0,0,0,0) 18px,
    rgba(255,255,255,0.12) 22px,
    rgba(255,255,255,0) 26px);
  background-size: 60px 100%;
  animation: s13SpecBands 2.5s linear infinite;
  mix-blend-mode: overlay;
}
.s13-spec-bands-pink {
  background: repeating-linear-gradient(90deg,
    rgba(255,255,255,0) 0px,
    rgba(255,255,255,0) 5px,
    rgba(255,255,255,0.2) 6px,
    rgba(255,255,255,0) 8px,
    rgba(0,0,0,0.3) 12px,
    rgba(0,0,0,0) 16px,
    rgba(255,255,255,0.15) 20px,
    rgba(255,255,255,0) 24px);
  background-size: 50px 100%;
  animation: s13SpecBandsPink 2.2s linear infinite;
  mix-blend-mode: overlay;
}
@keyframes s13SpecNoise {
  0%, 100% { opacity: 0.3; transform: translateX(0); }
  50% { opacity: 0.5; transform: translateX(2px); }
}
.s13-spec-noise { 
  background: repeating-linear-gradient(90deg, rgba(0,0,0,0) 0px, rgba(0,0,0,0) 3px, rgba(255,255,255,0.08) 3px, rgba(255,255,255,0.08) 5px);
  animation: s13SpecNoise 1.5s ease-in-out infinite;
}
@keyframes s13DividerGlow {
  0%, 100% { box-shadow: 0 0 4px currentColor, 0 0 8px rgba(244,114,182,0.5); }
  50% { box-shadow: 0 0 10px currentColor, 0 0 20px rgba(244,114,182,0.9); }
}
.s13-divider-glow { animation: s13DividerGlow 1.8s ease-in-out infinite; color: #f472b6; }
@keyframes s13StackShimmer {
  0%, 100% { filter: brightness(1) saturate(1.3); }
  50% { filter: brightness(1.4) saturate(1.7); }
}
.s13-stack-shimmer { animation: s13StackShimmer 2.5s ease-in-out infinite; }
@keyframes s13StackedGlow {
  0%, 100% { box-shadow: 0 0 12px rgba(52,211,153,0.4), inset 0 0 8px rgba(52,211,153,0.1); border-color: rgba(52,211,153,0.7); }
  50% { box-shadow: 0 0 28px rgba(52,211,153,0.8), 0 0 50px rgba(52,211,153,0.4), inset 0 0 18px rgba(52,211,153,0.25); border-color: #34d399; }
}
.s13-stacked-glow { animation: s13StackedGlow 2.8s ease-in-out infinite; }
@keyframes s13TransitionGlow {
  0%, 100% { box-shadow: 0 0 4px rgba(251,146,60,0.3); transform: scale(1); }
  50% { box-shadow: 0 0 14px rgba(251,146,60,0.8); transform: scale(1.05); }
}
.s13-transition-tag { animation: s13TransitionGlow 1.8s ease-in-out infinite; }
@keyframes s13BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s13-badge { animation: s13BadgePulse 2s ease-in-out infinite; }
@keyframes s13FormulaActivate {
  0%, 80%, 100% { box-shadow: inset 0 0 0 1px transparent; filter: brightness(1) saturate(1); border-color: currentColor; transform: scale(1); }
  88%, 92% { box-shadow: 0 0 20px currentColor, 0 0 35px currentColor, inset 0 0 16px rgba(255,255,255,0.25), inset 0 0 0 2px currentColor; filter: brightness(1.8) saturate(1.6); transform: scale(1.03); }
}
[class*="s13-formula-"] { animation: s13FormulaActivate 2.8s ease-in-out infinite; }
.s13-formula-1 { animation-delay: 0s; color: #67e8f9; }
.s13-formula-2 { animation-delay: 0.7s; color: #c084fc; }
.s13-formula-3 { animation-delay: 1.4s; color: #e879f9; }
.s13-formula-4 { animation-delay: 2.1s; color: #34d399; }
@keyframes s13Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s13-pulse { animation: s13Pulse 1.6s ease-in-out infinite; }
@keyframes s13PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s13-pulse-strong { animation: s13PulseStrong 0.9s ease-in-out infinite; }
@keyframes s13BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s13-blink-text { animation: s13BlinkText 0.9s steps(2, end) infinite; }
@keyframes s13Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s13BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s13-bar-pulse-1, .s13-bar-pulse-2, .s13-bar-pulse-3 { animation: s13BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s13-bar-pulse-1 { color: #67e8f9; animation-delay: 0s; }
.s13-bar-pulse-2 { color: #e879f9; animation-delay: -0.8s; }
.s13-bar-pulse-3 { color: #34d399; animation-delay: -1.6s; }
@keyframes s13BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #a78bfa, 0 0 12px rgba(167,139,250,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #a78bfa; transform: scale(0.85); }
}
.s13-bar-dot { animation: s13BarDot 1.6s ease-in-out infinite; }
.s13-breathe-1 { animation: s13Breathe 8s ease-in-out infinite; }
.s13-breathe-2 { animation: s13Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s13-breathe-3 { animation: s13Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s13ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s13-scan-line { animation: s13ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-orange-500/8 rounded-full blur-[140px] s14-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s14-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s14-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s14-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s14-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 14 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Deep Learning </span><span class="bg-gradient-to-r from-orange-300 via-emerald-300 to-fuchsia-300 bg-clip-text text-transparent">Feature Extraction</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-orange-400 rounded-full s14-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s14-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-fuchsia-400 rounded-full s14-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-violet-400 rounded-full s14-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">STFT → CNN Backbones → Per-Modality Feature Vectors</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s14-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s14-blink-text">Live Pipeline</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-1 min-h-0">
    <div class="border border-amber-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-amber-500/20 via-amber-500/5 to-transparent px-2 py-0.5 border-b border-amber-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-amber-300">▸ Feature Extraction · Loop Per CNN Backbone · Output: { EEG | Gaze | EEG+Gaze }</div>
        <div class="flex-1 h-px bg-gradient-to-r from-amber-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-amber-400/70">[ X<sub>STFT</sub> ∈ ℝ<sup>F·C × T × 3</sup> ] → [ f<sub>CNN</sub> ∈ ℝ<sup>1 × D</sup> ] → [ Modality Vectors ]</div>
      </div>
      <div class="p-2 grid grid-cols-[1.6fr_auto_1.6fr_auto_2.6fr_auto_2.2fr_auto_3fr] gap-1 items-stretch flex-1 min-h-0">
        <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">1</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-violet-300 text-center mb-1 flex-shrink-0 pl-5">STFT Spectrogram</div>
          <div class="flex-1 flex flex-col gap-0.5 min-h-0">
            <div class="flex items-center gap-1 flex-shrink-0">
              <div class="text-[7px] font-mono text-violet-200/70 -rotate-90 origin-center" style="width:8px;">Freq↑</div>
              <div class="flex-1 flex flex-col gap-[1px] rounded-sm overflow-hidden" style="height: 60px;">
                <div class="flex-1 s14-spec-row" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 25%, #06b6d4 50%, #fbbf24 75%, #ef4444 100%);"></div>
                <div class="flex-1 s14-spec-row" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 30%, #06b6d4 55%, #fbbf24 80%, #ef4444 100%); animation-delay: -0.4s;"></div>
                <div class="flex-1 s14-spec-row" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 22%, #06b6d4 48%, #fbbf24 72%, #ef4444 100%); animation-delay: -0.8s;"></div>
                <div class="flex-1 s14-spec-row" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 28%, #06b6d4 52%, #fbbf24 78%, #ef4444 100%); animation-delay: -1.2s;"></div>
                <div class="flex-1 s14-spec-row" style="background: linear-gradient(to right, #1e1b4b 0%, #4338ca 26%, #06b6d4 50%, #fbbf24 74%, #ef4444 100%); animation-delay: -1.6s;"></div>
              </div>
            </div>
            <div class="text-[7px] font-mono text-violet-200/70 text-center">← Time →</div>
            <div class="bg-violet-900/40 border border-violet-400/40 rounded px-1 py-0.5 text-center flex-shrink-0">
              <div class="text-[8px] font-mono font-bold text-violet-200">V-Stack · 8 EEG + 2 Gaze</div>
            </div>
            <div class="text-[8.5px] text-center text-violet-100 font-mono">X<sub>STFT</sub> ∈ ℝ<sup>F·C × T × 3</sup></div>
            <div class="text-[8.5px] text-center text-violet-200/60 leading-tight">Parula → RGB<br/>Per-Segment 3-ch image</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">2</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center mb-1 flex-shrink-0 pl-5">Prepared RGB</div>
          <div class="flex-1 flex flex-col justify-center gap-1 min-h-0">
            <div class="border-2 border-orange-400/80 rounded bg-gradient-to-br from-orange-600/30 to-orange-900/20 px-1 py-1 text-center s14-rgb-orange">
              <div class="text-[9px] font-bold text-orange-200 leading-tight">227 × 227 × 3</div>
              <div class="text-[8px] font-mono text-orange-300/90 leading-tight mt-0.5">→ SqueezeNet</div>
            </div>
            <div class="border-2 border-emerald-400/80 rounded bg-gradient-to-br from-emerald-600/30 to-emerald-900/20 px-1 py-1 text-center s14-rgb-emerald">
              <div class="text-[9px] font-bold text-emerald-200 leading-tight">224 × 224 × 3</div>
              <div class="text-[8px] font-mono text-emerald-300/90 leading-tight mt-0.5">→ ShuffleNet</div>
            </div>
          </div>
          <div class="text-[8.5px] text-center text-cyan-200/70 leading-tight mt-1 flex-shrink-0">Resize + Stretch [p1, p99]<br/>One Input → Two Backbones</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">3</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-amber-300 text-center mb-1 flex-shrink-0 pl-5">Pretrained CNN Backbones</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0">
            <div class="border border-orange-400/70 rounded bg-orange-950/30 p-1 flex-1 min-h-0 flex flex-col s14-backbone-orange min-w-0 overflow-hidden">
              <div class="text-[10px] font-mono font-bold text-orange-200 text-center leading-tight flex-shrink-0">SqueezeNet</div>
              <div class="flex-1 flex flex-col justify-center gap-0.5 min-w-0 min-h-0">
                <div class="flex items-center justify-center gap-0.5">
                  <div class="px-1 py-0.5 rounded bg-orange-700/60 border border-orange-400/50 text-[7px] font-mono text-orange-100 s14-layer-1 flex-shrink-0">Conv1</div>
                  <div class="text-orange-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-orange-600/60 border border-orange-400/50 text-[7px] font-mono text-orange-100 s14-layer-2 flex-shrink-0">Fire3</div>
                  <div class="text-orange-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-orange-500/60 border border-orange-400/50 text-[7px] font-mono text-orange-100 s14-layer-3 flex-shrink-0">Fire6</div>
                </div>
                <div class="flex items-center justify-center gap-0.5">
                  <div class="text-orange-400/70 text-[8px] flex-shrink-0">↳</div>
                  <div class="px-1 py-0.5 rounded bg-orange-400/60 border border-orange-300/60 text-[7px] font-mono text-orange-50 s14-layer-4 flex-shrink-0">Fire9</div>
                  <div class="text-orange-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-yellow-400/70 border border-yellow-200 text-[7px] font-mono text-yellow-50 font-bold s14-layer-5 flex-shrink-0">Pool10</div>
                </div>
              </div>
              <div class="text-[8px] font-mono text-orange-200/80 text-center leading-tight flex-shrink-0">f<sub>sqz</sub> ∈ ℝ<sup>1 × 1000</sup></div>
            </div>
            <div class="border border-emerald-400/70 rounded bg-emerald-950/30 p-1 flex-1 min-h-0 flex flex-col s14-backbone-emerald min-w-0 overflow-hidden">
              <div class="text-[10px] font-mono font-bold text-emerald-200 text-center leading-tight flex-shrink-0">ShuffleNet</div>
              <div class="flex-1 flex flex-col justify-center gap-0.5 min-w-0 min-h-0">
                <div class="flex items-center justify-center gap-0.5">
                  <div class="px-1 py-0.5 rounded bg-emerald-700/60 border border-emerald-400/50 text-[7px] font-mono text-emerald-100 s14-layer-1 flex-shrink-0">Conv</div>
                  <div class="text-emerald-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[7px] font-mono text-emerald-100 s14-layer-2 flex-shrink-0">Stage2</div>
                  <div class="text-emerald-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-emerald-500/60 border border-emerald-400/50 text-[7px] font-mono text-emerald-100 s14-layer-3 flex-shrink-0">Stage3</div>
                </div>
                <div class="flex items-center justify-center gap-0.5">
                  <div class="text-emerald-400/70 text-[8px] flex-shrink-0">↳</div>
                  <div class="px-1 py-0.5 rounded bg-emerald-400/60 border border-emerald-300/60 text-[7px] font-mono text-emerald-50 s14-layer-4 flex-shrink-0">Stage4</div>
                  <div class="text-emerald-400 text-[8px] flex-shrink-0">›</div>
                  <div class="px-1 py-0.5 rounded bg-lime-400/70 border border-lime-200 text-[7px] font-mono text-lime-50 font-bold s14-layer-5 flex-shrink-0">GAP</div>
                </div>
              </div>
              <div class="text-[8px] font-mono text-emerald-200/80 text-center leading-tight flex-shrink-0">f<sub>shuf</sub> ∈ ℝ<sup>1 × 544</sup></div>
            </div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-yellow-400/60 rounded-md p-1.5 bg-yellow-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-yellow-500 border border-yellow-200 flex items-center justify-center text-[8px] font-bold text-black s14-badge">4</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-yellow-300 text-center mb-1 flex-shrink-0 pl-5">Activations + NL Duplication</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0">
            <div class="border border-orange-400/60 rounded bg-orange-950/30 p-1 flex-1 min-h-0 flex flex-col justify-center gap-0.5 s14-block-1">
              <div class="text-[10px] font-mono font-bold text-orange-200 text-center leading-tight">Block M1 = SqueezeNet</div>
              <div class="bg-orange-900/50 rounded px-1 py-0.5 text-center">
                <div class="text-[9px] font-mono text-orange-100 leading-tight">f<sub>sqz</sub> from Pool10</div>
              </div>
              <div class="text-[7.5px] font-mono text-orange-200/80 text-center leading-tight">[ f<sub>NL</sub> ⊕ f<sub>sqz</sub> ]</div>
            </div>
            <div class="text-[9px] font-mono text-yellow-300/80 text-center s14-dup-tag">⊕ NL Block Duplicated ⊕</div>
            <div class="border border-emerald-400/60 rounded bg-emerald-950/30 p-1 flex-1 min-h-0 flex flex-col justify-center gap-0.5 s14-block-2">
              <div class="text-[10px] font-mono font-bold text-emerald-200 text-center leading-tight">Block M2 = ShuffleNet</div>
              <div class="bg-emerald-900/50 rounded px-1 py-0.5 text-center">
                <div class="text-[9px] font-mono text-emerald-100 leading-tight">f<sub>shuf</sub> from GAP</div>
              </div>
              <div class="text-[7.5px] font-mono text-emerald-200/80 text-center leading-tight">[ f<sub>NL</sub> ⊕ f<sub>shuf</sub> ]</div>
            </div>
          </div>
          <div class="text-[8px] text-center text-yellow-200/70 mt-1 flex-shrink-0">GPU Forward · Per-Segment</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">5</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-fuchsia-300 text-center mb-1 flex-shrink-0 pl-5">Modality Vectors</div>
          <div class="flex-1 flex flex-col justify-between gap-1 min-h-0 pt-3">
            <div class="border border-cyan-400/70 rounded bg-cyan-950/30 px-2 py-1 s14-vec-eeg flex-[0.85] flex flex-col justify-center">
              <div class="flex items-baseline justify-between gap-2">
                <div class="text-[10px] font-mono font-bold text-cyan-200 whitespace-nowrap">EEG Features</div>
                <div class="text-[9px] font-mono text-cyan-300 font-bold whitespace-nowrap">[ 1 × 2104 ]</div>
              </div>
              <div class="text-[8.5px] font-mono text-cyan-100/90 text-center mt-1 leading-tight">[ f<sub>NL</sub><sup>EEG</sup> ⊕ f<sub>sqz</sub><sup>EEG</sup> ⊕ f<sub>shuf</sub><sup>EEG</sup> ]</div>
            </div>
            <div class="border border-pink-400/70 rounded bg-pink-950/30 px-2 py-1 s14-vec-gaze flex-1 flex flex-col justify-center">
              <div class="flex items-baseline justify-between gap-2">
                <div class="text-[9px] font-mono font-bold text-pink-200 whitespace-nowrap">Gaze Features</div>
                <div class="text-[8px] font-mono text-pink-300 font-bold whitespace-nowrap">[ 1 × N<sub>G</sub>+1544 ]</div>
              </div>
              <div class="text-[8px] font-mono text-pink-100/90 text-center mt-1 leading-tight">[ f<sub>NL</sub><sup>Gaze</sup> ⊕ f<sub>sqz</sub><sup>Gaze</sup> ⊕ f<sub>shuf</sub><sup>Gaze</sup> ]</div>
            </div>
            <div class="border border-violet-400/70 rounded bg-violet-950/30 px-2 py-1 s14-vec-fusion flex-1 flex flex-col justify-center">
              <div class="flex items-baseline justify-between gap-2">
                <div class="text-[10px] font-mono font-bold text-violet-200 whitespace-nowrap">EEG+Gaze Fusion</div>
                <div class="text-[9px] font-mono text-violet-300 font-bold whitespace-nowrap">Multimodal</div>
              </div>
              <div class="text-[8.5px] font-mono text-violet-100/90 text-center mt-1 leading-tight">[ EEG<sub>vec</sub> ⊕ Gaze<sub>vec</sub> ]</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1.55]">
      <div class="bg-gradient-to-r from-violet-500/20 via-violet-500/5 to-transparent px-2 py-0.5 border-b border-violet-400/30">
        <div class="text-[10px] font-mono font-bold text-violet-300">▸ Mathematical Description · STFT Power · CNN Dimensionality · NL Concatenation Rule</div>
      </div>
      <div class="p-2 grid grid-cols-[1fr_auto_1fr_auto_1.2fr] gap-1.5 items-stretch">
        <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s14-formula-1">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">A</div>
          <div class="text-[9px] uppercase font-mono font-bold text-violet-300 text-center tracking-wider pl-5">Step A</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">STFT Power Per Channel</div>
          <div class="text-center mt-1 text-[10.5px] text-violet-100 font-serif italic">S<sub>c</sub>(f, τ) = | Σ x<sub>c</sub>[n] · w[n−τ] · e<sup>−j2πfn/F<sub>s</sub></sup> |²</div>
          <div class="text-center mt-0.5 text-[9px] text-violet-200/70 font-mono">X<sub>STFT</sub> ∈ ℝ<sup>F·C × T × 3</sup></div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s14-formula-2">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">B</div>
          <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider pl-5">Step B</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">CNN Backbone Dim.</div>
          <div class="text-center mt-1 text-[10.5px] text-emerald-100 font-serif italic">f<sub>CNN</sub> = GAP( ℱ<sup>(L)</sup>(X<sub>STFT</sub>) )</div>
          <div class="text-center mt-0.5 text-[9px] text-emerald-200/70 font-mono">f<sub>sqz</sub> ∈ ℝ<sup>1×1000</sup> · f<sub>shuf</sub> ∈ ℝ<sup>1×544</sup></div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s14-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 relative s14-formula-3">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s14-badge">C</div>
          <div class="text-[9px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider pl-5">Step C</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">NL Concatenation Rule</div>
          <div class="text-center mt-1 text-[10.5px] text-fuchsia-100 font-serif italic">(EEG+Gaze)<sub>vec</sub> = [ f<sub>NL</sub><sup>EEG+Gaze</sup> ⊕ f<sub>sqz</sub><sup>EEG+Gaze</sup> ⊕ f<sub>NL</sub><sup>EEG+Gaze</sup> ⊕ f<sub>shuf</sub><sup>EEG+Gaze</sup> ]</div>
          <div class="text-center mt-0.5 text-[9px] text-fuchsia-200/70 font-mono">Dim = 2·N<sub>NL</sub> + N<sub>sqz</sub> + N<sub>shuf</sub> = <span class="text-fuchsia-300 font-bold">2104</span></div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>STFT Input</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>SqueezeNet</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>ShuffleNet</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>NL Duplication</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-sm"></div>Modality Vector</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-yellow-400"></div>Data Flow</div>
    </div>
  </div>
</div>

<style>
@keyframes s14SpecRow {
  0%, 100% { filter: brightness(1) saturate(1.2); }
  50% { filter: brightness(1.3) saturate(1.6); }
}
.s14-spec-row { animation: s14SpecRow 2s ease-in-out infinite; }
@keyframes s14DashMarch { to { stroke-dashoffset: -10; } }
.s14-dash { animation: s14DashMarch 0.6s linear infinite; }
@keyframes s14BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s14-badge { animation: s14BadgePulse 2s ease-in-out infinite; }
@keyframes s14RgbGlow {
  0%, 100% { box-shadow: 0 0 6px rgba(251,146,60,0.3); transform: scale(1); }
  50% { box-shadow: 0 0 18px rgba(251,146,60,0.7), 0 0 30px rgba(251,146,60,0.4); transform: scale(1.02); }
}
.s14-rgb-orange { animation: s14RgbGlow 2.4s ease-in-out infinite; }
@keyframes s14RgbGlowGreen {
  0%, 100% { box-shadow: 0 0 6px rgba(52,211,153,0.3); transform: scale(1); }
  50% { box-shadow: 0 0 18px rgba(52,211,153,0.7), 0 0 30px rgba(52,211,153,0.4); transform: scale(1.02); }
}
.s14-rgb-emerald { animation: s14RgbGlowGreen 2.4s ease-in-out infinite; animation-delay: -1.2s; }
@keyframes s14LayerActivate {
  0%, 80%, 100% { filter: brightness(1) saturate(1); transform: scale(1); }
  40%, 50% { filter: brightness(1.6) saturate(1.5); transform: scale(1.1); box-shadow: 0 0 8px currentColor; }
}
.s14-layer-1 { animation: s14LayerActivate 2.5s ease-in-out infinite; animation-delay: 0s; color: #fb923c; }
.s14-layer-2 { animation: s14LayerActivate 2.5s ease-in-out infinite; animation-delay: 0.3s; color: #fb923c; }
.s14-layer-3 { animation: s14LayerActivate 2.5s ease-in-out infinite; animation-delay: 0.6s; color: #fb923c; }
.s14-layer-4 { animation: s14LayerActivate 2.5s ease-in-out infinite; animation-delay: 0.9s; color: #fbbf24; }
.s14-layer-5 { animation: s14LayerActivate 2.5s ease-in-out infinite; animation-delay: 1.2s; color: #facc15; }
@keyframes s14BackboneGlow {
  0%, 100% { box-shadow: inset 0 0 8px rgba(251,146,60,0.1); }
  50% { box-shadow: inset 0 0 16px rgba(251,146,60,0.25), 0 0 12px rgba(251,146,60,0.4); }
}
.s14-backbone-orange { animation: s14BackboneGlow 3s ease-in-out infinite; }
@keyframes s14BackboneGlowGreen {
  0%, 100% { box-shadow: inset 0 0 8px rgba(52,211,153,0.1); }
  50% { box-shadow: inset 0 0 16px rgba(52,211,153,0.25), 0 0 12px rgba(52,211,153,0.4); }
}
.s14-backbone-emerald { animation: s14BackboneGlowGreen 3s ease-in-out infinite; animation-delay: -1.5s; }
@keyframes s14BlockGlow {
  0%, 100% { box-shadow: 0 0 6px rgba(251,146,60,0.2); border-color: rgba(251,146,60,0.6); }
  50% { box-shadow: 0 0 18px rgba(251,146,60,0.6), inset 0 0 10px rgba(251,146,60,0.2); border-color: #fb923c; }
}
.s14-block-1 { animation: s14BlockGlow 2.6s ease-in-out infinite; }
@keyframes s14BlockGlowGreen {
  0%, 100% { box-shadow: 0 0 6px rgba(52,211,153,0.2); border-color: rgba(52,211,153,0.6); }
  50% { box-shadow: 0 0 18px rgba(52,211,153,0.6), inset 0 0 10px rgba(52,211,153,0.2); border-color: #34d399; }
}
.s14-block-2 { animation: s14BlockGlowGreen 2.6s ease-in-out infinite; animation-delay: -1.3s; }
@keyframes s14DupTag {
  0%, 100% { opacity: 0.6; text-shadow: none; }
  50% { opacity: 1; text-shadow: 0 0 8px #fbbf24, 0 0 16px rgba(251,191,36,0.6); color: #fde047; }
}
.s14-dup-tag { animation: s14DupTag 1.8s ease-in-out infinite; }
@keyframes s14VecActivate {
  0%, 75%, 100% { box-shadow: inset 0 0 0 1px transparent; filter: brightness(1) saturate(1); transform: scale(1); }
  85%, 95% { box-shadow: 0 0 16px currentColor, 0 0 28px currentColor, inset 0 0 12px rgba(255,255,255,0.2); filter: brightness(1.6) saturate(1.5); transform: scale(1.03); }
}
.s14-vec-eeg { animation: s14VecActivate 3.6s ease-in-out infinite; animation-delay: 0s; color: #67e8f9; }
.s14-vec-gaze { animation: s14VecActivate 3.6s ease-in-out infinite; animation-delay: 1.2s; color: #f472b6; }
.s14-vec-fusion { animation: s14VecActivate 3.6s ease-in-out infinite; animation-delay: 2.4s; color: #c084fc; }
@keyframes s14FormulaActivate {
  0%, 80%, 100% { box-shadow: inset 0 0 0 1px transparent; filter: brightness(1) saturate(1); transform: scale(1); }
  88%, 92% { box-shadow: 0 0 20px currentColor, 0 0 35px currentColor, inset 0 0 16px rgba(255,255,255,0.25), inset 0 0 0 2px currentColor; filter: brightness(1.7) saturate(1.5); transform: scale(1.03); }
}
[class*="s14-formula-"] { animation: s14FormulaActivate 3s ease-in-out infinite; }
.s14-formula-1 { animation-delay: 0s; color: #c084fc; }
.s14-formula-2 { animation-delay: 1s; color: #34d399; }
.s14-formula-3 { animation-delay: 2s; color: #e879f9; }
@keyframes s14Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s14-pulse { animation: s14Pulse 1.6s ease-in-out infinite; }
@keyframes s14PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s14-pulse-strong { animation: s14PulseStrong 0.9s ease-in-out infinite; }
@keyframes s14BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s14-blink-text { animation: s14BlinkText 0.9s steps(2, end) infinite; }
@keyframes s14Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s14BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s14-bar-pulse-1, .s14-bar-pulse-2, .s14-bar-pulse-3 { animation: s14BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s14-bar-pulse-1 { color: #fb923c; animation-delay: 0s; }
.s14-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s14-bar-pulse-3 { color: #e879f9; animation-delay: -1.6s; }
@keyframes s14BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #a78bfa, 0 0 12px rgba(167,139,250,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #a78bfa; transform: scale(0.85); }
}
.s14-bar-dot { animation: s14BarDot 1.6s ease-in-out infinite; }
.s14-breathe-1 { animation: s14Breathe 8s ease-in-out infinite; }
.s14-breathe-2 { animation: s14Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s14-breathe-3 { animation: s14Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s14ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s14-scan-line { animation: s14ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s15-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s15-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s15-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-violet-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-violet-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-violet-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-violet-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-violet-300 to-transparent s15-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-violet-400 rounded-full s15-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-violet-400 font-mono">Slide 15 · Methodology</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Cross-Scene </span><span class="bg-gradient-to-r from-cyan-300 via-emerald-300 to-rose-300 bg-clip-text text-transparent">Classification Pipeline</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-cyan-400 rounded-full s15-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s15-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-rose-400 rounded-full s15-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-violet-400 rounded-full s15-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">SMOTE → MRMR → Cubic SVM → Best k★</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s15-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s15-blink-text">Live Pipeline</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex flex-col gap-1 min-h-0">
    <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Classification · Modality: EEG+Gaze (Fused) · For Each Split s ∈ { PVT→UGV, PVT→UAV } · Repeats r = 1..5</div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-cyan-400/70">Total = 2 × 241 × 5 = <span class="text-cyan-300 font-bold">2410 Fits</span></div>
      </div>
      <div class="p-2 grid grid-cols-[1.3fr_auto_1.5fr_auto_1.6fr_auto_1.6fr_auto_2fr_auto_1.9fr] gap-1 items-stretch flex-1 min-h-0">
        <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">1</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-violet-300 text-center mb-1 flex-shrink-0 pl-5">Input · Form NL+DL</div>
          <div class="flex-1 flex flex-col justify-center gap-1 min-h-0">
            <div class="border-2 border-yellow-400/80 rounded bg-gradient-to-br from-yellow-600/20 to-amber-900/20 px-1 py-1 text-center s15-input-box">
              <div class="text-[8.5px] font-bold text-yellow-200 leading-tight">EEG + Gaze</div>
              <div class="text-[7px] font-mono text-yellow-300/90 leading-tight">Feat Vector</div>
              <div class="text-[8px] font-mono text-yellow-100 font-bold leading-tight mt-0.5 whitespace-nowrap">[ 1 × D<sub>fused</sub> ]</div>
            </div>
            <div class="text-[7.5px] font-mono text-violet-200/80 text-center leading-tight">Fused Modality<br/>From NL + DL</div>
            <div class="border border-violet-400/40 rounded bg-violet-900/20 px-1 py-0.5 text-center">
              <div class="text-[7px] font-mono text-violet-200 leading-tight">Single Modality View</div>
            </div>
          </div>
          <div class="bg-yellow-500/20 border border-yellow-400/60 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0">
            <div class="text-[7.5px] font-mono font-bold text-yellow-200">EEG+Gaze (Fused)</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">2</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-cyan-300 text-center mb-1 flex-shrink-0 pl-5">Scenario Split</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0 justify-center">
            <div class="border border-cyan-400/60 rounded bg-cyan-900/20 p-1 s15-split-a">
              <div class="text-[8.5px] font-mono font-bold text-cyan-200 text-center leading-tight">Split A · PVT → UGV</div>
              <div class="flex gap-0.5 mt-0.5">
                <div class="flex-1 px-1 py-0.5 rounded bg-cyan-700/50 border border-cyan-400/40 text-[7px] font-mono text-cyan-100 text-center">Train: PVT</div>
                <div class="flex-1 px-1 py-0.5 rounded bg-orange-700/50 border border-orange-400/40 text-[7px] font-mono text-orange-100 text-center">Test: UGV</div>
              </div>
            </div>
            <div class="border border-cyan-400/60 rounded bg-cyan-900/20 p-1 s15-split-b">
              <div class="text-[8.5px] font-mono font-bold text-cyan-200 text-center leading-tight">Split B · PVT → UAV</div>
              <div class="flex gap-0.5 mt-0.5">
                <div class="flex-1 px-1 py-0.5 rounded bg-cyan-700/50 border border-cyan-400/40 text-[7px] font-mono text-cyan-100 text-center">Train: PVT</div>
                <div class="flex-1 px-1 py-0.5 rounded bg-orange-700/50 border border-orange-400/40 text-[7px] font-mono text-orange-100 text-center">Test: UAV</div>
              </div>
            </div>
            <div class="text-[7.5px] font-mono text-cyan-200/70 text-center leading-tight">Train/Test<br/>Scene-Disjoint</div>
          </div>
          <div class="bg-cyan-500/20 border border-cyan-400/60 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0">
            <div class="text-[8px] font-mono font-bold text-cyan-200">For Each s ∈ {A, B}</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-orange-400/60 rounded-md p-1.5 bg-orange-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-orange-500 border border-orange-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">3</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-orange-300 text-center mb-1 flex-shrink-0 pl-5">SMOTE Balance · Train Only</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0 justify-center">
            <div class="border border-orange-400/40 rounded bg-orange-950/40 p-1 s15-smote-before">
              <div class="text-[7px] font-mono font-bold text-orange-300/80 text-center leading-tight">Before · Imbalanced</div>
              <div class="flex items-end gap-0.5 mt-1 h-4 justify-center">
                <div class="w-3 bg-orange-400 rounded-sm" style="height:100%"></div>
                <div class="w-3 bg-orange-700 rounded-sm" style="height:25%"></div>
              </div>
            </div>
            <div class="text-[9px] text-orange-400 text-center font-bold s15-arrow-down leading-tight">↓ SMOTE k=5 NN</div>
            <div class="border border-emerald-400/60 rounded bg-emerald-950/30 p-1 s15-smote-after">
              <div class="text-[7px] font-mono font-bold text-emerald-300 text-center leading-tight">After · Balanced</div>
              <div class="flex items-end gap-0.5 mt-1 h-4 justify-center">
                <div class="w-3 bg-emerald-400 rounded-sm" style="height:100%"></div>
                <div class="w-3 bg-emerald-500 rounded-sm s15-synth-bar" style="height:100%"></div>
              </div>
              <div class="text-[6.5px] font-mono text-emerald-300/80 text-center leading-tight mt-0.5">+ Synthetic</div>
            </div>
            <div class="text-[7.5px] font-mono text-orange-100 text-center italic leading-tight whitespace-nowrap">x<sub>new</sub> = x<sub>i</sub> + λ(x<sub>nn</sub> − x<sub>i</sub>)</div>
          </div>
          <div class="bg-orange-500/20 border border-orange-400/60 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0">
            <div class="text-[8px] font-mono font-bold text-orange-200">Applied Per Split</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">4</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-fuchsia-300 text-center mb-1 flex-shrink-0 pl-5">MRMR Feature Sweep</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0 justify-center">
            <div class="text-[7.5px] font-mono font-bold text-fuchsia-200 text-center leading-tight">① Rank by MRMR Score</div>
            <div class="relative h-7 flex items-end justify-center gap-0.5">
              <div class="w-2 bg-fuchsia-400 rounded-sm s15-bar-1" style="height:100%"></div>
              <div class="w-2 bg-fuchsia-500 rounded-sm s15-bar-2" style="height:80%"></div>
              <div class="w-2 bg-fuchsia-500 rounded-sm s15-bar-3" style="height:62%"></div>
              <div class="w-2 bg-fuchsia-600 rounded-sm s15-bar-4" style="height:48%"></div>
              <div class="w-px h-full bg-yellow-400 s15-cut-line"></div>
              <div class="w-2 bg-fuchsia-700/60 rounded-sm" style="height:35%"></div>
              <div class="w-2 bg-fuchsia-800/50 rounded-sm" style="height:24%"></div>
              <div class="absolute right-2 top-0 text-[6px] font-mono text-yellow-300 font-bold">Top-k</div>
            </div>
            <div class="text-[7.5px] font-mono font-bold text-fuchsia-200 text-center leading-tight">② Keep Top-k%</div>
            <div class="text-[8px] font-mono text-fuchsia-100 text-center italic leading-tight">X̂ = X[ : , idx(1:k) ]</div>
            <div class="border border-yellow-400/60 rounded bg-yellow-950/30 px-1 py-0.5 text-center s15-sweep-box">
              <div class="text-[7.5px] font-mono font-bold text-yellow-200 leading-tight">k% ∈ [40, 100]</div>
              <div class="text-[7px] font-mono text-yellow-300/80 leading-tight">Step 0.25 ⇒ <span class="text-yellow-300 font-bold">241 Pts</span></div>
            </div>
          </div>
          <div class="bg-fuchsia-500/20 border border-fuchsia-400/60 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0">
            <div class="text-[8px] font-mono font-bold text-fuchsia-200">For Each k% (241)</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">5</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-emerald-300 text-center mb-1 flex-shrink-0 pl-5">Cubic SVM Trainer</div>
          <div class="flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
            <div class="border border-emerald-400/60 rounded bg-emerald-900/20 px-1 py-1.5 s15-svm-train">
              <div class="text-[8px] font-mono font-bold text-emerald-200 text-center leading-tight">Polynomial Kernel · Order 3</div>
              <div class="text-[7px] font-mono text-emerald-100 text-center italic leading-snug mt-1 whitespace-nowrap">K(x, x') = (γ x<sup>T</sup>x' + r)<sup>3</sup></div>
              <div class="text-[7px] font-mono text-emerald-100 text-center italic leading-snug mt-0.5 whitespace-nowrap">f(x) = Σ α<sub>i</sub>y<sub>i</sub>K(x<sub>i</sub>, x) + b</div>
            </div>
            <div class="flex items-center justify-center gap-1">
              <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[6.5px] font-mono text-emerald-50 s15-seed-1">S1</div>
              <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[6.5px] font-mono text-emerald-50 s15-seed-2">S2</div>
              <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[6.5px] font-mono text-emerald-50 s15-seed-3">S3</div>
              <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[6.5px] font-mono text-emerald-50 s15-seed-4">S4</div>
              <div class="px-1 py-0.5 rounded bg-emerald-600/60 border border-emerald-400/50 text-[6.5px] font-mono text-emerald-50 s15-seed-5">S5</div>
            </div>
            <div class="border border-emerald-400/40 rounded bg-emerald-950/40 px-1 py-1 text-center">
              <div class="text-[7px] font-mono text-emerald-200 leading-snug whitespace-nowrap">ŷ = sign(f(X<sub>test</sub>))</div>
              <div class="text-[6px] font-mono text-emerald-300/80 leading-snug mt-0.5 whitespace-nowrap tracking-tight">ACC·MCC·AUC·F1·P·R</div>
            </div>
          </div>
          <div class="bg-emerald-500/20 border border-emerald-400/60 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0">
            <div class="text-[8px] font-mono font-bold text-emerald-200">For Each r = 1..5</div>
          </div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 30 12" class="w-7 h-3"><path d="M0 6 L22 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M20 2 L26 6 L20 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-rose-400/60 rounded-md p-1.5 bg-rose-950/20 flex flex-col min-h-0 overflow-hidden relative">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">6</div>
          <div class="text-[9px] uppercase tracking-wider font-mono font-bold text-rose-300 text-center mb-1 flex-shrink-0 pl-5">Best k★ + Avg → Best Config</div>
          <div class="flex-1 flex flex-col gap-1 min-h-0 justify-center">
            <div class="border border-rose-400/60 rounded bg-rose-950/30 px-1 py-2 relative">
              <svg viewBox="0 0 100 30" class="w-full h-12" preserveAspectRatio="none">
                <path d="M5,28 Q15,24 25,18 T50,8 T75,12 T95,22" stroke="#fb7185" stroke-width="0.8" fill="none" class="s15-acc-curve"/>
                <circle cx="50" cy="8" r="1.6" fill="#fbbf24" class="s15-peak"/>
                <text x="54" y="9" font-size="3" font-family="monospace" fill="#fde047" font-weight="bold">k★</text>
                <text x="2" y="10" font-size="2.8" font-family="monospace" fill="#fb7185">Acc</text>
                <text x="88" y="29" font-size="2.8" font-family="monospace" fill="#fb7185">k%</text>
              </svg>
            </div>
            <div class="text-[8px] font-mono text-rose-100 text-center italic leading-tight">k★ = argmax<sub>k</sub> acc<sub>r</sub>(k)</div>
            <div class="border border-rose-400/40 rounded bg-rose-950/30 px-1 py-0.5 text-center">
              <div class="text-[7.5px] font-mono font-bold text-rose-200 leading-tight">Avg 5 Repeats</div>
              <div class="text-[7.5px] font-mono text-rose-100 italic leading-tight">μ<sub>s</sub> = (1/5)Σ<sub>r</sub> metric<sub>s,r</sub></div>
            </div>
            <div class="border border-rose-400/40 rounded bg-rose-950/30 px-1 py-0.5 text-center">
              <div class="text-[7.5px] font-mono font-bold text-rose-200 leading-tight">Avg 2 Splits</div>
              <div class="text-[7.5px] font-mono text-rose-100 italic leading-tight">μ̄ = ½(μ<sub>A</sub> + μ<sub>B</sub>)</div>
            </div>
          </div>
          <div class="bg-rose-500/20 border-2 border-rose-400 rounded px-1 py-0.5 mt-1 text-center flex-shrink-0 s15-best-config">
            <div class="text-[9px] font-mono font-bold text-rose-100">★ Best Config</div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1.55]">
      <div class="bg-gradient-to-r from-violet-500/20 via-violet-500/5 to-transparent px-2 py-0.5 border-b border-violet-400/30">
        <div class="text-[10px] font-mono font-bold text-violet-300">▸ Mathematical Description · MRMR · Cubic SVM Kernel · Binary Decision · Scenario-Averaged Metric</div>
      </div>
      <div class="p-2 grid grid-cols-[1.2fr_auto_1fr_auto_1fr_auto_1fr] gap-1.5 items-stretch">
        <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 relative s15-formula-1">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">A</div>
          <div class="text-[9px] uppercase font-mono font-bold text-fuchsia-300 text-center tracking-wider pl-5">Step A</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">MRMR · Min Redundancy</div>
          <div class="text-center mt-1 text-[9.5px] text-fuchsia-100 font-serif italic leading-tight">V<sub>j</sub> = I(x<sub>j</sub>; y) · W<sub>j</sub> = (1/|S|) Σ<sub>k∈S</sub> I(x<sub>j</sub>; x<sub>k</sub>)</div>
          <div class="text-center mt-0.5 text-[9.5px] text-fuchsia-100 font-serif italic leading-tight">score<sub>j</sub> = V<sub>j</sub> − W<sub>j</sub> (MID)</div>
          <div class="text-center mt-0.5 text-[8.5px] text-fuchsia-200/70 font-mono">Rank ↓ score<sub>j</sub> ⇒ Top-k%</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s15-formula-2">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">B</div>
          <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 text-center tracking-wider pl-5">Step B</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">Cubic SVM · Poly Kernel</div>
          <div class="text-center mt-1 text-[10px] text-emerald-100 font-serif italic">K(x, x') = (γ · x<sup>T</sup>x' + r)<sup>3</sup></div>
          <div class="text-center mt-0.5 text-[10px] text-emerald-100 font-serif italic">f(x) = Σ α<sub>i</sub>y<sub>i</sub>K(x<sub>i</sub>, x) + b</div>
          <div class="text-center mt-0.5 text-[8.5px] text-emerald-200/70 font-mono">Degree 3 · Binary</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-yellow-400/60 rounded-md p-1.5 bg-yellow-950/20 relative s15-formula-3">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-yellow-500 border border-yellow-200 flex items-center justify-center text-[8px] font-bold text-black s15-badge">C</div>
          <div class="text-[9px] uppercase font-mono font-bold text-yellow-300 text-center tracking-wider pl-5">Step C</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">Binary Decision</div>
          <div class="text-center mt-1 text-[10px] text-yellow-100 font-serif italic">ŷ(x) = sign(f(x))</div>
          <div class="text-center mt-0.5 text-[10px] text-yellow-100 font-serif italic">∈ { Alert, Unguarded }</div>
          <div class="text-center mt-0.5 text-[8.5px] text-yellow-200/70 font-mono">C=2 · Hinge Loss</div>
        </div>
        <div class="flex items-center"><svg viewBox="0 0 24 12" class="w-6 h-3"><path d="M0 6 L18 6" stroke="#facc15" stroke-width="1.5" stroke-dasharray="3 2" class="s15-dash"/><path d="M16 2 L22 6 L16 10" stroke="#facc15" stroke-width="1.5" fill="none" stroke-linecap="round"/></svg></div>
        <div class="border border-rose-400/60 rounded-md p-1.5 bg-rose-950/20 relative s15-formula-4">
          <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[8px] font-bold text-white s15-badge">D</div>
          <div class="text-[9px] uppercase font-mono font-bold text-rose-300 text-center tracking-wider pl-5">Step D</div>
          <div class="text-[11px] font-bold text-white text-center mt-0.5">Scenario-Averaged</div>
          <div class="text-center mt-1 text-[10px] text-rose-100 font-serif italic">μ<sub>s</sub> = (1/5) Σ<sub>r</sub> metric<sub>s,r</sub>(k★<sub>r</sub>)</div>
          <div class="text-center mt-0.5 text-[10px] text-rose-100 font-serif italic">μ̄ = ½(μ<sub>A</sub> + μ<sub>B</sub>)</div>
          <div class="text-center mt-0.5 text-[8.5px] text-rose-200/70 font-mono">A: PVT→UGV · B: PVT→UAV</div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Input Vector</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Scene Split</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>SMOTE</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-fuchsia-400 rounded-sm"></div>MRMR</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Cubic SVM</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Best Config</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px bg-yellow-400"></div>Data Flow</div>
    </div>
  </div>
</div>

<style>
@keyframes s15DashMarch { to { stroke-dashoffset: -10; } }
.s15-dash { animation: s15DashMarch 0.6s linear infinite; }
@keyframes s15BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s15-badge { animation: s15BadgePulse 2s ease-in-out infinite; }
@keyframes s15InputBox {
  0%, 100% { box-shadow: 0 0 6px rgba(250,204,21,0.3); transform: scale(1); }
  50% { box-shadow: 0 0 18px rgba(250,204,21,0.7), 0 0 30px rgba(250,204,21,0.4); transform: scale(1.02); }
}
.s15-input-box { animation: s15InputBox 2.4s ease-in-out infinite; }
@keyframes s15SplitGlow {
  0%, 100% { box-shadow: inset 0 0 4px rgba(34,211,238,0.1); border-color: rgba(34,211,238,0.6); }
  50% { box-shadow: 0 0 14px rgba(34,211,238,0.5), inset 0 0 8px rgba(34,211,238,0.2); border-color: #22d3ee; }
}
.s15-split-a { animation: s15SplitGlow 2.4s ease-in-out infinite; }
.s15-split-b { animation: s15SplitGlow 2.4s ease-in-out infinite; animation-delay: -1.2s; }
@keyframes s15SmoteBefore {
  0%, 100% { filter: brightness(1) saturate(1); }
  50% { filter: brightness(0.7) saturate(0.8); }
}
.s15-smote-before { animation: s15SmoteBefore 2.5s ease-in-out infinite; }
@keyframes s15SmoteAfter {
  0%, 100% { box-shadow: 0 0 4px rgba(52,211,153,0.3); }
  50% { box-shadow: 0 0 14px rgba(52,211,153,0.7), inset 0 0 8px rgba(52,211,153,0.2); }
}
.s15-smote-after { animation: s15SmoteAfter 2.5s ease-in-out infinite; animation-delay: -1.25s; }
@keyframes s15SynthBar {
  0%, 100% { background-color: #10b981; box-shadow: 0 0 4px #10b981; }
  50% { background-color: #34d399; box-shadow: 0 0 10px #34d399; }
}
.s15-synth-bar { animation: s15SynthBar 1.8s ease-in-out infinite; }
@keyframes s15ArrowDown {
  0%, 100% { opacity: 0.5; transform: translateY(0); }
  50% { opacity: 1; transform: translateY(2px); text-shadow: 0 0 8px #fb923c; }
}
.s15-arrow-down { animation: s15ArrowDown 1.8s ease-in-out infinite; }
@keyframes s15Bar {
  0%, 100% { filter: brightness(1); transform: scaleY(1); transform-origin: bottom; }
  50% { filter: brightness(1.6); transform: scaleY(1.08); }
}
.s15-bar-1 { animation: s15Bar 1.8s ease-in-out infinite; animation-delay: 0s; }
.s15-bar-2 { animation: s15Bar 1.8s ease-in-out infinite; animation-delay: 0.18s; }
.s15-bar-3 { animation: s15Bar 1.8s ease-in-out infinite; animation-delay: 0.36s; }
.s15-bar-4 { animation: s15Bar 1.8s ease-in-out infinite; animation-delay: 0.54s; }
@keyframes s15CutLine {
  0%, 100% { box-shadow: 0 0 3px #facc15; opacity: 0.7; }
  50% { box-shadow: 0 0 10px #facc15, 0 0 18px rgba(250,204,21,0.6); opacity: 1; }
}
.s15-cut-line { animation: s15CutLine 1.6s ease-in-out infinite; }
@keyframes s15SweepBox {
  0%, 100% { box-shadow: 0 0 4px rgba(250,204,21,0.3); }
  50% { box-shadow: 0 0 14px rgba(250,204,21,0.7), inset 0 0 8px rgba(250,204,21,0.2); }
}
.s15-sweep-box { animation: s15SweepBox 2.4s ease-in-out infinite; }
@keyframes s15SvmTrain {
  0%, 100% { box-shadow: inset 0 0 4px rgba(52,211,153,0.1); border-color: rgba(52,211,153,0.6); }
  50% { box-shadow: 0 0 14px rgba(52,211,153,0.5), inset 0 0 8px rgba(52,211,153,0.2); border-color: #34d399; }
}
.s15-svm-train { animation: s15SvmTrain 2.4s ease-in-out infinite; }
@keyframes s15Seed {
  0%, 80%, 100% { filter: brightness(1) saturate(1); transform: scale(1); }
  40%, 50% { filter: brightness(1.6) saturate(1.5); transform: scale(1.15); box-shadow: 0 0 10px #34d399; }
}
.s15-seed-1 { animation: s15Seed 2.5s ease-in-out infinite; animation-delay: 0s; }
.s15-seed-2 { animation: s15Seed 2.5s ease-in-out infinite; animation-delay: 0.25s; }
.s15-seed-3 { animation: s15Seed 2.5s ease-in-out infinite; animation-delay: 0.5s; }
.s15-seed-4 { animation: s15Seed 2.5s ease-in-out infinite; animation-delay: 0.75s; }
.s15-seed-5 { animation: s15Seed 2.5s ease-in-out infinite; animation-delay: 1s; }
@keyframes s15AccCurve {
  0%, 100% { stroke-width: 0.8; }
  50% { stroke-width: 1; }
}
.s15-acc-curve { animation: s15AccCurve 2s ease-in-out infinite; }
@keyframes s15Peak {
  0%, 100% { r: 1.4; }
  50% { r: 1.8; }
}
.s15-peak { animation: s15Peak 1.6s ease-in-out infinite; }
@keyframes s15BestConfig {
  0%, 100% { box-shadow: 0 0 6px rgba(251,113,133,0.4), inset 0 0 4px rgba(251,113,133,0.2); transform: scale(1); }
  50% { box-shadow: 0 0 22px rgba(251,113,133,0.9), 0 0 40px rgba(251,113,133,0.5), inset 0 0 12px rgba(251,113,133,0.3); transform: scale(1.04); }
}
.s15-best-config { animation: s15BestConfig 2.2s ease-in-out infinite; }
@keyframes s15FormulaActivate {
  0%, 80%, 100% { box-shadow: inset 0 0 0 1px transparent; filter: brightness(1) saturate(1); transform: scale(1); }
  88%, 92% { box-shadow: 0 0 20px currentColor, 0 0 35px currentColor, inset 0 0 16px rgba(255,255,255,0.25), inset 0 0 0 2px currentColor; filter: brightness(1.7) saturate(1.5); transform: scale(1.03); }
}
[class*="s15-formula-"] { animation: s15FormulaActivate 3.2s ease-in-out infinite; }
.s15-formula-1 { animation-delay: 0s; color: #e879f9; }
.s15-formula-2 { animation-delay: 0.8s; color: #34d399; }
.s15-formula-3 { animation-delay: 1.6s; color: #facc15; }
.s15-formula-4 { animation-delay: 2.4s; color: #fb7185; }
@keyframes s15Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s15-pulse { animation: s15Pulse 1.6s ease-in-out infinite; }
@keyframes s15PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s15-pulse-strong { animation: s15PulseStrong 0.9s ease-in-out infinite; }
@keyframes s15BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s15-blink-text { animation: s15BlinkText 0.9s steps(2, end) infinite; }
@keyframes s15Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s15BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s15-bar-pulse-1, .s15-bar-pulse-2, .s15-bar-pulse-3 { animation: s15BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s15-bar-pulse-1 { color: #22d3ee; animation-delay: 0s; }
.s15-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s15-bar-pulse-3 { color: #fb7185; animation-delay: -1.6s; }
@keyframes s15BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #a78bfa, 0 0 12px rgba(167,139,250,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #a78bfa; transform: scale(0.85); }
}
.s15-bar-dot { animation: s15BarDot 1.6s ease-in-out infinite; }
.s15-breathe-1 { animation: s15Breathe 8s ease-in-out infinite; }
.s15-breathe-2 { animation: s15Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s15-breathe-3 { animation: s15Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s15ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s15-scan-line { animation: s15ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-20%] left-[20%] w-[800px] h-[800px] bg-emerald-500/15 rounded-full blur-[160px] s16-breathe"></div>
  <div class="absolute bottom-[-20%] right-[10%] w-[700px] h-[700px] bg-teal-500/12 rounded-full blur-[160px] s16-breathe-2"></div>
</div>
<div class="absolute inset-0 opacity-[0.18] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s16-eeg" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q150,420 300,450 T600,450 Q750,380 900,450 T1200,450 Q1350,500 1500,450 T1800,450 Q1950,400 2100,450 T2400,450 Q2550,500 2700,450 T3000,450 L3200,450" fill="none" stroke="#34d399" stroke-width="0.8"/>
  </svg>
</div>
<div class="absolute inset-0 opacity-[0.12] pointer-events-none overflow-hidden">
  <svg class="w-[200%] h-full s16-eeg-2" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,250 Q80,250 130,230 T230,250 Q280,150 330,250 T430,250 Q480,310 530,250 T630,250 Q680,190 730,250 T830,250 Q880,270 930,250 T1030,250 Q1080,220 1130,250 T1230,250 Q1280,150 1330,250 T1430,250 Q1480,310 1530,250 T1630,250 L3200,250" fill="none" stroke="#6ee7b7" stroke-width="1"/>
    <path d="M0,650 Q100,650 160,630 T260,650 Q310,710 360,650 T460,650 Q510,590 560,650 T660,650 Q710,670 760,650 T860,650 L3200,650" fill="none" stroke="#a3e635" stroke-width="1"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[15%] left-[10%] w-1 h-1 bg-emerald-400 rounded-full s16-particle-1"></div>
  <div class="absolute top-[25%] left-[85%] w-1.5 h-1.5 bg-teal-300 rounded-full s16-particle-2"></div>
  <div class="absolute top-[75%] left-[12%] w-1 h-1 bg-emerald-400 rounded-full s16-particle-3"></div>
  <div class="absolute top-[80%] left-[88%] w-1.5 h-1.5 bg-teal-400 rounded-full s16-particle-1"></div>
  <div class="absolute top-[40%] left-[5%] w-1 h-1 bg-emerald-300 rounded-full s16-particle-2"></div>
  <div class="absolute top-[55%] left-[92%] w-1 h-1 bg-teal-300 rounded-full s16-particle-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-60"></div>
<div class="absolute top-6 left-6 w-8 h-8 border-l-2 border-t-2 border-emerald-400 opacity-60 s16-bracket-1"></div>
<div class="absolute top-6 right-6 w-8 h-8 border-r-2 border-t-2 border-emerald-400 opacity-60 s16-bracket-1"></div>
<div class="absolute bottom-6 left-6 w-8 h-8 border-l-2 border-b-2 border-emerald-400 opacity-60 s16-bracket-2"></div>
<div class="absolute bottom-6 right-6 w-8 h-8 border-r-2 border-b-2 border-emerald-400 opacity-60 s16-bracket-2"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-15">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s16-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col">
  <div class="flex items-center justify-between px-16 py-4 s16-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s16-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Section Transition</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex-1 flex items-center justify-center px-16">
    <div class="relative w-full max-w-5xl">
      <div class="relative flex items-center justify-center mb-3 s16-number-wrap">
        <div class="absolute w-[180px] h-[180px] rounded-full bg-emerald-500/10 blur-3xl s16-aura"></div>
        <div class="absolute w-[120px] h-[120px] rounded-full border border-emerald-400/20 s16-ring-1"></div>
        <div class="absolute w-[155px] h-[155px] rounded-full border border-emerald-400/15 s16-ring-2"></div>
        <div class="absolute w-[190px] h-[190px] rounded-full border border-emerald-400/10 s16-ring-3"></div>
        <div class="relative z-10 flex items-baseline gap-1">
          <span class="text-[5.5rem] font-black leading-none tracking-tighter bg-gradient-to-b from-emerald-300 via-teal-400 to-emerald-700 bg-clip-text text-transparent s16-number-glow">03</span>
          <span class="text-[1.1rem] font-light text-slate-600 font-mono tracking-wider">/ 04</span>
        </div>
      </div>
      <div class="text-center s16-label-wrap">
        <div class="flex items-center justify-center gap-4 mb-2">
          <div class="h-px w-12 bg-gradient-to-r from-transparent to-emerald-400"></div>
          <div class="text-[10px] uppercase tracking-[0.5em] text-emerald-400 font-mono">Section Three</div>
          <div class="h-px w-12 bg-gradient-to-l from-transparent to-emerald-400"></div>
        </div>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight s16-title">
          <span class="bg-gradient-to-r from-white via-emerald-100 to-white bg-clip-text text-transparent">EXPERIMENTAL</span>
        </h1>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight mt-1 s16-title-2">
          <span class="bg-gradient-to-r from-emerald-300 via-teal-300 to-emerald-300 bg-clip-text text-transparent">RESULTS</span>
        </h1>
        <div class="mt-4 max-w-2xl mx-auto s16-subtitle">
          <p class="!text-xs !text-slate-400 !m-0 font-light tracking-wide leading-relaxed">
            Cross-scenario classification benchmarks · MRMR sweep performance · Modality fusion gains
          </p>
        </div>
      </div>
      <div class="flex items-center justify-center gap-2 mt-4 s16-dots">
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-8 h-[2px] bg-emerald-400 rounded-full"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between px-16 py-4 s16-fade-in-last">
    <div class="flex items-center gap-3">
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Paper 01 · Proposal</div>
    </div>
    <div class="flex items-center gap-3">
      <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s16-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Entering Section</div>
    </div>
  </div>
</div>

<style>
@keyframes s16Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.1); } }
.s16-breathe { animation: s16Breathe 10s ease-in-out infinite; }
.s16-breathe-2 { animation: s16Breathe 12s ease-in-out infinite; animation-delay: -5s; }
@keyframes s16EegFlow { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.s16-eeg { animation: s16EegFlow 30s linear infinite; }
.s16-eeg-2 { animation: s16EegFlow 22s linear infinite; }
@keyframes s16Particle1 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-12px, -10px); opacity: 1; } }
@keyframes s16Particle2 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(10px, -12px); opacity: 1; } }
@keyframes s16Particle3 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-8px, 12px); opacity: 1; } }
.s16-particle-1 { animation: s16Particle1 5s ease-in-out infinite; }
.s16-particle-2 { animation: s16Particle2 6s ease-in-out infinite; animation-delay: -1.5s; }
.s16-particle-3 { animation: s16Particle3 5.5s ease-in-out infinite; animation-delay: -2.5s; }
@keyframes s16StrongPulse { 0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor; } 50% { opacity: 0.5; box-shadow: 0 0 14px currentColor; } }
.s16-strong-pulse { animation: s16StrongPulse 1.8s ease-in-out infinite; }
@keyframes s16ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s16-scan-line { animation: s16ScanLine 5s linear infinite; }
@keyframes s16BracketPulse1 { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.08); } }
.s16-bracket-1 { animation: s16BracketPulse1 4s ease-in-out infinite; transform-origin: top left; }
.s16-bracket-2 { animation: s16BracketPulse1 4s ease-in-out infinite; animation-delay: -2s; transform-origin: bottom right; }
@keyframes s16Aura { 0%, 100% { opacity: 0.6; transform: scale(1); } 50% { opacity: 1; transform: scale(1.15); } }
.s16-aura { animation: s16Aura 4s ease-in-out infinite; }
@keyframes s16RingRotate1 { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
@keyframes s16RingRotate2 { from { transform: rotate(0deg); } to { transform: rotate(-360deg); } }
@keyframes s16RingPulse { 0%, 100% { opacity: 0.4; } 50% { opacity: 0.9; } }
.s16-ring-1 { animation: s16RingRotate1 40s linear infinite, s16RingPulse 3s ease-in-out infinite; }
.s16-ring-2 { animation: s16RingRotate2 60s linear infinite, s16RingPulse 3s ease-in-out infinite; animation-delay: -1s; }
.s16-ring-3 { animation: s16RingRotate1 80s linear infinite, s16RingPulse 3s ease-in-out infinite; animation-delay: -2s; }
@keyframes s16NumberGlow {
  0%, 100% { filter: drop-shadow(0 0 20px rgba(52, 211, 153, 0.4)) drop-shadow(0 0 40px rgba(20, 184, 166, 0.2)); }
  50% { filter: drop-shadow(0 0 30px rgba(110, 231, 183, 0.6)) drop-shadow(0 0 60px rgba(52, 211, 153, 0.3)); }
}
.s16-number-glow { animation: s16NumberGlow 3s ease-in-out infinite; }
@keyframes s16NumberIn {
  from { opacity: 0; transform: scale(0.6); filter: blur(20px); }
  to { opacity: 1; transform: scale(1); filter: blur(0); }
}
.s16-number-wrap { animation: s16NumberIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) 0.3s both; }
@keyframes s16FadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
.s16-label-wrap { animation: s16FadeUp 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.0s both; }
@keyframes s16TitleIn {
  from { opacity: 0; transform: translateY(20px); letter-spacing: 0.5em; filter: blur(8px); }
  to { opacity: 1; transform: translateY(0); letter-spacing: -0.025em; filter: blur(0); }
}
.s16-title { animation: s16TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.2s both; }
.s16-title-2 { animation: s16TitleIn 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.5s both; }
@keyframes s16SubIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
.s16-subtitle { animation: s16SubIn 0.8s ease-out 2.0s both; }
.s16-dots { animation: s16SubIn 0.8s ease-out 2.3s both; }
@keyframes s16FadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
.s16-fade-in { animation: s16FadeIn 0.8s ease-out both; }
.s16-fade-in-last { animation: s16FadeIn 0.8s ease-out 2.5s both; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s17-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s17-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-teal-500/8 rounded-full blur-[140px] s17-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s17-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s17-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 17 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Class </span><span class="bg-gradient-to-r from-emerald-300 via-teal-300 to-rose-300 bg-clip-text text-transparent">Distribution</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-emerald-400 rounded-full s17-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-teal-400 rounded-full s17-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-rose-400 rounded-full s17-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s17-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Alert vs Unguarded · 100 Trials Per Scenario</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s17-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s17-blink-text">Live Data</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[2.4] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Distribution of Alert vs Unguarded Trials Across Scenarios</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">PVT · UAV · UGV</div>
      </div>
      <div class="flex-1 p-3 min-h-0 flex flex-col">
        <div class="text-[10px] font-bold text-white text-center mb-1 flex-shrink-0">Distribution of Alert vs Unguarded Trials Across Scenarios</div>
        <div class="flex-1 flex min-h-0">
          <div class="flex flex-col justify-between text-[8px] font-mono text-slate-400 pr-1 py-1" style="writing-mode: horizontal-tb;">
            <div class="text-right w-6">90</div>
            <div class="text-right w-6">80</div>
            <div class="text-right w-6">70</div>
            <div class="text-right w-6">60</div>
            <div class="text-right w-6">50</div>
            <div class="text-right w-6">40</div>
            <div class="text-right w-6">30</div>
            <div class="text-right w-6">20</div>
            <div class="text-right w-6">10</div>
            <div class="text-right w-6">0</div>
          </div>
          <div class="flex-1 flex flex-col min-h-0 relative">
            <div class="absolute inset-0 flex flex-col justify-between pointer-events-none">
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
              <div class="border-t border-slate-700/40"></div>
            </div>
            <div class="flex-1 flex items-end justify-around pb-0 px-2 relative z-10">
              <div class="flex items-end gap-2 h-full" style="width: 28%;">
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-emerald-200 leading-tight">82</div>
                  <div class="text-[8px] font-mono text-emerald-300 leading-tight">(82.0%)</div>
                  <div class="w-full bg-gradient-to-t from-emerald-600 to-emerald-400 rounded-t-sm s17-bar-pvt-alert" style="height: 91%;"></div>
                </div>
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-rose-300 leading-tight">18</div>
                  <div class="text-[8px] font-mono text-transparent leading-tight">(0.0%)</div>
                  <div class="w-full bg-gradient-to-t from-rose-600 to-rose-400 rounded-t-sm s17-bar-pvt-unguarded" style="height: 20%;"></div>
                </div>
              </div>
              <div class="flex items-end gap-2 h-full" style="width: 28%;">
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-emerald-200 leading-tight">76</div>
                  <div class="text-[8px] font-mono text-emerald-300 leading-tight">(76.0%)</div>
                  <div class="w-full bg-gradient-to-t from-emerald-600 to-emerald-400 rounded-t-sm s17-bar-uav-alert" style="height: 84%;"></div>
                </div>
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-rose-300 leading-tight">24</div>
                  <div class="text-[8px] font-mono text-transparent leading-tight">(0.0%)</div>
                  <div class="w-full bg-gradient-to-t from-rose-600 to-rose-400 rounded-t-sm s17-bar-uav-unguarded" style="height: 27%;"></div>
                </div>
              </div>
              <div class="flex items-end gap-2 h-full" style="width: 28%;">
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-emerald-200 leading-tight">59</div>
                  <div class="text-[8px] font-mono text-emerald-300 leading-tight">(59.0%)</div>
                  <div class="w-full bg-gradient-to-t from-emerald-600 to-emerald-400 rounded-t-sm s17-bar-ugv-alert" style="height: 65%;"></div>
                </div>
                <div class="flex-1 flex flex-col items-center justify-end h-full">
                  <div class="text-[10px] font-bold text-rose-300 leading-tight">41</div>
                  <div class="text-[8px] font-mono text-transparent leading-tight">(0.0%)</div>
                  <div class="w-full bg-gradient-to-t from-rose-600 to-rose-400 rounded-t-sm s17-bar-ugv-unguarded" style="height: 45%;"></div>
                </div>
              </div>
            </div>
            <div class="border-t-2 border-slate-500 flex-shrink-0"></div>
            <div class="flex justify-around mt-1 px-2">
              <div class="text-[10px] font-mono font-bold text-white" style="width: 28%; text-align: center;">PVT</div>
              <div class="text-[10px] font-mono font-bold text-white" style="width: 28%; text-align: center;">UAV</div>
              <div class="text-[10px] font-mono font-bold text-white" style="width: 28%; text-align: center;">UGV</div>
            </div>
          </div>
        </div>
        <div class="flex items-center justify-center gap-4 mt-2 flex-shrink-0">
          <div class="flex items-center gap-1.5">
            <div class="w-3 h-3 bg-emerald-400 rounded-sm"></div>
            <div class="text-[9px] font-mono text-slate-300">Alert (High Vigilance)</div>
          </div>
          <div class="flex items-center gap-1.5">
            <div class="w-3 h-3 bg-rose-400 rounded-sm"></div>
            <div class="text-[9px] font-mono text-slate-300">Unguarded (Low Vigilance)</div>
          </div>
        </div>
        <div class="text-center mt-1 text-[8px] font-mono text-slate-500 italic flex-shrink-0">Number of Trials</div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.3] min-h-0">
      <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Per-Scenario Summary</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 s17-summary-row">
            <div class="flex items-center justify-between mb-1">
              <div class="text-[10px] font-mono font-bold text-violet-200">PVT</div>
              <div class="text-[8px] font-mono text-violet-300/80">Lab Baseline</div>
            </div>
            <div class="flex h-3 rounded overflow-hidden">
              <div class="bg-emerald-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 82%;">82</div>
              <div class="bg-rose-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 18%;">18</div>
            </div>
            <div class="flex justify-between mt-0.5 text-[7px] font-mono">
              <span class="text-emerald-300">Alert 82%</span>
              <span class="text-rose-300">Unguarded 18%</span>
            </div>
          </div>
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 s17-summary-row">
            <div class="flex items-center justify-between mb-1">
              <div class="text-[10px] font-mono font-bold text-cyan-200">UAV</div>
              <div class="text-[8px] font-mono text-cyan-300/80">Sea Survivor Search</div>
            </div>
            <div class="flex h-3 rounded overflow-hidden">
              <div class="bg-emerald-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 76%;">76</div>
              <div class="bg-rose-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 24%;">24</div>
            </div>
            <div class="flex justify-between mt-0.5 text-[7px] font-mono">
              <span class="text-emerald-300">Alert 76%</span>
              <span class="text-rose-300">Unguarded 24%</span>
            </div>
          </div>
          <div class="border border-orange-400/60 rounded-md p-1.5 bg-orange-950/20 s17-summary-row">
            <div class="flex items-center justify-between mb-1">
              <div class="text-[10px] font-mono font-bold text-orange-200">UGV</div>
              <div class="text-[8px] font-mono text-orange-300/80">Fire Survivor Search</div>
            </div>
            <div class="flex h-3 rounded overflow-hidden">
              <div class="bg-emerald-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 59%;">59</div>
              <div class="bg-rose-500 flex items-center justify-center text-[7.5px] font-mono font-bold text-white" style="width: 41%;">41</div>
            </div>
            <div class="flex justify-between mt-0.5 text-[7px] font-mono">
              <span class="text-emerald-300">Alert 59%</span>
              <span class="text-rose-300">Unguarded 41%</span>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Class Imbalance</span> escalates with task complexity (PVT → UAV → UGV)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">UGV</span> shows the most balanced split (59/41) → high cognitive demand</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">SMOTE</span> applied per training split to balance minority class</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Alert (High Vigilance)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Unguarded (Low Vigilance)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>PVT</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>UAV</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>UGV</div>
    </div>
  </div>
</div>

<style>
@keyframes s17BarGrow {
  0% { transform: scaleY(0); opacity: 0; }
  100% { transform: scaleY(1); opacity: 1; }
}
.s17-bar-pvt-alert, .s17-bar-pvt-unguarded, .s17-bar-uav-alert, .s17-bar-uav-unguarded, .s17-bar-ugv-alert, .s17-bar-ugv-unguarded {
  transform-origin: bottom;
  animation: s17BarGrow 1.2s cubic-bezier(0.16, 1, 0.3, 1) both;
  box-shadow: 0 0 8px rgba(255,255,255,0.05);
}
.s17-bar-pvt-alert { animation-delay: 0.2s; }
.s17-bar-pvt-unguarded { animation-delay: 0.35s; }
.s17-bar-uav-alert { animation-delay: 0.5s; }
.s17-bar-uav-unguarded { animation-delay: 0.65s; }
.s17-bar-ugv-alert { animation-delay: 0.8s; }
.s17-bar-ugv-unguarded { animation-delay: 0.95s; }
@keyframes s17BarGlow {
  0%, 100% { filter: brightness(1) saturate(1); }
  50% { filter: brightness(1.15) saturate(1.2); box-shadow: 0 0 14px currentColor; }
}
.s17-bar-pvt-alert, .s17-bar-uav-alert, .s17-bar-ugv-alert { color: #34d399; }
.s17-bar-pvt-unguarded, .s17-bar-uav-unguarded, .s17-bar-ugv-unguarded { color: #fb7185; }
@keyframes s17SummaryRow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 12px currentColor, inset 0 0 6px rgba(255,255,255,0.05); transform: scale(1.01); }
}
[class*="s17-summary-row"] { animation: s17SummaryRow 3.5s ease-in-out infinite; }
.s17-summary-row:nth-child(1) { color: #c084fc; animation-delay: 0s; }
.s17-summary-row:nth-child(2) { color: #67e8f9; animation-delay: 1.2s; }
.s17-summary-row:nth-child(3) { color: #fb923c; animation-delay: 2.4s; }
@keyframes s17Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s17-pulse { animation: s17Pulse 1.6s ease-in-out infinite; }
@keyframes s17PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s17-pulse-strong { animation: s17PulseStrong 0.9s ease-in-out infinite; }
@keyframes s17BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s17-blink-text { animation: s17BlinkText 0.9s steps(2, end) infinite; }
@keyframes s17Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s17BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s17-bar-pulse-1, .s17-bar-pulse-2, .s17-bar-pulse-3 { animation: s17BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s17-bar-pulse-1 { color: #34d399; animation-delay: 0s; }
.s17-bar-pulse-2 { color: #2dd4bf; animation-delay: -0.8s; }
.s17-bar-pulse-3 { color: #fb7185; animation-delay: -1.6s; }
@keyframes s17BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s17-bar-dot { animation: s17BarDot 1.6s ease-in-out infinite; }
.s17-breathe-1 { animation: s17Breathe 8s ease-in-out infinite; }
.s17-breathe-2 { animation: s17Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s17-breathe-3 { animation: s17Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s17ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s17-scan-line { animation: s17ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s18-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s18-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-yellow-500/8 rounded-full blur-[140px] s18-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s18-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s18-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 18 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">EEG Preprocessing </span><span class="bg-gradient-to-r from-cyan-300 via-emerald-300 to-yellow-300 bg-clip-text text-transparent">Result</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-cyan-400 rounded-full s18-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s18-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-yellow-400 rounded-full s18-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s18-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Raw → Step+Spike Correction → Final Segment</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s18-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s18-blink-text">UGV · Seg 50</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ UGV · Artifact Detection Visualization · Segment 50 (Unguarded)</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">8 Channels · 7s Window · 500 Hz</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s18-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s18-corner-1" style="border-color: #22d3ee;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s18-corner-2" style="border-color: #22d3ee;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s18-corner-3" style="border-color: #22d3ee;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s18-corner-4" style="border-color: #22d3ee;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s18-scan-overlay" style="background: linear-gradient(to right, transparent, #22d3ee, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s18-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s18-rec-badge" style="border-color: rgba(34,211,238,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s18-rec-dot" style="background: #22d3ee;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #22d3ee;">LIVE</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-emerald-400/40">
            <div class="text-[7px] font-mono text-emerald-300 tracking-wider">EEG · 8 CHANNELS · 500 HZ</div>
          </div>
          <img src="/preprocessing-result.png" alt="UGV - Artifact Detection Visualization - Segment 50" class="max-w-full max-h-full object-contain rounded shadow-lg s18-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📊</div>
            <div>Place image at: <span class="text-emerald-300">public/preprocessing-result.png</span></div>
            <div class="text-[8px] text-slate-600">UGV - Artifact Detection Visualization - Segment 50</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Pipeline Stages</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 relative s18-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s18-badge">1</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-cyan-300 tracking-wider">Raw EEG</div>
              <div class="text-[8px] font-mono text-cyan-100/90 leading-tight mt-0.5">Steps=0 · Spikes=0</div>
              <div class="text-[7.5px] font-mono text-cyan-200/70 leading-tight">8 channels · POz, PO3..O2</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s18-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s18-badge">2</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">Step + Spike Corr.</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">Median filter + Interp.</div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Removes drift &amp; outliers</div>
            </div>
          </div>
          <div class="border border-yellow-400/60 rounded-md p-1.5 bg-yellow-950/20 relative s18-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-yellow-500 border border-yellow-200 flex items-center justify-center text-[8px] font-bold text-black s18-badge">3</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-yellow-300 tracking-wider">Final Segment</div>
              <div class="text-[8px] font-mono text-yellow-100/90 leading-tight mt-0.5">FIR Bandpass 1–80 Hz</div>
              <div class="text-[7.5px] font-mono text-yellow-200/70 leading-tight">Notch 49–51 · Avg Ref</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-violet-500/20 via-violet-500/5 to-transparent px-2 py-0.5 border-b border-violet-400/30">
          <div class="text-[10px] font-mono font-bold text-violet-300">▸ Quality Indicators</div>
        </div>
        <div class="p-2 grid grid-cols-2 gap-1.5">
          <div class="border border-emerald-400/40 rounded bg-emerald-950/30 px-1.5 py-1 text-center">
            <div class="text-[14px] font-bold text-emerald-300 leading-none">0</div>
            <div class="text-[7.5px] font-mono text-emerald-200/80 mt-0.5">Steps Detected</div>
          </div>
          <div class="border border-emerald-400/40 rounded bg-emerald-950/30 px-1.5 py-1 text-center">
            <div class="text-[14px] font-bold text-emerald-300 leading-none">0</div>
            <div class="text-[7.5px] font-mono text-emerald-200/80 mt-0.5">Spikes Detected</div>
          </div>
          <div class="border border-cyan-400/40 rounded bg-cyan-950/30 px-1.5 py-1 text-center">
            <div class="text-[14px] font-bold text-cyan-300 leading-none">8s</div>
            <div class="text-[7.5px] font-mono text-cyan-200/80 mt-0.5">Window Size</div>
          </div>
          <div class="border border-yellow-400/40 rounded bg-yellow-950/30 px-1.5 py-1 text-center">
            <div class="text-[14px] font-bold text-yellow-300 leading-none">✓</div>
            <div class="text-[7.5px] font-mono text-yellow-200/80 mt-0.5">Clean Signal</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Raw EEG</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Step+Spike Correction</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Final Processed</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Quality Metrics</div>
    </div>
  </div>
</div>

<style>
@keyframes s18ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s18-image-container { animation: s18ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s18ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s18-image-effect { 
  animation: s18ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s18-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s18ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s18-scan-overlay { 
  animation: s18ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #22d3ee, 0 0 16px rgba(34,211,238,0.5);
}
@keyframes s18BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(34,211,238,0.3), 0 0 12px rgba(34,211,238,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(34,211,238,0.7), 0 0 24px rgba(34,211,238,0.4), 0 0 40px rgba(34,211,238,0.2); }
}
.s18-border-shimmer { animation: s18BorderShimmer 3s ease-in-out infinite; }
@keyframes s18Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #22d3ee; }
}
.s18-corner-1 { animation: s18Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s18-corner-2 { animation: s18Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s18-corner-3 { animation: s18Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s18-corner-4 { animation: s18Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s18RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(34,211,238,0.4); }
  50% { box-shadow: 0 0 12px rgba(34,211,238,0.9), 0 0 20px rgba(34,211,238,0.5); }
}
.s18-rec-badge { animation: s18RecBadge 1.6s ease-in-out infinite; }
@keyframes s18RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #22d3ee, 0 0 8px #22d3ee; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s18-rec-dot { animation: s18RecDot 0.8s ease-in-out infinite; }
@keyframes s18BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s18-badge { animation: s18BadgePulse 2s ease-in-out infinite; }
@keyframes s18StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s18-stage-1 { animation: s18StageGlow 3s ease-in-out infinite; color: #22d3ee; animation-delay: 0s; }
.s18-stage-2 { animation: s18StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s18-stage-3 { animation: s18StageGlow 3s ease-in-out infinite; color: #facc15; animation-delay: 2s; }
@keyframes s18Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s18-pulse { animation: s18Pulse 1.6s ease-in-out infinite; }
@keyframes s18PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s18-pulse-strong { animation: s18PulseStrong 0.9s ease-in-out infinite; }
@keyframes s18BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s18-blink-text { animation: s18BlinkText 0.9s steps(2, end) infinite; }
@keyframes s18Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s18BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s18-bar-pulse-1, .s18-bar-pulse-2, .s18-bar-pulse-3 { animation: s18BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s18-bar-pulse-1 { color: #22d3ee; animation-delay: 0s; }
.s18-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s18-bar-pulse-3 { color: #facc15; animation-delay: -1.6s; }
@keyframes s18BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s18-bar-dot { animation: s18BarDot 1.6s ease-in-out infinite; }
.s18-breathe-1 { animation: s18Breathe 8s ease-in-out infinite; }
.s18-breathe-2 { animation: s18Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s18-breathe-3 { animation: s18Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s18ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s18-scan-line { animation: s18ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s19-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s19-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-violet-500/8 rounded-full blur-[140px] s19-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s19-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s19-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 19 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Eye Tracker </span><span class="bg-gradient-to-r from-rose-300 via-cyan-300 to-violet-300 bg-clip-text text-transparent">Result</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-rose-400 rounded-full s19-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-cyan-400 rounded-full s19-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-violet-400 rounded-full s19-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s19-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Gaze X / Y · Cross-Scenario · Alert vs Unguarded</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s19-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s19-blink-text">Tobii · 90Hz</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Gaze Signals · Cross Scenario · 6 Sample Trials (PVT · UGV · UAV)</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">Gaze X (red) · Gaze Y (cyan)</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s19-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s19-corner-1" style="border-color: #fb7185;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s19-corner-2" style="border-color: #fb7185;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s19-corner-3" style="border-color: #fb7185;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s19-corner-4" style="border-color: #fb7185;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s19-scan-overlay" style="background: linear-gradient(to right, transparent, #fb7185, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s19-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s19-rec-badge" style="border-color: rgba(251,113,133,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s19-rec-dot" style="background: #fb7185;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #fb7185;">TRACK</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-cyan-400/40">
            <div class="text-[7px] font-mono text-cyan-300 tracking-wider">TOBII · 90 HZ · 6 TRIALS</div>
          </div>
          <img src="/gaze-signals.png" alt="Gaze Signals - Cross Scenario" class="max-w-full max-h-full object-contain rounded shadow-lg s19-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">👁️</div>
            <div>Place image at: <span class="text-emerald-300">public/gaze-signals.png</span></div>
            <div class="text-[8px] text-slate-600">Gaze Signals - Cross Scenario</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Per-Scenario Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s19-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s19-badge">1</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">PVT</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Stable fixation · Low variance</div>
              <div class="text-[7.5px] font-mono text-violet-200/70 leading-tight">Unguarded → drop-off near end</div>
            </div>
          </div>
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 relative s19-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s19-badge">2</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-cyan-300 tracking-wider">UGV</div>
              <div class="text-[8px] font-mono text-cyan-100/90 leading-tight mt-0.5">Moderate scan · Spike events</div>
              <div class="text-[7.5px] font-mono text-cyan-200/70 leading-tight">Unguarded → erratic spikes</div>
            </div>
          </div>
          <div class="border border-rose-400/60 rounded-md p-1.5 bg-rose-950/20 relative s19-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[8px] font-bold text-white s19-badge">3</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-rose-300 tracking-wider">UAV</div>
              <div class="text-[8px] font-mono text-rose-100/90 leading-tight mt-0.5">High-freq oscillation</div>
              <div class="text-[7.5px] font-mono text-rose-200/70 leading-tight">Active sea-surface scanning</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> trials show stable, regular gaze paths</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> trials show drop-offs, spikes, and saturation</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">UAV</span> demands the most active visual scanning</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Gaze X</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Gaze Y</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>PVT</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>UGV</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>UAV</div>
    </div>
  </div>
</div>

<style>
@keyframes s19ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s19-image-container { animation: s19ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s19ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s19-image-effect { 
  animation: s19ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s19-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s19ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s19-scan-overlay { 
  animation: s19ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #fb7185, 0 0 16px rgba(251,113,133,0.5);
}
@keyframes s19BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(251,113,133,0.3), 0 0 12px rgba(251,113,133,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(251,113,133,0.7), 0 0 24px rgba(251,113,133,0.4), 0 0 40px rgba(251,113,133,0.2); }
}
.s19-border-shimmer { animation: s19BorderShimmer 3s ease-in-out infinite; }
@keyframes s19Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #fb7185; }
}
.s19-corner-1 { animation: s19Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s19-corner-2 { animation: s19Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s19-corner-3 { animation: s19Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s19-corner-4 { animation: s19Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s19RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(251,113,133,0.4); }
  50% { box-shadow: 0 0 12px rgba(251,113,133,0.9), 0 0 20px rgba(251,113,133,0.5); }
}
.s19-rec-badge { animation: s19RecBadge 1.6s ease-in-out infinite; }
@keyframes s19RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #fb7185, 0 0 8px #fb7185; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s19-rec-dot { animation: s19RecDot 0.8s ease-in-out infinite; }
@keyframes s19BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s19-badge { animation: s19BadgePulse 2s ease-in-out infinite; }
@keyframes s19StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s19-stage-1 { animation: s19StageGlow 3s ease-in-out infinite; color: #c084fc; animation-delay: 0s; }
.s19-stage-2 { animation: s19StageGlow 3s ease-in-out infinite; color: #67e8f9; animation-delay: 1s; }
.s19-stage-3 { animation: s19StageGlow 3s ease-in-out infinite; color: #fb7185; animation-delay: 2s; }
@keyframes s19Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s19-pulse { animation: s19Pulse 1.6s ease-in-out infinite; }
@keyframes s19PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s19-pulse-strong { animation: s19PulseStrong 0.9s ease-in-out infinite; }
@keyframes s19BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s19-blink-text { animation: s19BlinkText 0.9s steps(2, end) infinite; }
@keyframes s19Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s19BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s19-bar-pulse-1, .s19-bar-pulse-2, .s19-bar-pulse-3 { animation: s19BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s19-bar-pulse-1 { color: #fb7185; animation-delay: 0s; }
.s19-bar-pulse-2 { color: #67e8f9; animation-delay: -0.8s; }
.s19-bar-pulse-3 { color: #c084fc; animation-delay: -1.6s; }
@keyframes s19BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s19-bar-dot { animation: s19BarDot 1.6s ease-in-out infinite; }
.s19-breathe-1 { animation: s19Breathe 8s ease-in-out infinite; }
.s19-breathe-2 { animation: s19Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s19-breathe-3 { animation: s19Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s19ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s19-scan-line { animation: s19ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s20-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s20-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s20-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s20-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s20-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 20 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP · PVT · </span><span class="bg-gradient-to-r from-fuchsia-300 via-amber-300 to-cyan-300 bg-clip-text text-transparent">Stimulus</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-fuchsia-400 rounded-full s20-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-amber-400 rounded-full s20-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-cyan-400 rounded-full s20-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s20-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Stimulus-Locked Spectrogram · Alert (Top) vs Unguarded (Bottom) · 8 Electrodes</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s20-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s20-blink-text">Time-Freq</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ERP Spectrogram · PVT Task · Stimulus-Locked Time-Frequency Response</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">α · β · γ Bands · 0-35 Hz</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s20-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s20-corner-1" style="border-color: #e879f9;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s20-corner-2" style="border-color: #e879f9;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s20-corner-3" style="border-color: #e879f9;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s20-corner-4" style="border-color: #e879f9;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s20-scan-overlay" style="background: linear-gradient(to right, transparent, #e879f9, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s20-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s20-rec-badge" style="border-color: rgba(232,121,249,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s20-rec-dot" style="background: #e879f9;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #e879f9;">TIME-FREQ</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-fuchsia-400/40">
            <div class="text-[7px] font-mono text-fuchsia-300 tracking-wider">PVT · 16 SPECTROGRAMS</div>
          </div>
          <img src="/erp-pvt-spectro.png" alt="ERP - PVT - Stimulus Spectrogram" class="max-w-full max-h-full object-contain rounded shadow-lg s20-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📈</div>
            <div>Place image at: <span class="text-emerald-300">public/erp-pvt-spectro.png</span></div>
            <div class="text-[8px] text-slate-600">ERP - PVT - Stimulus Spectrogram</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Spectral Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-rose-400/60 rounded-md p-1.5 bg-rose-950/20 relative s20-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[8px] font-bold text-white s20-badge">α</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-rose-300 tracking-wider">Low · &lt;10 Hz</div>
              <div class="text-[8px] font-mono text-rose-100/90 leading-tight mt-0.5">Power increase (red)</div>
              <div class="text-[7.5px] font-mono text-rose-200/70 leading-tight">Sustained post-stimulus</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s20-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s20-badge">β</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">Mid · 15-30 Hz</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">Power decrease (dark)</div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Stronger in Alert state</div>
            </div>
          </div>
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s20-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s20-badge">⏱</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">Time · 0-0.4s</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Stimulus locked at t=0</div>
              <div class="text-[7.5px] font-mono text-violet-200/70 leading-tight">Baseline-corrected window</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Sustained low-freq power</span> (&lt;10 Hz) appears post-stimulus across all electrodes</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> shows clearer β-band suppression (dark patches at 15-30 Hz)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> shows weaker suppression → reduced cortical engagement</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Low-freq Power ↑</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Mid-freq Power ↓</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Time Window</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Power (dB)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Baseline-corrected</div>
    </div>
  </div>
</div>

<style>
@keyframes s20ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s20-image-container { animation: s20ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s20ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s20-image-effect { 
  animation: s20ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s20-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s20ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s20-scan-overlay { 
  animation: s20ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #e879f9, 0 0 16px rgba(232,121,249,0.5);
}
@keyframes s20BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(232,121,249,0.3), 0 0 12px rgba(232,121,249,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(232,121,249,0.7), 0 0 24px rgba(232,121,249,0.4), 0 0 40px rgba(232,121,249,0.2); }
}
.s20-border-shimmer { animation: s20BorderShimmer 3s ease-in-out infinite; }
@keyframes s20Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #e879f9; }
}
.s20-corner-1 { animation: s20Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s20-corner-2 { animation: s20Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s20-corner-3 { animation: s20Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s20-corner-4 { animation: s20Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s20RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(232,121,249,0.4); }
  50% { box-shadow: 0 0 12px rgba(232,121,249,0.9), 0 0 20px rgba(232,121,249,0.5); }
}
.s20-rec-badge { animation: s20RecBadge 1.6s ease-in-out infinite; }
@keyframes s20RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #e879f9, 0 0 8px #e879f9; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s20-rec-dot { animation: s20RecDot 0.8s ease-in-out infinite; }
@keyframes s20BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s20-badge { animation: s20BadgePulse 2s ease-in-out infinite; }
@keyframes s20StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s20-stage-1 { animation: s20StageGlow 3s ease-in-out infinite; color: #fb7185; animation-delay: 0s; }
.s20-stage-2 { animation: s20StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s20-stage-3 { animation: s20StageGlow 3s ease-in-out infinite; color: #c084fc; animation-delay: 2s; }
@keyframes s20Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s20-pulse { animation: s20Pulse 1.6s ease-in-out infinite; }
@keyframes s20PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s20-pulse-strong { animation: s20PulseStrong 0.9s ease-in-out infinite; }
@keyframes s20BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s20-blink-text { animation: s20BlinkText 0.9s steps(2, end) infinite; }
@keyframes s20Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s20BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s20-bar-pulse-1, .s20-bar-pulse-2, .s20-bar-pulse-3 { animation: s20BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s20-bar-pulse-1 { color: #e879f9; animation-delay: 0s; }
.s20-bar-pulse-2 { color: #fbbf24; animation-delay: -0.8s; }
.s20-bar-pulse-3 { color: #67e8f9; animation-delay: -1.6s; }
@keyframes s20BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s20-bar-dot { animation: s20BarDot 1.6s ease-in-out infinite; }
.s20-breathe-1 { animation: s20Breathe 8s ease-in-out infinite; }
.s20-breathe-2 { animation: s20Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s20-breathe-3 { animation: s20Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s20ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s20-scan-line { animation: s20ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-orange-500/8 rounded-full blur-[140px] s21-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s21-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s21-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s21-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s21-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 21 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP · UGV · </span><span class="bg-gradient-to-r from-orange-300 via-rose-300 to-cyan-300 bg-clip-text text-transparent">Stimulus</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-orange-400 rounded-full s21-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-rose-400 rounded-full s21-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-cyan-400 rounded-full s21-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s21-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Stimulus-Locked Spectrogram · Alert (Top) vs Unguarded (Bottom) · 8 Electrodes</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s21-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s21-blink-text">Time-Freq</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ERP Spectrogram · UGV Task · Stimulus-Locked Time-Frequency Response</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">0-35 Hz · 0-1.9s · ±3 dB</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s21-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s21-corner-1" style="border-color: #fb923c;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s21-corner-2" style="border-color: #fb923c;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s21-corner-3" style="border-color: #fb923c;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s21-corner-4" style="border-color: #fb923c;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s21-scan-overlay" style="background: linear-gradient(to right, transparent, #fb923c, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s21-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s21-rec-badge" style="border-color: rgba(251,146,60,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s21-rec-dot" style="background: #fb923c;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #fb923c;">TIME-FREQ</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-orange-400/40">
            <div class="text-[7px] font-mono text-orange-300 tracking-wider">UGV · 16 SPECTROGRAMS</div>
          </div>
          <img src="/erp-ugv-stim.png" alt="ERP - UGV - Stimulus Spectrogram" class="max-w-full max-h-full object-contain rounded shadow-lg s21-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📈</div>
            <div>Place image at: <span class="text-emerald-300">public/erp-ugv-stim.png</span></div>
            <div class="text-[8px] text-slate-600">ERP - UGV - Stimulus Spectrogram</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Spectral Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-orange-400/60 rounded-md p-1.5 bg-orange-950/20 relative s21-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-orange-500 border border-orange-200 flex items-center justify-center text-[8px] font-bold text-white s21-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-orange-300 tracking-wider">High Power · Mid-Band</div>
              <div class="text-[8px] font-mono text-orange-100/90 leading-tight mt-0.5">Scattered red hotspots</div>
              <div class="text-[7.5px] font-mono text-orange-200/70 leading-tight">15-30 Hz · throughout time</div>
            </div>
          </div>
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 relative s21-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s21-badge">↓</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-cyan-300 tracking-wider">Suppression Patches</div>
              <div class="text-[8px] font-mono text-cyan-100/90 leading-tight mt-0.5">Dark blue regions</div>
              <div class="text-[7.5px] font-mono text-cyan-200/70 leading-tight">Less prominent in Unguarded</div>
            </div>
          </div>
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s21-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s21-badge">⏱</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">Time · 0-1.9s</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Extended trial window</div>
              <div class="text-[7.5px] font-mono text-violet-200/70 leading-tight">Sustained motor + cognitive</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">UGV</span> shows broader spectral activation than PVT (motor + visual)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> shows persistent red bands → reduced cortical regulation</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> shows more dynamic suppression-activation patterns</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>Power ↑ (Red)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Power ↓ (Blue)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Time Window</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Power (dB)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Baseline-corrected</div>
    </div>
  </div>
</div>

<style>
@keyframes s21ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s21-image-container { animation: s21ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s21ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s21-image-effect { 
  animation: s21ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s21-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s21ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s21-scan-overlay { 
  animation: s21ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #fb923c, 0 0 16px rgba(251,146,60,0.5);
}
@keyframes s21BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(251,146,60,0.3), 0 0 12px rgba(251,146,60,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(251,146,60,0.7), 0 0 24px rgba(251,146,60,0.4), 0 0 40px rgba(251,146,60,0.2); }
}
.s21-border-shimmer { animation: s21BorderShimmer 3s ease-in-out infinite; }
@keyframes s21Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #fb923c; }
}
.s21-corner-1 { animation: s21Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s21-corner-2 { animation: s21Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s21-corner-3 { animation: s21Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s21-corner-4 { animation: s21Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s21RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(251,146,60,0.4); }
  50% { box-shadow: 0 0 12px rgba(251,146,60,0.9), 0 0 20px rgba(251,146,60,0.5); }
}
.s21-rec-badge { animation: s21RecBadge 1.6s ease-in-out infinite; }
@keyframes s21RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #fb923c, 0 0 8px #fb923c; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s21-rec-dot { animation: s21RecDot 0.8s ease-in-out infinite; }
@keyframes s21BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s21-badge { animation: s21BadgePulse 2s ease-in-out infinite; }
@keyframes s21StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s21-stage-1 { animation: s21StageGlow 3s ease-in-out infinite; color: #fb923c; animation-delay: 0s; }
.s21-stage-2 { animation: s21StageGlow 3s ease-in-out infinite; color: #67e8f9; animation-delay: 1s; }
.s21-stage-3 { animation: s21StageGlow 3s ease-in-out infinite; color: #c084fc; animation-delay: 2s; }
@keyframes s21Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s21-pulse { animation: s21Pulse 1.6s ease-in-out infinite; }
@keyframes s21PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s21-pulse-strong { animation: s21PulseStrong 0.9s ease-in-out infinite; }
@keyframes s21BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s21-blink-text { animation: s21BlinkText 0.9s steps(2, end) infinite; }
@keyframes s21Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s21BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s21-bar-pulse-1, .s21-bar-pulse-2, .s21-bar-pulse-3 { animation: s21BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s21-bar-pulse-1 { color: #fb923c; animation-delay: 0s; }
.s21-bar-pulse-2 { color: #fb7185; animation-delay: -0.8s; }
.s21-bar-pulse-3 { color: #67e8f9; animation-delay: -1.6s; }
@keyframes s21BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s21-bar-dot { animation: s21BarDot 1.6s ease-in-out infinite; }
.s21-breathe-1 { animation: s21Breathe 8s ease-in-out infinite; }
.s21-breathe-2 { animation: s21Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s21-breathe-3 { animation: s21Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s21ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s21-scan-line { animation: s21ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-red-500/8 rounded-full blur-[140px] s22-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-orange-500/8 rounded-full blur-[140px] s22-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-cyan-500/8 rounded-full blur-[140px] s22-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s22-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s22-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 22 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP · UGV · </span><span class="bg-gradient-to-r from-red-300 via-orange-300 to-cyan-300 bg-clip-text text-transparent">Collision</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-red-400 rounded-full s22-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-orange-400 rounded-full s22-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-cyan-400 rounded-full s22-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s22-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Collision-Locked Spectrogram · Alert (Top) vs Unguarded (Bottom) · 8 Electrodes</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s22-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s22-blink-text">Error Event</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ERP Spectrogram · UGV Task · Collision-Locked Time-Frequency Response</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">0-35 Hz · 0-1.9s · ±3 dB</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s22-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 border-red-400 z-10 s22-corner-1"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 border-red-400 z-10 s22-corner-2"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 border-red-400 z-10 s22-corner-3"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 border-red-400 z-10 s22-corner-4"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] bg-gradient-to-r from-transparent via-red-400 to-transparent opacity-60 s22-scan-overlay"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s22-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-red-400/40 s22-rec-badge">
            <div class="w-1.5 h-1.5 bg-red-500 rounded-full s22-rec-dot"></div>
            <div class="text-[7px] font-mono font-bold text-red-300 tracking-wider">REC</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-emerald-400/40">
            <div class="text-[7px] font-mono text-emerald-300 tracking-wider">UGV · 16 SPECTROGRAMS</div>
          </div>
          <img src="/erp-ugv-col.png" alt="ERP UGV Collision Spectrogram" class="max-w-full max-h-full object-contain rounded shadow-lg s22-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">💥</div>
            <div>Place image at: <span class="text-emerald-300">public/erp-ugv-col.png</span></div>
            <div class="text-[8px] text-slate-600">ERP - UGV - Collision Spectrogram</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Spectral Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-red-400/60 rounded-md p-1.5 bg-red-950/20 relative s22-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-red-500 border border-red-200 flex items-center justify-center text-[8px] font-bold text-white s22-badge">⚡</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-red-300 tracking-wider">Strong Activation</div>
              <div class="text-[8px] font-mono text-red-100/90 leading-tight mt-0.5">Wide red bands</div>
              <div class="text-[7.5px] font-mono text-red-200/70 leading-tight">15-30 Hz · post-collision</div>
            </div>
          </div>
          <div class="border border-orange-400/60 rounded-md p-1.5 bg-orange-950/20 relative s22-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-orange-500 border border-orange-200 flex items-center justify-center text-[8px] font-bold text-white s22-badge">!</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-orange-300 tracking-wider">Error-Related Burst</div>
              <div class="text-[8px] font-mono text-orange-100/90 leading-tight mt-0.5">Sustained mid-band power</div>
              <div class="text-[7.5px] font-mono text-orange-200/70 leading-tight">Stronger over PO3, PO4, O1</div>
            </div>
          </div>
          <div class="border border-cyan-400/60 rounded-md p-1.5 bg-cyan-950/20 relative s22-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-cyan-500 border border-cyan-200 flex items-center justify-center text-[8px] font-bold text-white s22-badge">↓</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-cyan-300 tracking-wider">Brief Suppression</div>
              <div class="text-[8px] font-mono text-cyan-100/90 leading-tight mt-0.5">Dark blue near onset</div>
              <div class="text-[7.5px] font-mono text-cyan-200/70 leading-tight">Pre-error inhibition</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Collision events</span> trigger broader and stronger ERP than stimulus</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> shows sustained error response → late awareness</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> shows early suppression → proactive error monitoring</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-red-400 rounded-sm"></div>Strong Activation</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>Error Burst</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Suppression</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Power (dB)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Baseline-corrected</div>
    </div>
  </div>
</div>

<style>
@keyframes s22ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s22-image-container { animation: s22ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s22ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s22-image-effect { 
  animation: s22ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s22-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s22ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s22-scan-overlay { 
  animation: s22ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #f87171, 0 0 16px rgba(248,113,113,0.5);
}
@keyframes s22BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(248,113,113,0.3), 0 0 12px rgba(248,113,113,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(248,113,113,0.7), 0 0 24px rgba(248,113,113,0.4), 0 0 40px rgba(251,146,60,0.2); }
}
.s22-border-shimmer { animation: s22BorderShimmer 3s ease-in-out infinite; }
@keyframes s22Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #f87171; }
}
.s22-corner-1 { animation: s22Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s22-corner-2 { animation: s22Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s22-corner-3 { animation: s22Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s22-corner-4 { animation: s22Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s22RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(248,113,113,0.4); }
  50% { box-shadow: 0 0 12px rgba(248,113,113,0.9), 0 0 20px rgba(248,113,113,0.5); }
}
.s22-rec-badge { animation: s22RecBadge 1.6s ease-in-out infinite; }
@keyframes s22RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #ef4444, 0 0 8px #ef4444; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s22-rec-dot { animation: s22RecDot 0.8s ease-in-out infinite; }
@keyframes s22BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s22-badge { animation: s22BadgePulse 2s ease-in-out infinite; }
@keyframes s22StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s22-stage-1 { animation: s22StageGlow 3s ease-in-out infinite; color: #f87171; animation-delay: 0s; }
.s22-stage-2 { animation: s22StageGlow 3s ease-in-out infinite; color: #fb923c; animation-delay: 1s; }
.s22-stage-3 { animation: s22StageGlow 3s ease-in-out infinite; color: #67e8f9; animation-delay: 2s; }
@keyframes s22Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s22-pulse { animation: s22Pulse 1.6s ease-in-out infinite; }
@keyframes s22PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s22-pulse-strong { animation: s22PulseStrong 0.9s ease-in-out infinite; }
@keyframes s22BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s22-blink-text { animation: s22BlinkText 0.9s steps(2, end) infinite; }
@keyframes s22Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s22BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s22-bar-pulse-1, .s22-bar-pulse-2, .s22-bar-pulse-3 { animation: s22BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s22-bar-pulse-1 { color: #f87171; animation-delay: 0s; }
.s22-bar-pulse-2 { color: #fb923c; animation-delay: -0.8s; }
.s22-bar-pulse-3 { color: #67e8f9; animation-delay: -1.6s; }
@keyframes s22BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s22-bar-dot { animation: s22BarDot 1.6s ease-in-out infinite; }
.s22-breathe-1 { animation: s22Breathe 8s ease-in-out infinite; }
.s22-breathe-2 { animation: s22Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s22-breathe-3 { animation: s22Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s22ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s22-scan-line { animation: s22ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-sky-500/8 rounded-full blur-[140px] s23-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s23-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s23-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s23-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s23-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 23 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP · UAV · </span><span class="bg-gradient-to-r from-sky-300 via-rose-300 to-amber-300 bg-clip-text text-transparent">Stimulus</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-sky-400 rounded-full s23-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-rose-400 rounded-full s23-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-amber-400 rounded-full s23-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s23-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Stimulus-Locked Spectrogram · Alert (Top) vs Unguarded (Bottom) · 8 Electrodes</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s23-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s23-blink-text">Time-Freq</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ERP Spectrogram · UAV Task · Stimulus-Locked Time-Frequency Response</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">0-35 Hz · 0-2.5s · ±4 dB</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s23-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s23-corner-1" style="border-color: #38bdf8;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s23-corner-2" style="border-color: #38bdf8;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s23-corner-3" style="border-color: #38bdf8;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s23-corner-4" style="border-color: #38bdf8;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s23-scan-overlay" style="background: linear-gradient(to right, transparent, #38bdf8, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s23-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s23-rec-badge" style="border-color: rgba(56,189,248,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s23-rec-dot" style="background: #38bdf8;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #38bdf8;">TIME-FREQ</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-sky-400/40">
            <div class="text-[7px] font-mono text-sky-300 tracking-wider">UAV · 16 SPECTROGRAMS</div>
          </div>
          <img src="/erp-uav-stim.png" alt="ERP UAV Stimulus Spectrogram" class="max-w-full max-h-full object-contain rounded shadow-lg s23-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📈</div>
            <div>Place image at: <span class="text-emerald-300">public/erp-uav-stim.png</span></div>
            <div class="text-[8px] text-slate-600">ERP - UAV - Stimulus Spectrogram</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Spectral Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-rose-400/60 rounded-md p-1.5 bg-rose-950/20 relative s23-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[8px] font-bold text-white s23-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-rose-300 tracking-wider">Strong Mid-Band Power</div>
              <div class="text-[8px] font-mono text-rose-100/90 leading-tight mt-0.5">Dense red bands</div>
              <div class="text-[7.5px] font-mono text-rose-200/70 leading-tight">10-25 Hz · sustained activity</div>
            </div>
          </div>
          <div class="border border-sky-400/60 rounded-md p-1.5 bg-sky-950/20 relative s23-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-sky-500 border border-sky-200 flex items-center justify-center text-[8px] font-bold text-white s23-badge">↓</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-sky-300 tracking-wider">Periodic Suppression</div>
              <div class="text-[8px] font-mono text-sky-100/90 leading-tight mt-0.5">Vertical blue stripes</div>
              <div class="text-[7.5px] font-mono text-sky-200/70 leading-tight">Rhythmic scanning pattern</div>
            </div>
          </div>
          <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 relative s23-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-black s23-badge">⏱</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-amber-300 tracking-wider">Time · 0-2.5s</div>
              <div class="text-[8px] font-mono text-amber-100/90 leading-tight mt-0.5">Long search window</div>
              <div class="text-[7.5px] font-mono text-amber-200/70 leading-tight">Sea-surface visual scanning</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">UAV</span> shows densest spectral activation among all tasks</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> O1 channel shows extreme red saturation → fatigue</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> shows balanced suppression-activation rhythm</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Power ↑ (Red)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-sky-400 rounded-sm"></div>Power ↓ (Blue)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-amber-400 rounded-sm"></div>Time Window</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Power (dB)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Baseline-corrected</div>
    </div>
  </div>
</div>

<style>
@keyframes s23ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s23-image-container { animation: s23ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s23ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s23-image-effect { 
  animation: s23ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s23-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s23ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s23-scan-overlay { 
  animation: s23ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #38bdf8, 0 0 16px rgba(56,189,248,0.5);
}
@keyframes s23BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.3), 0 0 12px rgba(56,189,248,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.7), 0 0 24px rgba(56,189,248,0.4), 0 0 40px rgba(56,189,248,0.2); }
}
.s23-border-shimmer { animation: s23BorderShimmer 3s ease-in-out infinite; }
@keyframes s23Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #38bdf8; }
}
.s23-corner-1 { animation: s23Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s23-corner-2 { animation: s23Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s23-corner-3 { animation: s23Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s23-corner-4 { animation: s23Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s23RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(56,189,248,0.4); }
  50% { box-shadow: 0 0 12px rgba(56,189,248,0.9), 0 0 20px rgba(56,189,248,0.5); }
}
.s23-rec-badge { animation: s23RecBadge 1.6s ease-in-out infinite; }
@keyframes s23RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #38bdf8, 0 0 8px #38bdf8; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s23-rec-dot { animation: s23RecDot 0.8s ease-in-out infinite; }
@keyframes s23BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s23-badge { animation: s23BadgePulse 2s ease-in-out infinite; }
@keyframes s23StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s23-stage-1 { animation: s23StageGlow 3s ease-in-out infinite; color: #fb7185; animation-delay: 0s; }
.s23-stage-2 { animation: s23StageGlow 3s ease-in-out infinite; color: #38bdf8; animation-delay: 1s; }
.s23-stage-3 { animation: s23StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 2s; }
@keyframes s23Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s23-pulse { animation: s23Pulse 1.6s ease-in-out infinite; }
@keyframes s23PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s23-pulse-strong { animation: s23PulseStrong 0.9s ease-in-out infinite; }
@keyframes s23BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s23-blink-text { animation: s23BlinkText 0.9s steps(2, end) infinite; }
@keyframes s23Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s23BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s23-bar-pulse-1, .s23-bar-pulse-2, .s23-bar-pulse-3 { animation: s23BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s23-bar-pulse-1 { color: #38bdf8; animation-delay: 0s; }
.s23-bar-pulse-2 { color: #fb7185; animation-delay: -0.8s; }
.s23-bar-pulse-3 { color: #fbbf24; animation-delay: -1.6s; }
@keyframes s23BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s23-bar-dot { animation: s23BarDot 1.6s ease-in-out infinite; }
.s23-breathe-1 { animation: s23Breathe 8s ease-in-out infinite; }
.s23-breathe-2 { animation: s23Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s23-breathe-3 { animation: s23Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s23ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s23-scan-line { animation: s23ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-yellow-500/8 rounded-full blur-[140px] s24-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-orange-500/8 rounded-full blur-[140px] s24-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-violet-500/8 rounded-full blur-[140px] s24-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s24-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s24-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 24 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP · UAV · </span><span class="bg-gradient-to-r from-yellow-300 via-orange-300 to-violet-300 bg-clip-text text-transparent">Deviation</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-yellow-400 rounded-full s24-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-orange-400 rounded-full s24-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-violet-400 rounded-full s24-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s24-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Deviation-Locked Spectrogram · Alert (Top) vs Unguarded (Bottom) · 8 Electrodes</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s24-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s24-blink-text">Drift Event</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ERP Spectrogram · UAV Task · Deviation-Locked Time-Frequency Response</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">0-35 Hz · 0-3.5s · -4 to +3 dB</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-slate-950/40 relative">
        <div class="relative max-w-full max-h-full s24-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s24-corner-1" style="border-color: #facc15;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s24-corner-2" style="border-color: #facc15;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s24-corner-3" style="border-color: #facc15;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s24-corner-4" style="border-color: #facc15;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s24-scan-overlay" style="background: linear-gradient(to right, transparent, #facc15, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s24-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s24-rec-badge" style="border-color: rgba(250,204,21,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s24-rec-dot" style="background: #facc15;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #facc15;">DRIFT</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-yellow-400/40">
            <div class="text-[7px] font-mono text-yellow-300 tracking-wider">UAV · YAW DEVIATION EVENT</div>
          </div>
          <img src="/erp-uav-dev.png" alt="ERP UAV Deviation Spectrogram" class="max-w-full max-h-full object-contain rounded shadow-lg s24-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">⚠️</div>
            <div>Place image at: <span class="text-emerald-300">public/erp-uav-dev.png</span></div>
            <div class="text-[8px] text-slate-600">ERP - UAV - Deviation Spectrogram</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Spectral Patterns</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-yellow-400/60 rounded-md p-1.5 bg-yellow-950/20 relative s24-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-yellow-500 border border-yellow-200 flex items-center justify-center text-[8px] font-bold text-black s24-badge">↓</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-yellow-300 tracking-wider">Suppression Mosaic</div>
              <div class="text-[8px] font-mono text-yellow-100/90 leading-tight mt-0.5">Mixed dark patches</div>
              <div class="text-[7.5px] font-mono text-yellow-200/70 leading-tight">Strong in Alert · 15-30 Hz</div>
            </div>
          </div>
          <div class="border border-orange-400/60 rounded-md p-1.5 bg-orange-950/20 relative s24-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-orange-500 border border-orange-200 flex items-center justify-center text-[8px] font-bold text-white s24-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-orange-300 tracking-wider">Persistent Red Power</div>
              <div class="text-[8px] font-mono text-orange-100/90 leading-tight mt-0.5">Sustained activation</div>
              <div class="text-[7.5px] font-mono text-orange-200/70 leading-tight">Dominant in Unguarded</div>
            </div>
          </div>
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s24-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s24-badge">⏱</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">Time · 0-3.5s</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Continuous correction</div>
              <div class="text-[7.5px] font-mono text-violet-200/70 leading-tight">Long control window</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Alert</span> shows active suppression mosaic → engaged correction</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Unguarded</span> dominated by red bands → poor cortical regulation</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">POz, PO6, Oz</span> show strongest unguarded power increase</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Suppression ↓</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-orange-400 rounded-sm"></div>Activation ↑</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Time Window</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Power (dB)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>Baseline-corrected</div>
    </div>
  </div>
</div>

<style>
@keyframes s24ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); filter: blur(8px) saturate(0.5); }
  100% { opacity: 1; transform: scale(1) translateY(0); filter: blur(0) saturate(1); }
}
.s24-image-container { animation: s24ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; }
@keyframes s24ImageEffect {
  0%, 100% { filter: brightness(1) saturate(1) contrast(1); }
  50% { filter: brightness(1.05) saturate(1.15) contrast(1.05); }
}
.s24-image-effect { 
  animation: s24ImageEffect 4s ease-in-out infinite; 
  transition: transform 0.4s ease-out, filter 0.4s ease-out;
}
.s24-image-effect:hover { 
  transform: scale(1.02); 
  filter: brightness(1.1) saturate(1.3) contrast(1.1);
}
@keyframes s24ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s24-scan-overlay { 
  animation: s24ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #facc15, 0 0 16px rgba(250,204,21,0.5);
}
@keyframes s24BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(250,204,21,0.3), 0 0 12px rgba(250,204,21,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(250,204,21,0.7), 0 0 24px rgba(250,204,21,0.4), 0 0 40px rgba(250,204,21,0.2); }
}
.s24-border-shimmer { animation: s24BorderShimmer 3s ease-in-out infinite; }
@keyframes s24Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #facc15; }
}
.s24-corner-1 { animation: s24Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s24-corner-2 { animation: s24Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s24-corner-3 { animation: s24Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s24-corner-4 { animation: s24Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s24RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(250,204,21,0.4); }
  50% { box-shadow: 0 0 12px rgba(250,204,21,0.9), 0 0 20px rgba(250,204,21,0.5); }
}
.s24-rec-badge { animation: s24RecBadge 1.6s ease-in-out infinite; }
@keyframes s24RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #facc15, 0 0 8px #facc15; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s24-rec-dot { animation: s24RecDot 0.8s ease-in-out infinite; }
@keyframes s24BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s24-badge { animation: s24BadgePulse 2s ease-in-out infinite; }
@keyframes s24StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s24-stage-1 { animation: s24StageGlow 3s ease-in-out infinite; color: #facc15; animation-delay: 0s; }
.s24-stage-2 { animation: s24StageGlow 3s ease-in-out infinite; color: #fb923c; animation-delay: 1s; }
.s24-stage-3 { animation: s24StageGlow 3s ease-in-out infinite; color: #c084fc; animation-delay: 2s; }
@keyframes s24Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s24-pulse { animation: s24Pulse 1.6s ease-in-out infinite; }
@keyframes s24PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s24-pulse-strong { animation: s24PulseStrong 0.9s ease-in-out infinite; }
@keyframes s24BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s24-blink-text { animation: s24BlinkText 0.9s steps(2, end) infinite; }
@keyframes s24Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s24BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s24-bar-pulse-1, .s24-bar-pulse-2, .s24-bar-pulse-3 { animation: s24BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s24-bar-pulse-1 { color: #facc15; animation-delay: 0s; }
.s24-bar-pulse-2 { color: #fb923c; animation-delay: -0.8s; }
.s24-bar-pulse-3 { color: #c084fc; animation-delay: -1.6s; }
@keyframes s24BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s24-bar-dot { animation: s24BarDot 1.6s ease-in-out infinite; }
.s24-breathe-1 { animation: s24Breathe 8s ease-in-out infinite; }
.s24-breathe-2 { animation: s24Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s24-breathe-3 { animation: s24Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s24ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s24-scan-line { animation: s24ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-red-500/8 rounded-full blur-[140px] s25-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-blue-500/8 rounded-full blur-[140px] s25-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-violet-500/8 rounded-full blur-[140px] s25-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s25-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s25-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 25 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ERP </span><span class="bg-gradient-to-r from-red-300 via-blue-300 to-violet-300 bg-clip-text text-transparent">Topography</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-red-400 rounded-full s25-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-blue-400 rounded-full s25-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-violet-400 rounded-full s25-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s25-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Scalp Topography · Alert vs Unguarded · 4 Event Types</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s25-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s25-blink-text">Animated</div>
      </div>
    </div>
  </div>
  <div class="flex-1 grid grid-cols-2 grid-rows-2 gap-2 min-h-0 mt-1">
    <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="w-4 h-4 rounded-full bg-cyan-500 flex items-center justify-center text-[8px] font-bold text-white">1</div>
        <div class="text-[10px] font-mono font-bold text-cyan-300">▸ UGV · Stimulus · +300 ms</div>
        <div class="flex-1 h-px bg-gradient-to-r from-cyan-400/50 to-transparent"></div>
        <div class="text-[7px] font-mono text-cyan-400/70">P3 component</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s25-image-container">
          <div class="absolute -top-1 -left-1 w-3 h-3 border-l-2 border-t-2 z-10 s25-corner" style="border-color: #67e8f9;"></div>
          <div class="absolute -top-1 -right-1 w-3 h-3 border-r-2 border-t-2 z-10 s25-corner" style="border-color: #67e8f9; animation-delay: -0.6s;"></div>
          <div class="absolute -bottom-1 -left-1 w-3 h-3 border-l-2 border-b-2 z-10 s25-corner" style="border-color: #67e8f9; animation-delay: -1.2s;"></div>
          <div class="absolute -bottom-1 -right-1 w-3 h-3 border-r-2 border-b-2 z-10 s25-corner" style="border-color: #67e8f9; animation-delay: -1.8s;"></div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s25-shimmer-cyan"></div>
          <div class="absolute top-1.5 right-1.5 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-cyan-400/40 s25-rec-cyan">
            <div class="w-1 h-1 rounded-full bg-cyan-400 s25-rec-dot-cyan"></div>
            <div class="text-[6px] font-mono font-bold text-cyan-300 tracking-wider">.GIF</div>
          </div>
          <img src="/topo-ugv-stim.gif" alt="UGV Stimulus Topography" class="block w-full h-full object-contain rounded shadow-lg s25-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-1 text-slate-500 font-mono text-[8px] p-3 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[12px] text-cyan-400">🧠</div>
            <div class="text-cyan-300">topo-ugv-stim.gif</div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-red-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-red-500/20 via-red-500/5 to-transparent px-2 py-0.5 border-b border-red-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="w-4 h-4 rounded-full bg-red-500 flex items-center justify-center text-[8px] font-bold text-white">2</div>
        <div class="text-[10px] font-mono font-bold text-red-300">▸ UGV · Collision · +140 ms</div>
        <div class="flex-1 h-px bg-gradient-to-r from-red-400/50 to-transparent"></div>
        <div class="text-[7px] font-mono text-red-400/70">ERN/Pe</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s25-image-container" style="animation-delay: 0.4s;">
          <div class="absolute -top-1 -left-1 w-3 h-3 border-l-2 border-t-2 z-10 s25-corner" style="border-color: #f87171;"></div>
          <div class="absolute -top-1 -right-1 w-3 h-3 border-r-2 border-t-2 z-10 s25-corner" style="border-color: #f87171; animation-delay: -0.6s;"></div>
          <div class="absolute -bottom-1 -left-1 w-3 h-3 border-l-2 border-b-2 z-10 s25-corner" style="border-color: #f87171; animation-delay: -1.2s;"></div>
          <div class="absolute -bottom-1 -right-1 w-3 h-3 border-r-2 border-b-2 z-10 s25-corner" style="border-color: #f87171; animation-delay: -1.8s;"></div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s25-shimmer-red"></div>
          <div class="absolute top-1.5 right-1.5 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-red-400/40 s25-rec-red">
            <div class="w-1 h-1 rounded-full bg-red-400 s25-rec-dot-red"></div>
            <div class="text-[6px] font-mono font-bold text-red-300 tracking-wider">.GIF</div>
          </div>
          <img src="/topo-ugv-col.gif" alt="UGV Collision Topography" class="block w-full h-full object-contain rounded shadow-lg s25-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-1 text-slate-500 font-mono text-[8px] p-3 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[12px] text-red-400">💥</div>
            <div class="text-red-300">topo-ugv-col.gif</div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-sky-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-sky-500/20 via-sky-500/5 to-transparent px-2 py-0.5 border-b border-sky-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="w-4 h-4 rounded-full bg-sky-500 flex items-center justify-center text-[8px] font-bold text-white">3</div>
        <div class="text-[10px] font-mono font-bold text-sky-300">▸ UAV · Stimulus · +300 ms</div>
        <div class="flex-1 h-px bg-gradient-to-r from-sky-400/50 to-transparent"></div>
        <div class="text-[7px] font-mono text-sky-400/70">P3 component</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s25-image-container" style="animation-delay: 0.8s;">
          <div class="absolute -top-1 -left-1 w-3 h-3 border-l-2 border-t-2 z-10 s25-corner" style="border-color: #38bdf8;"></div>
          <div class="absolute -top-1 -right-1 w-3 h-3 border-r-2 border-t-2 z-10 s25-corner" style="border-color: #38bdf8; animation-delay: -0.6s;"></div>
          <div class="absolute -bottom-1 -left-1 w-3 h-3 border-l-2 border-b-2 z-10 s25-corner" style="border-color: #38bdf8; animation-delay: -1.2s;"></div>
          <div class="absolute -bottom-1 -right-1 w-3 h-3 border-r-2 border-b-2 z-10 s25-corner" style="border-color: #38bdf8; animation-delay: -1.8s;"></div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s25-shimmer-sky"></div>
          <div class="absolute top-1.5 right-1.5 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-sky-400/40 s25-rec-sky">
            <div class="w-1 h-1 rounded-full bg-sky-400 s25-rec-dot-sky"></div>
            <div class="text-[6px] font-mono font-bold text-sky-300 tracking-wider">.GIF</div>
          </div>
          <img src="/topo-uav-stim.gif" alt="UAV Stimulus Topography" class="block w-full h-full object-contain rounded shadow-lg s25-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-1 text-slate-500 font-mono text-[8px] p-3 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[12px] text-sky-400">🛩️</div>
            <div class="text-sky-300">topo-uav-stim.gif</div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="w-4 h-4 rounded-full bg-yellow-500 flex items-center justify-center text-[8px] font-bold text-black">4</div>
        <div class="text-[10px] font-mono font-bold text-yellow-300">▸ UAV · Deviation · +300 ms</div>
        <div class="flex-1 h-px bg-gradient-to-r from-yellow-400/50 to-transparent"></div>
        <div class="text-[7px] font-mono text-yellow-400/70">Drift response</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s25-image-container" style="animation-delay: 1.2s;">
          <div class="absolute -top-1 -left-1 w-3 h-3 border-l-2 border-t-2 z-10 s25-corner" style="border-color: #facc15;"></div>
          <div class="absolute -top-1 -right-1 w-3 h-3 border-r-2 border-t-2 z-10 s25-corner" style="border-color: #facc15; animation-delay: -0.6s;"></div>
          <div class="absolute -bottom-1 -left-1 w-3 h-3 border-l-2 border-b-2 z-10 s25-corner" style="border-color: #facc15; animation-delay: -1.2s;"></div>
          <div class="absolute -bottom-1 -right-1 w-3 h-3 border-r-2 border-b-2 z-10 s25-corner" style="border-color: #facc15; animation-delay: -1.8s;"></div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s25-shimmer-yellow"></div>
          <div class="absolute top-1.5 right-1.5 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-yellow-400/40 s25-rec-yellow">
            <div class="w-1 h-1 rounded-full bg-yellow-400 s25-rec-dot-yellow"></div>
            <div class="text-[6px] font-mono font-bold text-yellow-300 tracking-wider">.GIF</div>
          </div>
          <img src="/topo-uav-dev.gif" alt="UAV Deviation Topography" class="block w-full h-full object-contain rounded shadow-lg s25-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-1 text-slate-500 font-mono text-[8px] p-3 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[12px] text-yellow-400">⚠️</div>
            <div class="text-yellow-300">topo-uav-dev.gif</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>UGV Stim</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-red-400 rounded-sm"></div>UGV Col</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-sky-400 rounded-sm"></div>UAV Stim</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>UAV Dev</div>
      <div class="flex items-center gap-1"><div class="w-3 h-1.5 rounded-sm" style="background: linear-gradient(to right, #2563eb, #fff, #dc2626);"></div>Power (-/+ μV)</div>
    </div>
  </div>
</div>

<style>
@keyframes s25ImageEntry {
  0% { opacity: 0; transform: scale(0.85) translateY(15px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s25-image-container { 
  animation: s25ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; 
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.s25-image-effect { 
  transition: transform 0.3s ease-out;
}
.s25-image-effect:hover { 
  transform: scale(1.03); 
}
@keyframes s25Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.25); box-shadow: 0 0 6px currentColor; }
}
.s25-corner { animation: s25Corner 2.4s ease-in-out infinite; transform-origin: center; }
@keyframes s25ShimmerCyan {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(103,232,249,0.25), 0 0 8px rgba(103,232,249,0.1); }
  50% { box-shadow: inset 0 0 0 1px rgba(103,232,249,0.6), 0 0 16px rgba(103,232,249,0.3), 0 0 28px rgba(103,232,249,0.15); }
}
.s25-shimmer-cyan { animation: s25ShimmerCyan 3s ease-in-out infinite; }
@keyframes s25ShimmerRed {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(248,113,113,0.25), 0 0 8px rgba(248,113,113,0.1); }
  50% { box-shadow: inset 0 0 0 1px rgba(248,113,113,0.6), 0 0 16px rgba(248,113,113,0.3), 0 0 28px rgba(248,113,113,0.15); }
}
.s25-shimmer-red { animation: s25ShimmerRed 3s ease-in-out infinite; animation-delay: -0.75s; }
@keyframes s25ShimmerSky {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.25), 0 0 8px rgba(56,189,248,0.1); }
  50% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.6), 0 0 16px rgba(56,189,248,0.3), 0 0 28px rgba(56,189,248,0.15); }
}
.s25-shimmer-sky { animation: s25ShimmerSky 3s ease-in-out infinite; animation-delay: -1.5s; }
@keyframes s25ShimmerYellow {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(250,204,21,0.25), 0 0 8px rgba(250,204,21,0.1); }
  50% { box-shadow: inset 0 0 0 1px rgba(250,204,21,0.6), 0 0 16px rgba(250,204,21,0.3), 0 0 28px rgba(250,204,21,0.15); }
}
.s25-shimmer-yellow { animation: s25ShimmerYellow 3s ease-in-out infinite; animation-delay: -2.25s; }
@keyframes s25RecBadgeCyan {
  0%, 100% { box-shadow: 0 0 3px rgba(103,232,249,0.3); }
  50% { box-shadow: 0 0 8px rgba(103,232,249,0.7), 0 0 14px rgba(103,232,249,0.4); }
}
.s25-rec-cyan { animation: s25RecBadgeCyan 1.6s ease-in-out infinite; }
.s25-rec-red { animation: s25RecBadgeCyan 1.6s ease-in-out infinite; animation-delay: -0.4s; box-shadow: 0 0 3px rgba(248,113,113,0.3); }
.s25-rec-sky { animation: s25RecBadgeCyan 1.6s ease-in-out infinite; animation-delay: -0.8s; box-shadow: 0 0 3px rgba(56,189,248,0.3); }
.s25-rec-yellow { animation: s25RecBadgeCyan 1.6s ease-in-out infinite; animation-delay: -1.2s; box-shadow: 0 0 3px rgba(250,204,21,0.3); }
@keyframes s25RecDotCyan {
  0%, 100% { opacity: 1; box-shadow: 0 0 3px #67e8f9; }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; }
}
.s25-rec-dot-cyan { animation: s25RecDotCyan 0.8s ease-in-out infinite; }
.s25-rec-dot-red { animation: s25RecDotCyan 0.8s ease-in-out infinite; animation-delay: -0.2s; }
.s25-rec-dot-sky { animation: s25RecDotCyan 0.8s ease-in-out infinite; animation-delay: -0.4s; }
.s25-rec-dot-yellow { animation: s25RecDotCyan 0.8s ease-in-out infinite; animation-delay: -0.6s; }
@keyframes s25Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s25-pulse { animation: s25Pulse 1.6s ease-in-out infinite; }
@keyframes s25PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s25-pulse-strong { animation: s25PulseStrong 0.9s ease-in-out infinite; }
@keyframes s25BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s25-blink-text { animation: s25BlinkText 0.9s steps(2, end) infinite; }
@keyframes s25Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s25BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s25-bar-pulse-1, .s25-bar-pulse-2, .s25-bar-pulse-3 { animation: s25BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s25-bar-pulse-1 { color: #f87171; animation-delay: 0s; }
.s25-bar-pulse-2 { color: #60a5fa; animation-delay: -0.8s; }
.s25-bar-pulse-3 { color: #c084fc; animation-delay: -1.6s; }
@keyframes s25BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s25-bar-dot { animation: s25BarDot 1.6s ease-in-out infinite; }
.s25-breathe-1 { animation: s25Breathe 8s ease-in-out infinite; }
.s25-breathe-2 { animation: s25Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s25-breathe-3 { animation: s25Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s25ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s25-scan-line { animation: s25ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-fuchsia-500/8 rounded-full blur-[140px] s26-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s26-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s26-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s26-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s26-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 26 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Feature Selection </span><span class="bg-gradient-to-r from-fuchsia-300 via-emerald-300 to-amber-300 bg-clip-text text-transparent">Result</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-fuchsia-400 rounded-full s26-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s26-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-amber-400 rounded-full s26-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s26-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">5 FS Methods · EEG vs EEG+Gaze · PVT → UGV + UAV</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s26-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s26-blink-text">Best Config</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Feature Selection Comparison · Test Accuracy vs No. of Features</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">5 Methods · n=10 Repeats · 40-100% Range</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s26-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s26-corner-1" style="border-color: #e879f9;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s26-corner-2" style="border-color: #e879f9;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s26-corner-3" style="border-color: #e879f9;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s26-corner-4" style="border-color: #e879f9;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s26-scan-overlay" style="background: linear-gradient(to right, transparent, #e879f9, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s26-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s26-rec-badge" style="border-color: rgba(232,121,249,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s26-rec-dot" style="background: #e879f9;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #e879f9;">FS BENCH</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-fuchsia-400/40">
            <div class="text-[7px] font-mono text-fuchsia-300 tracking-wider">EEG vs EEG+GAZE · ★ BEST k</div>
          </div>
          <img src="/feature-selection-result.png" alt="Feature Selection Result" class="block w-full h-full object-contain rounded shadow-lg s26-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📊</div>
            <div>Place image at: <span class="text-emerald-300">public/feature-selection-result.png</span></div>
            <div class="text-[8px] text-slate-600">Feature Selection - MRMR Sweep Result</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Best Configuration</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-fuchsia-400/60 rounded-md p-1.5 bg-fuchsia-950/20 relative s26-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-fuchsia-500 border border-fuchsia-200 flex items-center justify-center text-[8px] font-bold text-white s26-badge">★</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-fuchsia-300 tracking-wider">EEG only</div>
              <div class="text-[8px] font-mono text-fuchsia-100/90 leading-tight mt-0.5">ReliefF/KW · k=1365 (65%)</div>
              <div class="text-[7.5px] font-mono text-fuchsia-200/70 leading-tight">Acc <span class="text-fuchsia-100 font-bold">58.00%</span> · 2104 features</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s26-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s26-badge">★</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">EEG + Gaze</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">MRMR · k=3227 (88%)</div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Acc <span class="text-emerald-100 font-bold">82.50%</span> · 3672 features</div>
            </div>
          </div>
          <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 relative s26-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-black s26-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-amber-300 tracking-wider">Fusion Gain</div>
              <div class="text-[8px] font-mono text-amber-100/90 leading-tight mt-0.5">+24.5 pp accuracy</div>
              <div class="text-[7.5px] font-mono text-amber-200/70 leading-tight">Eye-tracking adds value</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Key Observations</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">EEG+Gaze</span> outperforms EEG-only by <span class="text-emerald-300 font-bold">+24.5 pp</span> (82.5% vs 58%)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">MRMR</span> wins on multimodal · <span class="text-fuchsia-200">ReliefF/KW</span> on EEG-only</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Accuracy plateaus</span> beyond k≈88% → diminishing returns</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #3b82f6;"></div>MRMR</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #f97316;"></div>ANOVA</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #facc15;"></div>Chi²</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #c084fc;"></div>KW</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22c55e;"></div>ReliefF</div>
      <div class="flex items-center gap-1"><span class="text-yellow-300">★</span>Best</div>
    </div>
  </div>
</div>

<style>
@keyframes s26ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s26-image-container { 
  animation: s26ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; 
}
.s26-image-effect { 
  transition: transform 0.3s ease-out;
}
.s26-image-effect:hover { 
  transform: scale(1.02); 
}
@keyframes s26ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s26-scan-overlay { 
  animation: s26ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #e879f9, 0 0 16px rgba(232,121,249,0.5);
}
@keyframes s26BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(232,121,249,0.3), 0 0 12px rgba(232,121,249,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(232,121,249,0.7), 0 0 24px rgba(232,121,249,0.4), 0 0 40px rgba(232,121,249,0.2); }
}
.s26-border-shimmer { animation: s26BorderShimmer 3s ease-in-out infinite; }
@keyframes s26Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #e879f9; }
}
.s26-corner-1 { animation: s26Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s26-corner-2 { animation: s26Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s26-corner-3 { animation: s26Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s26-corner-4 { animation: s26Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s26RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(232,121,249,0.4); }
  50% { box-shadow: 0 0 12px rgba(232,121,249,0.9), 0 0 20px rgba(232,121,249,0.5); }
}
.s26-rec-badge { animation: s26RecBadge 1.6s ease-in-out infinite; }
@keyframes s26RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #e879f9, 0 0 8px #e879f9; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s26-rec-dot { animation: s26RecDot 0.8s ease-in-out infinite; }
@keyframes s26BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s26-badge { animation: s26BadgePulse 2s ease-in-out infinite; }
@keyframes s26StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s26-stage-1 { animation: s26StageGlow 3s ease-in-out infinite; color: #e879f9; animation-delay: 0s; }
.s26-stage-2 { animation: s26StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s26-stage-3 { animation: s26StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 2s; }
@keyframes s26Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s26-pulse { animation: s26Pulse 1.6s ease-in-out infinite; }
@keyframes s26PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s26-pulse-strong { animation: s26PulseStrong 0.9s ease-in-out infinite; }
@keyframes s26BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s26-blink-text { animation: s26BlinkText 0.9s steps(2, end) infinite; }
@keyframes s26Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s26BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s26-bar-pulse-1, .s26-bar-pulse-2, .s26-bar-pulse-3 { animation: s26BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s26-bar-pulse-1 { color: #e879f9; animation-delay: 0s; }
.s26-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s26-bar-pulse-3 { color: #fbbf24; animation-delay: -1.6s; }
@keyframes s26BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s26-bar-dot { animation: s26BarDot 1.6s ease-in-out infinite; }
.s26-breathe-1 { animation: s26Breathe 8s ease-in-out infinite; }
.s26-breathe-2 { animation: s26Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s26-breathe-3 { animation: s26Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s26ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s26-scan-line { animation: s26ScanLine 6s linear infinite; }
</style>


---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-blue-500/8 rounded-full blur-[140px] s27-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s27-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s27-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s27-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s27-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 27 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Classification </span><span class="bg-gradient-to-r from-blue-300 via-emerald-300 to-amber-300 bg-clip-text text-transparent">Result</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-blue-400 rounded-full s27-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s27-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-amber-400 rounded-full s27-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s27-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Confusion Matrix · 9 Models · EEG vs EEG+Gaze</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s27-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s27-blink-text">Benchmark</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Confusion Matrix Comparison · My Model vs 8 Baselines</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">Alert vs Unguarded · 2 Modalities</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s27-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s27-corner-1" style="border-color: #60a5fa;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s27-corner-2" style="border-color: #60a5fa;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s27-corner-3" style="border-color: #60a5fa;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s27-corner-4" style="border-color: #60a5fa;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s27-scan-overlay" style="background: linear-gradient(to right, transparent, #60a5fa, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s27-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s27-rec-badge" style="border-color: rgba(96,165,250,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s27-rec-dot" style="background: #60a5fa;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #60a5fa;">CONF MAT</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-blue-400/40">
            <div class="text-[7px] font-mono text-blue-300 tracking-wider">9 MODELS · TRUE vs PREDICTED</div>
          </div>
          <img src="/confusion-matrix.png" alt="Confusion Matrix EEG Models" class="block w-full h-full object-contain rounded shadow-lg s27-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📊</div>
            <div>Place image at: <span class="text-emerald-300">public/confusion-matrix.png</span></div>
            <div class="text-[8px] text-slate-600">Confusion Matrix - EEG Models Benchmark</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ My Model · Per-Class Recall</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-blue-400/60 rounded-md p-1.5 bg-blue-950/20 relative s27-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-blue-500 border border-blue-200 flex items-center justify-center text-[8px] font-bold text-white s27-badge">E</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-blue-300 tracking-wider">EEG Only</div>
              <div class="text-[8px] font-mono text-blue-100/90 leading-tight mt-0.5">Alert <span class="text-blue-200 font-bold">40.0%</span> · Unguarded <span class="text-blue-200 font-bold">95.4%</span></div>
              <div class="text-[7.5px] font-mono text-blue-200/70 leading-tight">Bias toward Unguarded class</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s27-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s27-badge">★</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">EEG + Gaze</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">Alert <span class="text-emerald-200 font-bold">91.9%</span> · Unguarded <span class="text-emerald-200 font-bold">63.1%</span></div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Balanced · Fusion stabilizes</div>
            </div>
          </div>
          <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 relative s27-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-black s27-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-amber-300 tracking-wider">Recall Gain</div>
              <div class="text-[8px] font-mono text-amber-100/90 leading-tight mt-0.5">Alert: <span class="text-amber-200 font-bold">+51.9 pp</span></div>
              <div class="text-[7.5px] font-mono text-amber-200/70 leading-tight">Eye-tracking corrects bias</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Baseline Failure Modes</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">EEGSurvNet</span> degenerate → predicts only Alert (100/0%)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">DeepConvNet · LaBraM</span> over-predict Alert (~94%)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">ShallowConvNet</span> inverted → over-predict Unguarded</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #3b82f6;"></div>My Model</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22c55e;"></div>DeepConvNet</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #ef4444;"></div>ShallowConvNet</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #facc15;"></div>ViT</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #c084fc;"></div>EEGConformer</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22d3ee;"></div>LaBraM</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #ec4899;"></div>EEGNetV4</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #84cc16;"></div>BIOT</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #a78bfa;"></div>EEGSurvNet</div>
    </div>
  </div>
</div>

<style>
@keyframes s27ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s27-image-container { 
  animation: s27ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; 
}
.s27-image-effect { 
  transition: transform 0.3s ease-out;
}
.s27-image-effect:hover { 
  transform: scale(1.02); 
}
@keyframes s27ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s27-scan-overlay { 
  animation: s27ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #60a5fa, 0 0 16px rgba(96,165,250,0.5);
}
@keyframes s27BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(96,165,250,0.3), 0 0 12px rgba(96,165,250,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(96,165,250,0.7), 0 0 24px rgba(96,165,250,0.4), 0 0 40px rgba(96,165,250,0.2); }
}
.s27-border-shimmer { animation: s27BorderShimmer 3s ease-in-out infinite; }
@keyframes s27Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #60a5fa; }
}
.s27-corner-1 { animation: s27Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s27-corner-2 { animation: s27Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s27-corner-3 { animation: s27Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s27-corner-4 { animation: s27Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s27RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(96,165,250,0.4); }
  50% { box-shadow: 0 0 12px rgba(96,165,250,0.9), 0 0 20px rgba(96,165,250,0.5); }
}
.s27-rec-badge { animation: s27RecBadge 1.6s ease-in-out infinite; }
@keyframes s27RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #60a5fa, 0 0 8px #60a5fa; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s27-rec-dot { animation: s27RecDot 0.8s ease-in-out infinite; }
@keyframes s27BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s27-badge { animation: s27BadgePulse 2s ease-in-out infinite; }
@keyframes s27StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s27-stage-1 { animation: s27StageGlow 3s ease-in-out infinite; color: #60a5fa; animation-delay: 0s; }
.s27-stage-2 { animation: s27StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s27-stage-3 { animation: s27StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 2s; }
@keyframes s27Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s27-pulse { animation: s27Pulse 1.6s ease-in-out infinite; }
@keyframes s27PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s27-pulse-strong { animation: s27PulseStrong 0.9s ease-in-out infinite; }
@keyframes s27BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s27-blink-text { animation: s27BlinkText 0.9s steps(2, end) infinite; }
@keyframes s27Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s27BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s27-bar-pulse-1, .s27-bar-pulse-2, .s27-bar-pulse-3 { animation: s27BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s27-bar-pulse-1 { color: #60a5fa; animation-delay: 0s; }
.s27-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s27-bar-pulse-3 { color: #fbbf24; animation-delay: -1.6s; }
@keyframes s27BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s27-bar-dot { animation: s27BarDot 1.6s ease-in-out infinite; }
.s27-breathe-1 { animation: s27Breathe 8s ease-in-out infinite; }
.s27-breathe-2 { animation: s27Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s27-breathe-3 { animation: s27Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s27ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s27-scan-line { animation: s27ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-sky-500/8 rounded-full blur-[140px] s28-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s28-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s28-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s28-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s28-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 28 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">ROC </span><span class="bg-gradient-to-r from-sky-300 via-emerald-300 to-amber-300 bg-clip-text text-transparent">Curve</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-sky-400 rounded-full s28-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s28-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-amber-400 rounded-full s28-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s28-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">TPR vs FPR · 9 Models · AUC Benchmark</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s28-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s28-blink-text">AUC=0.816</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ ROC Curves · EEG (Top) vs EEG+Gaze (Bottom) · AUC Bar Chart</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">Dashed line = Random (AUC=0.50)</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s28-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s28-corner-1" style="border-color: #38bdf8;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s28-corner-2" style="border-color: #38bdf8;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s28-corner-3" style="border-color: #38bdf8;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s28-corner-4" style="border-color: #38bdf8;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s28-scan-overlay" style="background: linear-gradient(to right, transparent, #38bdf8, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s28-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s28-rec-badge" style="border-color: rgba(56,189,248,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s28-rec-dot" style="background: #38bdf8;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #38bdf8;">ROC-AUC</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-sky-400/40">
            <div class="text-[7px] font-mono text-sky-300 tracking-wider">9 MODELS · TPR vs FPR</div>
          </div>
          <img src="/roc-curve.png" alt="ROC Curve EEG Models" class="block w-full h-full object-contain rounded shadow-lg s28-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📈</div>
            <div>Place image at: <span class="text-emerald-300">public/roc-curve.png</span></div>
            <div class="text-[8px] text-slate-600">ROC Curve - EEG Models Benchmark</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ My Model · AUC Performance</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-sky-400/60 rounded-md p-1.5 bg-sky-950/20 relative s28-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-sky-500 border border-sky-200 flex items-center justify-center text-[8px] font-bold text-white s28-badge">E</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-sky-300 tracking-wider">EEG Only</div>
              <div class="text-[8px] font-mono text-sky-100/90 leading-tight mt-0.5">AUC <span class="text-sky-200 font-bold">0.709</span></div>
              <div class="text-[7.5px] font-mono text-sky-200/70 leading-tight">Beats best baseline (ViT 0.611)</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s28-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s28-badge">★</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">EEG + Gaze</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">AUC <span class="text-emerald-200 font-bold">0.816</span></div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Best overall · Strong discrimination</div>
            </div>
          </div>
          <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 relative s28-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-black s28-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-amber-300 tracking-wider">Fusion Gain</div>
              <div class="text-[8px] font-mono text-amber-100/90 leading-tight mt-0.5">+0.107 AUC · <span class="text-amber-200 font-bold">+15.1%</span></div>
              <div class="text-[7.5px] font-mono text-amber-200/70 leading-tight">Eye-tracking lifts curve</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Baseline Performance</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Best baseline</span> ViT (0.611) · still &lt; My Model EEG</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Most baselines</span> hover near random (~0.50)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">EEGConformer</span> (0.445) · below chance line</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #3b82f6;"></div>My Model</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #facc15;"></div>ViT 0.611</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #f97316;"></div>EEGNetV4 0.566</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22d3ee;"></div>LaBraM 0.553</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22c55e;"></div>DeepConv 0.547</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #84cc16;"></div>BIOT 0.537</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #ef4444;"></div>ShallowConv 0.521</div>
      <div class="flex items-center gap-1"><span class="text-slate-400">- - -</span>Random 0.50</div>
    </div>
  </div>
</div>

<style>
@keyframes s28ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s28-image-container { 
  animation: s28ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; 
}
.s28-image-effect { 
  transition: transform 0.3s ease-out;
}
.s28-image-effect:hover { 
  transform: scale(1.02); 
}
@keyframes s28ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s28-scan-overlay { 
  animation: s28ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #38bdf8, 0 0 16px rgba(56,189,248,0.5);
}
@keyframes s28BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.3), 0 0 12px rgba(56,189,248,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(56,189,248,0.7), 0 0 24px rgba(56,189,248,0.4), 0 0 40px rgba(56,189,248,0.2); }
}
.s28-border-shimmer { animation: s28BorderShimmer 3s ease-in-out infinite; }
@keyframes s28Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #38bdf8; }
}
.s28-corner-1 { animation: s28Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s28-corner-2 { animation: s28Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s28-corner-3 { animation: s28Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s28-corner-4 { animation: s28Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s28RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(56,189,248,0.4); }
  50% { box-shadow: 0 0 12px rgba(56,189,248,0.9), 0 0 20px rgba(56,189,248,0.5); }
}
.s28-rec-badge { animation: s28RecBadge 1.6s ease-in-out infinite; }
@keyframes s28RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #38bdf8, 0 0 8px #38bdf8; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s28-rec-dot { animation: s28RecDot 0.8s ease-in-out infinite; }
@keyframes s28BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s28-badge { animation: s28BadgePulse 2s ease-in-out infinite; }
@keyframes s28StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s28-stage-1 { animation: s28StageGlow 3s ease-in-out infinite; color: #38bdf8; animation-delay: 0s; }
.s28-stage-2 { animation: s28StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s28-stage-3 { animation: s28StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 2s; }
@keyframes s28Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s28-pulse { animation: s28Pulse 1.6s ease-in-out infinite; }
@keyframes s28PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s28-pulse-strong { animation: s28PulseStrong 0.9s ease-in-out infinite; }
@keyframes s28BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s28-blink-text { animation: s28BlinkText 0.9s steps(2, end) infinite; }
@keyframes s28Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s28BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s28-bar-pulse-1, .s28-bar-pulse-2, .s28-bar-pulse-3 { animation: s28BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s28-bar-pulse-1 { color: #38bdf8; animation-delay: 0s; }
.s28-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s28-bar-pulse-3 { color: #fbbf24; animation-delay: -1.6s; }
@keyframes s28BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s28-bar-dot { animation: s28BarDot 1.6s ease-in-out infinite; }
.s28-breathe-1 { animation: s28Breathe 8s ease-in-out infinite; }
.s28-breathe-2 { animation: s28Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s28-breathe-3 { animation: s28Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s28ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s28-scan-line { animation: s28ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-violet-500/8 rounded-full blur-[140px] s29-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s29-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s29-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-emerald-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-emerald-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-emerald-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-emerald-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-emerald-300 to-transparent s29-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-emerald-400 rounded-full s29-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-emerald-400 font-mono">Slide 29 · Results</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Classification </span><span class="bg-gradient-to-r from-violet-300 via-emerald-300 to-amber-300 bg-clip-text text-transparent">Metrics</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-violet-400 rounded-full s29-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-emerald-400 rounded-full s29-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-amber-400 rounded-full s29-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s29-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">6 Metrics · 9 Models · Baselines = EEG Default</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s29-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s29-blink-text">Avg 77.6</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-emerald-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[3.5] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-emerald-500/20 via-emerald-500/5 to-transparent px-2 py-0.5 border-b border-emerald-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-emerald-300">▸ Deep Learning Model Comparison · Precision · Sensitivity · Specificity · Accuracy · F-Measure · MCC</div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-emerald-400/70">Yellow line = Avg Metric</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative w-full h-full s29-image-container">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s29-corner-1" style="border-color: #c084fc;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s29-corner-2" style="border-color: #c084fc;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s29-corner-3" style="border-color: #c084fc;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s29-corner-4" style="border-color: #c084fc;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s29-scan-overlay" style="background: linear-gradient(to right, transparent, #c084fc, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s29-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s29-rec-badge" style="border-color: rgba(192,132,252,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s29-rec-dot" style="background: #c084fc;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #c084fc;">METRICS</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-violet-400/40">
            <div class="text-[7px] font-mono text-violet-300 tracking-wider">9 MODELS · 6 METRICS · ★ AVG LINE</div>
          </div>
          <img src="/model-metrics.png" alt="Model Metrics Comparison" class="block w-full h-full object-contain rounded shadow-lg s29-image-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-8 border-2 border-dashed border-slate-700 rounded-lg">
            <div class="text-[14px] text-emerald-400">📊</div>
            <div>Place image at: <span class="text-emerald-300">public/model-metrics.png</span></div>
            <div class="text-[8px] text-slate-600">Deep Learning Model Comparison Bar Chart</div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.4] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ My Model · Avg Metric</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 min-h-0 justify-center">
          <div class="border border-violet-400/60 rounded-md p-1.5 bg-violet-950/20 relative s29-stage-1">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-violet-500 border border-violet-200 flex items-center justify-center text-[8px] font-bold text-white s29-badge">E</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">EEG Only</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Avg <span class="text-violet-200 font-bold">55.7</span> · Acc <span class="text-violet-200 font-bold">58.0%</span></div>
              <div class="text-[7.5px] font-mono text-violet-200/70 leading-tight">Above all baselines</div>
            </div>
          </div>
          <div class="border border-emerald-400/60 rounded-md p-1.5 bg-emerald-950/20 relative s29-stage-2">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[8px] font-bold text-white s29-badge">★</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">EEG + Gaze</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">Avg <span class="text-emerald-200 font-bold">77.6</span> · Acc <span class="text-emerald-200 font-bold">82.5%</span></div>
              <div class="text-[7.5px] font-mono text-emerald-200/70 leading-tight">Best · Strong on all metrics</div>
            </div>
          </div>
          <div class="border border-amber-400/60 rounded-md p-1.5 bg-amber-950/20 relative s29-stage-3">
            <div class="absolute top-1 left-1 w-5 h-5 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[8px] font-bold text-black s29-badge">↑</div>
            <div class="pl-5">
              <div class="text-[9px] uppercase font-mono font-bold text-amber-300 tracking-wider">Fusion Gain</div>
              <div class="text-[8px] font-mono text-amber-100/90 leading-tight mt-0.5">Avg <span class="text-amber-200 font-bold">+21.9 pp</span></div>
              <div class="text-[7.5px] font-mono text-amber-200/70 leading-tight">Only My Model uses Gaze fusion</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Baseline Comparison</div>
        </div>
        <div class="p-2 flex flex-col gap-1">
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">All baselines</span> use EEG only (their default architecture)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Best baseline</span> ViT (54.1) and EEGNetV4 (52.3)</div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-1 h-1 bg-yellow-400 rounded-full mt-1.5 flex-shrink-0"></div>
            <div class="text-[9px] text-slate-300 leading-tight"><span class="text-yellow-200 font-bold">Near-zero MCC</span> across baselines → poor discrimination</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #7c3aed;"></div>Precision</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #38bdf8;"></div>Sensitivity</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #22c55e;"></div>Specificity</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #f97316;"></div>Accuracy</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #dc2626;"></div>F-Measure</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-sm" style="background: #e879f9;"></div>MCC</div>
      <div class="flex items-center gap-1"><div class="w-3 h-px" style="background: #facc15; border-top: 1px dashed #facc15;"></div>Avg Metric</div>
    </div>
  </div>
</div>

<style>
@keyframes s29ImageEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s29-image-container { 
  animation: s29ImageEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s both; 
}
.s29-image-effect { 
  transition: transform 0.3s ease-out;
}
.s29-image-effect:hover { 
  transform: scale(1.02); 
}
@keyframes s29ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s29-scan-overlay { 
  animation: s29ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #c084fc, 0 0 16px rgba(192,132,252,0.5);
}
@keyframes s29BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(192,132,252,0.3), 0 0 12px rgba(192,132,252,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(192,132,252,0.7), 0 0 24px rgba(192,132,252,0.4), 0 0 40px rgba(192,132,252,0.2); }
}
.s29-border-shimmer { animation: s29BorderShimmer 3s ease-in-out infinite; }
@keyframes s29Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #c084fc; }
}
.s29-corner-1 { animation: s29Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s29-corner-2 { animation: s29Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s29-corner-3 { animation: s29Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s29-corner-4 { animation: s29Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s29RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(192,132,252,0.4); }
  50% { box-shadow: 0 0 12px rgba(192,132,252,0.9), 0 0 20px rgba(192,132,252,0.5); }
}
.s29-rec-badge { animation: s29RecBadge 1.6s ease-in-out infinite; }
@keyframes s29RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #c084fc, 0 0 8px #c084fc; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s29-rec-dot { animation: s29RecDot 0.8s ease-in-out infinite; }
@keyframes s29BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s29-badge { animation: s29BadgePulse 2s ease-in-out infinite; }
@keyframes s29StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.01); }
}
.s29-stage-1 { animation: s29StageGlow 3s ease-in-out infinite; color: #c084fc; animation-delay: 0s; }
.s29-stage-2 { animation: s29StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1s; }
.s29-stage-3 { animation: s29StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 2s; }
@keyframes s29Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s29-pulse { animation: s29Pulse 1.6s ease-in-out infinite; }
@keyframes s29PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s29-pulse-strong { animation: s29PulseStrong 0.9s ease-in-out infinite; }
@keyframes s29BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s29-blink-text { animation: s29BlinkText 0.9s steps(2, end) infinite; }
@keyframes s29Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s29BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s29-bar-pulse-1, .s29-bar-pulse-2, .s29-bar-pulse-3 { animation: s29BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s29-bar-pulse-1 { color: #c084fc; animation-delay: 0s; }
.s29-bar-pulse-2 { color: #34d399; animation-delay: -0.8s; }
.s29-bar-pulse-3 { color: #fbbf24; animation-delay: -1.6s; }
@keyframes s29BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s29-bar-dot { animation: s29BarDot 1.6s ease-in-out infinite; }
.s29-breathe-1 { animation: s29Breathe 8s ease-in-out infinite; }
.s29-breathe-2 { animation: s29Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s29-breathe-3 { animation: s29Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s29ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s29-scan-line { animation: s29ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0 overflow-hidden">
  <div class="absolute top-[-20%] left-[20%] w-[800px] h-[800px] bg-rose-500/15 rounded-full blur-[160px] s30-breathe"></div>
  <div class="absolute bottom-[-20%] right-[10%] w-[700px] h-[700px] bg-amber-500/12 rounded-full blur-[160px] s30-breathe-2"></div>
</div>
<div class="absolute inset-0 opacity-[0.06] overflow-hidden">
  <svg class="w-[200%] h-full s30-eeg" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,450 Q100,420 200,450 T400,440 T600,460 T800,430 T1000,450 T1200,440 T1400,455 T1600,440 T1800,460 T2000,445 T2200,450 T2400,440 T2600,455 T2800,445 T3000,450 T3200,445" stroke="#fb7185" stroke-width="1.2" fill="none"/>
  </svg>
</div>
<div class="absolute inset-0 opacity-[0.04] overflow-hidden">
  <svg class="w-[200%] h-full s30-eeg-2" viewBox="0 0 3200 900" preserveAspectRatio="none">
    <path d="M0,500 Q150,470 300,500 T600,490 T900,510 T1200,480 T1500,500 T1800,490 T2100,505 T2400,490 T2700,510 T3000,495 T3200,500" stroke="#fbbf24" stroke-width="1" fill="none"/>
  </svg>
</div>
<div class="absolute inset-0 pointer-events-none">
  <div class="absolute top-[15%] left-[10%] w-1 h-1 bg-rose-400 rounded-full s30-particle-1"></div>
  <div class="absolute top-[25%] left-[85%] w-1.5 h-1.5 bg-amber-300 rounded-full s30-particle-2"></div>
  <div class="absolute top-[75%] left-[12%] w-1 h-1 bg-rose-400 rounded-full s30-particle-3"></div>
  <div class="absolute top-[80%] left-[88%] w-1.5 h-1.5 bg-amber-400 rounded-full s30-particle-1"></div>
  <div class="absolute top-[40%] left-[5%] w-1 h-1 bg-rose-300 rounded-full s30-particle-2"></div>
  <div class="absolute top-[55%] left-[92%] w-1 h-1 bg-amber-300 rounded-full s30-particle-3"></div>
  <div class="absolute top-[10%] left-[50%] w-1 h-1 bg-yellow-300 rounded-full s30-particle-2"></div>
  <div class="absolute top-[90%] left-[48%] w-1 h-1 bg-rose-300 rounded-full s30-particle-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-rose-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-8 h-8 border-l-2 border-t-2 border-rose-400 opacity-60 s30-bracket-1"></div>
<div class="absolute top-6 right-6 w-8 h-8 border-r-2 border-t-2 border-rose-400 opacity-60 s30-bracket-1"></div>
<div class="absolute bottom-6 left-6 w-8 h-8 border-l-2 border-b-2 border-amber-400 opacity-60 s30-bracket-2"></div>
<div class="absolute bottom-6 right-6 w-8 h-8 border-r-2 border-b-2 border-amber-400 opacity-60 s30-bracket-2"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-15">
  <div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-rose-300 to-transparent s30-scan-line"></div>
</div>
<div class="relative z-10 h-full flex flex-col">
  <div class="flex items-center justify-between px-16 py-4 s30-fade-in">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-rose-400 rounded-full s30-strong-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-rose-400 font-mono">Section 04 · Closing</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex-1 flex flex-col items-center justify-center px-16">
    <div class="flex flex-col items-center">
      <div class="relative flex items-center justify-center mb-3 s30-number-wrap">
        <div class="absolute w-[180px] h-[180px] rounded-full bg-rose-500/10 blur-3xl s30-aura"></div>
        <div class="absolute w-[120px] h-[120px] rounded-full border border-rose-400/20 s30-ring-1"></div>
        <div class="absolute w-[155px] h-[155px] rounded-full border border-amber-400/15 s30-ring-2"></div>
        <div class="absolute w-[190px] h-[190px] rounded-full border border-yellow-400/10 s30-ring-3"></div>
        <div class="relative flex items-baseline">
          <span class="text-[5.5rem] font-black leading-none tracking-tighter bg-gradient-to-b from-rose-300 via-amber-400 to-rose-700 bg-clip-text text-transparent s30-number-glow">04</span>
          <span class="text-[1.6rem] font-mono text-slate-600 ml-2">/04</span>
        </div>
      </div>
      <div class="text-center s30-label-wrap">
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight s30-title">
          <span class="bg-gradient-to-r from-white via-rose-200 to-white bg-clip-text text-transparent">SUMMARY</span>
        </h1>
        <h1 class="!text-[2.6rem] !leading-[1] !font-black !m-0 tracking-tight mt-1 s30-title-2">
          <span class="bg-gradient-to-r from-rose-400 via-amber-400 to-yellow-400 bg-clip-text text-transparent">&amp; OUTLOOK</span>
        </h1>
        <div class="mt-4 max-w-2xl mx-auto s30-subtitle">
          <div class="text-[12px] text-slate-400 font-mono leading-relaxed">
            <span class="text-rose-300">Key contributions</span> · <span class="text-amber-300">Multimodal fusion gains</span> · <span class="text-yellow-300">Future directions</span>
          </div>
        </div>
      </div>
      <div class="flex items-center justify-center gap-2 mt-4 s30-dots">
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2 h-2 rounded-full bg-slate-700"></div>
        <div class="w-2.5 h-2.5 rounded-full bg-rose-400 s30-active-dot"></div>
      </div>
    </div>
  </div>
  <div class="flex items-center justify-between px-16 py-4 s30-fade-in-last">
    <div class="flex items-center gap-2">
      <div class="w-1.5 h-1.5 bg-rose-400 rounded-full s30-strong-pulse"></div>
      <div class="text-[9px] uppercase tracking-[0.3em] text-rose-400/70 font-mono">Final Section</div>
    </div>
    <div class="flex items-center gap-2">
      <div class="text-[9px] uppercase tracking-[0.3em] text-slate-500 font-mono">Conclusion · Contributions · Future Work</div>
      <div class="w-1.5 h-1.5 bg-amber-400 rounded-full s30-strong-pulse"></div>
    </div>
  </div>
</div>

<style>
@keyframes s30Breathe {
  0%, 100% { opacity: 0.85; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.06); }
}
.s30-breathe { animation: s30Breathe 9s ease-in-out infinite; }
.s30-breathe-2 { animation: s30Breathe 11s ease-in-out infinite; animation-delay: -3s; }
@keyframes s30Eeg {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
.s30-eeg { animation: s30Eeg 30s linear infinite; }
.s30-eeg-2 { animation: s30Eeg 22s linear infinite reverse; }
@keyframes s30FadeIn {
  0% { opacity: 0; transform: translateY(-10px); }
  100% { opacity: 1; transform: translateY(0); }
}
.s30-fade-in { animation: s30FadeIn 0.8s ease-out 0s both; }
.s30-fade-in-last { animation: s30FadeIn 0.8s ease-out 2.5s both; }
@keyframes s30NumberWrap {
  0% { opacity: 0; transform: scale(0.8) translateY(20px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s30-number-wrap { animation: s30NumberWrap 1.2s cubic-bezier(0.16, 1, 0.3, 1) 0.3s both; }
@keyframes s30NumberGlow {
  0%, 100% { filter: drop-shadow(0 0 12px rgba(251,113,133,0.4)) drop-shadow(0 0 24px rgba(251,113,133,0.2)); }
  50% { filter: drop-shadow(0 0 20px rgba(251,113,133,0.7)) drop-shadow(0 0 40px rgba(251,191,36,0.4)); }
}
.s30-number-glow { animation: s30NumberGlow 4s ease-in-out infinite; }
@keyframes s30Aura {
  0%, 100% { opacity: 0.6; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.15); }
}
.s30-aura { animation: s30Aura 4s ease-in-out infinite; }
@keyframes s30Ring1 { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
.s30-ring-1 { animation: s30Ring1 40s linear infinite; }
.s30-ring-2 { animation: s30Ring1 60s linear infinite reverse; }
.s30-ring-3 { animation: s30Ring1 80s linear infinite; }
@keyframes s30LabelWrap {
  0% { opacity: 0; transform: translateY(15px); }
  100% { opacity: 1; transform: translateY(0); }
}
.s30-label-wrap { animation: s30LabelWrap 1s ease-out 1s both; }
@keyframes s30Title {
  0% { opacity: 0; letter-spacing: 0.5em; }
  100% { opacity: 1; letter-spacing: -0.025em; }
}
.s30-title { animation: s30Title 1.2s cubic-bezier(0.16, 1, 0.3, 1) 1.2s both; }
.s30-title-2 { animation: s30Title 1.2s cubic-bezier(0.16, 1, 0.3, 1) 1.5s both; }
@keyframes s30Subtitle {
  0% { opacity: 0; transform: translateY(10px); }
  100% { opacity: 1; transform: translateY(0); }
}
.s30-subtitle { animation: s30Subtitle 1s ease-out 2s both; }
@keyframes s30Dots {
  0% { opacity: 0; }
  100% { opacity: 1; }
}
.s30-dots { animation: s30Dots 1s ease-out 2.3s both; }
@keyframes s30ActiveDot {
  0%, 100% { box-shadow: 0 0 8px #fb7185, 0 0 16px rgba(251,113,133,0.6); transform: scale(1); }
  50% { box-shadow: 0 0 16px #fb7185, 0 0 28px rgba(251,113,133,0.9), 0 0 40px rgba(251,191,36,0.4); transform: scale(1.15); }
}
.s30-active-dot { animation: s30ActiveDot 1.6s ease-in-out infinite; }
@keyframes s30StrongPulse {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px currentColor, 0 0 12px rgba(251,113,133,0.5); }
  50% { opacity: 0.4; box-shadow: 0 0 0 transparent; }
}
.s30-strong-pulse { animation: s30StrongPulse 1.4s ease-in-out infinite; }
@keyframes s30Particle {
  0%, 100% { opacity: 0.3; transform: translate(0, 0) scale(1); }
  50% { opacity: 1; transform: translate(8px, -8px) scale(1.4); }
}
.s30-particle-1 { animation: s30Particle 4s ease-in-out infinite; }
.s30-particle-2 { animation: s30Particle 5s ease-in-out infinite; animation-delay: -1s; }
.s30-particle-3 { animation: s30Particle 6s ease-in-out infinite; animation-delay: -2s; }
@keyframes s30Bracket {
  0%, 100% { opacity: 0.4; }
  50% { opacity: 0.9; box-shadow: 0 0 8px currentColor; }
}
.s30-bracket-1 { animation: s30Bracket 2.4s ease-in-out infinite; color: #fb7185; }
.s30-bracket-2 { animation: s30Bracket 2.4s ease-in-out infinite; color: #fbbf24; animation-delay: -1.2s; }
@keyframes s30ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s30-scan-line { animation: s30ScanLine 8s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s31-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s31-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s31-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-rose-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-rose-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-rose-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-amber-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-amber-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-rose-300 to-transparent s31-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-rose-400 rounded-full s31-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-rose-400 font-mono">Slide 31 · Summary</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Validation for </span><span class="bg-gradient-to-r from-rose-300 via-amber-300 to-emerald-300 bg-clip-text text-transparent">Research Proposal</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-rose-400 rounded-full s31-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-amber-400 rounded-full s31-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-emerald-400 rounded-full s31-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s31-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Pre-Experiment Outcomes · Lab → Field Readiness</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s31-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s31-blink-text">Validated</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-3 min-h-0 mt-1">
    <div class="border border-rose-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[2.6] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-rose-500/20 via-rose-500/5 to-transparent px-2 py-0.5 border-b border-rose-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-rose-300">▸ Key Validation Outcomes</div>
        <div class="flex-1 h-px bg-gradient-to-r from-rose-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-rose-400/70">4 Strategic Findings</div>
      </div>
      <div class="p-3 flex-1 flex flex-col gap-2 min-h-0 justify-center">
        <div class="border border-rose-400/60 rounded-md p-2 bg-rose-950/20 relative s31-stage-1">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-rose-500 border border-rose-200 flex items-center justify-center text-[10px] font-bold text-white s31-badge">1</div>
          <div class="pl-9">
            <div class="text-[10px] uppercase font-mono font-bold text-rose-300 tracking-wider">Technical Feasibility</div>
            <div class="text-[10px] text-slate-200 leading-snug mt-0.5">Demonstrates technical feasibility of <span class="text-rose-200 font-bold">cross-scenario vigilance detection</span></div>
          </div>
        </div>
        <div class="border border-amber-400/60 rounded-md p-2 bg-amber-950/20 relative s31-stage-2">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-amber-500 border border-amber-200 flex items-center justify-center text-[10px] font-bold text-black s31-badge">2</div>
          <div class="pl-9">
            <div class="text-[10px] uppercase font-mono font-bold text-amber-300 tracking-wider">Lab → Real Operations</div>
            <div class="text-[10px] text-slate-200 leading-snug mt-0.5">Ready pipeline proves concept can move from <span class="text-amber-200 font-bold">lab (PVT)</span> to <span class="text-amber-200 font-bold">real operations (UGV/UAV)</span></div>
          </div>
        </div>
        <div class="border border-emerald-400/60 rounded-md p-2 bg-emerald-950/20 relative s31-stage-3">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-emerald-500 border border-emerald-200 flex items-center justify-center text-[10px] font-bold text-white s31-badge">3</div>
          <div class="pl-9">
            <div class="text-[10px] uppercase font-mono font-bold text-emerald-300 tracking-wider">Strong Foundation · Risk Mitigated</div>
            <div class="text-[10px] text-slate-200 leading-snug mt-0.5">Foundation for <span class="text-emerald-200 font-bold">larger datasets &amp; real-time deployment</span> · Pre-experiment handles <span class="text-emerald-200">data heterogeneity, artifacts, domain shift</span></div>
          </div>
        </div>
        <div class="border-2 border-yellow-400/80 rounded-md p-2 bg-gradient-to-br from-yellow-950/40 to-amber-950/30 relative s31-stage-4 s31-conclusion">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-yellow-400 border-2 border-yellow-100 flex items-center justify-center text-[10px] font-bold text-black s31-badge-conclusion">★</div>
          <div class="pl-9">
            <div class="text-[10px] uppercase font-mono font-black text-yellow-300 tracking-wider flex items-center gap-1">Conclusion <span class="text-yellow-500/70">›</span> <span class="text-emerald-300">Highly Viable</span></div>
            <div class="text-[10px] text-slate-100 leading-snug mt-0.5 font-semibold">Proposal is <span class="text-yellow-200 font-bold">highly viable</span> — proceed to <span class="text-emerald-200 font-bold">full-scale study with confidence</span></div>
          </div>
        </div>
      </div>
    </div>
    <div class="border border-amber-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-amber-500/20 via-amber-500/5 to-transparent px-2 py-0.5 border-b border-amber-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-amber-300">▸ Field Demo</div>
        <div class="flex-1 h-px bg-gradient-to-r from-amber-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-amber-400/70">Live</div>
      </div>
      <div class="flex-1 p-2 min-h-0 flex items-center justify-center bg-black relative">
        <div class="relative h-full s31-video-container" style="aspect-ratio: 9/16;">
          <div class="absolute -top-1 -left-1 w-4 h-4 border-l-2 border-t-2 z-10 s31-corner-1" style="border-color: #fbbf24;"></div>
          <div class="absolute -top-1 -right-1 w-4 h-4 border-r-2 border-t-2 z-10 s31-corner-2" style="border-color: #fbbf24;"></div>
          <div class="absolute -bottom-1 -left-1 w-4 h-4 border-l-2 border-b-2 z-10 s31-corner-3" style="border-color: #fbbf24;"></div>
          <div class="absolute -bottom-1 -right-1 w-4 h-4 border-r-2 border-b-2 z-10 s31-corner-4" style="border-color: #fbbf24;"></div>
          <div class="absolute inset-0 pointer-events-none overflow-hidden rounded z-20">
            <div class="absolute left-0 right-0 h-[3px] opacity-60 s31-scan-overlay" style="background: linear-gradient(to right, transparent, #fbbf24, transparent);"></div>
          </div>
          <div class="absolute inset-0 pointer-events-none rounded z-20 s31-border-shimmer"></div>
          <div class="absolute top-2 right-2 z-30 flex items-center gap-1 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border s31-rec-badge" style="border-color: rgba(251,191,36,0.4);">
            <div class="w-1.5 h-1.5 rounded-full s31-rec-dot" style="background: #ef4444;"></div>
            <div class="text-[7px] font-mono font-bold tracking-wider" style="color: #fbbf24;">REC</div>
          </div>
          <div class="absolute bottom-2 left-2 z-30 bg-black/60 backdrop-blur-sm rounded px-1.5 py-0.5 border border-amber-400/40">
            <div class="text-[7px] font-mono text-amber-300 tracking-wider">TELEOPERATION</div>
          </div>
          <video src="/teleoperation-video.mp4" autoplay loop muted playsinline class="block w-full h-full object-cover rounded shadow-lg s31-video-effect" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
            Video not supported
          </video>
          <div class="hidden flex-col items-center justify-center gap-2 text-slate-500 font-mono text-[10px] p-4 border-2 border-dashed border-slate-700 rounded-lg h-full">
            <div class="text-[14px] text-amber-400">🎬</div>
            <div class="text-center">Place video at:</div>
            <div class="text-amber-300 text-center text-[8px]">public/teleoperation-video.mp4</div>
            <div class="text-[7px] text-slate-600 text-center">Portrait · Field Demo</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Feasibility</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-amber-400 rounded-sm"></div>Lab → Field</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Foundation</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>★ Conclusion</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-red-500 rounded-full"></div>Live Demo</div>
    </div>
  </div>
</div>

<style>
@keyframes s31VideoEntry {
  0% { opacity: 0; transform: scale(0.92) translateY(10px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
.s31-video-container { 
  animation: s31VideoEntry 1s cubic-bezier(0.16, 1, 0.3, 1) 0.5s both; 
}
.s31-video-effect { 
  transition: transform 0.3s ease-out;
}
.s31-video-effect:hover { 
  transform: scale(1.02); 
}
@keyframes s31ScanOverlay {
  0%, 100% { top: 0%; opacity: 0; }
  10% { opacity: 0.8; }
  90% { opacity: 0.8; }
  100% { top: 100%; opacity: 0; }
}
.s31-scan-overlay { 
  animation: s31ScanOverlay 4s ease-in-out infinite;
  box-shadow: 0 0 8px #fbbf24, 0 0 16px rgba(251,191,36,0.5);
}
@keyframes s31BorderShimmer {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(251,191,36,0.3), 0 0 12px rgba(251,191,36,0.15); }
  50% { box-shadow: inset 0 0 0 1px rgba(251,191,36,0.7), 0 0 24px rgba(251,191,36,0.4), 0 0 40px rgba(251,191,36,0.2); }
}
.s31-border-shimmer { animation: s31BorderShimmer 3s ease-in-out infinite; }
@keyframes s31Corner {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); box-shadow: 0 0 8px #fbbf24; }
}
.s31-corner-1 { animation: s31Corner 2.4s ease-in-out infinite; transform-origin: top left; animation-delay: 0s; }
.s31-corner-2 { animation: s31Corner 2.4s ease-in-out infinite; transform-origin: top right; animation-delay: -0.6s; }
.s31-corner-3 { animation: s31Corner 2.4s ease-in-out infinite; transform-origin: bottom left; animation-delay: -1.2s; }
.s31-corner-4 { animation: s31Corner 2.4s ease-in-out infinite; transform-origin: bottom right; animation-delay: -1.8s; }
@keyframes s31RecBadge {
  0%, 100% { box-shadow: 0 0 4px rgba(251,191,36,0.4); }
  50% { box-shadow: 0 0 12px rgba(251,191,36,0.9), 0 0 20px rgba(239,68,68,0.5); }
}
.s31-rec-badge { animation: s31RecBadge 1.6s ease-in-out infinite; }
@keyframes s31RecDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 4px #ef4444, 0 0 8px #ef4444; transform: scale(1); }
  50% { opacity: 0.3; box-shadow: 0 0 0 transparent; transform: scale(0.7); }
}
.s31-rec-dot { animation: s31RecDot 0.8s ease-in-out infinite; }
@keyframes s31BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.15); box-shadow: 0 0 12px currentColor; }
}
.s31-badge { animation: s31BadgePulse 2s ease-in-out infinite; }
@keyframes s31BadgeConclusion {
  0%, 100% { transform: scale(1) rotate(0deg); box-shadow: 0 0 8px #facc15, 0 0 16px rgba(250,204,21,0.4); }
  50% { transform: scale(1.2) rotate(180deg); box-shadow: 0 0 16px #facc15, 0 0 28px rgba(250,204,21,0.8), 0 0 40px rgba(34,197,94,0.3); }
}
.s31-badge-conclusion { animation: s31BadgeConclusion 2.4s ease-in-out infinite; }
@keyframes s31StageGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; transform: scale(1); }
  50% { box-shadow: 0 0 14px currentColor, inset 0 0 8px rgba(255,255,255,0.05); transform: scale(1.005); }
}
.s31-stage-1 { animation: s31StageGlow 3s ease-in-out infinite; color: #fb7185; animation-delay: 0s; }
.s31-stage-2 { animation: s31StageGlow 3s ease-in-out infinite; color: #fbbf24; animation-delay: 0.7s; }
.s31-stage-3 { animation: s31StageGlow 3s ease-in-out infinite; color: #34d399; animation-delay: 1.4s; }
.s31-stage-4 { animation: s31StageGlow 3s ease-in-out infinite; color: #facc15; animation-delay: 2.1s; }
@keyframes s31Conclusion {
  0%, 100% { box-shadow: 0 0 16px rgba(250,204,21,0.3), 0 0 32px rgba(34,197,94,0.15), inset 0 0 12px rgba(250,204,21,0.05); }
  50% { box-shadow: 0 0 28px rgba(250,204,21,0.6), 0 0 56px rgba(34,197,94,0.3), inset 0 0 20px rgba(250,204,21,0.1); }
}
.s31-conclusion { animation: s31Conclusion 3s ease-in-out infinite; }
@keyframes s31Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s31-pulse { animation: s31Pulse 1.6s ease-in-out infinite; }
@keyframes s31PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s31-pulse-strong { animation: s31PulseStrong 0.9s ease-in-out infinite; }
@keyframes s31BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s31-blink-text { animation: s31BlinkText 0.9s steps(2, end) infinite; }
@keyframes s31Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s31BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s31-bar-pulse-1, .s31-bar-pulse-2, .s31-bar-pulse-3 { animation: s31BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s31-bar-pulse-1 { color: #fb7185; animation-delay: 0s; }
.s31-bar-pulse-2 { color: #fbbf24; animation-delay: -0.8s; }
.s31-bar-pulse-3 { color: #34d399; animation-delay: -1.6s; }
@keyframes s31BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s31-bar-dot { animation: s31BarDot 1.6s ease-in-out infinite; }
.s31-breathe-1 { animation: s31Breathe 8s ease-in-out infinite; }
.s31-breathe-2 { animation: s31Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s31-breathe-3 { animation: s31Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s31ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s31-scan-line { animation: s31ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s32-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s32-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s32-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-rose-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-rose-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-rose-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-amber-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-amber-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-rose-300 to-transparent s32-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-rose-400 rounded-full s32-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-rose-400 font-mono">Slide 32 · Summary</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Full-Scale </span><span class="bg-gradient-to-r from-rose-300 via-amber-300 to-emerald-300 bg-clip-text text-transparent">Experiment Plan</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-rose-400 rounded-full s32-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-amber-400 rounded-full s32-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-emerald-400 rounded-full s32-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s32-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">Data Collection · 8 Subjects · 2 Sessions · 3 Scenarios</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s32-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s32-blink-text">Ready</div>
      </div>
    </div>
  </div>
  <div class="grid grid-cols-4 gap-2 mt-1">
    <div class="border border-rose-400/50 rounded-lg bg-rose-950/20 p-2 relative overflow-hidden s32-stat-card">
      <div class="absolute top-0 right-0 w-16 h-16 bg-rose-500/10 rounded-full blur-2xl"></div>
      <div class="relative flex items-center gap-2">
        <div class="text-[2rem] font-black leading-none bg-gradient-to-b from-rose-200 to-rose-500 bg-clip-text text-transparent s32-number">8</div>
        <div class="flex-1">
          <div class="text-[8px] uppercase font-mono font-bold text-rose-300 tracking-wider">Subjects</div>
          <div class="text-[8px] font-mono text-rose-100/80 leading-tight">Including PI</div>
        </div>
      </div>
    </div>
    <div class="border border-amber-400/50 rounded-lg bg-amber-950/20 p-2 relative overflow-hidden s32-stat-card" style="animation-delay: 0.15s;">
      <div class="absolute top-0 right-0 w-16 h-16 bg-amber-500/10 rounded-full blur-2xl"></div>
      <div class="relative flex items-center gap-2">
        <div class="text-[2rem] font-black leading-none bg-gradient-to-b from-amber-200 to-amber-500 bg-clip-text text-transparent s32-number">2</div>
        <div class="flex-1">
          <div class="text-[8px] uppercase font-mono font-bold text-amber-300 tracking-wider">Sessions</div>
          <div class="text-[8px] font-mono text-amber-100/80 leading-tight">Per subject</div>
        </div>
      </div>
    </div>
    <div class="border border-emerald-400/50 rounded-lg bg-emerald-950/20 p-2 relative overflow-hidden s32-stat-card" style="animation-delay: 0.3s;">
      <div class="absolute top-0 right-0 w-16 h-16 bg-emerald-500/10 rounded-full blur-2xl"></div>
      <div class="relative flex items-center gap-2">
        <div class="text-[2rem] font-black leading-none bg-gradient-to-b from-emerald-200 to-emerald-500 bg-clip-text text-transparent s32-number">3</div>
        <div class="flex-1">
          <div class="text-[8px] uppercase font-mono font-bold text-emerald-300 tracking-wider">Scenarios</div>
          <div class="text-[8px] font-mono text-emerald-100/80 leading-tight">PVT · UGV · UAV</div>
        </div>
      </div>
    </div>
    <div class="border border-cyan-400/50 rounded-lg bg-cyan-950/20 p-2 relative overflow-hidden s32-stat-card" style="animation-delay: 0.45s;">
      <div class="absolute top-0 right-0 w-16 h-16 bg-cyan-500/10 rounded-full blur-2xl"></div>
      <div class="relative flex items-center gap-2">
        <div class="text-[2rem] font-black leading-none bg-gradient-to-b from-cyan-200 to-cyan-500 bg-clip-text text-transparent s32-number">64</div>
        <div class="flex-1">
          <div class="text-[8px] uppercase font-mono font-bold text-cyan-300 tracking-wider">EEG Channels</div>
          <div class="text-[8px] font-mono text-cyan-100/80 leading-tight">Full montage</div>
        </div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-2">
    <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1.8] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-violet-500/20 via-violet-500/5 to-transparent px-2 py-0.5 border-b border-violet-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-violet-300">▸ Protocol Structure · Per Subject</div>
        <div class="flex-1 h-px bg-gradient-to-r from-violet-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-violet-400/70">Hierarchy</div>
      </div>
      <div class="p-3 flex-1 flex flex-col justify-center gap-1.5">
        <div class="flex items-center gap-2 s32-row-1">
          <div class="flex items-center gap-1.5 w-[88px]">
            <div class="w-5 h-5 rounded bg-rose-500/80 flex items-center justify-center text-[9px] font-bold text-white">S</div>
            <div class="text-[9px] font-mono text-rose-300 font-bold">Subject</div>
          </div>
          <div class="flex-1 relative h-6 bg-rose-950/40 rounded border border-rose-400/40 flex items-center justify-center">
            <div class="absolute inset-0 bg-gradient-to-r from-rose-500/20 to-transparent rounded"></div>
            <div class="relative text-[9px] font-mono text-rose-100 font-bold">1 Subject</div>
          </div>
        </div>
        <div class="flex items-center gap-1 text-violet-400/70 text-[11px] pl-[100px]">└─</div>
        <div class="flex items-center gap-2 s32-row-2">
          <div class="flex items-center gap-1.5 w-[88px]">
            <div class="w-5 h-5 rounded bg-amber-500/80 flex items-center justify-center text-[9px] font-bold text-white">×2</div>
            <div class="text-[9px] font-mono text-amber-300 font-bold">Sessions</div>
          </div>
          <div class="flex-1 grid grid-cols-2 gap-1">
            <div class="h-6 bg-amber-950/40 rounded border border-amber-400/40 flex items-center justify-center text-[9px] font-mono text-amber-200">Session 1</div>
            <div class="h-6 bg-amber-950/40 rounded border border-amber-400/40 flex items-center justify-center text-[9px] font-mono text-amber-200">Session 2</div>
          </div>
        </div>
        <div class="flex items-center gap-1 text-violet-400/70 text-[11px] pl-[100px]">└─</div>
        <div class="flex items-center gap-2 s32-row-3">
          <div class="flex items-center gap-1.5 w-[88px]">
            <div class="w-5 h-5 rounded bg-emerald-500/80 flex items-center justify-center text-[9px] font-bold text-white">×3</div>
            <div class="text-[9px] font-mono text-emerald-300 font-bold">Scenarios</div>
          </div>
          <div class="flex-1 grid grid-cols-3 gap-1">
            <div class="h-6 bg-violet-950/40 rounded border border-violet-400/40 flex items-center justify-center text-[9px] font-mono text-violet-200 font-bold">PVT</div>
            <div class="h-6 bg-cyan-950/40 rounded border border-cyan-400/40 flex items-center justify-center text-[9px] font-mono text-cyan-200 font-bold">UGV</div>
            <div class="h-6 bg-orange-950/40 rounded border border-orange-400/40 flex items-center justify-center text-[9px] font-mono text-orange-200 font-bold">UAV</div>
          </div>
        </div>
        <div class="flex items-center gap-1 text-violet-400/70 text-[11px] pl-[100px]">└─</div>
        <div class="flex items-center gap-2 s32-row-4">
          <div class="flex items-center gap-1.5 w-[88px]">
            <div class="w-5 h-5 rounded bg-yellow-500/80 flex items-center justify-center text-[9px] font-bold text-black">★</div>
            <div class="text-[9px] font-mono text-yellow-300 font-bold">Trials</div>
          </div>
          <div class="flex-1 relative h-6 bg-yellow-950/40 rounded border border-yellow-400/40 flex items-center justify-center overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-yellow-500/20 rounded s32-trial-shimmer"></div>
            <div class="relative text-[9px] font-mono text-yellow-100 font-bold">200 Trials · per Scenario</div>
          </div>
        </div>
        <div class="mt-2 border border-yellow-400/50 rounded-md bg-gradient-to-r from-yellow-950/40 via-amber-950/30 to-yellow-950/40 p-1.5 s32-total-card">
          <div class="flex items-center justify-between">
            <div class="text-[9px] uppercase font-mono font-bold text-yellow-300 tracking-wider flex items-center gap-1">
              <span>∑</span> Total Trials · Per Subject
            </div>
            <div class="text-[11px] font-mono font-black text-yellow-100">2 × 3 × 200 = <span class="text-yellow-300">1,200</span></div>
          </div>
          <div class="flex items-center justify-between mt-0.5">
            <div class="text-[8px] font-mono text-amber-300/80">Dataset Total · All Subjects</div>
            <div class="text-[10px] font-mono font-black text-emerald-300">8 × 1,200 = <span class="text-emerald-200">9,600 trials</span></div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1] min-h-0">
      <div class="border border-cyan-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-1 flex flex-col min-h-0">
        <div class="bg-gradient-to-r from-cyan-500/20 via-cyan-500/5 to-transparent px-2 py-0.5 border-b border-cyan-400/30 flex-shrink-0">
          <div class="text-[10px] font-mono font-bold text-cyan-300">▸ Scheduling · Flexible</div>
        </div>
        <div class="p-2 flex-1 flex flex-col gap-1.5 justify-center">
          <div class="flex items-start gap-1.5">
            <div class="w-5 h-5 rounded-full bg-cyan-500/80 flex items-center justify-center text-[9px] font-bold text-white flex-shrink-0 mt-0.5 s32-icon">⏰</div>
            <div>
              <div class="text-[9px] uppercase font-mono font-bold text-cyan-300 tracking-wider">Subject-Driven Timing</div>
              <div class="text-[8px] font-mono text-cyan-100/90 leading-tight mt-0.5">Experiment timing adapts to subject availability and preference</div>
            </div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-5 h-5 rounded-full bg-violet-500/80 flex items-center justify-center text-[9px] font-bold text-white flex-shrink-0 mt-0.5 s32-icon" style="animation-delay: 0.5s;">🗓</div>
            <div>
              <div class="text-[9px] uppercase font-mono font-bold text-violet-300 tracking-wider">Session Gap</div>
              <div class="text-[8px] font-mono text-violet-100/90 leading-tight mt-0.5">Session 2 scheduled on different time for cross-session analysis</div>
            </div>
          </div>
          <div class="flex items-start gap-1.5">
            <div class="w-5 h-5 rounded-full bg-emerald-500/80 flex items-center justify-center text-[9px] font-bold text-white flex-shrink-0 mt-0.5 s32-icon" style="animation-delay: 1s;">✓</div>
            <div>
              <div class="text-[9px] uppercase font-mono font-bold text-emerald-300 tracking-wider">Breaks Between</div>
              <div class="text-[8px] font-mono text-emerald-100/90 leading-tight mt-0.5">Short rest between scenarios to prevent fatigue bleed</div>
            </div>
          </div>
        </div>
      </div>
      <div class="border border-yellow-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0">
        <div class="bg-gradient-to-r from-yellow-500/20 via-yellow-500/5 to-transparent px-2 py-0.5 border-b border-yellow-400/30">
          <div class="text-[10px] font-mono font-bold text-yellow-300">▸ Data Acquisition</div>
        </div>
        <div class="p-2 grid grid-cols-2 gap-1.5">
          <div class="border border-cyan-400/40 rounded bg-cyan-950/30 px-1.5 py-1 text-center">
            <div class="text-[12px] font-bold text-cyan-300 leading-none">64ch</div>
            <div class="text-[7px] font-mono text-cyan-200/80 mt-0.5">EEG Montage</div>
          </div>
          <div class="border border-rose-400/40 rounded bg-rose-950/30 px-1.5 py-1 text-center">
            <div class="text-[12px] font-bold text-rose-300 leading-none">90Hz</div>
            <div class="text-[7px] font-mono text-rose-200/80 mt-0.5">Eye Tracker</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Subjects</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-amber-400 rounded-sm"></div>Sessions</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Scenarios</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>Trials</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-cyan-400 rounded-sm"></div>64ch EEG</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-violet-400 rounded-sm"></div>Flexible Schedule</div>
    </div>
  </div>
</div>

<style>
@keyframes s32StatCard {
  0% { opacity: 0; transform: translateY(10px) scale(0.95); }
  100% { opacity: 1; transform: translateY(0) scale(1); }
}
.s32-stat-card { animation: s32StatCard 0.6s cubic-bezier(0.16, 1, 0.3, 1) both; }
@keyframes s32Number {
  0%, 100% { filter: drop-shadow(0 0 4px currentColor); }
  50% { filter: drop-shadow(0 0 12px currentColor) drop-shadow(0 0 20px currentColor); }
}
.s32-number { animation: s32Number 3s ease-in-out infinite; }
@keyframes s32RowIn {
  0% { opacity: 0; transform: translateX(-20px); }
  100% { opacity: 1; transform: translateX(0); }
}
.s32-row-1 { animation: s32RowIn 0.6s ease-out 0.8s both; }
.s32-row-2 { animation: s32RowIn 0.6s ease-out 1.0s both; }
.s32-row-3 { animation: s32RowIn 0.6s ease-out 1.2s both; }
.s32-row-4 { animation: s32RowIn 0.6s ease-out 1.4s both; }
@keyframes s32TrialShimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}
.s32-trial-shimmer { animation: s32TrialShimmer 2.5s linear infinite; }
@keyframes s32TotalCard {
  0%, 100% { box-shadow: 0 0 8px rgba(250,204,21,0.2), inset 0 0 4px rgba(250,204,21,0.05); }
  50% { box-shadow: 0 0 20px rgba(250,204,21,0.5), 0 0 32px rgba(34,197,94,0.2), inset 0 0 8px rgba(250,204,21,0.08); }
}
.s32-total-card { animation: s32TotalCard 3s ease-in-out infinite; }
@keyframes s32Icon {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.15); box-shadow: 0 0 8px currentColor; }
}
.s32-icon { animation: s32Icon 2s ease-in-out infinite; }
@keyframes s32Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s32-pulse { animation: s32Pulse 1.6s ease-in-out infinite; }
@keyframes s32PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s32-pulse-strong { animation: s32PulseStrong 0.9s ease-in-out infinite; }
@keyframes s32BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s32-blink-text { animation: s32BlinkText 0.9s steps(2, end) infinite; }
@keyframes s32Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s32BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s32-bar-pulse-1, .s32-bar-pulse-2, .s32-bar-pulse-3 { animation: s32BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s32-bar-pulse-1 { color: #fb7185; animation-delay: 0s; }
.s32-bar-pulse-2 { color: #fbbf24; animation-delay: -0.8s; }
.s32-bar-pulse-3 { color: #34d399; animation-delay: -1.6s; }
@keyframes s32BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s32-bar-dot { animation: s32BarDot 1.6s ease-in-out infinite; }
.s32-breathe-1 { animation: s32Breathe 8s ease-in-out infinite; }
.s32-breathe-2 { animation: s32Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s32-breathe-3 { animation: s32Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s32ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s32-scan-line { animation: s32ScanLine 6s linear infinite; }
</style>



---
transition: fade
---
<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0">
  <div class="absolute top-[-10%] left-[-5%] w-[500px] h-[500px] bg-rose-500/8 rounded-full blur-[140px] s33-breathe-1"></div>
  <div class="absolute top-[40%] right-[-10%] w-[500px] h-[500px] bg-amber-500/8 rounded-full blur-[140px] s33-breathe-2"></div>
  <div class="absolute bottom-[-10%] left-[30%] w-[500px] h-[500px] bg-emerald-500/8 rounded-full blur-[140px] s33-breathe-3"></div>
</div>
<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-rose-400 to-transparent opacity-70"></div>
<div class="absolute bottom-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-amber-400 to-transparent opacity-50"></div>
<div class="absolute top-6 left-6 w-6 h-6 border-l border-t border-rose-400 opacity-50"></div>
<div class="absolute top-6 right-6 w-6 h-6 border-r border-t border-rose-400 opacity-50"></div>
<div class="absolute bottom-6 left-6 w-6 h-6 border-l border-b border-amber-400 opacity-50"></div>
<div class="absolute bottom-6 right-6 w-6 h-6 border-r border-b border-amber-400 opacity-50"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden opacity-10"><div class="absolute left-0 w-full h-[2px] bg-gradient-to-r from-transparent via-rose-300 to-transparent s33-scan-line"></div></div>
<div class="relative z-10 h-full flex flex-col px-6" style="padding-top: 4px; padding-bottom: 12px;">
  <div class="flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-2 h-2 bg-rose-400 rounded-full s33-pulse"></div>
      <div class="text-[10px] uppercase tracking-[0.4em] text-rose-400 font-mono">Slide 33 · Summary</div>
    </div>
    <div class="text-[10px] uppercase tracking-[0.3em] text-slate-500 font-mono">Dedik Romahadi · BIT</div>
  </div>
  <div class="flex items-end justify-between mt-3 mb-1">
    <div class="flex-1">
      <h1 class="!text-[1.1rem] !leading-[1.1] !font-bold !m-0 tracking-tight">
        <span class="text-white">Publication </span><span class="bg-gradient-to-r from-rose-300 via-amber-300 to-emerald-300 bg-clip-text text-transparent">Strategy</span>
      </h1>
      <div class="flex items-center gap-2 mt-1.5">
        <div class="h-1 w-12 bg-rose-400 rounded-full s33-bar-pulse-1"></div>
        <div class="h-1 w-20 bg-sky-400 rounded-full s33-bar-pulse-2"></div>
        <div class="h-1 w-8 bg-emerald-400 rounded-full s33-bar-pulse-3"></div>
        <div class="flex-1 h-px bg-gradient-to-r from-emerald-400/60 to-transparent"></div>
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s33-bar-dot"></div>
      </div>
    </div>
    <div class="flex items-center gap-3 ml-3">
      <div class="text-[9px] uppercase tracking-[0.2em] text-slate-400 font-mono text-right">4 Planned Papers · Progressive Cross-Scenario Transfer</div>
      <div class="flex items-center gap-2">
        <div class="w-1.5 h-1.5 bg-emerald-400 rounded-full s33-pulse-strong"></div>
        <div class="text-[10px] uppercase tracking-[0.3em] text-emerald-300 font-mono font-bold s33-blink-text">4 Papers</div>
      </div>
    </div>
  </div>
  <div class="flex-1 flex gap-2 min-h-0 mt-1">
    <div class="border border-rose-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-[1.9] flex flex-col min-h-0">
      <div class="bg-gradient-to-r from-rose-500/20 via-rose-500/5 to-transparent px-2 py-0.5 border-b border-rose-400/30 flex items-center gap-2 flex-shrink-0">
        <div class="text-[10px] font-mono font-bold text-rose-300">▸ Transfer Learning Roadmap · Visual Diagram</div>
        <div class="flex-1 h-px bg-gradient-to-r from-rose-400/50 to-transparent"></div>
        <div class="text-[8px] font-mono text-rose-400/70">Source → Target</div>
      </div>
      <div class="flex-1 p-3 min-h-0 flex items-center justify-center">
        <div class="relative w-full h-full" style="min-height: 320px;">
          <div class="absolute s33-arrow-1" style="left: 22%; top: 10%; width: 48%; height: 3%; display: flex; align-items: center;">
            <div class="flex-1 h-[3px] rounded-full s33-flow-bar-1" style="box-shadow: 0 0 8px rgba(251,113,133,0.5);"></div>
            <div style="width: 0; height: 0; border-top: 10px solid transparent; border-bottom: 10px solid transparent; border-left: 15px solid #fb7185; margin-left: -1px;"></div>
          </div>
          <svg class="absolute" style="left: 22%; top: 8%; width: 20%; height: 42%; pointer-events: none; overflow: visible; z-index: 5;" viewBox="0 0 100 100" preserveAspectRatio="none">
            <defs>
              <marker id="s33-mk-amber" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto">
                <path d="M 0 0 L 10 5 L 0 10 z" fill="#38bdf8"/>
              </marker>
            </defs>
            <path d="M 0 10 C 40 10 50 85 85 88" stroke="#38bdf8" stroke-width="3" fill="none" marker-end="url(#s33-mk-amber)" vector-effect="non-scaling-stroke" class="s33-flow"/>
          </svg>
          <svg class="absolute" style="left: 55%; top: 12%; width: 35%; height: 40%; pointer-events: none; overflow: visible; z-index: 5;" viewBox="0 0 100 100" preserveAspectRatio="none">
            <defs>
              <marker id="s33-mk-em-down" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto">
                <path d="M 0 0 L 10 5 L 0 10 z" fill="#34d399"/>
              </marker>
              <marker id="s33-mk-em-up" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto">
                <path d="M 0 0 L 10 5 L 0 10 z" fill="#34d399"/>
              </marker>
            </defs>
            <path d="M 45 30 C 87 50 44 60 20 71" stroke="#34d399" stroke-width="3" fill="none" marker-end="url(#s33-mk-em-down)" vector-effect="non-scaling-stroke" class="s33-flow"/>
            <path d="M 16 70 C -26 50 17 41 41 30" stroke="#34d399" stroke-width="3" fill="none" marker-end="url(#s33-mk-em-up)" vector-effect="non-scaling-stroke" class="s33-flow"/>
          </svg>
          <svg class="absolute" style="left: 6%; top: 18%; width: 45%; height: 70%; pointer-events: none; overflow: visible; z-index: 5;" viewBox="0 0 100 100" preserveAspectRatio="none">
            <defs>
              <marker id="s33-mk-yellow2" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto">
                <path d="M 0 0 L 10 5 L 0 10 z" fill="#facc15"/>
              </marker>
            </defs>
            <path d="M 13 4 C 0 40 84 45 84 89" stroke="#facc15" stroke-width="3" fill="none" marker-end="url(#s33-mk-yellow2)" vector-effect="non-scaling-stroke" class="s33-flow"/>
          </svg>
          <div class="absolute s33-node-pvt" style="left: 2%; top: 4%; width: 20%;">
            <div class="rounded-xl border-2 border-violet-300 px-2 py-2 text-center shadow-lg" style="background: linear-gradient(135deg, #a78bfa, #6d28d9);">
              <div class="text-[20px] font-black text-white leading-tight tracking-wider font-mono">PVT</div>
              <div class="text-[8px] font-mono text-violet-100 mt-0.5 tracking-wider">LAB BASELINE</div>
            </div>
          </div>
          <div class="absolute s33-node-ugv" style="left: 70%; top: 4%; width: 20%;">
            <div class="rounded-xl border-2 border-cyan-300 px-2 py-2 text-center shadow-lg" style="background: linear-gradient(135deg, #22d3ee, #0e7490);">
              <div class="text-[20px] font-black text-white leading-tight tracking-wider font-mono">UGV</div>
              <div class="text-[8px] font-mono text-cyan-100 mt-0.5 tracking-wider">GROUND OPS</div>
            </div>
          </div>
          <div class="absolute s33-node-uav" style="left: 40%; top: 42%; width: 20%;">
            <div class="rounded-xl border-2 border-orange-300 px-2 py-2 text-center shadow-lg" style="background: linear-gradient(135deg, #fb923c, #9a3412);">
              <div class="text-[20px] font-black text-white leading-tight tracking-wider font-mono">UAV</div>
              <div class="text-[8px] font-mono text-orange-100 mt-0.5 tracking-wider">AERIAL OPS</div>
            </div>
          </div>
          <div class="absolute s33-node-combined" style="left: 25%; top: 82%; width: 38%;">
            <div class="rounded-xl border-2 border-yellow-100 px-2 py-1.5 text-center shadow-xl" style="background: linear-gradient(135deg, #fde047, #a16207);">
              <div class="text-[8px] font-mono font-bold text-amber-900 tracking-widest">★ UNIFIED MODEL</div>
              <div class="text-[16px] font-black text-slate-900 leading-tight tracking-wider font-mono mt-0.5">UGV + UAV</div>
            </div>
          </div>
          <div class="absolute s33-label-1 px-2 py-0.5 rounded-full border-2 border-rose-400 bg-slate-950 text-[9px] font-mono font-bold text-rose-300 tracking-widest z-10" style="left: 43%; top: 8%;">PAPER 1</div>
          <div class="absolute s33-label-2 px-2 py-0.5 rounded-full border-2 border-sky-400 bg-slate-950 text-[9px] font-mono font-bold text-sky-300 tracking-widest z-10" style="left: 22%; top: 24%;">PAPER 2</div>
          <div class="absolute s33-label-3 px-2 py-0.5 rounded-full border-2 border-emerald-400 bg-slate-950 text-[9px] font-mono font-bold text-emerald-300 tracking-widest z-10" style="left: 65%; top: 30%;">PAPER 3</div>
          <div class="absolute s33-label-4 px-2 py-0.5 rounded-full border-2 border-yellow-400 bg-slate-950 text-[9px] font-mono font-bold text-yellow-300 tracking-widest z-10" style="left: 10%; top: 38%;">PAPER 4</div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-2 flex-[1.1] min-h-0">
      <div class="border border-rose-400/60 rounded-md p-2 bg-rose-950/20 relative s33-paper-1">
        <div class="flex items-start gap-2.5">
          <div class="flex-shrink-0 w-14 h-11 rounded-md bg-rose-500 border border-rose-200 flex flex-col items-center justify-center s33-badge">
            <div class="text-[8px] font-mono text-rose-100 leading-none font-bold tracking-wider">PAPER</div>
            <div class="text-[14px] font-mono font-black text-white leading-none mt-0.5">1</div>
          </div>
          <div class="flex-1">
            <div class="flex items-center gap-1.5">
              <div class="text-[12px] uppercase font-mono font-bold text-rose-300 tracking-wider">PVT → UGV</div>
              <div class="text-[9px] font-mono text-rose-400/80">Lab → Ground Ops</div>
            </div>
            <div class="text-[11px] text-slate-200 leading-snug mt-1">Foundational transfer · Establish lab-trained model generalizes to ground teleoperation</div>
          </div>
        </div>
      </div>
      <div class="border border-sky-400/60 rounded-md p-2 bg-sky-950/20 relative s33-paper-2">
        <div class="flex items-start gap-2.5">
          <div class="flex-shrink-0 w-14 h-11 rounded-md bg-sky-500 border border-sky-200 flex flex-col items-center justify-center s33-badge">
            <div class="text-[8px] font-mono text-sky-100 leading-none font-bold tracking-wider">PAPER</div>
            <div class="text-[14px] font-mono font-black text-white leading-none mt-0.5">2</div>
          </div>
          <div class="flex-1">
            <div class="flex items-center gap-1.5">
              <div class="text-[12px] uppercase font-mono font-bold text-sky-300 tracking-wider">PVT → UAV</div>
              <div class="text-[9px] font-mono text-sky-400/80">Lab → Aerial Ops</div>
            </div>
            <div class="text-[11px] text-slate-200 leading-snug mt-1">Aerial extension · Tests model robustness on higher-workload UAV teleoperation</div>
          </div>
        </div>
      </div>
      <div class="border border-emerald-400/60 rounded-md p-2 bg-emerald-950/20 relative s33-paper-3">
        <div class="flex items-start gap-2.5">
          <div class="flex-shrink-0 w-14 h-11 rounded-md bg-emerald-500 border border-emerald-200 flex flex-col items-center justify-center s33-badge">
            <div class="text-[8px] font-mono text-emerald-100 leading-none font-bold tracking-wider">PAPER</div>
            <div class="text-[14px] font-mono font-black text-white leading-none mt-0.5">3</div>
          </div>
          <div class="flex-1">
            <div class="flex items-center gap-1.5">
              <div class="text-[12px] uppercase font-mono font-bold text-emerald-300 tracking-wider">UGV ⇄ UAV</div>
              <div class="text-[9px] font-mono text-emerald-400/80">Bidirectional Ops</div>
            </div>
            <div class="text-[11px] text-slate-200 leading-snug mt-1">Operation-to-operation · Real-world switching between ground and aerial platforms</div>
          </div>
        </div>
      </div>
      <div class="border-2 border-yellow-400/80 rounded-md p-2 bg-gradient-to-br from-yellow-950/40 to-amber-950/30 relative s33-paper-4">
        <div class="flex items-start gap-2.5">
          <div class="flex-shrink-0 w-14 h-11 rounded-md bg-yellow-400 border-2 border-yellow-100 flex flex-col items-center justify-center s33-badge-conclusion">
            <div class="text-[8px] font-mono text-yellow-900 leading-none font-bold tracking-wider">PAPER</div>
            <div class="text-[14px] font-mono font-black text-black leading-none mt-0.5">4</div>
          </div>
          <div class="flex-1">
            <div class="flex items-center gap-1.5">
              <div class="text-[12px] uppercase font-mono font-black text-yellow-300 tracking-wider">PVT → UGV + UAV</div>
              <div class="text-[9px] font-mono text-yellow-400/90">★ Unified</div>
            </div>
            <div class="text-[11px] text-slate-100 leading-snug mt-1 font-semibold">Capstone · Single lab-trained model generalizes to <span class="text-yellow-200 font-bold">all operational scenarios</span></div>
          </div>
        </div>
      </div>
      <div class="border border-violet-400/40 rounded-lg bg-slate-900/30 overflow-hidden flex-shrink-0 mt-0.5">
        <div class="px-2 py-1 flex items-center gap-2">
          <div class="text-[9px] font-mono font-bold text-violet-300">▸ Progressive Complexity</div>
          <div class="flex-1 flex items-center gap-1">
            <div class="flex-1 h-1 bg-gradient-to-r from-rose-500 via-sky-500 via-emerald-500 to-yellow-400 rounded-full s33-progress"></div>
            <div class="text-[7px] font-mono text-violet-400/80 ml-1">P1 → P4</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="absolute left-8 right-6 flex items-center justify-between" style="bottom: -2px;">
    <div class="flex items-center gap-3 text-[8px] uppercase tracking-[0.2em] text-slate-500 font-mono">
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-rose-400 rounded-sm"></div>Paper 1</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-sky-400 rounded-sm"></div>Paper 2</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-emerald-400 rounded-sm"></div>Paper 3</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 bg-yellow-400 rounded-sm"></div>★ Paper 4 (Capstone)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-full" style="background: #c084fc;"></div>PVT (Lab)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-full" style="background: #67e8f9;"></div>UGV (Ground)</div>
      <div class="flex items-center gap-1"><div class="w-1.5 h-1.5 rounded-full" style="background: #fb923c;"></div>UAV (Aerial)</div>
    </div>
  </div>
</div>

<style>
@keyframes s33NodeEntry {
  0% { opacity: 0; transform: scale(0.5); transform-origin: center; }
  100% { opacity: 1; transform: scale(1); }
}
.s33-node-pvt { animation: s33NodeEntry 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.3s both; }
.s33-node-ugv { animation: s33NodeEntry 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.5s both; }
.s33-node-uav { animation: s33NodeEntry 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.9s both; }
.s33-node-combined { animation: s33NodeEntry 0.6s cubic-bezier(0.16, 1, 0.3, 1) 1.3s both; }
@keyframes s33LabelFade {
  0% { opacity: 0; }
  100% { opacity: 1; }
}
.s33-label-1 { animation: s33LabelFade 0.4s ease-out 1.1s both; }
.s33-label-2 { animation: s33LabelFade 0.4s ease-out 1.5s both; }
.s33-label-3 { animation: s33LabelFade 0.4s ease-out 1.9s both; }
.s33-label-4 { animation: s33LabelFade 0.4s ease-out 2.5s both; }
@keyframes s33ArrowDraw {
  0% { stroke-dashoffset: 300; opacity: 0; }
  100% { stroke-dashoffset: 0; opacity: 1; }
}
.s33-arrow-1 { stroke-dasharray: 300; animation: s33ArrowDraw 0.8s ease-out 0.6s both; }
.s33-arrow-2 { stroke-dasharray: 300; animation: s33ArrowDraw 0.8s ease-out 1.0s both; }
.s33-arrow-3a { stroke-dasharray: 200; animation: s33ArrowDraw 0.8s ease-out 1.3s both; }
.s33-arrow-3b { animation: s33ArrowDraw 0.8s ease-out 1.5s both; }
.s33-arrow-4 { animation: s33ArrowDraw 1s ease-out 1.8s both; }
@keyframes s33PaperIn {
  0% { opacity: 0; transform: translateX(15px); }
  100% { opacity: 1; transform: translateX(0); }
}
.s33-paper-1 { animation: s33PaperIn 0.6s ease-out 0.4s both; }
.s33-paper-2 { animation: s33PaperIn 0.6s ease-out 0.9s both; }
.s33-paper-3 { animation: s33PaperIn 0.6s ease-out 1.4s both; }
.s33-paper-4 { animation: s33PaperIn 0.6s ease-out 1.9s both; }
@keyframes s33PaperGlow {
  0%, 100% { box-shadow: 0 0 0 transparent; }
  50% { box-shadow: 0 0 14px currentColor; }
}
.s33-paper-1 { color: #fb7185; animation: s33PaperIn 0.6s ease-out 0.4s both, s33PaperGlow 3s ease-in-out 2s infinite; }
.s33-paper-2 { color: #38bdf8; animation: s33PaperIn 0.6s ease-out 0.9s both, s33PaperGlow 3s ease-in-out 2.7s infinite; }
.s33-paper-3 { color: #34d399; animation: s33PaperIn 0.6s ease-out 1.4s both, s33PaperGlow 3s ease-in-out 3.4s infinite; }
.s33-paper-4 { color: #facc15; animation: s33PaperIn 0.6s ease-out 1.9s both, s33PaperGlow 2.4s ease-in-out 4.1s infinite; }
@keyframes s33BadgePulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 4px currentColor; }
  50% { transform: scale(1.08); box-shadow: 0 0 12px currentColor; }
}
.s33-badge { animation: s33BadgePulse 2s ease-in-out infinite; }
@keyframes s33BadgeConclusion {
  0%, 100% { transform: scale(1) rotate(0deg); box-shadow: 0 0 8px #facc15, 0 0 16px rgba(250,204,21,0.4); }
  50% { transform: scale(1.15) rotate(180deg); box-shadow: 0 0 16px #facc15, 0 0 28px rgba(250,204,21,0.8); }
}
.s33-badge-conclusion { animation: s33BadgeConclusion 2.4s ease-in-out infinite; }
@keyframes s33Progress {
  0% { background-size: 0% 100%; background-repeat: no-repeat; }
  100% { background-size: 100% 100%; background-repeat: no-repeat; }
}
.s33-progress { box-shadow: 0 0 8px rgba(250,204,21,0.4); }
@keyframes s33Pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
.s33-pulse { animation: s33Pulse 1.6s ease-in-out infinite; }
@keyframes s33PulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); box-shadow: 0 0 8px #34d399, 0 0 16px rgba(52,211,153,0.6); }
  50% { opacity: 0.4; transform: scale(0.7); box-shadow: 0 0 0 transparent; }
}
.s33-pulse-strong { animation: s33PulseStrong 0.9s ease-in-out infinite; }
@keyframes s33BlinkText {
  0%, 49%, 100% { opacity: 1; text-shadow: 0 0 8px #34d399, 0 0 14px rgba(52,211,153,0.8); color: #34d399; }
  50%, 99% { opacity: 0.25; text-shadow: none; color: #6ee7b7; }
}
.s33-blink-text { animation: s33BlinkText 0.9s steps(2, end) infinite; }
@keyframes s33Breathe { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.7; transform: scale(1.05); } }
@keyframes s33BarPulse {
  0%, 100% { opacity: 0.6; box-shadow: 0 0 4px currentColor; transform: scaleX(1); }
  50% { opacity: 1; box-shadow: 0 0 12px currentColor, 0 0 20px currentColor; transform: scaleX(1.08); }
}
.s33-bar-pulse-1, .s33-bar-pulse-2, .s33-bar-pulse-3 { animation: s33BarPulse 2.4s ease-in-out infinite; transform-origin: left center; }
.s33-bar-pulse-1 { color: #fb7185; animation-delay: 0s; }
.s33-bar-pulse-2 { color: #38bdf8; animation-delay: -0.8s; }
.s33-bar-pulse-3 { color: #34d399; animation-delay: -1.6s; }
@keyframes s33BarDot {
  0%, 100% { opacity: 1; box-shadow: 0 0 6px #34d399, 0 0 12px rgba(52,211,153,0.6); transform: scale(1); }
  50% { opacity: 0.5; box-shadow: 0 0 2px #34d399; transform: scale(0.85); }
}
.s33-bar-dot { animation: s33BarDot 1.6s ease-in-out infinite; }
.s33-breathe-1 { animation: s33Breathe 8s ease-in-out infinite; }
.s33-breathe-2 { animation: s33Breathe 10s ease-in-out infinite; animation-delay: -3s; }
.s33-breathe-3 { animation: s33Breathe 9s ease-in-out infinite; animation-delay: -5s; }
@keyframes s33ScanLine { 0% { top: -5%; } 100% { top: 105%; } }
.s33-scan-line { animation: s33ScanLine 6s linear infinite; }
@keyframes s33Flow { to { stroke-dashoffset: -25; } }
.s33-flow { stroke-dasharray: 18 7; animation: s33Flow 1.5s linear infinite; }
@keyframes s33BarFlow { to { background-position: 25px 0; } }
.s33-flow-bar-1 { background: repeating-linear-gradient(90deg, #fb7185 0, #fb7185 18px, transparent 18px, transparent 25px); animation: s33BarFlow 1.5s linear infinite; }
</style>



---
layout: default
---

<div class="absolute inset-0 bg-black"></div>
<div class="absolute inset-0 overflow-hidden">
  <div class="absolute top-[-12%] left-[-12%] w-[620px] h-[620px] rounded-full send-breathe-1" style="background: radial-gradient(circle, rgba(6,182,212,0.22), transparent 70%); filter: blur(100px);"></div>
  <div class="absolute top-[10%] right-[-12%] w-[580px] h-[580px] rounded-full send-breathe-2" style="background: radial-gradient(circle, rgba(232,121,249,0.18), transparent 70%); filter: blur(100px);"></div>
  <div class="absolute bottom-[-15%] left-[28%] w-[560px] h-[560px] rounded-full send-breathe-3" style="background: radial-gradient(circle, rgba(251,191,36,0.14), transparent 70%); filter: blur(110px);"></div>
  <div class="absolute top-[38%] left-[12%] w-[380px] h-[380px] rounded-full send-breathe-1" style="background: radial-gradient(circle, rgba(52,211,153,0.10), transparent 70%); filter: blur(90px); animation-delay: -3s;"></div>
</div>
<div class="absolute inset-0" style="background-image: radial-gradient(circle at 50% 50%, rgba(6,182,212,0.35) 1px, transparent 1.2px); background-size: 28px 28px; opacity: 0.2;"></div>
<div class="absolute inset-0 pointer-events-none overflow-hidden z-[2]">
  <div class="absolute left-0 w-full send-scan-h" style="height: 1px; background: linear-gradient(90deg, transparent, rgba(34,211,238,0.9), transparent); box-shadow: 0 0 10px rgba(34,211,238,0.7);"></div>
  <div class="absolute top-0 h-full send-scan-v" style="width: 1px; background: linear-gradient(180deg, transparent, rgba(232,121,249,0.7), transparent); box-shadow: 0 0 8px rgba(232,121,249,0.5);"></div>
</div>
<div class="absolute top-4 left-4 z-20" style="width: 56px; height: 56px;">
  <div class="absolute top-0 left-0 w-full h-px" style="background: linear-gradient(90deg, #22d3ee, transparent);"></div>
  <div class="absolute top-0 left-0 h-full w-px" style="background: linear-gradient(180deg, #22d3ee, transparent);"></div>
  <div class="absolute top-0 left-0 w-1.5 h-1.5 bg-cyan-400" style="box-shadow: 0 0 8px #22d3ee;"></div>
  <div class="absolute top-[2px] left-2.5 w-[3px] h-[3px] bg-cyan-400"></div>
  <div class="absolute top-2.5 left-[2px] w-[3px] h-[3px] bg-cyan-400"></div>
  <div class="absolute top-7 left-1 text-[7px] text-cyan-400/80 font-mono tracking-[0.25em]">N.01</div>
</div>
<div class="absolute top-4 right-4 z-20" style="width: 56px; height: 56px;">
  <div class="absolute top-0 right-0 w-full h-px" style="background: linear-gradient(270deg, #e879f9, transparent);"></div>
  <div class="absolute top-0 right-0 h-full w-px" style="background: linear-gradient(180deg, #e879f9, transparent);"></div>
  <div class="absolute top-0 right-0 w-1.5 h-1.5 bg-fuchsia-400" style="box-shadow: 0 0 8px #e879f9;"></div>
  <div class="absolute top-[2px] right-2.5 w-[3px] h-[3px] bg-fuchsia-400"></div>
  <div class="absolute top-2.5 right-[2px] w-[3px] h-[3px] bg-fuchsia-400"></div>
  <div class="absolute top-7 right-1 text-[7px] text-fuchsia-400/80 font-mono tracking-[0.25em]">N.02</div>
</div>
<div class="absolute bottom-4 left-4 z-20" style="width: 56px; height: 56px;">
  <div class="absolute bottom-0 left-0 w-full h-px" style="background: linear-gradient(90deg, #fbbf24, transparent);"></div>
  <div class="absolute bottom-0 left-0 h-full w-px" style="background: linear-gradient(0deg, #fbbf24, transparent);"></div>
  <div class="absolute bottom-0 left-0 w-1.5 h-1.5 bg-amber-400" style="box-shadow: 0 0 8px #fbbf24;"></div>
  <div class="absolute bottom-[2px] left-2.5 w-[3px] h-[3px] bg-amber-400"></div>
  <div class="absolute bottom-2.5 left-[2px] w-[3px] h-[3px] bg-amber-400"></div>
  <div class="absolute bottom-7 left-1 text-[7px] text-amber-400/80 font-mono tracking-[0.25em]">N.03</div>
</div>
<div class="absolute bottom-4 right-4 z-20" style="width: 56px; height: 56px;">
  <div class="absolute bottom-0 right-0 w-full h-px" style="background: linear-gradient(270deg, #34d399, transparent);"></div>
  <div class="absolute bottom-0 right-0 h-full w-px" style="background: linear-gradient(0deg, #34d399, transparent);"></div>
  <div class="absolute bottom-0 right-0 w-1.5 h-1.5 bg-emerald-400" style="box-shadow: 0 0 8px #34d399;"></div>
  <div class="absolute bottom-[2px] right-2.5 w-[3px] h-[3px] bg-emerald-400"></div>
  <div class="absolute bottom-2.5 right-[2px] w-[3px] h-[3px] bg-emerald-400"></div>
  <div class="absolute bottom-7 right-1 text-[7px] text-emerald-400/80 font-mono tracking-[0.25em]">N.04</div>
</div>
<div class="absolute top-5 left-1/2 -translate-x-1/2 z-20 flex items-center gap-3">
  <div class="flex items-center gap-2 px-2.5 py-1 border border-cyan-400/50" style="background: rgba(6,182,212,0.08);">
    <span class="w-1 h-1 bg-cyan-400 rounded-full send-pulse-dot"></span>
    <span class="text-[8px] text-cyan-300 font-mono tracking-[0.3em] uppercase">SYS.READY</span>
  </div>
  <span class="text-slate-600 text-[8px] font-mono">//</span>
  <div class="flex items-center gap-2 px-2.5 py-1 border border-amber-400/50" style="background: rgba(251,191,36,0.08);">
    <span class="w-1 h-1 bg-amber-400 rounded-full send-pulse-dot" style="animation-delay: -0.4s;"></span>
    <span class="text-[8px] text-amber-300 font-mono tracking-[0.3em] uppercase">SEC.END</span>
  </div>
  <span class="text-slate-600 text-[8px] font-mono">//</span>
  <div class="flex items-center gap-2 px-2.5 py-1 border border-fuchsia-400/50" style="background: rgba(232,121,249,0.08);">
    <span class="w-1 h-1 bg-fuchsia-400 rounded-full send-pulse-dot" style="animation-delay: -0.8s;"></span>
    <span class="text-[8px] text-fuchsia-300 font-mono tracking-[0.3em] uppercase">NODE.BIT</span>
  </div>
</div>
<div class="absolute z-20 flex flex-col items-center gap-2" style="left: calc(25% - 45px); top: calc(50% - 130px); transform: translate(-50%, -50%);">
  <div class="text-[8px] text-cyan-300 font-mono tracking-[0.3em]">&gt; UAV.TRACK</div>
  <svg viewBox="0 0 140 140" width="110" height="110" style="filter: drop-shadow(0 0 10px rgba(34,211,238,0.55));">
    <ellipse cx="70" cy="130" rx="24" ry="3" fill="#22d3ee" opacity="0.25" class="send-uav-shadow"/>
    <g class="send-uav-hover">
      <line x1="70" y1="70" x2="28" y2="28" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
      <line x1="70" y1="70" x2="112" y2="28" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
      <line x1="70" y1="70" x2="28" y2="112" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
      <line x1="70" y1="70" x2="112" y2="112" stroke="#22d3ee" stroke-width="3" stroke-linecap="round"/>
      <circle cx="28" cy="28" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
      <g style="transform-origin: 28px 28px;" class="send-rotor-cw">
        <line x1="14" y1="28" x2="42" y2="28" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
      </g>
      <circle cx="28" cy="28" r="3" fill="#22d3ee"/>
      <circle cx="112" cy="28" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
      <g style="transform-origin: 112px 28px;" class="send-rotor-ccw">
        <line x1="98" y1="28" x2="126" y2="28" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
      </g>
      <circle cx="112" cy="28" r="3" fill="#22d3ee"/>
      <circle cx="28" cy="112" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
      <g style="transform-origin: 28px 112px;" class="send-rotor-ccw">
        <line x1="14" y1="112" x2="42" y2="112" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
      </g>
      <circle cx="28" cy="112" r="3" fill="#22d3ee"/>
      <circle cx="112" cy="112" r="14" fill="rgba(34,211,238,0.06)" stroke="#22d3ee" stroke-width="0.8" opacity="0.5"/>
      <g style="transform-origin: 112px 112px;" class="send-rotor-cw">
        <line x1="98" y1="112" x2="126" y2="112" stroke="#22d3ee" stroke-width="2.5" opacity="0.85" stroke-linecap="round"/>
      </g>
      <circle cx="112" cy="112" r="3" fill="#22d3ee"/>
      <circle cx="70" cy="70" r="12" fill="#000" stroke="#22d3ee" stroke-width="2"/>
      <circle cx="70" cy="70" r="5" fill="#22d3ee" class="send-beacon"/>
      <circle cx="82" cy="70" r="1.5" fill="#fbbf24" class="send-beacon" style="animation-delay: -0.4s;"/>
    </g>
  </svg>
  <div class="text-[7px] text-cyan-400/60 font-mono tracking-[0.3em]">ALT.150M</div>
</div>
<div class="absolute z-20 flex flex-col items-center gap-2" style="left: calc(75% + 45px); top: calc(50% - 130px); transform: translate(-50%, -50%);">
  <div class="text-[8px] text-fuchsia-300 font-mono tracking-[0.3em]">&gt; UGV.TRACK</div>
  <svg viewBox="0 0 140 140" width="110" height="110" style="filter: drop-shadow(0 0 10px rgba(232,121,249,0.55));">
    <line x1="5" y1="120" x2="135" y2="120" stroke="#e879f9" stroke-width="1" opacity="0.35" stroke-dasharray="6 3" class="send-ground-scroll"/>
    <g class="send-ugv-bob">
      <path d="M 95 75 L 125 68 L 125 82 L 95 79 Z" fill="#e879f9" opacity="0.15" class="send-headlight"/>
      <path d="M 30 90 L 30 72 L 42 62 L 98 62 L 110 72 L 110 90 Z" fill="#000" stroke="#e879f9" stroke-width="2"/>
      <rect x="52" y="46" width="32" height="16" rx="1" fill="#000" stroke="#e879f9" stroke-width="2"/>
      <circle cx="68" cy="54" r="3" fill="#e879f9" class="send-camera-pulse"/>
      <line x1="85" y1="46" x2="96" y2="24" stroke="#e879f9" stroke-width="1.5"/>
      <circle cx="96" cy="24" r="2.5" fill="#e879f9" class="send-antenna-pulse"/>
      <path d="M 96 24 Q 104 18 108 24" fill="none" stroke="#e879f9" stroke-width="1" class="send-signal-1"/>
      <path d="M 96 24 Q 108 12 116 24" fill="none" stroke="#e879f9" stroke-width="1" class="send-signal-2"/>
      <circle cx="108" cy="78" r="2" fill="#e879f9"/>
      <line x1="42" y1="70" x2="45" y2="62" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
      <line x1="98" y1="62" x2="95" y2="70" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
      <g style="transform-origin: 95px 95px;" class="send-wheel-spin">
        <circle cx="95" cy="95" r="13" fill="#000" stroke="#e879f9" stroke-width="2"/>
        <circle cx="95" cy="95" r="5" fill="#e879f9"/>
        <line x1="95" y1="82" x2="95" y2="108" stroke="#e879f9" stroke-width="1.5"/>
        <line x1="82" y1="95" x2="108" y2="95" stroke="#e879f9" stroke-width="1.5"/>
        <line x1="86" y1="86" x2="104" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
        <line x1="104" y1="86" x2="86" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
      </g>
      <g style="transform-origin: 45px 95px;" class="send-wheel-spin">
        <circle cx="45" cy="95" r="13" fill="#000" stroke="#e879f9" stroke-width="2"/>
        <circle cx="45" cy="95" r="5" fill="#e879f9"/>
        <line x1="45" y1="82" x2="45" y2="108" stroke="#e879f9" stroke-width="1.5"/>
        <line x1="32" y1="95" x2="58" y2="95" stroke="#e879f9" stroke-width="1.5"/>
        <line x1="36" y1="86" x2="54" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
        <line x1="54" y1="86" x2="36" y2="104" stroke="#e879f9" stroke-width="1" opacity="0.6"/>
      </g>
    </g>
  </svg>
  <div class="text-[7px] text-fuchsia-400/60 font-mono tracking-[0.3em]">VEL.2.5M/S</div>
</div>
<div class="absolute left-6 top-1/2 -translate-y-1/2 z-20 flex flex-col items-center gap-1.5">
  <div class="text-[7px] text-cyan-400/70 font-mono tracking-[0.25em]">CH.A</div>
  <div class="flex items-end gap-[2px] h-10">
    <div class="w-[3px] bg-cyan-400 send-bar-1" style="height: 50%; box-shadow: 0 0 4px #22d3ee;"></div>
    <div class="w-[3px] bg-cyan-400 send-bar-2" style="height: 60%; box-shadow: 0 0 4px #22d3ee;"></div>
    <div class="w-[3px] bg-cyan-400 send-bar-3" style="height: 55%; box-shadow: 0 0 4px #22d3ee;"></div>
    <div class="w-[3px] bg-cyan-400 send-bar-4" style="height: 70%; box-shadow: 0 0 4px #22d3ee;"></div>
    <div class="w-[3px] bg-cyan-400 send-bar-5" style="height: 40%; box-shadow: 0 0 4px #22d3ee;"></div>
    <div class="w-[3px] bg-cyan-400 send-bar-2" style="height: 55%; box-shadow: 0 0 4px #22d3ee;"></div>
  </div>
  <div class="text-[7px] text-cyan-400/70 font-mono tracking-[0.25em]">SIG.OK</div>
</div>
<div class="absolute right-6 top-1/2 -translate-y-1/2 z-20 flex flex-col items-center gap-1.5">
  <div class="text-[7px] text-fuchsia-400/70 font-mono tracking-[0.25em]">CH.B</div>
  <div class="flex items-end gap-[2px] h-10">
    <div class="w-[3px] bg-fuchsia-400 send-bar-3" style="height: 55%; box-shadow: 0 0 4px #e879f9;"></div>
    <div class="w-[3px] bg-fuchsia-400 send-bar-1" style="height: 65%; box-shadow: 0 0 4px #e879f9;"></div>
    <div class="w-[3px] bg-fuchsia-400 send-bar-5" style="height: 45%; box-shadow: 0 0 4px #e879f9;"></div>
    <div class="w-[3px] bg-fuchsia-400 send-bar-2" style="height: 75%; box-shadow: 0 0 4px #e879f9;"></div>
    <div class="w-[3px] bg-fuchsia-400 send-bar-4" style="height: 50%; box-shadow: 0 0 4px #e879f9;"></div>
    <div class="w-[3px] bg-fuchsia-400 send-bar-1" style="height: 60%; box-shadow: 0 0 4px #e879f9;"></div>
  </div>
  <div class="text-[7px] text-fuchsia-400/70 font-mono tracking-[0.25em]">LINK.UP</div>
</div>
<div class="relative z-10 h-full flex flex-col items-center justify-center px-8">
  <div class="relative" style="width: 180px; height: 180px;">
    <div class="absolute -inset-3 send-rotate-reverse opacity-40" style="border: 1px dashed rgba(34,211,238,0.5); border-radius: 50%;"></div>
    <div class="absolute inset-0 send-rotate-slow" style="border-radius: 50%; background: conic-gradient(from 0deg, transparent 0%, rgba(6,182,212,0.5) 15%, transparent 30%, transparent 50%, rgba(232,121,249,0.5) 65%, transparent 80%, transparent 100%); filter: blur(6px);"></div>
    <div class="absolute inset-0" style="clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%); background: linear-gradient(135deg, #22d3ee 0%, #e879f9 50%, #fbbf24 100%);">
      <div class="absolute" style="inset: 2px; clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%); background: #000;"></div>
    </div>
    <div class="absolute rounded-full send-rotate opacity-50" style="inset: 18%; background: conic-gradient(from 0deg, rgba(34,211,238,0.6), rgba(34,211,238,0.2) 20%, transparent 40%, transparent 100%);"></div>
    <div class="absolute rounded-full send-pulse-bg" style="inset: 22%; background: radial-gradient(circle, #ffffff 0%, #fef3c7 55%, #fbbf24 95%);"></div>
    <div class="absolute flex items-center justify-center" style="inset: 25%;">
      <img src="/logo.svg" class="w-full h-full object-contain" style="filter: drop-shadow(0 2px 6px rgba(0,0,0,0.5));" />
    </div>
    <div class="absolute top-0 left-1/2 -translate-x-1/2 -translate-y-1/2 w-2.5 h-2.5 rotate-45 bg-cyan-400" style="box-shadow: 0 0 8px #22d3ee;"></div>
    <div class="absolute bottom-0 left-1/2 -translate-x-1/2 translate-y-1/2 w-2.5 h-2.5 rotate-45 bg-fuchsia-400" style="box-shadow: 0 0 8px #e879f9;"></div>
    <div class="absolute left-0 top-1/4 -translate-x-1/2 w-2 h-2 rotate-45 bg-amber-400" style="box-shadow: 0 0 6px #fbbf24;"></div>
    <div class="absolute right-0 top-1/4 translate-x-1/2 w-2 h-2 rotate-45 bg-amber-400" style="box-shadow: 0 0 6px #fbbf24;"></div>
    <div class="absolute left-0 bottom-1/4 -translate-x-1/2 w-2 h-2 rotate-45 bg-emerald-400" style="box-shadow: 0 0 6px #34d399;"></div>
    <div class="absolute right-0 bottom-1/4 translate-x-1/2 w-2 h-2 rotate-45 bg-emerald-400" style="box-shadow: 0 0 6px #34d399;"></div>
  </div>
  <div class="mt-5 flex items-center gap-3">
    <div class="h-px w-10" style="background: linear-gradient(90deg, transparent, #22d3ee);"></div>
    <div class="px-3 py-1 border border-cyan-400/40" style="background: rgba(6,182,212,0.05);">
      <span class="text-[10px] font-mono tracking-[0.45em] uppercase text-cyan-100">Beijing Institute of Technology</span>
    </div>
    <div class="h-px w-10" style="background: linear-gradient(90deg, #22d3ee, transparent);"></div>
  </div>
  <div class="mt-5 flex items-center gap-4">
    <span class="text-cyan-400/60 text-5xl font-thin leading-none">&lt;</span>
    <h1 class="leading-none send-shimmer" style="font-size: 55px; font-weight: 900; letter-spacing: 0.14em; background: linear-gradient(135deg, #22d3ee 0%, #e879f9 48%, #fbbf24 100%); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;">THANK YOU</h1>
    <span class="text-amber-400/60 text-5xl font-thin leading-none">/&gt;</span>
  </div>
  <div class="mt-2 flex items-center gap-3">
    <span class="text-slate-500 text-sm font-mono">//</span>
    <span class="text-slate-300 text-sm tracking-[0.45em] uppercase">For Your Kind Attention</span>
    <span class="text-slate-500 text-sm font-mono">//</span>
  </div>
  <div class="mt-5 relative" style="width: 620px;">
    <div class="absolute inset-0" style="clip-path: polygon(14px 0, calc(100% - 14px) 0, 100% 14px, 100% calc(100% - 14px), calc(100% - 14px) 100%, 14px 100%, 0 calc(100% - 14px), 0 14px); background: linear-gradient(135deg, #22d3ee, #e879f9, #fbbf24); opacity: 0.55;"></div>
    <div class="relative" style="margin: 1px; clip-path: polygon(13px 0, calc(100% - 13px) 0, 100% 13px, 100% calc(100% - 13px), calc(100% - 13px) 100%, 13px 100%, 0 calc(100% - 13px), 0 13px); background: linear-gradient(135deg, rgba(15,23,42,0.96), rgba(30,41,59,0.92)); box-shadow: inset 0 0 40px rgba(6,182,212,0.1);">
      <div class="px-8 py-4 grid grid-cols-3 gap-4 text-center">
        <div>
          <div class="text-[9px] font-mono text-cyan-400 tracking-[0.35em] uppercase mb-1">&gt; PRESENTER</div>
          <div class="text-white font-bold text-lg tracking-wide">Dedik Romahadi</div>
        </div>
        <div class="border-x border-slate-700/60 px-2">
          <div class="text-[9px] font-mono text-fuchsia-400 tracking-[0.35em] uppercase mb-1">&gt; STUDENT_ID</div>
          <div class="text-white font-bold text-lg tracking-[0.2em] font-mono">3820222028</div>
        </div>
        <div>
          <div class="text-[9px] font-mono text-amber-400 tracking-[0.35em] uppercase mb-1">&gt; DATE</div>
          <div class="text-white font-bold text-lg">{{ new Date().toLocaleDateString('en-US', { year: 'numeric', month: 'long', day: 'numeric' }) }}</div>
        </div>
      </div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-1/2 -translate-x-1/2 z-20 flex items-center gap-3">
  <div class="flex items-center gap-2 px-3 py-1 border border-cyan-400/40" style="background: rgba(6,182,212,0.08); clip-path: polygon(8px 0, 100% 0, calc(100% - 8px) 100%, 0 100%);">
    <span class="w-1.5 h-1.5 bg-cyan-400 rounded-full send-pulse-strong"></span>
    <span class="text-[9px] text-cyan-300 font-mono tracking-[0.3em] uppercase">Open.For.Q&amp;A</span>
  </div>
  <span class="text-slate-500 text-[9px] font-mono tracking-[0.3em]">PROPOSAL.END</span>
  <div class="flex items-center gap-2 px-3 py-1 border border-fuchsia-400/40" style="background: rgba(232,121,249,0.08); clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 100%, 8px 100%);">
    <span class="text-[9px] text-fuchsia-300 font-mono tracking-[0.3em] uppercase">SIG.LOCKED</span>
    <span class="w-1.5 h-1.5 bg-fuchsia-400 rounded-full send-pulse-strong" style="animation-delay: -0.5s;"></span>
  </div>
</div>

<style scoped>
@keyframes sendBreathe1 {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.75; transform: scale(1.05); }
}
.send-breathe-1 { animation: sendBreathe1 6s ease-in-out infinite; }
@keyframes sendBreathe2 {
  0%, 100% { opacity: 0.85; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.08); }
}
.send-breathe-2 { animation: sendBreathe2 7s ease-in-out infinite; }
@keyframes sendBreathe3 {
  0%, 100% { opacity: 0.9; transform: scale(1.02); }
  50% { opacity: 0.65; transform: scale(1); }
}
.send-breathe-3 { animation: sendBreathe3 8s ease-in-out infinite; }
@keyframes sendScanH {
  0% { top: -2%; opacity: 0; }
  10% { opacity: 0.7; }
  50% { opacity: 1; }
  90% { opacity: 0.7; }
  100% { top: 102%; opacity: 0; }
}
.send-scan-h { animation: sendScanH 7s linear infinite; }
@keyframes sendScanV {
  0% { left: -2%; opacity: 0; }
  10% { opacity: 0.5; }
  50% { opacity: 0.8; }
  90% { opacity: 0.5; }
  100% { left: 102%; opacity: 0; }
}
.send-scan-v { animation: sendScanV 9s linear infinite; animation-delay: -3s; }
@keyframes sendRotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
.send-rotate { animation: sendRotate 4s linear infinite; }
.send-rotate-slow { animation: sendRotate 22s linear infinite; }
.send-rotate-reverse { animation: sendRotate 30s linear infinite reverse; }
@keyframes sendShimmer {
  0%, 100% { filter: drop-shadow(0 0 25px rgba(6,182,212,0.45)) drop-shadow(0 0 35px rgba(232,121,249,0.3)); }
  50% { filter: drop-shadow(0 0 40px rgba(6,182,212,0.65)) drop-shadow(0 0 50px rgba(232,121,249,0.5)) drop-shadow(0 0 60px rgba(251,191,36,0.35)); }
}
.send-shimmer { animation: sendShimmer 3.5s ease-in-out infinite; }
@keyframes sendPulseDot {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.45; transform: scale(0.75); }
}
.send-pulse-dot { animation: sendPulseDot 1.5s ease-in-out infinite; }
@keyframes sendPulseStrong {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.7; transform: scale(1.35); }
}
.send-pulse-strong { animation: sendPulseStrong 1.3s ease-in-out infinite; }
@keyframes sendPulseBg {
  0%, 100% { box-shadow: 0 0 32px rgba(251,191,36,0.55), inset 0 0 22px rgba(255,255,255,0.6); }
  50% { box-shadow: 0 0 48px rgba(251,191,36,0.75), inset 0 0 28px rgba(255,255,255,0.75); }
}
.send-pulse-bg { animation: sendPulseBg 4s ease-in-out infinite; box-shadow: 0 0 32px rgba(251,191,36,0.55), inset 0 0 22px rgba(255,255,255,0.6); }
@keyframes sendUavHover {
  0%, 100% { transform: translate(0, 0); }
  25% { transform: translate(-3px, -4px); }
  50% { transform: translate(0, -7px); }
  75% { transform: translate(3px, -4px); }
}
.send-uav-hover { animation: sendUavHover 4s ease-in-out infinite; }
@keyframes sendUavShadow {
  0%, 100% { opacity: 0.25; transform: scale(1); }
  50% { opacity: 0.1; transform: scale(0.75); }
}
.send-uav-shadow { animation: sendUavShadow 4s ease-in-out infinite; transform-origin: center; transform-box: fill-box; }
@keyframes sendRotorCw { to { transform: rotate(360deg); } }
.send-rotor-cw { animation: sendRotorCw 0.12s linear infinite; }
@keyframes sendRotorCcw { to { transform: rotate(-360deg); } }
.send-rotor-ccw { animation: sendRotorCcw 0.12s linear infinite; }
@keyframes sendBeacon {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.25; }
}
.send-beacon { animation: sendBeacon 0.9s ease-in-out infinite; }
@keyframes sendUgvBob {
  0%, 100% { transform: translate(0, 0) rotate(0deg); }
  20% { transform: translate(0, -1.5px) rotate(-0.6deg); }
  40% { transform: translate(0, 0) rotate(0deg); }
  60% { transform: translate(0, -2px) rotate(0.8deg); }
  80% { transform: translate(0, -0.5px) rotate(-0.3deg); }
}
.send-ugv-bob { animation: sendUgvBob 1.2s ease-in-out infinite; transform-origin: 70px 95px; transform-box: fill-box; }
@keyframes sendWheelSpin { to { transform: rotate(-720deg); } }
.send-wheel-spin { animation: sendWheelSpin 0.8s linear infinite; }
@keyframes sendGroundScroll { from { stroke-dashoffset: 0; } to { stroke-dashoffset: -18; } }
.send-ground-scroll { animation: sendGroundScroll 0.5s linear infinite; }
@keyframes sendAntennaPulse {
  0%, 100% { opacity: 1; r: 2.5; }
  50% { opacity: 0.4; r: 1.5; }
}
.send-antenna-pulse { animation: sendAntennaPulse 1s ease-in-out infinite; }
@keyframes sendCameraPulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.35; }
}
.send-camera-pulse { animation: sendCameraPulse 1.3s ease-in-out infinite; }
@keyframes sendSignal {
  0% { opacity: 0; }
  40% { opacity: 0.8; }
  100% { opacity: 0; }
}
.send-signal-1 { animation: sendSignal 1.2s ease-in-out infinite; }
.send-signal-2 { animation: sendSignal 1.2s ease-in-out infinite; animation-delay: -0.4s; }
@keyframes sendHeadlight {
  0%, 100% { opacity: 0.15; }
  50% { opacity: 0.4; }
}
.send-headlight { animation: sendHeadlight 1.5s ease-in-out infinite; }
@keyframes sendBar1 { 0%, 100% { height: 40%; } 50% { height: 85%; } }
@keyframes sendBar2 { 0%, 100% { height: 72%; } 50% { height: 28%; } }
@keyframes sendBar3 { 0%, 100% { height: 55%; } 50% { height: 95%; } }
@keyframes sendBar4 { 0%, 100% { height: 85%; } 50% { height: 42%; } }
@keyframes sendBar5 { 0%, 100% { height: 30%; } 50% { height: 70%; } }
.send-bar-1 { animation: sendBar1 1.2s ease-in-out infinite; }
.send-bar-2 { animation: sendBar2 1.4s ease-in-out infinite; }
.send-bar-3 { animation: sendBar3 1.6s ease-in-out infinite; }
.send-bar-4 { animation: sendBar4 1.3s ease-in-out infinite; }
.send-bar-5 { animation: sendBar5 1.5s ease-in-out infinite; }
</style>
