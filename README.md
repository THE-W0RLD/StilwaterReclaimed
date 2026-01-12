# Stilwater Reclaimed

An open-source native PC port of Saints Row 2 based on static recompilation of the Xbox 360 version.

**⚠️ This project contains ZERO game assets. You must provide your own legally acquired copy of Saints Row 2 for Xbox 360.**

---

## Project Status

🚧 **Early Development** - Infrastructure and tooling phase

Current milestone: **Toolchain & Build System**

---

## What Is This?

Stilwater Reclaimed is a community effort to create a modern, native PC port by converting the Xbox 360 executable into maintainable C++ code using static recompilation tools.

**This is NOT:**
- An emulator
- A mod for the existing PC version
- A way to pirate the game

**This IS:**
- A preservation and modernization project
- Legally clean (no assets, no leaked code)
- Open source and community-driven

---

## Technical Approach

- **Static Recompilation**: Xbox 360 XEX → C++ via XenonRecomp
- **Custom Runtime**: Replace Xbox OS services (file I/O, threading, input, audio)
- **Modern Renderer**: Translate shaders (XenosRecomp) + D3D12/Vulkan backend
- **User-Supplied Assets**: Extractor tools read your legally owned game files

---

## Legal & Distribution

### Zero Assets Policy

✅ **Allowed in repo:**
- Our own C++ code and runtime
- Build scripts and tools
- Documentation

❌ **NEVER allowed:**
- Game executables, textures, models, audio, scripts
- Leaked Volition source code
- Links to pirated game dumps

### How Users Get Game Data

Users provide their own Xbox 360 copy of Saints Row 2. Our asset extractor reads those files at install time.

---

## Roadmap

### Milestone 1: Toolchain & Build ✅ (Current)
- [ ] XenonRecomp successfully converts SR2 XEX
- [ ] Basic C++ runtime skeleton compiles
- [ ] CI/CD builds on Windows and Linux
- [ ] Contributor guidelines finalized

### Milestone 2: Asset Loading
- [ ] Parse Xbox 360 game file formats
- [ ] Extract textures, models, scripts
- [ ] Asset pipeline documented

### Milestone 3: First Frame
- [ ] Window creation + input initialization
- [ ] Load and display one texture/model
- [ ] Basic shader translation working

### Milestone 4: Menu Navigation
- [ ] Boot to main menu
- [ ] UI rendering functional
- [ ] Menu input working

### Milestone 5: In-Game
- [ ] Load into Stilwater
- [ ] Player movement
- [ ] Camera controls

### Milestone 6: Story Playable
- [ ] Complete story missions
- [ ] Save/load system
- [ ] Stability fixes

### Milestone 7: Feature Complete (v1.0)
- [ ] Co-op networking
- [ ] Restored DLC (Ultor Exposed, Corporate Warfare)
- [ ] Performance optimization
- [ ] Cross-platform polish

---

## Contributing

**We Need Help With:**
- 🔧 Platform/runtime programming (file I/O, threading, audio)
- 🎨 Graphics programming (D3D12/Vulkan, shader translation)
- 🔍 Reverse engineering (XenonRecomp, Ghidra experience)
- 🧪 Testing and bug reproduction
- 📝 Documentation

**See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.**

---

## Getting Started

### Prerequisites
- Legal copy of Saints Row 2 for Xbox 360
- C++20 compiler (MSVC/GCC/Clang)
- CMake 3.20+
- Git

### Build Instructions

```bash
git clone https://github.com/THE-W0RLD/StilwaterReclaimed.git
cd StilwaterReclaimed
mkdir build && cd build
cmake ..
cmake --build .
```

(Note: Currently builds a stub runtime only - game not yet playable)

---

## Community

- **Discord**: [Link TBD]
- **Issues**: Report bugs and request features via GitHub Issues
- **Discussions**: Technical questions welcome in GitHub Discussions

---

## References

- [XenonRecomp](https://github.com/hedge-dev/XenonRecomp) - Xbox 360 static recompilation
- [XenosRecomp](https://github.com/hedge-dev/XenosRecomp) - Xbox 360 shader converter
- [UnleashedRecomp](https://github.com/hedge-dev/UnleashedRecomp) - Example 360 recomp project

---

## License

This project's original code is licensed under [GPL-3.0](LICENSE).

Saints Row 2 is © Volition / Deep Silver / Embracer Group. This project is not affiliated with or endorsed by them.

---

## FAQ

**Q: Can I download and play this now?**  
A: No, the project is in early development. Nothing is playable yet.

**Q: Is this legal?**  
A: Yes. Reverse engineering for interoperability is legal in many jurisdictions. We distribute no copyrighted assets.

**Q: Do you have the source code?**  
A: No. We use publicly available reverse engineering tools on legally owned game copies.

**Q: When will it be done?**  
A: This is a volunteer project with no timeline. Progress depends on community contributions.

**Q: Can I help if I'm not a programmer?**  
A: Yes! We need testers, documentation writers, and community moderators.
