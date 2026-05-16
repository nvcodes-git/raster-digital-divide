# Territorial Digital Divide — Cusco Region

This project analyzes digital inequality in the Cusco region of Peru by combining NASA nighttime lights satellite data with mobile network coverage information. The central research question is: which territories in Cusco have significant human presence but lack connectivity, and how can we prioritize them for intervention?

## Dependencies

Install all required libraries with:

```bash
pip install -r requirements.txt
```

The notebook also installs dependencies automatically on the first cell run.

## How to Run

1. Download the input raster files from the course Google Drive folder and place them in the `data/` directory:
   - `VNL_cusco_2025.tif`
   - `kernel_cobmovil2019_50m.tif`
2. Open `notebooks/digital_divide_cusco.ipynb` in Jupyter or VS Code.
3. Run all cells from top to bottom. Each step builds on the previous one.

## Output Files

| File | Description |
|------|-------------|
| `output/vnl_norm.tif` | Normalized nighttime lights raster (0 to 1) |
| `output/conn_norm.tif` | Normalized mobile connectivity raster (0 to 1) |
| `output/ibd_brecha_digital.tif` | Digital Divide Index raster (IBD, range -1 to 1) |
| `output/clasificacion_brecha.tif` | 4-class territorial classification raster |
| `output/dashboard_brecha_digital.png` | Composite dashboard with all maps and statistics |

## Findings

About 91.8% of the Cusco region falls into the Critical Divide class, meaning most of the territory has both low nighttime light and no mobile coverage. The small urban clusters around Cusco city and the main road corridors account for nearly all connectivity, while vast rural Andean areas remain excluded on both dimensions. The Welch t-test between Urban Connected and Critical Divide classes confirmed a statistically significant difference (Cohen's d = 5.82), showing the gap between these zones is not marginal but structural.
