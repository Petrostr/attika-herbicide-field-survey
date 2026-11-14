# Survey form

[← Back to overview](README.md)

Each field point stores the fields below. Coded fields use a fixed list of values, so the answers can be counted and compared.

## Fields

| Field | Type | Values |
|---|---|---|
| `date_time` | automatic | date and time of the observation |
| `crop_type` | coded | `vineyard`, `olive`, `pistachio`, `fig`, `uncultivated`, `other_crop`, `uncertain` |
| `crop type other` | free text | crop name when `other_crop` is chosen |
| `spray_status` | coded | `sprayed_like`, `not_sprayed`, `uncertain` |
| `understory_state` | coded | `green`, `yellow_dry`, `bare_soil`, `tilled`, `mowed`, `mixed` |
| `management_evidence` | coded | `herbicide_consistent`, `tillage_consistent`, `mowing_consistent`, `grazing_consistent`, `no_suppression`, `uncertain` |
| `confidence` | coded | `A`, `B`, `C` |
| `control_case` | coded | `yes`, `no`, `possible` |
| `notes` | free text | anything the codes do not cover |
| `photo`, `photo1`, `photo2` | photo | up to three photos per point |

## What the main fields mean

**`spray_status`** is the overall visual judgement of the plot.

- `sprayed_like`: the ground cover looks as if a herbicide was used, for example yellow or dry strips along the rows next to green vegetation outside the plot.
- `not_sprayed`: the ground cover is green and looks normal.
- `uncertain`: the evidence is unclear.

"Sprayed-like" is a visual judgement. It does not confirm that a herbicide was applied.

**`understory_state`** describes the ground between the trees or vines at the time of the visit: green cover, yellow or dry vegetation, bare soil, tilled soil, mowed vegetation, or a mix.

**`management_evidence`** records which practice the visible evidence points to: herbicide, tillage, mowing, grazing, or no weed suppression at all.

**`confidence`** grades how clear the evidence is. `A` is clear, strong evidence. `B` and `C` are progressively weaker. Analyses can start with grade A only.

**`control_case`** marks plots that are clear reference examples, useful as training or validation cases.

## Form history

| Version | Content | Points |
|---|---|---|
| v1 (pilot) | photo + free notes | 101 |
| v2 | coded fields + confidence grade + up to 3 photos | 495 |

The 101 pilot points and the first v2 points describe the same plots. The pilot showed that free text was too slow to fill in and too hard to analyse.

## Known issues

- `spray_status` and `management_evidence` can disagree, for example a plot marked `sprayed_like` whose evidence is recorded as `tillage_consistent`. Bare soil from tillage can look sprayed at first sight. These cases need a second look before analysis.
- The coded fields were added during the first field days, so some early points have an empty `understory_state`, `management_evidence` or `confidence`.
