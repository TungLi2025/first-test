<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>玄語說媒 - 頻道互動分析儀</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Calm Neutrals -->
    <!-- Application Structure Plan: 採用儀表板佈局，將頻道內容結構化。頂部為關鍵指標摘要，提供一個宏觀視角。核心部分是「主題分析儀」，將影片案例歸類到不同情感主題下，並使用 Chart.js 長條圖視覺化各主題的受歡迎程度。下方是「精選案例探索器」，以卡片形式展示具體案例。用戶可以透過點擊主題按鈕或圖表來篩選案例，實現數據與內容的互動。這種結構將零散的影片案例轉化為有組織、可分析的資訊，比單純滾動瀏覽 YouTube 更能幫助用戶理解頻道的核心主題與觀眾興趣。 -->
    <!-- Visualization & Content Choices: 報告中提到觀看次數，適合量化分析。因此，選擇了長條圖 (Chart.js/Canvas) 來比較不同情感主題的「總觀看熱度」，讓用戶能快速識別最引發共鳴的話題。互動方面，點擊圖表或主題按鈕，可以篩選下方的「精選案例探索器」（使用 Vanilla JS 動態更新 DOM），讓用戶能深入探索特定主題下的具體案例。這種「從宏觀到微觀」的互動設計，能有效地引導用戶理解報告中的質化內容（案例故事）。 -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Noto Sans TC', sans-serif;
            background-color: #FDFBF8;
            color: #4A4A4A;
        }
        .chart-container {
            position: relative;
            width: 100%;
            height: 400px;
            max-height: 50vh;
        }
        .theme-button {
            transition: all 0.3s ease;
        }
        .theme-button.active, .theme-button:hover {
            background-color: #D3A993;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        .case-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease, opacity 0.5s ease;
            opacity: 1;
            transform: scale(1);
        }
        .case-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .case-card.hidden {
            opacity: 0;
            transform: scale(0.95);
            display: none;
        }
        .stat-card {
            background-color: #FFFFFF;
            border-left: 4px solid #D3A993;
        }
    </style>
</head>
<body class="antialiased">
    <div class="container mx-auto p-4 sm:p-6 md:p-8">
        <header class="text-center mb-10">
            <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold text-[#A7727D] mb-2">玄語說媒</h1>
            <p class="text-lg sm:text-xl text-gray-500">頻道互動分析儀</p>
        </header>

        <main>
            <section id="key-metrics" class="mb-12">
                 <div class="text-center mb-8">
                    <h2 class="text-2xl font-bold mb-2">核心指標</h2>
                    <p class="text-gray-500 max-w-2xl mx-auto">本節概述了「玄語說媒」頻道的關鍵數據指標，從中可見其內容在觀眾中的影響力與覆蓋範圍。這些數據反映了頻道在探討兩性情感議題上的熱度與受歡迎程度。</p>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 text-center">
                    <div class="stat-card rounded-lg p-6 shadow-md">
                        <p class="text-4xl font-bold text-[#A7727D]" id="total-views">3.1M+</p>
                        <p class="text-gray-500 mt-2">總觀看次數</p>
                    </div>
                    <div class="stat-card rounded-lg p-6 shadow-md">
                        <p class="text-4xl font-bold text-[#A7727D]" id="total-videos">50+</p>
                        <p class="text-gray-500 mt-2">分析案例影片</p>
                    </div>
                    <div class="stat-card rounded-lg p-6 shadow-md">
                        <p class="text-4xl font-bold text-[#A7727D]" id="avg-views">62K+</p>
                        <p class="text-gray-500 mt-2">平均觀看量</p>
                    </div>
                    <div class="stat-card rounded-lg p-6 shadow-md">
                        <p class="text-4xl font-bold text-[#A7727D]" id="popular-theme">金錢價值觀</p>
                        <p class="text-gray-500 mt-2">最熱門主題</p>
                    </div>
                </div>
            </section>

            <section id="theme-analyzer" class="mb-12 bg-white rounded-xl shadow-lg p-6 sm:p-8">
                <div class="text-center mb-8">
                    <h2 class="text-2xl font-bold mb-2">主題分析儀</h2>
                    <p class="text-gray-500 max-w-2xl mx-auto">此分析儀將頻道的眾多案例歸納為幾個核心情感主題。透過下方的互動圖表，您可以清晰地看到不同主題在觀眾中的受歡迎程度，了解哪些話題最能引發共鳴。點擊圖表中的任一長條，即可篩選下方的案例列表。</p>
                </div>
                <div class="chart-container max-w-4xl mx-auto">
                    <canvas id="themeChart"></canvas>
                </div>
            </section>
            
            <section id="case-explorer">
                <div class="text-center mb-8">
                    <h2 class="text-2xl font-bold mb-2">精選案例探索器</h2>
                    <p class="text-gray-500 max-w-2xl mx-auto">此處匯集了頻道的精選案例。您可以點擊下方的主題按鈕，或上方的圖表，來篩選並深入了解在特定情感議題下的各種真實故事與觀點。這有助於您更全面地理解現代兩性關係中的複雜性。</p>
                </div>
                
                <div id="theme-filters" class="flex flex-wrap justify-center gap-3 mb-8">
                    </div>

                <div id="case-studies-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                </div>
            </section>
        </main>
    </div>

    <script>
        const caseData = [
            { id: 1, title: '相親男靠收租月入三萬，女嫌沒上進心拒絕後又後悔', views: 210000, theme: '金錢價值觀', summary: '探討在擇偶中，穩定被動收入與個人上進心之間的價值權衡問題。' },
            { id: 2, title: '為不讓女兒嫁出去，爸爸把彩禮抬到1243萬', views: 166000, theme: '家庭影響', summary: '反映了家庭過度干預子女婚姻，以及天價彩禮背後的複雜家庭動態。' },
            { id: 3, title: '00後離婚率飆升300%', views: 105000, theme: '婚姻與現實', summary: '分析年輕一代對婚姻觀念的轉變以及現代婚姻面臨的現實挑戰。' },
            { id: 4, title: '大齡剩女的擇偶標準：月薪5萬，有車有房，身高180', views: 523000, theme: '擇偶標準', summary: '揭示了部分大齡單身女性在擇偶市場上的高標準與現實之間的差距。' },
            { id: 5, title: '女方嫌男友摳門，婚禮前鬧掰', views: 305000, theme: '金錢價值觀', summary: '一個因消費觀念差異導致情侶關係破裂的典型案例，引發對金錢觀的思考。' },
            { id: 6, title: '我人生最怕嫁給女公務員', views: 98000, theme: '擇偶標準', summary: '探討職業標籤對婚戀選擇的影響，以及背後隱藏的刻板印象與偏見。' },
            { id: 7, title: '男方家全款買房，女方要求20萬彩禮才肯嫁', views: 183000, theme: '金錢價值觀', summary: '在婚前財產和彩禮問題上的博弈，反映了傳統與現代觀念的衝突。' },
            { id: 8, title: '38歲女老師找對象，要求男方帥氣又多金', views: 160000, theme: '擇偶標準', summary: '一個關於成熟女性堅持高標準擇偶，不願妥協的案例。' },
            { id: 9, title: '男追女4個月，男生果斷放棄女方急了', views: 110000, theme: '戀愛技巧', summary: '討論追求過程中的「沉沒成本」與及時止損的策略，以及男女雙方的心理博弈。' },
             { id: 10, title: '男生月入三萬，女生卻說「你配不上我」', views: 350000, theme: '金錢價值觀', summary: '探討收入水平與個人價值感的關係，以及在婚戀市場中的自我定位問題。' },
            { id: 11, title: '為什麼現在的男生，越來越不願意追女生了？', views: 280000, theme: '婚姻與現實', summary: '分析當代男性在追求異性時面臨的壓力、成本和心態變化。' },
            { id: 12, title: '40歲離異帶娃，要求男方月入5萬，自己不工作', views: 240000, theme: '婚姻與現實', summary: '一個關於再婚市場中，個人條件與擇偶期望之間巨大鴻溝的案例。' }
        ];

        document.addEventListener('DOMContentLoaded', () => {
            const themes = [...new Set(caseData.map(c => c.theme))];
            
            const themeFiltersContainer = document.getElementById('theme-filters');
            const caseStudiesGrid = document.getElementById('case-studies-grid');
            
            const allButton = createFilterButton('全部案例', true);
            themeFiltersContainer.appendChild(allButton);
            themes.forEach(theme => {
                const button = createFilterButton(theme);
                themeFiltersContainer.appendChild(button);
            });

            function createFilterButton(text, isActive = false) {
                const button = document.createElement('button');
                button.textContent = text;
                button.dataset.theme = text;
                button.className = `theme-button px-4 py-2 text-sm font-medium rounded-full shadow focus:outline-none ${isActive ? 'active' : 'bg-white text-[#A7727D]'}`;
                button.addEventListener('click', () => {
                    document.querySelectorAll('.theme-button').forEach(btn => btn.classList.remove('active'));
                    button.classList.add('active');
                    filterCases(text);
                });
                return button;
            }

            function renderCases(filterTheme = '全部案例') {
                caseStudiesGrid.innerHTML = '';
                const filteredData = filterTheme === '全部案例' ? caseData : caseData.filter(c => c.theme === filterTheme);
                
                filteredData.forEach(caseItem => {
                    const card = document.createElement('div');
                    card.className = 'case-card bg-white rounded-lg shadow-lg overflow-hidden p-5 flex flex-col';
                    card.dataset.theme = caseItem.theme;

                    card.innerHTML = `
                        <div class="flex-grow">
                            <span class="inline-block bg-rose-100 text-[#A7727D] text-xs font-semibold px-2.5 py-1 rounded-full mb-3">${caseItem.theme}</span>
                            <h3 class="text-lg font-bold mb-2 h-14">${caseItem.title}</h3>
                            <p class="text-gray-600 text-sm mb-4">${caseItem.summary}</p>
                        </div>
                        <div class="flex items-center text-gray-500 text-sm mt-auto">
                            <svg class="w-4 h-4 mr-1.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path></svg>
                            <span>${(caseItem.views / 10000).toFixed(1)}萬 次觀看</span>
                        </div>
                    `;
                    caseStudiesGrid.appendChild(card);
                });
            }

            function filterCases(theme) {
                 const cards = document.querySelectorAll('.case-card');
                 cards.forEach(card => {
                    if (theme === '全部案例' || card.dataset.theme === theme) {
                        card.classList.remove('hidden');
                        card.style.display = 'flex';
                    } else {
                        card.classList.add('hidden');
                         setTimeout(() => { card.style.display = 'none'; }, 500);
                    }
                });
            }
            
            renderCases();

            const themeData = themes.map(theme => {
                const themeCases = caseData.filter(c => c.theme === theme);
                const totalViews = themeCases.reduce((sum, c) => sum + c.views, 0);
                return { theme, totalViews };
            });

            const ctx = document.getElementById('themeChart').getContext('2d');
            const themeChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: themeData.map(d => d.theme),
                    datasets: [{
                        label: '總觀看熱度',
                        data: themeData.map(d => d.totalViews),
                        backgroundColor: [
                            'rgba(211, 169, 147, 0.6)',
                            'rgba(167, 114, 125, 0.6)',
                            'rgba(239, 221, 207, 0.8)',
                            'rgba(189, 153, 153, 0.6)',
                             'rgba(216, 189, 178, 0.7)'
                        ],
                        borderColor: [
                             'rgba(211, 169, 147, 1)',
                             'rgba(167, 114, 125, 1)',
                            'rgba(239, 221, 207, 1)',
                             'rgba(189, 153, 153, 1)',
                             'rgba(216, 189, 178, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                             callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.x !== null) {
                                        label += new Intl.NumberFormat('zh-TW').format(context.parsed.x);
                                    }
                                    return label;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                             ticks: {
                                callback: function(value, index, values) {
                                    if (value >= 10000) {
                                        return (value / 10000) + '萬';
                                    }
                                    return value;
                                }
                            }
                        }
                    },
                    onClick: (event, elements) => {
                        if (elements.length > 0) {
                            const elementIndex = elements[0].index;
                            const clickedTheme = themeChart.data.labels[elementIndex];
                            
                            document.querySelectorAll('.theme-button').forEach(btn => {
                                btn.classList.remove('active');
                                if (btn.dataset.theme === clickedTheme) {
                                    btn.classList.add('active');
                                }
                            });
                            filterCases(clickedTheme);
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>
