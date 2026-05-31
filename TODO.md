# TODO - Pulse path connectors

## Plan (approved)
- Update `src/App.jsx` so connector lines between icon nodes and chip use `PULSE_PATHS` instead of `defaultRouteD` / `ROUTES_NODE_OVERRIDES`.
- Use a **strict mapping**: each node id is fixed to a specific pulse path index.

## Steps
1. Add helper to convert `PULSE_PATHS` polyline segments to an SVG `d` string. ✅
2. Add `NODE_TO_PULSE_PATH_INDEX` mapping for node ids in `NODES`. ✅
3. Update `DiagramArea` SVG connector rendering to use `PULSE_PATHS[mappedIndex]`. ✅
4. Temporarily keep `defaultRouteD` / `ROUTES_NODE_OVERRIDES` as fallback (or remove if not needed after verification). ✅ (fallback kept)
5. Run the dev server and visually verify connector paths align with trace routes.


