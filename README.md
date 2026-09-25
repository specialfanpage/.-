<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PrivateSpot | Exclusive World</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Inter,Arial,sans-serif;
}

:root{
    --pink:#ff4d88;
    --pink2:#ff78a7;
    --dark:#08080c;
    --card:#111116;
    --card2:#17171e;
    --text:#fff;
    --muted:#a8a8b3;
    --border:rgba(255,255,255,.09);
}

body{
    background:#08080c;
    color:var(--text);
    min-height:100vh;
    overflow-x:hidden;
}

body:before{
    content:"";
    position:fixed;
    width:500px;
    height:500px;
    background:rgba(255,77,136,.12);
    filter:blur(120px);
    border-radius:50%;
    top:-200px;
    left:-150px;
    z-index:-1;
}

body:after{
    content:"";
    position:fixed;
    width:450px;
    height:450px;
    background:rgba(120,70,255,.08);
    filter:blur(120px);
    border-radius:50%;
    right:-180px;
    bottom:-150px;
    z-index:-1;
}

/* NAVIGATION */

nav{
    position:sticky;
    top:0;
    z-index:1000;
    min-height:72px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 5%;
    background:rgba(8,8,12,.88);
    backdrop-filter:blur(18px);
    border-bottom:1px solid var(--border);
}

.logo{
    font-size:23px;
    font-weight:900;
    letter-spacing:-1px;
}

.logo span{
    color:var(--pink);
}

#navLinks{
    display:flex;
    gap:8px;
    align-items:center;
    flex-wrap:wrap;
}

.nav-btn{
    background:transparent;
    color:#ddd;
    border:0;
    padding:10px 13px;
    border-radius:10px;
    cursor:pointer;
    transition:.25s;
    font-size:14px;
}

.nav-btn:hover{
    background:rgba(255,77,136,.1);
    color:#fff;
}

.logout-btn{
    border:1px solid rgba(255,77,136,.4);
    color:var(--pink);
}

/* GENERAL */

.page{
    display:none;
    min-height:calc(100vh - 72px);
    padding:55px 7%;
    animation:fade .4s ease;
}

.page.active{
    display:block;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(10px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.container{
    max-width:1150px;
    margin:auto;
}

.section-title{
    margin-bottom:30px;
}

.section-title small{
    color:var(--pink);
    text-transform:uppercase;
    letter-spacing:3px;
    font-size:11px;
    font-weight:bold;
}

.section-title h2{
    font-size:36px;
    margin-top:8px;
}

.section-title p{
    color:var(--muted);
    margin-top:8px;
}

/* HOME */

.home-page{
    display:none;
    align-items:center;
    padding:0 7%;
    min-height:calc(100vh - 72px);
    position:relative;
}

.home-page.active{
    display:flex;
}

.home-layout{
    max-width:1150px;
    width:100%;
    margin:auto;
    display:grid;
    grid-template-columns:1.15fr .85fr;
    gap:60px;
    align-items:center;
}

.badge{
    display:inline-flex;
    align-items:center;
    gap:8px;
    padding:8px 14px;
    border:1px solid rgba(255,77,136,.3);
    background:rgba(255,77,136,.07);
    color:#ff8bb2;
    border-radius:50px;
    font-size:12px;
    margin-bottom:20px;
}

.home-content h1{
    font-size:clamp(45px,7vw,82px);
    line-height:.95;
    letter-spacing:-4px;
}

.home-content h1 span{
    color:var(--pink);
}

.home-content p{
    color:var(--muted);
    max-width:560px;
    line-height:1.8;
    margin:25px 0;
    font-size:16px;
}

.primary-btn{
    border:0;
    padding:14px 24px;
    background:linear-gradient(135deg,var(--pink),#ff286d);
    color:#fff;
    border-radius:13px;
    cursor:pointer;
    font-weight:bold;
    box-shadow:0 12px 35px rgba(255,77,136,.2);
    transition:.25s;
}

.primary-btn:hover{
    transform:translateY(-3px);
    box-shadow:0 16px 40px rgba(255,77,136,.35);
}

.secondary-btn{
    padding:13px 20px;
    border-radius:13px;
    background:transparent;
    color:#fff;
    border:1px solid var(--border);
    cursor:pointer;
}

/* HERO CARD */

.hero-card{
    height:430px;
    border-radius:30px;
    background:
        linear-gradient(145deg,rgba(255,77,136,.2),rgba(20,20,30,.95));
    border:1px solid var(--border);
    position:relative;
    overflow:hidden;
    box-shadow:0 30px 80px rgba(0,0,0,.35);
}

.hero-circle{
    position:absolute;
    width:280px;
    height:280px;
    border-radius:50%;
    border:1px solid rgba(255,255,255,.1);
    left:50%;
    top:43%;
    transform:translate(-50%,-50%);
}

.hero-circle:before{
    content:"";
    position:absolute;
    width:190px;
    height:190px;
    border-radius:50%;
    border:1px solid rgba(255,77,136,.25);
    left:50%;
    top:50%;
    transform:translate(-50%,-50%);
}

.hero-center{
    position:absolute;
    left:50%;
    top:43%;
    transform:translate(-50%,-50%);
    width:130px;
    height:130px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    background:linear-gradient(145deg,#ff4d88,#7f1741);
    font-size:48px;
    box-shadow:0 0 70px rgba(255,77,136,.3);
}

.hero-info{
    position:absolute;
    bottom:25px;
    left:25px;
    right:25px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.online{
    color:#5dff9b;
    font-size:12px;
}

/* CARDS */

.cards{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.card{
    background:linear-gradient(145deg,var(--card2),var(--card));
    border:1px solid var(--border);
    border-radius:20px;
    padding:25px;
    transition:.3s;
}

.card:hover{
    transform:translateY(-5px);
    border-color:rgba(255,77,136,.35);
}

.icon{
    width:45px;
    height:45px;
    border-radius:13px;
    background:rgba(255,77,136,.1);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:21px;
    margin-bottom:18px;
}

.card h3{
    margin-bottom:9px;
}

.card p{
    color:var(--muted);
    line-height:1.6;
    font-size:14px;
}

/* WELCOME */

.welcome-box{
    max-width:900px;
    margin:30px auto;
    padding:70px 40px;
    text-align:center;
    border-radius:30px;
    background:linear-gradient(145deg,#17171e,#0e0e13);
    border:1px solid var(--border);
}

.welcome-box h1{
    font-size:52px;
    letter-spacing:-2px;
}

.welcome-box h1 span{
    color:var(--pink);
}

.welcome-box p{
    color:var(--muted);
    max-width:600px;
    margin:20px auto 30px;
    line-height:1.8;
}

/* AUTH */

.auth-wrapper{
    max-width:450px;
    margin:20px auto;
}

.auth-card{
    background:linear-gradient(145deg,#17171e,#0d0d12);
    padding:35px;
    border:1px solid var(--border);
    border-radius:25px;
}

.auth-card h2{
    margin-bottom:8px;
    font-size:30px;
}

.auth-card > p{
    color:var(--muted);
    margin-bottom:25px;
}

input,select{
    width:100%;
    padding:14px 15px;
    background:#09090d;
    border:1px solid var(--border);
    border-radius:11px;
    color:#fff;
    outline:none;
    margin-bottom:13px;
}

input:focus,
select:focus{
    border-color:var(--pink);
}

.auth-card button{
    width:100%;
}

/* LOCKED CONTENT */

.content-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.lock-card{
    height:230px;
    border-radius:20px;
    background:
        linear-gradient(135deg,rgba(255,77,136,.1),rgba(0,0,0,.7));
    border:1px solid var(--border);
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    position:relative;
    overflow:hidden;
}

.lock-card:before{
    content:"";
    position:absolute;
    inset:0;
    background:repeating-linear-gradient(
        45deg,
        transparent,
        transparent 10px,
        rgba(255,255,255,.015) 10px,
        rgba(255,255,255,.015) 20px
    );
}

.lock-icon{
    width:62px;
    height:62px;
    border-radius:50%;
    background:rgba(255,77,136,.1);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:26px;
    z-index:1;
}

.lock-card h3,
.lock-card p{
    z-index:1;
}

.lock-card h3{
    margin-top:15px;
}

.lock-card p{
    color:var(--muted);
    font-size:13px;
    margin-top:5px;
}

/* PLANS */

.plans{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.plan{
    background:linear-gradient(145deg,#15151c,#0c0c11);
    border:1px solid var(--border);
    padding:30px;
    border-radius:24px;
    position:relative;
}

.plan.featured{
    border-color:var(--pink);
    transform:translateY(-8px);
}

.plan-tag{
    position:absolute;
    right:20px;
    top:20px;
    background:var(--pink);
    color:#fff;
    padding:5px 9px;
    font-size:10px;
    border-radius:20px;
    font-weight:bold;
}

.plan h3{
    font-size:21px;
}

.price{
    font-size:42px;
    font-weight:900;
    margin:18px 0;
}

.price small{
    font-size:13px;
    color:var(--muted);
    font-weight:normal;
}

.plan ul{
    list-style:none;
    margin:20px 0;
}

.plan li{
    color:#c4c4ca;
    margin:12px 0;
    font-size:14px;
}

.plan li:before{
    content:"✓";
    color:var(--pink);
    margin-right:9px;
}

/* CHAT */

.chat-shell{
    max-width:850px;
    margin:auto;
    background:#0d0d12;
    border:1px solid var(--border);
    border-radius:25px;
    overflow:hidden;
}

.chat-header{
    padding:20px;
    border-bottom:1px solid var(--border);
    display:flex;
    align-items:center;
    gap:12px;
}

.chat-avatar{
    width:45px;
    height:45px;
    border-radius:50%;
    background:linear-gradient(135deg,var(--pink),#771538);
    display:flex;
    align-items:center;
    justify-content:center;
}

.chat-status{
    color:#5dff9b;
    font-size:11px;
}

#chatMessages{
    height:450px;
    overflow-y:auto;
    padding:25px;
}

.message{
    max-width:75%;
    padding:12px 15px;
    margin-bottom:12px;
    border-radius:16px;
    line-height:1.5;
    font-size:14px;
}

.bot{
    background:#191920;
    border-bottom-left-radius:5px;
}

.user{
    background:linear-gradient(135deg,var(--pink),#e92e6c);
    margin-left:auto;
    border-bottom-right-radius:5px;
}

.chat-form{
    display:flex;
    gap:10px;
    padding:15px;
    border-top:1px solid var(--border);
}

.chat-form input{
    margin:0;
}

.chat-form button{
    width:55px;
    border:0;
    border-radius:12px;
    background:var(--pink);
    color:#fff;
    cursor:pointer;
}

.handoff-box{
    margin:0 20px 20px;
    padding:20px;
    border:1px solid rgba(255,77,136,.3);
    border-radius:17px;
    background:rgba(255,77,136,.06);
}

.handoff-box a{
    display:inline-block;
    margin-top:12px;
    color:#fff;
    background:var(--pink);
    text-decoration:none;
    padding:11px 17px;
    border-radius:10px;
}

/* PROFILE */

.profile-header{
    background:linear-gradient(135deg,#17171e,#0d0d12);
    border:1px solid var(--border);
    border-radius:25px;
    padding:35px;
    display:flex;
    align-items:center;
    gap:25px;
    margin-bottom:25px;
}

.profile-avatar{
    width:90px;
    height:90px;
    border-radius:50%;
    background:linear-gradient(135deg,var(--pink),#751638);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:32px;
    font-weight:bold;
}

.profile-header p{
    color:var(--muted);
    margin-top:5px;
}

.profile-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.profile-stat{
    background:#111116;
    border:1px solid var(--border);
    border-radius:18px;
    padding:22px;
}

.profile-stat span{
    color:var(--muted);
    font-size:12px;
}

.profile-stat strong{
    display:block;
    margin-top:7px;
    font-size:20px;
}

/* ABOUT */

.about-box{
    max-width:900px;
    margin:auto;
    background:linear-gradient(145deg,#15151c,#0d0d12);
    border:1px solid var(--border);
    border-radius:25px;
    padding:40px;
}

.about-box p{
    color:#bcbcc5;
    line-height:1.9;
    margin-bottom:18px;
}

/* MODAL */

.modal{
    display:none;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.75);
    backdrop-filter:blur(10px);
    z-index:3000;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.modal.active{
    display:flex;
}

.modal-box{
    width:100%;
    max-width:500px;
    max-height:90vh;
    overflow:auto;
    background:#111116;
    border:1px solid var(--border);
    border-radius:25px;
    padding:30px;
}

.modal-head{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:25px;
}

.close{
    background:none;
    border:0;
    color:#fff;
    font-size:25px;
    cursor:pointer;
}

/* FOOTER */

footer{
    text-align:center;
    padding:30px;
    border-top:1px solid var(--border);
    color:#777;
    font-size:12px;
}

/* RESPONSIVE */

@media(max-width:850px){

    nav{
        height:auto;
        min-height:70px;
        padding:14px 5%;
        align-items:flex-start;
        gap:10px;
    }

    #navLinks{
        justify-content:flex-end;
    }

    .nav-btn{
        padding:7px 8px;
        font-size:12px;
    }

    .home-layout{
        grid-template-columns:1fr;
        padding:45px 0;
    }

    .hero-card{
        height:350px;
    }

    .cards,
    .content-grid,
    .plans,
    .profile-grid{
        grid-template-columns:1fr;
    }

    .plan.featured{
        transform:none;
    }

    .page{
        padding:40px 5%;
    }

    .home-content h1{
        font-size:54px;
    }

    .welcome-box h1{
        font-size:38px;
    }

    .profile-header{
        flex-direction:column;
        text-align:center;
    }
}

@media(max-width:500px){

    .home-content h1{
        font-size:43px;
    }

    .hero-card{
        height:300px;
    }

    .auth-card,
    .about-box,
    .welcome-box{
        padding:25px;
    }

    .chat-form{
        padding:10px;
    }
}
</style>
</head>

<body>

<nav>

    <div class="logo">
        Private<span>Spot</span>
    </div>

    <div id="navLinks"></div>

</nav>


<!-- HOME -->

<section id="home" class="page home-page active">

    <div class="home-layout">

        <div class="home-content">

            <div class="badge">
                ● PRIVATE MEMBERSHIP
            </div>

            <h1>
                Welcome to
                <span>PrivateSpot</span>
            </h1>

            <p>
                A private space where members can explore exclusive
                experiences, connect through private chat and discover
                premium content.
            </p>

            <button
                class="primary-btn"
                onclick="startExploring()">

                Start Exploring →

            </button>

        </div>


        <div class="hero-card">

            <div class="hero-circle"></div>

            <div class="hero-center">
                ✦
            </div>

            <div class="hero-info">

                <div>

                    <strong>
                        Private Experience
                    </strong>

                    <div class="online">
                        ● Members online
                    </div>

                </div>

                <div>
                    🔒
                </div>

            </div>

        </div>

    </div>

</section>


<!-- ABOUT -->

<section id="about" class="page">

    <div class="container">

        <div class="section-title">

            <small>
                About PrivateSpot
            </small>

            <h2>
                A private world made for members.
            </h2>

            <p>
                Explore a more personal and exclusive experience.
            </p>

        </div>


        <div class="about-box">

            <p>
                PrivateSpot is designed as a private membership environment
                where registered members can explore exclusive areas,
                communicate through private chat and choose a membership plan.
            </p>

            <p>
                Create your account, explore the platform and discover
                content that is available to members.
            </p>

            <p>
                Your account gives you access to your personal profile,
                membership plans and private communication area.
            </p>

        </div>

    </div>

</section>


<!-- SIGNUP -->

<section id="signup" class="page">

    <div class="auth-wrapper">

        <div class="auth-card">

            <h2>
                Create Account
            </h2>

            <p>
                Join PrivateSpot and begin exploring.
            </p>

            <form onsubmit="signup(event)">

                <input
                    id="signupName"
                    type="text"
                    placeholder="Full name"
                    required
                >

                <input
                    id="signupEmail"
                    type="email"
                    placeholder="Email address"
                    required
                >

                <input
                    id="signupPassword"
                    type="password"
                    placeholder="Create password"
                    required
                >

                <button
                    class="primary-btn"
                    type="submit">

                    Create Account

                </button>

            </form>

        </div>

    </div>

</section>


<!-- LOGIN -->

<section id="login" class="page">

    <div class="auth-wrapper">

        <div class="auth-card">

            <h2>
                Welcome Back
            </h2>

            <p>
                Login to continue your PrivateSpot experience.
            </p>

            <form onsubmit="login(event)">

                <input
                    id="loginEmail"
                    type="email"
                    placeholder="Email address"
                    required
                >

                <input
                    id="loginPassword"
                    type="password"
                    placeholder="Password"
                    required
                >

                <button
                    class="primary-btn"
                    type="submit">

                    Login

                </button>

            </form>

        </div>

    </div>

</section>


<!-- WELCOME
     THIS PAGE IS SHOWN ONLY ONCE -->

<section id="welcome" class="page">

    <div class="welcome-box">

        <div class="badge">
            ✦ MEMBER AREA
        </div>

        <h1>

            Welcome,
            <span id="welcomeName">
                Guest
            </span>

        </h1>

        <p>
            Your private PrivateSpot experience is ready.
            Explore your account, discover locked content,
            view membership plans and chat privately.
        </p>

        <button
            class="primary-btn"
            onclick="finishWelcome()">

            Continue Exploring →

        </button>

    </div>

</section>


<!-- CONTENT -->

<section id="content" class="page">

    <div class="container">

        <div class="section-title">

            <small>
                Exclusive Area
            </small>

            <h2>
                Locked Content
            </h2>

            <p>
                Some content requires an active membership.
            </p>

        </div>


        <div class="content-grid">

            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    Private Collection
                </h3>

                <p>
                    Members only
                </p>

            </div>


            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    Exclusive Gallery
                </h3>

                <p>
                    Members only
                </p>

            </div>


            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    Premium Updates
                </h3>

                <p>
                    Members only
                </p>

            </div>


            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    Private Videos
                </h3>

                <p>
                    Members only
                </p>

            </div>


            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    Special Releases
                </h3>

                <p>
                    Members only
                </p>

            </div>


            <div class="lock-card">

                <div class="lock-icon">
                    🔒
                </div>

                <h3>
                    VIP Collection
                </h3>

                <p>
                    Members only
                </p>

            </div>

        </div>

    </div>

</section>


<!-- PLANS -->

<section id="plans" class="page">

    <div class="container">

        <div class="section-title">

            <small>
                Membership
            </small>

            <h2>
                Choose Your Access
            </h2>

            <p>
                Select the membership level you want.
            </p>

        </div>


        <div class="plans">


            <!-- REGULAR -->

            <div class="plan">

                <h3>
                    Regular
                </h3>

                <div class="price">
                    $50
                    <small>
                        /month
                    </small>
                </div>

                <ul>

                    <li>
                        Member access
                    </li>

                    <li>
                        Exclusive updates
                    </li>

                    <li>
                        Private chat
                    </li>

                </ul>

                <button
                    class="primary-btn"
                    onclick="openPayment('Regular','$50')">

                    Subscribe

                </button>

            </div>


            <!-- PREMIUM -->

            <div class="plan featured">

                <div class="plan-tag">
                    POPULAR
                </div>

                <h3>
                    Premium
                </h3>

                <div class="price">
                    $100
                    <small>
                        /month
                    </small>
                </div>

                <ul>

                    <li>
                        Premium access
                    </li>

                    <li>
                        Exclusive content
                    </li>

                    <li>
                        Private chat
                    </li>

                    <li>
                        Premium updates
                    </li>

                </ul>

                <button
                    class="primary-btn"
                    onclick="openPayment('Premium','$100')">

                    Subscribe

                </button>

            </div>


            <!-- VIP -->

            <div class="plan">

                <h3>
                    VIP
                </h3>

                <div class="price">
                    $200
                    <small>
                        /month
                    </small>
                </div>

                <ul>

                    <li>
                        VIP access
                    </li>

                    <li>
                        Premium content
                    </li>

                    <li>
                        Private chat
                    </li>

                    <li>
                        VIP updates
                    </li>

                    <li>
                        Priority access
                    </li>

                </ul>

                <button
                    class="primary-btn"
                    onclick="openPayment('VIP','$200')">

                    Subscribe

                </button>

            </div>

        </div>

    </div>

</section>


<!-- CHAT -->

<section id="chat" class="page">

    <div class="container">

        <div class="section-title">

            <small>
                Private Communication
            </small>

            <h2>
                Private Chat
            </h2>

            <p>
                Send a message and receive an automatic response.
            </p>

        </div>


        <div class="chat-shell">

            <div class="chat-header">

                <div class="chat-avatar">
                    ✦
                </div>

                <div>

                    <strong>
                        PrivateSpot Chat
                    </strong>

                    <div class="chat-status">
                        ● Online
                    </div>

                </div>

            </div>


            <div id="chatMessages"></div>


            <div id="telegramHandoff"></div>


            <form
                class="chat-form"
                id="chatForm"
                onsubmit="sendMessage(event)">

                <input
                    id="chatInput"
                    type="text"
                    placeholder="Write a message..."
                    autocomplete="off"
                    required
                >

                <button type="submit">
                    ➤
                </button>

            </form>

        </div>

    </div>

</section>


<!-- PROFILE -->

<section id="profile" class="page">

    <div class="container">

        <div class="section-title">

            <small>
                Your Account
            </small>

            <h2>
                Profile
            </h2>

        </div>


        <div class="profile-header">

            <div
                class="profile-avatar"
                id="profileInitial">

                P

            </div>

            <div>

                <h2 id="profileName">
                    Guest
                </h2>

                <p id="profileEmail">
                    Not logged in
                </p>

            </div>

        </div>


        <div class="profile-grid">

            <div class="profile-stat">

                <span>
                    ACCOUNT STATUS
                </span>

                <strong>
                    Active
                </strong>

            </div>


            <div class="profile-stat">

                <span>
                    MEMBERSHIP
                </span>

                <strong id="profilePlan">
                    No Plan
                </strong>

            </div>


            <div class="profile-stat">

                <span>
                    CHAT STATUS
                </span>

                <strong>
                    Available
                </strong>

            </div>

        </div>

    </div>

</section>


<!-- PAYMENT MODAL -->

<div
    class="modal"
    id="paymentModal">

    <div class="modal-box">

        <div class="modal-head">

            <div>

                <h2>
                    Complete Payment
                </h2>

                <p id="selectedPlanText"></p>

            </div>

            <button
                class="close"
                onclick="closePayment()">

                ×

            </button>

        </div>


        <label>
            Payment Method
        </label>

        <select
            id="paymentMethod"
            onchange="paymentMethodChanged()">

            <option value="bitcoin">
                Bitcoin
            </option>

            <option value="usdt">
                USDT BEP20
            </option>

            <option value="ethereum">
                Ethereum ERC20
            </option>

            <option value="giftcard">
                Gift Card
            </option>

        </select>


        <div id="cryptoBox">

            <p style="color:#aaa;font-size:13px;margin-bottom:8px;">

                Send payment to the wallet address below:

            </p>

            <input
                id="walletAddress"
                readonly
                value="13CVQWXmyHA1YgcH9JDUq7BWkZGfcdKEoN"
            >

            <button
                class="secondary-btn"
                style="width:100%;margin-bottom:15px"
                onclick="copyWallet()">

                Copy Wallet Address

            </button>

        </div>


        <div
            id="giftCardBox"
            style="display:none">

            <label>
                Gift Card Type
            </label>

            <select>

                <option>
                    Amazon
                </option>

                <option>
                    Apple
                </option>

                <option>
                    Google Play
                </option>

                <option>
                    Steam
                </option>

                <option>
                    Other
                </option>

            </select>

        </div>


        <label>
            Upload Payment Screenshot
        </label>

        <input
            type="file"
            accept="image/*"
        >


        <button
            class="primary-btn"
            style="width:100%;margin-top:10px"
            onclick="submitPayment()">

            Submit Payment

        </button>

    </div>

</div>


<footer>

    © 2026 PrivateSpot | Exclusive World

</footer>


<script>

/* STORAGE */

const USER_KEY =
    "privateSpotUser";

const LOGIN_KEY =
    "privateSpotLoggedIn";

const WELCOME_SEEN_KEY =
    "privateSpotWelcomeSeen";

const CHAT_KEY =
    "privateSpotChat";

const MESSAGE_COUNT_KEY =
    "privateSpotMessageCount";

const CHAT_TIMER_KEY =
    "privateSpot15SecondTimerStart";

const TELEGRAM_SHOWN_KEY =
    "privateSpot15SecondTelegramShown";


let timerInterval = null;


/* NAVIGATION */

function buildNavigation(){

    const nav =
        document.getElementById("navLinks");

    nav.innerHTML = "";

    const loggedIn =
        localStorage.getItem(LOGIN_KEY) === "true";


    function addNavButton(text,id){

        const button =
            document.createElement("button");

        button.className =
            "nav-btn";

        button.textContent =
            text;

        button.onclick =
            function(){

                showPage(id);

            };

        nav.appendChild(button);
    }


    if(!loggedIn){

        addNavButton(
            "Login",
            "login"
        );

        addNavButton(
            "Signup",
            "signup"
        );

        addNavButton(
            "About",
            "about"
        );

        addNavButton(
            "Chat",
            "chat"
        );

    }else{

        addNavButton(
            "Home",
            "home"
        );

        addNavButton(
            "About",
            "about"
        );

        addNavButton(
            "Content",
            "content"
        );

        addNavButton(
            "Plans",
            "plans"
        );

        addNavButton(
            "Chat",
            "chat"
        );

        addNavButton(
            "Profile",
            "profile"
        );


        const logout =
            document.createElement("button");

        logout.className =
            "nav-btn logout-btn";

        logout.textContent =
            "Logout";

        logout.onclick =
            logoutUser;

        nav.appendChild(logout);
    }

}


/* PAGE CONTROL */

function showPage(pageId){

    const loggedIn =
        localStorage.getItem(LOGIN_KEY) === "true";


    const publicPages = [

        "home",
        "about",
        "signup",
        "login",
        "chat"

    ];


    if(
        !loggedIn &&
        !publicPages.includes(pageId)
    ){

        pageId = "login";

    }


    document
        .querySelectorAll(".page")
        .forEach(function(page){

            page.classList.remove("active");

        });


    const page =
        document.getElementById(pageId);


    if(page){

        page.classList.add("active");

    }


    if(pageId === "welcome"){

        updateUserDisplay();

    }


    if(pageId === "profile"){

        updateProfile();

    }


    if(pageId === "chat"){

        renderChat();

        resume15SecondTimer();

    }


    window.scrollTo({
        top:0,
        behavior:"smooth"
    });

}


/* START EXPLORING */

function startExploring(){

    const loggedIn =
        localStorage.getItem(LOGIN_KEY) === "true";


    if(!loggedIn){

        showPage("signup");

        return;

    }


    if(
        localStorage.getItem(
            WELCOME_SEEN_KEY
        ) === "true"
    ){

        showPage("content");

    }else{

        showPage("welcome");

    }

}


/* FINISH WELCOME */

function finishWelcome(){

    localStorage.setItem(
        WELCOME_SEEN_KEY,
        "true"
    );


    showPage("home");

}


/* SIGNUP */

function signup(event){

    event.preventDefault();


    const name =
        document
            .getElementById("signupName")
            .value
            .trim();


    const email =
        document
            .getElementById("signupEmail")
            .value
            .trim();


    const password =
        document
            .getElementById("signupPassword")
            .value;


    const user = {

        name:name,

        email:email,

        password:password,

        plan:"No Plan"

    };


    localStorage.setItem(
        USER_KEY,
        JSON.stringify(user)
    );


    localStorage.setItem(
        LOGIN_KEY,
        "true"
    );


    localStorage.removeItem(
        WELCOME_SEEN_KEY
    );


    updateUserDisplay();

    buildNavigation();


    showPage("welcome");


    alert(
        "Account created successfully."
    );

}


/* LOGIN */

function login(event){

    event.preventDefault();


    const email =
        document
            .getElementById("loginEmail")
            .value
            .trim();


    const password =
        document
            .getElementById("loginPassword")
            .value;


    const saved =
        JSON.parse(
            localStorage.getItem(
                USER_KEY
            ) || "null"
        );


    if(
        !saved ||
        saved.email !== email ||
        saved.password !== password
    ){

        alert(
            "Incorrect email or password."
        );

        return;

    }


    localStorage.setItem(
        LOGIN_KEY,
        "true"
    );


    updateUserDisplay();

    buildNavigation();


    if(
        localStorage.getItem(
            WELCOME_SEEN_KEY
        ) !== "true"
    ){

        showPage("welcome");

    }else{

        showPage("home");

    }


    alert(
        "Login successful."
    );

}


/* LOGOUT */

function logoutUser(){

    localStorage.removeItem(
        LOGIN_KEY
    );


    buildNavigation();


    showPage("home");

}


/* USER DISPLAY */

function updateUserDisplay(){

    const user =
        JSON.parse(
            localStorage.getItem(
                USER_KEY
            ) || "null"
        );


    if(!user){

        return;

    }


    document
        .getElementById("welcomeName")
        .textContent =
        user.name;


    document
        .getElementById("profileName")
        .textContent =
        user.name;


    document
        .getElementById("profileEmail")
        .textContent =
        user.email;


    document
        .getElementById("profileInitial")
        .textContent =
        user.name
            .charAt(0)
            .toUpperCase();


    document
        .getElementById("profilePlan")
        .textContent =
        user.plan ||
        "No Plan";

}


/* PROFILE */

function updateProfile(){

    updateUserDisplay();

}


/* CHAT STORAGE */

function getChat(){

    return JSON.parse(
        localStorage.getItem(
            CHAT_KEY
        ) || "[]"
    );

}


function saveChat(messages){

    localStorage.setItem(
        CHAT_KEY,
        JSON.stringify(messages)
    );

}


/* ADD MESSAGE */

function addMessage(sender,text){

    const messages =
        getChat();


    messages.push({

        sender:sender,

        text:text,

        time:Date.now()

    });


    saveChat(messages);


    renderChat();

}


/* RENDER CHAT */

function renderChat(){

    const box =
        document.getElementById(
            "chatMessages"
        );


    if(!box){

        return;

    }


    box.innerHTML = "";


    const messages =
        getChat();


    if(messages.length === 0){

        const welcome =
            document.createElement(
                "div"
            );


        welcome.className =
            "message bot";


        welcome.textContent =
            "Hello 😊 Welcome to PrivateSpot. Send me a message.";


        box.appendChild(
            welcome
        );


        return;

    }


    messages.forEach(
        function(message){

            const div =
                document.createElement(
                    "div"
                );


            div.className =
                "message " +
                (
                    message.sender === "user"
                    ? "user"
                    : "bot"
                );


            div.textContent =
                message.text;


            box.appendChild(
                div
            );

        }
    );


    box.scrollTop =
        box.scrollHeight;

}


/* AUTOMATIC CHAT RESPONSE */

function automaticReply(text){

    const lower =
        text.toLowerCase();


    let response;


    if(
        lower.includes("hello") ||
        lower.includes("hi") ||
        lower.includes("hey")
    ){

        response =
            "Hey 😊 It's nice to hear from you.";

    }

    else if(
        lower.includes("how are you")
    ){

        response =
            "I'm doing well 😊 How are you doing?";

    }

    else if(
        lower.includes("miss") ||
        lower.includes("thinking")
    ){

        response =
            "That's sweet ❤️ Tell me what's on your mind.";

    }

    else if(
        lower.includes("beautiful") ||
        lower.includes("pretty") ||
        lower.includes("gorgeous")
    ){

        response =
            "Aww 😊 Thank you for the compliment.";

    }

    else if(
        lower.includes("love") ||
        lower.includes("like you")
    ){

        response =
            "That's really sweet ❤️";

    }

    else if(
        lower.includes("photo") ||
        lower.includes("picture") ||
        lower.includes("pic")
    ){

        response =
            "Some private content is available to members.";

    }

    else if(
        lower.includes("video")
    ){

        response =
            "Check the membership plans for access to exclusive content.";

    }

    else if(
        lower.includes("subscription") ||
        lower.includes("subscribe") ||
        lower.includes("plan")
    ){

        response =
            "You can view the Regular, Premium and VIP plans in Membership.";

    }

    else if(
        lower.includes("payment") ||
        lower.includes("pay")
    ){

        response =
            "Choose a membership plan and the payment options will appear.";

    }

    else if(
        lower.includes("?")
    ){

        response =
            "That's a good question 😊 Tell me a little more.";

    }

    else{

        const replies = [

            "That's interesting 😊 Tell me more.",

            "I understand. What happened next?",

            "Hmm, tell me more about that ❤️",

            "I'm listening 😊 Keep going.",

            "What made you think about that?",

            "I like hearing from you 😊 Tell me more."

        ];


        response =
            replies[
                Math.floor(
                    Math.random() *
                    replies.length
                )
            ];

    }


    setTimeout(
        function(){

            addMessage(
                "bot",
                response
            );

        },
        700
    );

}


/* SEND CHAT */

function sendMessage(event){

    event.preventDefault();


    const input =
        document.getElementById(
            "chatInput"
        );


    const text =
        input.value.trim();


    if(!text){

        return;

    }


    const messages =
        getChat();


    const userMessageCount =
        messages.filter(
            function(message){

                return message.sender === "user";

            }
        ).length;


    if(
        userMessageCount === 0 &&
        !localStorage.getItem(
            CHAT_TIMER_KEY
        ) &&
        localStorage.getItem(
            TELEGRAM_SHOWN_KEY
        ) !== "true"
    ){

        localStorage.setItem(
            CHAT_TIMER_KEY,
            Date.now().toString()
        );

    }


    addMessage(
        "user",
        text
    );


    input.value = "";


    let count =
        Number(
            localStorage.getItem(
                MESSAGE_COUNT_KEY
            ) || 0
        );


    count++;


    localStorage.setItem(
        MESSAGE_COUNT_KEY,
        count
    );


    resume15SecondTimer();


    automaticReply(text);

}


/* 15 SECOND TIMER */

function resume15SecondTimer(){

    if(
        localStorage.getItem(
            TELEGRAM_SHOWN_KEY
        ) === "true"
    ){

        stop15SecondTimer();

        return;

    }


    const start =
        Number(
            localStorage.getItem(
                CHAT_TIMER_KEY
            ) || 0
        );


    if(!start){

        return;

    }


    if(timerInterval){

        return;

    }


    check15SecondTimer();


    timerInterval =
        setInterval(
            check15SecondTimer,
            250
        );

}


function check15SecondTimer(){

    if(
        localStorage.getItem(
            TELEGRAM_SHOWN_KEY
        ) === "true"
    ){

        stop15SecondTimer();

        return;

    }


    const start =
        Number(
            localStorage.getItem(
                CHAT_TIMER_KEY
            ) || 0
        );


    if(!start){

        stop15SecondTimer();

        return;

    }


    const elapsed =
        Date.now() - start;


    if(elapsed >= 15000){

        stop15SecondTimer();

        showTelegramMessage();

    }

}


function stop15SecondTimer(){

    if(timerInterval){

        clearInterval(
            timerInterval
        );

        timerInterval = null;

    }

}


/* TELEGRAM MESSAGE */

function showTelegramMessage(){

    if(
        localStorage.getItem(
            TELEGRAM_SHOWN_KEY
        ) === "true"
    ){

        return;

    }


    localStorage.setItem(
        TELEGRAM_SHOWN_KEY,
        "true"
    );


    localStorage.removeItem(
        CHAT_TIMER_KEY
    );


    addMessage(
        "bot",
        "You can continue the conversation in the live chat."
    );


    showTelegramHandoff();

}


/* TELEGRAM HANDOFF */

function showTelegramHandoff(){

    const existing =
        document.querySelector(
            ".handoff-box"
        );


    if(existing){

        return;

    }


    const wrapper =
        document.createElement(
            "div"
        );


    wrapper.className =
        "handoff-box";


    const title =
        document.createElement(
            "strong"
        );


    title.textContent =
        "Continue in Live Chat";


    const text =
        document.createElement(
            "p"
        );


    text.textContent =
        "Continue your conversation through the private live chat.";


    text.style.color =
        "#aaa";


    text.style.marginTop =
        "7px";


    const link =
        document.createElement(
            "a"
        );


    link.href =
        "https://t.me/sexy_sexy_x";


    link.target =
        "_blank";


    link.rel =
        "noopener noreferrer";


    link.textContent =
        "💬 Continue to Telegram";


    wrapper.appendChild(
        title
    );


    wrapper.appendChild(
        text
    );


    wrapper.appendChild(
        link
    );


    const form =
        document.getElementById(
            "chatForm"
        );


    form.parentNode.insertBefore(
        wrapper,
        form
    );

}


/* PAYMENT */

let selectedPlan = "";


function openPayment(plan,price){

    selectedPlan =
        plan;


    document.getElementById(
        "selectedPlanText"
    ).textContent =
        plan +
        " Membership — " +
        price;


    document.getElementById(
        "paymentModal"
    ).classList.add(
        "active"
    );

}


function closePayment(){

    document.getElementById(
        "paymentModal"
    ).classList.remove(
        "active"
    );

}


function paymentMethodChanged(){

    const method =
        document.getElementById(
            "paymentMethod"
        ).value;


    const crypto =
        document.getElementById(
            "cryptoBox"
        );


    const gift =
        document.getElementById(
            "giftCardBox"
        );


    if(method === "giftcard"){

        crypto.style.display =
            "none";

        gift.style.display =
            "block";

    }

    else{

        crypto.style.display =
            "block";

        gift.style.display =
            "none";


        const wallet =
            document.getElementById(
                "walletAddress"
            );


        if(method === "bitcoin"){

            wallet.value =
                "13CVQWXmyHA1YgcH9JDUq7BWkZGfcdKEoN";

        }

        else{

            wallet.value =
                "0x2d1a039b1b44f2605c055d2cc67a3b08f5127457";

        }

    }

}


function copyWallet(){

    const wallet =
        document.getElementById(
            "walletAddress"
        );


    navigator.clipboard.writeText(
        wallet.value
    );


    alert(
        "Wallet address copied."
    );

}


function submitPayment(){

    const user =
        JSON.parse(
            localStorage.getItem(
                USER_KEY
            ) || "null"
        );


    if(user){

        user.plan =
            selectedPlan;


        localStorage.setItem(
            USER_KEY,
            JSON.stringify(user)
        );

    }


    closePayment();


    updateProfile();


    alert(
        "Payment information submitted. Your membership status can be verified by the administrator."
    );

}


/* INITIALIZE */

buildNavigation();


if(
    localStorage.getItem(
        LOGIN_KEY
    ) === "true"
){

    updateUserDisplay();

}


renderChat();


if(
    localStorage.getItem(
        TELEGRAM_SHOWN_KEY
    ) === "true"
){

    setTimeout(
        showTelegramHandoff,
        100
    );

}


resume15SecondTimer();


if(
    localStorage.getItem(
        LOGIN_KEY
    ) === "true"
){

    if(
        localStorage.getItem(
            WELCOME_SEEN_KEY
        ) === "true"
    ){

        showPage("home");

    }else{

        showPage("welcome");

    }

}

</script>

</body>
</html>
