<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AZLANTV - Free Live TV Streaming</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="logo">
            <h1>AZLANTV</h1>
            <p>Live TV Streaming</p>
        </div>
        <nav>
            <ul>
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#">Channels</a></li>
                <li><a href="#">Categories</a></li>
                <li><a href="#">Guide</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
        <div class="user-actions">
            <button class="search-btn"><i class="fas fa-search"></i></button>
            <button class="login-btn">Login</button>
        </div>
    </header>

    <main>
        <section class="featured-channel">
            <div class="video-player" id="mainPlayer">
                <!-- Video player will be loaded here -->
                <div class="player-placeholder">
                    <i class="fas fa-tv"></i>
                    <p>Select a channel to start watching</p>
                </div>
            </div>
            <div class="channel-info">
                <h2 id="current-channel">No Channel Selected</h2>
                <p id="current-program">--</p>
                <div class="player-controls">
                    <button id="playPauseBtn"><i class="fas fa-play"></i></button>
                    <button id="muteBtn"><i class="fas fa-volume-up"></i></button>
                    <button id="fullscreenBtn"><i class="fas fa-expand"></i></button>
                    <button id="qualityBtn"><i class="fas fa-cog"></i> Quality</button>
                </div>
            </div>
        </section>

        <section class="channel-list">
            <h3>Popular Channels</h3>
            <div class="channels-grid" id="popularChannels">
                <!-- Channels will be loaded here via JavaScript -->
            </div>
        </section>

        <section class="categories">
            <h3>Browse by Category</h3>
            <div class="categories-grid">
                <div class="category-card" data-category="news">
                    <i class="fas fa-newspaper"></i>
                    <span>News</span>
                </div>
                <div class="category-card" data-category="sports">
                    <i class="fas fa-baseball-ball"></i>
                    <span>Sports</span>
                </div>
                <div class="category-card" data-category="entertainment">
                    <i class="fas fa-film"></i>
                    <span>Entertainment</span>
                </div>
                <div class="category-card" data-category="kids">
                    <i class="fas fa-child"></i>
                    <span>Kids</span>
                </div>
                <div class="category-card" data-category="music">
                    <i class="fas fa-music"></i>
                    <span>Music</span>
                </div>
                <div class="category-card" data-category="education">
                    <i class="fas fa-graduation-cap"></i>
                    <span>Education</span>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>AZLANTV</h4>
                <p>Free live TV streaming for everyone</p>
            </div>
            <div class="footer-section">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Channels</a></li>
                    <li><a href="#">Categories</a></li>
                    <li><a href="#">TV Guide</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h4>Legal</h4>
                <ul>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">DMCA</a></li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 AZLANTV. All rights reserved.</p>
        </div>
    </footer>

    <script src="js/script.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
</body>
</html># ipl2025
