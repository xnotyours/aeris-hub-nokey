# Aeris Hub — Violence District (no key)

Versi **tanpa key system** dari Aeris Hub VD. Key check (menu verifikasi, `REQUIRED_KEY`,
file `Aeris/key_<userId>.json`, badge "Aeris Verified", countdown key di sidebar) sudah dibuang
total — script langsung jalan begitu di-execute.

- File: `Aeris_Hub_nokey.lua` (17.131 baris)
- Platform: Roblox executor (butuh `require`, `firesignal`, `gethui`, `writefile`/`readfile` opsional)
- Place: [BUTCHER] Violence District (PlaceId `93978595733734`)
- UI: engine sendiri (nggak HttpGet library luar)

## Cara pakai

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/xnotyours/aeris-hub-nokey/main/Aeris_Hub_nokey.lua"))()
```

## Fitur

6 tab, 30 section, ±223 kontrol (81 toggle, 41 slider, 21 checkbox, 36 keybind, 20 tombol, 12 color picker, 10 dropdown):

- **Main** — Auto Vault/Pallet Slide/Auto Run, Speed Boost, Skip Endscreen, Fake Perks (Quick Recovery,
  Perfect Landing, Flowstate, Adrenaline Rush, Perk Cooldown), Stretch Res, Third Person, Infinity Zoom,
  Camera FOV, DBD Camera (8 slider), Streamer Mode, Invisibility, Fast Bandage, Moonwalk, Fly GUI,
  Crosshair, Copy Avatar + Favorites
- **Survivor** — Auto Skill Check + Skill Check Mode (Legit/Instant/Normal/Random), Gen Boost
  (Multi-Repair), Silent Aim Pistol (ToF, Predict ToF, Block Knocked/Peluru, Lock Aim, Wallcheck,
  Laser, Flashlight), Anti Hook, Survivor Ability (Instant TP Gate, Auto Crouch/Dodge S1, Unlimited
  Vault, Anti Slow Vault, Flowstate No CD, No Fall Damage, Bypass Exit Gate, Self Heal, God Mode,
  Korless, Instant Escape), Survivor Aimbot (+Target Part), Auto Parry V1 & V2, Auto Drop Pallet
- **Killer** — Killer Aimbot (melee), Silent Veil (Auto Predict, FOV, Lead, Spear/Aura speed-gravity),
  Anti Blind, Anti Parry, Infinite Lunge, Auto Stalk, No Slowdown, Skill Hidden No CD, Infinite Corrupt,
  Dash Lock, Mask GUI, Silent Aim Flask + Flask Laser, Anti Looping (Block Vault & Pallets)
- **Visual** — ESP (player/killer/name/distance/status/item icon/warn/outline/hook count), World
  Effects (Fullbright, Time of Day, No Fog, No Shadow, Low GFX), Map ESP (generator +progress, pallet,
  window, hook, gate, SCP), Information (Next Killer, Next Map, Killer Perks, Stun Indicator, Spectator)
- **Teleport** — Generator/Hook/Gate/Pallet/Window (gantian), Select Player + TP ke player
- **Settings** — UI Config (transparency, lock, watermark, mobile button) + Config Manager


## Fix layar HP (UI Scale)

Window-nya fixed 690x470 px, jadi di HP keliatan kebesaran sampai keluar layar. Sekarang
ada `UIScale` di frame window + auto-fit:

- **Auto Fit Layar (HP)** — default NYALA. Window ngecil otomatis kalau viewport sempit
  (dan tetap 1:1 kayak aslinya di PC, karena fit cuma bisa ngecil, max 1.0). Window boleh
  makan sampai **95% lebar & 92% tinggi** area yang kepake (naik dari 88%/82% biar nggak
  kekecilan di HP).
- **UI Scale (%)** — slider manual 50–160% kalau mau lebih kecil/besar.
- **Reset Ukuran Window & Skala** — balikin auto-fit + 100%.
- Auto-update kalau layar dirotasi / window di-resize (dengerin `ViewportSize`).

Hitungan dari rumus auto-fit (bukan test di device, cuma aritmatika):

- PC 1280x720 → scale 1.000 (690x470 px)
- HP 812x375 → scale 0.734 (506x345 px)
- HP kecil 480x260 → scale 0.509 (351x239 px)


## Anti nyangkut di luar layar (posisi window)

Dulu window bisa di-drag sampai headernya lewat atas layar. Begitu header hilang, nggak ada
lagi bagian yang bisa dipegang buat narik balik — satu-satunya jalan adalah re-execute
script. Sekarang:

- **Drag di-clamp** — tiap geser, posisi window diukur ulang (`AbsolutePosition`) dan
  ditahan biar selalu utuh di dalam viewport, jadi header mustahil kabur ke atas.
- **Clamp ikut jalan saat resize & ganti skala/layar** — gedein window atau rotasi HP
  nggak bisa bikin sisi lain kelewat layar. Kalau window beneran lebih gede dari layar,
  dia dipaku ke pinggir atas/kiri supaya header tetap kejangkau.
- **Lock GUI beneran ngunci** — toggle di Settings → UI Config sekarang menahan drag &
  resize (sebelumnya cuma nyimpen flag yang nggak ada pengeceknya, jadi keliatan nyala
  padahal window masih bisa digeser).
- **Balikin Window ke Tengah** — tombol recovery di Settings → UI Config, buat balikin
  posisi kalau window udah kepepet di pinggir.
- **Reset Ukuran Window & Skala** sekarang juga balikin ukuran window ke 690x470 desain
  (dulu resize nggak punya jalan balik sama sekali).
- Tombol buka menu di HP (floating button) juga di-clamp — nggak bisa lagi ditarik ke
  luar layar sampai menunya nggak bisa dibuka.
- **Re-inject bersih** — execute ulang script sekarang ngebuang GUI lama dulu
  (`Aeris_MainHub`, notifikasi, watermark), jadi nggak numpuk kalau lagi balikin keadaan.

Catatan teknis: offset `Position` yang di-skala `UIScale` itu ambigu di Roblox, jadi clamp-nya
nggak nebak — dia geser, ukur hasil aslinya, terus koreksi sisa error pakai faktor hasil ukur.
Diuji di harness 2 semantik (offset di-skala / 1:1), dua-duanya lolos.


## Minimize — auto hide total

Minimize (`-`) sekarang **sembunyi total**: window ditutup dan yang kelihatan cuma tombol
floating bulat 48x48 di **pojok kanan atas** (di bawah top bar Roblox, ngikutin
`GuiService:GetGuiInset()`). Nggak ada lagi bar/pill setengah-setengah yang bisa kesenggol
terus kebuka sendiri pas lagi main.

- **Tap tombol floating** → window kebuka lagi dalam ukuran penuh.
- **Tombol `-` dan `X` sama-sama nutup** ke tombol floating — dua-duanya bisa dibuka lagi.
- **Tombol floating bisa di-drag** kalau mau dipindah, dan tetap di-clamp biar nggak bisa
  dibuang keluar layar (kalau hilang, menunya nggak bisa dibuka lagi di HP).
- **"Selalu tampil tombolnya"** di Settings → UI Config kalau mau tombol floating tetap
  kelihatan walau menunya lagi kebuka.
- **Tap dua kali di header buat minimize sudah dihapus** — itu yang tadi bikin window kebuka
  sendiri cuma gara-gara kegeser/kesenggol.
- **Reset Ukuran Window** balikin window ke 690x470 desain dan matiin state minimize.


## Branding

- **Splash screen dihapus** — layar putih + logo "Aeris. / All for you" yang muncul 6 detik
  (1s fade in → 4s hold → 1s fade out) sudah dibuang total. Script langsung masuk ke menu,
  dan startup jadi ~6 detik lebih cepat.
- **Watermark default OFF** — badge "Aeris" di kiri atas nggak nempel lagi. Mau dinyalain?
  Settings → UI Config → Watermark.
- Yang masih ada: logo + judul "Aeris Hub" di header window.

## Catatan

- Fast Bandage masih memanggil `script.panduhub.com/BoostBandage.lua` (fitur lain tidak butuh internet).
- Key removal diverifikasi: compile Luau lolos, 0 sisa referensi key, dan jalan di test harness
  (splash + UI kebentuk tanpa prompt key).
- Script aslinya milik tim Aeris Hub; repo ini cuma versi yang key-nya sudah dilepas.
