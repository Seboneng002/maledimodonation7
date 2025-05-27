<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Help a Student Hold On to Hope - #helpboseborsa</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #f0f4f8 0%, #e8f0fe 100%);
      font-family: 'Georgia', serif;
      color: #333;
      margin: 0;
      padding: 0;
      line-height: 1.8;
    }

    .container {
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      background: #fff;
      box-shadow: 0 8px 32px rgba(0,0,0,0.1);
      border-radius: 16px;
    }

    .header {
      text-align: center;
      margin-bottom: 30px;
    }

    h1 {
      color: #5c3d2e;
      margin-bottom: 10px;
      font-size: clamp(24px, 4vw, 36px);
    }

    h2 {
      color: #7c574d;
      font-weight: normal;
      margin-top: 0;
      font-size: clamp(16px, 3vw, 20px);
    }

    .student-profile {
      display: flex;
      gap: 20px;
      margin-bottom: 30px;
      padding: 20px;
      background: #f8f9fa;
      border-radius: 12px;
      flex-wrap: wrap;
    }

    .student-photo {
      width: 150px;
      height: 150px;
      background: linear-gradient(45deg, #639a67, #7c574d);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 60px;
      flex-shrink: 0;
      margin: 0 auto;
    }

    .student-info {
      flex: 1;
      min-width: 250px;
    }

    .student-details {
      background: white;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
    }

    .student-details h3 {
      margin: 0 0 10px 0;
      color: #5c3d2e;
    }

    .student-details p {
      margin: 5px 0;
      font-size: 16px;
    }

    .progress-section {
      background: #fff;
      padding: 25px;
      border-radius: 12px;
      margin: 25px 0;
      border: 2px solid #e9ecef;
    }

    .progress-bar {
      width: 100%;
      height: 20px;
      background: #e9ecef;
      border-radius: 10px;
      overflow: hidden;
      margin: 15px 0;
    }

    .progress-fill {
      height: 100%;
      background: linear-gradient(90deg, #639a67, #4a7c59);
      width: 8.75%;
      border-radius: 10px;
      transition: width 0.3s ease;
    }

    .progress-text {
      display: flex;
      justify-content: space-between;
      font-weight: bold;
      color: #5c3d2e;
    }

    .donation-amounts {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 15px;
      margin: 25px 0;
    }

    .amount-btn {
      padding: 15px;
      border: 2px solid #639a67;
      background: white;
      color: #639a67;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.3s;
      text-align: center;
      font-size: 18px;
      font-weight: bold;
    }

    .amount-btn:hover, .amount-btn.active {
      background: #639a67;
      color: white;
      transform: translateY(-2px);
    }

    .custom-amount {
      grid-column: 1 / -1;
      display: flex;
      gap: 10px;
      align-items: center;
      margin-top: 15px;
    }

    .custom-amount input {
      padding: 12px;
      border: 2px solid #ddd;
      border-radius: 6px;
      font-size: 16px;
      flex: 1;
    }

    .impact-statement {
      background: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      margin: 20px 0;
      border-left: 4px solid #639a67;
    }

    .impact-statement h4 {
      margin: 0 0 10px 0;
      color: #5c3d2e;
    }

    .donate-btn, .btn {
      display: block;
      margin: 30px auto;
      padding: 18px 40px;
      background: linear-gradient(45deg, #639a67, #4a7c59);
      color: white;
      text-decoration: none;
      border-radius: 8px;
      font-size: 20px;
      text-align: center;
      transition: all 0.3s;
      border: none;
      cursor: pointer;
      width: 100%;
      max-width: 400px;
    }

    .donate-btn:hover, .btn:hover {
      transform: scale(1.03);
      box-shadow: 0 10px 20px rgba(99, 154, 103, 0.3);
    }

    .share-section {
      text-align: center;
      margin: 30px 0;
    }

    .share-buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 15px;
      flex-wrap: wrap;
    }

    .share-btn {
      padding: 12px 20px;
      border-radius: 6px;
      color: white;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 8px;
      transition: transform 0.3s;
    }

    .share-btn:hover {
      transform: translateY(-2px);
    }

    .share-btn.whatsapp { background: #25D366; }
    .share-btn.facebook { background: #1877F2; }
    .share-btn.twitter { background: #1DA1F2; }

    .security-badges {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 20px 0;
      flex-wrap: wrap;
    }

    .security-badge {
      display: flex;
      align-items: center;
      gap: 8px;
      color: #666;
      font-size: 14px;
    }

    .testimonial {
      background: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      margin: 20px 0;
      border-left: 4px solid #c9a27e;
      font-style: italic;
    }

    .contact-info {
      background: #e8f0fe;
      padding: 15px;
      border-radius: 8px;
      margin: 20px 0;
      text-align: center;
    }

    .urgency-banner {
      background: linear-gradient(45deg, #ff6b6b, #ee5a52);
      color: white;
      padding: 15px;
      text-align: center;
      border-radius: 8px;
      margin-bottom: 20px;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.02); }
    }

    .thank-you-page {
      display: none;
      text-align: center;
      padding: 40px 20px;
    }

    .thank-you-page.show {
      display: block;
    }

    .thank-you-letter {
      background: #f8f9fa;
      padding: 30px;
      border-radius: 12px;
      margin: 20px 0;
      border: 2px solid #639a67;
      text-align: left;
    }

    .letter-header {
      text-align: center;
      margin-bottom: 30px;
      color: #5c3d2e;
    }

    .signature {
      text-align: right;
      margin-top: 30px;
      font-style: italic;
    }

    .bank-details {
      background: #e8f5e8;
      border: 2px solid #639a67;
      border-radius: 8px;
      padding: 20px;
      margin: 20px 0;
      text-align: center;
    }

    .bank-details h3 {
      color: #5c3d2e;
      margin-top: 0;
    }

    .notification {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #639a67;
      color: white;
      padding: 15px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      transform: translateX(400px);
      transition: transform 0.3s ease;
      z-index: 1000;
    }

    .notification.show {
      transform: translateX(0);
    }

    .stats-widget {
      background: linear-gradient(135deg, #639a67, #4a7c59);
      color: white;
      padding: 20px;
      border-radius: 12px;
      margin: 20px 0;
      text-align: center;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
      margin-top: 15px;
    }

    .stat-item h4 {
      margin: 0 0 5px 0;
      font-size: 24px;
    }

    .stat-item p {
      margin: 0;
      opacity: 0.9;
    }

    .countdown-timer {
      background: #fff3cd;
      border: 2px solid #ffeaa7;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      margin: 20px 0;
    }

    .timer-display {
      font-size: 24px;
      font-weight: bold;
      color: #856404;
      margin: 10px 0;
    }

    .faq-section {
      background: #f8f9fa;
      padding: 25px;
      border-radius: 12px;
      margin: 25px 0;
    }

    .faq-item {
      margin: 15px 0;
      border-bottom: 1px solid #dee2e6;
      padding-bottom: 15px;
    }

    .faq-question {
      font-weight: bold;
      color: #5c3d2e;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .faq-answer {
      margin-top: 10px;
      display: none;
      color: #666;
    }

    .faq-answer.show {
      display: block;
    }

    footer {
      text-align: center;
      margin-top: 50px;
      font-size: 14px;
      color: #888;
      border-top: 1px solid #eee;
      padding-top: 20px;
    }

    @media (max-width: 768px) {
      .container {
        margin: 10px;
        padding: 15px;
      }
      
      .student-profile {
        flex-direction: column;
        text-align: center;
      }
      
      .donation-amounts {
        grid-template-columns: repeat(2, 1fr);
      }
      
      .share-buttons {
        flex-direction: column;
        align-items: center;
      }

      .notification {
        right: 10px;
        left: 10px;
        transform: translateY(-100px);
      }

      .notification.show {
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

<div class="notification" id="notification">
  <i class="fas fa-check-circle"></i>
  <span id="notification-text">Thank you for your support!</span>
</div>

<div class="container" id="main-content">
  <div class="urgency-banner">
    <i class="fas fa-clock"></i> Help Clifford reach his goal before semester fees are due!
  </div>

  <div class="header">
    <h1>Hold On, Clifford</h1>
    <h2>A letter to anyone who's ever struggled to believe tomorrow will be better</h2>
  </div>

  <div class="countdown-timer">
    <h4><i class="fas fa-hourglass-half"></i> Time Until Semester Fees Due</h4>
    <div class="timer-display" id="countdown">45 days remaining</div>
    <p>Every day counts - help Clifford secure his education!</p>
  </div>

  <div class="student-profile">
    <div class="student-photo">
      <i class="fas fa-user-graduate"></i>
    </div>
    <div class="student-info">
      <h3>Meet Clifford</h3>
      <p>A dedicated student who believes that education can change lives. Despite financial hardships, Clifford maintains hope and works tirelessly toward his dream of becoming a teacher.</p>
      
      <div class="student-details">
        <h3><i class="fas fa-graduation-cap"></i> Student Details</h3>
        <p><strong>Course:</strong> Bachelor of Education</p>
        <p><strong>University:</strong> University Of Western Cape</p>
        <p><strong>Year:</strong> 1st Year</p>
        <p><strong>Goal:</strong> Become a life-changing educator</p>
      </div>
    </div>
  </div>

  <div class="stats-widget">
    <h3><i class="fas fa-chart-line"></i> Campaign Impact</h3>
    <div class="stats-grid">
      <div class="stat-item">
        <h4 id="donor-count">47</h4>
        <p>Kind Donors</p>
      </div>
      <div class="stat-item">
        <h4 id="days-left">45</h4>
        <p>Days Remaining</p>
      </div>
      <div class="stat-item">
        <h4 id="share-count">123</h4>
        <p>Times Shared</p>
      </div>
    </div>
  </div>

  <div class="progress-section">
    <h3><i class="fas fa-target"></i> Fundraising Progress</h3>
    <div class="progress-text">
      <span>R<span id="current-amount">875</span> raised</span>
      <span>R<span id="goal-amount">10000</span> goal</span>
    </div>
    <div class="progress-bar">
      <div class="progress-fill" id="progress-fill"></div>
    </div>
    <p style="text-align: center; color: #666;">
      <span id="progress-percentage">8.75</span>% of goal reached • 
      <span id="donor-count-text">47</span> generous donors
    </p>
  </div>

  <p>
    This page is not just about money. It is about belief—belief that even in a world that often forgets the quiet strugglers,
    there are still people who care.
  </p>

  <p>
    Clifford is a student—quiet, kind, thoughtful. 
    He studies Bachelor of Education not just to get a job, 
    but because he believes that a teacher is a life changer who 
    transforms lives and builds better futures.
    He stays up late reading borrowed books. He eats one meal a 
    day so he can save for tuition. Not because anyone told him 
    to—but because he dreams. I also tried student financial aid and all the help that 
    is offered on campus by the institution but all takes time to be processed and being approved but 
    since i know that i am from a country where you dont face the problem alone but with fellow citizens i reached and still reaching 
    for whatever help i can get take me as you would take your relative in need as we do know who might face the
    problems in the future and i further say         
  </p>

  <div class="impact-statement">
    <h4><i class="fas fa-heart"></i> Your Impact</h4>
    <p><strong>R10</strong> - Provides a nutritious meal for one day</p>
    <p><strong>R50</strong> - Covers weekly transportation to university</p>
    <p><strong>R100</strong> - Helps with textbook rental and laptop purchase</p>
    <p><strong>R250</strong> - Contributes significantly to monthly groceries</p>
  </div>

  <div class="donation-amounts">
    <div class="amount-btn" onclick="selectAmount(10)">R10</div>
    <div class="amount-btn" onclick="selectAmount(25)">R25</div>
    <div class="amount-btn" onclick="selectAmount(50)">R50</div>
    <div class="amount-btn" onclick="selectAmount(100)">R100</div>
    <div class="amount-btn" onclick="selectAmount(250)">R250</div>
    <div class="amount-btn" onclick="selectAmount(500)">R500</div>
    
    <div class="custom-amount">
      <span>Custom amount: R</span>
      <input type="number" id="customAmount" placeholder="Enter amount" min="1">
      <button onclick="selectCustomAmount()" style="padding: 12px 20px; background: #639a67; color: white; border: none; border-radius: 6px; cursor: pointer;">Select</button>
    </div>
  </div>

  <div class="testimonial">
    <p>"Sometimes I look up at the ceiling at night and wonder if anyone sees how hard I'm trying. I don't want pity. I just don't want to give up yet."</p>
    <p style="text-align: right; margin-top: 15px; font-weight: bold;">— Clifford</p>
  </div>

  <p>
    If you've ever been in that place—where you didn't know how to ask for help, where every small act of kindness felt like a lifeline—
    then you already understand what this page is about.
  </p>

  <a href="https://pay.capitecbank.co.za/payme/EF666I" class="donate-btn" target="_blank" onclick="trackDonation()">
    <i class="fas fa-heart"></i> Send Support Now
  </a>

  <div class="bank-details">
    <h3><i class="fas fa-university"></i> Alternative Payment Method</h3>
    <p><strong>Bank:</strong> Capitec Bank</p>
    <p><strong>Account Holder:</strong> Mr SC BAPELA</p>
    <p><strong>Account Number:</strong> 2094927136</p>
    <p><em>Please use "HelpClifford" as reference</em></p>
    <button onclick="copyBankDetails()" class="btn" style="background: #7c574d; margin-top: 15px; font-size: 16px; padding: 10px 20px;">
      <i class="fas fa-copy"></i> Copy Bank Details
    </button>
  </div>

  <div class="security-badges">
    <div class="security-badge">
      <i class="fas fa-shield-alt"></i>
      <span>Secure Payment</span>
    </div>
    <div class="security-badge">
      <i class="fas fa-lock"></i>
      <span>SSL Protected</span>
    </div>
    <div class="security-badge">
      <i class="fas fa-check-circle"></i>
      <span>Verified Student</span>
    </div>
  </div>

  <div class="faq-section">
    <h3><i class="fas fa-question-circle"></i> Frequently Asked Questions</h3>
    
    <div class="faq-item">
      <div class="faq-question" onclick="toggleFAQ(0)">
        How do I know my donation will reach Clifford?
        <i class="fas fa-chevron-down"></i>
      </div>
      <div class="faq-answer">
        All donations go directly to Clifford's verified bank account. We provide regular updates on how funds are being used for education expenses.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question" onclick="toggleFAQ(1)">
        Is my donation tax-deductible?
        <i class="fas fa-chevron-down"></i>
      </div>
      <div class="faq-answer">
        This is a personal fundraiser, so donations may not be tax-deductible. Please consult your tax advisor for specific guidance.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question" onclick="toggleFAQ(2)">
        Can I get updates on Clifford's progress?
        <i class="fas fa-chevron-down"></i>
      </div>
      <div class="faq-answer">
        Yes! Send us your email after donating, and we'll include you in our update list. You'll receive progress reports and thank you messages.
      </div>
    </div>
  </div>

  <div class="share-section">
    <h3>Help Spread the Word</h3>
    <p>Share Clifford's story and help us reach more kind hearts</p>
    <div class="share-buttons">
      <a href="#" class="share-btn whatsapp" onclick="shareOnWhatsApp()">
        <i class="fab fa-whatsapp"></i>
        WhatsApp
      </a>
      <a href="#" class="share-btn facebook" onclick="shareOnFacebook()">
        <i class="fab fa-facebook"></i>
        Facebook
      </a>
      <a href="#" class="share-btn twitter" onclick="shareOnTwitter()">
        <i class="fab fa-twitter"></i>
        Twitter
      </a>
    </div>
  </div>

  <div class="contact-info">
    <h4><i class="fas fa-envelope"></i> Questions or Want Updates?</h4>
    <p>Email: sebonengcliffordbapela@gmail.com<br> Student email: 4506432@myuwc.ac.za</p>
    <p>We'll send you updates on how your donation is making a difference!</p>
  </div>

  <div style="text-align: center; margin: 30px 0;">
    <button class="btn" onclick="showThankYou()">
      <i class="fas fa-envelope-open"></i> Read Thank You Letter
    </button>
  </div>

  <footer>
    Your kindness is a light someone else is waiting for. Thank you for reading.
  </footer>
</div>

<!-- Thank You Page -->
<div class="container thank-you-page" id="thank-you-content">
  <div class="header">
    <h1><i class="fas fa-heart" style="color: #639a67;"></i> Thank You!</h1>
    <h2>Your generosity means the world to Clifford</h2>
  </div>

  <div class="thank-you-letter" id="thank-you-letter">
    <div class="letter-header">
      <h3>A Personal Thank You Letter</h3>
      <p><em>From Clifford's Heart to Yours</em></p>
    </div>

    <p>Dear Kind Soul,</p>

    <p>Words cannot express how grateful I am for your generous support. In a world where it's easy to scroll past someone's struggles, you chose to stop, read my story, and extend a helping hand.</p>

    <p>Your contribution will directly help me with:</p>
    <ul>
      <li>Purchasing necessary textbooks and study materials</li>
      <li>Covering transportation costs to attend lectures</li>
      <li>Ensuring I have proper meals to maintain my health and focus</li>
      <li>Paying for essential academic resources and assignments</li>
    </ul>

    <p>But beyond the financial help, you've given me something even more precious—hope. You've shown me that there are still people who believe in dreams, who support struggles they've never experienced personally, and who choose kindness over indifference.</p>

    <p>I promise you that every rand will be used wisely and purposefully. As I sit in lecture halls that your generosity helped me reach, I'll remember that I'm not just studying for myself, but carrying the hopes and kindness of people like you.</p>

    <p>When I become a teacher and stand in front of my first classroom, I'll tell my students about the stranger who believed in education enough to support a dream they'd never benefit from directly. I'll teach them that kindness creates ripples that travel far beyond what we can see.</p>

    <p>Your support today is creating teachers, changing lives, and building a better tomorrow.</p>

    <p>Thank you for seeing me, believing in me, and choosing to help.</p>

    <div class="signature">
      <p>With endless gratitude and determination,</p>
      <p><strong>Clifford</strong></p>
      <p><em>Future Educator, Current Dreamer</em></p>
    </div>
  </div>

  <div style="text-align: center; margin: 30px 0;">
    <p><strong>Letter Date:</strong> <span id="letter-date"></span></p>
  </div>

  <div style="text-align: center;">
    <button onclick="downloadLetter()" class="btn" style="margin: 10px;">
      <i class="fas fa-download"></i> Download This Letter
    </button>
    <button onclick="showMainContent()" class="btn" style="background: #7c574d; margin: 10px;">
      <i class="fas fa-arrow-left"></i> Back to Main Page
    </button>
  </div>
</div>

<script>
let selectedAmount = 0;
let currentAmount = 875;
let goalAmount = 10000;
let donorCount = 47;
let shareCount = 123;

// Initialize page
document.addEventListener('DOMContentLoaded', function() {
  updateProgress();
  startCountdown();
  animateStats();
});

function selectAmount(amount) {
  selectedAmount = amount;
  document.querySelectorAll('.amount-btn').forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');
  document.getElementById('customAmount').value = '';
  
  // Show impact message
  showNotification(`You selected R${amount}. Thank you for your kindness!`);
}

function selectCustomAmount() {
  const customAmount = document.getElementById('customAmount').value;
  if (customAmount && customAmount > 0) {
    selectedAmount = parseInt(customAmount);
    document.querySelectorAll('.amount-btn').forEach(btn => btn.classList.remove('active'));
    showNotification(`You selected R${customAmount}. Thank you for your generosity!`);
  } else {
    showNotification('Please enter a valid amount', 'error');
  }
}

function updateProgress() {
  const percentage = (currentAmount / goalAmount * 100).toFixed(2);
  document.getElementById('current-amount').textContent = currentAmount;
  document.getElementById('goal-amount').textContent = goalAmount;
  document.getElementById('progress-percentage').textContent = percentage;
  document.getElementById('donor-count-text').textContent = donorCount;
  document.getElementById('progress-fill').style.width = percentage + '%';
}

function animateStats() {
  // Animate the stats numbers
  const statsItems = [
    { element: 'donor-count', target: donorCount },
    { element: 'days-left', target: 45 },
    { element: 'share-count', target: shareCount }
  ];
  
  statsItems.forEach(stat => {
    animateNumber(stat.element, 0, stat.target, 2000);
  });
}

function animateNumber(elementId, start, end, duration) {
  const element = document.getElementById(elementId);
  const range = end - start;
  const increment = range / (duration / 16);
  let current = start;
  
  const timer = setInterval(() => {
    current += increment;
    if (current >= end) {
      current = end;
      clearInterval(timer);
    }
    element.textContent = Math.floor(current);
  }, 16);
}

function startCountdown() {
  const semesterDate = new Date();
  semesterDate.setDate(semesterDate.getDate() + 45);
  
  function updateCountdown() {
    const now = new Date().getTime();
    const distance = semesterDate.getTime() - now;
    
    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    
    if (days > 0) {
      document.getElementById('countdown').textContent = `${days} days and ${hours} hours remaining`;
      document.getElementById('days-left').textContent = days;
    } else {
      document.getElementById('countdown').textContent = 'Time is up!';
    }
  }
  
  updateCountdown();
  setInterval(updateCountdown, 1000 * 60 * 60); // Update every hour
}

function showNotification(message, type = 'success') {
  const notification = document.getElementById('notification');
  const notificationText = document.getElementById('notification-text');
  
  notificationText.textContent = message;
  
  if (type === 'error') {
    notification.style.background = '#dc3545';
  } else {
    notification.style.background = '#639a67';
  }
  
  notification.classList.add('show');
  
  setTimeout(() => {
    notification.classList.remove('show');
  }, 3000);
}

function showThankYou() {
  document.getElementById('main-content').style.display = 'none';
  document.getElementById('thank-you-content').classList.add('show');
  document.getElementById('letter-date').textContent = new Date().toLocaleDateString();
  window.scrollTo(0, 0);
}

function showMainContent() {
  document.getElementById('main-content').style.display = 'block';
  document.getElementById('thank-you-content').classList.remove('show');
  window.scrollTo(0, 0);
}

function downloadLetter() {
  const letterContent = document.querySelector('.thank-you-letter').innerHTML;
  const fullContent = `
    <!DOCTYPE html>
    <html>
    <head>
      <title>Thank You Letter from Clifford</title>
      <style>
        body { font-family: Georgia, serif; line-height: 1.6; padding: 40px; max-width: 800px; margin: 0 auto; }
        h3 { color: #5c3d2e; text-align: center; }
        .signature { text-align: right; margin-top: 30px; font-style: italic; }
        ul { margin: 20px 0; }
        li { margin: 5px 0; }
      </style>
    </head>
    <body>
      ${letterContent}
      <hr style="margin: 40px 0;">
      <p style="text-align: center; color: #666; font-size: 14px;">
        Generated on ${new Date().toLocaleDateString()}
      </p>
    </body>
    </html>
  `;
  
  const blob = new Blob([fullContent], { type: 'text/html' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = `Thank_You_Letter_Clifford_${new Date().toISOString().split('T')[0]}.html`;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  URL.revokeObjectURL(url);
}

function copyBankDetails() {
  const bankDetails = `Bank: Capitec Bank
Account Holder: Mr SC BAPELA
Account Number: 2094927136
Reference: HelpClifford`;
  
  navigator.clipboard.writeText(bankDetails).then(() => {
    showNotification('Bank details copied to clipboard!');
  }).catch(() => {
    showNotification('Could not copy bank details. Please copy manually.', 'error');
  });
}

function trackDonation() {
  showNotification('Thank you for clicking donate! Your kindness means everything.');
  
  // Simulate donation tracking (in real app, this would be server-side)
  setTimeout(() => {
    if (selectedAmount > 0) {
      currentAmount += selectedAmount;
      donorCount += 1;
      updateProgress();
      showNotification(`Thank you for your R${selectedAmount} donation!`);
    }
  }, 2000);
}

function toggleFAQ(index) {
  const faqItems = document.querySelectorAll('.faq-item');
  const answer = faqItems[index].querySelector('.faq-answer');
  const icon = faqItems[index].querySelector('.fas');
  
  if (answer.classList.contains('show')) {
    answer.classList.remove('show');
    icon.classList.remove('fa-chevron-up');
    icon.classList.add('fa-chevron-down');
  } else {
    // Close all other FAQs
    document.querySelectorAll('.faq-answer').forEach(ans => ans.classList.remove('show'));
    document.querySelectorAll('.faq-question .fas').forEach(ic => {
      ic.classList.remove('fa-chevron-up');
      ic.classList.add('fa-chevron-down');
    });
    
    // Open clicked FAQ
    answer.classList.add('show');
    icon.classList.remove('fa-chevron-down');
    icon.classList.add('fa-chevron-up');
  }
}

function shareOnWhatsApp() {
  const message = encodeURIComponent("Help Clifford, a dedicated education student, reach his dreams! Every contribution matters. #helpboseborsa");
  window.open(`https://wa.me/?text=${message}`, '_blank');
  shareCount += 1;
  document.getElementById('share-count').textContent = shareCount;
  showNotification('Thank you for sharing on WhatsApp!');
}

function shareOnFacebook() {
  const url = encodeURIComponent(window.location.href);
  window.open(`https://www.facebook.com/sharer/sharer.php?u=${url}`, '_blank');
  shareCount += 1;
  document.getElementById('share-count').textContent = shareCount;
  showNotification('Thank you for sharing on Facebook!');
}

function shareOnTwitter() {
  const message = encodeURIComponent("Help Clifford achieve his education dreams! Every contribution makes a difference. #EducationMatters #HelpAStudent #helpboseborsa");
  const url = encodeURIComponent(window.location.href);
  window.open(`https://twitter.com/intent/tweet?text=${message}&url=${url}`, '_blank');
  shareCount += 1;
  document.getElementById('share-count').textContent = shareCount;
  showNotification('Thank you for sharing on Twitter!');
}

// Animate progress bar on page load
window.addEventListener('load', function() {
  setTimeout(() => {
    document.querySelector('.progress-fill').style.width = (currentAmount / goalAmount * 100) + '%';
  }, 500);
});
</script>

</body>
</html>
