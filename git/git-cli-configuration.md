# Git CLI Configuration

**Installasi GIT**
Windows
> Download https://git-scm.com/downloads

Linux
    
> **RPM-based distribution, such as RHEL or CentOS), you can use dnf:**
sudo dnf install git-all

> **Debian-based distribution, such as Ubuntu, try apt:**
sudo apt install git

> **OpenSUSE**
sudo zypper install git

Mac OS
> Download https://git-scm.com/downloads

---


**Git Login**
Inisialisasi username dan Email pada PC
> git config --global user.name <github_username>
git config --global user.email <email yang digunakan pada username>

**Generate SSH pada pc.**

    ssh-keygen -t ed25519 -C "your_email@example.com"

Setelah itu silahkan copy ssh public key: (pilih os yang anda gunakan)

> **macOS:**
tr -d '\n' < ~/.ssh/id_ed25519.pub | pbcopy

> **Linux (requires the xclip package):**
xclip -sel clip < ~/.ssh/id_ed25519.pub

> **Git Bash on Windows:**
cat ~/.ssh/id_ed25519.pub | clip

---

**Inisialisasi SSH dari PC ke GITHUB**
> - Klik link ini : https://github.com/settings/keys
> - Klik New SSH Key
> - Isi kolom Title sembarang
> - Paste pada kolom KEY
> - Klik Add SSH Key
> - Masukkan Password akun github
> - Selesai

---

**Meng-Clone Github Repository to Local Computer**
    
    git clone <ssh pada repository github>

**Pull from GitHub Repository to Local Repository**
Menarik file yang ada di github untuk update pada local repository (pc kita sendiri)

    git pull origin <branch pada repository>

**Push to Local Repository to GitHub Repository**

Menambahkan atau menselect semua file yang ada dalam repository

    git add . (atau file directory yang ingin di push ke github)

Membuat commit atau comment pada perubahan repository

    git commit -m "first commit"

Menambahkan Remote Server dari github ke local (Jika Diperlukan)

    git remote add origin <ssh pada repository github>

Mendorong atau mengupload file yang telah kita commit
    
    git push -u origin <branch pada repository>
