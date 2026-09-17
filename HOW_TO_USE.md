# How to Use - That's It

## 1. Clone

```bash
git clone https://github.com/YOUR_USERNAME/cachyos-setup.git
cd cachyos-setup
```

## 2. One Command

```bash
sudo bash install
```

## 3. Answer One Question

```
Do you need NVIDIA GPU for deep learning training?

  A) NO - Turn GPU completely OFF (simplest)
  B) YES - GPU ON-DEMAND (recommended for BTech)

Choose A or B (default: B):
```

Type `A` or `B`. Then press Enter.

## 4. It's Done

Script automatically:
- Installs everything
- Configures battery optimization
- Sets up power management
- **Reboots when done**

---

## That's It

No other steps. No other commands. Just:

```
git clone
cd cachyos-setup
sudo bash install
```

Press a key when it asks about GPU. **Done.**

---

## After Reboot

```bash
# Check it worked
powerprofilesctl get   # Shows current power profile
upower -e              # Shows battery status
gpu-status             # (If you chose GPU on-demand)
```

**Plug/unplug charger. Profile should switch automatically.**

---

## Use Your System

**If you chose A (no GPU)**:
```bash
python train.py        # Runs normally, battery lasts longer
```

**If you chose B (GPU on-demand)**:
```bash
python train.py                 # CPU mode, battery lasts 8-10 hrs
prime-run python train.py       # GPU mode, full power for training
```

---

**That's literally everything.** ✓

One command. Done.
