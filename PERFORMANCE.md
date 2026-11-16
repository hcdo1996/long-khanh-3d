# Performance: Phase 1 measurements

Measured on 16 Nov 2026 with the page's built-in benchmark (FPS button, or key P, then "Đo cả 3 mức").

**Test environment.** Headless Chrome 153 on Linux, 1280×720 viewport, device pixel ratio 1, software renderer (ANGLE / SwiftShader, no GPU). A software renderer draws a frame in seconds, so the frame times below only show the relative change. They are not what a real graphics card will give. Triangle and draw-call counts are exact and do not depend on the machine.

**Route.** Three fixed viewpoints (monument forecourt, park tip looking at Hùng Vương, Hùng Vương pavement) × three conditions (clear day, rainy day, night) × three tiers.

"Before" counts are from the unmodified scene. The "before" frame times were recorded after the lighter tree trunks were already in place (the first timing run could not record frames longer than 5 s), so the true starting point was slower than shown; only the Hùng Vương view has a timing from the fully unmodified scene (Nhẹ 3039 ms, Cao 3289 ms, Tối đa 4450 ms).

| Tier | Condition | Viewpoint | Triangles before | after | Draw calls before | after | Frame ms before | after | Animated NPCs before | after |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nhẹ | Ngày nắng | Sân tượng đài | 1,017,807 | 401,731 | 559 | 446 | 6166 | 3300 | 20 | 5 |
| Nhẹ | Ngày nắng | Mũi công viên | 883,498 | 383,873 | 351 | 268 | 5233 | 3133 | 20 | 4 |
| Nhẹ | Ngày nắng | Vỉa hè Hùng Vương | 872,207 | 320,228 | 297 | 148 | 2855 | 1621 | 20 | 3 |
| Nhẹ | Ngày mưa | Sân tượng đài | 1,015,881 | 391,108 | 552 | 407 | 6391 | 3139 | 20 | 1 |
| Nhẹ | Ngày mưa | Mũi công viên | 883,458 | 383,833 | 337 | 254 | 5591 | 3216 | 20 | 4 |
| Nhẹ | Ngày mưa | Vỉa hè Hùng Vương | 872,177 | 320,228 | 288 | 149 | 3022 | 1626 | 20 | 3 |
| Nhẹ | Đêm | Sân tượng đài | 1,015,957 | 395,016 | 531 | 412 | 6450 | 3658 | 20 | 4 |
| Nhẹ | Đêm | Mũi công viên | 883,122 | 383,829 | 337 | 255 | 5966 | 3850 | 20 | 5 |
| Nhẹ | Đêm | Vỉa hè Hùng Vương | 871,841 | 322,217 | 288 | 151 | 2894 | 1880 | 20 | 1 |
| Cao | Ngày nắng | Sân tượng đài | 1,018,125 | 603,653 | 559 | 421 | 6842 | 4333 | 20 | 4 |
| Cao | Ngày nắng | Mũi công viên | 883,458 | 461,682 | 336 | 260 | 6142 | 3844 | 20 | 6 |
| Cao | Ngày nắng | Vỉa hè Hùng Vương | 872,177 | 411,228 | 287 | 157 | 3394 | 1933 | 20 | 3 |
| Cao | Ngày mưa | Sân tượng đài | 1,013,759 | 633,865 | 529 | 425 | 6958 | 4233 | 20 | 4 |
| Cao | Ngày mưa | Mũi công viên | 883,458 | 454,592 | 337 | 259 | 6408 | 3955 | 20 | 6 |
| Cao | Ngày mưa | Vỉa hè Hùng Vương | 872,177 | 411,228 | 288 | 158 | 3378 | 1980 | 20 | 3 |
| Cao | Đêm | Sân tượng đài | 1,013,423 | 612,714 | 529 | 418 | 6916 | 6133 | 20 | 4 |
| Cao | Đêm | Mũi công viên | 883,122 | 457,514 | 337 | 251 | 6283 | 5558 | 20 | 10 |
| Cao | Đêm | Vỉa hè Hùng Vương | 874,827 | 398,195 | 291 | 157 | 3322 | 2536 | 20 | 3 |
| Tối đa | Ngày nắng | Sân tượng đài | 2,052,359 | 1,483,295 | 1208 | 1042 | 8166 | 6158 | 20 | 6 |
| Tối đa | Ngày nắng | Mũi công viên | 1,923,364 | 1,351,806 | 1015 | 899 | 7125 | 5658 | 20 | 10 |
| Tối đa | Ngày nắng | Vỉa hè Hùng Vương | 1,912,421 | 1,300,181 | 971 | 770 | 4483 | 3461 | 20 | 4 |
| Tối đa | Ngày mưa | Sân tượng đài | 2,050,979 | 1,479,943 | 1207 | 1039 | 8275 | 6116 | 20 | 6 |
| Tối đa | Ngày mưa | Mũi công viên | 1,921,868 | 1,355,178 | 1015 | 911 | 7275 | 5375 | 20 | 11 |
| Tối đa | Ngày mưa | Vỉa hè Hùng Vương | 1,910,449 | 1,299,185 | 970 | 768 | 4475 | 3455 | 20 | 4 |
| Tối đa | Đêm | Sân tượng đài | 2,048,735 | 1,467,819 | 1201 | 1032 | 8191 | 7958 | 20 | 6 |
| Tối đa | Đêm | Mũi công viên | 1,924,068 | 1,351,348 | 1013 | 906 | 7308 | 7075 | 20 | 11 |
| Tối đa | Đêm | Vỉa hè Hùng Vương | 1,913,505 | 1,288,947 | 970 | 767 | 4625 | 4339 | 20 | 4 |

## Repeat it on your own computer

1. Open the page, wait for loading to finish, close the cards.
2. Press **P** (or tap the round **FPS** button). The overlay shows FPS, frame time, draw calls, triangles, tier, render resolution and animated NPCs.
3. Press **Đo cả 3 mức**. Do not touch the page for about 90 seconds. It visits the same three viewpoints in day, rain and night on each tier.
4. A card titled "Kết quả đo hiệu năng" lists every result with your browser, graphics card and viewport. The same data is printed in the browser console as `LKBENCH {...}`.
5. Keep the window the same size between runs so results are comparable.

# Phase 2 (park life) against Phase 1

Same benchmark, same headless Chrome 153, 1280×720, device pixel ratio 1, software renderer (no GPU). As before, frame times only show relative change; they are not real-device FPS.

| Tier | Condition | Viewpoint | Triangles P1 | P2 | Draw calls P1 | P2 | Frame ms P1 | P2 | Animated NPCs P1 | P2 |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nhẹ | Ngày nắng | Sân tượng đài | 401,731 | 378,258 | 446 | 402 | 3300 | 2828 | 5 | 1 |
| Nhẹ | Ngày nắng | Mũi công viên | 383,873 | 437,964 | 268 | 391 | 3133 | 2929 | 4 | 8 |
| Nhẹ | Ngày nắng | Vỉa hè Hùng Vương | 320,228 | 339,006 | 148 | 137 | 1621 | 1583 | 3 | 1 |
| Nhẹ | Ngày mưa | Sân tượng đài | 391,108 | 370,085 | 407 | 381 | 3139 | 2812 | 1 | 4 |
| Nhẹ | Ngày mưa | Mũi công viên | 383,833 | 433,980 | 254 | 339 | 3216 | 2967 | 4 | 8 |
| Nhẹ | Ngày mưa | Vỉa hè Hùng Vương | 320,228 | 336,375 | 149 | 138 | 1626 | 1487 | 3 | 1 |
| Nhẹ | Đêm | Sân tượng đài | 395,016 | 345,549 | 412 | 384 | 3658 | 3567 | 4 | 4 |
| Nhẹ | Đêm | Mũi công viên | 383,829 | 438,701 | 255 | 347 | 3850 | 4078 | 5 | 10 |
| Nhẹ | Đêm | Vỉa hè Hùng Vương | 322,217 | 338,672 | 151 | 139 | 1880 | 1967 | 1 | 1 |
| Cao | Ngày nắng | Sân tượng đài | 603,653 | 605,193 | 421 | 396 | 4333 | 4008 | 4 | 4 |
| Cao | Ngày nắng | Mũi công viên | 461,682 | 525,172 | 260 | 352 | 3844 | 3794 | 6 | 12 |
| Cao | Ngày nắng | Vỉa hè Hùng Vương | 411,228 | 420,172 | 157 | 143 | 1933 | 1939 | 3 | 3 |
| Cao | Ngày mưa | Sân tượng đài | 633,865 | 631,169 | 425 | 403 | 4233 | 3775 | 4 | 4 |
| Cao | Ngày mưa | Mũi công viên | 454,592 | 518,277 | 259 | 349 | 3955 | 3739 | 6 | 12 |
| Cao | Ngày mưa | Vỉa hè Hùng Vương | 411,228 | 420,172 | 158 | 144 | 1980 | 1933 | 3 | 3 |
| Cao | Đêm | Sân tượng đài | 612,714 | 612,441 | 418 | 397 | 6133 | 5608 | 4 | 4 |
| Cao | Đêm | Mũi công viên | 457,514 | 520,874 | 251 | 340 | 5558 | 5508 | 10 | 13 |
| Cao | Đêm | Vỉa hè Hùng Vương | 398,195 | 419,836 | 157 | 144 | 2536 | 2479 | 3 | 3 |
| Tối đa | Ngày nắng | Sân tượng đài | 1,483,295 | 1,459,612 | 1042 | 981 | 6158 | 5700 | 6 | 5 |
| Tối đa | Ngày nắng | Mũi công viên | 1,351,806 | 1,395,456 | 899 | 985 | 5658 | 5350 | 10 | 16 |
| Tối đa | Ngày nắng | Vỉa hè Hùng Vương | 1,300,181 | 1,281,100 | 770 | 708 | 3461 | 3372 | 4 | 3 |
| Tối đa | Ngày mưa | Sân tượng đài | 1,479,943 | 1,456,065 | 1039 | 978 | 6116 | 5675 | 6 | 5 |
| Tối đa | Ngày mưa | Mũi công viên | 1,355,178 | 1,399,160 | 911 | 998 | 5375 | 5458 | 11 | 17 |
| Tối đa | Ngày mưa | Vỉa hè Hùng Vương | 1,299,185 | 1,288,390 | 768 | 709 | 3455 | 3361 | 4 | 3 |
| Tối đa | Đêm | Sân tượng đài | 1,467,819 | 1,452,357 | 1032 | 977 | 7958 | 7266 | 6 | 5 |
| Tối đa | Đêm | Mũi công viên | 1,351,348 | 1,401,782 | 906 | 996 | 7075 | 7008 | 11 | 17 |
| Tối đa | Đêm | Vỉa hè Hùng Vương | 1,288,947 | 1,289,720 | 767 | 718 | 4339 | 3916 | 4 | 4 |

Summary: frame time is unchanged or slightly lower in 23 of 27 cells. The park-tip view now contains the dog, the guide and the tourists, so on Nhẹ it draws 391 calls instead of 268. That costs nothing measurable on the software renderer, but it is the view to watch on a weak GPU.

# Phase 3 (upgrade: events, jumping, traffic, quests, seating) against Phase 2

Both builds were run back to back on the same machine (headless Chrome, 1280×720, DPR 1, software renderer, no GPU). Frame times show relative change only; they are not real-device FPS. Phase 2 was re-measured in this session, so its numbers differ a little from the table above. The new **Đêm + pháo hoa** condition runs the night scene with a fireworks show in progress.

| Tier | Condition | Viewpoint | Triangles P2 | P3 | Draw calls P2 | P3 | Frame ms P2 | P3 |
|---|---|---|---:|---:|---:|---:|---:|---:|
| Nhẹ | Ngày nắng | Sân tượng đài | 381,927 | 381,481 | 416 | 419 | 3066 | 3133 |
| Nhẹ | Ngày nắng | Mũi công viên | 435,327 | 437,068 | 391 | 410 | 3137 | 3196 |
| Nhẹ | Ngày nắng | Vỉa hè Hùng Vương | 342,330 | 343,483 | 137 | 150 | 1662 | 1640 |
| Nhẹ | Ngày mưa | Sân tượng đài | 384,588 | 384,462 | 384 | 387 | 2961 | 3011 |
| Nhẹ | Ngày mưa | Mũi công viên | 435,211 | 436,952 | 339 | 358 | 3029 | 3021 |
| Nhẹ | Ngày mưa | Vỉa hè Hùng Vương | 342,330 | 343,483 | 138 | 151 | 1564 | 1636 |
| Nhẹ | Đêm | Sân tượng đài | 389,870 | 389,744 | 389 | 392 | 3775 | 3775 |
| Nhẹ | Đêm | Mũi công viên | 435,189 | 436,930 | 339 | 358 | 4278 | 4250 |
| Nhẹ | Đêm | Vỉa hè Hùng Vương | 344,627 | 345,506 | 139 | 154 | 2000 | 2040 |
| Nhẹ | Đêm + pháo hoa | Sân tượng đài | — | 385,922 | — | 389 | — | 3858 |
| Nhẹ | Đêm + pháo hoa | Mũi công viên | — | 438,934 | — | 369 | — | 4222 |
| Nhẹ | Đêm + pháo hoa | Vỉa hè Hùng Vương | — | 348,492 | — | 158 | — | 2033 |
| Cao | Ngày nắng | Sân tượng đài | 607,064 | 605,978 | 396 | 399 | 4375 | 4166 |
| Cao | Ngày nắng | Mũi công viên | 526,723 | 527,148 | 352 | 368 | 4178 | 4016 |
| Cao | Ngày nắng | Vỉa hè Hùng Vương | 421,452 | 422,331 | 143 | 158 | 1990 | 2013 |
| Cao | Ngày mưa | Sân tượng đài | 567,617 | 563,997 | 397 | 398 | 3950 | 3916 |
| Cao | Ngày mưa | Mũi công viên | 549,242 | 551,467 | 350 | 369 | 4028 | 4028 |
| Cao | Ngày mưa | Vỉa hè Hùng Vương | 421,452 | 422,331 | 144 | 159 | 2017 | 2060 |
| Cao | Đêm | Sân tượng đài | 631,401 | 629,675 | 401 | 404 | 5508 | 5591 |
| Cao | Đêm | Mũi công viên | 558,188 | 558,649 | 340 | 359 | 5841 | 6025 |
| Cao | Đêm | Vỉa hè Hùng Vương | 424,293 | 425,194 | 142 | 160 | 2600 | 2639 |
| Cao | Đêm + pháo hoa | Sân tượng đài | — | 598,961 | — | 391 | — | 5666 |
| Cao | Đêm + pháo hoa | Mũi công viên | — | 527,068 | — | 360 | — | 5758 |
| Cao | Đêm + pháo hoa | Vỉa hè Hùng Vương | — | 421,972 | — | 161 | — | 2694 |
| Tối đa | Ngày nắng | Sân tượng đài | 1,465,254 | 1,459,889 | 981 | 999 | 6016 | 5933 |
| Tối đa | Ngày nắng | Mũi công viên | 1,403,632 | 1,406,356 | 987 | 1043 | 5700 | 5583 |
| Tối đa | Ngày nắng | Vỉa hè Hùng Vương | 1,287,304 | 1,288,096 | 708 | 753 | 3422 | 3355 |
| Tối đa | Ngày mưa | Sân tượng đài | 1,465,036 | 1,459,109 | 984 | 1002 | 6000 | 5766 |
| Tối đa | Ngày mưa | Mũi công viên | 1,405,364 | 1,406,356 | 998 | 1044 | 5691 | 5533 |
| Tối đa | Ngày mưa | Vỉa hè Hùng Vương | 1,294,594 | 1,294,934 | 709 | 753 | 3422 | 3422 |
| Tối đa | Đêm | Sân tượng đài | 1,458,561 | 1,454,441 | 977 | 1000 | 7825 | 7650 |
| Tối đa | Đêm | Mũi công viên | 1,407,986 | 1,403,194 | 996 | 1022 | 7250 | 7150 |
| Tối đa | Đêm | Vỉa hè Hùng Vương | 1,293,866 | 1,290,262 | 717 | 757 | 4092 | 4108 |
| Tối đa | Đêm + pháo hoa | Sân tượng đài | — | 1,451,869 | — | 995 | — | 7650 |
| Tối đa | Đêm + pháo hoa | Mũi công viên | — | 1,393,736 | — | 1019 | — | 7391 |
| Tối đa | Đêm + pháo hoa | Vỉa hè Hùng Vương | — | 1,280,438 | — | 756 | — | 4125 |

Summary:

- Frame time is within run-to-run noise of Phase 2 in every shared cell (between −5% and +5%).
- Draw calls rise by up to about 55 per view (traffic and pedestrian signal heads, zebra and stop lines, quest props, seat/eat props). Triangles rise by under 1%.
- A running fireworks show changes frame time by −4% to +4% against plain night: sparks are one pooled `THREE.Points` draw (1,800 slots, 320/900/1,800 live caps for Nhẹ/Cao/Tối đa), no per-spark mesh or light; the single flash light is used only on Tối đa.
- With no show running, the event system costs nothing per frame beyond one state check: the points object is hidden and nothing is updated.
- 20 start/stop cycles left geometry, texture and scene-object counts unchanged (616 / 267 / 643 before and after).
