

### **1. Các gói cơ bản bắt buộc**
- **Hyprland**: Compositor Wayland chính.
- **waybar**: Thanh panel (có thể thay thế bằng **eww** nếu muốn custom phức tạp).
- **rofi** hoặc **wofi**: Application launcher (chạy trên Wayland).
- **swaylock** hoặc **swaylock-effects**: Khóa màn hình.
- **swayidle**: Quản lý trạng thái idle (sleep, lock...).
- **networkmanager**: Quản lý mạng (có thể dùng **iwd** nếu muốn nhẹ).
- **pulseaudio** hoặc **pipewire**: Hệ thống âm thanh.

---

### **2. Các công cụ hỗ trợ giao diện**
- **swaybg** hoặc **swayimg**: Đặt hình nền.
- **grim** + **slurp**: Chụp màn hình và chọn vùng.
- **wl-clipboard**: Quản lý clipboard.
- **mako** hoặc **dunst**: Notifications.
- **gammastep** hoặc **wlsunset**: Điều chỉnh nhiệt độ màu màn hình (giống f.lux).

---

### **3. Các gói tùy chọn nâng cao**
- **eww**: Tạo widget custom (thanh panel, hệ thống...).
- **pyprland**: Plugin Python để mở rộng tính năng Hyprland.
- **swaync**: Notification center đẹp hơn.
- **wf-recorder**: Quay màn hình.
- **hyprpaper**: Công cụ quản lý hình nền đa màn hình.
- **xdg-desktop-portal-hyprland**: Hỗ trợ screencast, file picker...

---

### **4. Các công cụ theming**
- **gtk3** và **gtk4**: Để ứng dụng GTK hiển thị đúng.
- **qt5ct** + **qt6ct**: Chỉnh theme cho ứng dụng Qt.
- **lxsession**: Quản lý session (tùy chọn).
- **nwg-look**: Công cụ chỉnh theme GTK/Qt dễ dàng.

---

### **5. Fonts và Icons**
- **ttf-font-awesome**: Icon phổ biến cho thanh panel.
- **ttf-nerd-fonts-symbols**: Font đẹp cho terminal và widgets.
- **noto-fonts**: Font mặc định đẹp, hỗ trợ Unicode.
- **papirus-icon-theme**: Bộ icon đẹp.

---

### **6. Scripts và tiện ích nhỏ**
- **brightnessctl** hoặc **light**: Điều chỉnh độ sáng.
- **playerctl**: Điều khiển media (play/pause/next).
- **polkit**: Quản lý quyền root (cần cho các ứng dụng như `gnome-disk-utility`).

---

### **7. Cài đặt cơ bản (ví dụ trên Arch Linux)**
```bash
# Cài đặt Hyprland và các gói chính
yay -S hyprland waybar rofi swaylock swayidle networkmanager pipewire grim slurp wl-clipboard mako gammastep

# Các gói tùy chọn
yay -S eww pyprland swaync wf-recorder hyprpaper xdg-desktop-portal-hyprland

# Font và theme
yay -S ttf-font-awesome ttf-nerd-fonts-symbols noto-fonts papirus-icon-theme nwg-look

# Tiện ích
yay -S brightnessctl playerctl polkit
```

---

### **8. Lưu ý quan trọng**
- Đảm bảo bạn đã bật **XDG Desktop Portal**:
  ```bash
  systemctl enable --now xdg-desktop-portal-hyprland
  ```
- Cấu hình Hyprland nằm ở `~/.config/hypr/hyprland.conf` (tạo nếu chưa có).
- Nếu dùng **NVIDIA**, cần thêm biến môi trường vào file cấu hình:
  ```ini
  env = LIBVA_DRIVER_NAME,nvidia
  env = GBM_BACKEND,nvidia-drm
  env = __GLX_VENDOR_LIBRARY_NAME,nvidia
  ```

---

### **Kết quả mong đợi**
- Một hệ thống Hyprland mượt mà, hỗ trợ animation và transparency.
- Thanh **waybar** hoặc **eww** đẹp với nhiều module (CPU, RAM, network...).
- Notification đẹp với **swaync** hoặc **mako**.
- Hình nền động hoặc slideshow với **hyprpaper**.
