<img width="1313" height="787" alt="image" src="https://github.com/user-attachments/assets/07b7da6c-6d14-4973-a43c-bb075a35aee7" />Nhấn qua phần Actions, để tải firmware nạp .urf2

https://nickcoutsos.github.io/keymap-editor/


## 🔄 Chuyển đổi các Layer (Layer Transitions)

Bàn phím sử dụng các phím ngón cái (Thumb keys) và một số phím đặc biệt để di chuyển giữa các layer. Dưới đây là cách kích hoạt:

| Tên Layer | Phím Kích Hoạt | Thao tác | Chức năng chính |
| :--- | :--- | :--- | :--- |
| **SYMB** (1) | `Ngón cái Phải - Phím ngoài cùng` | **Giữ** (Hold) | Gõ các ký tự đặc biệt (Symbols) |
| **NUM** (2) | `Ngón cái Trái - Phím trong cùng` | **Giữ** (Hold) | Gõ số (Numpad) bên tay phải |
| **FUN** (3) | `Ngón cái Trái - Phím ngoài cùng` | **Giữ** (Hold) | Các phím F1-F12 |
| **NAV** (4) | `Ngón cái Trái - Phím giữa` <br>hoặc `Ngón cái Phải - Phím giữa` | **Giữ** (Hold) | Phím điều hướng (Mũi tên, Home/End, PgUp/Dn) |
| **MDIA** (7) | Phím `O` (Ngón út Phải, hàng giữa) | **Giữ** > 200ms | Điều khiển Nhạc (Play, Volume) và Chuột |
| **NAVL** (6) | Từ layer **FUN**, nhấn phím `J` (Ngón trỏ Phải, hàng trên) | **Nhấn** (Tap) | Chuyển hẳn (Toggle) sang layer Mũi tên trái & **Bluetooth** |
| **NWIN** (5) | Từ layer **NAV**, **giữ** phím `Shift trái` | **Giữ** (Hold) | Cụm phím tắt `Alt + [Phím]` dùng điều hướng app |

---

## 📶 Quản lý kết nối Bluetooth

Các phím điều khiển Bluetooth được đặt ở **Layer NAVL (6)**. 

**Cách vào Layer NAVL:** 1. **Giữ** phím `FUN` (Ngón cái trái ngoài cùng).
2. **Nhấn** phím `J` (Ngón trỏ phải, hàng trên cùng). 

Khi đã ở trong Layer NAVL, bạn dùng các phím sau:

| Thao tác | Vị trí phím (trên Layer NAVL) | Giải thích |
| :--- | :--- | :--- |
| **Profile 1 $\rightarrow$ 5** | 5 phím hàng trên cùng, bên tay Phải | Nhấn để chuyển đổi nhanh giữa 5 thiết bị đã kết nối. |
| **Xóa Profile (Clear)** | Phím dưới cùng, góc ngoài tay Phải (vị trí `ESC`) | Xóa bộ nhớ thiết bị hiện tại để kết nối với máy mới. |
| **Thoát về Base** | Các phím góc trên cùng / dưới cùng tay Trái | Nhấn để thoát khỏi chế độ Bluetooth, quay lại gõ phím bình thường. |

> **💡 Mẹo xử lý lỗi Bluetooth:** > Nếu không kết nối được với thiết bị cũ, hãy chọn Profile đó trên bàn phím $\rightarrow$ Nhấn **Clear** $\rightarrow$ Quên thiết bị (Forget) trên máy tính/điện thoại $\rightarrow$ Tiến hành kết nối lại từ đầu.

---

## ⚡ Các tổ hợp phím tắt nhanh (Combos)

Combos cho phép bạn nhấn cùng lúc 2-3 phím để tạo ra một phím khác, giúp hạn chế việc phải di chuyển ngón tay. Nhấn đồng thời các phím sau (sai số tối đa 50ms):

| Tổ hợp phím nhấn | Kết quả | Giải thích / Mục đích |
| :--- | :--- | :--- |
| `N` + `E` + `I` (Tay phải) | **Ctrl** (One-shot) | Nhấn nhả nhanh tạo ra phím Ctrl (chờ bấm phím tiếp theo), tiện lợi khi dùng tay phải. |
| `X` + `D` (Tay trái) | **Ctrl** (One-shot) | Tương tự như trên nhưng dành cho tay trái. |
| `Z` + `D` (Tay trái) | **Tab** | Gõ nhanh phím Tab bằng tay trái mà không cần với ngón tay lên trên. |
| `,` + `.` | `;` (Chấm phẩy) | Gõ nhanh dấu `;` để kết thúc câu lệnh khi lập trình. |
| `H` + `,` | `-` (Gạch ngang) | Gõ nhanh dấu gạch ngang/dấu trừ. |

### 0. BASE (Layer Mặc định - Colemak-DH)
Lớp gõ phím cơ bản. Phím `O` và `SPACE` được lồng tính năng giữ để chuyển layer (Hold-Tap).
```text
// -----------------------------------------------------------------------------------------
// |  TAB |  Q  |  W  |  F  |  P  |  B  |   |  J  |  L  |  U  |  Y  |  '  | BKSP |
// | CTRL |  A  |  R  |  S  |  T  |  G  |   |  M  |  N  |  E  |  I  |O/MDA| RET  |
// | SHFT |  Z  |  X  |  C  |  D  |  V  |   |  K  |  H  |  ,  |  .  |  /  | ESC  |
//                    | FUN |NV/SP| NUM |   | SHFT| NAV | SYM |

        /* LAYER 1: SYMBOLS */
// -----------------------------------------------------------------------------------------
// | TRNS |  -  |  _  |  =  |  +  |  \  |   | C_Z |  &  |  * |  .  | C_V | TRNS |
// | TRNS |  '  |  "  |  (  |  )  |  `  |   |  :  | SHFT| CTRL| ALT | GUI | TRNS |
// | TRNS |  ;  |  :  |  [  |  ]  |  ~  |   |  -  |  !  |  <  |  >  |  ?  | TRNS |
//                    | TRNS| TRNS| RET |   | TRNS| TRNS| TRNS|
        /* LAYER 2: NUM (Numpad bên phải) */
        num_layer {
// -----------------------------------------------------------------------------------------
// |  TAB | LFT |  .  | RGT |  _  | TRNS|   | TRNS|  7  |  8  |  9  |  +  | TRNS |
// | GUI  | ALT | CTRL| SHFT| NAV | TRNS|   |  :  |  4  |  5  |  6  |  -  | TRNS |
// | C_Z  | TRNS|  ,  |  :  | C_Y | TRNS|   |  -  |  1  |  2  |  3  | TRNS| TRNS |
//                    | TRNS| TRNS| TRNS|   | RET | BKSP|  0  |
        /* LAYER 3: FUN (F-Keys) */
// -----------------------------------------------------------------------------------------
// | TRNS |  1  |  2  |  3  |  4  |  5  |   | NAVL| F7  | F8  | F9  | F12 | TRNS |
// | TRNS | GUI | ALT | CTRL| SHFT| TRNS|   | TRNS| F4  | F5  | F6  | F11 | TRNS |
// | TRNS |  6  |  7  |  8  |  9  |  0  |   | TRNS| F1  | F2  | F3  | F10 | TRNS |
//                    | TRNS| TRNS| TRNS|   | TRNS| CAPS| TRNS|

        /* LAYER 4: NAV (Điều hướng & Thao tác) */
// -----------------------------------------------------------------------------------------
// | ALTB | S_TB| C_W | C_TB| ALTB| TRNS|   | PGUP| HOME|  UP | END |C_BSP| TRNS |
// | GUI  | ALT | CTRL| SHFT| NWIN| TRNS|   | PGDN| LFT | DWN | RGT | SPC | TRNS |
// | C_Z  | C_X | C_C | C_V | C_Y | TRNS|   | ESC | BKSP| RET | TAB | DEL | TRNS |
//                    | TRNS| TRNS| TRNS|   | RET | BKSP| TRNS|

        /* LAYER 5: NAV WIN (Alt + Phím) */
// -----------------------------------------------------------------------------------------
// | TRNS | A_Q | A_W | A_F | A_P | A_B |   | A_J | A_7 | A_8 | A_9 | A_' | TRNS |
// | TRNS | GUI | ALT | CTRL| SHFT| TRNS|   | A_M | A_4 | A_5 | A_6 | A_O | TRNS |
// | TRNS | A_Z | A_X | A_C | A_D | A_V |   | A_K | A_1 | A_2 | A_3 | A_/ | TRNS |
//                    | TRNS| TRNS| TRNS|   | TRNS| TRNS| TRNS|

        /* LAYER 6: NAV LEFT (Mũi tên tay trái) */
// -----------------------------------------------------------------------------------------
// | BASE | HOME|  UP | END | PGUP| TRNS|   | BT0 | BT1 | BT2 | BT3 | BT4 | BASE |
// | SPC  | LFT | DWN | RGT | PGDN| TRNS|   | TRNS| SHFT| CTRL| ALT | GUI | TRNS |
// | DEL  | TAB | RET | BKSP| ESC | TRNS|   | TRNS| TRNS| TRNS| TRNS| TRNS|BTCLR |
//                    | BASE| BASE| TRNS|   | RET | BKSP| TRNS|

        /* LAYER 7: MEDIA & MOUSE */
// -----------------------------------------------------------------------------------------
// | RESET| TRNS| TRNS| TRNS| TRNS| TRNS|   | S_UP| PREV| M_UP| NEXT| PSCR| TRNS |
// | GUI  | ALT | CTRL| SHFT| TRNS| TRNS|   | S_DN| M_LF| M_DN| M_RT| TRNS| TRNS |
// | TRNS | TRNS| TRNS| TRNS| TRNS| TRNS|   | MUTE| V_DN| PP  | V_UP| TRNS| TRNS |
//                    | TRNS| TRNS| TRNS|   | MB3 | MB1 | MB2 |
        };
    };
};****
