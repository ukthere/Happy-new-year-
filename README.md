<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy New Year 2026</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0a0a2a 0%, #1a1a3a 50%, #2a1a3a 100%);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
            perspective: 1000px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 2;
        }
        
        /* 3D Photo Background */
        .photo-3d-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
            transform-style: preserve-3d;
        }
        
        .photo-3d {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 120%;
            height: 120%;
            background-image: url('https://images.unsplash.com/photo-1540959733332-eab4deabeeaf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1494&q=80');
            background-size: cover;
            background-position: center;
            transform: translate(-50%, -50%) rotateX(10deg) rotateY(-5deg) scale(1.2);
            filter: brightness(0.7) saturate(1.2);
            animation: float3d 20s infinite ease-in-out;
            box-shadow: 
                0 0 100px rgba(0, 255, 255, 0.2),
                0 0 60px rgba(255, 215, 0, 0.1) inset;
        }
        
        .photo-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, transparent 30%, rgba(10, 10, 40, 0.9) 70%);
            z-index: 1;
        }
        
        /* Handwriting Style Text */
        .handwriting-container {
            text-align: center;
            padding: 60px 20px;
            position: relative;
            z-index: 3;
            margin-top: 80px;
        }
        
        .handwriting-text {
            font-family: 'Dancing Script', cursive;
            font-size: 6.5rem;
            font-weight: 700;
            color: #fff;
            text-shadow: 
                0 0 20px rgba(255, 215, 0, 0.8),
                0 0 40px rgba(255, 87, 51, 0.5),
                0 5px 15px rgba(0, 0, 0, 0.5);
            line-height: 1.1;
            margin-bottom: 30px;
            position: relative;
            display: inline-block;
            animation: handwriting 3s ease-out;
        }
        
        .handwriting-text::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 10%;
            width: 80%;
            height: 5px;
            background: linear-gradient(90deg, transparent, #ffd700, #ff5733, transparent);
            border-radius: 5px;
            animation: lineDraw 3s ease-out;
        }
        
        /* Additional decorative text */
        .subtitle {
            font-family: 'Poppins', sans-serif;
            font-size: 1.8rem;
            font-weight: 300;
            letter-spacing: 3px;
            margin-bottom: 50px;
            text-transform: uppercase;
            color: rgba(255, 255, 255, 0.9);
            text-shadow: 0 0 15px rgba(0, 255, 255, 0.5);
        }
        
        /* Creator attribution - positioned on right side */
        .creator-attribution {
            position: fixed;
            top: 50%;
            right: 30px;
            transform: translateY(-50%) rotate(90deg);
            transform-origin: right top;
            z-index: 10;
            text-align: right;
            padding: 15px 20px;
            background: rgba(10, 10, 40, 0.7);
            border-radius: 10px;
            backdrop-filter: blur(5px);
            border-left: 3px solid #ffd700;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            animation: slideInRight 2s ease-out 1s both;
        }
        
        .creator-text {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            font-size: 1.2rem;
            color: #fff;
            letter-spacing: 1px;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .creator-name {
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            font-size: 1.3rem;
        }
        
        .creator-icon {
            color: #ff5733;
            font-size: 1.4rem;
        }
        
        /* Decorative elements */
        .decorations {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        
        .decoration-item {
            font-size: 2.5rem;
            animation: bounce 2s infinite ease-in-out;
        }
        
        .decoration-item:nth-child(2) {
            animation-delay: 0.2s;
            color: #ffd700;
        }
        
        .decoration-item:nth-child(3) {
            animation-delay: 0.4s;
            color: #ff5733;
        }
        
        .decoration-item:nth-child(4) {
            animation-delay: 0.6s;
            color: #33ff57;
        }
        
        .decoration-item:nth-child(5) {
            animation-delay: 0.8s;
            color: #5733ff;
        }
        
        /* Year display - UPDATED TO 2026 */
        .year-container {
            margin-top: 50px;
            font-size: 8rem;
            font-weight: 700;
            color: rgba(255, 255, 255, 0.9);
            text-shadow: 
                0 0 30px rgba(255, 215, 0, 0.7),
                0 0 60px rgba(255, 87, 51, 0.5),
                0 0 90px rgba(51, 153, 255, 0.4);
            font-family: 'Poppins', sans-serif;
            letter-spacing: 10px;
            position: relative;
            display: inline-block;
            animation: glow 4s infinite alternate, numberChange 2s ease-out;
        }
        
        .year-container::before, .year-container::after {
            content: '';
            position: absolute;
            top: 50%;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 215, 0, 0.7);
            transform: translateY(-50%);
        }
        
        .year-container::before {
            left: -60px;
            animation: sparkle 1.5s infinite;
        }
        
        .year-container::after {
            right: -60px;
            animation: sparkle 1.5s infinite reverse;
        }
        
        /* New year celebration animation */
        .year-change {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: transparent;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 3rem;
            color: #ffd700;
            animation: celebrate 3s ease-out;
            opacity: 0;
            pointer-events: none;
        }
        
        /* Footer */
        .footer {
            text-align: center;
            margin-top: 80px;
            padding: 20px;
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.7);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            z-index: 3;
        }
        
        /* Animations */
        @keyframes float3d {
            0%, 100% {
                transform: translate(-50%, -50%) rotateX(10deg) rotateY(-5deg) scale(1.2);
            }
            50% {
                transform: translate(-50%, -50%) rotateX(12deg) rotateY(5deg) scale(1.25);
            }
        }
        
        @keyframes handwriting {
            0% {
                opacity: 0;
                transform: translateY(50px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes lineDraw {
            0% {
                width: 0;
                left: 50%;
            }
            100% {
                width: 80%;
                left: 10%;
            }
        }
        
        @keyframes slideInRight {
            0% {
                right: -200px;
                opacity: 0;
            }
            100% {
                right: 30px;
                opacity: 1;
            }
        }
        
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        
        @keyframes glow {
            0% {
                text-shadow: 
                    0 0 30px rgba(255, 215, 0, 0.7),
                    0 0 60px rgba(255, 87, 51, 0.5);
            }
            100% {
                text-shadow: 
                    0 0 40px rgba(255, 215, 0, 0.9),
                    0 0 80px rgba(255, 87, 51, 0.7),
                    0 0 100px rgba(51, 255, 87, 0.4);
            }
        }
        
        @keyframes numberChange {
            0% {
                transform: scale(0.8);
                opacity: 0;
            }
            70% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }
        
        @keyframes sparkle {
            0%, 100% {
                transform: translateY(-50%) scale(1);
                opacity: 0.7;
            }
            50% {
                transform: translateY(-50%) scale(1.3);
                opacity: 1;
            }
        }
        
        /* Responsive adjustments */
        @media (max-width: 1200px) {
            .handwriting-text {
                font-size: 5.5rem;
            }
            
            .year-container {
                font-size: 6rem;
            }
        }
        
        @media (max-width: 992px) {
            .handwriting-text {
                font-size: 4.5rem;
            }
            
            .year-container {
                font-size: 5rem;
            }
            
            .creator-attribution {
                position: absolute;
                top: auto;
                bottom: 30px;
                right: 30px;
                transform: none;
                transform-origin: initial;
            }
            
            .creator-text {
                font-size: 1rem;
            }
        }
        
        @media (max-width: 768px) {
            .handwriting-text {
                font-size: 3.5rem;
            }
            
            .subtitle {
                font-size: 1.4rem;
            }
            
            .year-container {
                font-size: 4rem;
                letter-spacing: 5px;
            }
            
            .creator-attribution {
                right: 20px;
                bottom: 20px;
                padding: 10px 15px;
            }
            
            .creator-text {
                flex-direction: column;
                gap: 5px;
                font-size: 0.9rem;
            }
            
            .creator-name {
                font-size: 1.1rem;
            }
        }
        
        @media (max-width: 576px) {
            .handwriting-text {
                font-size: 2.8rem;
            }
            
            .year-container {
                font-size: 3rem;
            }
            
            .creator-attribution {
                position: relative;
                top: auto;
                bottom: auto;
                right: auto;
                transform: none;
                margin: 40px auto 20px;
                width: 80%;
                text-align: center;
            }
            
            .creator-text {
                flex-direction: row;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- 3D Photo Background -->
    <div class="photo-3d-container">
        <div class="photo-3d"></div>
        <div class="photo-overlay"></div>
    </div>
    
    <!-- Creator Attribution - Right Side -->
    <div class="creator-attribution">
        <div class="creator-text">
            <span>Made with <i class="fas fa-heart creator-icon"></i> by</span>
            <span class="creator-name">Uddhav Krishnan</span>
        </div>
    </div>
    
    <div class="container">
        <div class="handwriting-container">
            <h1 class="handwriting-text">Happy New Year</h1>
            <div class="subtitle">Wishing you joy, prosperity, and happiness</div>
            
            <div class="decorations">
                <div class="decoration-item">🎉</div>
                <div class="decoration-item">✨</div>
                <div class="decoration-item">🎆</div>
                <div class="decoration-item">🎊</div>
                <div class="decoration-item">🥂</div>
            </div>
            
            <!-- UPDATED YEAR TO 2026 -->
            <div class="year-container">2026</div>
        </div>
        
        <div class="footer">
            <p>May the coming year bring you new opportunities and wonderful experiences</p>
            <p>Welcome to 2026 - A year of new beginnings and endless possibilities!</p>
            <p>© <span id="current-year">2026</span> | All Rights Reserved</p>
        </div>
    </div>
    
    <script>
        // Set current year in footer
        document.getElementById('current-year').textContent = new Date().getFullYear();
        
        // Add interactive mouse effect on the 3D photo
        document.addEventListener('mousemove', (e) => {
            const photo3d = document.querySelector('.photo-3d');
            const xAxis = (window.innerWidth / 2 - e.pageX) / 50;
            const yAxis = (window.innerHeight / 2 - e.pageY) / 50;
            
            photo3d.style.transform = `translate(-50%, -50%) rotateX(${10 + yAxis}deg) rotateY(${-5 + xAxis}deg) scale(1.2)`;
        });
        
        // Add sparkle effect when clicking on decorations
        document.querySelectorAll('.decoration-item').forEach(item => {
            item.addEventListener('click', function() {
                this.style.transform = 'scale(1.5)';
                this.style.transition = 'transform 0.3s';
                
                // Create a mini celebration effect
                const celebration = document.createElement('div');
                celebration.innerHTML = '🎊';
                celebration.style.position = 'absolute';
                celebration.style.left = `${this.getBoundingClientRect().left}px`;
                celebration.style.top = `${this.getBoundingClientRect().top}px`;
                celebration.style.fontSize = '2rem';
                celebration.style.zIndex = '100';
                celebration.style.pointerEvents = 'none';
                document.body.appendChild(celebration);
                
                // Animate celebration
                celebration.animate([
                    { transform: 'translateY(0) scale(1)', opacity: 1 },
                    { transform: 'translateY(-50px) scale(1.5)', opacity: 0 }
                ], {
                    duration: 800,
                    easing: 'ease-out'
                });
                
                // Remove after animation
                setTimeout(() => {
                    celebration.remove();
                    this.style.transform = '';
                }, 800);
            });
        });
        
        // Special 2026 celebration effect
        setTimeout(() => {
            const yearElement = document.querySelector('.year-container');
            yearElement.animate([
                { transform: 'scale(1)' },
                { transform: 'scale(1.2)' },
                { transform: 'scale(1)' }
            ], {
                duration: 1000,
                easing: 'ease-in-out'
            });
        }, 2000);
    </script>
</body>
</html>
