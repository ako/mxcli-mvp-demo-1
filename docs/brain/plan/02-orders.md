# Slice: 02-orders

<!-- mxcli-brain -->

Requirements for this slice. Anchors point FORWARD, at what the slice
will build — an anchor that does not resolve yet means not built, not
stale. `mxcli brain plan` counts them against the model.

## Record webshop orders with customer, delivery address and order lines

Anchors: `@Logistics.WebOrder`, `@Logistics.OrderLine`, `@Logistics.WebOrder_Overview`, `@Logistics.WebOrder_NewEdit` · id `0ccf12` · 2026-09-28

## Move an order through fulfilment: new, picking, packed, shipped, delivered

Anchors: `@Logistics.ENUM_OrderStatus`, `@Logistics.ACT_WebOrder_Advance` · id `12da28` · 2026-09-28
