# Daily Reflection Tree — Visual Diagram

```mermaid
flowchart TD
    START([🌙 START\nGood evening...]) --> A1_OPEN

    A1_OPEN[/A1_OPEN\nWeather report today?/]
    A1_OPEN -->|Sunny / Mixed| A1_D1_H[A1_D1\nRoute: HIGH]
    A1_OPEN -->|Cloudy / Stormy| A1_D1_L[A1_D1\nRoute: LOW]

    A1_D1_H --> A1_Q_AGENCY_HIGH[/A1_Q_AGENCY_HIGH\nWhen things went well\nwhat made it happen?/]
    A1_D1_L --> A1_Q_AGENCY_LOW[/A1_Q_AGENCY_LOW\nWhen things got difficult\nwhat did you do?/]

    A1_Q_AGENCY_HIGH -->|Prepared / Adapted| A1_Q_CHOICE_INT
    A1_Q_AGENCY_HIGH -->|Timing / Someone else| A1_Q_CHOICE_EXT
    A1_Q_AGENCY_LOW -->|Looked for control / Pushed through| A1_Q_CHOICE_INT
    A1_Q_AGENCY_LOW -->|Waited / Frustrated| A1_Q_CHOICE_EXT

    A1_Q_CHOICE_INT[/A1_Q_CHOICE_INT\nWhat did you actually do\nwhen plans changed?/]
    A1_Q_CHOICE_EXT[/A1_Q_CHOICE_EXT\nWas there a choice available\neven a small one?/]

    A1_Q_CHOICE_INT --> A1_R_INT
    A1_Q_CHOICE_EXT -->|Yes / Maybe| A1_R_INT_SOFT
    A1_Q_CHOICE_EXT -->|Not really / Wouldn't matter| A1_R_EXT

    A1_R_INT[📖 A1_R_INT\nYou stayed in the\ndriver's seat today]
    A1_R_INT_SOFT[📖 A1_R_INT_SOFT\nNoticing the gap is\nwhere agency begins]
    A1_R_EXT[📖 A1_R_EXT\nHard days pull focus outward\nBut you made a call]

    A1_R_INT --> BRIDGE_1_2
    A1_R_INT_SOFT --> BRIDGE_1_2
    A1_R_EXT --> BRIDGE_1_2

    BRIDGE_1_2[⬦ BRIDGE 1→2\nFrom how you handled it\nto what you brought]

    BRIDGE_1_2 --> A2_OPEN

    A2_OPEN[/A2_OPEN\nYour interactions today —\ngiving or receiving?/]
    A2_OPEN -->|Giving / Balanced| A2_Q_CONTRIB
    A2_OPEN -->|Receiving / Transacting| A2_Q_ENTITLE

    A2_Q_CONTRIB[/A2_Q_CONTRIB\nDid you do something\nnot required of you?/]
    A2_Q_ENTITLE[/A2_Q_ENTITLE\nDid you feel your effort\nwasn't seen fairly?/]

    A2_Q_CONTRIB -->|Yes — outside scope / Flagged issue / Went deeper| A2_Q_MOTIVE
    A2_Q_CONTRIB -->|Not really| A2_Q_OPPORTUNITY

    A2_Q_ENTITLE -->|Underrecognized / Credit stolen| A2_R_ENTITLE
    A2_Q_ENTITLE -->|A little / Not focused| A2_Q_MOTIVE

    A2_Q_MOTIVE[/A2_Q_MOTIVE\nWhat was underneath\nthat effort?/]
    A2_Q_OPPORTUNITY[/A2_Q_OPPORTUNITY\nWas there a moment you\ncould have helped but didn't?/]

    A2_Q_MOTIVE --> A2_R_CONTRIB
    A2_Q_OPPORTUNITY -->|Saw it but busy / Not sure my place| A2_R_MISSED
    A2_Q_OPPORTUNITY -->|Maybe / No| A2_R_CONTRIB

    A2_R_CONTRIB[📖 A2_R_CONTRIB\nGiving without keeping score\nis rarer than it sounds]
    A2_R_ENTITLE[📖 A2_R_ENTITLE\nWanting recognition is human\nBut the shift to giving is energising]
    A2_R_MISSED[📖 A2_R_MISSED\nNoticing missed opportunities\nwithout guilt — that's growth]

    A2_R_CONTRIB --> BRIDGE_2_3
    A2_R_ENTITLE --> BRIDGE_2_3
    A2_R_MISSED --> BRIDGE_2_3

    BRIDGE_2_3[⬦ BRIDGE 2→3\nNow zoom out —\nwho else was in today?]

    BRIDGE_2_3 --> A3_OPEN

    A3_OPEN[/A3_OPEN\nWhose experience comes\nto mind first today?/]
    A3_OPEN -->|Just mine| A3_Q_SELF
    A3_OPEN -->|Team / Specific colleague| A3_Q_OTHER
    A3_OPEN -->|End user / Those we serve| A3_Q_WIDE

    A3_Q_SELF[/A3_Q_SELF\nDid anyone else's\nexperience cross your mind?/]
    A3_Q_OTHER[/A3_Q_OTHER\nDid that awareness\nchange how you acted?/]
    A3_Q_WIDE[/A3_Q_WIDE\nDid thinking of end users\nshift something for you?/]

    A3_Q_SELF -->|Yes — thought about team| A3_R_EXPAND
    A3_Q_SELF -->|Briefly / Not really / Unsure| A3_R_SELF

    A3_Q_OTHER -->|Checked in / Adjusted approach| A3_R_OTHER
    A3_Q_OTHER -->|Noticed but didn't act / Just shifted mood| A3_R_EXPAND

    A3_Q_WIDE -->|Reminded why / Made task meaningful| A3_R_TRANSCEND
    A3_Q_WIDE -->|Felt abstract / Too close to day-to-day| A3_R_EXPAND

    A3_R_SELF[📖 A3_R_SELF\nMeaning lives at the edge\nwhere worlds meet]
    A3_R_EXPAND[📖 A3_R_EXPAND\nYou glimpsed someone else's\nday inside your own]
    A3_R_OTHER[📖 A3_R_OTHER\nYou saw clearly and\nthat changed what you did]
    A3_R_TRANSCEND[📖 A3_R_TRANSCEND\nSelf-transcendence —\nwhat does the world need from me?]

    A3_R_SELF --> SUMMARY
    A3_R_EXPAND --> SUMMARY
    A3_R_OTHER --> SUMMARY
    A3_R_TRANSCEND --> SUMMARY

    SUMMARY[📊 SUMMARY\nToday's axis scores +\nPersonalised reflection]
    SUMMARY --> END([🌙 END\nRest well.\nTomorrow is another chance.])

    style START fill:#1a1a2e,color:#e0e0ff,stroke:#6c63ff
    style END fill:#1a1a2e,color:#e0e0ff,stroke:#6c63ff
    style BRIDGE_1_2 fill:#2d1b69,color:#c9b8ff,stroke:#6c63ff
    style BRIDGE_2_3 fill:#2d1b69,color:#c9b8ff,stroke:#6c63ff
    style SUMMARY fill:#1b3a2d,color:#b8ffd9,stroke:#00c896
    style A1_R_INT fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A1_R_INT_SOFT fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A1_R_EXT fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A2_R_CONTRIB fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A2_R_ENTITLE fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A2_R_MISSED fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A3_R_SELF fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A3_R_EXPAND fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A3_R_OTHER fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
    style A3_R_TRANSCEND fill:#1b2d3a,color:#b8d9ff,stroke:#4a9eff
```

## Node Count Summary

| Type | Count |
|------|-------|
| start | 1 |
| question | 12 |
| decision | 9 |
| reflection | 10 |
| bridge | 2 |
| summary | 1 |
| end | 1 |
| **Total** | **36** |

## Axes at a Glance

| Axis | Spectrum | Questions |
|------|----------|-----------|
| Axis 1: Locus | Victim ↔ Victor | A1_OPEN, A1_Q_AGENCY_HIGH/LOW, A1_Q_CHOICE_INT/EXT |
| Axis 2: Orientation | Entitlement ↔ Contribution | A2_OPEN, A2_Q_CONTRIB, A2_Q_ENTITLE, A2_Q_MOTIVE, A2_Q_OPPORTUNITY |
| Axis 3: Radius | Self-Centrism ↔ Altrocentrism | A3_OPEN, A3_Q_SELF, A3_Q_OTHER, A3_Q_WIDE |
