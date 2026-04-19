# 🦕 Dino Runner

Bản tái tạo game khủng long offline của Google Chrome — với các tính năng nâng cấp độc quyền.

## Chơi ngay

Chỉ cần mở `index.html` trong trình duyệt. Không cần server, không cần cài đặt.

> Hoặc deploy lên GitHub Pages: `Settings → Pages → Branch: main → / (root)`

---

## Điều khiển

| Phím | Hành động |
|------|-----------|
| `SPACE` / `↑` | Nhảy (nhảy đôi được hỗ trợ) |
| `Z` | Bắn súng (mở khóa sau 1000 điểm) |
| Chạm màn hình | Nhảy (mobile) |

---

## Tính năng nâng cấp

### Mốc điểm
| Điểm | Phần thưởng |
|------|------------|
| **100** | 🦅 Thằn lằn bay đồng hành — bay phía sau, tự động tiêu diệt thằn lằn bay kẻ thù |
| **250** | 🛸 UFO bảo vệ — bay phía trước, tự động bắn nổ chướng ngại vật (hồi chiêu 2s) |
| **500** | 🪣 Thùng gỗ xuất hiện — va vào bị chậm và giảm tốc độ |
| **600** | 🟢 Slime xuất hiện — va vào giảm tốc 20% trong 5 giây |
| **1000** | 🔫 Súng gắn lưng — nhấn `Z` để bắn (hồi chiêu 5s) |
| **Mỗi 100** | ⚡ Tốc độ tăng +0.5 |

### Powerup ngẫu nhiên (mỗi ~15 giây)
- ★ **Bất tử 5 giây** — không bị sát thương
- ▣ **Khiên bảo vệ** — hấp thụ 1 đòn

### Chướng ngại vật
- 🌵 Xương rồng (single / double)
- 🦅 Thằn lằn bay (3 mực độ cao)
- 🪣 Thùng gỗ (500+) — vỡ khi va, giảm tốc
- 🟢 Slime (600+) — di chuyển nhanh, giảm tốc tạm thời

---

## Cấu trúc file

```
dino-runner/
├── index.html   ← khung HTML
├── style.css    ← giao diện
├── game.js      ← toàn bộ logic game
└── README.md
```

---

## Tùy chỉnh

Mở `game.js` và chỉnh các hằng số ở đầu file:

```js
const W      = 800;   // chiều rộng canvas
const H      = 320;   // chiều cao canvas
const GROUND = 240;   // vị trí mặt đất
```

Tốc độ khởi đầu và tốc độ tăng theo mốc:
```js
game.speed     = 6;        // tốc độ ban đầu
// Mỗi 100 điểm: speed += 0.5  (dòng ~130 trong game.js)
```

---

## License

MIT — dùng thoải mái, chơi thoải mái.
