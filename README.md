<!DOCTYPE html>
<html lang="mr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DC ThumbCraft Pro - मोफत YouTube थंबनेल मेकर</title>
  
  <meta name="description" content="DC ThumbCraft Pro - मोबाईलवरून मोफत YouTube आणि Shorts थंबनेल बनवा. 100% Free Marathi & English Thumbnail Maker.">
  <meta name="keywords" content="DC ThumbCraft, YouTube Thumbnail Maker Marathi, Free Thumbnail Generator, Shorts Thumbnail">
  <meta name="author" content="Dnyaneshwar Deokar">
  <meta name="robots" content="index, follow">

  <!-- Open Graph / Meta -->
  <meta property="og:title" content="DC ThumbCraft Pro - मोफत थंबनेल मेकर">
  <meta property="og:description" content="फक्त २ मिनिटांत व्हायरल YouTube & Shorts थंबनेल बनवा. 100% मोफत!">
  <meta property="og:type" content="website">

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
  <!-- Google Fonts: Hind, Poppins, Teko -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Hind:wght@400;600;700&family=Poppins:wght@600;800;900&family=Teko:wght@700&display=swap" rel="stylesheet">
  
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: { 500: '#6366f1', 600: '#4f46e5', 700: '#4338ca' },
            gold: { 400: '#fbbf24', 500: '#f59e0b', 600: '#d97706' },
            darkbg: '#0f172a',
            darkcard: '#1e293b',
            darkborder: '#334155'
          },
          fontFamily: {
            marathi: ['Hind', 'sans-serif'],
            display: ['Poppins', 'sans-serif'],
            impact: ['Teko', 'sans-serif']
          }
        }
      }
    }
  </script>

  <style>
    body {
      font-family: 'Poppins', 'Hind', sans-serif;
      background-color: #0b0f19;
      color: #f1f5f9;
      user-select: none;
    }
    canvas {
      image-rendering: auto;
      touch-action: none;
    }
    .custom-scroll::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    .custom-scroll::-webkit-scrollbar-track {
      background: #111827;
    }
    .custom-scroll::-webkit-scrollbar-thumb {
      background: #374151;
      border-radius: 4px;
    }
    .gold-gradient {
      background: linear-gradient(135deg, #fcd34d 0%, #f59e0b 50%, #d97706 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col justify-between custom-scroll">

  <!-- Header -->
  <header class="bg-[#111827]/90 backdrop-blur-md border-b border-darkborder sticky top-0 z-40 px-4 py-3">
    <div class="max-w-7xl mx-auto flex items-center justify-between flex-wrap gap-2">
      <div class="flex items-center gap-3">
        <!-- SECRET OWNER TRIGGER: 4 fast taps/clicks on DC logo unlocks your drawer with PIN 261126 -->
        <div id="secretOwnerLogo" onclick="handleSecretAdminClick()" title="DC ThumbCraft" class="w-10 h-10 rounded-xl bg-gradient-to-tr from-indigo-600 via-purple-600 to-amber-500 flex items-center justify-center shadow-lg shadow-indigo-500/20 text-white font-black text-xl tracking-tighter cursor-pointer active:scale-95 select-none transition-transform">
          DC
        </div>
        <div>
          <div class="flex items-center gap-1.5">
            <h1 class="text-lg font-black tracking-tight text-white flex items-center gap-1">
              <span class="gold-gradient">DC</span> ThumbCraft <span class="text-xs px-2 py-0.5 rounded bg-indigo-500/20 text-indigo-400 border border-indigo-500/30 uppercase tracking-widest font-semibold">Pro</span>
            </h1>
          </div>
          <p class="text-[11px] text-gray-400">व्हायरल YouTube & Shorts थंबनेल क्रिएटर</p>
        </div>
      </div>

      <!-- Public View: Direct Download Button -->
      <div class="flex items-center gap-2">
        <button onclick="downloadThumbnail()" class="px-3.5 py-1.5 rounded-lg bg-emerald-600 hover:bg-emerald-500 text-white font-semibold text-xs flex items-center gap-1.5 shadow-md shadow-emerald-600/30 transition-all active:scale-95">
          <i class="fa-solid fa-download"></i>
          <span>थंबनेल डाऊनलोड करा</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Secret Admin Panel Drawer (Only unlocks with 4 clicks on DC logo + PIN 261126) -->
  <div id="adminPanelDrawer" class="hidden bg-[#131b2e] border-b border-amber-500/40 px-4 py-4 shadow-2xl transition-all">
    <div class="max-w-7xl mx-auto">
      <div class="flex items-center justify-between mb-3">
        <div class="flex items-center gap-2">
          <span class="text-sm font-bold text-amber-400 flex items-center gap-1.5">
            <i class="fa-solid fa-user-shield"></i> अधिकृत मालक ॲडमिन (Dnyaneshwar Deokar)
          </span>
        </div>
        <button onclick="lockAdminPanel()" class="text-xs text-rose-300 hover:text-white px-3 py-1 rounded bg-rose-950/60 border border-rose-500/40 flex items-center gap-1">
          <i class="fa-solid fa-lock text-[10px]"></i> पॅनेल बंद करा
        </button>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-3 text-xs">
        <div>
          <label class="font-semibold text-gray-300 block mb-1">तुमचा खरा UPI ID:</label>
          <input type="text" id="ownerUpiInput" value="dnyaneshwardeokar@ybl" class="w-full bg-darkbg border border-darkborder px-3 py-2 rounded-lg text-emerald-400 font-mono focus:outline-none focus:border-emerald-500">
        </div>
        <div>
          <label class="font-semibold text-gray-300 block mb-1">तुमचा WhatsApp नंबर:</label>
          <input type="text" id="ownerWhatsappInput" value="919405478111" class="w-full bg-darkbg border border-darkborder px-3 py-2 rounded-lg text-emerald-400 font-mono focus:outline-none focus:border-emerald-500">
        </div>
      </div>

      <div class="mt-3 flex items-center justify-between flex-wrap gap-2">
        <p class="text-[11px] text-gray-400">माहिती कायमस्वरूपी सेव्ह आहे. गरज असल्यास बदलून सेव्ह करा.</p>
        <button onclick="saveOwnerPaymentDetails()" class="px-4 py-2 bg-emerald-500 hover:bg-emerald-400 text-black font-extrabold rounded-lg text-xs shadow-lg transition-all active:scale-95 flex items-center gap-1.5">
          <i class="fa-solid fa-floppy-disk"></i> माहिती सेव्ह करा
        </button>
      </div>
    </div>
  </div>

  <main class="max-w-7xl mx-auto w-full p-3 sm:p-4 grid grid-cols-1 lg:grid-cols-12 gap-4 flex-1">
    
    <!-- LEFT SIDEBAR: Tools & Design Controls (5 Cols) -->
    <div class="lg:col-span-5 flex flex-col gap-4">
      
      <!-- Preset Themes Section -->
      <div class="bg-darkcard border border-darkborder rounded-2xl p-3.5 shadow-lg">
        <h2 class="text-xs font-bold text-gray-300 uppercase tracking-wider mb-2.5 flex items-center gap-1.5">
          <i class="fa-solid fa-wand-magic-sparkles text-amber-400"></i> 1-क्लिक व्हायरल टेम्पलेट्स
        </h2>
        <div class="grid grid-cols-2 sm:grid-cols-4 gap-2">
          <button onclick="applyPreset('earning')" class="p-2 rounded-xl bg-gradient-to-br from-emerald-950 to-slate-900 border border-emerald-500/30 text-left hover:border-emerald-400 transition-all">
            <span class="text-lg">💰</span>
            <p class="text-xs font-bold text-white mt-1">पैसे कमवा</p>
            <p class="text-[10px] text-emerald-400">Earning Pro</p>
          </button>
          <button onclick="applyPreset('tech')" class="p-2 rounded-xl bg-gradient-to-br from-indigo-950 to-slate-900 border border-indigo-500/30 text-left hover:border-indigo-400 transition-all">
            <span class="text-lg">🤖</span>
            <p class="text-xs font-bold text-white mt-1">AI / Tech</p>
            <p class="text-[10px] text-indigo-400">Sci-Fi Viral</p>
          </button>
          <button onclick="applyPreset('breaking')" class="p-2 rounded-xl bg-gradient-to-br from-rose-950 to-slate-900 border border-rose-500/30 text-left hover:border-rose-400 transition-all">
            <span class="text-lg">🚨</span>
            <p class="text-xs font-bold text-white mt-1">मोठी बातमी</p>
            <p class="text-[10px] text-rose-400">Breaking</p>
          </button>
          <button onclick="applyPreset('gaming')" class="p-2 rounded-xl bg-gradient-to-br from-purple-950 to-slate-900 border border-purple-500/30 text-left hover:border-purple-400 transition-all">
            <span class="text-lg">🎮</span>
            <p class="text-xs font-bold text-white mt-1">गेमिंग</p>
            <p class="text-[10px] text-purple-400">Gaming HD</p>
          </button>
        </div>
      </div>

      <!-- Text Inputs Section -->
      <div class="bg-darkcard border border-darkborder rounded-2xl p-3.5 shadow-lg flex flex-col gap-3">
        <h2 class="text-xs font-bold text-gray-300 uppercase tracking-wider flex items-center justify-between">
          <span class="flex items-center gap-1.5"><i class="fa-solid fa-heading text-indigo-400"></i> थंबनेल मजकूर</span>
          <span class="text-[10px] text-gray-400 font-normal">कॅनव्हासवर ड्रॅग करा</span>
        </h2>

        <div>
          <label class="text-[11px] text-gray-300 font-medium block mb-1">मुख्य ठळक शीर्षक:</label>
          <input type="text" id="primaryTextInput" value="मोबाईलवरून दररोज ₹२,००० कमवा!" placeholder="उदा. मोबाईलवरून पैसे कमवा..." class="w-full bg-darkbg border border-darkborder rounded-lg px-3 py-2 text-sm text-white focus:outline-none focus:border-indigo-500">
        </div>

        <div>
          <label class="text-[11px] text-gray-300 font-medium block mb-1">उपशीर्षक / बॅज मजकूर:</label>
          <input type="text" id="secondaryTextInput" value="100% मोफत ट्रिक | आजच सुरू करा 🔥" placeholder="उदा. 100% मोफत पद्धत..." class="w-full bg-darkbg border border-darkborder rounded-lg px-3 py-2 text-sm text-amber-300 focus:outline-none focus:border-indigo-500">
        </div>

        <!-- Marathi Quick Phrases -->
        <div>
          <span class="text-[10px] text-gray-400 block mb-1">रेडीमेड मराठी वाक्ये (टॅप करा):</span>
          <div class="flex flex-wrap gap-1.5">
            <button onclick="addMarathiText('मोफत शिका')" class="text-[10px] px-2 py-0.5 rounded bg-darkbg border border-darkborder text-gray-300 hover:border-indigo-400">मोफत शिका</button>
            <button onclick="addMarathiText('दरमहा ₹५०,००० कमाई')" class="text-[10px] px-2 py-0.5 rounded bg-darkbg border border-darkborder text-gray-300 hover:border-indigo-400">दरमहा ₹५०,००० कमाई</button>
            <button onclick="addMarathiText('नवीन भन्नाट अपडेट!')" class="text-[10px] px-2 py-0.5 rounded bg-darkbg border border-darkborder text-gray-300 hover:border-indigo-400">नवीन भन्नाट अपडेट!</button>
            <button onclick="addMarathiText('फक्त ५ मिनिटांत')" class="text-[10px] px-2 py-0.5 rounded bg-darkbg border border-darkborder text-gray-300 hover:border-indigo-400">फक्त ५ मिनिटांत</button>
          </div>
        </div>

        <!-- Font, Size & Styling Grid -->
        <div class="grid grid-cols-2 gap-2 text-xs pt-1">
          <div>
            <label class="text-[11px] text-gray-300 block mb-1">फॉन्ट स्टाईल:</label>
            <select id="fontFamilySelect" class="w-full bg-darkbg border border-darkborder rounded-lg px-2.5 py-1.5 text-xs text-white focus:outline-none">
              <option value="'Hind', sans-serif">Hind (मराठी ठळक)</option>
              <option value="'Poppins', sans-serif">Poppins (आधुनिक)</option>
              <option value="'Teko', sans-serif">Teko (Ultra Bold)</option>
              <option value="sans-serif">System Sans</option>
            </select>
          </div>

          <div>
            <label class="text-[11px] text-gray-300 block mb-1">फॉन्ट साईज: <span id="fontSizeDisplay" class="text-amber-400 font-bold">54px</span></label>
            <input type="range" id="fontSizeSlider" min="28" max="90" value="54" class="w-full accent-indigo-500">
          </div>
        </div>

        <!-- Text Colors -->
        <div class="grid grid-cols-2 gap-2 text-xs">
          <div class="flex items-center justify-between p-2 rounded-lg bg-darkbg border border-darkborder">
            <span class="text-[11px] text-gray-300">शीर्षक रंग:</span>
            <input type="color" id="primaryColorInput" value="#ffffff" class="w-7 h-7 rounded border-0 bg-transparent cursor-pointer">
          </div>
          <div class="flex items-center justify-between p-2 rounded-lg bg-darkbg border border-darkborder">
            <span class="text-[11px] text-gray-300">उपशीर्षक रंग:</span>
            <input type="color" id="secondaryColorInput" value="#facc15" class="w-7 h-7 rounded border-0 bg-transparent cursor-pointer">
          </div>
        </div>
      </div>

      <!-- Badges, Emojis & Photos -->
      <div class="bg-darkcard border border-darkborder rounded-2xl p-3.5 shadow-lg flex flex-col gap-3">
        <h2 class="text-xs font-bold text-gray-300 uppercase tracking-wider flex items-center justify-between">
          <span class="flex items-center gap-1.5"><i class="fa-solid fa-shapes text-emerald-400"></i> स्टिकर्स आणि बॅजेस</span>
        </h2>

        <div>
          <div class="flex flex-wrap gap-1.5">
            <button onclick="addBadge('100% FREE', '#10b981')" class="px-2.5 py-1 rounded bg-emerald-500/20 text-emerald-400 border border-emerald-500/40 text-xs font-bold">100% FREE</button>
            <button onclick="addBadge('₹ 1,00,000', '#f59e0b')" class="px-2.5 py-1 rounded bg-amber-500/20 text-amber-400 border border-amber-500/40 text-xs font-bold">₹ 1,00,000</button>
            <button onclick="addBadge('LIVE 🔴', '#ef4444')" class="px-2.5 py-1 rounded bg-rose-500/20 text-rose-400 border border-rose-500/40 text-xs font-bold">LIVE 🔴</button>
            <button onclick="addBadge('PRO TRICK ⚡', '#8b5cf6')" class="px-2.5 py-1 rounded bg-purple-500/20 text-purple-400 border border-purple-500/40 text-xs font-bold">PRO TRICK ⚡</button>
          </div>
        </div>

        <div>
          <div class="flex flex-wrap gap-2 text-xl bg-darkbg p-2 rounded-xl border border-darkborder">
            <button onclick="addEmoji('🔥')" class="hover:scale-125 transition-transform">🔥</button>
            <button onclick="addEmoji('🤑')" class="hover:scale-125 transition-transform">🤑</button>
            <button onclick="addEmoji('😱')" class="hover:scale-125 transition-transform">😱</button>
            <button onclick="addEmoji('🚀')" class="hover:scale-125 transition-transform">🚀</button>
            <button onclick="addEmoji('💥')" class="hover:scale-125 transition-transform">💥</button>
            <button onclick="addEmoji('💸')" class="hover:scale-125 transition-transform">💸</button>
          </div>
        </div>

        <!-- Custom Uploads -->
        <div class="grid grid-cols-2 gap-2 text-xs">
          <label class="p-2.5 rounded-xl bg-darkbg border border-dashed border-darkborder hover:border-indigo-400 flex flex-col items-center justify-center cursor-pointer transition-all">
            <i class="fa-solid fa-user-plus text-indigo-400 mb-1"></i>
            <span class="text-gray-300 font-medium">स्वतःचा फोटो जोडा</span>
            <input type="file" id="userPhotoInput" accept="image/*" class="hidden" onchange="handleImageUpload(event, 'photo')">
          </label>
          <label class="p-2.5 rounded-xl bg-darkbg border border-dashed border-darkborder hover:border-amber-400 flex flex-col items-center justify-center cursor-pointer transition-all">
            <i class="fa-solid fa-image text-amber-400 mb-1"></i>
            <span class="text-gray-300 font-medium">बॅकग्राउंड फोटो</span>
            <input type="file" id="bgPhotoInput" accept="image/*" class="hidden" onchange="handleImageUpload(event, 'bg')">
          </label>
        </div>
      </div>
    </div>

    <!-- RIGHT SECTION: Canvas & Live Payment System (7 Cols) -->
    <div class="lg:col-span-7 flex flex-col gap-4">
      
      <!-- Canvas Card -->
      <div class="bg-darkcard border border-darkborder rounded-2xl p-4 shadow-xl flex flex-col gap-3">
        <!-- Canvas Toolbar -->
        <div class="flex items-center justify-between flex-wrap gap-2">
          <div class="flex items-center gap-2">
            <button id="ratio169" class="px-2.5 py-1 rounded bg-indigo-600 text-white text-xs font-semibold">16:9 YouTube</button>
            <button id="ratio916" class="px-2.5 py-1 rounded bg-darkbg text-gray-400 hover:text-white border border-darkborder text-xs font-semibold">9:16 Shorts</button>
          </div>
          <span class="text-gray-400 text-[11px]">1280 × 720 HD</span>
        </div>

        <!-- Canvas Container -->
        <div class="relative w-full aspect-video bg-black rounded-xl overflow-hidden shadow-2xl border border-slate-700/80 flex items-center justify-center">
          <canvas id="thumbnailCanvas" width="1280" height="720" class="w-full h-full object-contain cursor-crosshair"></canvas>
        </div>

        <!-- Bottom Action Bar -->
        <div class="flex items-center justify-between flex-wrap gap-2 pt-1">
          <div class="flex items-center gap-2">
            <button onclick="clearCanvasElements()" class="px-3 py-2 rounded-lg bg-darkbg hover:bg-slate-700 text-gray-300 text-xs font-medium border border-darkborder">
              <i class="fa-solid fa-rotate-left mr-1"></i> रिसेट
            </button>
            <button onclick="addLightningEffect()" class="px-3 py-2 rounded-lg bg-darkbg hover:bg-slate-700 text-amber-300 text-xs font-medium border border-darkborder">
              <i class="fa-solid fa-bolt mr-1"></i> लाईट इफेक्ट
            </button>
          </div>

          <button onclick="downloadThumbnail()" class="px-5 py-2.5 rounded-xl bg-gradient-to-r from-emerald-500 to-teal-500 hover:from-emerald-400 hover:to-teal-400 text-slate-950 font-black text-sm shadow-lg shadow-emerald-500/30 transition-all active:scale-95 flex items-center gap-2">
            <i class="fa-solid fa-download text-base"></i>
            <span>HD थंबनेल डाऊनलोड करा</span>
          </button>
        </div>
      </div>

      <!-- LIVE Direct Payment Box (Locked to Dnyaneshwar Deokar's Real Details) -->
      <div class="bg-gradient-to-br from-indigo-950/60 via-darkcard to-slate-900 border border-indigo-500/30 rounded-2xl p-4 shadow-xl">
        <div class="flex items-center justify-between flex-wrap gap-2 mb-3">
          <div class="flex items-center gap-2">
            <div class="w-8 h-8 rounded-lg bg-amber-500/20 text-amber-400 flex items-center justify-center">
              <i class="fa-solid fa-indian-rupee-sign text-sm"></i>
            </div>
            <div>
              <h3 class="text-sm font-bold text-white flex items-center gap-1.5">
                थेट बँक खात्यात पैसे पाठवा / मिळवा
              </h3>
              <p class="text-[11px] text-gray-400">Dnyaneshwar Deokar अधिकृत खात्यात थेट व्यवहार</p>
            </div>
          </div>
          <span class="text-[10px] bg-amber-500/10 text-amber-300 border border-amber-500/30 px-2 py-0.5 rounded-full font-bold">
            0% कमिशन | थेट बँक जमा
          </span>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-3 items-center bg-darkbg/80 p-3 rounded-xl border border-darkborder">
          <!-- UPI QR Code Display (Locked to dnyaneshwardeokar@ybl) -->
          <div class="flex items-center gap-3">
            <div class="w-20 h-20 bg-white p-1 rounded-lg shrink-0 flex items-center justify-center shadow-md">
              <img id="displayQrCode" src="https://api.qrserver.com/v1/create-qr-code/?size=160x160&data=upi://pay?pa=dnyaneshwardeokar@ybl&pn=Dnyaneshwar%20Deokar" alt="UPI QR Code" class="w-full h-full object-contain">
            </div>
            <div>
     
