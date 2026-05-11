<!DOCTYPE html>
<html lang="zh-TW" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>合一生技 - 1142 國際策略管理 G8</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&display=swap');
        
        body {
            font-family: 'Noto Sans TC', sans-serif;
            transition: background-color 0.3s, color 0.3s;
        }

        .dark {
            background-color: #0f172a;
            color: #f1f5f9;
        }

        /* 翻轉字卡樣式 */
        .flip-card {
            background-color: transparent;
            perspective: 1000px;
            height: 320px;
        }
        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        .flip-card:hover .flip-card-inner {
            transform: rotateY(180deg);
        }
        .flip-card-front, .flip-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 2rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
        }
        .flip-card-back {
            transform: rotateY(180deg);
        }

        .nav-link {
            position: relative;
            transition: color 0.3s;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 0;
            background-color: #2563eb;
            transition: width 0.3s;
        }
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-900 transition-colors duration-300">

    <!-- 頂端列 (整合所有功能) -->
    <nav class="fixed w-full z-50 bg-white/90 dark:bg-slate-900/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <!-- Logo -->
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 bg-blue-600 rounded-lg flex items-center justify-center text-white">
                        <i class="fas fa-dna text-xl"></i>
                    </div>
                    <span class="font-bold text-xl tracking-tight text-slate-800 dark:text-white">合一生技 <span class="text-blue-600">G8 Merida</span></span>
                </div>
                
                <!-- 導航選單 (桌面) -->
                <div class="hidden lg:flex items-center space-x-8">
                    <div class="flex space-x-6 text-sm font-medium border-r border-slate-200 dark:border-slate-700 pr-6 mr-6">
                        <a href="#about" class="nav-link" data-en="About" data-zh="公司概況">公司概況</a>
                        <a href="#strategy" class="nav-link" data-en="Strategy" data-zh="策略分析">策略分析</a>
                        <a href="#careers" class="nav-link" data-en="Careers" data-zh="人才招募">人才招募</a>
                        <a href="#quiz" class="nav-link" data-en="Quiz" data-zh="互動測驗">互動測驗</a>
                    </div>
                    
                    <!-- 功能控制區 -->
                    <div class="flex items-center space-x-3">
                        <!-- 語音按鈕 -->
                        <button onclick="speakText()" class="p-2.5 rounded-xl bg-blue-50 dark:bg-blue-900/30 text-blue-600 dark:text-blue-400 hover:scale-105 transition-transform" title="語音導覽">
                            <i class="fas fa-volume-up"></i>
                        </button>
                        <!-- 語言切換 -->
                        <button id="langToggle" class="p-2.5 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 transition-colors flex items-center space-x-2">
                            <i class="fas fa-language text-lg"></i>
                            <span class="text-xs font-bold" id="langText">EN</span>
                        </button>
                        <!-- 明暗模式 -->
                        <button id="themeToggle" class="p-2.5 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 transition-colors">
                            <i class="fas fa-moon dark:hidden"></i>
                            <i class="fas fa-sun hidden dark:block text-yellow-500"></i>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- 英雄區塊 -->
    <section id="home" class="relative pt-44 pb-24 overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <span class="inline-block px-4 py-1.5 mb-6 text-sm font-semibold tracking-wide text-blue-600 uppercase bg-blue-50 dark:bg-blue-900/20 rounded-full" data-en="Oneness Biotech" data-zh="合一生技">合一生技</span>
            <h1 class="text-5xl md:text-7xl font-black mb-8 leading-tight tracking-tight dark:text-white"
                data-en="Pioneering Innovations for Unmet Needs" data-zh="創新研發，解決未被滿足的醫療需求">
                創新研發，解決未被滿足的醫療需求
            </h1>
            <p class="text-xl text-slate-600 dark:text-slate-400 mb-10 max-w-3xl mx-auto leading-relaxed"
               data-en="A global leader in chronic wound healing and immunology, transforming lives through scientific excellence."
               data-zh="全球慢性傷口癒合與免疫學領域的領導者，透過卓越科學改變病患生活。">
                全球慢性傷口癒合與免疫學領域的領導者，透過卓越科學改變病患生活。
            </p>
        </div>
    </section>

    <!-- 公司概況 - 翻轉卡片 -->
    <section id="about" class="py-24 bg-white dark:bg-slate-800/50 transition-colors">
        <div class="max-w-7xl mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4 dark:text-white" data-en="Company Insight" data-zh="公司深度概況">公司深度概況</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto rounded-full"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- 核心願景 -->
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front bg-gradient-to-br from-blue-50 to-white dark:from-slate-700 dark:to-slate-800">
                            <div class="w-16 h-16 bg-blue-100 dark:bg-blue-900/50 rounded-2xl flex items-center justify-center mb-6">
                                <i class="fas fa-eye text-2xl text-blue-600"></i>
                            </div>
                            <h3 class="text-xl font-bold dark:text-white" data-en="Our Vision" data-zh="核心願景">核心願景</h3>
                            <p class="mt-4 text-sm text-slate-500 dark:text-slate-400" data-en="Hover to explore" data-zh="懸停查看詳細資訊">懸停查看詳細資訊</p>
                        </div>
                        <div class="flip-card-back bg-blue-600 text-white">
                            <p class="leading-loose" data-en="Patient-centric R&D focusing on global licensing and fast-track market entry for revolutionary treatments."
                               data-zh="以病患為中心的研發策略，專注於革命性療法的全球授權與快速通關市場進入。">
                               以病患為中心的研發策略，專注於革命性療法的全球授權與快速通關市場進入。
                            </p>
                        </div>
                    </div>
                </div>
                <!-- 財務實力 -->
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front bg-gradient-to-br from-teal-50 to-white dark:from-slate-700 dark:to-slate-800">
                            <div class="w-16 h-16 bg-teal-100 dark:bg-teal-900/50 rounded-2xl flex items-center justify-center mb-6">
                                <i class="fas fa-vault text-2xl text-teal-600"></i>
                            </div>
                            <h3 class="text-xl font-bold dark:text-white" data-en="Financial Health" data-zh="財務實力">財務實力</h3>
                            <p class="mt-4 text-sm text-slate-500 dark:text-slate-400" data-en="Hover to explore" data-zh="懸停查看詳細資訊">懸停查看詳細資訊</p>
                        </div>
                        <div class="flip-card-back bg-teal-600 text-white">
                            <p class="leading-loose" data-en="Maintaining an extremely low-risk capital structure with consistent high-volume investment in long-term R&D."
                               data-zh="維持極低風險的資本結構，並在長期研發中持續投入高額資金，展現穩定韌性。">
                               維持極低風險的資本結構，並在長期研發中持續投入高額資金，展現穩定韌性。
                            </p>
                        </div>
                    </div>
                </div>
                <!-- 國際佈局 -->
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front bg-gradient-to-br from-purple-50 to-white dark:from-slate-700 dark:to-slate-800">
                            <div class="w-16 h-16 bg-purple-100 dark:bg-purple-900/50 rounded-2xl flex items-center justify-center mb-6">
                                <i class="fas fa-globe-americas text-2xl text-purple-600"></i>
                            </div>
                            <h3 class="text-xl font-bold dark:text-white" data-en="Global Reach" data-zh="國際佈局">國際佈局</h3>
                            <p class="mt-4 text-sm text-slate-500 dark:text-slate-400" data-en="Hover to explore" data-zh="懸停查看詳細資訊">懸停查看詳細資訊</p>
                        </div>
                        <div class="flip-card-back bg-purple-600 text-white">
                            <p class="leading-loose" data-en="Successfully entered multiple markets with innovative new drugs, bridging the gap between Taiwan and the world."
                               data-zh="成功將創新藥物推向多國市場，搭起台灣與世界生醫產業的橋樑。">
                               成功將創新藥物推向多國市場，搭起台灣與世界生醫產業的橋樑。
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 策略分析區區塊 -->
    <section id="strategy" class="py-24 dark:bg-slate-900">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-16 dark:text-white" data-en="TP0 Strategic Framework" data-zh="TP0 策略架構分析">TP0 策略架構分析</h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="space-y-8">
                    <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
                        <h4 class="text-lg font-bold mb-4 text-blue-600" data-en="Growth Vector" data-zh="成長路徑">成長路徑</h4>
                        <p class="text-slate-600 dark:text-slate-400 leading-relaxed" data-en="Expanding product pipeline from single DFU focus to a broader immunology portfolio, utilizing cross-border technology transfers."
                           data-zh="產品線從單一的 DFU 糖尿病足潰瘍擴展至更廣泛的免疫療法組合，並靈活運用跨國技術轉移。">
                            產品線從單一的 DFU 糖尿病足潰瘍擴展至更廣泛的免疫療法組合，並靈活運用跨國技術轉移。
                        </p>
                    </div>
                    <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
                        <h4 class="text-lg font-bold mb-4 text-teal-600" data-en="Operational Excellence" data-zh="營運卓越">營運卓越</h4>
                        <p class="text-slate-600 dark:text-slate-400 leading-relaxed" data-en="Optimized clinical trial pathways reducing time-to-market while maintaining stringent global regulatory standards."
                           data-zh="優化臨床試驗路徑，在維持嚴格全球法規標準的同時，有效縮短產品上市時間。">
                            優化臨床試驗路徑，在維持嚴格全球法規標準的同時，有效縮短產品上市時間。
                        </p>
                    </div>
                </div>
                <!-- 示意圖形 -->
                <div class="relative p-8 bg-blue-600/5 dark:bg-blue-400/5 rounded-[3rem] border border-blue-100 dark:border-blue-900/30 flex justify-center">
                    <div class="w-full max-w-sm aspect-square bg-white dark:bg-slate-800 rounded-full shadow-2xl flex flex-col items-center justify-center p-8 text-center">
                        <i class="fas fa-chart-pie text-5xl text-blue-600 mb-4"></i>
                        <span class="text-sm font-medium text-slate-500 dark:text-slate-400" data-en="Resource Evaluation" data-zh="資源評價">資源評價</span>
                        <span class="text-xl font-black mt-2 dark:text-white" data-en="VRIN Analysis" data-zh="VRIN 模型分析">VRIN 模型分析</span>
                        <div class="mt-6 flex flex-wrap justify-center gap-2">
                            <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-700 dark:text-blue-200 text-xs rounded-full">Valuable</span>
                            <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-700 dark:text-blue-200 text-xs rounded-full">Rare</span>
                            <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-700 dark:text-blue-200 text-xs rounded-full">Inimitable</span>
                            <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-700 dark:text-blue-200 text-xs rounded-full">Non-substitutable</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 104 職缺資料區 -->
    <section id="careers" class="py-24 bg-slate-50 dark:bg-slate-800/30">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-16 dark:text-white" data-en="Join Our Mission" data-zh="加入我們的行列 (104)">加入我們的行列 (104)</h2>
            <div class="bg-white dark:bg-slate-900 rounded-3xl overflow-hidden shadow-xl border border-slate-100 dark:border-slate-800">
                <table class="w-full">
                    <thead class="bg-slate-50 dark:bg-slate-800 text-slate-500 dark:text-slate-400 uppercase text-xs tracking-wider">
                        <tr>
                            <th class="px-8 py-6 text-left" data-en="Position" data-zh="職缺職位">職缺職位</th>
                            <th class="px-8 py-6 text-left" data-en="Requirements" data-zh="職務要求">職務要求</th>
                            <th class="px-8 py-6 text-right" data-en="Benefits" data-zh="薪資福利">薪資福利</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-100 dark:divide-slate-800">
                        <tr class="hover:bg-slate-50 dark:hover:bg-slate-800/50 transition-colors">
                            <td class="px-8 py-8">
                                <p class="font-bold text-lg dark:text-white" data-en="Senior Bio-Researcher" data-zh="高級生化研究員">高級生化研究員</p>
                                <span class="text-sm text-blue-600">R&D Department</span>
                            </td>
                            <td class="px-8 py-8 text-slate-600 dark:text-slate-400 text-sm leading-relaxed" data-en="PhD in Life Sciences, expertise in molecular immunology." data-zh="生命科學博士學位，具備分子免疫學專長。">生命科學博士學位，具備分子免疫學專長。</td>
                            <td class="px-8 py-8 text-right font-medium dark:text-white" data-en="Competitive / Negotiable" data-zh="待遇優渥 / 面議">待遇優渥 / 面議</td>
                        </tr>
                        <tr class="hover:bg-slate-50 dark:hover:bg-slate-800/50 transition-colors">
                            <td class="px-8 py-8">
                                <p class="font-bold text-lg dark:text-white" data-en="Clinical Trial Coordinator" data-zh="臨床試驗協調員">臨床試驗協調員</p>
                                <span class="text-sm text-blue-600">Clinical Operations</span>
                            </td>
                            <td class="px-8 py-8 text-slate-600 dark:text-slate-400 text-sm leading-relaxed" data-en="3+ years in multi-national clinical studies, fluent English." data-zh="3年以上跨國臨床研究經驗，英文流利。">3年以上跨國臨床研究經驗，英文流利。</td>
                            <td class="px-8 py-8 text-right font-medium dark:text-white" data-en="Full Benefits Packages" data-zh="完整福利體系">完整福利體系</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- 互動測驗 -->
    <section id="quiz" class="py-24">
        <div class="max-w-4xl mx-auto px-4">
            <div class="bg-gradient-to-br from-blue-600 to-indigo-700 rounded-[2.5rem] p-12 text-white shadow-2xl relative overflow-hidden">
                <i class="fas fa-brain absolute -bottom-10 -right-10 text-[12rem] opacity-10"></i>
                <div class="relative z-10 text-center">
                    <h2 class="text-3xl font-bold mb-8" data-en="Knowledge Challenge" data-zh="知識互動挑戰">知識互動挑戰</h2>
                    <p class="text-xl mb-10 text-blue-50" data-en="Which competitive advantage makes Oneness Biotech stand out?" data-zh="哪一項競爭優勢讓合一生技脫穎而出？">哪一項競爭優勢讓合一生技脫穎而出？</p>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <button onclick="checkAnswer(false)" class="p-5 bg-white/10 hover:bg-white/20 backdrop-blur-md rounded-2xl border border-white/20 transition-all text-left">
                            A) <span data-en="Lowest Production Cost" data-zh="最低的生產成本">最低的生產成本</span>
                        </button>
                        <button onclick="checkAnswer(true)" class="p-5 bg-white/10 hover:bg-white/20 backdrop-blur-md rounded-2xl border border-white/20 transition-all text-left">
                            B) <span data-en="Patented R&D for Unmet Needs" data-zh="解決未滿足需求的專利研發">解決未滿足需求的專利研發</span>
                        </button>
                    </div>
                    <div id="quizResult" class="mt-8 font-bold text-lg hidden animate-bounce"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- 團隊合作與 AI 運用 -->
    <section class="py-24 dark:bg-slate-900 border-t border-slate-100 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-16">
                <div>
                    <h3 class="text-2xl font-bold mb-6 flex items-center dark:text-white">
                        <i class="fas fa-users-cog text-blue-600 mr-4"></i>
                        <span data-en="Collaborative Reflection" data-zh="團隊合作與製作反思">團隊合作與製作反思</span>
                    </h3>
                    <p class="text-slate-600 dark:text-slate-400 leading-relaxed italic" data-en="Our team engaged in dynamic brainstorming sessions, ensuring every module reflects shared insights rather than isolated work."
                       data-zh="我們小組不僅是分工，更是融合。每週的動態腦力激盪確保了每個網頁模組都能反映出全體的集體智慧，而非孤立的工作片段。">
                        「我們小組不僅是分工，更是融合。每週的動態腦力激盪確保了每個網頁模組都能反映出全體的集體智慧，而非孤立的工作片段。」
                    </p>
                </div>
                <div>
                    <h3 class="text-2xl font-bold mb-6 flex items-center dark:text-white">
                        <i class="fas fa-robot text-teal-600 mr-4"></i>
                        <span data-en="AI Synergy" data-zh="AI 工具協作說明">AI 工具協作說明</span>
                    </h3>
                    <p class="text-slate-600 dark:text-slate-400 leading-relaxed" data-en="Leveraged LLMs for structured coding, bilingual translation polish, and UI layout optimization to meet competition standards."
                       data-zh="運用大型語言模型進行結構化編碼、中英翻譯潤飾以及 UI 版面優化，確保網頁各項技術指標符合競賽的高標準要求。">
                        本專案深度運用大型語言模型進行結構化編碼、中英翻譯潤飾以及 UI 版面優化，確保網頁在視覺與功能技術指標上均能符合競賽的高標準要求。
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- 頁尾 (強化課程與教師資訊) -->
    <footer class="py-16 bg-slate-900 text-slate-400">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <div class="mb-10 inline-flex items-center space-x-4 px-6 py-2 bg-slate-800 rounded-full text-slate-300">
                <span class="font-bold border-r border-slate-700 pr-4">1142 國際策略管理</span>
                <span class="font-medium">授課教師：<span class="text-white">梅筱珍 教授</span></span>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-center pt-8 border-t border-slate-800 text-sm">
                <div class="md:text-left">
                    <p>© 2026 國立暨南國際大學</p>
                </div>
                <div class="flex justify-center space-x-6">
                    <a href="#" class="hover:text-white transition-colors">期末網頁競賽</a>
                    <a href="#" class="hover:text-white transition-colors">小組專案報告</a>
                </div>
                <div class="md:text-right">
                    <p>© 2026 國際策略管理 G8 Merida. All rights reserved.</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // 狀態變數
        let currentLang = 'zh';
        let isDarkMode = false;

        // 語音導覽設定
        const voices = {
            zh: { text: "您好，歡迎瀏覽合一生技的學習網頁。本專案由第G8 Merida小組製作，為您深度解析合一的國際策略。", lang: "zh-TW" },
            en: { text: "Hello, welcome to Oneness Biotech learning portal. This project is created by Group G8 Merida, analyzing international strategies.", lang: "en-GB" }
        };

        function speakText() {
            window.speechSynthesis.cancel(); // 先停止當前語音
            const msg = new SpeechSynthesisUtterance();
            const config = voices[currentLang];
            msg.text = config.text;
            msg.lang = config.lang;
            msg.rate = 1.0;
            window.speechSynthesis.speak(msg);
        }

        // 語言切換邏輯
        const langToggle = document.getElementById('langToggle');
        const langText = document.getElementById('langText');
        langToggle.addEventListener('click', () => {
            currentLang = currentLang === 'zh' ? 'en' : 'zh';
            langText.innerText = currentLang === 'zh' ? 'EN' : 'ZH';
            
            document.querySelectorAll('[data-en]').forEach(el => {
                el.innerText = el.getAttribute(`data-${currentLang}`);
            });
        });

        // 主題切換邏輯
        const themeToggle = document.getElementById('themeToggle');
        themeToggle.addEventListener('click', () => {
            document.documentElement.classList.toggle('dark');
        });

        // 測驗邏輯
        function checkAnswer(isCorrect) {
            const result = document.getElementById('quizResult');
            result.classList.remove('hidden', 'text-green-400', 'text-yellow-400');
            
            if (isCorrect) {
                result.innerText = currentLang === 'zh' ? "🎉 太棒了！答對了！" : "🎉 Excellent! That's correct!";
                result.classList.add('text-green-400');
            } else {
                result.innerText = currentLang === 'zh' ? "❌ 差一點點，再想一下！" : "❌ Almost there, try again!";
                result.classList.add('text-yellow-400');
            }
        }
    </script>
</body>
</html>
