SIRIUS TR JOURNAL

=== A) APK (GitHub orqali) ===
1) Zip ichidagi hamma narsani GitHub repository ildiziga yuklang (.github papkasi ham!).
2) Actions > Build APK (5-8 daqiqa) > Releases > SIRIUS-TR-JOURNAL.apk

=== B) TELEGRAM (2 ta bot kerak) ===
Telegram bot o'zi yuborgan xabarni o'qiy olmaydi, shuning uchun:
1) @BotFather orqali 2 ta bot yarating: SENDER (robot yuboradi) va READER (ilova o'qiydi).
2) Yangi PRIVATE kanal yarating, ikkala botni ADMIN qiling.
3) Kanal ID sini oling (-100... bilan boshlanadi).
4) Ilova > Настройки APK & Бот: READER tokeni + kanal ID > "Подключить и Проверить Бота".

=== C) MT5 ROBOT (SiriusSync.mq5) ===
1) MT5 > File > Open Data Folder > MQL5 > Experts ichiga mt5/SiriusSync.mq5 ni qo'ying.
2) MetaEditor'da oching, F7 (Compile). Xato chiqsa, matnini yuboring.
3) MT5 > Tools > Options > Expert Advisors:
   - "Allow algorithmic trading" yoqing
   - "Allow WebRequest for listed URL" yoqing va https://api.telegram.org qo'shing
4) Istalgan grafikka robotni tashlang. Inputs: BotToken = SENDER tokeni, ChatID = kanal ID,
   LocalUTCOffset = 5 (Toshkent).
5) Har bir MT5 hisobi (Personal, FTMO, FundedNext...) terminalida robotni alohida ishga tushiring.
   Ilovadagi hisobning MT5 Login ID si terminal login bilan bir xil bo'lishi kerak.

Robot yuboradi: balans/equity/margin, ochiq pozitsiyalar, limit orderlar (har 60 soniya),
yopilgan sdelkalar (darhol) va birinchi ishga tushganda hisob ochilganidan beri BARCHA tarix.

MUHIM: Telegram botlar xabarlarni faqat 24 soat saqlaydi. Tarix yuborilayotganda
ilovani oching va "Синхронизировать сейчас" bosing (yoki ilova ochiq tursin).
Tarixni qayta yuborish: robot Inputs > ResendHistory = true.

=== YANGILIKLAR ===
- Jurnal: filtr (juft, strategiya, model, natija, sana) + CSV eksport.
- Sessiya: Toshkent vaqti bilan avtomatik (Asia/Frankfurt/London/NY + Kill Zone), yozgi/qishki vaqtga o'zi o'tadi.
- Har sdelkada R, jami va o'rtacha R, equity $ / R.
- Sdelkani tahrirlash: strategiya, model, psixologiya, sessiya, risk, PnL, izohlar.
- PIN-kod + barmoq izi (Sozlamalar > Xavfsizlik).
- Bildirishnomalar: sdelka yopilganda va oy oxirida (20:00).
- Robot: NotifyChatID (ixtiyoriy) — yopilgan sdelka haqida Telegram push.
  O'z ID ngizni @userinfobot dan oling va SENDER botga /start yozing.
