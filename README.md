# EZYCLOUDX

Ứng dụng desktop EZYCLOUDX cho macOS và Windows: đăng nhập, quản lý và kết nối tới Cloud PC của bạn
với độ trễ thấp. Repo này chỉ chứa các bản phát hành, không có mã nguồn.

> English below.

## Tải về

| Hệ điều hành | Tệp | Yêu cầu |
| --- | --- | --- |
| macOS | `EZC_<version>_universal.dmg` | macOS 13 trở lên, Apple Silicon hoặc Intel |
| Windows | `EZC_<version>_x64-setup.exe` | Windows 10 (1903 trở lên) hoặc Windows 11, 64-bit |

- Bản mới nhất: [Releases, Latest](https://github.com/ezycloudx/ezc-app-release/releases/latest)
- macOS, link cố định tới bản mới nhất:
  [EZC_universal.dmg](https://github.com/ezycloudx/ezc-app-release/releases/latest/download/EZC_universal.dmg)
- Hoặc tải ở trang [ezycloudx.com/download](https://www.ezycloudx.com/download)

Bản có nhãn **Pre-release** là bản thử nghiệm nội bộ; hãy dùng bản **Latest**.

## Cài trên macOS

1. Mở tệp `.dmg` vừa tải, kéo **EZYCLOUDX** vào thư mục **Applications**.
2. Mở **EZYCLOUDX** từ Applications (hoặc Launchpad).

### Nếu macOS chặn ứng dụng (Gatekeeper)

Ứng dụng hiện chưa được Apple notarize, nên **ở lần cài đầu tiên** macOS sẽ chặn **hai lần**: khi mở
tệp `.dmg`, và khi mở ứng dụng sau khi đã kéo vào Applications. Mỗi lần:

1. Bấm **Done** (không bấm *Move to Trash*).
2. Mở **System Settings**, chọn **Privacy & Security**, kéo xuống mục **Security**.
3. Bấm **Open Anyway** cạnh dòng báo về EZYCLOUDX, rồi xác nhận bằng mật khẩu hoặc Touch ID.
4. Mở lại tệp hoặc ứng dụng, bấm **Open**.

Cách khác, bằng Terminal (thay đường dẫn nếu bạn để tệp ở chỗ khác):

```bash
xattr -dr com.apple.quarantine ~/Downloads/EZC_*_universal.dmg
xattr -dr com.apple.quarantine /Applications/EZYCLOUDX.app
```

Chỉ cần làm một lần: các bản cập nhật sau tự cài từ bên trong ứng dụng và không bị chặn.

### Quyền trên macOS

- **Microphone**: macOS hỏi ở lần đầu bạn bật micro trong stream. Nếu đã từ chối:
  System Settings, Privacy & Security, Microphone, bật EZYCLOUDX.
- **Accessibility**: cần để gửi các phím tắt hệ thống (Command-Tab, Command-Space) tới máy từ xa:
  System Settings, Privacy & Security, Accessibility, bật EZYCLOUDX.

## Cài trên Windows

1. Mở tệp `EZC_<version>_x64-setup.exe` vừa tải và làm theo bộ cài. Ứng dụng cài cho tài khoản của
   bạn, **không cần quyền quản trị**; nếu máy chưa có Microsoft Edge WebView2, bộ cài tự tải về.
2. Mở **EZYCLOUDX** từ Start menu.

### Nếu trình duyệt hoặc Windows chặn bộ cài

Bộ cài hiện chưa có chữ ký số, nên **ở lần đầu**:

- Trình duyệt có thể giữ tệp lại: chọn **Keep** (Edge: dấu ba chấm, **Keep**, rồi **Keep anyway**).
- SmartScreen báo **Windows protected your PC**: bấm **More info**, rồi **Run anyway**.

Các bản cập nhật sau tự cài từ bên trong ứng dụng và không gặp SmartScreen.

## Cập nhật

Ứng dụng tự kiểm tra và tải bản mới ở chế độ nền, rồi cài khi không có stream nào đang chạy. Nếu
ứng dụng báo **cần cập nhật** khi mở, phiên bản của bạn đã quá cũ để kết nối: bấm **Cập nhật**, ứng
dụng sẽ khởi động lại ở bản mới.

## Kiểm tra tệp tải về (không bắt buộc)

Mỗi bản phát hành có `SHA256SUMS` (macOS) và `SHA256SUMS-windows` (Windows).

```bash
# macOS, trong thư mục chứa tệp đã tải và SHA256SUMS
shasum -a 256 -c SHA256SUMS --ignore-missing
```

```powershell
# Windows PowerShell: so với dòng tương ứng trong SHA256SUMS-windows
Get-FileHash .\EZC_<version>_x64-setup.exe -Algorithm SHA256
```

## Gỡ cài đặt

- **macOS:** thoát ứng dụng, kéo **EZYCLOUDX** trong Applications vào Trash.
- **Windows:** Settings, Apps, Installed apps, **EZYCLOUDX**, Uninstall.

## Hỗ trợ

Khi liên hệ bộ phận hỗ trợ, gửi kèm **phiên bản** và **mã cài đặt** của ứng dụng (ở menu tài khoản
hoặc trang Hỗ trợ trong ứng dụng). Hướng dẫn đầy đủ: trang **Hướng dẫn** trong console.

[Chính sách quyền riêng tư](https://www.ezycloudx.com/privacy-policy) ·
[Điều khoản dịch vụ](https://www.ezycloudx.com/terms-of-service)

---

# EZYCLOUDX (English)

The EZYCLOUDX desktop app for macOS and Windows: sign in, manage and connect to your Cloud PC with
low latency. This repository holds releases only, no source code.

## Download

| OS | File | Requirements |
| --- | --- | --- |
| macOS | `EZC_<version>_universal.dmg` | macOS 13 or later, Apple Silicon or Intel |
| Windows | `EZC_<version>_x64-setup.exe` | Windows 10 (1903 or later) or Windows 11, 64-bit |

- Latest release: [Releases, Latest](https://github.com/ezycloudx/ezc-app-release/releases/latest)
- macOS, a fixed link to the latest:
  [EZC_universal.dmg](https://github.com/ezycloudx/ezc-app-release/releases/latest/download/EZC_universal.dmg)
- Or from [ezycloudx.com/en/download](https://www.ezycloudx.com/en/download)

Releases marked **Pre-release** are internal test builds; use the **Latest** one.

## Install on macOS

1. Open the downloaded `.dmg` and drag **EZYCLOUDX** into **Applications**.
2. Open **EZYCLOUDX** from Applications (or Launchpad).

### If macOS blocks the app (Gatekeeper)

The app is not notarized by Apple yet, so **on the first install only** macOS blocks it **twice**:
when you open the `.dmg`, and when you open the app after copying it to Applications. Each time:

1. Press **Done** (not *Move to Trash*).
2. Open **System Settings**, **Privacy & Security**, and scroll to **Security**.
3. Press **Open Anyway** next to the line about EZYCLOUDX, and confirm with your password or
   Touch ID.
4. Open the file or the app again and press **Open**.

Or in Terminal (adjust the paths if your files are elsewhere):

```bash
xattr -dr com.apple.quarantine ~/Downloads/EZC_*_universal.dmg
xattr -dr com.apple.quarantine /Applications/EZYCLOUDX.app
```

This is needed once: later updates install from inside the app and are not blocked.

### Permissions on macOS

- **Microphone**: macOS asks the first time you turn the microphone on in a stream. If you declined:
  System Settings, Privacy & Security, Microphone, turn on EZYCLOUDX.
- **Accessibility**: needed to send system shortcuts (Command-Tab, Command-Space) to the remote PC:
  System Settings, Privacy & Security, Accessibility, turn on EZYCLOUDX.

## Install on Windows

1. Open the downloaded `EZC_<version>_x64-setup.exe` and follow the installer. It installs for your
   account only and **needs no administrator rights**; if Microsoft Edge WebView2 is missing, the
   installer downloads it.
2. Open **EZYCLOUDX** from the Start menu.

### If the browser or Windows blocks the installer

The installer is not code-signed yet, so **the first time**:

- Your browser may hold the file back: choose **Keep** (Edge: the three dots, **Keep**, then
  **Keep anyway**).
- SmartScreen says **Windows protected your PC**: press **More info**, then **Run anyway**.

Later updates install from inside the app and do not meet SmartScreen.

## Updates

The app checks for and downloads new versions in the background, and installs them when no stream
is running. If the app says an **update is required** when it opens, your version is too old to
connect: press **Update** and it restarts on the new version.

## Verify the download (optional)

Each release carries `SHA256SUMS` (macOS) and `SHA256SUMS-windows` (Windows).

```bash
# macOS, in the folder with the downloaded file and SHA256SUMS
shasum -a 256 -c SHA256SUMS --ignore-missing
```

```powershell
# Windows PowerShell: compare with the matching line in SHA256SUMS-windows
Get-FileHash .\EZC_<version>_x64-setup.exe -Algorithm SHA256
```

## Uninstall

- **macOS:** quit the app and drag **EZYCLOUDX** from Applications to the Trash.
- **Windows:** Settings, Apps, Installed apps, **EZYCLOUDX**, Uninstall.

## Support

When you contact support, include the app's **version** and **install id** (in the account menu or
the Support page in the app). The full guide is the **Guide** page in the console.

[Privacy policy](https://www.ezycloudx.com/en/privacy-policy) ·
[Terms of service](https://www.ezycloudx.com/en/terms-of-service)
