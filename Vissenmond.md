# README -- Uitslag vismond (T-verbinding)

Deze formule beschrijft de uitslag van een **vismond** voor een
T-verbinding van twee buizen met gelijke buitendiameter die elkaar onder
**90°** kruisen.

## Voorbeeld: Ø300 mm

-   Buitendiameter: **300 mm**
-   Straal: **150 mm**

De uitslag wordt berekend met:

\[ y = 150 `\left`{=tex}(1 -
`\left`{=tex}\|`\cos`{=tex}`\left`{=tex}(`\frac{x}{150}`{=tex}`\right`{=tex})`\right`{=tex}\|`\right`{=tex})
\]

waarbij:

-   **x** = afstand langs de ontwikkelde omtrek (0 t/m 942,478 mm)
-   **y** = uitsnijdiepte vanaf het rechte buiseinde (mm)

De ontwikkelde lengte is:

\[ L = 2`\pi `{=tex}r = 942{,}478 `\text{mm}`{=tex} \]

## Excel

``` text
=150*(1-ABS(COS(A2/150)))
```

waarbij **A2** de afstand langs de ontwikkelde plaat in millimeters
bevat.

## Andere buisdiameter

Voor een andere buitendiameter **D** vervang je overal de straal:

``` text
r = D / 2
```

De algemene formule wordt dan:

\[ y = r `\left`{=tex}(1 -
`\left`{=tex}\|`\cos`{=tex}`\left`{=tex}(`\frac{x}{r}`{=tex}`\right`{=tex})`\right`{=tex}\|`\right`{=tex})
\]

en de ontwikkelde lengte van de plaat is:

\[ L = 2`\pi `{=tex}r = `\pi `{=tex}D \]

Voorbeeld: bij een buis van Ø400 mm geldt **r = 200 mm** en wordt de
Excel-formule:

``` text
=200*(1-ABS(COS(A2/200)))
```
