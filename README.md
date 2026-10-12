# Reactor Profit Optimizer

An interactive web app that finds the most profitable operating point for a
continuous stirred-tank reactor (CSTR) running the series reaction A → B → C.

Choose your prices, heating and reactor costs, and process limits, then let the
optimizer search for the best reactor temperature, volume and feed rate.

## Features
- Live profit, B yield, A conversion and residence time as you move the sliders
- One-click optimization using multi-start Nelder–Mead with constraint penalties
- Profit vs temperature chart with infeasible regions marked in red
- Composition vs residence time chart showing where product B peaks
- Limit checks for max temperature, min conversion and max waste yield
- Light and dark themes, responsive layout, no dependencies

## The model
- First-order, irreversible reactions with Arrhenius rate constants
- Isothermal CSTR with feed concentration of 2 kmol/m³
- Profit = B sales − feed cost − C disposal − heating − reactor cost

## Key trade-off
Higher temperature speeds up the reaction but favors waste C, while a larger
reactor improves selectivity but costs more. The optimizer balances these
under your constraints.

## Run it
Open `index.html` in any browser. No build step or install needed.

## Tech
HTML, CSS and vanilla JavaScript (Canvas for charts).

## Possible extensions
Multiple reactors in series, price sensitivity analysis, CSV export, and
non-isothermal energy balances.