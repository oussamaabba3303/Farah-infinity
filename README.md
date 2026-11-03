<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>FARAH & INFINITY | Café • Restaurant • Salon de Thé Casablanca</title>
<script src="https://cdn.tailwindcss.com"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;800&family=Poppins:wght@300;400;500;600;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
<script>tailwind.config={theme:{extend:{colors:{gold:'#C9A227',gold2:'#E8C547',dark:'#0B0B0F',dark2:'#15151D',cream:'#FFF8F0',rouge:'#D32F2F'},fontFamily:{playfair:['"Playfair Display"','serif'],poppins:['Poppins','sans-serif']}}}}</script>
<style>
*{scroll-behavior:smooth}body{font-family:Poppins,sans-serif;background:#FFF8F0;color:#1a1a1a}
.zellige{background-image:radial-gradient(#C9A227 1px,transparent 1px);background-size:22px 22px;opacity:.12}
.hero-anim{animation:zoom 18s infinite alternate} @keyframes zoom{from{transform:scale(1)}to{transform:scale(1.15)}}
.card-h:hover{transform:translateY(-8px);box-shadow:0 20px 40px rgba(0,0,0,.15)} .card-h{transition:.4s}
.cat-pill.active{background:#0B0B0F!important;color:#E8C547!important;border-color:#C9A227!important}
.no-sb::-webkit-scrollbar{display:none}.no-sb{scrollbar-width:none}
.drawer{transition:.4s cubic-bezier(.4,0,.2,1)}
.gold-grad{background:linear-gradient(135deg,#C9A227,#E8C547,#C9A227)}
input,select,textarea{outline:none}input:focus,select:focus,textarea:focus{border-color:#C9A227!important;box-shadow:0 0 0 3px rgba(201,162,39,.2)}
.toast{animation:slideIn .3s} @keyframes slideIn{from{transform:translateX(100%);opacity:0}}
iframe{border-radius:16px}
.admin-tab.active{background:#C9A227;color:#000}
</style>
</head>
<body>
<!-- PROMO -->
<div id="promoBar" class="bg-dark text-center text-[13px] md:text-sm py-2 px-4 text-gold2 font-medium"></div>

<!-- NAV -->
<header class="sticky top-0 z-40 bg-dark/95 backdrop-blur-md border-b border-gold/30 shadow-lg">
<div class="max-w-7xl mx-auto flex items-center justify-between px-4 py-3">
<div class="flex items-center gap-3">
<div class="w-12 h-12 rounded-full gold-grad flex items-center justify-center text-2xl font-playfair font-bold text-black shadow">F</div>
<div><h1 id="siteName" class="font-playfair font-bold text-white text-lg leading-tight">FARAH & INFINITY</h1><p id="siteSub" class="text-gold2 text-[11px] tracking-widest">CAFÉ • RESTAURANT • SALON DE THÉ</p></div>
</div>
<nav class="hidden md:flex gap-6 text-white text-sm font-medium">
<a href="#menu" class="hover:text-gold2">Menu</a><a href="#jour" class="hover:text-gold2">Plat du Jour</a><a href="#videos" class="hover:text-gold2">Vidéos</a><a href="#about" class="hover:text-gold2">À propos</a><a href="#contact" class="hover:text-gold2">Contact</a>
</nav>
<div class="flex items-center gap-2">
<a id="callBtn" href="tel:+212662253212" class="hidden sm:flex bg-white/10 text-white px-3 py-2 rounded-full text-sm hover:bg-white/20"><i class="fa fa-phone mr-2 text-gold2"></i><span id="phoneTxt">06 62 25 32 12</span></a>
<button onclick="toggleCart(true)" class="relative bg-gold text-black w-11 h-11 rounded-full font-bold hover:bg-gold2"><i class="fa fa-shopping-basket"></i><span id="cartCount" class="absolute -top-1 -right-1 bg-rouge text-white text-xs w-6 h-6 rounded-full flex items-center justify-center">0</span></button>
<button class="md:hidden text-white text-2xl ml-1" onclick="document.getElementById('mobMenu').classList.toggle('hidden')"><i class="fa fa-bars"></i></button>
</div></div>
<div id="mobMenu" class="hidden md:hidden bg-dark2 px-6 py-4 flex flex-col gap-3 text-white"><a href="#menu">Menu</a><a href="#jour">Plat du Jour</a><a href="#videos">Vidéos</a><a href="#contact">Contact</a></div>
</header>

<!-- HERO -->
<section class="relative min-h-[92vh] flex items-center overflow-hidden bg-dark">
<img id="heroImg" src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=1400" class="absolute inset-0 w-full h-full object-cover hero-anim opacity-60">
<div class="absolute inset-0 bg-gradient-to-r from-black via-black/70 to-black/30"></div>
<div class="absolute inset-0 zellige"></div>
<div class="relative max-w-7xl mx-auto px-5 py-16 grid md:grid-cols-2 gap-10 items-center w-full">
<div>
<div class="inline-flex items-center gap-2 bg-gold/20 border border-gold text-gold2 px-4 py-1.5 rounded-full text-sm mb-5"><i class="fa fa-star"></i> <span id="heroBadge">Authentique Cuisine Marocaine à Casablanca</span></div>
<h2 id="heroTitle" class="font-playfair text-4xl md:text-6xl font-bold text-white leading-tight">Bienvenue chez <span class="text-gold2">Farah & Infinity</span></h2>
<p id="heroDesc" class="text-gray-200 mt-4 text-lg">Tajines beldi, Tanjia, Couscous du Vendredi, Rfissa, Pizza, Tacos & Salon de Thé. Le goût du Maroc, servi avec amour.</p>
<div class="flex flex-wrap gap-3 mt-7">
<a href="#menu" class="gold-grad text-black font-bold px-7 py-3.5 rounded-full hover:scale-105 transition"><i class="fa fa-utensils mr-2"></i>Voir le Menu</a>
<a href="https://wa.me/212662253212?text=Bonjour%20FARAH%20%26%20INFINITY%2C%20je%20veux%20commander" target="_blank" class="bg-[#25D366] text-white font-bold px-7 py-3.5 rounded-full hover:scale-105 transition"><i class="fab fa-whatsapp mr-2"></i>Commander</a>
</div>
<div class="flex flex-wrap gap-3 mt-6 text-sm">
<div class="bg-white/10 backdrop-blur text-white px-4 py-2 rounded-full"><i class="fa fa-clock text-gold2 mr-2"></i><span id="hoursTxt">7j/7 : 07h00 - 23h00</span></div>
<div class="bg-white/10 backdrop-blur text-white px-4 py-2 rounded-full"><i class="fa fa-location-dot text-gold2 mr-2"></i><span id="addrTxt">Route Azemmour, Casa</span></div>
</div></div>
<div class="hidden md:grid grid-cols-2 gap-4">
<img src="https://images.unsplash.com/photo-1541518763669-27fef04b14ea?w=600" class="rounded-2xl h-56 w-full object-cover border-2 border-gold/40 shadow-2xl rotate-2">
<img src="https://images.unsplash.com/photo-1585937421612-70a008356fbe?w=600" class="rounded-2xl h-56 w-full object-cover border-2 border-gold/40 shadow-2xl -rotate-2 mt-8">
<img src="https://images.unsplash.com/photo-1544787219-7f47ccb76574?w=600" class="rounded-2xl h-48 w-full object-cover border-2 border-gold/40 shadow-2xl -rotate-1">
<img src="https://images.unsplash.com/photo-1513104890138-7c749659a591?w=600" class="rounded-2xl h-48 w-full object-cover border-2 border-gold/40 shadow-2xl rotate-1 mt-[-20px]">
</div></div></section>

<!-- STATS -->
<div class="bg-gold text-black py-4"><div class="max-w-6xl mx-auto grid grid-cols-4 text-center font-bold"><div><div class="text-2xl">60+</div><div class="text-xs">Plats</div></div><div><div class="text-2xl">4.8★</div><div class="text-xs">Avis clients</div></div><div><div class="text-2xl">7j/7</div><div class="text-xs">Ouvert</div></div><div><div class="text-2xl">15min</div><div class="text-xs">Service rapide</div></div></div></div>

<!-- MENU -->
<section id="menu" class="max-w-7xl mx-auto px-4 py-14">
<div class="text-center mb-8"><p class="text-rouge font-bold tracking-widest">— NOTRE CARTE —</p><h3 class="font-playfair text-4xl font-bold">Menu & Boutique</h3><p class="text-gray-600 mt-2">Cliquez sur <b>+</b> pour ajouter au panier • Commande via WhatsApp</p></div>
<div class="flex gap-2 mb-4 max-w-xl mx-auto"><div class="relative flex-1"><i class="fa fa-search absolute left-4 top-4 text-gray-400"></i><input id="searchInp" oninput="renderProducts()" placeholder="Rechercher: tajine, pizza, jus..." class="w-full border rounded-full pl-11 pr-4 py-3 bg-white"></div></div>
<div id="catBar" class="flex gap-2 overflow-x-auto no-sb pb-3 justify-start md:justify-center"></div>
<div id="grid" class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 md:gap-6 mt-6"></div>
</section>

<!-- PLAT DU JOUR -->
<section id="jour" class="bg-dark py-14 relative overflow-hidden"><div class="absolute inset-0 zellige"></div>
<div class="max-w-6xl mx-auto px-4 relative"><div class="text-center mb-8"><p class="text-gold2 font-bold tracking-widest">— PLAT DU JOUR BELDI —</p><h3 class="font-playfair text-4xl font-bold text-white">Mercredi Rfissa • Vendredi Couscous</h3></div>
<div class="grid md:grid-cols-2 gap-6">
<div class="bg-white/5 border border-gold/30 rounded-3xl overflow-hidden"><img src="https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=800" class="h-64 w-full object-cover"><div class="p-6"><span class="bg-rouge text-white text-xs px-3 py-1 rounded-full font-bold">MERCREDI</span><h4 class="text-white font-playfair text-2xl font-bold mt-2">Rfissa Poulet Beldi</h4><p class="text-gray-300 text-sm mt-2">Msemen, lentilles, fenugrec, oignons caramélisés, poulet fermier. La vraie Rfissa Fassia.</p><div class="flex items-center justify-between mt-4"><div><span class="text-gold2 font-bold text-2xl">70 DH</span> <span class="text-gray-400 text-sm">/ Beldi • 50 DH poulet</span></div><button onclick="addToCartByName('Rfissa Poulet Beldi')" class="gold-grad px-5 py-2.5 rounded-full font-bold text-sm">+ Ajouter</button></div></div></div>
<div class="bg-white/5 border border-gold/30 rounded-3xl overflow-hidden"><img src="https://images.unsplash.com/photo-1585937421612-70a008356fbe?w=800" class="h-64 w-full object-cover"><div class="p-6"><span class="bg-gold text-black text-xs px-3 py-1 rounded-full font-bold">VENDREDI</span><h4 class="text-white font-playfair text-2xl font-bold mt-2">Couscous Viande / Poulet</h4><p class="text-gray-300 text-sm mt-2">Couscous roulé à la main, 7 légumes, viande tendre, tfaya. Servi avec lben & harira.</p><div class="flex items-center justify-between mt-4"><div><span class="text-gold2 font-bold text-2xl">50 DH</span> <span class="text-gray-400 text-sm">/ viande • 40 DH poulet</span></div><button onclick="addToCartByName('Couscous Viande')" class="gold-grad px-5 py-2.5 rounded-full font-bold text-sm">+ Ajouter</button></div></div></div>
</div></div></section>

<!-- VIDEOS -->
<section id="videos" class="max-w-7xl mx-auto px-4 py-14">
<div class="text-center mb-8"><p class="text-rouge font-bold tracking-widest">— SAVEURS DU MAROC EN VIDÉO —</p><h3 class="font-playfair text-4xl font-bold">Nos Spécialités en Images</h3></div>
<div id="videoGrid" class="grid md:grid-cols-3 gap-6"></div>
</section>

<!-- ABOUT -->
<section id="about" class="bg-white py-14 border-y"><div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-10 items-center">
<img src="https://images.unsplash.com/photo-1552566626-52f8b828add9?w=800" class="rounded-3xl shadow-2xl h-96 w-full object-cover">
<div><p class="text-rouge font-bold">— ESPACE FARAH & INFINITY —</p><h3 class="font-playfair text-4xl font-bold mt-2">Café • Restaurant • Salon de Thé</h3><p class="text-gray-600 mt-4">Situé sur Route Azemmour à Casablanca, notre espace vous accueille dans une ambiance familiale moderne. Cuisine marocaine authentique (Tajines, Tanjia, Grillades), fast-food (Pizza, Tacos), petits-déjeuners beldi et salon de thé.</p>
<div class="grid grid-cols-2 gap-3 mt-6 text-sm"><div class="bg-cream p-3 rounded-xl">✅ Produits frais beldi</div><div class="bg-cream p-3 rounded-xl">✅ Prix familiaux</div><div class="bg-cream p-3 rounded-xl">✅ Terrasse & Salle</div><div class="bg-cream p-3 rounded-xl">✅ Service rapide</div></div>
<a href="#contact" class="inline-block mt-6 bg-dark text-gold2 px-7 py-3 rounded-full font-bold">Réserver une Table</a></div>
</div></section>

<!-- AVIS -->
<section class="max-w-6xl mx-auto px-4 py-12"><h3 class="font-playfair text-3xl font-bold text-center mb-8">Ce que disent nos clients ❤️</h3>
<div class="grid md:grid-cols-3 gap-5">
<div class="bg-white p-6 rounded-2xl shadow"><div class="text-gold">★★★★★</div><p class="mt-3 text-sm">"Meilleur couscous du vendredi à Casa! Service top et prix raisonnables."</p><b class="text-sm mt-3 block">— Yasmine B.</b></div>
<div class="bg-white p-6 rounded-2xl shadow"><div class="text-gold">★★★★★</div><p class="mt-3 text-sm">"Rfissa bldia zwina bzaf, tanjia tayba 3la 7a9ha. Je recommande."</p><b class="text-sm mt-3 block">— Mehdi E.</b></div>
<div class="bg-white p-6 rounded-2xl shadow"><div class="text-gold">★★★★★</div><p class="mt-3 text-sm">"Petit-déj amazighi complet + thé. Terrasse agréable sur route Azemmour."</p><b class="text-sm mt-3 block">— Salma R.</b></div>
</div></section>

<!-- CONTACT -->
<section id="contact" class="bg-dark text-white py-14"><div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-8">
<div><h3 class="font-playfair text-3xl font-bold text-gold2">Contact & Réservation</h3>
<div class="mt-6 space-y-4 text-sm">
<div class="flex gap-3"><i class="fa fa-location-dot text-gold2 text-xl"></i><div><b>Adresse</b><br><span id="addrFull">Route Azemmour, Casablanca 70000</span></div></div>
<div class="flex gap-3"><i class="fa fa-phone text-gold2 text-xl"></i><div><b>Téléphone / WhatsApp</b><br><a href="tel:+212662253212" class="text-gold2 font-bold text-lg">+212 6 62 25 32 12</a></div></div>
<div class="flex gap-3"><i class="fab fa-instagram text-gold2 text-xl"></i><div><b>Instagram</b><br><a id="instaLink" href="https://www.instagram.com/farahinfiniti?obrf=NTU2OHh1bjJ1Z3Bw" target="_blank" class="underline text-gold2">@farahinfiniti</a></div></div>
<div class="flex gap-3"><i class="fa fa-clock text-gold2 text-xl"></i><div><b>Horaires</b><br>7j/7 : 07h00 - 23h00<br>Petit-déj : 7h00 - 11h30 • Vendredi Couscous • Mercredi Rfissa</div></div>
</div>
<form onsubmit="event.preventDefault();reserveWA()" class="mt-6 bg-white/5 border border-gold/30 p-5 rounded-2xl grid grid-cols-2 gap-3">
<input id="rName" required placeholder="Nom" class="col-span-2 md:col-span-1 bg-white/10 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-gray-400">
<input id="rPhone" required placeholder="Téléphone" class="bg-white/10 border border-white/20 rounded-xl px-4 py-3 text-white placeholder-gray-400">
<input id="rDate" type="date" class="bg-white/10 border border-white/20 rounded-xl px-4 py-3 text-white">
<input id="rGuest" type="number" min="1" value="2" placeholder="Personnes" class="bg-white/10 border border-white/20 rounded-xl px-4 py-3 text-white">
<button class="col-span-2 gold-grad text-black font-bold py-3 rounded-xl">Réserver via WhatsApp</button>
</form></div>
<div><iframe src="https://www.google.com/maps?q=Route+Azemmour+Casablanca+Morocco&output=embed" class="w-full h-[520px] border-2 border-gold/40" loading="lazy"></iframe></div>
</div></section>

<footer class="bg-black text-gray-400 py-8 text-sm text-center px-4">
<b class="text-white font-playfair text-lg">FARAH & INFINITY</b><br>Café • Restaurant • Salon de Thé — Casablanca<br><br>
<div class="flex justify-center gap-3"><a href="tel:+212662253212" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-black"><i class="fa fa-phone"></i></a><a href="https://wa.me/212662253212" target="_blank" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-black"><i class="fab fa-whatsapp"></i></a><a id="instaFoot" href="https://www.instagram.com/farahinfiniti?obrf=NTU2OHh1bjJ1Z3Bw" target="_blank" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-black"><i class="fab fa-instagram"></i></a></div>
<p class="mt-4">© 2026 Farah & Infinity • Tous droits réservés</p>
<button onclick="openLogin()" class="mt-3 text-xs underline opacity-50 hover:opacity-100">🔒 Admin / لوحة التحكم</button>
</footer>

<!-- FLOAT -->
<a href="https://wa.me/212662253212?text=Bonjour%2C%20je%20veux%20commander" target="_blank" class="fixed bottom-5 left-5 z-40 w-14 h-14 bg-[#25D366] rounded-full flex items-center justify-center text-white text-2xl shadow-2xl hover:scale-110 transition"><i class="fab fa-whatsapp"></i></a>

<!-- CART -->
<div id="cartOverlay" onclick="toggleCart(false)" class="hidden fixed inset-0 bg-black/60 z-50"></div>
<div id="cartDrawer" class="drawer fixed top-0 right-0 h-full w-full max-w-md bg-white z-50 translate-x-full flex flex-col shadow-2xl">
<div class="bg-dark text-white p-5 flex justify-between items-center"><h3 class="font-playfair text-xl font-bold"><i class="fa fa-shopping-basket text-gold2 mr-2"></i>Votre Panier</h3><button onclick="toggleCart(false)" class="text-2xl">×</button></div>
<div id="cartItems" class="flex-1 overflow-y-auto p-4 space-y-3"></div>
<div class="p-5 border-t bg-cream">
<div class="grid grid-cols-2 gap-2 mb-3"><input id="cName" placeholder="Votre nom" class="border rounded-xl px-3 py-2.5 text-sm"><input id="cPhone" placeholder="Téléphone" class="border rounded-xl px-3 py-2.5 text-sm"></div>
<select id="cType" class="w-full border rounded-xl px-3 py-2.5 text-sm mb-3"><option>Livraison à domicile</option><option>À emporter</option><option>Sur place</option></select>
<div class="flex justify-between font-bold text-lg mb-3"><span>Total:</span><span id="cartTotal" class="text-rouge">0 DH</span></div>
<button onclick="checkoutWA()" class="w-full bg-[#25D366] text-white font-bold py-3.5 rounded-xl"><i class="fab fa-whatsapp mr-2"></i>Commander via WhatsApp</button>
</div></div>

<!-- LOGIN -->
<div id="loginModal" class="hidden fixed inset-0 bg-black/70 z-[60] flex items-center justify-center p-4">
<div class="bg-white rounded-3xl p-8 w-full max-w-sm"><h3 class="font-playfair text-2xl font-bold text-center">🔒 Espace Admin</h3><p class="text-center text-sm text-gray-500 mb-5">لوحة التحكم - Farah & Infinity</p>
<input id="aUser" placeholder="Utilisateur (admin)" class="w-full border rounded-xl px-4 py-3 mb-3"><input id="aPass" type="password" placeholder="Mot de passe" class="w-full border rounded-xl px-4 py-3 mb-4">
<button onclick="doLogin()" class="w-full bg-dark text-gold2 font-bold py-3 rounded-xl">Se connecter</button>
<button onclick="document.getElementById('loginModal').classList.add('hidden')" class="w-full mt-2 text-sm text-gray-500">Annuler</button></div></div>

<!-- ADMIN -->
<div id="adminPanel" class="hidden fixed inset-0 bg-gray-100 z-[70] overflow-y-auto">
<div class="bg-dark text-white p-4 flex justify-between items-center sticky top-0 z-10"><h3 class="font-bold">⚙️ لوحة التحكم - Tableau de bord</h3><div class="flex gap-2"><button onclick="exportData()" class="bg-white/10 px-4 py-2 rounded-lg text-sm">📥 Export</button><button onclick="resetData()" class="bg-rouge px-4 py-2 rounded-lg text-sm">Reset</button><button onclick="closeAdmin()" class="bg-gold text-black px-4 py-2 rounded-lg text-sm font-bold">✕ Fermer</button></div></div>
<div class="max-w-6xl mx-auto p-4 grid md:grid-cols-[220px_1fr] gap-4">
<div class="flex md:flex-col gap-2 overflow-x-auto"><button onclick="showTab('general',this)" class="admin-tab active bg-white px-4 py-3 rounded-xl text-sm font-bold text-left whitespace-nowrap">🏠 Général</button><button onclick="showTab('products',this)" class="admin-tab bg-white px-4 py-3 rounded-xl text-sm font-bold text-left whitespace-nowrap">🍲 Produits (<span id="prodCount">0</span>)</button><button onclick="showTab('videos',this)" class="admin-tab bg-white px-4 py-3 rounded-xl text-sm font-bold text-left whitespace-nowrap">🎬 Vidéos</button><button onclick="showTab('orders',this)" class="admin-tab bg-white px-4 py-3 rounded-xl text-sm font-bold text-left whitespace-nowrap">📦 Commandes</button></div>
<div>
<div id="tab-general" class="bg-white rounded-2xl p-6 space-y-3">
<h4 class="font-bold text-lg mb-3">Informations générales</h4>
<label class="text-xs font-bold">Bannière promo</label><input id="s_promo" class="w-full border rounded-xl px-3 py-2 text-sm">
<div class="grid md:grid-cols-2 gap-3"><div><label class="text-xs font-bold">Titre Hero</label><input id="s_heroTitle" class="w-full border rounded-xl px-3 py-2 text-sm"></div><div><label class="text-xs font-bold">Badge Hero</label><input id="s_badge" class="w-full border rounded-xl px-3 py-2 text-sm"></div></div>
<label class="text-xs font-bold">Description Hero</label><textarea id="s_heroDesc" class="w-full border rounded-xl px-3 py-2 text-sm"></textarea>
<div class="grid md:grid-cols-2 gap-3"><div><label class="text-xs font-bold">Téléphone</label><input id="s_phone" class="w-full border rounded-xl px-3 py-2 text-sm"></div><div><label class="text-xs font-bold">Adresse</label><input id="s_addr" class="w-full border rounded-xl px-3 py-2 text-sm"></div></div>
<div class="grid md:grid-cols-2 gap-3"><div><label class="text-xs font-bold">Instagram URL</label><input id="s_insta" class="w-full border rounded-xl px-3 py-2 text-sm"></div><div><label class="text-xs font-bold">Horaires</label><input id="s_hours" class="w-full border rounded-xl px-3 py-2 text-sm"></div></div>
<label class="text-xs font-bold">Image Hero (URL)</label><input id="s_heroImg" class="w-full border rounded-xl px-3 py-2 text-sm">
<button onclick="saveGeneral()" class="bg-dark text-gold2 font-bold px-6 py-3 rounded-xl">💾 Enregistrer</button>
</div>
<div id="tab-products" class="hidden bg-white rounded-2xl p-6">
<h4 class="font-bold text-lg mb-3">Ajouter / Modifier produit</h4>
<div class="bg-gray-50 p-4 rounded-xl grid md:grid-cols-3 gap-2 mb-5">
<input id="p_name" placeholder="Nom (ex: Tajine Kefta)" class="border rounded-lg px-3 py-2 text-sm"><select id="p_cat" class="border rounded-lg px-3 py-2 text-sm"></select><input id="p_price" type="number" placeholder="Prix DH" class="border rounded-lg px-3 py-2 text-sm">
<input id="p_img" placeholder="Image URL (ou laisser vide)" class="border rounded-lg px-3 py-2 text-sm md:col-span-2"><input id="p_badge" placeholder="Badge: Populaire / Nouveau / Top" class="border rounded-lg px-3 py-2 text-sm">
<input id="p_desc" placeholder="Description" class="border rounded-lg px-3 py-2 text-sm md:col-span-3">
<input type="file" id="p_file" accept="image/*" class="text-sm md:col-span-2"><button onclick="addProduct()" class="bg-gold font-bold rounded-lg py-2 text-sm">+ Ajouter produit</button>
<input type="hidden" id="p_editId">
</div>
<div id="adminProdList" class="space-y-2 max-h-[500px] overflow-y-auto"></div>
</div>
<div id="tab-videos" class="hidden bg-white rounded-2xl p-6">
<h4 class="font-bold text-lg mb-3">Gérer les vidéos YouTube</h4>
<div class="grid md:grid-cols-3 gap-2 bg-gray-50 p-4 rounded-xl mb-4"><input id="v_title" placeholder="Titre" class="border rounded-lg px-3 py-2 text-sm"><input id="v_url" placeholder="Lien embed YouTube" class="border rounded-lg px-3 py-2 text-sm"><button onclick="addVideo()" class="bg-gold font-bold rounded-lg text-sm">+ Ajouter</button></div>
<div id="adminVidList" class="space-y-2"></div>
</div>
<div id="tab-orders" class="hidden bg-white rounded-2xl p-6"><h4 class="font-bold text-lg mb-3">Commandes reçues</h4><div id="adminOrderList" class="space-y-3"></div></div>
</div></div></div>

<div id="toasts" class="fixed bottom-5 right-5 z-[80] space-y-2"></div>

<script>
// ===== CONFIG =====
const ADMIN_USER="admin", ADMIN_PASS="farah123";
const IMG={
tajine:"https://images.unsplash.com/photo-1541518763669-27fef04b14ea?w=600",
tanjia:"https://images.unsplash.com/photo-1544025162-d76694265947?w=600",
couscous:"https://images.unsplash.com/photo-1585937421612-70a008356fbe?w=600",
rfissa:"https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=600",
pizza:"https://images.unsplash.com/photo-1513104890138-7c749659a591?w=600",
tacos:"https://images.unsplash.com/photo-1565299585323-38d6b0865b47?w=600",
sand:"https://images.unsplash.com/photo-1528735602780-2552fd46c7af?w=600",
pasta:"https://images.unsplash.com/photo-1621996346565-e3dbc646d9a9?w=600",
past:"https://images.unsplash.com/photo-1619895092538-128341789043?w=600",
salad:"https://images.unsplash.com/photo-1512621776951-a57141f2eefd?w=600",
bastilla:"https://images.unsplash.com/photo-1601050690597-df0568f70950?w=600",
chicken:"https://images.unsplash.com/photo-1598103442097-8b74394b95c6?w=600",
fish:"https://images.unsplash.com/photo-1519708227418-c8fd9a32b7a2?w=600",
bfast:"https://images.unsplash.com/photo-1533089860892-a7c6f0a88666?w=600",
msemen:"https://images.unsplash.com/photo-1565557623262-b51c2513a641?w=600",
tea:"https://images.unsplash.com/photo-1544787219-7f47ccb76574?w=600",
coffee:"https://images.unsplash.com/photo-1509042239860-f550ce710b93?w=600",
juice:"https://images.unsplash.com/photo-1600271886742-f049cd451bba?w=600",
ice:"https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=600",
soup:"https://images.unsplash.com/photo-1547592166-23ac45744acd?w=600",
bread:"https://images.unsplash.com/photo-1509440159596-0249088772ff?w=600"};
const CATS=[
{id:"all",n:"Tout",e:"🍽️"},{id:"tajines",n:"Tajines & Tanjia",e:"🍲"},{id:"jour",n:"Plat du Jour",e:"⭐"},{id:"pizza",n:"Pizza",e:"🍕"},{id:"tacos",n:"Tacos & Sandwichs",e:"🌮"},{id:"pates",n:"Pâtes & Pasticcio",e:"🍝"},{id:"salades",n:"Salades & Bastilla",e:"🥗"},{id:"poulet",n:"Poulet & Poisson",e:"🍗"},{id:"ptitdej",n:"Petit-Déjeuner",e:"🥐"},{id:"boissons",n:"Café, Thé & Jus",e:"☕"}];
const DEFAULT_PRODUCTS=[
{n:"Tanjia Grande (Bœuf)",c:"tajines",p:190,d:"Viande fondante, cuisson lente traditionnelle",i:IMG.tanjia,b:"Top"},
{n:"Tajine Poulet Beldi Moyen",c:"tajines",p:95,d:"Citron confit, olives, safran",i:IMG.tajine,b:"Populaire"},
{n:"Tajine Poulet Beldi Grand",c:"tajines",p:185,d:"Format familial, poulet fermier",i:IMG.tajine,b:""},
{n:"Tajine Chèvre Moyen",c:"tajines",p:95,d:"Viande de chèvre, légumes",i:IMG.tajine,b:""},
{n:"Tajine Chèvre Grand",c:"tajines",p:190,d:"Format familial",i:IMG.tajine,b:""},
{n:"Tajine Bœuf Moyen",c:"tajines",p:95,d:"Pruneaux & amandes ou légumes",i:IMG.tanjia,b:""},
{n:"Tanjia Moyenne",c:"tajines",p:110,d:"Spécialité Marrakech",i:IMG.tanjia,b:"Nouveau"},
{n:"Tajine Sardine",c:"tajines",p:40,d:"Chermoula, tomate, olives",i:IMG.fish,b:""},
{n:"Couscous Viande (Vendredi)",c:"jour",p:50,d:"7 légumes, tfaya, lben",i:IMG.couscous,b:"Vendredi"},
{n:"Couscous Poulet (Vendredi)",c:"jour",p:40,d:"Légumes frais, bouillon",i:IMG.couscous,b:"Vendredi"},
{n:"Rfissa Poulet Beldi (Mercredi)",c:"jour",p:70,d:"Msemen, lentilles, poulet fermier",i:IMG.rfissa,b:"Mercredi"},
{n:"Rfissa Poulet (Mercredi)",c:"jour",p:50,d:"Recette fassia authentique",i:IMG.rfissa,b:"Mercredi"},
{n:"Pizza Royale",c:"pizza",p:70,d:"Mixte complète, fromage",i:IMG.pizza,b:"Top"},
{n:"Pizza 4 Saisons",c:"pizza",p:70,d:"4 garnitures",i:IMG.pizza,b:""},
{n:"Pizza Fruits de Mer",c:"pizza",p:65,d:"Crevettes, calamars",i:IMG.pizza,b:""},
{n:"Pizza 4 Fromages",c:"pizza",p:50,d:"Mozzarella, gouda, edam...",i:IMG.pizza,b:""},
{n:"Pizza Viande Hachée",c:"pizza",p:50,d:"Sauce tomate, fromage",i:IMG.pizza,b:""},
{n:"Pizza Poulet",c:"pizza",p:45,d:"Poulet mariné",i:IMG.pizza,b:""},
{n:"Pizza Thon",c:"pizza",p:35,d:"Thon, olives, oignons",i:IMG.pizza,b:""},
{n:"Pizza Margarita",c:"pizza",p:30,d:"Tomate, mozzarella",i:IMG.pizza,b:""},
{n:"Tacos Viande Hachée",c:"tacos",p:40,d:"Frites, sauce algérienne",i:IMG.tacos,b:"Populaire"},
{n:"Tacos Mixte",c:"tacos",p:40,d:"Poulet + viande",i:IMG.tacos,b:""},
{n:"Tacos Poulet",c:"tacos",p:30,d:"Poulet crispy",i:IMG.tacos,b:""},
{n:"Tacos Nuggets",c:"tacos",p:30,d:"Nuggets, fromage",i:IMG.tacos,b:""},
{n:"Sandwich Viande Hachée",c:"tacos",p:30,d:"Kefta, crudités",i:IMG.sand,b:""},
{n:"Sandwich Mixte",c:"tacos",p:30,d:"Dinde + kefta",i:IMG.sand,b:""},
{n:"Sandwich Dinde",c:"tacos",p:25,d:"Dinde fumée",i:IMG.sand,b:""},
{n:"Sandwich Thon",c:"tacos",p:20,d:"Thon, œuf, olives",i:IMG.sand,b:""},
{n:"Spaghetti Fruits de Mer",c:"pates",p:70,d:"Crevettes, sauce tomate",i:IMG.pasta,b:"Top"},
{n:"Spaghetti Bolognaise",c:"pates",p:40,d:"Viande hachée",i:IMG.pasta,b:""},
{n:"Pâtes Sauce Blanche",c:"pates",p:40,d:"Crème, champignons, poulet",i:IMG.pasta,b:""},
{n:"Pasticcio Mix",c:"pates",p:50,d:"Gratin béchamel mixte",i:IMG.past,b:""},
{n:"Pasticcio Viande Hachée",c:"pates",p:45,d:"Gratin béchamel",i:IMG.past,b:""},
{n:"Pasticcio Poulet",c:"pates",p:40,d:"Poulet, béchamel gratinée",i:IMG.past,b:""},
{n:"Bastilla Fruits de Mer",c:"salades",p:80,d:"Feuilleté croustillant",i:IMG.bastilla,b:"Luxe"},
{n:"Bastilla Poulet",c:"salades",p:60,d:"Amandes, cannelle",i:IMG.bastilla,b:""},
{n:"Salade Royale",c:"salades",p:70,d:"Mixte complète fruits de mer",i:IMG.salad,b:""},
{n:"Salade Pêcheur",c:"salades",p:60,d:"Poisson, crevettes",i:IMG.salad,b:""},
{n:"Salade César",c:"salades",p:40,d:"Poulet, parmesan",i:IMG.salad,b:""},
{n:"Salade Maison",c:"salades",p:40,d:"Composition du chef",i:IMG.salad,b:""},
{n:"Salade Niçoise",c:"salades",p:35,d:"Thon, œuf, olives",i:IMG.salad,b:""},
{n:"Salade Marocaine",c:"salades",p:20,d:"Tomate, concombre, oignon",i:IMG.salad,b:""},
{n:"Poulet Complet Rôti",c:"poulet",p:140,d:"Frites + pain + sauces",i:IMG.chicken,b:"Familial"},
{n:"Demi Poulet Rôti",c:"poulet",p:70,d:"Frites maison",i:IMG.chicken,b:"Populaire"},
{n:"Quart Poulet Rôti",c:"poulet",p:35,d:"Frites + pain",i:IMG.chicken,b:""},
{n:"Friture Mixte Poisson",c:"poulet",p:100,d:"Calamars, crevettes, poisson",i:IMG.fish,b:""},
{n:"Petit-Déj Fassia",c:"ptitdej",p:38,d:"Khlii, hssoua, huile olive, jus, thé/café",i:IMG.bfast,b:"Top"},
{n:"Petit-Déj Amazighi",c:"ptitdej",p:35,d:"Amlou, argan, miel, croissant, hssoua",i:IMG.bfast,b:""},
{n:"Petit-Déj Beldi",c:"ptitdej",p:25,d:"Harcha, msemen, hssoua, jus",i:IMG.msemen,b:""},
{n:"Petit-Déj Farah",c:"ptitdej",p:25,d:"Omelette, fromage, jus, pain",i:IMG.bfast,b:""},
{n:"Petit-Déj Spécial",c:"ptitdej",p:22,d:"Fromage, jus orange, thé/café",i:IMG.bfast,b:""},
{n:"Harira Marocaine",c:"boissons",p:15,d:"Soupe traditionnelle, dattes",i:IMG.soup,b:""},
{n:"Thé à la Menthe Grand",c:"boissons",p:20,d:"Théière familiale",i:IMG.tea,b:""},
{n:"Thé Moyen",c:"boissons",p:15,d:"Thé menthe",i:IMG.tea,b:""},
{n:"Café au Lait / Lavazza",c:"boissons",p:14,d:"Café crème",i:IMG.coffee,b:""},
{n:"Café Noir / Américain",c:"boissons",p:12,d:"Express",i:IMG.coffee,b:""},
{n:"Jus Panaché",c:"boissons",p:30,d:"Multi-couches fruits",i:IMG.juice,b:"Top"},
{n:"Jus d'Avocat",c:"boissons",p:25,d:"Avocat, amandes, lait",i:IMG.juice,b:""},
{n:"Jus de Mangue / Ananas",c:"boissons",p:25,d:"100% naturel",i:IMG.juice,b:""},
{n:"Jus d'Orange",c:"boissons",p:20,d:"Pressé frais",i:IMG.juice,b:""},
{n:"Coupe Noix",c:"boissons",p:50,d:"Glace noix, chantilly",i:IMG.ice,b:"Dessert"},
{n:"Coupe Caramel",c:"boissons",p:40,d:"Caramel, glace vanille",i:IMG.ice,b:"Dessert"}
];
const DEFAULT_VIDEOS=[
{t:"Tajine Poulet Beldi - Recette Authentique",u:"https://www.youtube.com/embed/4LxNSkRiaGg"},
{t:"Couscous Marocain du Vendredi",u:"https://www.youtube.com/embed/AClImR0Xw6k"},
{t:"Thé à la Menthe & Msemen",u:"https://www.youtube.com/embed/jWfDLToqk1E"}];
const DEFAULT_SETTINGS={promo:"🔥 Offre Spéciale : Couscous Vendredi + Thé offert | Rfissa Mercredi | Livraison rapide Casablanca",heroTitle:"Bienvenue chez Farah & Infinity",heroDesc:"Tajines beldi, Tanjia, Couscous du Vendredi, Rfissa, Pizza, Tacos & Salon de Thé. Le goût du Maroc, servi avec amour.",badge:"Authentique Cuisine Marocaine à Casablanca",phone:"+212 6 62 25 32 12",addr:"Route Azemmour, Casablanca 70000",insta:"https://www.instagram.com/farahinfiniti?obrf=NTU2OHh1bjJ1Z3Bw",hours:"7j/7 : 07h00 - 23h00 | Petit-déj : 7h - 11h30",heroImg:"https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=1400"};

// ===== STATE =====
let DB=JSON.parse(localStorage.getItem("farah_v1")||"null")||{settings:DEFAULT_SETTINGS,products:DEFAULT_PRODUCTS.map((p,i)=>({...p,id:i+1})),videos:DEFAULT_VIDEOS};
let cart=JSON.parse(localStorage.getItem("farah_cart")||"[]");
let orders=JSON.parse(localStorage.getItem("farah_orders")||"[]");
let activeCat="all";
function save(){localStorage.setItem("farah_v1",JSON.stringify(DB));localStorage.setItem("farah_cart",JSON.stringify(cart));localStorage.setItem("farah_orders",JSON.stringify(orders))}
function toast(m){const d=document.createElement("div");d.className="toast bg-dark text-white px-5 py-3 rounded-xl shadow-2xl text-sm";d.innerHTML=m;document.getElementById("toasts").appendChild(d);setTimeout(()=>d.remove(),3000)}

// ===== RENDER =====
function renderAll(){const s=DB.settings;
document.getElementById("promoBar").textContent=s.promo;
document.getElementById("heroTitle").innerHTML=s.heroTitle.replace("Farah & Infinity",'<span class="text-gold2">Farah & Infinity</span>');
document.getElementById("heroDesc").textContent=s.heroDesc;document.getElementById("heroBadge").textContent=s.badge;
document.getElementById("heroImg").src=s.heroImg;document.getElementById("phoneTxt").textContent=s.phone;
document.getElementById("addrTxt").textContent=s.addr.split(",")[0];document.getElementById("addrFull").textContent=s.addr;
document.getElementById("hoursTxt").textContent=s.hours.split("|")[0];document.getElementById("instaLink").href=s.insta;document.getElementById("instaFoot").href=s.insta;
renderCats();renderProducts();renderVideos();renderCart();
document.getElementById("p_cat").innerHTML=CATS.filter(c=>c.id!=="all").map(c=>`<option value="${c.id}">${c.e} ${c.n}</option>`).join("");
}
function renderCats(){document.getElementById("catBar").innerHTML=CATS.map(c=>`<button onclick="setCat('${c.id}')" class="cat-pill ${activeCat===c.id?'active':''} whitespace-nowrap bg-white border px-5 py-2.5 rounded-full text-sm font-bold shadow hover:border-gold">${c.e} ${c.n}</button>`).join("")}
function setCat(id){activeCat=id;renderCats();renderProducts()}
function renderProducts(){const q=(document.getElementById("searchInp").value||"").toLowerCase();
const list=DB.products.filter(p=>(activeCat==="all"||p.c===activeCat)&&(p.n.toLowerCase().includes(q)||p.d.toLowerCase().includes(q)));
document.getElementById("grid").innerHTML=list.map(p=>`
<div class="card-h bg-white rounded-2xl overflow-hidden shadow-md border">
<div class="relative"><img src="${p.i}" class="h-40 md:h-48 w-full object-cover" loading="lazy" onerror="this.src='${IMG.tajine}'">
${p.b?`<span class="absolute top-2 left-2 bg-dark text-gold2 text-[11px] font-bold px-3 py-1 rounded-full">${p.b}</span>`:""}
<span class="absolute bottom-2 right-2 bg-white/95 font-bold text-rouge px-3 py-1 rounded-full text-sm">${p.p} DH</span></div>
<div class="p-3"><h4 class="font-bold text-sm md:text-base leading-tight">${p.n}</h4><p class="text-gray-500 text-xs mt-1 line-clamp-2">${p.d}</p>
<button onclick="addToCart(${p.id})" class="mt-3 w-full bg-dark text-white font-bold py-2.5 rounded-xl text-sm hover:bg-gold hover:text-black transition"><i class="fa fa-plus mr-2"></i>Ajouter</button>
</div></div>`).join("")||'<p class="col-span-4 text-center text-gray-500 py-10">Aucun plat trouvé.</p>';
document.getElementById("prodCount").textContent=DB.products.length}
function renderVideos(){document.getElementById("videoGrid").innerHTML=DB.videos.map(v=>`<div class="bg-white rounded-2xl overflow-hidden shadow-lg border"><div class="aspect-video"><iframe src="${v.u}" class="w-full h-full" allowfullscreen></iframe></div><div class="p-4 font-bold text-sm">${v.t}</div></div>`).join("")}

// ===== CART =====
function addToCart(id){const f=cart.find(c=>c.id===id);f?f.q++:cart.push({id,q:1});save();renderCart();toast("✅ Ajouté au panier");toggleCart(true)}
function addToCartByName(name){const p=DB.products.find(x=>x.n.includes(name.split(" ")[0])&&x.n.includes(name.split(" ")[1]||""));if(p)addToCart(p.id);else toast("Plat ajouté!")}
function toggleCart(o){document.getElementById("cartDrawer").classList.toggle("translate-x-full",!o);document.getElementById("cartOverlay").classList.toggle("hidden",!o)}
function chQ(id,d){const it=cart.find(c=>c.id===id);if(!it)return;it.q+=d;if(it.q<=0)cart=cart.filter(c=>c.id!==id);save();renderCart()}
function renderCart(){const box=document.getElementById("cartItems");let total=0;
document.getElementById("cartCount").textContent=cart.reduce((a,c)=>a+c.q,0);
if(!cart.length){box.innerHTML='<p class="text-center text-gray-400 py-10">Panier vide.<br>Choisissez vos plats 😋</p>';document.getElementById("cartTotal").textContent="0 DH";return}
box.innerHTML=cart.map(c=>{const p=DB.products.find(x=>x.id===c.id);if(!p)return"";total+=p.p*c.q;return `<div class="flex gap-3 bg-gray-50 p-2 rounded-xl border"><img src="${p.i}" class="w-16 h-16 rounded-lg object-cover"><div class="flex-1"><b class="text-sm">${p.n}</b><div class="text-rouge font-bold text-sm">${p.p} DH</div><div class="flex items-center gap-2 mt-1"><button onclick="chQ(${p.id},-1)" class="w-7 h-7 bg-white border rounded-full">-</button><b>${c.q}</b><button onclick="chQ(${p.id},1)" class="w-7 h-7 bg-dark text-white rounded-full">+</button></div></div></div>`}).join("");
document.getElementById("cartTotal").textContent=total+" DH"}
function checkoutWA(){if(!cart.length)return toast("Panier vide!");
const name=document.getElementById("cName").value||"Client",phone=document.getElementById("cPhone").value||"-",type=document.getElementById("cType").value;
let total=0,lines=cart.map(c=>{const p=DB.products.find(x=>x.id===c.id);total+=p.p*c.q;return `• ${c.q}x ${p.n} (${p.p}DH)`}).join("\n");
const msg=`Bonjour FARAH & INFINITY%0A🧾 NOUVELLE COMMANDE%0A👤 ${encodeURIComponent(name)}%0A📞 ${encodeURIComponent(phone)}%0A📦 ${encodeURIComponent(type)}%0A%0A${encodeURIComponent(lines)}%0A%0A💰 TOTAL: ${total} DH`;
orders.unshift({date:new Date().toLocaleString(),name,phone,type,total,items:lines});save();renderOrders();
window.open(`https://wa.me/212662253212?text=${msg}`,"_blank");cart=[];save();renderCart();toggleCart(false);toast("✅ Commande envoyée!")}
function reserveWA(){const n=document.getElementById("rName").value,p=document.getElementById("rPhone").value,d=document.getElementById("rDate").value,g=document.getElementById("rGuest").value;
window.open(`https://wa.me/212662253212?text=${encodeURIComponent(`Bonjour, je veux réserver:\n👤 ${n}\n📞 ${p}\n📅 ${d}\n👥 ${g} personnes`)}`,"_blank")}

// ===== ADMIN =====
function openLogin(){document.getElementById("loginModal").classList.remove("hidden")}
function doLogin(){if(document.getElementById("aUser").value===ADMIN_USER&&document.getElementById("aPass").value===ADMIN_PASS){document.getElementById("loginModal").classList.add("hidden");document.getElementById("adminPanel").classList.remove("hidden");loadAdmin();toast("Bienvenue Admin 👋")}else toast("❌ Identifiants incorrects")}
function closeAdmin(){document.getElementById("adminPanel").classList.add("hidden");renderAll()}
function showTab(id,btn){["general","products","videos","orders"].forEach(t=>document.getElementById("tab-"+t).classList.add("hidden"));document.getElementById("tab-"+id).classList.remove("hidden");document.querySelectorAll(".admin-tab").forEach(b=>b.classList.remove("active"));btn.classList.add("active")}
function loadAdmin(){const s=DB.settings;document.getElementById("s_promo").value=s.promo;document.getElementById("s_heroTitle").value=s.heroTitle;document.getElementById("s_heroDesc").value=s.heroDesc;document.getElementById("s_badge").value=s.badge;document.getElementById("s_phone").value=s.phone;document.getElementById("s_addr").value=s.addr;document.getElementById("s_insta").value=s.insta;document.getElementById("s_hours").value=s.hours;document.getElementById("s_heroImg").value=s.heroImg;renderAdminProds();renderAdminVids();renderOrders()}
function saveGeneral(){DB.settings={promo:document.getElementById("s_promo").value,heroTitle:document.getElementById("s_heroTitle").value,heroDesc:document.getElementById("s_heroDesc").value,badge:document.getElementById("s_badge").value,phone:document.getElementById("s_phone").value,addr:document.getElementById("s_addr").value,insta:document.getElementById("s_insta").value,hours:document.getElementById("s_hours").value,heroImg:document.getElementById("s_heroImg").value};save();toast("✅ Enregistré")}
function renderAdminProds(){document.getElementById("adminProdList").innerHTML=DB.products.map(p=>`<div class="flex items-center gap-2 border rounded-xl p-2"><img src="${p.i}" class="w-12 h-12 rounded-lg object-cover"><div class="flex-1 text-sm"><b>${p.n}</b><br><span class="text-gray-500">${p.c} • ${p.p} DH</span></div><button onclick="editProd(${p.id})" class="bg-blue-100 text-blue-700 px-3 py-1.5 rounded-lg text-xs font-bold">Modifier</button><button onclick="delProd(${p.id})" class="bg-red-100 text-red-700 px-3 py-1.5 rounded-lg text-xs font-bold">X</button></div>`).join("")}
function addProduct(){const n=document.getElementById("p_name").value;if(!n)return toast("Nom requis!");
const file=document.getElementById("p_file").files[0];
const done=(imgUrl)=>{const editId=document.getElementById("p_editId").value;
const obj={n,c:document.getElementById("p_cat").value,p:+document.getElementById("p_price").value||0,i:imgUrl||document.getElementById("p_img").value||IMG.tajine,b:document.getElementById("p_badge").value,d:document.getElementById("p_desc").value||"Délicieux plat maison"};
if(editId){Object.assign(DB.products.find(x=>x.id==editId),obj);document.getElementById("p_editId").value=""}else{obj.id=Date.now();DB.products.unshift(obj)}
save();renderProducts();renderAdminProds();toast("✅ Produit enregistré");document.getElementById("p_name").value="";document.getElementById("p_price").value=""};
if(file){const r=new FileReader();r.onload=e=>done(e.target.result);r.readAsDataURL(file)}else done(null)}
function editProd(id){const p=DB.products.find(x=>x.id===id);document.getElementById("p_name").value=p.n;document.getElementById("p_cat").value=p.c;document.getElementById("p_price").value=p.p;document.getElementById("p_img").value=p.i;document.getElementById("p_badge").value=p.b||"";document.getElementById("p_desc").value=p.d;document.getElementById("p_editId").value=id;window.scrollTo(0,0);toast("✏️ Modifiez puis cliquez Ajouter")}
function delProd(id){if(confirm("Supprimer?")){DB.products=DB.products.filter(x=>x.id!==id);save();renderProducts();renderAdminProds()}}
function addVideo(){const t=document.getElementById("v_title").value,u=document.getElementById("v_url").value;if(!t||!u)return toast("Remplissez tout");DB.videos.push({t,u});save();renderVideos();renderAdminVids()}
function renderAdminVids(){document.getElementById("adminVidList").innerHTML=DB.videos.map((v,i)=>`<div class="flex justify-between border rounded-xl p-3 text-sm"><b>${v.t}</b><button onclick="DB.videos.splice(${i},1);save();renderVideos();renderAdminVids()" class="text-red-600 font-bold">Supprimer</button></div>`).join("")}
function renderOrders(){document.getElementById("adminOrderList").innerHTML=orders.length?orders.map(o=>`<div class="border rounded-xl p-3 text-sm bg-gray-50"><b>${o.name}</b> (${o.phone}) • ${o.date}<br>${o.type} • <b class="text-rouge">${o.total} DH</b><pre class="whitespace-pre-wrap mt-1 text-xs">${o.items}</pre></div>`).join(""):"<p class='text-gray-400'>Aucune commande pour le moment.</p>"}
function exportData(){const a=document.createElement("a");a.href="data:text/json;charset=utf-8,"+encodeURIComponent(JSON.stringify(DB));a.download="farah-backup.json";a.click()}
function resetData(){if(confirm("Réinitialiser tout?")){localStorage.removeItem("farah_v1");location.reload()}}
renderAll();
</script>
</body>
</html>
