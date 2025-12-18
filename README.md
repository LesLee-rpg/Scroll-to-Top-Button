# Scroll-to-Top Button

Egyszerű JavaScript gomb, amely a lap tetejére görgeti a felhasználót.

A kódot a saját weboldalam fejlesztéséhez készítettem, bal alsó sarokban megjelenő gombként.  
A gomb színe a vállalkozásom arculatához igazodik: `#ffeb3b`.

---

## Telepítés

Másold be az alábbi kódot a weboldalad HTML fájljába, közvetlenül a `</body>` elé:

```html
<!-- Scroll to Top Button - Left Side -->
<style>
/* ... ide jön a CSS ... */
</style>

<!-- Scroll to Top Button - Left Side -->
<style>
#scrollTopBtn {
  position: fixed;
  bottom: 30px;
  left: 30px;
  background: #ffeb3b;
  color: #000;
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  font-size: 24px;
  font-weight: bold;
  cursor: pointer;
  display: none;
  z-index: 9999;
  transition: 0.3s;
  box-shadow: 0 0 10px rgba(0,0,0,0.3);
}

#scrollTopBtn:hover {
  background: #f1d600;
}
</style>

<div id="scrollTopBtn">∧</div>

<script>
let btn = document.getElementById("scrollTopBtn");

window.onscroll = function () {
  if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
    btn.style.display = "flex";
  } else {
    btn.style.display = "none";
  }
};

btn.onclick = function () {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>


<script>
/* ... ide jön a JS ... */
</script>
```
## Funkciók

Automatikusan megjelenik görgetés után
Simán visszavisz a tetejére
Bal alsó sarokra pozicionált
Arculathoz illeszkedő szín (#ffeb3b)
Egyfájlos megoldás

---

## Élő példa

https://www.nemethlaszlokomuves.hu

---

## Fejlesztési tervek:

Mobilbarát verzió

SVG ikon opciók

Dark mode

Automatikus méretezés

---

## Changelog
v1.0 — (2025.12.18)

Alapverzió feltöltve

Működő scroll-to-top gomb

Egyfájlos telepítés

# License

MIT License
Felhasználható, módosítható, terjeszthető — kérlek jelöld a forrást.

