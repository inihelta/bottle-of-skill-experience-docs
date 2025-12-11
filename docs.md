# Panduan Skill Bottle

## Apa itu Skill Bottle?
**Skill Bottle** adalah item khusus berupa potion yang berisi pengalaman untuk meningkatkan skill dari aurelium skill. Pemain dapat mengkonsumsi (minum) item ini untuk mendapatkan poin pengalaman di skill pilihan mereka.

## Fitur Utama
- 💎 **3 Tingkatan** - Tier I, II, dan III dengan reward pengalaman berbeda
- 🎯 **15 Skill Berbeda** - Pilih skill mana yang ingin ditingkatkan
- 🎮 **Antarmuka Mudah** - Menu GUI yang user-friendly
- 🔊 **Feedback Visual** - Suara dan pesan konfirmasi saat menggunakan

---

## Perintah (Commands)

- `/skillbottle <tier>` — Buka GUI Skill Bottle untuk memilih item.
   - Contoh: `/skillbottle 1` (Tier I)
   - Permission: `admin`
- `/skillbottle-give <skill> <tier> <player>` — Berikan Bottle langsung ke pemain.
   - Contoh: `/skillbottle-give Archery 2 SomePlayer` (memberi Tier II Archery)
   - Permission: `admin`

---

## Perilaku Saat Dikonsumsi (Consume Behavior)

- Saat diminum, pemain akan:
   - Mendapatkan item (potion) di-inventory jika diambil dari GUI,
   - Mendengar suara `entity.experience_orb.pickup`.
   - Menerima XP skill melalui perintah konsol yang dieksekusi oleh script: `/skill xp add <player> <skill> <xp>`.
   - Nilai XP sesuai tier:
   - Tier I = `1000 XP`
   - Tier II = `5000 XP`
   - Tier III = `10000 XP`

---

## Quick Reference

- GUI: `/skillbottle <1|2|3>`
- Give langsung: `/skillbottle-give <SkillName> <1|2|3> <player>`
<!-- - Consume → executes: `/skill xp add <player> <skill> <1000|5000|10000>` -->

## Cara Menggunakan Untuk Pemain

### Langkah-Langkah:
1. **Terima Skill Bottle** dari Admin
   - Admin akan memberikan potion Skill Bottle kepada Anda
   
2. **Buka Skill Bottle**
   - Klik kanan (atau konsumsi) potion di inventory Anda
   - Potion akan "diminum" dan Anda akan mendapatkan pengalaman
   
3. **Lihat Hasilnya**
   - Pengalaman skill Anda akan bertambah secara otomatis
   - Anda akan mendengar suara "experience orb pickup"

### Contoh:
- Jika Anda memiliki **Bottle o' Skill (Tier I)** untuk **Archery**
- Minum potion tersebut → Dapatkan **1000 XP Archery**

---

## Cara Untuk Admin

### Memberikan Skill Bottle kepada Pemain:

1. **Buka Menu Skill Bottle**
   ```
   /skillbottle 1
   /skillbottle 2
   /skillbottle 3
   ```
   - **1** = Tier I (1000 XP per skill)
   - **2** = Tier II (5000 XP per skill)
   - **3** = Tier III (10000 XP per skill)

2. **Pilih Skill yang Ingin Diberikan**
   - Menu akan menampilkan 15 skill berbeda
   - Klik skill yang diinginkan untuk menerima itemnya

3. **Berikan ke Pemain**
   - Drag & drop atau gunakan perintah give untuk memberikan ke pemain lain

---

## Tingkatan Skill Bottle

| Tingkatan    | XP per Penggunaan |
| ------------ | ----------------- |
| **Tier I**   | 1000 XP           |
| **Tier II**  | 5000 XP           |
| **Tier III** | 10000 XP          |

---

## Daftar 15 Skill

1. **Agility** - Increases player mobility and movement
2. **Alchemy** - Enhances potion-related abilities
3. **Archery** - Improves bow combat effectiveness
4. **Defense** - Boosts defensive capabilities
5. **Enchanting** - Enhances item enchantment skills
6. **Endurance** - Increases stamina and durability
7. **Excavation** - Improves mining and digging speed
8. **Farming** - Enhances crop growth and harvesting
9. **Fighting** - Increases melee combat damage
10. **Fishing** - Improves fishing success rates
11. **Foraging** - Enhances resource gathering
12. **Forging** - Increases crafting and smithing abilities
13. **Healing** - Improves healing effectiveness
14. **Mining** - Increases mining speed and ore extraction
15. **Sorcery** - Enhances magic-related abilities

---

## Item Specifications

### Model Data IDs
setiap skill bottle memiliki custom model data tersendiri untuk custom texturing:

| Skill      | Model Data | Color             |
| ---------- | ---------- | ----------------- |
| Agility    | 22210      | Green (`&a`)      |
| Alchemy    | 22211      | Magenta (`&d`)    |
| Archery    | 22212      | Gold (`&6`)       |
| Defense    | 22213      | Blue (`&9`)       |
| Enchanting | 22214      | Purple (`&5`)     |
| Endurance  | 22215      | Yellow (`&e`)     |
| Excavation | 22216      | Gray (`&7`)       |
| Farming    | 22217      | Dark Green (`&2`) |
| Fighting   | 22218      | Red (`&c`)        |
| Fishing    | 22219      | Cyan (`&b`)       |
| Foraging   | 22220      | Dark Green (`&2`) |
| Forging    | 22221      | Gold (`&6`)       |
| Healing    | 22222      | Magenta (`&d`)    |
| Mining     | 22223      | Dark Gray (`&8`)  |
| Sorcery    | 22224      | Purple (`&5`)     |

---

## Permission & Dependencies

- Permission untuk membuka GUI dan memberi item: `admin`/`Operator`
- Dependencies:
   - `Skript` (plugin Skript)
   - `Aurelium Skills` (atau plugin skill yang menyediakan `/skill xp add`)

---
