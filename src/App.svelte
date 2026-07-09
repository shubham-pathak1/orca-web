<script>
  import { onMount } from 'svelte';
  import { inject } from '@vercel/analytics';
  
  onMount(() => {
    // Initialize any required functionality
    // Initialize Vercel Analytics
    inject();
  });
</script>

<svelte:head>
  <title>Orca - Local Music Player</title>
</svelte:head>

<main id="main-content">
  <!-- Hero Section -->
  <section class="hero-section" id="hero">
    <div class="container">
      <!-- Static centered branding header -->
      <div class="brand-header">
        <img src="/screenshots/hero_gif.gif" alt="Listening to Music" class="brand-gif" />
        <div class="brand-label">
          <img src="/logo-square.png" alt="Orca Logo" class="brand-logo-small" />
          <span class="brand-name">orca</span>
        </div>
      </div>
      
      <h1>listen to your music offline.</h1>
      <p>
        Orca is a clean, fast music player for Windows. No subscriptions, no ads, just you and your music.
      </p>
      <div class="hero-actions">
        <!-- Download: Windows icon -->
        <a href="https://github.com/shubham-pathak1/orca/releases" class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="hero-download-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
          </svg>
          Download for Windows
        </a>
        <!-- Source Code: GitHub icon -->
        <a href="https://github.com/shubham-pathak1/orca" class="btn btn-secondary" target="_blank" rel="noopener noreferrer" id="hero-source-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0 0 22 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
          Source Code
        </a>
      </div>
    </div>
  </section>

  <!-- Scrolling Screenshot Showcase -->
  <section id="showcase" class="showcase-flow">
    <div class="container">

      <!-- Block 1: Library -->
      <div class="showcase-block" id="block-library">
        <div class="ambient-glow" style="background: rgba(167, 139, 250, 0.45);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">All your music in one place.</h2>
            <p class="block-description">
              Select your music folders and Orca scans them in a few seconds. It handles thousands of songs easily and lets you filter through them instantly as you type.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/library.png" alt="Orca Library View" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 2: Albums -->
      <div class="showcase-block" id="block-albums">
        <div class="ambient-glow" style="background: rgba(239, 68, 68, 0.4);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Organized by album.</h2>
            <p class="block-description">
              Browse your music by release. Orca extracts the artwork and track details from your files automatically and groups them into a clean grid.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/albums.png" alt="Orca Albums View" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 3: Artists -->
      <div class="showcase-block" id="block-artists">
        <div class="ambient-glow" style="background: rgba(236, 72, 153, 0.35);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Find your favorite artists.</h2>
            <p class="block-description">
              Browse your collection alphabetically and click any artist to see their complete discography in one place.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/artist.png" alt="Orca Artists View" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 4: Synced Lyrics -->
      <div class="showcase-block" id="block-lyrics">
        <div class="ambient-glow" style="background: rgba(139, 92, 246, 0.4);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Synced lyrics.</h2>
            <p class="block-description">
              Orca finds and displays time-coded lyrics that scroll automatically with your music. Click on any line to jump straight to that part of the song.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/lyrics.png" alt="Orca Synced Lyrics View" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 5: Full Player -->
      <div class="showcase-block" id="block-fullplayer">
        <div class="ambient-glow" style="background: rgba(239, 68, 68, 0.35);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Immersive playback.</h2>
            <p class="block-description">
              Expand the player to see high-resolution artwork on an ambient background that matches the colors of the album cover.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/fullplayer.png" alt="Orca Full Player View" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 6: Tag Editor -->
      <div class="showcase-block" id="block-tageditor">
        <div class="ambient-glow" style="background: rgba(245, 158, 11, 0.35);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Edit tags inside the app.</h2>
            <p class="block-description">
              Keep your music files clean. Edit titles, artists, album names, genres, and custom covers directly in Orca.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="/screenshots/metadata_editor.png" alt="Orca Tag Editor View" />
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- Final Download CTA -->
  <section class="cta-section" id="download">
    <div class="container">
      <div class="cta-inner">
        <div class="cta-text">
          <h2>Put your music back<br/>on your machine.</h2>
          <p>Free, open source, MIT licensed.</p>
          <div style="margin-top: 2rem;">
            <a href="https://github.com/shubham-pathak1/orca/releases" class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="cta-download-btn">
              <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
                <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
              </svg>
              Download Installer
            </a>
          </div>
        </div>
        <img src="/screenshots/footer.gif" alt="" class="cta-gif" aria-hidden="true" />
      </div>
    </div>
  </section>
</main>

<footer id="footer-main">
  <div class="container footer-flex">
    <span class="footer-copyright">&copy; {new Date().getFullYear()} orca · MIT License</span>

    <div class="footer-tech">
      <a href="https://www.rust-lang.org/" target="_blank" rel="noopener noreferrer" class="tech-link" title="Rust">
        <img src="/screenshots/rust.png" alt="Rust" />
        <span>Rust</span>
      </a>
      <a href="https://tauri.app/" target="_blank" rel="noopener noreferrer" class="tech-link" title="Tauri">
        <img src="/screenshots/tauri.png" alt="Tauri" />
        <span>Tauri</span>
      </a>
      <a href="https://svelte.dev/" target="_blank" rel="noopener noreferrer" class="tech-link" title="Svelte">
        <img src="/screenshots/svelte.png" alt="Svelte" />
        <span>Svelte</span>
      </a>
      <a href="https://sqlite.org/" target="_blank" rel="noopener noreferrer" class="tech-link" title="SQLite">
        <img src="/screenshots/sqlite.png" alt="SQLite" />
        <span>SQLite</span>
      </a>
      <a href="https://lrclib.net/" target="_blank" rel="noopener noreferrer" class="tech-link" title="LRCLIB">
        <img src="/screenshots/lrclib.png" alt="LRCLIB" />
        <span>LRCLIB</span>
      </a>
    </div>

    <div class="footer-links">
      <a href="https://github.com/shubham-pathak1/orca" class="footer-link" target="_blank" rel="noopener noreferrer" id="footer-repo-link">GitHub</a>
      <a href="https://github.com/shubham-pathak1/orca/issues" class="footer-link" target="_blank" rel="noopener noreferrer" id="footer-issues-link">Issues</a>
    </div>
  </div>
</footer>

