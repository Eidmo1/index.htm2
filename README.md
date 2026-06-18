# index.htm2
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Helix Verse Clone</title>
    <!-- تضمين مكتبة Tailwind CSS للتصميم الاحترافي والسريع -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <!-- أيقونات FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body { font-family: sans-serif; background-color: #0b0f12; color: #ffffff; }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
    </style>
</head>
<body class="select-none pb-24">

    <!-- شريط علوي يحاكي التطبيق -->
    <div class="p-4 flex justify-between items-center border-b border-gray-800 bg-[#0f141c]">
        <div class="flex items-center gap-2">
            <span class="text-amber-500 font-bold text-lg">★</span>
            <span class="font-bold text-amber-500">Waddafah Bot</span>
        </div>
        <button class="text-xs bg-gray-800 px-3 py-1 rounded-full text-gray-400">BÁSICO</button>
    </div>

    <!-- ================= صبحة الرئيسية (Home) ================= -->
    <div id="home" class="tab-content active p-4">
        <!-- الخزنة والرصيد -->
        <div class="bg-[#141a23] p-4 rounded-2xl border border-gray-800 shadow-xl mb-4">
            <p class="text-xs text-amber-400 font-semibold mb-1">VAULT BALANCE</p>
            <div class="flex items-center gap-2 mb-2">
                <span class="text-2xl">⚡</span>
                <h1 class="text-3xl font-black text-amber-400" id="balance-display">35.00 <span class="text-sm text-gray-400">HLX</span></h1>
            </div>
            <p class="text-xs text-emerald-400">+0.0244 HLX ready to claim</p>
        </div>

        <!-- حالة الحفار -->
        <div class="bg-[#141a23] p-4 rounded-2xl border border-emerald-900/30 flex justify-between items-center mb-4">
            <div class="flex items-center gap-3">
                <div class="bg-emerald-500/10 p-3 rounded-xl text-emerald-400">⚡</div>
                <div>
                    <h3 class="font-bold text-sm">Rig Active</h3>
                    <p class="text-xs text-gray-400">Next cycle • 23h 56m</p>
                </div>
            </div>
            <span class="text-xs font-bold text-emerald-400 bg-emerald-500/10 px-2 py-1 rounded">0%</span>
        </div>

        <!-- زر المطالبة (Claim) الشهير باللون الذهبي -->
        <button onclick="claimMining()" class="w-full bg-gradient-to-r from-amber-500 to-yellow-400 text-gray-900 font-black py-4 rounded-2xl shadow-lg shadow-amber-500/20 active:scale-95 transition-transform text-center mb-6">
            ⚡ Claim 0.0244 HLX
        </button>

        <!-- بيانات التعدين الـ Telemetry -->
        <h2 class="font-bold text-sm text-gray-400 mb-3">Telemetry <span class="float-left text-xs text-emerald-500">● Live</span></h2>
        <div class="bg-[#141a23] p-4 rounded-2xl border border-gray-800 grid grid-cols-2 gap-4">
            <div class="col-span-2 bg-[#0f141c] p-3 rounded-xl">
                <p class="text-xs text-gray-400">Hash Rate</p>
                <p class="text-xl font-bold text-cyan-400">0.1 GH/s</p>
                <!-- محاكاة الرسم البياني -->
                <div class="flex items-end gap-1 h-8 mt-2">
                    <div class="bg-cyan-500/40 w-full h-4 rounded-sm"></div>
                    <div class="bg-cyan-500/60 w-full h-6 rounded-sm"></div>
                    <div class="bg-cyan-500/80 w-full h-5 rounded-sm"></div>
                    <div class="bg-cyan-500 w-full h-8 rounded-sm"></div>
                </div>
            </div>
            <div class="bg-[#0f141c] p-3 rounded-xl">
                <p class="text-xs text-gray-400">Efficiency</p>
                <p class="text-lg font-bold text-emerald-400">72%</p>
            </div>
            <div class="bg-[#0f141c] p-3 rounded-xl">
                <p class="text-xs text-gray-400">Core Temp</p>
                <p class="text-lg font-bold text-amber-500">48 °C</p>
            </div>
        </div>
    </div>

    <!-- ================= صفحة المهام (Tasks) ================= -->
    <div id="tasks" class="tab-content p-4">
        <h2 class="text-2xl font-black text-amber-400 mb-1">Tasks & Earn</h2>
        <p class="text-xs text-gray-400 mb-6">Complete quests to earn rewards</p>

        <div class="space-y-3">
            <div class="bg-[#141a23] p-4 rounded-xl flex justify-between items-center border border-gray-800">
                <div class="flex items-center gap-3">
                    <div class="text-cyan-400 text-xl"><i class="fa-solid fa-play-circle"></i></div>
                    <div>
                        <h4 class="font-bold text-sm">Adsgram <span class="text-xs text-cyan-400">0/5</span></h4>
                        <p class="text-xs text-gray-400">+15 HLX  •  +20 ⚡</p>
                    </div>
                </div>
                <button class="bg-blue-600 px-4 py-1.5 rounded-lg text-xs font-bold">Watch</button>
            </div>
        </div>
    </div>

    <!-- ================= صفحة الألعاب (Games) ================= -->
    <div id="games" class="tab-content p-4">
        <h2 class="text-2xl font-black text-amber-400 mb-1">Games</h2>
        <p class="text-xs text-gray-400 mb-6">Have fun and earn while you play</p>
        <div class="grid grid-cols-2 gap-4">
            <div class="bg-[#141a23] p-3 rounded-2xl border border-gray-800 text-center">
                <div class="bg-red-500/20 h-24 rounded-xl mb-2 flex items-center justify-center text-3xl">🍉</div>
                <h4 class="font-bold text-sm">Fruit Slice</h4>
                <p class="text-xs text-gray-500 mb-3">Arcade</p>
                <button class="w-full bg-amber-500 text-gray-900 text-xs font-bold py-2 rounded-xl">Play</button>
            </div>
            <div class="bg-[#141a23] p-3 rounded-2xl border border-gray-800 text-center">
                <div class="bg-blue-500/20 h-24 rounded-xl mb-2 flex items-center justify-center text-3xl">🐧</div>
                <h4 class="font-bold text-sm">Pengu Pengu</h4>
                <p class="text-xs text-gray-500 mb-3">Arcade</p>
                <button class="w-full bg-amber-500 text-gray-900 text-xs font-bold py-2 rounded-xl">Play</button>
            </div>
        </div>
    </div>

    <!-- ================= صفحة المحفظة (Wallet) ================= -->
    <div id="wallet" class="tab-content p-4">
        <h2 class="text-2xl font-black text-amber-400 mb-6">My Wallet</h2>
        <div class="bg-[#141a23] p-6 rounded-2xl border border-gray-800 mb-6">
            <p class="text-xs text-gray-400 mb-2">Total Balance</p>
            <h1 class="text-3xl font-black text-amber-400 mb-4">35.00 <span class="text-sm text-gray-500">HLX</span></h1>
            <div class="flex justify-between border-t border-gray-800 pt-4 text-sm">
                <span class="text-gray-400">💵 USDT</span>
                <span class="font-bold text-emerald-400">0.00</span>
            </div>
        </div>
        <div class="grid grid-cols-3 gap-3">
            <button class="bg-cyan-400 text-gray-900 font-bold py-3 rounded-xl text-xs"><i class="fa-solid fa-arrow-down mr-1"></i> Deposit</button>
            <button class="bg-amber-400 text-gray-900 font-bold py-3 rounded-xl text-xs"><i class="fa-solid fa-arrow-up mr-1"></i> Withdraw</button>
            <button class="bg-cyan-400 text-gray-900 font-bold py-3 rounded-xl text-xs"><i class="fa-solid fa-rotate mr-1"></i> Convert</button>
        </div>
    </div>

    <!-- ================= صفحة الحساب الشخصي (You) ================= -->
    <div id="you" class="tab-content p-4">
        <div class="text-center my-6">
            <div class="w-20 h-20 bg-gradient-to-tr from-cyan-400 to-amber-400 rounded-full mx-auto flex items-center justify-center text-2xl font-black text-gray-900 mb-3">EI</div>
            <h2 class="text-xl font-bold" id="username-display">Eid</h2>
            <p class="text-xs text-gray-500">@Eidmo11</p>
        </div>
        <div class="bg-[#141a23] p-4 rounded-xl space-y-4 border border-gray-800 text-sm">
            <div class="flex justify-between"><span class="text-gray-400">Language</span><span class="text-xs">English 🇺🇸</span></div>
            <div class="flex justify-between"><span class="text-gray-400">Promo Code</span><span class="text-xs text-amber-400">Redeem ></span></div>
        </div>
    </div>

    <!-- ================= شريط التنقل السفلي المتطابق (Navigation Bar) ================= -->
    <div class="fixed bottom-0 left-0 right-0 bg-[#0f141c]/95 backdrop-blur-md border-t border-gray-800 flex justify-around py-3 text-center text-[10px] text-gray-500 z-50">
        <button onclick="switchTab('home')" class="nav-btn text-amber-400"><i class="fa-solid fa-house text-lg block mb-1"></i>Home</button>
        <button onclick="switchTab('tasks')" class="nav-btn"><i class="fa-solid fa-list-check text-lg block mb-1"></i>Tasks</button>
        <button onclick="switchTab('games')" class="nav-btn"><i class="fa-solid fa-gamepad text-lg block mb-1"></i>Games</button>
        <button onclick="switchTab('wallet')" class="nav-btn"><i class="fa-solid fa-wallet text-lg block mb-1"></i>Wallet</button>
        <button onclick="switchTab('you')" class="nav-btn"><i class="fa-solid fa-user text-lg block mb-1"></i>You</button>
    </div>

    <!-- السكريبت الخاص بالتحكم في الواجهة والربط بالسيرفر -->
    <script>
        let currentBalance = 35.00;

        function switchTab(tabId) {
            // إخفاء كل الصفحات
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            // إظهار الصفحة المحددة
            document.getElementById(tabId).classList.add('active');
            
            // تغيير تلوين الأزرار النشطة
            document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('text-amber-400'));
            event.currentTarget.classList.add('text-amber-400');
        }

        function claimMining() {
            currentBalance += 0.0244;
            document.getElementById('balance-display').innerHTML = currentBalance.toFixed(4) + ' <span class="text-sm text-gray-400">HLX</span>';
            alert('تمت المطالبة بنجاح والتعدين مستمر!');
        }
    </script>
</body>
</html>
