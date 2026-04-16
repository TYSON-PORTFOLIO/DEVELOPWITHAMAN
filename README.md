<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Develop With Aman | Tyson Game Demos + Premium Game Dev Package</title>
    <meta name="description" content="Explore live game demos with admin access & get complete game development package with hosting, domain, admin panel, APK in 24h. By Develop With Aman.">
    <!-- Fonts & Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #050c14;
            color: #eef2ff;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 30%, rgba(0, 40, 60, 0.5) 0%, rgba(0, 10, 25, 0.9) 100%),
                        repeating-linear-gradient(45deg, rgba(59,130,246,0.02) 0px, rgba(59,130,246,0.02) 2px, transparent 2px, transparent 8px);
            pointer-events: none;
            z-index: -2;
        }

        .glass-nav {
            background: rgba(8, 18, 28, 0.92);
            backdrop-filter: blur(18px);
            border-bottom: 1px solid rgba(0, 255, 255, 0.2);
            transition: all 0.3s ease;
            box-shadow: 0 8px 20px -6px rgba(0,0,0,0.3);
            z-index: 1030;
        }
        .brand-minimal {
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: -0.2px;
            background: linear-gradient(135deg, #e0f2fe, #60a5fa);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        .nav-link-custom {
            color: #cbd5e6;
            font-weight: 500;
            transition: 0.2s;
            margin: 0 0.5rem;
        }
        .nav-link-custom:hover, .nav-link-custom.active {
            color: #60a5fa;
        }
        
        /* Hero Section with Big Bold "DEVELOP WITH AMAN" */
        .hero-main {
            padding: 3rem 0 2rem;
            text-align: center;
            position: relative;
            border-bottom: 1px solid rgba(59,130,246,0.4);
            background: radial-gradient(ellipse at 50% 0%, rgba(30, 80, 120, 0.4), transparent 80%);
        }
        .main-brand {
            font-size: 4rem;
            font-weight: 900;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #ffffff, #60a5fa, #38bdf8);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            text-shadow: 0 2px 10px rgba(56,189,248,0.3);
        }
        .sub-brand {
            font-size: 1.2rem;
            font-weight: 500;
            color: #9ab3d4;
            border-top: 2px solid rgba(59,130,246,0.5);
            display: inline-block;
            padding-top: 0.5rem;
        }
        .hero-badge {
            background: rgba(59,130,246,0.2);
            backdrop-filter: blur(4px);
            border: 1px solid #3b82f6;
            color: #b9f2ff;
        }
        
        .demo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(360px, 1fr));
            gap: 2rem;
        }
        .game-card {
            background: rgba(12, 22, 35, 0.75);
            backdrop-filter: blur(12px);
            border-radius: 2rem;
            border: 1px solid rgba(56, 189, 248, 0.25);
            transition: all 0.4s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            overflow: hidden;
            box-shadow: 0 25px 35px -18px rgba(0,0,0,0.5);
        }
        .game-card:hover {
            transform: translateY(-6px) scale(1.01);
            border-color: #3b82f6;
            box-shadow: 0 30px 45px -12px rgba(59,130,246,0.35);
        }
        .card-header-plain {
            background: linear-gradient(95deg, rgba(0, 40, 60, 0.7), rgba(0, 20, 40, 0.5));
            padding: 1rem 1.5rem;
            border-bottom: 1px solid rgba(59,130,246,0.4);
        }
        .badge-category {
            background: rgba(59,130,246,0.2);
            backdrop-filter: blur(4px);
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.7rem;
            font-weight: 700;
            color: #b9f2ff;
            border: 1px solid rgba(59,130,246,0.5);
        }
        .credential-box {
            background: rgba(0, 0, 0, 0.5);
            border-radius: 1.4rem;
            padding: 0.9rem 1rem;
            font-size: 0.8rem;
            margin-top: 0.75rem;
            font-family: 'Inter', monospace;
            border-left: 3px solid #3b82f6;
        }
        .cred-row {
            display: flex;
            align-items: center;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 8px;
            font-size: 0.75rem;
            font-weight: 500;
        }
        .cred-label {
            font-weight: 700;
            color: #9ab3d4;
            min-width: 60px;
        }
        .copyable, .copy-icon {
            cursor: pointer;
            background: rgba(255,255,245,0.08);
            padding: 3px 8px;
            border-radius: 30px;
            transition: 0.15s;
        }
        .copyable:hover, .copy-icon:hover {
            background: #3b82f6;
            color: white;
        }
        .btn-demo, .btn-admin {
            padding: 0.5rem 1.2rem;
            border-radius: 2.5rem;
            font-weight: 600;
            font-size: 0.75rem;
            transition: 0.25s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            text-decoration: none;
        }
        .btn-demo {
            background: linear-gradient(105deg, #2563eb, #1e40af);
            color: white;
            box-shadow: 0 4px 10px rgba(37,99,235,0.3);
        }
        .btn-admin {
            background: rgba(30, 41, 59, 0.8);
            color: #cff3ff;
            border: 1px solid #3b82f6;
        }
        .filter-sidebar {
            background: rgba(8, 20, 32, 0.65);
            backdrop-filter: blur(16px);
            border-radius: 2rem;
            padding: 1.8rem;
            position: sticky;
            top: 100px;
            border: 1px solid rgba(56,189,248,0.25);
        }
        .filter-btn {
            background: rgba(15, 35, 55, 0.6);
            border: none;
            color: #cbd5e6;
            font-weight: 600;
            padding: 0.75rem 1rem;
            text-align: left;
            border-radius: 1.4rem;
            width: 100%;
            margin-bottom: 0.5rem;
        }
        .filter-btn.active {
            background: linear-gradient(95deg, #1e40af, #2563eb);
            color: white;
            box-shadow: 0 8px 18px -6px #1e3a8a;
        }
        .section-card {
            background: rgba(12, 22, 35, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 2rem;
            border: 1px solid rgba(59,130,246,0.3);
            transition: 0.2s;
        }
        .contact-icon-box {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 1.5rem;
            padding: 1.2rem;
            text-align: center;
            transition: 0.2s;
            height: 100%;
        }
        .contact-icon-box:hover {
            background: #1e293b;
            border-color: #3b82f6;
        }
        .premium-section {
            margin-top: 2rem;
            background: radial-gradient(circle at 10% 20%, #0a1428, #030b17);
            border-radius: 2.5rem;
            padding: 2rem 2rem 3rem;
            border: 1px solid rgba(59,130,246,0.3);
            box-shadow: 0 25px 40px -12px rgba(0,0,0,0.5);
        }
        .package-card {
            background: linear-gradient(145deg, rgba(255,255,255,0.05), rgba(30, 41, 59, 0.5));
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 1.5rem;
            padding: 1.5rem;
            transition: all 0.3s;
            backdrop-filter: blur(8px);
        }
        .package-card.premium {
            border: 2px solid #f59e0b;
            transform: scale(1.02);
        }
        .package-price {
            font-size: 2rem;
            font-weight: 800;
            color: #10b981;
        }
        .features-list {
            list-style: none;
            padding: 0;
        }
        .features-list li {
            padding: 0.5rem 0;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }
        .btn-primary {
            background: linear-gradient(135deg, #6366f1, #4f46e5);
            border: none;
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 2rem;
            font-weight: 600;
        }
        .timer-container {
            background: linear-gradient(135deg, #4f46e5, #6366f1);
            border-radius: 1rem;
            padding: 1rem;
            text-align: center;
            min-width: 140px;
        }
        .timer {
            font-size: 1.8rem;
            font-weight: 800;
            font-family: monospace;
        }
        .upi-id {
            font-size: 1.2rem;
            background: rgba(0,0,0,0.3);
            padding: 0.75rem;
            border-radius: 1rem;
            word-break: break-all;
            font-weight: 600;
        }
        .payment-schedule-steps {
            display: flex;
            justify-content: space-between;
            gap: 1rem;
            margin: 1.5rem 0;
        }
        .schedule-step {
            flex: 1;
            background: rgba(0,0,0,0.3);
            border-radius: 1rem;
            padding: 0.8rem;
            text-align: center;
            border-left: 3px solid #10b981;
        }
        .toast-msg {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #0f212e;
            backdrop-filter: blur(12px);
            color: #b9f2ff;
            padding: 10px 24px;
            border-radius: 60px;
            font-size: 0.85rem;
            z-index: 9999;
            opacity: 0;
            transition: opacity 0.2s;
            pointer-events: none;
            border-left: 4px solid #3b82f6;
        }
        .floating-social-group {
            position: fixed;
            bottom: 25px;
            left: 25px;
            z-index: 999;
            display: flex;
            flex-direction: column;
            gap: 14px;
        }
        .float-icon {
            width: 52px;
            height: 52px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: white;
            transition: 0.2s;
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
        }
        .whatsapp-float { background: #25D366; }
        .telegram-float { background: #1f8dd6; }
        .back-to-top {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: #1e293b;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            border: 1px solid #3b82f6;
            z-index: 99;
        }
        .owner-card {
            background: linear-gradient(145deg, rgba(255,215,0,0.1), rgba(0,0,0,0.6));
            border-left: 5px solid #f59e0b;
        }
        @media (max-width: 768px) {
            .premium-section { padding: 1.5rem; }
            .package-card.premium { transform: scale(1); }
            .payment-schedule-steps { flex-direction: column; }
            .main-brand { font-size: 2.5rem; }
        }
    </style>
</head>
<body>
<div id="toastMsg" class="toast-msg">✓ Copied to clipboard</div>

<!-- Sticky Header with Menu -->
<header class="glass-nav py-2 position-sticky top-0 z-3">
    <div class="container">
        <div class="d-flex justify-content-between align-items-center">
            <div class="brand-minimal fw-bold"><i class="fas fa-crown text-primary me-2"></i> TYSON | DEVELOP WITH AMAN</div>
            <div class="d-none d-md-flex gap-3">
                <a href="#demos-section" class="nav-link-custom text-decoration-none">Demos</a>
                <a href="#payment-package" class="nav-link-custom text-decoration-none">Payment</a>
                <a href="#contact-section" class="nav-link-custom text-decoration-none">Contact</a>
                <a href="#info-section" class="nav-link-custom text-decoration-none">Info</a>
                <a href="#owner-section" class="nav-link-custom text-decoration-none">Owner</a>
            </div>
            <div class="d-flex gap-2">
                <a href="tel:+918092043236" class="btn btn-outline-info btn-sm rounded-pill px-3 d-none d-sm-block"><i class="fas fa-headset me-1"></i> +91 8092043236</a>
                <button class="btn btn-primary btn-sm rounded-pill d-md-none" type="button" data-bs-toggle="offcanvas" data-bs-target="#mobileMenu"><i class="fas fa-grid"></i></button>
            </div>
        </div>
    </div>
</header>

<!-- BIG BOLD HERO: DEVELOP WITH AMAN -->
<section class="hero-main">
    <div class="container">
        <div class="mb-2">
            <span class="hero-badge badge rounded-pill px-4 py-2"><i class="fas fa-code-branch me-1"></i> Premium Game Solutions</span>
        </div>
        <h1 class="main-brand">DEVELOP WITH AMAN</h1>
        <div class="sub-brand mt-2">Tyson Game Demos | 24h Delivery | Full Stack Game Developer</div>
        <p class="text-white-50 mt-3">Enterprise-level game scripts, admin panels, APK, hosting & domain — All in one place</p>
    </div>
</section>

<!-- ========== DEMOS SECTION ========== -->
<section id="demos-section" class="container py-4">
    <div class="row g-4">
        <div class="col-lg-4">
            <div class="filter-sidebar">
                <h5 class="fw-bold mb-3 fs-6"><i class="fas fa-compass me-2 text-info"></i> Categories</h5>
                <div class="d-flex flex-column gap-2" id="filterGroup">
                    <button class="filter-btn active" data-category="all"><i class="fas fa-th-large me-2"></i>All Demos</button>
                    <button class="filter-btn" data-category="color-prediction"><i class="fas fa-chart-line me-2"></i>Color Prediction</button>
                    <button class="filter-btn" data-category="casino"><i class="fas fa-dice-d6 me-2"></i>Casino & iGaming</button>
                </div>
                <hr class="bg-secondary opacity-25 my-4">
                <div class="text-center">
                    <i class="fas fa-rocket text-info fs-4 mb-2"></i>
                    <p class="small text-white-50">Need custom game? Contact owner directly</p>
                    <a href="#owner-section" class="btn btn-sm btn-outline-warning rounded-pill">Meet Aman <i class="fas fa-user-astronaut ms-1"></i></a>
                </div>
            </div>
        </div>
        <div class="col-lg-8">
            <div class="d-flex justify-content-between align-items-center mb-4 flex-wrap">
                <h5 class="fw-bold m-0"><i class="fas fa-cubes me-2 text-primary"></i>Live demo instances</h5>
                <span class="badge bg-primary bg-opacity-25 text-info px-3 py-2 rounded-pill fs-6" id="demoCount"></span>
            </div>
            <div id="cardsContainer" class="demo-grid">
                <div class="text-center py-5 w-100">Loading demos...</div>
            </div>
        </div>
    </div>
</section>

<!-- ========== PAYMENT & PACKAGE SECTION ========== -->
<section id="payment-package" class="container mb-5">
    <div class="premium-section">
        <div class="text-center mb-4">
            <span class="badge bg-warning text-dark px-3 py-2 rounded-pill"><i class="fas fa-bolt"></i> LIMITED TIME OFFER</span>
            <h2 class="display-6 fw-bold mt-3">Complete Game Development <span class="text-warning">Package in 24h</span></h2>
            <p class="text-white-50">Get hosting, domain, admin panel, APK, website & full script — everything included</p>
        </div>
        <!-- 3 Package Cards -->
        <div class="row g-4 mb-5">
            <div class="col-md-4">
                <div class="package-card h-100">
                    <div class="mb-3"><i class="fas fa-mobile-alt fa-2x text-primary"></i></div>
                    <h4>Basic Setup</h4>
                    <div class="package-price">₹5,000</div>
                    <ul class="features-list mt-3">
                        <li><i class="fas fa-check text-success"></i> 6 Months Hosting</li>
                        <li><i class="fas fa-check text-success"></i> Basic Admin Panel</li>
                        <li><i class="fas fa-check text-success"></i> Game Script</li>
                        <li><i class="fas fa-times text-danger"></i> No APK</li>
                        <li><i class="fas fa-times text-danger"></i> No Custom Domain</li>
                    </ul>
                    <button class="btn btn-primary w-100 mt-3" onclick="selectPackage('basic')">Select Basic</button>
                </div>
            </div>
            <div class="col-md-4">
                <div class="package-card premium h-100">
                    <div class="bg-warning text-dark rounded-pill px-3 py-1 d-inline-block mb-2">🔥 MOST POPULAR</div>
                    <div class="mb-3"><i class="fas fa-gamepad fa-2x text-warning"></i></div>
                    <h4>Complete Package</h4>
                    <div class="package-price">₹10,000</div>
                    <ul class="features-list mt-3">
                        <li><i class="fas fa-check text-success"></i> 1 Year Premium Hosting</li>
                        <li><i class="fas fa-check text-success"></i> 1 Year Domain (.com/.in)</li>
                        <li><i class="fas fa-check text-success"></i> Advanced Admin Panel</li>
                        <li><i class="fas fa-check text-success"></i> Android APK (Signed)</li>
                        <li><i class="fas fa-check text-success"></i> phpMyAdmin Access</li>
                        <li><i class="fas fa-check text-success"></i> 24/7 Support</li>
                    </ul>
                    <button class="btn btn-primary w-100 mt-3" onclick="selectPackage('complete')">Select Complete</button>
                </div>
            </div>
            <div class="col-md-4">
                <div class="package-card h-100">
                    <div class="mb-3"><i class="fas fa-rocket fa-2x text-primary"></i></div>
                    <h4>Enterprise</h4>
                    <div class="package-price">₹25,000</div>
                    <ul class="features-list mt-3">
                        <li><i class="fas fa-check text-success"></i> 2 Years Enterprise Hosting</li>
                        <li><i class="fas fa-check text-success"></i> Custom Admin Panel</li>
                        <li><i class="fas fa-check text-success"></i> Android + iOS Apps</li>
                        <li><i class="fas fa-check text-success"></i> Priority Support</li>
                    </ul>
                    <button class="btn btn-primary w-100 mt-3" onclick="selectPackage('enterprise')">Select Enterprise</button>
                </div>
            </div>
        </div>

        <!-- Professional Payment Gateway Section -->
        <div id="paymentSection">
            <div class="row g-4">
                <div class="col-lg-7">
                    <div class="bg-dark bg-opacity-50 rounded-4 p-4 h-100">
                        <div class="d-flex justify-content-between align-items-center flex-wrap mb-4">
                            <h3 class="mb-0"><i class="fas fa-lock text-primary me-2"></i> Secure Payment</h3>
                            <div class="timer-container">
                                <div class="small text-white-50">OFFER EXPIRES IN</div>
                                <div class="timer text-white" id="countdownTimer">05:00</div>
                            </div>
                        </div>
                        <div class="order-summary-card bg-black bg-opacity-40 rounded-4 p-3">
                            <h5 class="fw-bold mb-3"><i class="fas fa-receipt"></i> Order Summary</h5>
                            <div class="d-flex justify-content-between border-bottom pb-2 mb-2">
                                <span>Selected Package</span>
                                <strong id="selectedPackage">Complete Game Package</strong>
                            </div>
                            <div class="d-flex justify-content-between border-bottom pb-2 mb-2">
                                <span>Total Price</span>
                                <strong id="totalPrice">₹10,000</strong>
                            </div>
                            <div class="d-flex justify-content-between pb-2">
                                <span>Advance (40%)</span>
                                <strong class="text-success fs-4" id="advanceAmount">₹4,000</strong>
                            </div>
                        </div>
                        <div class="mt-4">
                            <h6 class="fw-bold"><i class="fas fa-calendar-week"></i> Payment Schedule</h6>
                            <div class="payment-schedule-steps">
                                <div class="schedule-step"><div class="schedule-percent">40%</div><div>Advance</div><small>to start</small></div>
                                <div class="schedule-step"><div class="schedule-percent">30%</div><div>After Game Live</div><small>demo ready</small></div>
                                <div class="schedule-step"><div class="schedule-percent">30%</div><div>On Delivery</div><small>final files</small></div>
                            </div>
                        </div>
                        <div class="mt-4 bg-black bg-opacity-30 p-3 rounded-3">
                            <div class="text-center mb-2"><i class="fas fa-qrcode text-primary"></i> Send Advance Payment To</div>
                            <div class="upi-id text-center" id="displayUpiId">8092043236@ybl</div>
                            <div class="d-flex gap-3 justify-content-center mt-3">
                                <button class="btn btn-primary btn-sm" onclick="copyUpiId()"><i class="fas fa-copy"></i> Copy UPI ID</button>
                                <button class="btn btn-secondary btn-sm" onclick="openAllUpiApps()"><i class="fas fa-external-link-alt"></i> Pay with UPI</button>
                            </div>
                            <p class="text-center small text-white-50 mt-2">After payment, share screenshot on Telegram for instant confirmation</p>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5">
                    <div class="bg-dark bg-opacity-50 rounded-4 p-4 text-center h-100 d-flex flex-column justify-content-center">
                        <h4><i class="fas fa-qrcode text-primary"></i> Scan QR Code</h4>
                        <canvas id="qrCanvas" width="200" height="200" style="background:white; border-radius: 1rem; margin: 1rem auto; display: block;"></canvas>
                        <p class="small text-white-50">Scan with any UPI app (Google Pay, PhonePe, Paytm)</p>
                        <a href="https://t.me/pluginxpertcode" target="_blank" class="btn btn-outline-info btn-sm mt-2"><i class="fab fa-telegram"></i> Contact on Telegram</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- ========== OWNER SECTION (About Owner with portfolio link) ========== -->
<section id="owner-section" class="container mb-5">
    <div class="section-card p-4 p-lg-5 owner-card">
        <div class="row align-items-center g-4">
            <div class="col-md-3 text-center">
                <div class="bg-primary bg-opacity-20 rounded-circle p-3 d-inline-block">
                    <i class="fas fa-user-tie fa-4x text-warning"></i>
                </div>
            </div>
            <div class="col-md-9">
                <h2 class="fw-bold mb-2"><i class="fas fa-crown text-warning me-2"></i> About The Owner: Aman</h2>
                <p class="lead fs-6 text-white-70">Full-stack game developer & founder of <strong class="text-info">"Develop With Aman"</strong>. Specialized in color prediction games, casino scripts, and complete iGaming ecosystems. 5+ years of experience, delivered 100+ projects worldwide.</p>
                <div class="d-flex flex-wrap gap-3 mt-3">
                    <a href="https://tyson-portfolio-v2.github.io/BIO/" target="_blank" class="btn btn-warning rounded-pill px-4"><i class="fas fa-globe me-2"></i> View Full Portfolio / BIO</a>
                    <a href="https://t.me/tyson_owner" target="_blank" class="btn btn-outline-light rounded-pill"><i class="fab fa-telegram"></i> Telegram: @tyson_owner</a>
                </div>
                <div class="mt-3 small text-white-50"><i class="fas fa-check-circle text-success"></i> Verified Creator | Premium Game Solutions | 24/7 Availability</div>
            </div>
        </div>
    </div>
</section>

<!-- ========== CONTACT SECTION ========== -->
<section id="contact-section" class="container mb-5">
    <div class="section-card p-4 p-lg-5">
        <h2 class="fw-bold mb-4 text-center"><i class="fas fa-address-card text-primary me-2"></i> Contact & Support</h2>
        <div class="row g-4">
            <div class="col-md-4">
                <div class="contact-icon-box">
                    <i class="fab fa-telegram fa-3x text-info mb-3"></i>
                    <h5>Telegram Direct</h5>
                    <p class="small">@tyson_owner</p>
                    <button class="btn btn-sm btn-outline-info copyable-telegram" data-copy="@tyson_owner">Copy Username</button>
                </div>
            </div>
            <div class="col-md-4">
                <div class="contact-icon-box">
                    <i class="fab fa-whatsapp fa-3x text-success mb-3"></i>
                    <h5>WhatsApp</h5>
                    <p class="small">+91 8092043236</p>
                    <a href="https://wa.me/+918092043236?text=I%20need%20game%20dev%20package" target="_blank" class="btn btn-sm btn-success">Chat Now</a>
                </div>
            </div>
            <div class="col-md-4">
                <div class="contact-icon-box">
                    <i class="fab fa-youtube fa-3x text-danger mb-3"></i>
                    <h5>YouTube Channel</h5>
                    <p class="small">@developwithaman</p>
                    <a href="https://youtube.com/@developwithaman?si=Qt9Uc01-mnJ3OaXn" target="_blank" class="btn btn-sm btn-outline-danger">Subscribe</a>
                </div>
            </div>
            <div class="col-12 mt-2">
                <div class="bg-black bg-opacity-30 p-3 rounded-4 text-center">
                    <i class="fas fa-envelope me-2 text-info"></i> Email: aman@developwithaman.com  |  <i class="fas fa-headset me-2"></i> Priority support: Telegram @pluginxpertcode
                </div>
            </div>
        </div>
    </div>
</section>

<!-- ========== INFO SECTION ========== -->
<section id="info-section" class="container mb-5">
    <div class="section-card p-4 p-lg-5">
        <h2 class="fw-bold mb-4 text-center"><i class="fas fa-circle-info text-primary me-2"></i> Why Choose Develop With Aman?</h2>
        <div class="row g-4">
            <div class="col-md-6">
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-clock fa-2x text-primary"></i>
                    <div><h5 class="mb-1">24 Hours Delivery</h5><p class="small text-white-50">Fully functional game + admin panel + APK delivered within 24h after advance.</p></div>
                </div>
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-code fa-2x text-primary"></i>
                    <div><h5 class="mb-1">100% Source Code</h5><p class="small text-white-50">Full PHP/MySQL script, editable, no encryption. Full ownership.</p></div>
                </div>
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-mobile-alt fa-2x text-primary"></i>
                    <div><h5 class="mb-1">Android APK + Website</h5><p class="small text-white-50">Signed APK ready for playstore, along with responsive web app.</p></div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-shield-alt fa-2x text-primary"></i>
                    <div><h5 class="mb-1">Secure Admin Panel</h5><p class="small text-white-50">Advanced dashboard, user management, withdrawal logs, analytics.</p></div>
                </div>
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-database fa-2x text-primary"></i>
                    <div><h5 class="mb-1">phpMyAdmin Access</h5><p class="small text-white-50">Full database control & backup, complete transparency.</p></div>
                </div>
                <div class="d-flex gap-3 mb-3">
                    <i class="fas fa-headset fa-2x text-primary"></i>
                    <div><h5 class="mb-1">24/7 Dedicated Support</h5><p class="small text-white-50">Free installation, bug fixes, and 1 month free technical support.</p></div>
                </div>
            </div>
        </div>
        <hr class="bg-secondary opacity-25 my-4">
        <div class="text-center">
            <p class="mb-0 fw-light">⚡ Over 100+ successful game deployments | Trusted by global clients | Money-back guarantee on delivery</p>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="pt-4 pb-3 mt-2">
    <div class="container">
        <div class="row gy-3 align-items-center">
            <div class="col-md-6"><p class="text-white-50 small m-0">© 2025 Develop With Aman | Tyson Game Demos | Premium Game Dev Solutions</p></div>
            <div class="col-md-6 text-md-end">
                <div class="d-flex gap-3 justify-content-md-end">
                    <a href="https://t.me/pluginxpertcode" target="_blank" class="text-white-50 small"><i class="fab fa-telegram"></i> Telegram</a>
                    <a href="https://youtube.com/@developwithaman" target="_blank" class="text-white-50 small"><i class="fab fa-youtube"></i> YouTube</a>
                    <a href="https://tyson-portfolio-v2.github.io/BIO/" target="_blank" class="text-white-50 small"><i class="fas fa-user"></i> Owner BIO</a>
                </div>
            </div>
        </div>
    </div>
</footer>

<!-- Floating Social & Back to top -->
<div class="floating-social-group">
    <a href="https://wa.me/+918092043236?text=I%20want%20to%20explore%20premium%20demos" target="_blank" class="float-icon whatsapp-float"><i class="fab fa-whatsapp"></i></a>
    <a href="https://t.me/tyson_owner" target="_blank" class="float-icon telegram-float"><i class="fab fa-telegram-plane"></i></a>
</div>
<div class="back-to-top" id="backToTop"><i class="fas fa-arrow-up"></i></div>

<script>
    // Demo Data same as before (11 games)
    const gamesData = [
        { name: "Tiranga Game", category: "color-prediction", userUrl: "https://tiranga.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://tiranga.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "YL Game", category: "color-prediction", userUrl: "https://yl.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://yl.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "91Club Game", category: "color-prediction", userUrl: "https://91club.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://91club.gamesdemo.shop/admin/index.php", adminUser: "admin", adminPass: "admin" },
        { name: "Daman Game", category: "color-prediction", userUrl: "https://daman.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://daman.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "Raja Game", category: "color-prediction", userUrl: "https://raja.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://raja.gamesdemo.shop/admin/index.php", adminUser: "admin", adminPass: "admin" },
        { name: "Big Daddy Game (BDG)", category: "color-prediction", userUrl: "https://bdg.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://bdg.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "1 Win Game", category: "casino", userUrl: "https://1win.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://1win.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "KWG Game", category: "color-prediction", userUrl: "https://kwg.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://kwg.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "RS Win Game", category: "color-prediction", userUrl: "https://rswin.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://rswin.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" },
        { name: "Deuwin Game", category: "color-prediction", userUrl: "https://deuwin.rcosdemo.online/", username: "1234567890", password: "1234567890", adminUrl: "https://diuwin.gamesdemo.shop/admin/index.php", adminUser: "admin", adminPass: "admin" },
        { name: "iGaming / Casino Suite", category: "casino", userUrl: "https://igaming.gamesdemo.shop/", username: "1234567890", password: "1234567890", adminUrl: "https://igaming.gamesdemo.shop/admin", adminUser: "admin", adminPass: "admin" }
    ];

    function copyToClipboard(text) {
        navigator.clipboard.writeText(text).then(() => {
            let toast = document.getElementById('toastMsg');
            toast.style.opacity = '1';
            setTimeout(() => toast.style.opacity = '0', 1500);
        }).catch(() => alert("Copy manually: " + text));
    }

    let currentCategory = "all";
    function renderCards() {
        const container = document.getElementById('cardsContainer');
        const filtered = currentCategory === "all" ? gamesData : gamesData.filter(g => g.category === currentCategory);
        document.getElementById('demoCount').innerText = `${filtered.length} demo${filtered.length !== 1 ? 's' : ''}`;
        if (filtered.length === 0) { container.innerHTML = `<div class="col-12 text-center py-5"><p>No demos</p></div>`; return; }
        let html = '';
        filtered.forEach((game, idx) => {
            const catDisplay = game.category === 'color-prediction' ? '🎨 Color Prediction' : '🎰 Casino / iGaming';
            html += `<div class="game-card">
                <div class="card-header-plain d-flex justify-content-between align-items-center">
                    <h5 class="fw-bold mb-0 fs-6">${game.name}</h5>
                    <span class="badge-category">${catDisplay}</span>
                </div>
                <div class="p-4">
                    <div class="credential-box">
                        <div class="cred-row"><span class="cred-label">🌐 User URL:</span> <a href="${game.userUrl}" target="_blank" class="text-info small">${game.userUrl.replace('https://','')}</a><i class="fas fa-copy copy-icon ms-1" data-copy="${game.userUrl}"></i></div>
                        <div class="cred-row"><span class="cred-label">👤 Login:</span> <span class="copyable" data-copy="${game.username}">${game.username}</span> / <span class="copyable" data-copy="${game.password}">${game.password}</span></div>
                        <div class="cred-row"><span class="cred-label">⚙️ Admin:</span> <a href="${game.adminUrl}" target="_blank" class="text-info small">${game.adminUrl.replace('https://','').substring(0,45)}</a><i class="fas fa-copy copy-icon ms-1" data-copy="${game.adminUrl}"></i></div>
                        <div class="cred-row"><span class="cred-label">🔐 Admin auth:</span> <span class="copyable" data-copy="${game.adminUser}">${game.adminUser}</span> / <span class="copyable" data-copy="${game.adminPass}">${game.adminPass}</span></div>
                    </div>
                    <div class="d-flex gap-3 mt-4"><a href="${game.userUrl}" target="_blank" class="btn-demo"><i class="fas fa-play-circle"></i> Launch Demo</a><a href="${game.adminUrl}" target="_blank" class="btn-admin"><i class="fas fa-shield-alt"></i> Admin Panel</a></div>
                </div>
            </div>`;
        });
        container.innerHTML = html;
        document.querySelectorAll('.copyable, .copy-icon').forEach(el => el.addEventListener('click', (e) => { e.stopPropagation(); let txt = el.getAttribute('data-copy') || el.innerText; if(txt) copyToClipboard(txt); }));
    }
    function initFilters() {
        document.querySelectorAll('.filter-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                currentCategory = btn.getAttribute('data-category');
                renderCards();
            });
        });
    }
    renderCards(); initFilters();
    document.getElementById('backToTop')?.addEventListener('click', () => window.scrollTo({top:0,behavior:'smooth'}));

    // Package logic
    let countdownMinutes = 5, countdownSeconds = 0, countdownInterval;
    function startCountdown() {
        const timerEl = document.getElementById('countdownTimer');
        countdownInterval = setInterval(() => {
            if (countdownSeconds === 0) {
                if (countdownMinutes === 0) { clearInterval(countdownInterval); timerEl.innerText = "EXPIRED"; timerEl.style.color = "#ef4444"; return; }
                countdownMinutes--; countdownSeconds = 59;
            } else countdownSeconds--;
            timerEl.innerText = `${String(countdownMinutes).padStart(2,'0')}:${String(countdownSeconds).padStart(2,'0')}`;
        }, 1000);
    }
    function selectPackage(type) {
        const pkg = { basic: { name: 'Basic Setup Package', price: 5000, advance: 2000 }, complete: { name: 'Complete Game Package', price: 10000, advance: 4000 }, enterprise: { name: 'Enterprise Package', price: 25000, advance: 10000 } };
        const selected = pkg[type];
        document.getElementById('selectedPackage').innerText = selected.name;
        document.getElementById('totalPrice').innerHTML = `₹${selected.price.toLocaleString()}`;
        document.getElementById('advanceAmount').innerHTML = `₹${selected.advance.toLocaleString()}`;
        updateQRCode(selected.advance);
        document.getElementById('payment-package').scrollIntoView({ behavior: 'smooth' });
    }
    function drawSimpleQR(ctx, amount) {
        ctx.fillStyle = '#ffffff'; ctx.fillRect(0, 0, 200, 200);
        ctx.fillStyle = '#000000';
        ctx.fillRect(20, 20, 40, 40); ctx.fillRect(20, 140, 40, 40); ctx.fillRect(140, 20, 40, 40);
        ctx.font = 'bold 14px Inter'; ctx.fillStyle = '#1e293b'; ctx.textAlign = 'center';
        ctx.fillText(`₹${amount}`, 100, 180);
        ctx.font = '10px monospace'; ctx.fillStyle = '#475569';
        ctx.fillText('8092043236@ybl', 100, 195);
    }
    function updateQRCode(amount) { const canvas = document.getElementById('qrCanvas'); if(canvas) { const ctx = canvas.getContext('2d'); drawSimpleQR(ctx, amount); } }
    function copyUpiId() { copyToClipboard('8092043236@ybl'); }
    function openAllUpiApps() { const amount = document.getElementById('advanceAmount').innerText.replace(/[^0-9]/g, ''); window.location.href = `upi://pay?pa=8092043236@ybl&pn=Tyson%20Dev&am=${amount}&cu=INR`; setTimeout(() => copyToClipboard('8092043236@ybl'), 800); }
    window.onload = () => {
        startCountdown();
        const canvas = document.getElementById('qrCanvas'); if(canvas) drawSimpleQR(canvas.getContext('2d'), 4000);
        document.querySelectorAll('.copyable-telegram').forEach(el => el.addEventListener('click', () => copyToClipboard('@tyson_owner')));
    };
</script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>

<!-- Offcanvas Mobile Menu -->
<div class="offcanvas offcanvas-start bg-dark" tabindex="-1" id="mobileMenu">
    <div class="offcanvas-header"><h5 class="offcanvas-title text-white">Menu</h5><button type="button" class="btn-close btn-close-white" data-bs-dismiss="offcanvas"></button></div>
    <div class="offcanvas-body">
        <ul class="nav flex-column gap-3">
            <li><a href="#demos-section" class="text-white text-decoration-none">Demos</a></li>
            <li><a href="#payment-package" class="text-white-50 text-decoration-none">Payment & Package</a></li>
            <li><a href="#contact-section" class="text-white-50 text-decoration-none">Contact</a></li>
            <li><a href="#info-section" class="text-white-50 text-decoration-none">Info</a></li>
            <li><a href="#owner-section" class="text-white-50 text-decoration-none">Owner Bio</a></li>
            <li><a href="tel:+918092043236" class="btn btn-outline-light w-100 rounded-pill mt-3"><i class="fas fa-phone-alt"></i> Call +91 8092043236</a></li>
        </ul>
    </div>
</div>
</body>
</html>
