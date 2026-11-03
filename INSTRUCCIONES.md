# Stickers Celestes - APK (Brothers Delivery)

## Qué hace la app
- Lee el chat de WhatsApp (.zip o .txt) y cuenta los stickers.
- Los +20 / +10 se suman al sticker anterior (35 + 20 = 55).
- Muestra al final: **Entregar a Brothers Deliverys** = 30% de (35, 45, 55...) + total de los +7.
- Cuenta **pedidos**: cada sticker principal (35+7, 35+7+20, etc.) es un pedido. Al final muestra cuántos pedidos sacó el repartidor.
- Aparece en el menú **Compartir** de WhatsApp y procesa el .zip automáticamente.

## Estructura del repositorio
```
├─ www/index.html
├─ android-patch/
│   ├─ MainActivity.java
│   └─ share-filter.xml
├─ scripts/patch_manifest.py
├─ .github/workflows/build.yml
├─ package.json
├─ capacitor.config.json
└─ .gitignore
```

## Subir a GitHub
1. Crea un repositorio nuevo en github.com (puede ser privado).
2. Sube TODO el contenido con "Add file -> Upload files".
   - La carpeta `.github` es oculta. Si no la ves al subir, usa
     "Add file -> Create new file", escribe `.github/workflows/build.yml`
     como nombre y pega el contenido de `build.yml`.
3. Rama principal: `main`.

## Compilar el APK
1. Entra a la pestaña **Actions**. Si no corre solo: **Build APK -> Run workflow**.
2. Espera ~4-6 minutos hasta ver el check verde.
3. Abre el run -> sección **Artifacts** -> descarga `stickers-celestes-apk`.
4. Descomprime e instala `app-debug.apk` (permite "instalar apps desconocidas").

## Usarla desde WhatsApp
1. Abre el chat -> 3 puntitos -> Más -> **Exportar chat**.
2. Elige **Incluir archivos** (sin esto no aparecen los nombres de los stickers).
3. Elige **Stickers Celestes** en la lista de apps.
4. La app se abre y calcula sola.

## Si el build falla
Abre el run en Actions, entra al paso en rojo y copia el error.
