import React, { useState, useEffect, useRef } from 'react';
import { Dice1, Dice2, Dice3, Dice4, Dice5, Dice6, Trophy, Users, Activity, Brain, Smile, Music, Star, RotateCcw, ArrowRight, ArrowDown, ArrowLeft, ArrowUp, Heart, Sun, Coffee, Volume2, Hand, Palette, Sparkles, Loader2, Zap, Wand2, Edit3, Check, Magnet, Shield, Gift, ThumbsUp } from 'lucide-react';

// --- Gemini API 設定 ---
const apiKey = ""; // 執行環境會自動填入 API Key

// --- 鼓勵話語清單 ---
const ENCOURAGING_PHRASES = [
  "太棒了！",
  "做得好！",
  "真厲害！",
  "活力滿滿！",
  "給您拍拍手！",
  "就是這樣！",
  "太優秀了！",
  "好樣的！"
];

// --- 懷舊配色與資料設定 ---

// 棋盤格子資料 (22格)
const BOARD_DATA = [
  // 上排 (左 -> 右)
  { id: 0, type: 'start', title: '起點', desc: '準備出發！', color: 'bg-amber-200', border: 'border-amber-600', points: 0, icon: <Star size={20} />, emoji: '🚩' },
  { id: 1, type: 'exercise', title: '摘蘋果', desc: '雙手向上伸展，左抓一下、右抓一下，共做10下！', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '🍎' },
  { id: 2, type: 'brain', title: '動動腦', desc: '請問大家：你最喜歡的水果是什麼？請3位回答。', color: 'bg-slate-200', border: 'border-slate-400', points: 10, icon: <Brain size={20} />, emoji: '🥣' },
  { id: 3, type: 'fun', title: '給個讚', desc: '轉頭跟旁邊的夥伴比個「讚」，大聲說「你好棒」！', color: 'bg-emerald-100', border: 'border-emerald-500', points: 5, icon: <Smile size={20} />, emoji: '👍' },
  { id: 4, type: 'exercise', title: '踏步走', desc: '坐在椅子上，原地踏步數20下，手也要擺動喔！', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '👞' },
  { id: 5, type: 'exercise', title: '聳聳肩', desc: '肩膀用力縮起來～再放鬆掉下來，做10次放鬆肩膀。', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '🤷' },
  { id: 6, type: 'chance', title: '機會', desc: '這組最有精神嗎？老師覺得是的話加 20 分！', color: 'bg-orange-100', border: 'border-orange-500', points: 20, icon: <Sun size={20} />, emoji: '🎁' },
  { id: 7, type: 'song', title: '懷舊曲', desc: '一起唱一段「望春風」或「甜蜜蜜」！', color: 'bg-indigo-100', border: 'border-indigo-400', points: 15, icon: <Music size={20} />, emoji: '🎵' },
  
  // 右排 (上 -> 下)
  { id: 8, type: 'brain', title: '水果點名', desc: '請全組一起說出 3 種「紅色的水果」！', color: 'bg-slate-200', border: 'border-slate-400', points: 15, icon: <Brain size={20} />, emoji: '🍉' },
  { id: 9, type: 'exercise', title: '轉脖子', desc: '頭慢慢轉向左邊，再轉向右邊，放鬆脖子，做5次。', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '😌' },
  { id: 10, type: 'brain', title: '算數', desc: '10 隻手指頭，減掉 3 隻，還剩幾隻？', color: 'bg-slate-200', border: 'border-slate-400', points: 15, icon: <Brain size={20} />, emoji: '🖐️' },
  
  // 下排 (右 -> 左)
  { id: 11, type: 'exercise', title: '彈鋼琴', desc: '手指頭動一動，像在彈鋼琴或是打字，動30秒！', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Hand size={20} />, emoji: '🎹' },
  { id: 12, type: 'rest', title: '喝茶趣', desc: '深呼吸放鬆～休息一回合(但在原地加5分)。', color: 'bg-stone-200', border: 'border-stone-500', points: 5, icon: <Coffee size={20} />, emoji: '🍵' },
  { id: 13, type: 'exercise', title: '抱大樹', desc: '雙手打開像擁抱大樹，做擴胸運動10下！', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '🌳' },
  { id: 14, type: 'fun', title: '大笑', desc: '全組一起大聲「哈！哈！哈！」三聲，把煩惱笑出來！', color: 'bg-emerald-100', border: 'border-emerald-500', points: 10, icon: <Smile size={20} />, emoji: '😆' },
  { id: 15, type: 'exercise', title: '抬膝蓋', desc: '坐穩了，左腳抬起來、右腳抬起來，像在走路，做20下。', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '🦵' },
  { id: 16, type: 'exercise', title: '轉手腕', desc: '雙手握拳轉手腕，順時針10圈，逆時針10圈。', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Activity size={20} />, emoji: '✊' },
  { id: 17, type: 'brain', title: '猜拳', desc: '跟老師猜拳，贏的人舉手！', color: 'bg-slate-200', border: 'border-slate-400', points: 15, icon: <Brain size={20} />, emoji: '✌️' },
  { id: 18, type: 'exercise', title: '抓抓樂', desc: '手掌用力張開，再用力握拳，反覆做10次，促進血液循環。', color: 'bg-rose-100', border: 'border-rose-400', points: 10, icon: <Hand size={20} />, emoji: '👐' },

  // 左排 (下 -> 上)
  { id: 19, type: 'chance', title: '好運', desc: '直接前進 2 格！(並執行那格任務)', color: 'bg-orange-100', border: 'border-orange-500', points: 0, icon: <Heart size={20} />, emoji: '🍀' },
  { id: 20, type: 'song', title: '接歌', desc: '老師唱一句，該組接下一句！', color: 'bg-indigo-100', border: 'border-indigo-400', points: 15, icon: <Music size={20} />, emoji: '🎤' },
  { id: 21, type: 'brain', title: '顏色題', desc: '找找看，今天誰的身上有「紅色」的東西？', color: 'bg-slate-200', border: 'border-slate-400', points: 15, icon: <Palette size={20} />, emoji: '🎨' },
];

const DEFAULT_TEAMS = [
  { name: '紅龜粿', emoji: '🐢', bg: 'bg-red-500', text: 'text-white', border: 'border-red-700' },
  { name: '藍白拖', emoji: '🩴', bg: 'bg-blue-500', text: 'text-white', border: 'border-blue-700' },
  { name: '綠郵筒', emoji: '📮', bg: 'bg-green-500', text: 'text-white', border: 'border-green-700' },
  { name: '旺來隊', emoji: '🍍', bg: 'bg-yellow-400', text: 'text-black', border: 'border-yellow-600' },
];

// 格子在 8x5 Grid 中的位置設定 (順時針繞圈)
const TILE_POSITIONS = [
  // Top Row (0-7)
  { col: 1, row: 1 }, { col: 2, row: 1 }, { col: 3, row: 1 }, { col: 4, row: 1 }, 
  { col: 5, row: 1 }, { col: 6, row: 1 }, { col: 7, row: 1 }, { col: 8, row: 1 },
  // Right Column (8-10)
  { col: 8, row: 2 }, { col: 8, row: 3 }, { col: 8, row: 4 },
  // Bottom Row (11-18)
  { col: 8, row: 5 }, { col: 7, row: 5 }, { col: 6, row: 5 }, { col: 5, row: 5 },
  { col: 4, row: 5 }, { col: 3, row: 5 }, { col: 2, row: 5 }, { col: 1, row: 5 },
  // Left Column (19-21)
  { col: 1, row: 4 }, { col: 1, row: 3 }, { col: 1, row: 2 }
];

const DiceIcon = ({ value }) => {
  const size = 64; 
  switch (value) {
    case 1: return <Dice1 size={size} />;
    case 2: return <Dice2 size={size} />;
    case 3: return <Dice3 size={size} />;
    case 4: return <Dice4 size={size} />;
    case 5: return <Dice5 size={size} />;
    case 6: return <Dice6 size={size} />;
    default: return <Dice1 size={size} />;
  }
};

const App = () => {
  // Game State: 'setup-count', 'setup-names', 'playing', 'modal', 'winner', 'moving'
  const [gameState, setGameState] = useState('setup-count');
  const [teams, setTeams] = useState([]);
  const [tempTeamNames, setTempTeamNames] = useState([]);
  const [teamCount, setTeamCount] = useState(2);
  
  const [currentTurnIndex, setCurrentTurnIndex] = useState(0);
  const [diceValue, setDiceValue] = useState(1);
  const [isRolling, setIsRolling] = useState(false);
  const [activeTask, setActiveTask] = useState(null);
  const [winner, setWinner] = useState(null);
  const [isSpeaking, setIsSpeaking] = useState(false);
  const [isAiLoading, setIsAiLoading] = useState(false);
  const [encouragement, setEncouragement] = useState(null); // 鼓勵話語狀態
  
  // Card System State
  const [showCardMenu, setShowCardMenu] = useState(false);
  // cardTargetMode: null | 'attack' | 'steal'
  const [cardTargetMode, setCardTargetMode] = useState(null);

  // --- Gemini AI API 呼叫邏輯 ---
  const callGeminiAPI = async (prompt) => {
    try {
      setIsAiLoading(true);
      const response = await fetch(
        `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`,
        {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({
            contents: [{ parts: [{ text: prompt }] }],
            generationConfig: {
              responseMimeType: "application/json",
              responseSchema: {
                type: "OBJECT",
                properties: {
                  title: { type: "STRING" },
                  desc: { type: "STRING" }
                }
              }
            }
          }),
        }
      );
      if (!response.ok) throw new Error('API Error');
      const data = await response.json();
      return JSON.parse(data.candidates[0].content.parts[0].text);
    } catch (error) {
      console.error('Gemini API Error:', error);
      return null;
    } finally {
      setIsAiLoading(false);
    }
  };

  const generateAiTask = async (currentTask) => {
    // 增加隨機風格，讓題目更多變
    const vibes = ["有趣好笑", "簡單輕鬆", "稍微挑戰", "懷舊溫馨", "充滿活力", "意想不到"];
    const randomVibe = vibes[Math.floor(Math.random() * vibes.length)];

    let prompt = "";
    if (currentTask.type === 'exercise') {
      prompt = `請產生一個適合 65 歲以上長者、可以坐在椅子上完成的簡單肢體運動任務。風格要「${randomVibe}」。請提供一個簡短的「title」(4個字以內) 和詳細但簡單的「desc」(操作步驟)。例如：title: '抬抬腿', desc: '左腳抬起停3秒，換右腳，重複5次。' 請使用繁體中文。`;
    } else if (currentTask.type === 'brain') {
      prompt = `請產生一個適合長者的簡單認知或懷舊問答題。風格要「${randomVibe}」。請提供「title」(如：動動腦) 和「desc」(問題內容)。問題要與台灣早期生活、食物、節慶或簡單算術有關。例如：title: '猜謎語', desc: '身穿綠衣裳，肚子紅通通，吐出黑點點，請問是什麼水果？' 請使用繁體中文。`;
    } else if (currentTask.type === 'song') {
      prompt = `請產生一個適合長者的唱歌任務。風格要「${randomVibe}」。請提供「title」(如：唱老歌) 和「desc」。內容請指定一首台灣 50-80 年代的經典國語或台語老歌，並要求大家一起唱一小段。例如：title: '月亮代表', desc: '請大家一起唱「月亮代表我的心」的副歌！' 請使用繁體中文。`;
    } else {
      prompt = `請產生一個適合長者的簡單互動任務，包含 title 和 desc。風格要「${randomVibe}」。請使用繁體中文。`;
    }
    
    const aiResult = await callGeminiAPI(prompt);
    if (aiResult) {
      setActiveTask(prev => ({ ...prev, title: aiResult.title, desc: aiResult.desc }));
    } else {
      alert("AI 正在休息中，請稍後再試！");
    }
  };

  // --- 音效功能 ---

  const playSound = (type) => {
    try {
      const AudioContext = window.AudioContext || window.webkitAudioContext;
      if (!AudioContext) return;
      const ctx = new AudioContext();
      const now = ctx.currentTime;
      const osc = ctx.createOscillator();
      const gain = ctx.createGain();
      osc.connect(gain);
      gain.connect(ctx.destination);

      if (type === 'roll') {
        osc.frequency.setValueAtTime(800, now);
        osc.frequency.exponentialRampToValueAtTime(100, now + 0.05);
        osc.type = 'square';
        osc.start(now);
        gain.gain.setValueAtTime(0.05, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.05);
        osc.stop(now + 0.05);
      } else if (type === 'step') { // 腳步聲
        osc.frequency.setValueAtTime(300, now);
        osc.frequency.linearRampToValueAtTime(100, now + 0.1);
        osc.type = 'triangle';
        osc.start(now);
        gain.gain.setValueAtTime(0.05, now);
        gain.gain.linearRampToValueAtTime(0, now + 0.1);
        osc.stop(now + 0.1);
      } else if (type === 'win') {
        const notes = [523.25, 659.25, 783.99, 1046.50];
        notes.forEach((freq, index) => {
          const o = ctx.createOscillator();
          const g = ctx.createGain();
          o.connect(g);
          g.connect(ctx.destination);
          o.frequency.value = freq;
          o.type = 'sine';
          o.start(now + index * 0.1);
          g.gain.setValueAtTime(0.01, now + index * 0.1);
          g.gain.linearRampToValueAtTime(0.2, now + index * 0.1 + 0.05);
          g.gain.exponentialRampToValueAtTime(0.001, now + index * 0.1 + 0.4);
          o.stop(now + index * 0.1 + 0.45);
        });
      } else if (type === 'applause') {
        const bufferSize = ctx.sampleRate * 2; 
        const buffer = ctx.createBuffer(1, bufferSize, ctx.sampleRate);
        const data = buffer.getChannelData(0);
        for (let i = 0; i < bufferSize; i++) {
          data[i] = (Math.random() * 2 - 1) * 0.5;
        }
        for(let i=0; i<15; i++) {
           const noise = ctx.createBufferSource();
           noise.buffer = buffer;
           const noiseGain = ctx.createGain();
           noise.connect(noiseGain);
           noiseGain.connect(ctx.destination);
           const startTime = now + Math.random() * 1.5;
           noise.start(startTime);
           noiseGain.gain.setValueAtTime(0, startTime);
           noiseGain.gain.linearRampToValueAtTime(0.1, startTime + 0.01);
           noiseGain.gain.exponentialRampToValueAtTime(0.001, startTime + 0.1);
           noise.stop(startTime + 0.15);
        }
      } else if (type === 'zap') {
         osc.frequency.setValueAtTime(400, now);
         osc.frequency.linearRampToValueAtTime(100, now + 0.3);
         osc.type = 'sawtooth';
         osc.start(now);
         gain.gain.setValueAtTime(0.1, now);
         gain.gain.linearRampToValueAtTime(0, now + 0.3);
         osc.stop(now + 0.3);
      } else if (type === 'magic') {
         osc.frequency.setValueAtTime(600, now);
         osc.frequency.linearRampToValueAtTime(1200, now + 0.5);
         osc.type = 'triangle';
         osc.start(now);
         gain.gain.setValueAtTime(0.05, now);
         gain.gain.linearRampToValueAtTime(0, now + 0.5);
         osc.stop(now + 0.5);
      } else if (type === 'shield') {
         osc.frequency.setValueAtTime(200, now);
         osc.frequency.exponentialRampToValueAtTime(50, now + 0.2);
         osc.type = 'square';
         osc.start(now);
         gain.gain.setValueAtTime(0.1, now);
         gain.gain.linearRampToValueAtTime(0, now + 0.2);
         osc.stop(now + 0.2);
      } else if (type === 'steal') {
         osc.frequency.setValueAtTime(1200, now);
         osc.frequency.exponentialRampToValueAtTime(400, now + 0.2);
         osc.type = 'sine';
         osc.start(now);
         gain.gain.setValueAtTime(0.1, now);
         gain.gain.linearRampToValueAtTime(0, now + 0.2);
         osc.stop(now + 0.2);
      }
    } catch (e) {}
  };

  // TTS
  const speakText = (text) => {
    if (!('speechSynthesis' in window)) return;
    window.speechSynthesis.cancel();
    const utterance = new SpeechSynthesisUtterance(text);
    utterance.lang = 'zh-TW'; 
    utterance.rate = 0.9;
    utterance.pitch = 1.0;
    utterance.onstart = () => setIsSpeaking(true);
    utterance.onend = () => setIsSpeaking(false);
    utterance.onerror = () => setIsSpeaking(false);
    window.speechSynthesis.speak(utterance);
  };

  useEffect(() => {
    if (activeTask && !isAiLoading) {
      const timer = setTimeout(() => {
        speakText(`${activeTask.title}。${activeTask.desc}`);
      }, 500);
      return () => clearTimeout(timer);
    } else {
      // Don't cancel speech immediately on task close, 
      // let encouragement finish if any, handled in completeTask
      if (!encouragement) {
          setIsSpeaking(false);
      }
    }
  }, [activeTask, isAiLoading]);

  useEffect(() => {
    if (gameState === 'winner') {
       setTimeout(() => playSound('applause'), 500);
    }
  }, [gameState]);

  // --- Game Flow Logic ---

  const initSetupNames = (count) => {
    setTeamCount(count);
    const initialNames = DEFAULT_TEAMS.slice(0, count).map(t => t.name);
    setTempTeamNames(initialNames);
    setGameState('setup-names');
  };

  const finalizeSetup = () => {
    const newTeams = Array.from({ length: teamCount }, (_, i) => ({
      id: i,
      name: tempTeamNames[i] || DEFAULT_TEAMS[i].name,
      emoji: DEFAULT_TEAMS[i].emoji,
      colorData: DEFAULT_TEAMS[i],
      position: 0,
      score: 0,
      laps: 0,
      shield: 0, 
      cards: { attack: 1, bonus: 1, steal: 1, shield: 1, share: 1 } 
    }));
    setTeams(newTeams);
    setGameState('playing');
    setCurrentTurnIndex(0);
  };

  const handleRollDice = () => {
    if (isRolling || cardTargetMode || gameState !== 'playing') return;
    setIsRolling(true);
    setShowCardMenu(false); // Hide menu when rolling
    let count = 0;
    const interval = setInterval(() => {
      setDiceValue(Math.floor(Math.random() * 6) + 1);
      playSound('roll');
      count++;
      if (count > 10) {
        clearInterval(interval);
        const finalValue = Math.floor(Math.random() * 6) + 1;
        setDiceValue(finalValue);
        setIsRolling(false);
        movePlayer(finalValue);
      }
    }, 100);
  };

  // 處理格子觸發邏輯 (移動結束後)
  const handleLandOnTile = (tileIndex) => {
    const landedTile = BOARD_DATA[tileIndex];
    
    // 特殊格子：好運 (ID 19) -> 再前進 2 格
    if (landedTile.id === 19) {
        // 先顯示好運提示，再移動
        speakText("好運降臨！再前進兩格！");
        setTimeout(() => {
            movePlayer(2); // 遞迴呼叫移動
        }, 1500);
    } else {
        setTimeout(() => openTaskModal(landedTile), 500);
    }
  };

  // 一格一格移動動畫
  const movePlayer = (totalSteps) => {
    let currentTeamPos = teams[currentTurnIndex].position;
    let stepsRemaining = totalSteps;

    const animateStep = () => {
      if (stepsRemaining <= 0) {
        handleLandOnTile(currentTeamPos); // 移動結束，處理落點
        return;
      }

      stepsRemaining--;
      currentTeamPos++;
      let lapBonus = false;

      // 處理繞圈
      if (currentTeamPos >= BOARD_DATA.length) {
        currentTeamPos = 0;
        lapBonus = true;
      }

      // 更新狀態
      setTeams(prev => {
        const newTeams = [...prev];
        const team = newTeams[currentTurnIndex];
        team.position = currentTeamPos;
        if (lapBonus) {
           team.laps += 1;
           team.score += 20;
        }
        return newTeams;
      });
      
      playSound('step'); // 播放腳步聲
      setTimeout(animateStep, 600); // 每 0.6 秒走一格，讓長輩看清楚
    };

    setGameState('moving'); // 暫時鎖定狀態避免重複操作
    animateStep();
  };

  const openTaskModal = (tile) => {
    setActiveTask(tile);
    setGameState('modal');
  };

  const completeTask = (success) => {
    if (success && activeTask) {
      setTeams(prev => {
        const newTeams = [...prev];
        newTeams[currentTurnIndex].score += activeTask.points;
        return newTeams;
      });
      
      // 顯示並朗讀鼓勵話語
      const phrase = ENCOURAGING_PHRASES[Math.floor(Math.random() * ENCOURAGING_PHRASES.length)];
      setEncouragement(phrase);
      playSound('win');
      speakText(`${phrase} 加 ${activeTask.points} 分！`);

      // 2.5秒後關閉鼓勵並換人
      setTimeout(() => {
          setEncouragement(null);
          setActiveTask(null);
          setGameState('playing');
          setCurrentTurnIndex((prev) => (prev + 1) % teams.length);
      }, 2500);

    } else {
      // 失敗或跳過，直接換人
      setActiveTask(null);
      setGameState('playing');
      setCurrentTurnIndex((prev) => (prev + 1) % teams.length);
    }
  };

  // --- Card Logic ---

  const useBonusCard = () => {
    const team = teams[currentTurnIndex];
    if (team.cards.bonus <= 0) return;
    setTeams(prev => {
      const newTeams = [...prev];
      newTeams[currentTurnIndex].score += 30;
      newTeams[currentTurnIndex].cards.bonus -= 1;
      return newTeams;
    });
    playSound('magic');
    alert(`✨ ${team.name} 使用了「加分卡」！\n自己加 30 分！`);
    setShowCardMenu(false);
  };

  const useShieldCard = () => {
    const team = teams[currentTurnIndex];
    if (team.cards.shield <= 0) return;
    setTeams(prev => {
      const newTeams = [...prev];
      newTeams[currentTurnIndex].shield += 1;
      newTeams[currentTurnIndex].cards.shield -= 1;
      return newTeams;
    });
    playSound('magic');
    alert(`🛡️ ${team.name} 使用了「平安卡」！\n獲得一層防護罩！`);
    setShowCardMenu(false);
  };

  const useShareCard = () => {
    const team = teams[currentTurnIndex];
    if (team.cards.share <= 0) return;
    setTeams(prev => {
      const newTeams = prev.map(t => ({ ...t, score: t.score + 10 }));
      newTeams[currentTurnIndex].cards.share -= 1;
      return newTeams;
    });
    playSound('win');
    alert(`🎁 ${team.name} 使用了「同樂卡」！\n大家一起加 10 分！`);
    setShowCardMenu(false);
  };

  const startTargetSelection = (mode) => {
    const team = teams[currentTurnIndex];
    if (mode === 'attack' && team.cards.attack <= 0) return;
    if (mode === 'steal' && team.cards.steal <= 0) return;
    setCardTargetMode(mode);
    setShowCardMenu(false);
    const actionName = mode === 'attack' ? '攻擊' : '偷分';
    alert(`請點擊畫面下方的「隊伍列表」選擇要${actionName}的對象！`);
  };

  const confirmTarget = (targetTeamId) => {
    if (!cardTargetMode || targetTeamId === currentTurnIndex) return;
    setTeams(prev => {
      const newTeams = [...prev];
      const target = newTeams[targetTeamId];
      const attacker = newTeams[currentTurnIndex];
      
      if (target.shield > 0) {
         target.shield -= 1;
         playSound('shield');
         alert(`🛡️ ${target.name} 的平安符生效了！\n擋住了這次的${cardTargetMode === 'attack' ? '攻擊' : '偷襲'}！`);
         if (cardTargetMode === 'attack') attacker.cards.attack -= 1;
         else attacker.cards.steal -= 1;
         return newTeams;
      }

      if (cardTargetMode === 'attack') {
        attacker.cards.attack -= 1;
        target.score = Math.max(0, target.score - 10);
        playSound('zap');
        alert(`⚡ 攻擊成功！${target.name} 被扣了 10 分！`);
      } else if (cardTargetMode === 'steal') {
        attacker.cards.steal -= 1;
        const stolen = Math.min(10, target.score);
        target.score -= stolen;
        attacker.score += stolen;
        playSound('steal');
        alert(`🧲 偷分成功！從 ${target.name} 偷走了 ${stolen} 分！`);
      }
      return newTeams;
    });
    setCardTargetMode(null);
  };

  const endGame = () => {
    const sorted = [...teams].sort((a, b) => b.score - a.score);
    setWinner(sorted[0]);
    setGameState('winner');
  };

  const resetGame = () => {
    setGameState('setup-count');
    setTeams([]);
    setWinner(null);
    setDiceValue(1);
    setShowCardMenu(false);
    setCardTargetMode(null);
  };

  // --- Render Components ---

  // 1. 童趣設定畫面
  if (gameState.startsWith('setup')) {
    return (
      <div className="min-h-screen bg-yellow-50 flex flex-col items-center justify-center p-4 font-sans text-stone-700 relative overflow-hidden">
        <div className="absolute top-10 left-10 text-pink-300 opacity-50 transform -rotate-12"><Star size={80} fill="currentColor" /></div>
        <div className="absolute bottom-10 right-10 text-blue-300 opacity-50 transform rotate-12"><Smile size={80} /></div>
        
        <div className="bg-white border-4 border-dashed border-orange-300 p-8 rounded-[3rem] shadow-xl max-w-2xl w-full text-center relative z-10">
          <div className="flex justify-center mb-4">
             <div className="bg-orange-100 p-4 rounded-full">
               <Users size={48} className="text-orange-500" />
             </div>
          </div>
          
          <h1 className="text-4xl font-bold mb-2 text-orange-600 tracking-wider">長者運動大富翁</h1>
          <p className="text-gray-500 mb-8 text-xl">建立您的隊伍來開始比賽吧！</p>

          {gameState === 'setup-count' ? (
            <div className="space-y-6 animate-in slide-in-from-bottom duration-500">
               <p className="text-2xl font-bold mb-4">請問有幾組要玩？</p>
               <div className="flex justify-center gap-4 flex-wrap">
                 {[2, 3, 4].map(num => (
                   <button
                     key={num}
                     onClick={() => initSetupNames(num)}
                     className="bg-blue-100 hover:bg-blue-200 text-blue-700 border-2 border-blue-300 text-3xl font-bold w-24 h-24 rounded-2xl flex items-center justify-center shadow-sm transition-transform hover:scale-110"
                   >
                     {num}
                   </button>
                 ))}
               </div>
            </div>
          ) : (
            <div className="space-y-6 animate-in slide-in-from-right duration-500">
               <p className="text-2xl font-bold mb-4">幫隊伍取個好聽的名字！</p>
               <div className="grid grid-cols-1 gap-4 max-h-[40vh] overflow-auto px-4">
                 {Array.from({length: teamCount}).map((_, idx) => (
                   <div key={idx} className="flex items-center gap-3 bg-gray-50 p-3 rounded-xl border border-gray-200">
                      <span className="text-3xl">{DEFAULT_TEAMS[idx].emoji}</span>
                      <input 
                        type="text" 
                        value={tempTeamNames[idx]}
                        onChange={(e) => {
                          const newNames = [...tempTeamNames];
                          newNames[idx] = e.target.value;
                          setTempTeamNames(newNames);
                        }}
                        className="flex-1 bg-white border-2 border-gray-300 rounded-lg px-4 py-2 text-2xl font-bold text-gray-700 focus:border-orange-400 focus:outline-none"
                      />
                   </div>
                 ))}
               </div>
               <div className="flex gap-4 justify-center mt-6">
                 <button onClick={() => setGameState('setup-count')} className="px-6 py-3 rounded-xl bg-gray-200 text-gray-600 font-bold hover:bg-gray-300 text-lg">
                    回上一步
                 </button>
                 <button onClick={finalizeSetup} className="px-8 py-3 rounded-xl bg-green-500 text-white font-bold text-xl hover:bg-green-600 shadow-lg flex items-center gap-2">
                    開始遊戲 <ArrowRight />
                 </button>
               </div>
            </div>
          )}
        </div>
      </div>
    );
  }

  // 2. 獲勝畫面
  if (gameState === 'winner') {
    return (
      <div className="min-h-screen bg-yellow-50 flex flex-col items-center justify-center p-4 font-sans relative overflow-hidden">
        <div className="absolute inset-0 overflow-hidden pointer-events-none">
           {[...Array(20)].map((_, i) => (
              <div key={i} className="absolute rounded-full opacity-30 animate-pulse" 
                   style={{
                     left: `${Math.random()*100}%`, 
                     top: `${Math.random()*100}%`,
                     width: `${Math.random()*50 + 20}px`,
                     height: `${Math.random()*50 + 20}px`,
                     backgroundColor: ['#FFD700', '#FF69B4', '#00BFFF', '#32CD32'][Math.floor(Math.random()*4)],
                     animationDelay: `${Math.random()*2}s`
                   }} 
              />
           ))}
        </div>

        <div className="bg-white p-10 rounded-[3rem] shadow-2xl text-center max-w-2xl w-full border-8 border-yellow-300 relative z-10 animate-in zoom-in duration-500">
          <Trophy size={100} className="text-yellow-500 mx-auto mb-6 drop-shadow-lg" />
          <h1 className="text-5xl font-black text-red-500 mb-6">恭喜獲勝！</h1>
          
          <div className="bg-yellow-50 rounded-2xl p-6 mb-8 inline-block border-2 border-yellow-200">
             <div className="text-6xl mb-2">{winner?.emoji}</div>
             <div className="text-4xl font-bold text-gray-800">{winner?.name}</div>
             <div className="text-3xl font-bold text-orange-600 mt-2">總分：{winner?.score}</div>
          </div>
          
          <div className="space-y-3 mb-8 text-left max-h-[30vh] overflow-auto">
            {[...teams].sort((a,b) => b.score - a.score).map((t, idx) => (
              <div key={t.id} className="flex justify-between items-center p-3 bg-gray-50 rounded-xl">
                <span className="font-bold text-gray-600 flex items-center gap-2 text-xl">
                  <span className={`w-8 h-8 rounded-full flex items-center justify-center text-white text-sm font-bold ${idx===0?'bg-yellow-500':'bg-gray-400'}`}>{idx+1}</span>
                  <span>{t.emoji} {t.name}</span>
                </span>
                <span className="font-bold text-gray-800 text-xl">{t.score} 分</span>
              </div>
            ))}
          </div>

          <button
            onClick={resetGame}
            className="bg-green-500 text-white text-3xl py-4 px-12 rounded-full hover:bg-green-600 shadow-xl font-bold transform transition hover:scale-105"
          >
            再玩一次
          </button>
        </div>
      </div>
    );
  }

  // 3. 遊戲主畫面
  const currentTeam = teams[currentTurnIndex];

  return (
    <div className="min-h-screen bg-[#f0eee5] flex flex-col font-serif text-stone-800 overflow-auto">
      
      {/* Top Bar */}
      <header className="bg-[#e6e2d3] shadow p-2 px-4 flex justify-between items-center z-20 h-[10vh] min-h-[80px] border-b border-stone-300 shrink-0 sticky top-0">
        <h2 className="text-xl md:text-2xl font-bold text-stone-700 flex items-center gap-2 tracking-wide">
          <Activity size={24} /> 樂齡運動會
          <span className="bg-yellow-200 text-yellow-800 text-xs px-2 py-0.5 rounded-full border border-yellow-400 flex items-center gap-1">
             <Sparkles size={10} /> AI
          </span>
        </h2>

        {/* 隊伍列表 */}
        <div className="flex gap-2 overflow-x-auto pb-1 max-w-[60vw]">
           {teams.map(team => (
             <button 
                key={team.id} 
                onClick={() => confirmTarget(team.id)}
                disabled={!cardTargetMode || team.id === currentTurnIndex}
                className={`
                  flex flex-col items-center px-3 py-1 rounded border-2 transition-all min-w-[100px] relative
                  ${team.id === currentTurnIndex ? 'border-yellow-600 bg-yellow-50 scale-105 shadow-md' : 'border-transparent opacity-80 hover:bg-white'}
                  ${cardTargetMode && team.id !== currentTurnIndex ? 'animate-pulse ring-4 ring-red-400 cursor-pointer bg-red-50 opacity-100' : ''}
                `}
             >
                {team.shield > 0 && (
                   <div className="absolute -top-2 -right-2 bg-blue-500 text-white rounded-full p-1 shadow-sm z-10" title="有平安符保護中">
                      <Shield size={12} fill="white" />
                   </div>
                )}
                <div className={`${team.colorData.bg} ${team.colorData.text} px-2 py-0.5 rounded-full text-base font-bold w-full text-center shadow-sm flex items-center justify-center gap-1`}>
                  <span>{team.emoji}</span>
                  <span className="truncate max-w-[80px]">{team.name}</span>
                </div>
                <div className="text-xl font-bold text-stone-700 mt-0.5">{team.score}</div>
             </button>
           ))}
        </div>
        <button onClick={endGame} className="bg-stone-500 text-white px-3 py-1 md:px-4 md:py-2 rounded hover:bg-stone-600 text-sm md:text-base font-bold tracking-wide">
          結束
        </button>
      </header>

      {/* Target Mode Overlay Hint */}
      {cardTargetMode && (
        <div className="bg-red-500 text-white text-center py-2 font-bold animate-pulse sticky top-[10vh] z-30 shadow-md text-lg">
           ⚡ 請點擊上方隊伍列表，選擇要 {cardTargetMode === 'attack' ? '攻擊' : '偷分'} 的對手！
           <button onClick={() => setCardTargetMode(null)} className="ml-4 underline text-sm">取消</button>
        </div>
      )}

      {/* Game Board Container */}
      <div className="flex-1 p-4 flex items-center justify-center relative bg-[#f0eee5] min-h-[600px]">
        
        <div className="grid grid-cols-8 grid-rows-5 gap-2 w-full max-w-[95vw] aspect-[16/9] relative">
          
          {/* Tiles - 字體加大優化 */}
          {BOARD_DATA.map((tile, index) => {
            const pos = TILE_POSITIONS[index];
            const teamsHere = teams.filter(t => t.position === index);

            return (
              <div 
                key={tile.id} 
                style={{ gridColumn: pos.col, gridRow: pos.row }}
                className={`
                  relative border-2 rounded-lg flex flex-col items-center justify-center text-center shadow-sm transition-all overflow-hidden
                  ${tile.color} ${tile.border}
                  ${activeTask?.id === tile.id ? 'ring-4 ring-yellow-500 z-10 scale-105 shadow-xl' : ''}
                `}
              >
                 <span className="absolute top-0.5 left-1 text-xs font-bold text-stone-500 opacity-40">{index + 1}</span>
                <div className="text-3xl md:text-4xl mb-0 leading-none drop-shadow-sm">{tile.emoji}</div>
                <div className="font-bold text-base md:text-lg lg:text-xl text-stone-800 leading-tight px-0.5 mt-0.5 w-full break-words">{tile.title}</div>
                
                {index < 7 && <ArrowRight className="absolute -right-2.5 text-stone-400 opacity-40" size={20} />}
                {index >= 7 && index < 10 && <ArrowDown className="absolute -bottom-2.5 text-stone-400 opacity-40" size={20} />}
                {index >= 10 && index < 18 && <ArrowLeft className="absolute -left-2.5 text-stone-400 opacity-40" size={20} />}
                {index >= 18 && index < 21 && <ArrowUp className="absolute -top-2.5 text-stone-400 opacity-40" size={20} />}

                <div className="absolute bottom-0.5 left-0 right-0 flex justify-center gap-1 px-1 flex-wrap">
                  {teamsHere.map(team => (
                    <div 
                      key={team.id} 
                      className={`w-5 h-5 md:w-6 md:h-6 rounded-full bg-white border-2 border-[#f0eee5] shadow-sm flex items-center justify-center text-xs`}
                      title={team.name}
                    >
                      {team.emoji}
                    </div>
                  ))}
                </div>
              </div>
            );
          })}

          {/* Center Control Area */}
          <div className="col-start-2 col-end-8 row-start-2 row-end-5 bg-[#fffef8] rounded-2xl m-2 border-4 border-double border-stone-300 shadow-inner flex flex-col items-center justify-center p-2 relative">
            
            {/* Current Turn Display */}
            <div className="text-center w-full mb-2">
              <p className="text-xl text-stone-400 font-bold mb-1">現在輪到</p>
              <div className={`text-5xl font-bold ${currentTeam.colorData.text} ${currentTeam.colorData.bg} py-4 px-10 rounded-full shadow-lg ring-4 ring-[#f0eee5] flex items-center justify-center gap-3 inline-flex max-w-full overflow-hidden`}>
                <span>{currentTeam.emoji}</span>
                <span className="truncate">{currentTeam.name}</span>
              </div>
            </div>

            <div className="flex items-center gap-8 mt-6">
                {/* Dice Button */}
                <button 
                  onClick={handleRollDice} 
                  disabled={isRolling || gameState !== 'playing' || cardTargetMode}
                  className={`
                    group relative bg-[#f5f5f0] p-8 rounded-full shadow-lg border-4 border-stone-200 
                    transition-all transform hover:scale-105 active:scale-95 flex-shrink-0
                    ${(gameState !== 'playing' || cardTargetMode) ? 'opacity-50 cursor-not-allowed' : 'hover:border-stone-400 cursor-pointer'}
                  `}
                >
                  <div className={`transition-all duration-300 ${isRolling ? 'animate-spin' : 'group-hover:rotate-12 text-stone-800'}`}>
                      <DiceIcon value={diceValue} />
                  </div>
                  <div className="absolute -bottom-4 left-1/2 transform -translate-x-1/2 bg-stone-700 text-[#f5f5f0] px-4 py-1 rounded text-lg font-bold whitespace-nowrap shadow-md">
                    擲骰子
                  </div>
                </button>

                {/* Card Menu Button */}
                <div className="relative">
                   <button
                     onClick={() => setShowCardMenu(!showCardMenu)}
                     disabled={isRolling || cardTargetMode}
                     className="bg-purple-100 hover:bg-purple-200 text-purple-800 p-5 rounded-2xl border-2 border-purple-300 shadow-md flex flex-col items-center gap-1 disabled:opacity-50 min-w-[140px]"
                   >
                     <div className="flex gap-2 mb-1">
                       <span className="font-bold text-2xl">我的道具</span>
                     </div>
                     <span className="text-sm bg-white/50 px-3 py-0.5 rounded-full font-bold">
                       剩餘 {Object.values(currentTeam.cards).reduce((a,b)=>a+b,0)} 張
                     </span>
                   </button>

                   {/* Popover Menu */}
                   {showCardMenu && (
                     <div className="absolute bottom-full mb-2 left-1/2 -translate-x-1/2 bg-white rounded-xl shadow-xl border border-gray-200 p-3 w-64 z-30 animate-in zoom-in-95 origin-bottom max-h-[60vh] overflow-auto">
                        <h4 className="text-center font-bold text-gray-600 mb-2 text-base border-b pb-1">選擇道具卡</h4>
                        <div className="space-y-2">
                          <button onClick={() => startTargetSelection('attack')} disabled={currentTeam.cards.attack <= 0}
                            className="w-full bg-red-50 hover:bg-red-100 text-red-700 p-3 rounded-lg flex items-center justify-between text-base font-bold disabled:opacity-50">
                             <span className="flex items-center gap-2"><Zap size={20}/> 攻擊卡 <span className="text-xs font-normal">(-10分)</span></span>
                             <span className="bg-white px-2 rounded-full border text-sm">{currentTeam.cards.attack}</span>
                          </button>
                          <button onClick={useBonusCard} disabled={currentTeam.cards.bonus <= 0}
                            className="w-full bg-yellow-50 hover:bg-yellow-100 text-yellow-700 p-3 rounded-lg flex items-center justify-between text-base font-bold disabled:opacity-50">
                             <span className="flex items-center gap-2"><Wand2 size={20}/> 加分卡 <span className="text-xs font-normal">(+30分)</span></span>
                             <span className="bg-white px-2 rounded-full border text-sm">{currentTeam.cards.bonus}</span>
                          </button>
                          <button onClick={() => startTargetSelection('steal')} disabled={currentTeam.cards.steal <= 0}
                            className="w-full bg-blue-50 hover:bg-blue-100 text-blue-700 p-3 rounded-lg flex items-center justify-between text-base font-bold disabled:opacity-50">
                             <span className="flex items-center gap-2"><Magnet size={20}/> 偷分卡 <span className="text-xs font-normal">(搶10分)</span></span>
                             <span className="bg-white px-2 rounded-full border text-sm">{currentTeam.cards.steal}</span>
                          </button>
                          <button onClick={useShieldCard} disabled={currentTeam.cards.shield <= 0}
                            className="w-full bg-slate-50 hover:bg-slate-100 text-slate-700 p-3 rounded-lg flex items-center justify-between text-base font-bold disabled:opacity-50">
                             <span className="flex items-center gap-2"><Shield size={20}/> 平安卡 <span className="text-xs font-normal">(防禦)</span></span>
                             <span className="bg-white px-2 rounded-full border text-sm">{currentTeam.cards.shield}</span>
                          </button>
                           <button onClick={useShareCard} disabled={currentTeam.cards.share <= 0}
                            className="w-full bg-pink-50 hover:bg-pink-100 text-pink-700 p-3 rounded-lg flex items-center justify-between text-base font-bold disabled:opacity-50">
                             <span className="flex items-center gap-2"><Gift size={20}/> 同樂卡 <span className="text-xs font-normal">(全+10)</span></span>
                             <span className="bg-white px-2 rounded-full border text-sm">{currentTeam.cards.share}</span>
                          </button>
                        </div>
                        <div className="mt-2 text-center">
                          <button onClick={() => setShowCardMenu(false)} className="text-sm text-gray-400 underline">關閉</button>
                        </div>
                     </div>
                   )}
                </div>
            </div>
          </div>
        </div>
      </div>

      {/* Encouragement Overlay (鼓勵話語彈窗) */}
      {encouragement && (
         <div className="fixed inset-0 z-[60] flex items-center justify-center pointer-events-none">
            <div className="bg-yellow-400 text-red-600 font-black text-6xl md:text-8xl px-12 py-8 rounded-3xl border-8 border-white shadow-2xl animate-bounce transform rotate-3">
               {encouragement}
            </div>
         </div>
      )}

      {/* Task Modal */}
      {gameState === 'modal' && activeTask && !encouragement && (
        <div className="fixed inset-0 bg-stone-900/60 backdrop-blur-sm flex items-center justify-center z-50 p-4">
          <div className="bg-[#fffef8] rounded-lg shadow-2xl w-full max-w-3xl overflow-hidden transform scale-100 border-8 border-stone-200 animate-in zoom-in-95 duration-300 relative">
             <div className="absolute top-3 left-1/2 transform -translate-x-1/2 w-4 h-4 rounded-full bg-red-800 shadow-sm border border-red-900 z-10"></div>
             
             {isSpeaking && !isAiLoading && (
               <div className="absolute top-4 right-4 text-emerald-600 animate-pulse flex items-center gap-1">
                 <Volume2 size={32} />
                 <span className="text-lg font-bold">朗讀中...</span>
               </div>
             )}

            {/* Modal Header */}
            <div className={`${activeTask.color} p-8 flex items-center justify-center gap-6 border-b-4 ${activeTask.border} border-dashed`}>
              <div className="text-8xl drop-shadow-md">{activeTask.emoji}</div>
              <h2 className="text-6xl font-black text-stone-800 tracking-wide">{activeTask.title}</h2>
            </div>
            
            {/* Modal Body */}
            <div className="p-10 text-center flex flex-col items-center">
              
              <div className="flex gap-6 mb-8 items-center">
                 <div className="bg-yellow-100 text-yellow-900 px-8 py-3 rounded-full border-2 border-yellow-200 text-3xl font-black shadow-sm inline-block">
                  獎勵：{activeTask.points} 分
                 </div>
                 {activeTask.id !== 0 && activeTask.id !== 19 && (
                   <button 
                     onClick={() => generateAiTask(activeTask)}
                     disabled={isAiLoading}
                     className="bg-purple-100 text-purple-900 px-6 py-3 rounded-full border-2 border-purple-200 text-2xl font-bold shadow-sm hover:bg-purple-200 flex items-center gap-2 transition-colors disabled:opacity-50"
                   >
                     {isAiLoading ? <Loader2 className="animate-spin" /> : <Sparkles size={24} />}
                     {isAiLoading ? "思考中..." : "AI 隨機換題"}
                   </button>
                 )}
              </div>
              
              <p className="text-5xl font-bold text-stone-800 leading-snug mb-12 w-full px-6 font-sans min-h-[5rem]">
                {activeTask.desc}
              </p>

              {/* Action Buttons */}
              <div className="grid grid-cols-2 gap-8 w-full px-6">
                <button 
                  onClick={() => completeTask(false)}
                  className="bg-stone-200 hover:bg-stone-300 text-stone-600 text-4xl font-bold py-6 rounded-2xl border-4 border-stone-300 transition-colors"
                >
                  跳過
                </button>
                <button 
                  onClick={() => completeTask(true)}
                  className="bg-emerald-600 hover:bg-emerald-700 text-white text-4xl font-bold py-6 rounded-2xl border-b-8 border-emerald-800 shadow-xl hover:shadow-2xl transition-all transform hover:-translate-y-1 flex items-center justify-center gap-4"
                >
                  <ThumbsUp size={48} /> 完成任務
                </button>
              </div>
            </div>
          </div>
        </div>
      )}

    </div>
  );
};

export default App;
