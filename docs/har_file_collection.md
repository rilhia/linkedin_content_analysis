
## Best Practice: Capturing Large HAR Datasets from LinkedIn (Option 2)

When using LinkedIn's **infinite scroll** (e.g. browsing posts in a feed or profile), Chrome will continuously stream and load more data via network requests.

However — the Chrome DevTools HAR capture has a limitation:

- The HAR file grows as you scroll.
- But **it is NOT infinite** — older data may be dropped as the file grows too large.
    - Chrome uses an internal buffer and eventually discards old entries (not strictly FIFO, but similar).
    - This can result in "missing" data if you rely on a single HAR file after heavy scrolling.

### 🔥 Why Option 2 is Best

**Option 2** — Save and Reset the HAR every few scrolls — gives you a clean, reliable way to capture large volumes of LinkedIn data.

### Recommended Workflow:

1️⃣ Open Chrome DevTools → Network Tab  
2️⃣ Enable "Preserve log" (important!)  
3️⃣ Start recording (red dot)  
4️⃣ Begin scrolling through LinkedIn content  
5️⃣ Every **10-20 scrolls** (or when the feed feels "refreshed"):
   - Click "Export HAR" → Save the file (e.g. `linkedin_1.har`)
   - **Then click "Clear" (trash can icon)** to reset the Network log
   - Continue scrolling → new data will appear → repeat

6️⃣ Repeat this cycle:
   - Scroll → Save HAR → Reset → Scroll → Save HAR → Reset ...

7️⃣ At the end you will have **multiple HAR files**:
    - `linkedin_1.har`
    - `linkedin_2.har`
    - `linkedin_3.har`
    - ...

### Why this works:

✅ Prevents Chrome from dropping early data  
✅ Gives you "batches" of HAR files → easy to merge in the notebook  
✅ Safer than trying to capture everything in one huge HAR  
✅ More stable for LinkedIn's dynamic loading patterns  

---

### Important:

- **Do not refresh the LinkedIn page mid-capture** — it will reset internal state and may break connections between posts.
- You can safely **switch tabs / windows** — just don’t reload the LinkedIn feed itself.
- If you reach the bottom of a feed, you can scroll back up and **keep capturing** — LinkedIn reuses GraphQL requests so "older" posts can still appear.

---

This is the **best practice** if you want:
- High volume post collection (hundreds / thousands of posts)
- Reliable linkages between posts
- Safe merging across sessions

And — this is exactly why the notebook was designed to **merge multiple HAR files** automatically! 🚀
