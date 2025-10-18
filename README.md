# Shilpotoru
শিল্পতরু – A premium black-themed website showcasing Bangladeshi Nokshi Katha art.
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>শিল্পতরু</title>
<style>
    /* Reset */
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: 'Arial', sans-serif; background-color: #0a0a0a; color: #fff; scroll-behavior: smooth; }

    /* Nokshi katha background */
    body::before {
        content: '';
        position: fixed;
        top:0; left:0; width:100%; height:100%;
        background: url('https://i.ibb.co/pxR6D2H/nokshi-katha-pattern.png') repeat;
        opacity: 0.05;
        z-index: -1;
    }

    /* Header */
    header { position: fixed; width:100%; top:0; left:0; background: rgba(0,0,0,0.8); display:flex; justify-content:space-between; align-items:center; padding:20px 50px; z-index: 1000; }
    header h1 { font-family: 'Georgia', serif; font-size:28px; letter-spacing:2px; }
    nav a { color:#fff; margin-left:20px; text-decoration:none; font-weight:bold; transition:0.3s; }
    nav a:hover { color:#f0a500; }

    /* Hero Section */
    .hero { height: 100vh; display:flex; justify-content:center; align-items:center; text-align:center; background: rgba(0,0,0,0.7); }
    .hero h2 { font-size: 48px; font-weight:bold; color:#fff; text-shadow: 2px 2px 10px #000; }

    /* Sections */
    section { padding:100px 50px; }
    section h2 { font-size:36px; margin-bottom:20px; border-bottom:2px solid #f0a500; display:inline-block; padding-bottom:5px; }

    /* Gallery */
    .gallery { display:grid; grid-template-columns:repeat(auto-fit, minmax(250px,1fr)); gap:20px; }
    .gallery img { width:100%; border-radius:10px; transition:0.3s; cursor:pointer; }
    .gallery img:hover { transform:scale(1.05); box-shadow:0 0 20px #f0a500; }

    /* About */
    #about p { font-size:18px; line-height:1.6; max-width:800px; }

    /* Contact */
    #contact p, #contact a { font-size:18px; color:#fff; text-decoration:none; }

    /* Footer */
    footer { text-align:center; padding:20px; border-top:1px solid #333; font-size:14px; }

    /* Responsive */
    @media(max-width:768px) {
        header { flex-direction: column; }
        nav a { margin:10px 0; }
        .hero h2 { font-size:32px; }
        section { padding:60px 20px; }
    }
</style>
</head>
<body>

<header>
    <h1>শিল্পতরু</h1>
    <nav>
        <a href="#home">হোম</a>
        <a href="#gallery">গ্যালারি</a>
        <a href="#about">আমাদের সম্পর্কে</a>
        <a href="#contact">যোগাযোগ</a>
    </nav>
</header>

<section class="hero" id="home">
    <h2>বাংলার ঐতিহ্য, শিল্পের ছোঁয়ায়</h2>
</section>

<section class="gallery" id="gallery">
    <img src="https://via.placeholder.com/400x300" alt="Artwork1">
    <img src="https://via.placeholder.com/400x300" alt="Artwork2">
    <img src="https://via.placeholder.com/400x300" alt="Artwork3">
    <img src="https://via.placeholder.com/400x300" alt="Artwork4">
</section>

<section id="about">
    <h2>আমাদের সম্পর্কে</h2>
    <p>শিল্পতরু হল এক অনন্য প্ল্যাটফর্ম যেখানে আমরা বাংলার ঐতিহ্যবাহী নকশিকাঠা শিল্পকে প্রিমিয়াম মানের ডিজিটাল মাধ্যমে তুলে ধরি। আমাদের লক্ষ্য হচ্ছে শিল্পকে আধুনিক ডিজিটাল জগতে পৌঁছে দেয়া, যাতে এটি প্রতিটি মানুষের জীবনে আলোকবর্তিকা হিসেবে কাজ করে।</p>
</section>

<section id="contact">
    <h2>যোগাযোগ</h2>
    <p>Email: <a href="mailto:info@shilpotoru.com">info@shilpotoru.com</a></p>
    <p>Phone: +880 123 456 789</p>
</section>

<footer>
    &copy; 2025 শিল্পতরু. সর্বস্বত্ব সংরক্ষিত।
</footer>

</body>
</html>
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>শিল্পতরু</title>
<style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: 'Arial', sans-serif; background-color:#0a0a0a; color:#fff; scroll-behavior:smooth; }
    
    /* Background */
    body::before {
        content:'';
        position:fixed; top:0; left:0; width:100%; height:100%;
        background:url('https://i.ibb.co/pxR6D2H/nokshi-katha-pattern.png') repeat;
        opacity:0.05; z-index:-1;
    }

    /* Header */
    header { position:fixed; width:100%; top:0; left:0; background:rgba(0,0,0,0.85); display:flex; justify-content:space-between; align-items:center; padding:15px 50px; z-index:1000; }
    header h1 { font-family:'Georgia', serif; font-size:28px; letter-spacing:2px; }
    nav a { color:#fff; margin-left:20px; text-decoration:none; font-weight:bold; transition:0.3s; }
    nav a:hover { color:#f0a500; }

    /* Hero Slider */
    .hero { position:relative; height:100vh; display:flex; justify-content:center; align-items:center; text-align:center; overflow:hidden; }
    .slide { position:absolute; width:100%; height:100%; background-size:cover; background-position:center; opacity:0; transition:1s; }
    .slide.active { opacity:1; }
    .hero h2 { position:relative; z-index:2; font-size:48px; color:#fff; text-shadow:2px 2px 10px #000; }

    /* Sections */
    section { padding:100px 50px; }
    section h2 { font-size:36px; margin-bottom:20px; border-bottom:2px solid #f0a500; display:inline-block; padding-bottom:5px; }
    
    /* Gallery */
    .gallery { display:grid; grid-template-columns:repeat(auto-fit, minmax(250px,1fr)); gap:20px; }
    .gallery img { width:100%; border-radius:10px; cursor:pointer; transition:0.3s; }
    .gallery img:hover { transform:scale(1.05); box-shadow:0 0 20px #f0a500; }

    /* Lightbox */
    #lightbox { position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.9); display:none; justify-content:center; align-items:center; z-index:10000; }
    #lightbox img { max-width:90%; max-height:90%; border-radius:10px; }

    /* Contact */
    #contact p, #contact a { font-size:18px; color:#fff; text-decoration:none; }

    /* Footer */
    footer { text-align:center; padding:20px; border-top:1px solid #333; font-size:14px; }

    /* Responsive */
    @media(max-width:768px) {
        header { flex-direction:column; }
        nav a { margin:10px 0; }
        .hero h2 { font-size:32px; }
        section { padding:60px 20px; }
    }
</style>
</head>
<body>

<header>
    <h1>শিল্পতরু</h1>
    <nav>
        <a href="#home">হোম</a>
        <a href="#gallery">গ্যালারি</a>
        <a href="#about">আমাদের সম্পর্কে</a>
        <a href="#contact">যোগাযোগ</a>
    </nav>
</header>

<section class="hero" id="home">
    <div class="slide active" style="background-image:url('https://via.placeholder.com/1600x900/111111/ffffff?text=Slide+1');"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/1600x900/222222/ffffff?text=Slide+2');"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/1600x900/333333/ffffff?text=Slide+3');"></div>
    <h2>বাংলার ঐতিহ্য, শিল্পের ছোঁয়ায়</h2>
</section>

<section class="gallery" id="gallery">
    <img src="https://via.placeholder.com/400x300" alt="Artwork1">
    <img src="https://via.placeholder.com/400x300" alt="Artwork2">
    <img src="https://via.placeholder.com/400x300" alt="Artwork3">
    <img src="https://via.placeholder.com/400x300" alt="Artwork4">
</section>

<!-- Lightbox -->
<div id="lightbox"><img src="" alt="Artwork"></div>

<section id="about">
    <h2>আমাদের সম্পর্কে</h2>
    <p>শিল্পতরু হল এক অনন্য প্ল্যাটফর্ম যেখানে আমরা বাংলার ঐতিহ্যবাহী নকশিকাঠা শিল্পকে প্রিমিয়াম মানের ডিজিটাল মাধ্যমে তুলে ধরি। আমাদের লক্ষ্য হচ্ছে শিল্পকে আধুনিক ডিজিটাল জগতে পৌঁছে দেয়া, যাতে এটি প্রতিটি মানুষের জীবনে আলোকবর্তিকা হিসেবে কাজ করে।</p>
</section>

<section id="contact">
    <h2>যোগাযোগ</h2>
    <p>Email: <a href="mailto:info@shilpotoru.com">info@shilpotoru.com</a></p>
    <p>Phone: +880 1333370627</p>
</section>

<footer>
    &copy; 2025 শিল্পতরু. সর্বস্বত্ব সংরক্ষিত।
</footer>

<script>
    // Hero Slider
    let slides = document.querySelectorAll('.slide');
    let current = 0;
    setInterval(()=> {
        slides[current].classList.remove('active');
        current = (current+1)%slides.length;
        slides[current].classList.add('active');
    },5000);

    // Lightbox
    const galleryImages = document.querySelectorAll('.gallery img');
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = lightbox.querySelector('img');
    galleryImages.forEach(img=>{
        img.addEventListener('click', ()=> {
            lightboxImg.src = img.src;
            lightbox.style.display='flex';
        });
    });
    lightbox.addEventListener('click', ()=>{ lightbox.style.display='none'; });
</script>

</body>
</html>
