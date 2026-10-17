<script lang="ts">
  import { onMount } from 'svelte';
  import { inject } from '@vercel/analytics';

  onMount(() => {
    inject();
  });
</script>

<svelte:head>
  <title>Orca - Minimal Music Player for Windows | Rust + Slint</title>
</svelte:head>

<a href="#main-content" class="skip-link">Skip to content</a>

<main id="main-content">
  <!-- Hero Section -->
  <section class="hero-section" id="hero">
    <img class="hero-background" src="/illustrations/orca-hero.png" alt="" aria-hidden="true" width="736" height="736" decoding="async" fetchpriority="high" />
    <div class="container">
      <!-- Static centered branding header -->
      <div class="brand-header">
        <div class="brand-label">
          <img src="/orca-logo.png" alt="" width="76" height="76" class="brand-logo-small" />
          <h1 class="brand-name">orca</h1>
        </div>
      </div>
      
      <p>
        A minimal, open-source music player for Windows. Built with Rust and Slint.
      </p>
      <div class="hero-actions">
        <!-- Download: Windows icon -->
        <a href="https://github.com/shubham-pathak1/orca/releases" class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="hero-download-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
          </svg>
          View Windows releases
        </a>
        <!-- Source code: GitHub icon -->
        <a href="https://github.com/shubham-pathak1/orca" class="btn btn-secondary" target="_blank" rel="noopener noreferrer" id="hero-source-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0 0 22 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
          Source code
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
              Add your music folders, browse thousands of songs, and find your next listen as you type.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/library.png" alt="Orca library in grid view with album artwork" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 2: Albums -->
      <div class="showcase-block" id="block-albums">
        <div class="ambient-glow" style="background: rgba(239, 68, 68, 0.4);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Your albums, together.</h2>
            <p class="block-description">
              Find an album, pick a track, or listen from the beginning.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/album.png" alt="Orca album page with tracks and related albums" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 3: Artists -->
      <div class="showcase-block" id="block-artists">
        <div class="ambient-glow" style="background: rgba(236, 72, 153, 0.35);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Your favorite artists, easy to find.</h2>
            <p class="block-description">
              Explore each artist’s songs and albums without searching through folders.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/artist.png" alt="Orca artist page with songs and albums" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 4: Synced Lyrics -->
      <div class="showcase-block" id="block-lyrics">
        <div class="ambient-glow" style="background: rgba(139, 92, 246, 0.4);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Follow along with synced lyrics.</h2>
            <p class="block-description">
              Lyrics move with the music. Click a line to start listening from there.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/full_player_lyrics.png" alt="Orca full player with artwork, an ambient background, and synced lyrics" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 6: Tag Editor -->
      <div class="showcase-block" id="block-tageditor">
        <div class="ambient-glow" style="background: rgba(245, 158, 11, 0.35);"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Edit your music details.</h2>
            <p class="block-description">
              Update song details, change covers, and add lyrics in one place.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/metadata_editor.png" alt="Orca metadata editor with cover controls, song tags, and lyrics" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>

  <section class="faq-section" id="faq" aria-labelledby="faq-title">
    <div class="container">
      <div class="faq-layout">
        <div class="faq-heading">
          <h2 class="block-title" id="faq-title">Before you download.</h2>
        </div>
        <div class="faq-list">
          <details><summary>Is Orca free?</summary><p>Yes. Free and open source, with no ads or subscriptions. Orca plays your own music files.</p></details>
          <details><summary>Can I use it offline?</summary><p>Yes. Listening works offline. You only need a connection to fetch new artwork or lyrics.</p></details>
          <details><summary>Which platforms are supported?</summary><p>The native alpha is for Windows. Linux and macOS builds are not available yet.</p></details>
        </div>
        <div class="faq-art" aria-hidden="true">
          <img class="faq-penguins" src="/illustrations/record-penguins.jpg" alt="" width="580" height="580" loading="lazy" decoding="async" />
        </div>
      </div>
    </div>
  </section>

  <!-- Final Download CTA -->
  <section class="cta-section" id="download">
    <div class="container">
      <div class="cta-inner">
        <div class="cta-text">
          <h2>Ready to listen?</h2>
          <p>Get Orca for Windows and open your music collection.</p>
          <div class="cta-actions">
            <a href="https://github.com/shubham-pathak1/orca/releases" class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="cta-download-btn">
              <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
                <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
              </svg>
              View Windows releases
            </a>
          </div>
        </div>
        <img src="/screenshots/hero_gif.gif" alt="" class="cta-gif" aria-hidden="true" loading="lazy" decoding="async" />
      </div>
    </div>
  </section>
</main>

<footer id="footer-main">
  <div class="container footer-flex">
    <span class="footer-copyright">&copy; {new Date().getFullYear()} orca · <a href="https://github.com/shubham-pathak1/orca/blob/main/LICENSE" target="_blank" rel="noopener noreferrer">MIT License</a></span>

    <div class="footer-links">
      <a href="https://github.com/shubham-pathak1/orca" class="footer-link" target="_blank" rel="noopener noreferrer" id="footer-repo-link">GitHub</a>
      <a href="https://github.com/shubham-pathak1/orca/issues" class="footer-link" target="_blank" rel="noopener noreferrer" id="footer-issues-link">Report a bug</a>
    </div>
  </div>
</footer>

