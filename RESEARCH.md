# Monument research notes

Checked 16 Nov 2026. "Verified" means a readable source states it; it does not mean an on-site survey. Where sources disagree, both are listed.

## Supplied sources and what could be read

| Source | Result |
|---|---|
| baigiang.violet.vn (lecture slides) | Not readable: the site blocks automated fetching. Not used. |
| triphunter.vn | Read. 12 steps, 9 m block, 12 m statue, 21 m total, one man and one woman. |
| studocu.vn | Not readable: paywalled preview. Not used. |
| daidoanket.vn (50th anniversary, Apr 2025) | Read. Campaign 9–21/4/1975, "12 ngày đêm"; tank 714 unit. |
| baodongnai.com.vn (Công viên Bia Chiến thắng, 2019) | The link now returns a 404 page. Not used. |

## Additional sources found

- Long Khánh city portal, older page (newsdetail_GT.aspx?NewsId=755), seen through a search snippet only; the page itself would not load: sculptor, builder, dates, area, location.
- Long Khánh city portal, Trần Phú primary school article (news 589): names both figure prototypes.
- Long Khánh city portal, heritage survey of the two parks (news 698): area of each park and their separate locations.
- Báo Thái Nguyên, Apr 2025, "Chuyện bên Tượng đài chiến thắng Long Khánh": female figure is Hồ Thị Hương (code name H25); tank 714 unit.
- amazingvietnam.vn (2011): location at the Hùng Vương – QL 1A junction, start and completion dates.

## Facts used in the scene

| Claim | Status | Source |
|---|---|---|
| Sculptor Trần Thanh Thanh (Vietnam Fine Arts Association) | Verified, one official source | City portal NewsId=755 (snippet) |
| Cornerstone 21/4/2000; construction 22/12/2000; completed 15/4/2001 | Verified | City portal NewsId=755; amazingvietnam (start and completion) |
| Location: the triangle where QL 1 meets Hùng Vương | Verified | City portal NewsId=755; amazingvietnam |
| 12 steps = 12 days and nights of the campaign (9–21/4/1975) | Verified | triphunter; Báo Thái Nguyên; daidoanket |
| 9 m block + 12 m statue = 21 m, recalling 21/4 | Verified as the published figures | triphunter; Báo Thái Nguyên |
| Figures modelled on Lê A and Hồ Thị Hương | Verified, official local source | City portal news 589: "hình tượng hai anh hùng lực lượng vũ trang Hồ Thị Hương và Lê A được lựa chọn làm nguyên mẫu" |
| Female figure = Hồ Thị Hương | Verified, two sources | Báo Thái Nguyên; city portal 589 |
| Tank 714: Regiment 165, Division 7, 4th Corps | Verified, two sources | daidoanket; Báo Thái Nguyên |

The scene does not say which figure is Lê A; the sources pair the names with the two figures only by implication.

## Conflicting or unverified

- **Site area.** 7,712.3 m² (older city portal) against 5,618.5 m² (recent heritage survey). Not shown in the scene.
- **Construction start.** One Prezi deck says 19/12/2001; it conflicts with two other sources and is not used.
- **"12 days and nights".** 9 to 21 April is 13 calendar days; the sources still say 12. The scene repeats the published wording.
- **Pedestal height.** amazingvietnam says the statue stands on a "3 m granite base", which conflicts with the 9 m block. The scene keeps 9 m.

## Rear inscription

The owner asked for "THẦN TỐC / TÁO BẠO / BẤT NGỜ / CHẮC THẮNG" on the rear face, and it is now displayed there. It is a **user-requested reconstruction, not a verified inscription**: no source or photograph available to me shows this wording on the monument (the reference photos show gold lettering on more than one face, but it cannot be read). The code comment and the in-app credits say so. If a readable photo of the rear face turns up, the text should be corrected to match it.

## Reliefs

Reference frames t070s, t076s and t080s and Flickr photos 11 and 12 show a white relief band with a continuous procession of figures, some with rifles and flags. I could not confirm the suggested split (marching on two faces, celebration on the rear). At the owner's request the band now uses the two supplied textures (`models/textures/relief_march.jpg` on the front faces, `relief_celebration.jpg` on the rear). Their provenance is unknown; they are labelled in the credits as an interpretation, not a copy of the real reliefs.

## Statue scale

`SCULPT_SCALE` stays at 5.4. Measured in the scene's world space, the top of the pedestal is at 10.9 m. The figures reach 23.8 m: 12.9 m including the 1.1 m sculpted plinth, about 11.8 m without it. The raised rifle's tip is at 28.3 m, 17.4 m above the pedestal.

The sources' "12 m statue" fits the figures (11.8–12.9 m) and not a measurement to the rifle tip. That suggests the published figure leaves out the rifle, but this is an inference; no source says so. Raising the scale to 6.0–6.2 would make the figures about 14 m high, so it was not changed.

## Fountains

None of the sources, the reference photographs or the earlier evidence notes mention fountains or basins in this park. None were added. If you have a photograph showing them, I can add them.

## Roads and businesses

- QL 1 on the west side and Hùng Vương on the east side match the satellite review in the earlier reference pack. Labels unchanged; the tank island was not moved.
- Highlands Coffee (239 Hùng Vương): a public map pin puts it across Hùng Vương from the middle of the park. Its sign is placed on the nearest generated shophouse, marked as approximate; the facade is generic. Details in `STOREFRONT_PLACEMENTS.json`.
- Sacombank (259 Hùng Vương): address confirmed, but no coordinate source found, so it is listed as pending and not placed.
- Khách sạn Hòa Bình (110 Hùng Vương), Nước Sâm Bà Bảy (175 Hùng Vương): still leads only; not placed. All other signs stay generic.
- Công viên Bia Chiến thắng is a separate park (Xuân Lộc quarter, built 1985, renovated 2009 and 2019) and is not part of this scene. Neither is the Lê Lợi walking street.

## Gameplay additions (not part of the real park)

- **Lotus light mast**: moved to the centre of the lotus at the owner's request (scene x 47, z 0). Its exact real position was not re-verified.
- **Traffic lights, pedestrian signals and the traffic officer** at the Hùng Vương crossing (scene x ≈ −8): a gameplay feature. I have no evidence of signals or a zebra crossing at this spot.
- **Fireworks events** ("Đêm Long Khánh", "Đêm giao thừa", "Mừng ngày 21/4"): fictional shows, not records of real events.
- **Side quests, crates, litter, hurdles, the photo ring and the seating/eating system**: game props.
