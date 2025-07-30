# 🎉 Omanges FunFacts Extension for Streamer.bot

The **FunFacts Extension** is a Twitch chat addon for **Streamer.bot** that sends category-based random facts to your viewers using `!ff`, `!fact`, or `!funfact`. It’s a fun and modular way to surprise, educate, or unhinge your chat in real time.

---

## 💡 Features

* 🔥 **7 preloaded categories**, each with **100 facts**
* 🎯 Pick a **specific category** or go **random**
* 🚫 Move unwanted categories to a `Disabled` folder to turn them off automatically
* ⚙️ Built for **Streamer.bot v0.2.8+**
* ✅ Robust error handling for missing files or input
* 💬 Returns clean, non-empty facts only

---

## 📦 Preloaded Categories

Each of these `.txt` files includes **100 hand-curated facts**:

| Category   | Description                               |
| ---------- | ----------------------------------------- |
| `simple`   | Short, wholesome, or beginner-friendly    |
| `weird`    | Strange, quirky, or unexpected facts      |
| `unhinged` | Off-the-rails chaos—viewer favorite       |
| `science`  | Facts about biology, physics, space, etc. |
| `history`  | Surprising tidbits from the past          |
| `gaming`   | Fun, obscure, or nostalgic game facts     |
| `spicy`    | Edgy or R-rated (Twitch-safe) content     |

Each category lives in its own `.txt` file, one fact per line.

---

## 🧰 Commands

| Command    | Function                            |
| ---------- | ----------------------------------- |
| `!ff`      | Triggers the script with a category |
| `!fact`    | Alias of `!ff`                      |
| `!funfact` | Alias of `!ff`                      |

### Examples

* `!ff weird` → sends a weird fact
* `!fact science` → sends a science fact
* `!funfact random` → sends a random fact from a random active category

---

## 🗂 Folder Structure

This extension expects a folder structure like:

```
/Streamer.bot/
├── Streamer.bot.exe
├── FunFacts/
│   ├── simple.txt
│   ├── weird.txt
│   ├── unhinged.txt
│   ├── science.txt
│   ├── history.txt
│   ├── gaming.txt
│   ├── spicy.txt
│   └── Disabled/
│       └── (Any categories moved here are ignored)
```

### 📌 Disabled Folder

Move any `.txt` file into the `Disabled` subfolder to **deactivate** that category. The script will ignore anything in that folder and won’t list it as an option.

Example:

```bash
FunFacts/
├── weird.txt
└── Disabled/
    └── spicy.txt  ← will not be used or listed
```

---

## ⚙️ Installation

1. **Import Script**

   * Add the provided C# code to a new C# action in Streamer.bot.

2. **Create the `FunFacts` Folder**

   * Create a folder called `FunFacts` in the same directory as `Streamer.bot.exe`.

3. **Drop In .txt Files**

   * Place the preloaded category files in the `FunFacts` folder.
   * Each file must contain one fact per line (already done for you).

4. **Optional: Disable Categories**

   * Move any `.txt` file to the `FunFacts/Disabled/` folder to disable it.

5. **Setup Commands**

   * In Streamer.bot, add triggers for:

     * `!ff`
     * `!fact`
     * `!funfact`
   * Connect each trigger to the FunFacts script.

---

## 🧪 Example Output

```text
Fun Fact (science): Bananas are naturally radioactive due to their potassium content.
```

If a user enters an invalid category:

```text
Invalid category 'math'. Available categories: science, weird, simple, unhinged, ... or 'random'
```

---

## 🚧 Error Handling

The script returns helpful messages when:

* `FunFacts` folder is missing
* No valid category files exist
* A `.txt` file is empty
* The user provides an invalid category

---

## ✏️ Customization Tips

* Add your own `.txt` file to expand categories!
* Community-sourced facts? Easy—just paste into any category file.
* Facts are **not case-sensitive** and files can be named however you want (as long as they’re `.txt`).

---

## 🔧 Requirements

* **Streamer.bot v0.2.8 or newer**
* Twitch bot integration set up correctly
* C# scripting enabled inside Streamer.bot

---

## 💬 Feedback or Contributions

Want to submit more facts or categories?

* Open a pull request
* Create an issue with your suggestion
* Or fork it and go wild

You can also suggest ideas via [GitHub Issues](https://github.com/realOmanges/FunFacts/issues).

This tool is built to be modular, sharable, and Twitch-friendly.

---

## 👤 Author

**Omanges**
🟣 Twitch: [twitch.tv/omanges](https://twitch.tv/omanges)
💬 Join the [SIDOR Community Discord](https://discord.gg/2pcKpMrxdD)

---

## 📄 License

MIT License
You’re free to use, modify, and share this—just give credit.

---
