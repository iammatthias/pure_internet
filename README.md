# PURE INTERNET

**PURE INTERNET** is an art project exploring the boundaries of the web by embedding fully self-contained websites directly into NFC tags. These serverless sites require no external hosting or infrastructure, offering a glimpse into a truly decentralized and portable internet.

---

## **Concept**

The modern internet is heavily dependent on centralized servers and constant connectivity. **PURE INTERNET** seeks to reimagine this paradigm by storing entire websites within NFC tags. These tags carry self-contained data that browsers can interpret, creating an experience that is as much physical as it is digital.

---

## **How It Works**

1. **Encoding the Website**:
   - Websites are encoded as Base64 strings or lightweight JavaScript, small enough to fit into NFC tag memory.
   - The encoded content is written to the NFC tag as a URL or plain text record.

2. **Scanning the Tag**:
   - Users scan the NFC tag with their smartphone.
   - Depending on the encoding method, the website either loads automatically or requires minimal user interaction.

---

## **Methods Used**

Several approaches were explored to make websites work directly from NFC tags:

- **`data:` URIs**: Encodes HTML into a `data:text/html;base64,...` URI. This approach faced modern browser restrictions on top-level navigation.
- **`file://` Scheme**: Uses a `file://` scheme to store and render HTML. Browser support proved inconsistent.
- **`localhost` URLs**: Encodes websites in query strings or fragments (`#`) of `localhost` URLs, decoded via inline JavaScript.
- **Text Records**: Stores raw HTML as a plain text record for users to copy and paste into their browser.
- **JavaScript Bookmarklets**: Encodes dynamic rendering logic in a `javascript:` URL.
- **Inline JavaScript**: Combines JavaScript and HTML in a single encoded payload for self-rendering webpages.

---

## **Challenges**

1. **Browser Security**:
   - Many modern browsers block `data:` URIs and other non-standard schemes to prevent abuse.
2. **Tag Memory Limits**:
   - NTAG215 tags have a maximum usable memory of 504 bytes, requiring optimized content and encoding.
3. **Device Compatibility**:
   - NFC behavior and support for encoded URLs vary significantly between iOS and Android devices.

---

## **Usage**

1. **Scan an NFC Tag**:
   - Use an NFC-enabled smartphone to scan the tag.
   - Depending on the method, the website will either load directly or require you to follow simple instructions.

2. **Explore the Offline Internet**:
   - View the embedded experience entirely independent of any server or external connection.
