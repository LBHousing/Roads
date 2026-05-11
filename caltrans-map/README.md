# Caltrans KML/KMZ Viewer

This sample shows a simple HTML page that loads a KML/KMZ file into a Google map in the browser.

## How to use

1. Open `index.html` in a text editor.
2. Replace `YOUR_API_KEY` with your Google Maps JavaScript API key.
3. Replace `https://YOUR_KML_URL.kml` with the public URL to your KML or KMZ file.
4. Save and host the HTML page where your locked-down site allows it.

## Notes

- The KML/KMZ file must be publicly accessible by URL.
- If the file is KMZ, Google Maps can often load it directly if the URL points to the `.kmz` file.
- Use `mapTypeId: 'satellite'` to give the map an Earth-like view.

## Portal integration options

1. `portal-source-inline.html` — use this first if the portal allows inline HTML and inline JavaScript.
   - Replace `YOUR_API_KEY` and `YOUR_KML_URL`.
   - Paste the full block into the portal HTML source editor.
2. `portal-source-snippet.html` — alternative if the portal accepts explicit `<script src="...">` tags.
   - Replace `YOUR_API_KEY` and `YOUR_KML_URL`.
   - Paste the full block into the portal HTML source editor.
3. `portal-embed.html` — fallback if the portal allows iframe embedding.
   - Host `index.html` on a public web server.
   - Paste the iframe snippet into the portal source block.

## Portal guidance

- If the portal sanitizes `<script>` tags but preserves inline JavaScript inside a source block, use `portal-source-inline.html`.
- If `script` tags are fully blocked, the portal likely cannot load a custom Google map directly without admin support.
- If you can contact the portal admin, ask whether the source block supports inline JavaScript or only pure HTML.
