# Slice: 01-catalog-stock

<!-- mxcli-brain -->

Requirements for this slice. Anchors point FORWARD, at what the slice
will build — an anchor that does not resolve yet means not built, not
stale. `mxcli brain plan` counts them against the model.

## Keep a catalogue of the products the webshop sells (SKU, name, weight)

Anchors: `@Logistics.Product`, `@Logistics.Product_Overview` · id `e1a804` · 2026-09-28

## Keep track of the warehouses stock is held in

Anchors: `@Logistics.Warehouse`, `@Logistics.Warehouse_Overview` · id `1757e4` · 2026-09-28

## Record how many units of each product are on hand in each warehouse

Anchors: `@Logistics.StockLevel` · id `add038` · 2026-09-28

## Show total stock per product across all warehouses, computed by the database

Anchors: `@Logistics.ProductStock` · id `95e73c` · 2026-09-28
