<!DOCTYPE html>
<html lang="zh-CN"> <!-- Default language is Chinese -->
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>广州普丹娇皮具有限公司 / Guangzhou Pudanjiao Leather Co., Ltd. / บริษัท...</title>
    <meta name="description" content="广州普丹娇皮具有限公司 (Guangzhou Pudanjiao Leather Co., Ltd. / บริษัท...) - High-quality fashion leather bags manufacturer offering ODM and Brand Incubation services.">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&family=Noto+Sans+SC:wght@300;400;500;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">

    <!-- Font Awesome (for icons) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />

    <!-- Embedded CSS -->
    <style>
        /* --- Base Variables --- */
        :root {
            --primary-color: #8B4513; /* Saddle Brown */
            --secondary-color: #D2B48C; /* Tan */
            --accent-color: #A0522D;  /* Sienna */
            --text-color: #333333;    /* Dark Gray */
            --light-text-color: #ffffff; /* White */
            --bg-color: #FAF8F5;      /* Very Light Beige */
            --light-bg-color: #F5F5F5; /* Lighter Gray/Beige */
            --border-color: #E0E0E0;  /* Light Gray */
            --font-family-th: 'Kanit', sans-serif;
            --font-family-zh: 'Noto Sans SC', sans-serif; /* Chinese Font */
            --font-family-en: 'Roboto', sans-serif;      /* English Font */
        }

        /* --- Base Styles --- */
        * { box-sizing: border-box; margin: 0; padding: 0; }
        html { scroll-behavior: smooth; }
        body {
            font-family: var(--font-family-zh); /* Default font */
            line-height: 1.7; color: var(--text-color); background-color: var(--bg-color); font-size: 16px;
        }
        html[lang="th"] body { font-family: var(--font-family-th); }
        html[lang="en"] body { font-family: var(--font-family-en); }

        /* Specific font overrides (optional, handled by body switch) */
        .lang-th { font-family: var(--font-family-th); }
        .lang-en { font-family: var(--font-family-en); }
        .lang-zh { font-family: var(--font-family-zh); } /* Ensure ZH font */

        .container { max-width: 1100px; margin: 0 auto; padding: 0 20px; }
        .section { padding: 60px 0; }
        .bg-light { background-color: var(--light-bg-color); }
        h1, h2, h3 { margin-bottom: 20px; font-weight: 600; color: var(--primary-color); }
        h1 { font-size: 2.8rem; line-height: 1.2; }
        h2 { font-size: 2.2rem; text-align: center; margin-bottom: 40px; position: relative; }
        h2::after { content: ''; display: block; width: 60px; height: 3px; background-color: var(--accent-color); margin: 10px auto 0; }
        h3 { font-size: 1.4rem; color: var(--primary-color); font-weight: 500; margin-bottom: 10px; }
        p { margin-bottom: 15px; color: #555; }
        a { color: var(--accent-color); text-decoration: none; transition: color 0.3s ease; }
        a:hover { color: var(--primary-color); }
        img { max-width: 100%; height: auto; display: block; }

        /* --- Language Content Hiding --- */
        .lang-th, .lang-en { display: none; } /* Hide non-default languages initially */
        /* Ensure spans display correctly */
        .lang-content { display: inline; }
        /* Make sure parents allow inline content to flow naturally */
        h1, h2, h3, p, .feature-item, .service-content, .contact-item, .cta-button, .footer p, .partner-item {
             line-height: inherit; /* Allow content to wrap and flow */
        }

        /* --- NEW Language Dropdown Styles --- */
        .lang-switcher-container {
            position: absolute;
            top: 15px;
            right: 20px;
            z-index: 100; /* Ensure it's above other content */
        }

        #lang-toggle-btn {
            background-color: rgba(255, 255, 255, 0.9);
            color: var(--primary-color);
            border: 1px solid var(--border-color);
            padding: 8px 12px; /* Adjusted padding */
            border-radius: 5px;
            cursor: pointer;
            font-family: var(--font-family-en); /* Consistent font for switcher button */
            font-size: 0.9rem; /* Slightly smaller base size */
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 6px; /* Space between icon and arrow */
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            min-width: 50px; /* Adjust min width */
            justify-content: center;
        }
         #lang-toggle-btn .btn-lang-text {
             display: none; /* Hide text on small screens initially */
         }
         #lang-toggle-btn i.fa-globe {
             font-size: 1.2em; /* Make globe slightly bigger */
             margin-right: 4px; /* Space after globe */
         }
         #lang-toggle-btn i.fa-chevron-down {
             font-size: 0.8em;
             transition: transform 0.3s ease;
             margin-left: 4px; /* Space before arrow */
         }
         #lang-toggle-btn.open i.fa-chevron-down {
             transform: rotate(180deg);
         }

        .lang-dropdown {
            display: none; /* Hidden by default */
            position: absolute;
            top: calc(100% + 5px); /* Position below the button with gap */
            right: 0;
            background-color: white;
            min-width: 120px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            border-radius: 5px;
            overflow: hidden; /* Clip rounded corners */
            border: 1px solid var(--border-color);
        }

        .lang-dropdown.show-dropdown {
            display: block; /* Show when active */
        }

        .lang-dropdown button {
            color: var(--text-color);
            padding: 10px 15px;
            text-decoration: none;
            display: block;
            width: 100%;
            text-align: left;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 0.95rem;
            transition: background-color 0.2s ease;
        }
        /* Apply correct font for each language button */
        .lang-dropdown button[data-lang="th"] { font-family: var(--font-family-th); }
        .lang-dropdown button[data-lang="zh"] { font-family: var(--font-family-zh); }
        .lang-dropdown button[data-lang="en"] { font-family: var(--font-family-en); }

        .lang-dropdown button:hover {
            background-color: var(--light-bg-color);
        }
        /* Style for the currently active language in the dropdown */
        .lang-dropdown button.selected-lang {
            font-weight: bold;
            background-color: var(--accent-color);
            color: var(--light-text-color);
            cursor: default;
        }
         .lang-dropdown button.selected-lang:hover {
             background-color: var(--accent-color); /* Prevent hover style */
         }


        /* --- Hero Section --- */
        .hero-section { background: url('placeholder-hero.jpg') no-repeat center center/cover; /* REPLACE */ height: 70vh; min-height: 400px; color: var(--light-text-color); display: flex; justify-content: center; align-items: center; text-align: center; position: relative; }
        .hero-overlay { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.5); }
        .hero-content { position: relative; z-index: 1; padding: 0 15px; } /* Add padding for smaller screens */
        .hero-content h1 { color: var(--light-text-color); margin-bottom: 15px; }
        .hero-content .subtitle { font-size: 1.4rem; margin-bottom: 25px; font-weight: 400; color: var(--light-text-color); }
        .hero-content p { font-size: 1.1rem; margin-bottom: 30px; color: #eee; }
        .cta-button { display: inline-block; background-color: var(--accent-color); color: var(--light-text-color); padding: 12px 30px; border-radius: 25px; font-size: 1.1rem; font-weight: 500; text-transform: uppercase; transition: background-color 0.3s ease, transform 0.2s ease; }
        /* Button text language visibility */
        html[lang="th"] .cta-button .lang-th, html[lang="zh-CN"] .cta-button .lang-zh, html[lang="en"] .cta-button .lang-en { display: inline; font-family: inherit;}
        html[lang="th"] .cta-button .lang-zh, html[lang="th"] .cta-button .lang-en { display: none; }
        html[lang="zh-CN"] .cta-button .lang-th, html[lang="zh-CN"] .cta-button .lang-en { display: none; }
        html[lang="en"] .cta-button .lang-th, html[lang="en"] .cta-button .lang-zh { display: none; }
        .cta-button:hover { background-color: var(--primary-color); color: var(--light-text-color); transform: translateY(-2px); }

        /* --- About Section --- */
        #about { text-align: center; } #about p { max-width: 800px; margin-left: auto; margin-right: auto; }
        /* --- Why Choose Us Section --- */
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; text-align: center; }
        .feature-item { background-color: #fff; padding: 30px 20px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08); transition: transform 0.3s ease, box-shadow 0.3s ease; display: flex; flex-direction: column; align-items: center; }
        .feature-item:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12); }
        .feature-item i { color: var(--accent-color); margin-bottom: 15px; font-size: 1.8em; }
        .feature-item h3 { font-size: 1.3rem; } .feature-item p { font-size: 0.95rem; }
        /* --- Services Section --- */
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .service-card { background-color: #fff; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08); transition: transform 0.3s ease, box-shadow 0.3s ease; display: flex; flex-direction: column; }
        .service-card:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12); }
        .service-image { width: 100%; height: 200px; object-fit: cover; }
        .service-content { padding: 25px; text-align: center; flex-grow: 1; }
        .service-content i { color: var(--accent-color); margin-bottom: 15px; font-size: 1.8em; }
        .service-content h3 { margin-top: 0; font-size: 1.3rem; } .service-content p { font-size: 0.95rem; }
        /* --- Partners Section --- */
        #partners { text-align: center; } #partners > .container > p { max-width: 700px; margin-left: auto; margin-right: auto; }
        .partner-logos { display: flex; justify-content: center; align-items: center; flex-wrap: wrap; gap: 15px; /* Reduced gap slightly */ margin-top: 30px; margin-bottom: 30px; }
        .partner-logos .partner-item { font-size: 1.0rem; /* Adjusted size */ color: #666; font-weight: 500; padding: 8px 15px; /* Adjusted padding */ border: 1px solid var(--border-color); border-radius: 4px; background-color: #fff; box-shadow: 0 1px 3px rgba(0,0,0,0.05); }
        /* --- Contact Section --- */
        #contact { text-align: center; } #contact > .container > p { max-width: 700px; margin-left: auto; margin-right: auto; margin-bottom: 40px; }
        .contact-info { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; text-align: center; margin-bottom: 40px; }
        .contact-item i { color: var(--accent-color); margin-bottom: 10px; font-size: 1.8em; }
        .contact-item h3 { margin-bottom: 5px; font-size: 1.3rem; }
        .contact-item p { margin-bottom: 0; font-size: 1rem; line-height: 1.5; } .contact-item a { word-break: break-word; } /* Better word breaking */
        .contact-image { max-width: 600px; margin: 30px auto 0; border-radius: 8px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        /* --- Footer --- */
        .footer { background-color: var(--primary-color); color: var(--light-text-color); text-align: center; padding: 25px 0; margin-top: 60px; }
        .footer p { margin-bottom: 0; color: #eee; font-size: 0.95rem; padding: 0 10px;}

        /* --- Responsive Design Adjustments --- */
        @media (max-width: 768px) {
            h1 { font-size: 2.2rem; } h2 { font-size: 1.8rem; } .hero-section { height: auto; min-height: 55vh; padding: 80px 0 40px; } /* Adjust hero height/padding */
            .features-grid, .services-grid, .contact-info { grid-template-columns: 1fr; }
            .partner-logos { gap: 10px; } .partner-logos .partner-item { font-size: 0.95rem; padding: 6px 12px; }
            .contact-image { max-width: 90%; }
            .lang-switcher-container { top: 10px; right: 10px; } /* Adjust position */
            #lang-toggle-btn { padding: 6px 10px; font-size: 0.9rem; } /* Smaller button padding */
             .lang-dropdown button { padding: 8px 12px; font-size: 0.9rem; }
        }
        @media (max-width: 480px) {
            h1 { font-size: 1.8rem; } h2 { font-size: 1.5rem; } .hero-content .subtitle { font-size: 1.1rem; }
            .cta-button { padding: 10px 20px; font-size: 1rem; } .section { padding: 40px 0; }
            .feature-item h3, .service-content h3, .contact-item h3 { font-size: 1.2rem; }
            .partner-logos .partner-item { font-size: 0.9rem; }
            #lang-toggle-btn { min-width: 45px; } /* Allow button to be smaller */
            #lang-toggle-btn .btn-lang-text { display: none; } /* Hide text on very small screens */
            #lang-toggle-btn i.fa-globe { margin-right: 0; } /* Remove margin if text hidden */
            .contact-item p { font-size: 0.95rem; } /* Slightly smaller contact text */
        }
        /* Show language text on toggle button for larger screens */
         @media (min-width: 481px) {
             #lang-toggle-btn .btn-lang-text { display: inline; }
         }

    </style>
</head>
<body>

    <!-- Language Switcher Dropdown -->
    <div class="lang-switcher-container">
        <button id="lang-toggle-btn">
            <i class="fas fa-globe"></i>
            <span class="btn-lang-text">中文</span> <!-- Default Text -->
            <i class="fas fa-chevron-down"></i>
        </button>
        <div class="lang-dropdown">
            <button data-lang="th">ไทย</button>
            <button data-lang="zh" class="selected-lang">中文</button> <!-- Mark Chinese as selected -->
            <button data-lang="en">English</button>
        </div>
    </div>

    <!-- Hero Section -->
    <header class="hero-section" id="home">
        <div class="hero-overlay"></div>
        <div class="container hero-content">
            <h1>
                <span class="lang-content lang-th">บริษัท Guangzhou Pudanjiao Leather Co., Ltd.</span>
                <span class="lang-content lang-zh">广州普丹娇皮具有限公司</span>
                <span class="lang-content lang-en">Guangzhou Pudanjiao Leather Co., Ltd.</span>
            </h1>
            <p class="subtitle">
                <span class="lang-content lang-th">พันธมิตรผู้ผลิตกระเป๋าหนังแฟชั่น ที่มุ่งมั่นในคุณภาพและการออกแบบที่สร้างสรรค์</span>
                <span class="lang-content lang-zh">引领时尚皮具潮流</span>
                <span class="lang-content lang-en">Leading the Trend in Fashion Leather Goods</span>
            </p>
            <p>
                <span class="lang-content lang-th">ก่อตั้งในปี 2018 โดยทีมงานผู้มีประสบการณ์ในอุตสาหกรรมเครื่องหนังกว่า 10 ปี</span>
                <span class="lang-content lang-zh">凭借十年行业深耕经验，已成为东南亚地区领先的皮具供应商</span>
                <span class="lang-content lang-en">Established in 2018 by a team with over 10 years of experience in the leather industry.</span>
            </p>
            <a href="#contact" class="cta-button">
                <span class="lang-content lang-th">ติดต่อสอบถาม</span>
                <span class="lang-content lang-zh">联系我们</span>
                <span class="lang-content lang-en">Contact Us</span>
            </a>
        </div>
    </header>

    <main>
        <!-- About Section -->
        <section id="about" class="container section">
            <h2>
                <span class="lang-content lang-th">เกี่ยวกับเรา</span>
                <span class="lang-content lang-zh">关于我们</span>
                <span class="lang-content lang-en">About Us</span>
            </h2>
            <p>
                <span class="lang-content lang-th">เราคือผู้เชี่ยวชาญด้านการออกแบบ วิจัย และผลิตกระเป๋าสตรีและกระเป๋าเป้คุณภาพสูง ยึดมั่นในหลักการ "การออกแบบที่สร้างสรรค์และคุณภาพเป็นอันดับหนึ่ง" เราพร้อมเป็นส่วนหนึ่งในความสำเร็จของแบรนด์คุณ ด้วยความเข้าใจในตลาดเอเชียตะวันออกเฉียงใต้และความต้องการของลูกค้าอย่างแท้จริง</span>
                <span class="lang-content lang-zh">广州普丹娇皮具有限公司，自2018年成立以来，始终专注于时尚皮具的设计、研发与制造。我们秉承“创新设计，品质至上”的核心理念，凭借十年行业深耕经验，已成为东南亚地区领先的皮具供应商。我们致力于为全球客户提供卓越的产品与服务，共同缔造品质之美。</span>
                <span class="lang-content lang-en">Guangzhou Pudanjiao Leather Co., Ltd., established in 2018, specializes in the design, research, development, and manufacturing of fashion leather goods. Adhering to the core concept of "Innovative Design, Quality First," and leveraging over a decade of industry experience, we have become a leading leather goods supplier in Southeast Asia. We are committed to providing exceptional products and services to global clients, crafting quality together.</span>
            </p>
        </section>

        <!-- Why Choose Us Section -->
        <section id="why-us" class="section bg-light">
            <div class="container">
                <h2>
                    <span class="lang-content lang-th">ทำไมต้องเลือกเรา?</span>
                    <span class="lang-content lang-zh">核心优势</span>
                    <span class="lang-content lang-en">Core Advantages</span>
                </h2>
                <div class="features-grid">
                    <!-- Feature 1: Quality -->
                    <div class="feature-item">
                        <i class="fas fa-gem"></i>
                        <h3>
                            <span class="lang-content lang-th">คุณภาพและวัสดุพรีเมียม</span>
                            <span class="lang-content lang-zh">精湛工艺与严选材料</span>
                            <span class="lang-content lang-en">Exquisite Craftsmanship & Selected Materials</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">คัดสรรวัสดุชั้นเยี่ยม (PVC, PU, ไฟเบอร์สังเคราะห์, ไนลอน, Oxford) ผ่านมาตรฐานสากล REACH และ ROHS ควบคุมการผลิตแม่นยำ คลาดเคลื่อนไม่เกิน 0.5 มม.</span>
                            <span class="lang-content lang-zh">从原材料严苛筛选到生产流程精益求精，主材涵盖PVC、PU、超纤、尼龙布、牛津布等环保耐用材质，通过国际标准检测，误差控制在≤0.5mm。</span>
                            <span class="lang-content lang-en">From rigorous raw material selection to lean production processes, using eco-friendly materials like PVC, PU, microfiber, nylon, Oxford cloth. Meeting international standards (REACH, ROHS) with precision control (≤0.5mm tolerance).</span>
                        </p>
                    </div>
                    <!-- Feature 2: Design -->
                    <div class="feature-item">
                        <i class="fas fa-lightbulb"></i>
                        <h3>
                             <span class="lang-content lang-th">ดีไซน์ทันสมัย นำเทรนด์</span>
                             <span class="lang-content lang-zh">时尚基因与场景化产品</span>
                             <span class="lang-content lang-en">Fashion DNA & Scenario-Based Products</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">ทีมดีไซเนอร์รุ่นใหม่ ร่วมมือกับนักออกแบบสร้างสรรค์ อัปเดตคอลเลกชันใหม่ทุกไตรมาส ตามเทรนด์แฟชั่นระดับโลก (มิลาน, ปารีส) หลากหลายสไตล์ตอบโจทย์ทุกไลฟ์สไตล์</span>
                            <span class="lang-content lang-zh">与新锐设计师紧密合作，每季度推出引领潮流新款。紧跟国际时尚趋势，涵盖通勤、休闲、轻奢等多种风格，满足多元需求。</span>
                            <span class="lang-content lang-en">Collaborating with emerging designers, launching trend-setting new collections quarterly. Following global fashion trends (Milan, Paris), covering styles from commute and casual to light luxury.</span>
                        </p>
                    </div>
                    <!-- Feature 3: Production -->
                    <div class="feature-item">
                        <i class="fas fa-industry"></i>
                        <h3>
                            <span class="lang-content lang-th">กำลังการผลิตสูง</span>
                            <span class="lang-content lang-zh">标准化生产，精益求精</span>
                            <span class="lang-content lang-en">Standardized & Refined Production</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">โรงงานมาตรฐาน กำลังการผลิตมากกว่า 500,000 ชิ้นต่อปี รองรับการสั่งผลิตจำนวนมาก พร้อมส่งมอบตรงเวลา</span>
                            <span class="lang-content lang-zh">采用标准化生产管理，严格把控每一环节。年产能超过50万件，确保满足客户的大批量订单需求。</span>
                            <span class="lang-content lang-en">Utilizing standardized production management, strictly controlling every step. Annual capacity exceeds 500,000 pieces, ensuring fulfillment of large-volume orders on time.</span>
                        </p>
                    </div>
                     <!-- Feature 4: Sustainability -->
                    <div class="feature-item">
                        <i class="fas fa-leaf"></i>
                        <h3>
                            <span class="lang-content lang-th">ใส่ใจความยั่งยืน</span>
                             <span class="lang-content lang-zh">可持续发展承诺</span>
                             <span class="lang-content lang-en">Sustainability Commitment</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">มุ่งมั่นสู่การผลิตที่ยั่งยืน ใช้กาวสูตรน้ำ ลดสารเคมีอันตราย และกระบวนการฟอกหนังแบบไม่มีโครเมียม</span>
                            <span class="lang-content lang-zh">采用环保水性胶黏剂，替代传统化学胶黏剂。采用无铬鞣制工艺，避免有害铬。积极探索可持续材料。</span>
                            <span class="lang-content lang-en">Using eco-friendly water-based adhesives instead of traditional chemical ones. Employing chrome-free tanning processes. Actively exploring sustainable materials.</span>
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="container section">
             <h2>
                 <span class="lang-content lang-th">บริการของเรา</span>
                 <span class="lang-content lang-zh">我们的服务</span>
                 <span class="lang-content lang-en">Our Services</span>
            </h2>
             <div class="services-grid">
                 <!-- Service 1: ODM -->
                 <div class="service-card">
                     <img src="placeholder-services-odm.jpg" alt="ODM Service / 定制服务" class="service-image"> <!-- REPLACE -->
                     <div class="service-content">
                        <i class="fas fa-cogs"></i>
                        <h3>
                            <span class="lang-content lang-th">ODM (Original Design Manufacturing)</span>
                            <span class="lang-content lang-zh">ODM 定制服务</span>
                            <span class="lang-content lang-en">ODM (Original Design Manufacturing)</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">บริการออกแบบ สร้างตัวอย่าง และผลิตครบวงจร รองรับการสั่งผลิตขั้นต่ำ 100 ชิ้น พร้อมจัดส่งรวดเร็วภายใน 15-25 วัน</span>
                            <span class="lang-content lang-zh">提供从设计、打样到量产的一体化ODM定制服务。支持Logo、配件等专属定制。承接中小型订单(100件起)，15-25天极速交付。</span>
                            <span class="lang-content lang-en">Providing integrated ODM services from design, sampling to mass production. Supporting customization (Logo, accessories). Accepting small/medium orders (from 100 pcs) with fast 15-25 day delivery.</span>
                        </p>
                     </div>
                 </div>
                 <!-- Service 2: Brand Incubation -->
                 <div class="service-card">
                      <img src="placeholder-services-incubation.jpg" alt="Brand Incubation / 品牌孵化" class="service-image"> <!-- REPLACE -->
                      <div class="service-content">
                        <i class="fas fa-rocket"></i>
                        <h3>
                            <span class="lang-content lang-th">Brand Incubation (สนับสนุนแบรนด์ใหม่)</span>
                            <span class="lang-content lang-zh">品牌孵化服务</span>
                            <span class="lang-content lang-en">Brand Incubation</span>
                        </h3>
                        <p>
                            <span class="lang-content lang-th">ช่วยพัฒนาแบรนด์ใหม่ตั้งแต่เริ่มต้น ให้คำปรึกษาด้านวัตถุดิบ วางแผนสายผลิตภัณฑ์ และกลยุทธ์การผลิต</span>
                            <span class="lang-content lang-zh">为新兴品牌提供全方位的供应链整合与产品线规划支持，助力其快速成长。提供专业的指导和支持。</span>
                            <span class="lang-content lang-en">Offering comprehensive support for emerging brands, including supply chain integration and product line planning, fostering rapid growth with professional guidance.</span>
                        </p>
                      </div>
                 </div>
                 <!-- Service 3: Consultation -->
                 <div class="service-card">
                     <img src="placeholder-services-consult.jpg" alt="Consultation / 全方位支持" class="service-image"> <!-- REPLACE -->
                     <div class="service-content">
                        <i class="fas fa-handshake"></i>
                        <h3>
                            <span class="lang-content lang-th">ให้คำปรึกษาครบวงจร</span>
                            <span class="lang-content lang-zh">“设计+制造+服务”</span>
                            <span class="lang-content lang-en">"Design + Manufacturing + Service"</span>
                        </h3>
                        <p>
                             <span class="lang-content lang-th">ให้คำแนะนำด้านห่วงโซ่อุปทาน (Supply Chain) ภายใต้แนวทาง "การออกแบบ + การผลิต + บริการ" เพื่อประสิทธิภาพสูงสุด</span>
                             <span class="lang-content lang-zh">深化“设计+制造+服务”三位一体模式，提供供应链建议，致力于成为时尚皮具领域的标杆企业。</span>
                             <span class="lang-content lang-en">Deepening the "Design + Manufacturing + Service" integrated model, providing supply chain advice, aiming to be a benchmark in the fashion leather goods industry.</span>
                        </p>
                      </div>
                 </div>
             </div>
        </section>

        <!-- Partners Section -->
        <section id="partners" class="section bg-light">
            <div class="container">
                <h2>
                    <span class="lang-content lang-th">พันธมิตรทางธุรกิจที่ไว้วางใจ</span>
                    <span class="lang-content lang-zh">合作品牌</span>
                    <span class="lang-content lang-en">Trusted Partners</span>
                </h2>
                <p>
                    <span class="lang-content lang-th">เราภูมิใจที่ได้ร่วมงานและเป็นส่วนหนึ่งของความสำเร็จให้กับแบรนด์ชั้นนำมากมาย อาทิ:</span>
                    <span class="lang-content lang-zh">我们已与多个知名品牌建立了长期稳定的合作关系，产品质量和服务水平赢得了客户的广泛认可：</span>
                    <span class="lang-content lang-en">We have established long-term stable partnerships with several well-known brands, earning wide recognition for product quality and service:</span>
                </p>
                <div class="partner-logos">
                     <div class="partner-item">
                         <span class="lang-content lang-th">Polarboll (กระเป๋าสตรีแนวแฟชั่น)</span>
                         <span class="lang-content lang-zh">Polarboll (潮流女包)</span>
                         <span class="lang-content lang-en">Polarboll (Fashion Women's Bags)</span>
                     </div>
                     <div class="partner-item">
                         <span class="lang-content lang-th">Pomelo (แฟชั่นรวดเร็ว)</span>
                         <span class="lang-content lang-zh">Pomelo (快时尚)</span>
                         <span class="lang-content lang-en">Pomelo (Fast Fashion)</span>
                     </div>
                     <div class="partner-item">
                         <span class="lang-content lang-th">Muva (กระเป๋าหรูระดับกลาง)</span>
                         <span class="lang-content lang-zh">Muva (轻奢女包)</span>
                         <span class="lang-content lang-en">Muva (Light Luxury Women's Bags)</span>
                     </div>
                </div>
                 <p>
                    <span class="lang-content lang-th">ความสำเร็จของพันธมิตร คือเครื่องยืนยันคุณภาพและบริการที่เชื่อถือได้ของเรา</span>
                     <span class="lang-content lang-zh"></span> <!-- Keep empty or add Chinese conclusion -->
                     <span class="lang-content lang-en">Our partners' success affirms our reliable quality and service.</span>
                 </p>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="container section">
            <h2>
                <span class="lang-content lang-th">ติดต่อเราเพื่อเริ่มต้นโปรเจกต์ของคุณ</span>
                <span class="lang-content lang-zh">联系我们，共创美好未来</span>
                <span class="lang-content lang-en">Contact Us to Start Your Project</span>
            </h2>
            <p>
                <span class="lang-content lang-th">ทีมงานของเราพร้อมให้คำปรึกษาและบริการ เพื่อสร้างสรรค์ผลิตภัณฑ์เครื่องหนังที่ตอบโจทย์และสร้างความแตกต่างให้กับแบรนด์ของคุณ</span>
                 <span class="lang-content lang-zh">我们期待与您携手合作，共同开拓更广阔的市场，共创美好未来！</span>
                 <span class="lang-content lang-en">Our team is ready to consult and provide services to create leather products that meet your brand's needs and make a difference. Let's create a bright future together!</span>
            </p>
            <div class="contact-info">
                 <!-- Contact Item 1: Address -->
                 <div class="contact-item">
                     <i class="fas fa-map-marker-alt"></i>
                     <h3>
                         <span class="lang-content lang-th">ที่อยู่โรงงาน</span>
                         <span class="lang-content lang-zh">地址</span>
                         <span class="lang-content lang-en">Address</span>
                    </h3>
                     <p>
                         <span class="lang-content lang-th">เมืองกวางโจว, ประเทศจีน<br>(โปรดติดต่อสอบถามสำหรับรายละเอียดเพิ่มเติม)</span>
                         <span class="lang-content lang-zh">广州市花都区狮岭镇狮岭村横坑经济社自编7号</span>
                         <span class="lang-content lang-en">No. 7, Hengkeng Economic Society, Shiling Village, Shiling Town, Huadu District, Guangzhou City, China</span>
                     </p>
                 </div>
                 <!-- Contact Item 2: Phone -->
                 <div class="contact-item">
                     <i class="fas fa-phone"></i>
                     <h3>
                         <span class="lang-content lang-th">โทรศัพท์</span>
                         <span class="lang-content lang-zh">电话</span>
                         <span class="lang-content lang-en">Phone</span>
                    </h3>
                     <p><a href="tel:+8618124228857">+86 18124228857</a></p>
                 </div>
                 <!-- Contact Item 3: Email -->
                 <div class="contact-item">
                     <i class="fas fa-envelope"></i>
                     <h3>
                         <span class="lang-content lang-th">อีเมล</span>
                         <span class="lang-content lang-zh">邮箱</span>
                         <span class="lang-content lang-en">Email</span>
                    </h3>
                     <p><a href="mailto:914532079@qq.com">914532079@qq.com</a></p>
                 </div>
            </div>
             <img src="placeholder-contact.jpg" alt="Contact Guangzhou Pudanjiao Leather / 联系我们" class="contact-image"> <!-- REPLACE -->
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>
                <span class="lang-content lang-th">&copy; 2024 Guangzhou Pudanjiao Leather Co., Ltd. สงวนลิขสิทธิ์</span>
                <span class="lang-content lang-zh">&copy; 2024 广州普丹娇皮具有限公司 版权所有</span>
                <span class="lang-content lang-en">&copy; 2024 Guangzhou Pudanjiao Leather Co., Ltd. All rights reserved.</span>
            </p>
        </div>
    </footer>

    <!-- JavaScript for Language Switching and Smooth Scroll -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const toggleBtn = document.getElementById('lang-toggle-btn');
            const langDropdown = document.querySelector('.lang-dropdown');
            const langButtons = langDropdown.querySelectorAll('button[data-lang]');
            const htmlEl = document.documentElement;
            const toggleBtnText = toggleBtn.querySelector('.btn-lang-text'); // Get the text span

             // --- Language Switching Logic ---
            function setLanguage(lang) {
                 // Update HTML lang attribute
                const langAttr = lang === 'th' ? 'th' : (lang === 'zh' ? 'zh-CN' : 'en');
                htmlEl.lang = langAttr;

                // Update body font family
                document.body.style.fontFamily = lang === 'th' ? 'var(--font-family-th)' :
                                                 (lang === 'zh' ? 'var(--font-family-zh)' :
                                                 'var(--font-family-en)');

                // Toggle visibility of language content spans
                document.querySelectorAll('.lang-th').forEach(el => { el.style.display = lang === 'th' ? '' : 'none'; });
                document.querySelectorAll('.lang-zh').forEach(el => { el.style.display = lang === 'zh' ? '' : 'none'; });
                document.querySelectorAll('.lang-en').forEach(el => { el.style.display = lang === 'en' ? '' : 'none'; });

                 // Ensure correct display type (inline/block) after switching
                document.querySelectorAll('.lang-content').forEach(el => {
                    if (el.style.display !== 'none') {
                         // Restore inline display for spans (most common case)
                         if (el.tagName.toLowerCase() === 'span') {
                             el.style.display = 'inline';
                         }
                         // Add more specific rules if using block elements like <div>
                    }
                });

                // Update button text (optional, shows current lang)
                if (toggleBtnText) {
                    if (lang === 'th') toggleBtnText.textContent = 'ไทย';
                    else if (lang === 'zh') toggleBtnText.textContent = '中文';
                    else toggleBtnText.textContent = 'Eng'; // Abbreviated
                }

                // Update selected state in dropdown
                langButtons.forEach(button => {
                    button.classList.toggle('selected-lang', button.getAttribute('data-lang') === lang);
                });

                // Close dropdown after selection
                langDropdown.classList.remove('show-dropdown');
                toggleBtn.classList.remove('open');
            }

            // --- Dropdown Toggle Logic ---
            toggleBtn.addEventListener('click', function(event) {
                event.stopPropagation(); // Prevent click from immediately closing dropdown
                langDropdown.classList.toggle('show-dropdown');
                toggleBtn.classList.toggle('open'); // For rotating the arrow icon
            });

            // --- Language Selection Logic ---
            langButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const selectedLang = this.getAttribute('data-lang');
                    setLanguage(selectedLang);
                });
            });

            // --- Close Dropdown on Outside Click ---
            document.addEventListener('click', function(event) {
                if (!toggleBtn.contains(event.target) && !langDropdown.contains(event.target)) {
                    langDropdown.classList.remove('show-dropdown');
                    toggleBtn.classList.remove('open');
                }
            });

            // --- Set Initial Language State ---
            // Determine initial language (default is 'zh' based on HTML tag)
            let initialLang = 'zh'; // Default
            // Optionally check localStorage or other sources here if needed
            setLanguage(initialLang); // Apply initial language settings


            // --- Smooth Scroll Logic (remains the same) ---
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    if (targetId && targetId.length > 1) {
                         const targetElement = document.querySelector(targetId);
                         if (targetElement) {
                            targetElement.scrollIntoView({ behavior: 'smooth' });
                         }
                    }
                });
            });
        });
    </script>

</body>
</html>
