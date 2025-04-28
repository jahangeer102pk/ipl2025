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
/* Base Styles */
:root {
    --primary-color: #3498db;
    --secondary-color: #2c3e50;
    --accent-color: #e74c3c;
    --light-color: #ecf0f1;
    --dark-color: #2c3e50;
    --text-color: #333;
    --text-light: #7f8c8d;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f5f5f5;
    color: var(--text-color);
    line-height: 1.6;
}

/* Header Styles */
header {
    background-color: var(--secondary-color);
    color: white;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo h1 {
    font-size: 2rem;
    color: var(--primary-color);
    font-weight: 700;
}

.logo p {
    font-size: 0.8rem;
    color: var(--light-color);
}

nav ul {
    display: flex;
    list-style: none;
}

nav ul li a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: all 0.3s ease;
}

nav ul li a:hover, nav ul li a.active {
    background-color: var(--primary-color);
    color: white;
}

.user-actions button {
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    margin-left: 0.5rem;
    transition: all 0.3s ease;
}

.search-btn {
    background-color: transparent;
    color: white;
    font-size: 1rem;
}

.login-btn {
    background-color: var(--primary-color);
    color: white;
    font-weight: 600;
}

.login-btn:hover {
    background-color: #2980b9;
}

/* Main Content Styles */
main {
    padding: 2rem;
    max-width: 1400px;
    margin: 0 auto;
}

.featured-channel {
    background-color: var(--dark-color);
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: 2rem;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
}

.video-player {
    width: 100%;
    height: 0;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    position: relative;
    background-color: #000;
}

.video-player video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

.player-placeholder {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: var(--light-color);
    font-size: 1.2rem;
}

.player-placeholder i {
    font-size: 3rem;
    margin-bottom: 1rem;
    color: var(--primary-color);
}

.channel-info {
    padding: 1rem;
    background-color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.channel-info h2 {
    color: var(--secondary-color);
    margin-bottom: 0.5rem;
}

.channel-info p {
    color: var(--text-light);
    font-size: 0.9rem;
}

.player-controls button {
    background-color: var(--primary-color);
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    margin-left: 0.5rem;
    cursor: pointer;
    transition: all 0.3s ease;
}

.player-controls button:hover {
    background-color: #2980b9;
}

.player-controls button i {
    margin-right: 0.3rem;
}

/* Channel List Styles */
.channel-list h3, .categories h3 {
    margin-bottom: 1rem;
    color: var(--secondary-color);
    font-size: 1.5rem;
}

.channels-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 1rem;
    margin-bottom: 2rem;
}

.channel-card {
    background-color: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    cursor: pointer;
}

.channel-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.channel-card img {
    width: 100%;
    height: 120px;
    object-fit: cover;
}

.channel-card .channel-details {
    padding: 0.8rem;
}

.channel-card h4 {
    margin-bottom: 0.3rem;
    color: var(--secondary-color);
}

.channel-card p {
    font-size: 0.8rem;
    color: var(--text-light);
}

/* Categories Styles */
.categories-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    gap: 1rem;
    margin-bottom: 2rem;
}

.category-card {
    background-color: white;
    border-radius: 8px;
    padding: 1.5rem 1rem;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    cursor: pointer;
}

.category-card:hover {
    background-color: var(--primary-color);
    color: white;
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.category-card i {
    font-size: 2rem;
    margin-bottom: 0.5rem;
    display: block;
}

/* Footer Styles */
footer {
    background-color: var(--secondary-color);
    color: white;
    padding: 2rem;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.footer-section h4 {
    font-size: 1.2rem;
    margin-bottom: 1rem;
    color: var(--primary-color);
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 0.5rem;
}

.footer-section ul li a {
    color: var(--light-color);
    text-decoration: none;
    transition: all 0.3s ease;
}

.footer-section ul li a:hover {
    color: var(--primary-color);
    padding-left: 5px;
}

.copyright {
    text-align: center;
    padding-top: 2rem;
    margin-top: 2rem;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    color: var(--light-color);
    font-size: 0.9rem;
}

/* Responsive Styles */
@media (max-width: 768px) {
    header {
        flex-direction: column;
        padding: 1rem;
    }

    nav ul {
        margin: 1rem 0;
    }

    .user-actions {
        width: 100%;
        display: flex;
        justify-content: flex-end;
    }

    .channel-info {
        flex-direction: column;
        align-items: flex-start;
    }

    .player-controls {
        margin-top: 1rem;
        align-self: flex-end;
    }
}

@media (max-width: 480px) {
    .channels-grid {
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    }

    .categories-grid {
        grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    }
}
document.addEventListener('DOMContentLoaded', function() {
    // Sample channel data (replace with your actual channels)
    const channels = [
        {
            id: 1,
            name: "AZLAN News",
            category: "news",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+News",
            streamUrl: "https://example.com/stream1.m3u8",
            currentProgram: "Morning News",
            viewers: 1250
        },
        {
            id: 2,
            name: "AZLAN Sports",
            category: "sports",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+Sports",
            streamUrl: "https://example.com/stream2.m3u8",
            currentProgram: "Football Live",
            viewers: 3200
        },
        {
            id: 3,
            name: "AZLAN Movies",
            category: "entertainment",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+Movies",
            streamUrl: "https://example.com/stream3.m3u8",
            currentProgram: "Action Movie",
            viewers: 1800
        },
        {
            id: 4,
            name: "AZLAN Kids",
            category: "kids",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+Kids",
            streamUrl: "https://example.com/stream4.m3u8",
            currentProgram: "Cartoon Time",
            viewers: 950
        },
        {
            id: 5,
            name: "AZLAN Music",
            category: "music",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+Music",
            streamUrl: "https://example.com/stream5.m3u8",
            currentProgram: "Top Hits",
            viewers: 2100
        },
        {
            id: 6,
            name: "AZLAN Learn",
            category: "education",
            logo: "https://via.placeholder.com/200x120?text=AZLAN+Learn",
            streamUrl: "https://example.com/stream6.m3u8",
            currentProgram: "Science Today",
            viewers: 750
        }
    ];

    // DOM Elements
    const popularChannelsContainer = document.getElementById('popularChannels');
    const mainPlayerContainer = document.getElementById('mainPlayer');
    const currentChannelElement = document.getElementById('current-channel');
    const currentProgramElement = document.getElementById('current-program');
    const playPauseBtn = document.getElementById('playPauseBtn');
    const muteBtn = document.getElementById('muteBtn');
    const fullscreenBtn = document.getElementById('fullscreenBtn');
    const qualityBtn = document.getElementById('qualityBtn');
    const categoryCards = document.querySelectorAll('.category-card');

    // Video player variables
    let videoPlayer;
    let isPlaying = false;
    let isMuted = false;
    let currentChannel = null;

    // Initialize the page
    function init() {
        renderChannels();
        setupEventListeners();
    }

    // Render channels to the page
    function renderChannels() {
        popularChannelsContainer.innerHTML = '';
        
        channels.forEach(channel => {
            const channelCard = document.createElement('div');
            channelCard.className = 'channel-card';
            channelCard.dataset.id = channel.id;
            
            channelCard.innerHTML = `
                <img src="${channel.logo}" alt="${channel.name}">
                <div class="channel-details">
                    <h4>${channel.name}</h4>
                    <p>${channel.currentProgram}</p>
                    <small>${channel.viewers.toLocaleString()} viewers</small>
                </div>
            `;
            
            popularChannelsContainer.appendChild(channelCard);
        });
    }

    // Setup event listeners
    function setupEventListeners() {
        // Channel card click event
        document.querySelectorAll('.channel-card').forEach(card => {
            card.addEventListener('click', function() {
                const channelId = parseInt(this.dataset.id);
                const selectedChannel = channels.find(ch => ch.id === channelId);
                playChannel(selectedChannel);
            });
        });

        // Category card click event
        categoryCards.forEach(card => {
            card.addEventListener('click', function() {
                const category = this.dataset.category;
                filterChannelsByCategory(category);
            });
        });

        // Player control events
        playPauseBtn.addEventListener('click', togglePlayPause);
        muteBtn.addEventListener('click', toggleMute);
        fullscreenBtn.addEventListener('click', toggleFullscreen);
        qualityBtn.addEventListener('click', showQualityOptions);
    }

    // Play a channel
    function playChannel(channel) {
        currentChannel = channel;
        
        // Update UI
        currentChannelElement.textContent = channel.name;
        currentProgramElement.textContent = channel.currentProgram;
        
        // Create or update video player
        if (!videoPlayer) {
            createVideoPlayer(channel.streamUrl);
        } else {
            videoPlayer.src = channel.streamUrl;
            if (Hls.isSupported()) {
                hls.loadSource(channel.streamUrl);
                hls.attachMedia(videoPlayer);
            }
            videoPlayer.play();
            isPlaying = true;
            updatePlayPauseButton();
        }
    }

    // Create video player with HLS.js if supported
    let hls;
    function createVideoPlayer(streamUrl) {
        // Remove placeholder
        mainPlayerContainer.querySelector('.player-placeholder')?.remove();
        
        // Create video element
        videoPlayer = document.createElement('video');
        videoPlayer.controls = false;
        videoPlayer.style.width = '100%';
        videoPlayer.style.height = '100%';
        mainPlayerContainer.appendChild(videoPlayer);
        
        if (Hls.isSupported()) {
            hls = new Hls();
            hls.loadSource(streamUrl);
            hls.attachMedia(videoPlayer);
            hls.on(Hls.Events.MANIFEST_PARSED, function() {
                videoPlayer.play();
                isPlaying = true;
                updatePlayPauseButton();
            });
        } else if (videoPlayer.canPlayType('application/vnd.apple.mpegurl')) {
            // For Safari
            videoPlayer.src = streamUrl;
            videoPlayer.addEventListener('loadedmetadata', function() {
                videoPlayer.play();
                isPlaying = true;
                updatePlayPauseButton();
            });
        }
        
        // Player event listeners
        videoPlayer.addEventListener('play', function() {
            isPlaying = true;
            updatePlayPauseButton();
        });
        
        videoPlayer.addEventListener('pause', function() {
            isPlaying = false;
            updatePlayPauseButton();
        });
    }

    // Toggle play/pause
    function togglePlayPause() {
        if (!videoPlayer) return;
        
        if (isPlaying) {
            videoPlayer.pause();
        } else {
            videoPlayer.play();
        }
    }

    // Update play/pause button
    function updatePlayPauseButton() {
        if (isPlaying) {
            playPauseBtn.innerHTML = '<i class="fas fa-pause"></i>';
        } else {
            playPauseBtn.innerHTML = '<i class="fas fa-play"></i>';
        }
    }

    // Toggle mute
    function toggleMute() {
        if (!videoPlayer) return;
        
        isMuted = !isMuted;
        videoPlayer.muted = isMuted;
        
        if (isMuted) {
            muteBtn.innerHTML = '<i class="fas fa-volume-mute"></i>';
        } else {
            muteBtn.innerHTML = '<i class="fas fa-volume-up"></i>';
        }
    }

    // Toggle fullscreen
    function toggleFullscreen() {
        if (!videoPlayer) return;
        
        if (!document.fullscreenElement) {
            mainPlayerContainer.requestFullscreen().catch(err => {
                console.error(`Error attempting to enable fullscreen: ${err.message}`);
            });
        } else {
            document.exitFullscreen();
        }
    }

    // Show quality options (placeholder)
    function showQualityOptions() {
        alert('Quality options will be available here');
        // In a real implementation, you would show a dropdown with available quality levels
    }

    // Filter channels by category
    function filterChannelsByCategory(category) {
        const filteredChannels = channels.filter(ch => ch.category === category);
        
        // Update UI to show filtered channels
        popularChannelsContainer.innerHTML = '';
        
        if (filteredChannels.length === 0) {
            popularChannelsContainer.innerHTML = '<p>No channels found in this category</p>';
            return;
        }
        
        filteredChannels.forEach(channel => {
            const channelCard = document.createElement('div');
            channelCard.className = 'channel-card';
            channelCard.dataset.id = channel.id;
            
            channelCard.innerHTML = `
                <img src="${channel.logo}" alt="${channel.name}">
                <div class="channel-details">
                    <h4>${channel.name}</h4>
                    <p>${channel.currentProgram}</p>
                    <small>${channel.viewers.toLocaleString()} viewers</small>
                </div>
            `;
            
            popularChannelsContainer.appendChild(channelCard);
        });
        
        // Reattach event listeners to new channel cards
        document.querySelectorAll('.channel-card').forEach(card => {
            card.addEventListener('click', function() {
                const channelId = parseInt(this.dataset.id);
                const selectedChannel = channels.find(ch => ch.id === channelId);
                playChannel(selectedChannel);
            });
        });
    }

    // Initialize the application
    init();
});
