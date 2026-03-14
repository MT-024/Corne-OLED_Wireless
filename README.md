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

default_layer {
            bindings = <
&kp TAB    &kp Q      &kp W      &kp F      &kp P          &kp B           &kp J       &kp L          &kp U      &kp Y      &kp SQT          &kp BSPC
&kp LCTRL  &kp A      &kp R      &kp S      &kp T          &kp G           &kp M       &kp N          &kp E      &kp I      &lt_media MDIA O &kp RET
&kp LSHFT  &kp Z      &kp X      &kp C      &kp D          &kp V           &kp K       &kp H          &kp COMMA  &td_dot    &kp FSLH         &kp ESC
                                 &mo FUN    &lt NAV SPACE  &mo NUM         &skq LSHFT  &mo NAV        &mo SYMB
            >;
        };

        /* LAYER 1: SYMBOLS */
        sym_layer {
            bindings = <
&trans     &kp MINUS  &kp UNDER  &kp EQUAL  &kp PLUS       &kp BSLH        &kp LC(Z)   &kp LS(N7)     &kp LS(N8) &kp DOT    &kp LC(V)  &trans
&trans     &kp SQT    &kp DQT    &kp LPAR   &kp RPAR       &kp GRAVE       &kp COLON   &skq LSHFT     &skq LCTRL &skq LALT  &skq LGUI  &trans
&trans     &kp SEMI   &kp COLON  &kp LBKT   &kp RBKT       &kp TILDE       &kp MINUS   &kp EXCL       &kp LT     &kp GT     &kp QMARK  &trans
                                 &trans     &trans         &kp RET         &trans      &trans         &trans
            >;
        };

        /* LAYER 2: NUM (Numpad bên phải) */
        num_layer {
            bindings = <
&kp ESC    &kp LEFT   &kp DOT    &kp RIGHT  &kp UNDER      &trans          &trans      &kp N7         &kp N8     &kp N9     &kp PLUS   &trans
&skq LGUI  &skq LALT  &skq LCTRL &skq LSHFT &mo NAV        &trans          &kp COLON   &kp N4         &kp N5     &kp N6     &kp MINUS  &trans
&kp LC(Z)  &trans     &kp COMMA  &kp COLON  &kp LC(Y)      &trans          &kp MINUS   &kp N1         &kp N2     &kp N3     &trans     &trans
                                 &trans     &trans         &trans          &kp RET     &kp BSPC       &kp N0
            >;
        };

        /* LAYER 3: FUN (F-Keys) */
        fun_layer {
            bindings = <
&trans     &kp N1     &kp N2     &kp N3     &kp N4         &kp N5          &to NAVL    &kp F7         &kp F8     &kp F9     &kp F12    &trans
&trans     &skq LGUI  &skq LALT  &skq LCTRL &skq LSHFT     &trans          &trans      &kp F4         &kp F5     &kp F6     &kp F11    &trans
&trans     &kp N6     &kp N7     &kp N8     &kp N9         &kp N0          &trans      &kp F1         &kp F2     &kp F3     &kp F10    &trans
                                 &trans     &trans         &trans          &trans      &kp CAPS       &trans
            >;
        };

        /* LAYER 4: NAV (Điều hướng & Thao tác) */
        nav_layer {
            bindings = <
&alt_tab   &kp LS(TAB) &kp LC(W)  &kp LC(TAB) &alt_tab     &trans          &kp PG_UP   &kp HOME       &kp UP     &kp END    &kp LC(BSPC) &trans
&skq LGUI  &skq LALT   &skq LCTRL &skq LSHFT  &mo NWIN     &trans          &kp PG_DN   &kp LEFT       &kp DOWN   &kp RIGHT  &kp SPACE  &trans
&kp LC(Z)  &kp LC(X)   &kp LC(C)  &kp LC(V)   &kp LC(Y)    &trans          &kp ESC     &kp BSPC       &kp RET    &kp TAB    &kp DEL    &trans
                                  &trans      &trans       &trans          &kp RET     &kp BSPC       &trans
            >;
        };

        /* LAYER 5: NAV WIN (Alt + Phím) */
        navwin_layer {
            bindings = <
&trans     &kp LA(Q)  &kp LA(W)  &kp LA(F)  &kp LA(P)      &kp LA(B)       &kp LA(J)   &kp LA(N7)     &kp LA(N8) &kp LA(N9) &kp LA(SQT)  &trans
&trans     &skq LGUI  &skq LALT  &skq LCTRL &skq LSHFT     &trans          &kp LA(M)   &kp LA(N4)     &kp LA(N5) &kp LA(N6) &kp LA(O)    &trans
&trans     &kp LA(Z)  &kp LA(X)  &kp LA(C)  &kp LA(D)      &kp LA(V)       &kp LA(K)   &kp LA(N1)     &kp LA(N2) &kp LA(N3) &kp LA(FSLH) &trans
                                 &trans     &trans         &trans          &trans      &trans         &trans
            >;
        };

        /* LAYER 6: NAV LEFT (Mũi tên tay trái) */
        navl_layer {
            bindings = <
&to BASE   &kp HOME   &kp UP     &kp END    &kp PG_UP      &trans          &bt BT_SEL 0 &bt BT_SEL 1  &bt BT_SEL 2 &bt BT_SEL 3 &bt BT_SEL 4 &to BASE
&kp SPACE  &kp LEFT   &kp DOWN   &kp RIGHT  &kp PG_DN      &trans          &trans       &skq LSHFT    &skq LCTRL   &skq LALT    &skq LGUI    &trans
&kp DEL    &kp TAB    &kp RET    &kp BSPC   &kp ESC        &trans          &trans       &trans        &trans       &trans       &trans       &bt BT_CLR
                                 &to BASE   &to BASE       &trans          &kp RET      &kp BSPC      &trans
            >;
        };

        /* LAYER 7: MEDIA & MOUSE */
        media_layer {
            bindings = <
&sys_reset &trans     &trans     &trans     &trans         &trans          &msc SCRL_UP   &kp C_PREV  &mmv MOVE_UP   &kp C_NEXT &kp PSCRN &trans
&skq LGUI  &skq LALT  &skq LCTRL &skq LSHFT &trans         &trans          &msc SCRL_DOWN &mmv MOVE_LEFT &mmv MOVE_DOWN &mmv MOVE_RIGHT &trans &trans
&trans     &trans     &trans     &trans     &trans         &trans          &kp C_MUTE     &kp C_VOL_DN   &kp C_PP       &kp C_VOL_UP    &trans &trans
                                 &trans     &trans         &trans          &mkp MB3       &mkp MB1       &mkp MB2
            >;
        };
    };
};****
