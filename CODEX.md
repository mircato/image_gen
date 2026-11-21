# Map pieces to paint (Qesas map library, our region)

You are painting 144 map pieces, one image each. Work in this folder: `E:\Claude-projects\Qesas\experiments\mapdive2\chatgpt`

## Files
- `order.txt`: the piece codes, one per line, in the order to paint them (Egypt first, then Palestine, Saudi Arabia, Libya, ...).
- For each code `XXX-ij` there are two input images in this folder:
  - `XXX-ij-1map.jpg` = IMAGE 1, the exact map (where every coast, river, lake and border is).
  - `XXX-ij-2guide.jpg` = IMAGE 2, the same area cut from our painted atlas map (the style and colours to match).
- Put each finished picture in the subfolder `out` as `out/XXX-ij.png` (create `out` if it is missing).

## For each code in order.txt, one at a time
1. If `out/XXX-ij.png` already exists, skip it (so the work can be stopped and resumed).
2. Look at both input images, then use your built-in IMAGE GENERATION tool, with both images as the input/reference images
   (IMAGE 1 first, IMAGE 2 second), and the BRIEF below as the prompt. Wide 16:9 landscape.
3. Look at the result. If it has ANY text, letters, names, a compass or a frame, or the coasts are clearly not where IMAGE 1
   has them, generate it again (at most 2 more tries).
4. Save it as `out/XXX-ij.png`.
5. Go on with the next code. Do the 4 pieces of one country (same 3 letters) one right after the other, so they look alike.

## Never
- NEVER copy, resize, edit or save IMAGE 1, IMAGE 2 or any other existing file as a result. Every result must be a NEW picture
  made by the image generation tool. (Pictures that are copies are detected and thrown away.)
- Never draw it yourself with code (Python, PIL, SVG...).
- If the image generation tool is not available, or says you are out of quota / at a limit, STOP right away and say so.
  Do not try any other way.

## When you stop
Say how many pieces are in `out` and which code is next.

## BRIEF (the prompt for every piece)
IMAGE 1 is an exact map: its coastlines, rivers, lakes and borders are exact and its colours show the true kind of ground. It is the map of a place and the land around it, all painted the same way (the neighbours are not paler). Draw NO buildings, monuments, pyramids, temples, mosques, palms, oases, animals or figures anywhere: only the land, its relief, its waters and its borders. IMAGE 2 is the SAME area as it is on our painted map of the wider area, enlarged: keep its colours and look so the two maps match, only add the finer detail a closer map has. Paint IMAGE 1 in the very same style as IMAGE 2 (an old hand-coloured relief atlas, richly illustrated: soft green lowlands, tan and brown mountains with hachure shading wherever IMAGE 1 shows relief, finely stippled sand seas, pale blue seas with fine engraved wave lines along the coasts, rivers in blue, faint dotted borders, aged paper): the same colours, line work and texture, so it looks cut from the same atlas. TRACE IMAGE 1: every coastline, river, lake and border stays EXACTLY where it is, same framing, same scale, same orientation; do not move, crop, zoom, rotate or invent land. Lines as thin as an atlas at this scale. Wide 16:9 landscape covering exactly the same area as IMAGE 1. ABSOLUTELY NO TEXT: no names, no labels, no letters, no compass, no frame. Make a new painting: do not return IMAGE 1 or IMAGE 2 as it is.
