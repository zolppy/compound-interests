# 📈 Daily Compound Interest + Monthly Investment Calculator

A lightweight, browser-based financial calculator that projects the growth of an initial investment with daily compounding and optional monthly contributions. It uses a fixed daily rate derived from the current daily income, compounds it over 22 trading days per month, and adds any monthly investment at month-end.

![Screenshot placeholder – add an actual screenshot if desired](screenshot.png)

## ✨ Features

- **Daily compounding** based on a fixed daily rate calculated from initial capital and current daily income.
- **Monthly contributions** added at the end of each month.
- **Flexible periods**: 1, 3, 6, 12, or 24 months (22 trading days/month).
- **Instant updates** on any input change.
- **Profit calculation** (total − initial − total contributions).
- **Brazilian Real (BRL)** currency formatting.
- Clean, responsive design with dark theme.
- No dependencies – pure HTML, CSS, and JavaScript.

## 🚀 How to Use

1. Open the `index.html` file in any modern web browser.
2. Fill in the fields:
   - **Initial Capital** (R$) – starting amount.
   - **Current Daily Income** (R$) – how much the investment earns per day.
   - **Monthly Investment** (R$) – amount added at the end of each month (can be zero).
   - **Period** – select the number of months.
3. The **total after period** and **profit earned** update automatically.
4. The note at the bottom explains the assumptions.

## 🧮 Calculation Logic

- Daily rate = `dailyIncome / initialCapital` (fixed).
- Each month compounds daily for 22 days:
  ```
  balance = balance * (1 + dailyRate)^22
  ```
- Then the monthly investment is added at month‑end.
- Profit = final balance − initial capital − (monthly investment × number of months).

> **Note:** This model assumes the daily rate remains constant and uses 22 trading days per month – common for investments that only yield on business days (e.g., some fixed income or crypto staking).

## 🛠️ Technologies

- HTML5
- CSS3 (flexbox, clamp, custom properties)
- Vanilla JavaScript (ES6)
- `Intl.NumberFormat` for BRL currency

## 📁 File Structure

- `index.html` – the entire application (styles, markup, and script are all in one file).

## 📝 License

Feel free to use, modify, and distribute. No warranty provided.

---

**Enjoy projecting your investments!** If you have suggestions or improvements, open an issue or pull request.
