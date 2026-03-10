### 1. Dasar-Dasar OpenClaw (Getting Started)
Fokus pada instalasi awal dan konsep dasar asisten pribadi AI.

*   **Subtopik A: Instalasi & Runtime**
    *   Panduan Instalasi OpenClaw di Linux (Ubuntu/Debian).
    *   Menjalankan OpenClaw di Windows via WSL2.
    *   Instalasi macOS: Aplikasi Menu Bar & Gateway.
    *   Memilih Runtime: Perbedaan Node.js vs Bun.
    *   Langkah-langkah Uninstall Bersih OpenClaw.
*   **Subtopik B: Onboarding & Pengaturan Awal**
    *   Cara Menggunakan CLI Onboarding Wizard (`openclaw onboard`).
    *   Ritual Bootstrapping: Pengaturan Identitas Pertama Kali.
    *   Memilih dan Menyetel Model AI Primer.
    *   Memahami Struktur Direktori Workspace Agen.
    *   Verifikasi Kesehatan Instalasi dengan `openclaw status`.
*   **Subtopik C: Platform & Interface**
    *   Fitur Aplikasi Pendamping macOS OpenClaw.
    *   Menghubungkan Node Mobile: Panduan iOS & Android.
    *   Akses Remote: Mengaktifkan Web Dashboard/Control UI.
    *   Interaksi Terminal: Panduan Penggunaan OpenClaw TUI.
    *   Dasar-Dasar Perintah CLI OpenClaw yang Wajib Diketahui.

### 2. Konfigurasi & Manajemen Gateway
Manajemen teknis terhadap proses gateway yang selalu aktif.

*   **Subtopik A: Operasi Gateway**
    *   Runbook Gateway: Operasi Hari ke-1 dan ke-2.
    *   Supervisi Servis: Menggunakan Systemd & Launchd.
    *   Menjalankan Beberapa Gateway di Satu Host.
    *   Reload Konfigurasi Tanpa Restart Gateway.
    *   Memahami Mode Bind Gateway: Loopback vs LAN vs Tailnet.
*   **Subtopik B: Autentikasi & Model**
    *   API Key vs OAuth: Memilih Metode Autentikasi.
    *   Cara Setup Anthropic via `setup-token`.
    *   Konfigurasi OpenAI & Codex Subscription.
    *   Strategi Failover & Fallback Model AI.
    *   Integrasi Model Lokal via Ollama & LM Studio.
*   **Subtopik C: Kustomisasi Lanjutan**
    *   Referensi Lengkap File `openclaw.json`.
    *   Organisasi Konfigurasi Besar Menggunakan `$include`.
    *   Urutan Presedensi Variabel Lingkungan (Env Vars).
    *   Pengaturan Timezone dan Format Waktu Agen.
    *   Kustomisasi Log: Format Konsol vs File JSONL.

### 3. Integrasi Saluran Pesan (Channels)
Cara menghubungkan AI ke aplikasi pesan yang Anda gunakan.

*   **Subtopik A: Chat Messenger Utama**
    *   Integrasi WhatsApp: Panduan Pairing QR Baileys.
    *   Cara Membuat dan Menghubungkan Bot Telegram.
    *   Setup Discord Bot: Server, Saluran, dan DM.
    *   iMessage Support: Menggunakan BlueBubbles Bridge.
    *   Konfigurasi Signal Private Messenger.
*   **Subtopik B: Manajemen Grup & Interaksi**
    *   Aturan Mention dan Gating di Chat Grup.
    *   Isolasi Sesi: DM Pribadi vs Sesi Grup.
    *   Manajemen Antrean Pesan (Queueing).
    *   Streaming Reasoning di Telegram dan Slack.
    *   Formatting Outbound: Markdown ke HTML Per Saluran.
*   **Subtopik C: Saluran Korporat & Kustom**
    *   Integrasi Microsoft Teams via Adaptive Cards.
    *   Setup Plugin Matrix dan Dukungan E2EE.
    *   Menghubungkan Feishu dan Lark via WebSocket.
    *   Integrasi Saluran Chat IRC Klasik.
    *   Eksperimen: Integrasi Saluran Nostr dan Tlon.

### 4. Memori, Skill, & Alat (Intelligence)
Meningkatkan kemampuan agen AI agar bisa bertindak dan mengingat.

*   **Subtopik A: Sistem Memori Markdown**
    *   Cara Kerja Memori OpenClaw: File Markdown di Workspace.
    *   Memahami Pre-compaction Memory Flush.
    *   Setup Pencarian Vektor Semantik untuk Memori.
    *   Perbedaan MEMORY.md vs Log Harian (Daily Logs).
    *   Menggunakan Sidecar QMD untuk Pencarian Vektor Lokal.
*   **Subtopik B: Skill & Otomatisasi**
    *   Kustomisasi Kepribadian Agen via `SOUL.md`.
    *   Discovering Skills: Menggunakan Marketplace ClawHub.
    *   Tutorial Membuat Skill Kustom Pertama Anda.
    *   Otomatisasi Tugas dengan Cron Jobs & Heartbeats.
    *   Event-Driven Automation: Menggunakan Hooks Internal.
*   **Subtopik C: Alat Bantu (Tools)**
    *   Browser Control: Mengatur Profil Chrome yang Dikelola Agen.
    *   Eksekusi Shell: Keamanan Alat `exec` dan `process`.
    *   Live Canvas: Visualisasi Data Real-time di Mobile.
    *   Spawning Sub-agen untuk Tugas Paralel.
    *   Web Search & Fetch: Mengintegrasikan Brave & Firecrawl.

### 5. Keamanan & Infrastruktur
Melindungi server dan data pribadi Anda.

*   **Subtopik A: Sandboxing & Isolasi**
    *   Docker Sandboxing: Melindungi Host dari AI.
    *   Konfigurasi Hak Akses Filesystem (RW vs RO).
    *   Elevated Mode: Pintu Darurat Akses Host yang Aman.
    *   Manajemen UID/GID di Dalam Kontainer Sandbox.
    *   Membatasi Penggunaan Sumber Daya Sandbox.
*   **Subtopik B: Kontrol Akses & Audit**
    *   Menjalankan Audit Keamanan (`openclaw security audit`).
    *   Model Pairing: Menyetujui Siapa yang Bisa DM Bot.
    *   Manajemen Rahasia: Melindungi Token di Disk.
    *   Otorisasi Perintah untuk Pengguna Remote.
    *   Mitigasi Risiko Prompt Injection pada Agen Tool-Enabled.
*   **Subtopik C: Cloud & Deployment**
    *   Deploy OpenClaw di DigitalOcean ($6/bln).
    *   Setup Produksi Hemat di Hetzner VPS.
    *   Gratis Selamanya: Panduan Oracle Cloud ARM.
    *   Konfigurasi Docker Compose untuk Deployment Skala Besar.
    *   Backup & Migrasi: Memindahkan OpenClaw ke Server Baru.

### 6. Optimasi Lanjutan & Troubleshooting
Menangani masalah kompleks dan performa.

*   **Subtopik A: Performa & Konteks**
    *   Struktur System Prompt: Apa yang Dilihat Model.
    *   Manajemen Sesi via Auto-Compaction.
    *   Perbedaan Pruning vs Compaction dalam Token.
    *   Cara Membaca Status Token dengan Perintah `/status`.
    *   Optimasi Prompt untuk Jendela Konteks yang Kecil.
*   **Subtopik B: Protokol & Developer**
    *   Memahami Protokol Gateway WebSocket (WS).
    *   Cara Membuat Plugin Menggunakan OpenClaw SDK.
    *   Implementasi Transformasi Webhook Kustom.
    *   ACP Agents: Menjalankan Harness Coding Eksternal.
    *   OpenResponses: Ekspos Endpoint HTTP Kompatibel OpenAI.
*   **Subtopik C: Diagnosa & Perbaikan**
    *   Triage Cepat: Tangga Diagnostik 60 Detik.
    *   Menggunakan Perintah `openclaw doctor` untuk Perbaikan Otomatis.
    *   Mendiagnosa Error Handshake & Koneksi RPC.
    *   Manajemen Insiden: Tindakan Jika AI Melakukan Kesalahan.
    *   Cara Melaporkan Bug dan Kerentanan Keamanan.
