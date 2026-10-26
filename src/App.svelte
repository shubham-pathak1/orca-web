<script lang="ts">
  import { onMount } from 'svelte';
  import { inject } from '@vercel/analytics';

  const releaseTag = 'v0.1.8-alpha';
  const releaseUrl = `https://github.com/shubham-pathak1/orca/releases/tag/${releaseTag}`;

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
    <div class="container-wide hero-layout">
      <div class="hero-text">
        <div class="brand-header">
          <div class="brand-label">
            <img src="/orca-logo.png" alt="" width="76" height="76" class="brand-logo-small" />
            <h1 class="brand-name">orca</h1>
          </div>
        </div>
        <div class="hero-copy">
      <p>A fast, open-source player for your local music library, built with Rust and Slint.</p>
      <div class="hero-actions">
        <a href={releaseUrl} class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="hero-download-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
          </svg>
          Download for Windows
        </a>
      </div>
      <div class="hero-source">
        <a href="https://github.com/shubham-pathak1/orca" target="_blank" rel="noopener noreferrer" id="hero-source-btn">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0 0 22 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
          View source code
        </a>
      </div>
      </div>
      </div>
      <div class="hero-preview">
        <img src="https://ik.imagekit.io/shubhampathak/orca-web/library.png?v=20261026" alt="Orca's music library with album artwork, song list and playback controls" width="1917" height="1078" fetchpriority="high" decoding="async" />
      </div>
    </div>
  </section>

  <!-- Scrolling Screenshot Showcase -->
  <section id="showcase" class="showcase-flow">
    <div class="container">

      <!-- Albums -->
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
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/album.png?v=20261026" alt="Orca album page with tracks and related albums" width="1917" height="1078" loading="lazy" decoding="async" />
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
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/artist.png?v=20261026" alt="Orca artist page with songs and albums" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

      <!-- Block 4: Synced Lyrics -->
      <div class="showcase-block" id="block-lyrics">
        <div class="ambient-glow" style="background: linear-gradient(135deg, rgba(205, 205, 210, 0.4), rgba(72, 72, 80, 0.3));"></div>
        <div class="block-layout">
          <div class="block-text">
            <h2 class="block-title">Follow along with synced lyrics.</h2>
            <p class="block-description">
              Lyrics move with the music. Click a line to start listening from there.
            </p>
          </div>
          <div class="block-media-container">
            <div class="block-media">
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/fullplayer_lyrics.png?v=20261026" alt="Orca full player with artwork, an ambient background, and synced lyrics" width="1917" height="1078" loading="lazy" decoding="async" />
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
              <img src="https://ik.imagekit.io/shubhampathak/orca-web/metadata_editor.png?v=20261026" alt="Orca metadata editor with cover controls, song tags, and lyrics" width="1917" height="1078" loading="lazy" decoding="async" />
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>

  <section class="features-section" id="features" aria-labelledby="features-title">
    <div class="container">
      <div class="section-heading">
        <h2 class="block-title" id="features-title">Everything your local library needs.</h2>
        <p class="block-description">A focused player with the controls that matter every day.</p>
      </div>
      <div class="feature-list">
        <article class="feature-row"><h3>Browse your way</h3><p>Songs, artists, albums, genres, playlists, nested folders and Liked Songs. Search as you type.</p></article>
        <article class="feature-row"><h3>Keep the music flowing</h3><p>Gapless playback, shuffle, repeat, an editable queue and session restore.</p></article>
        <article class="feature-row"><h3>Follow the lyrics</h3><p>Synced and word-timed lyrics, click-to-seek, LRC import and online lookup.</p></article>
        <article class="feature-row"><h3>Make it yours</h3><p>Light and dark themes, dynamic artwork colors, custom fonts and Minimal Mode.</p></article>
        <article class="feature-row"><h3>Organize your files</h3><p>Edit tags and covers, update collection details, and import or export M3U playlists.</p></article>
        <article class="feature-row"><h3>Works with Windows</h3><p>Media controls, tray integration and keyboard shortcuts. Your own music plays offline.</p></article>
      </div>
      <p class="features-note">Online artwork and lyrics lookup use the internet. Automatic artwork matching is experimental.</p>
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
            <a href={releaseUrl} class="btn btn-primary" target="_blank" rel="noopener noreferrer" id="cta-download-btn">
              <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
                <path d="M0 3.449L9.75 2.1v9.451H0m10.949-9.602L24 0v11.4H10.949M0 12.6h9.75v9.451L0 20.699M10.949 12.6H24V24l-13.051-1.851"/>
              </svg>
              Download for Windows
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

