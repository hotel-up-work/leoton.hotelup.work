# Leoton Hotel

Live site: https://leoton.hotelup.work

## About
Leoton Hotel — готель у Чернівцях. Односторінковий лендинг. Фасад/рецепція (`photos_source: null`), тому hero типографічний (CSS/SVG). Фото номерів — реальні, з Booking.com; фото міста Чернівців з Pexels (див. Photos).

## Hero concept
Злітна смуга в перспективі: темне нічне тло, розмітка й бурштинові вогні, що біжать до горизонту. Концепт виходить із підтвердженого безкоштовного трансферу до аеропорту.

## Amenities (verified, list.json)
- Безкоштовний Wi‑Fi
- Безкоштовна парковка
- Кондиціонер
- Сімейні номери
- Цілодобова рецепція
- Обслуговування номерів
- Бар
- Безкоштовний трансфер з аеропорту

## Check-in / check-out
Заїзд з 14:00; Виїзд до 12:00

## Rooms (Booking.com room table; T&S and Панський Двір 2 from the official site)
- Двомісний номер / Твін економ-класу
- Стандартний двомісний номер
- Покращений двомісний номер
- Люкс

## House rules (Booking.com)
- Чи можна з дітьми? Так, діти будь-якого віку. Дитячих ліжечок і додаткових ліжок немає, тож обирайте номер на всіх гостей.
- Чи можна з домашньою твариною? Так, за попереднім запитом. Може стягуватися доплата.
- Як оплатити проживання? Готівкою. Після бронювання представник готелю зв’яжеться щодо передоплати — її потрібно внести протягом 5 днів.

## Reviews
Booking.com 8.3/10 (145), Google 3.8/5 (147). Знімок на 30.09.2026, платформи окремо, без aggregateRating.

## Contact
- Phone: +380 66 363 3201
- Booking.com: https://www.booking.com/hotel/ua/leoton.html
- Google Maps: https://maps.app.goo.gl/RQBD6fo4k4AVZYY7A
- Address: вул. Чкалова, 30В, Чернівці

## Sources
Booking.com listing text (description, rooms, breakfast, house rules; guest reviews ignored), captured 30.09.2026, plus the official site where there is one. Verbatim quotes: `shared/build/facts.json` у робочому просторі (поза репозиторієм сайту).

## Property-specific sections
- `#transfer` Безкоштовний трансфер

## Not published
Кількість номерів, зірковість (Google Hotels показує 3★ без офіційного джерела), email, сайт, Instagram, графік і умови трансферу, «біля аеропорту», відстань до станції Чернівці-Південна (Booking дає і 700 м, і 1,2 км). Телефон — з Google Hotels.

## Content TODO (не показується на сторінці)
- [ ] TODO: уточнити графік і умови безкоштовного трансферу (з якого аеропорту/вокзалу, години, обмеження)
- [x] TODO: уточнити ліжка: у Booking усі 4 категорії мають «1 широке двоспальне ліжко», навіть «Твін» — підпис номера «Твін економ-класу» виправлено на «2 односпальні ліжка» за реальним фото з Booking.com (сама Booking-картка суперечить власному фото)
- [ ] TODO: підтвердити телефон +380 66 363 3201
- [ ] TODO: отримати власні фото фасаду й рецепції і погодити їх використання — потім додати галерею (фото номерів вже є, див. Photos)
- [ ] TODO: перевірити ціни й наявність через сам готель; на сторінці цін немає

## Forms
HotelOS (`ch-leoton`): `stay-request` (проживання). Документ `hotels/ch-leoton` у Firestore треба створити вручну, інакше правила відхилять заявки.

## Photos
Фото міста — з Pexels, підключені за прямими посиланнями images.pexels.com (без копій у репо), з підписами та авторами на сторінці:

- Резиденція буковинських митрополитів, нині Чернівецький університет: pexels.com/photo/12961411 (Valeriia Harbuz)
- Вулиця в Чернівцях: pexels.com/photo/17268858 (Андрій Копічевський)
- Цегляні арки: pexels.com/photo/38163642 (Natalia Sevruk)

Фото номерів — реальні, з галереї кожного типу номера на Booking.com (`booking.com/hotel/ua/leoton.html`, розділ «Наявність місць» → фото при кліку на назву номера; сторінка стоїть за bot-challenge, знято headless-браузером). URL на bstatic.com підписані токеном (`?k=...`) і згасають, тому збережені локально в `images/`, а не захотлінкані:

| Файл | Номер на сторінці | Джерело (Booking.com photo id) |
| --- | --- | --- |
| images/room-twin-economy.jpg | Двомісний номер / Твін економ-класу | 331948945 |
| images/room-standard-double.jpg | Стандартний двомісний номер | 337074040 |
| images/room-improved-double.jpg | Покращений двомісний номер | 337073817 |
| images/room-lux.jpg | Люкс | 335364100 |

## SEO
Title і description з маніфесту, canonical, Open Graph, `geo.*`, JSON-LD `Hotel` лише з підтвердженими полями (без numberOfRooms, starRating, aggregateRating), `robots.txt`, `sitemap.xml`, `404.html`.
