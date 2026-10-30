# Aeris Hub — Violence District (no key)

Versi **tanpa key system** dari Aeris Hub VD. Key check (menu verifikasi, `REQUIRED_KEY`,
file `Aeris/key_<userId>.json`, badge "Aeris Verified", countdown key di sidebar) sudah dibuang
total — script langsung jalan begitu di-execute.

- File: `Aeris_Hub_nokey.lua` (17.011 baris)
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

## Catatan

- Fast Bandage masih memanggil `script.panduhub.com/BoostBandage.lua` (fitur lain tidak butuh internet).
- Key removal diverifikasi: compile Luau lolos, 0 sisa referensi key, dan jalan di test harness
  (splash + UI kebentuk tanpa prompt key).
- Script aslinya milik tim Aeris Hub; repo ini cuma versi yang key-nya sudah dilepas.
