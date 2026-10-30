# Fitur Aeris Hub — Violence District (no key)

Di-generate langsung dari source `Aeris_Hub_nokey.lua` (build **vd-1.6**, 17.159 baris), bukan ditulis manual — jadi angkanya sinkron sama script yang jalan.

## Ringkasan

**6 tab · 30 section · 174 kontrol**

| Tipe kontrol | Jumlah |
|---|---|
| Toggle | 80 |
| Slider | 41 |
| Tombol | 21 |
| Checkbox | 20 |
| Dropdown | 9 |
| Textbox | 1 |
| Keybind standalone (*Menu Keybind*) | 1 |
| Color picker | 10 |

Dua jenis kontrol yang jumlahnya lebih banyak dari yang kelihatan di daftar:

- **Keybind** — tiap dari 80 toggle punya slot bind sendiri (`[None]` di sebelah toggle).
  Klik `[None]` → tekan tombol → `Backspace`/`Esc` buat ngehapus. Disimpan per-flag (`<Flag>_Key`).
- **Color picker** — 1 standalone (*Gen Done Color* di Map ESP) + 9 nempel sebagai sub-kontrol
  di toggle ESP/crosshair. Ditandai 🎨 di daftar bawah.

---


## 🏠 Main — 9 section, 48 kontrol

### Movement

- **Auto Vault**  · `keybind`
- **Auto Pallet Slide**  · `keybind`
- **Auto Run PC**  · `keybind`
- **Auto Run Mobile**  · `keybind`
- **Enable Speed Boost**  · `keybind`
- **SpeedAmount**  `0.1..3 (def 0.1)`

### Server Utility

- **Skip Endscreen**  · `keybind`

### Fake Perks

- **Quick Recovery**  · `keybind`
- **Perfect Landing**  · `keybind`
- **Flowstate**  · `keybind`
- **Adrenaline Rush**  · `keybind`
- **Perk Cooldown**  `0..180 (def 10)`

### Camera Settings

- **Enable Stretch Res**  · `keybind`
- **Stretch Amount**  `0.4..1 (def 0.67)`
- **Third Person (Killer)**  · `keybind`
- **Infinity Zoom Out**  · `keybind`
- **Camera FOV**  · `keybind`
- **FOV Value**  `60..120 (def 90)`

### Camera DBD

- **DBD Camera**  · `keybind`
- **DBD Distance**  `6..20 (def 13)`
- **DBD Height**  `1..8 (def 4.2)`
- **DBD Run Smooth**  `0.03..0.35 (def 0.1)`
- **DBD Look Smooth**  `0.08..0.6 (def 0.28)`
- **DBD Sensitivity**  `0.15..1.2 (def 0.55)`
- **DBD Pitch Min**  `-1.2..0 (def -0.55)`
- **DBD Pitch Max**  `0..1.2 (def 0.45)`
- **DBD FOV**  `50..90 (def 70)`

### Streamer Mode

- **Streamer Mode**  · `keybind`

### Players Utility

- **Invisibility [OP]**  · `keybind`
- **Fast Bandage**  · `keybind`
- **BandageSpeed**  `10..200 (def 50)`
- **Moonwalk GUI**  · `keybind`
- **Moonwalk PC**  · `keybind`
- **Fly GUI** *(Tombol)*

### Crosshair

- **Enable Crosshair**  · `keybind`
- **Style** *(Dropdown)*
- **Size**  `2..30 (def 8)`
- **Thickness**  `1..5 (def 2)`
- **Position X**  `-100..100 (def 0)`
- **Position Y**  `-100..100 (def 0)`

### Copy Avatar

- **Select Avatar** *(Dropdown)*
- **Username / ID** *(Textbox)*
- **Apply Avatar** *(Tombol)*
- **Random Avatar** *(Tombol)*
- **Reset Avatar** *(Tombol)*
- **Add to Favorite** *(Tombol)*
- **Favorites** *(Dropdown)*
- **Delete Favorite** *(Tombol)*

## 🛡️ Survivor — 8 section, 52 kontrol

### Generator Settings

- **Auto Skill Check**  · `keybind`
- **Skill Check Mode** *(Dropdown)*
- **Gen Boost Mode** *(Dropdown)*
- **Gen Boost (Multi-Repair)**  · `keybind`

### Silent Aim (Pistol)

- **Silent Aim Twist Of Fate**  · `keybind`
- **Predict Aim ToF**  · `keybind`
- **Block aim Knocked** *(Checkbox)*
- **Block Peluru (TOF)**  · `keybind`
- **Lock Aim (Twist Of Fate)**  · `keybind`
- **Wallcheck**  · `keybind`
- **Enable Laser Effect** *(default ON)*  · `keybind`
- **Silent Aim Flashlight**  · `keybind`
- **FlashHeadOffset**  `0..15 (def 1.5)`

### Anti Hook

- **Anti Hook**  · `keybind`
- **Offset**  `50..1000 (def 250)`
- **Send HZ**  `1..60 (def 44)`

### Survivor Ability

- **Instant TP Gate**  · `keybind`
- **Auto Crouch (Dodge S1)**  · `keybind`
- **Unlimited Vault**  · `keybind`
- **Anti Slow Vault**  · `keybind`
- **Flowstate No CD**  · `keybind`
- **No Fall Damage**  · `keybind`
- **Bypass Exit Gate**  · `keybind`
- **Self Heal**  · `keybind`
- **God Mode (Anti Knockdown)**  · `keybind`
- **Apply Korless** *(Tombol)*
- **Instant Escape** *(Tombol)*

### Survivor Aimbot

- **Enable Aimbot**  · `keybind`
- **Show FOV Circle** *(default ON)*  · `keybind`
- **FOV Radius**  `30..500 (def 150)`
- **Max Distance**  `50..1000 (def 300)`
- **Smoothness**  `0.1..1 (def 0.5)`
- **Predict Offset**  `0..0.1 (def 0.01)`
- **Target Part** *(Dropdown)*

### Auto Parry V1

- **Auto Parry V1**  · `keybind`
- **Custom GUI (V1)**  · `keybind`
- **Safety Parry** *(Checkbox)*
- **Aggressive Mode**  · `keybind`
- **Show Range Circle** *(default ON)*  · `keybind`
- **Parry Radius**  `5..25 (def 15)`
- **Face Sensitivity**  `-10..10 (def 7)`

### Auto Parry V2

- **Auto Parry V2**  · `keybind`
- **Safety Parry** *(Checkbox)*
- **Mode** *(Dropdown)*
- **Trigger** *(Dropdown)*
- **Killer Face**  `-1..1 (def 0.6)`
- **Show Range Circle** *(default ON)*  · `keybind`
- **Parry Radius**  `2..20 (def 12)`

### Auto Drop Pallet

- **Auto Drop Pallet**  · `keybind`
- **Safety** *(Checkbox)*
- **Trigger Distance**  `5..30 (def 10)`
- **Drop All Pallets** *(Tombol)*

## 🔪 Killer — 5 section, 26 kontrol

### Killer Aimbot

- **Enable Aimbot (Melee)**  · `keybind`
- **Max Distance**  `5..30 (def 12)`
- **Smoothness**  `0.1..1 (def 0.5)`

### Silent Veil

- **Silent Veil**  · `keybind`
- **Auto Predict**  · `keybind`
- **Show FOV** *(default ON)*  · `keybind`
- **Lead**  `0.5..5 (def 1.4)`
- **Spear Speed**  `50..200 (def 165)`
- **Spear Gravity**  `10..200 (def 103)`
- **Aura Speed**  `50..200 (def 165)`
- **Aura Gravity**  `10..200 (def 96.5)`
- **FOV**  `50..500 (def 150)`
- **Max Dist**  `50..1000 (def 500)`

### Killer Ability

- **Anti Blind (Flashlight)**  · `keybind`
- **Anti Parry**  · `keybind`
- **Infinite Lunge**  · `keybind`
- **Auto Stalk**  · `keybind`
- **No Slowdown Killer**  · `keybind`
- **Skill Hidden No CD**  · `keybind`
- **Infinite Corrupt (Abyssal)**  · `keybind`
- **Dash Lock (Hidden)**  · `keybind`
- **Mask Selection GUI**  · `keybind`
- **Aim Lock Toggle** *(Tombol)*

### Silent Aim Flask (Cure)

- **Silent Aim Flask**  · `keybind`
- **Flask Laser**  · `keybind`

### Anti Looping

- **Block Vault & Pallets**  · `keybind`

## 👁️ Visual — 4 section, 30 kontrol

### ESP Settings

- **Enable ESP**  · `keybind`
- **ESP Max Distance**  `100..5000 (def 1000)`
- **Player ESP** *(Checkbox)*
- **Killer ESP** *(Checkbox)*
- **ESP Name** *(Checkbox)*
- **ESP Distance** *(Checkbox)*
- **ESP Status survivors** *(Checkbox)*
- **ESP Item Icon** *(Checkbox)*
- **ESP Killer Warn** *(Checkbox)*
- **ESP Outline Mode** *(Checkbox)*
- **ESP Hook Count** *(Checkbox)*

### World Effects

- **Full Bright**  · `keybind`
- **Time Of Day**  `0..24 (def 14)`
- **No Fog**  · `keybind`
- **No Shadow**  · `keybind`
- **Remove Texture (Low GFX)**  · `keybind`

### Map ESP

- **Generator ESP** *(Checkbox)*
- **Generator Name & Progress** *(Checkbox)*
- **Gen Done Color** *(Color picker)*
- **Pallet ESP** *(Checkbox)*
- **Window ESP** *(Checkbox)*
- **Hook ESP** *(Checkbox)*
- **Gate ESP** *(Checkbox)*
- **SCP ESP** *(Checkbox)*
- **Refresh Map** *(Tombol)*

### Information

- **Next Killer Display**  · `keybind`
- **Next Map Prediction**  · `keybind`
- **Killer Perks Display**  · `keybind`
- **Killer Stun Indicator**  · `keybind`
- **Spectator info**  · `keybind`

## 📍 Teleport — 2 section, 9 kontrol

### Teleport Map

- **Refresh Map Cache** *(Tombol)*
- **Teleport ke Generator** *(Tombol)*
- **Teleport ke Hook** *(Tombol)*
- **Teleport ke Gate** *(Tombol)*
- **Teleport ke Pallet** *(Tombol)*
- **Teleport ke Window** *(Tombol)*

### Teleport Player

- **Select Player** *(Dropdown)*
- **Refresh Player List** *(Tombol)*
- **Teleport ke Player** *(Tombol)*

## ⚙️ Settings — 2 section, 9 kontrol

### UI Config

- **Menu Keybind** *(Keybind)*
- **Transparency Toggle**  · `keybind`
- **Lock GUI**  · `keybind`
- **Watermark**  · `keybind`
- **Always Show Mobile Button**  · `keybind`
- **Auto Fit Layar (HP)** *(default ON)*  · `keybind`
- **UI Scale (%)**
- **Reset Ukuran Window & Skala** *(Tombol)*
- **Balikin Window ke Tengah** *(Tombol)*

### Config

*(kontrolnya lewat Config Manager — lihat catatan di bawah)*

---

## Catatan

- **Config Manager** (Settings → Config) nggak kehitung di total di atas — dia komponen khusus, bukan `AddToggle`/`AddSlider`. Simpan / load / hapus config lewat `writefile`/`readfile`, maks 10 slot.

- **Fast Bandage** satu-satunya fitur yang butuh internet: masih manggil `script.panduhub.com/BoostBandage.lua`. Fitur lain jalan offline.

- **UI Scale** default 120%. Auto-fit cuma nentuin skala dasar biar window muat layar; slider UI Scale DIKALI di atasnya, jadi selalu bisa dinaikin/turunin (30–160%).

- Fitur yang butuh `writefile`/`readfile` (keybind persist, Config Manager) tetap aman di executor yang nggak nyediain — sisanya jalan normal.

