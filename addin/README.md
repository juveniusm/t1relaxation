# T1 Relaxation — PowerPoint Content Add-in

Embeds the live T1 relaxation visualization (hosted on GitHub Pages) inside a PowerPoint slide.

## Sideload the add-in (Windows)

1. Pick a folder to act as a trusted catalog, e.g. `C:\OfficeAddins`. Right-click it → **Properties** → **Sharing** → **Share** → share with your user → copy the network path (looks like `\\YOUR-PC\OfficeAddins`).
2. In PowerPoint: **File → Options → Trust Center → Trust Center Settings → Trusted Add-in Catalogs**.
   - Paste the network path, click **Add catalog**, tick **Show in Menu**, click **OK**, then restart PowerPoint.
3. Copy `addin\manifest.xml` from this repo into that shared folder.
4. In PowerPoint: **Insert → Get Add-ins → SHARED FOLDER** tab → select **T1 Relaxation** → **Add**.

The add-in loads `https://juveniusm.github.io/t1relaxation/` into a slide-embedded frame.

## Sideload (Mac)

Drop `manifest.xml` into:

```
~/Library/Containers/com.microsoft.Powerpoint/Data/Documents/wef/
```

(create the `wef` folder if it doesn't exist), then restart PowerPoint and use **Insert → My Add-ins → Developer Add-ins**.

## Notes

- The manifest GUID is `0c52dd6a-1251-4878-b0ed-776430672d02`. Change it if you fork.
- `SourceLocation` and `IconUrl` must be HTTPS. GitHub Pages serves both.
- If the icon doesn't render, replace `icon.svg` with a 64x64 PNG and update the manifest's `IconUrl`.
