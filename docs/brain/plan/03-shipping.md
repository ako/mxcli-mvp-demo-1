# Slice: 03-shipping

<!-- mxcli-brain -->

Requirements for this slice. Anchors point FORWARD, at what the slice
will build — an anchor that does not resolve yet means not built, not
stale. `mxcli brain plan` counts them against the model.

## Keep track of the carriers used for shipping

Anchors: `@Logistics.Carrier` · id `7d54c8` · 2026-09-28

## Ship an order: create a shipment with carrier and tracking number and mark the order shipped

Anchors: `@Logistics.Shipment`, `@Logistics.ACT_WebOrder_Ship`, `@Logistics.Shipment_Overview` · id `57e121` · 2026-09-28
