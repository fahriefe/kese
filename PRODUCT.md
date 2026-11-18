# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack
Plain single-file HTML/CSS/JS today (`index.html`, no build step, data in browser localStorage). The user confirmed a real server/database (e.g. Supabase) will be added later, so UI and data logic should stay separable and portable.

## Users
Individuals tracking their personal spending, at home or on a phone, entering a few expenses a day and checking at month end where the money went. Turkish-first audience, with users in other countries (UI in Türkçe, English, Deutsch, Français, Español, Русский).

## Product Purpose
Let a person record expenses, sort them into categories, set per-category monthly budgets, and see the month and the last six months at a glance. Success: adding an expense takes seconds and the month-end picture is obvious.

## Positioning
Country-aware expense ledger: sign-up captures country, city and currency, and the app shows where the user's income sits in their own country's distribution using published World Bank statistics (poverty lines, Gini, income shares), with a six-language interface.

## Operating Context
Account and expense data live in the browser (localStorage); passwords are stored hashed (PBKDF2). City lists come from countriesnow.space for non-Turkey countries (Turkey's 81 provinces are local). World Bank statistics and PPP factors are embedded in the page. Income class is an estimate (log-normal model on World Bank data), shown with a disclaimer.

## Capabilities and Constraints
Sign-up/sign-in; country, city, currency, language; expenses with date, amount, description, category, payment method, note; edit/delete; categories with colour and optional monthly budget; month picker; per-category breakdown; 6-month comparison; CSV export; income class card. Dark only (light mode was removed at the user's request). No emoji. Hard constraints: no server yet; income class only for countries with World Bank data (171) and when income is entered in the country's currency.

## Brand Commitments
Name "Kese" (Turkish for pouch/purse), tagline "Gider Defteri". Logo concept the user approved: a coin with rising bars (money + chart), kept minimal. User wants the app to NOT look AI-generated, to feel friendly and usable, and to stay dark.

## Evidence on Hand
World Bank indicator data in `veri/ulke_verileri.csv` and embedded in `index.html`. No testimonials, customers or usage numbers exist; none may be invented.

## Product Principles
1. Adding an expense is the fastest thing in the product.
2. The month's answer (how much, where) is visible without clicking.
3. Statistics are honest: estimates are labelled, missing data is a dash, never invented.
4. Every user-facing string exists in all six languages.
5. Portable to a real backend later without redesign.

## Accessibility & Inclusion
Readable contrast in the dark theme, keyboard focus visible, six languages, number/date/currency formatting follows the chosen language.
