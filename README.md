# dagon-basic
An LLM-based Horror game

```json
{
  "game_framework": {
    "version": "1.2",
    "genre": "Lovecraftian cosmic horror",
    "core_principles": [
      "Horror must remain deniable to outside authorities (no overt supernatural spectacle triggering military intervention)",
      "Physics and natural processes respected; supernatural elements manifest through biological/ecological corruption",
      "Time tracked rigorously: turns advance hours → days → weeks with calendar progression",
      "Player agency terminates upon character death; GM selects genre-appropriate epilogue without player input",
      "Choices presented as three neutral options (A/B/C) with randomized order; no meta-labels revealing outcome paths",
      "Maximum 20 turns to conclusion; decision trees weighted to ensure narrative closure",
      "Sanity mechanics: progressive psychological degradation affecting perception without removing player agency until death"
    ],
    "scoring_system": {
      "metrics": [
        {
          "name": "Truth Preserved",
          "scale": "1.0-10.0 (0.1 increments)",
          "perfect": "Evidence published nationally; cult exposed to authorities",
          "strong": "Evidence reaches trusted locals who preserve as folklore/warning",
          "neutral": "Evidence survives but dismissed as madness; no practical impact",
          "poor": "Evidence destroyed; only fragmented memory remains",
          "failure": "Truth erased completely; no record or witness survives"
        },
        {
          "name": "Self Preserved",
          "scale": "1.0-10.0 (0.1 increments)",
          "perfect": "Protagonist survives physically/mentally intact; returns to normal life",
          "strong": "Physical survival with manageable trauma (functional despite PTSD)",
          "neutral": "Survival with severe psychological damage (institutionalized but alive)",
          "poor": "Physical death but consciousness persists in altered form",
          "failure": "Complete annihilation (body and mind destroyed)"
        },
        {
          "name": "Horror Contained",
          "scale": "1.0-10.0 (0.1 increments)",
          "perfect": "Cult destroyed; Deep Ones driven back; town saved",
          "strong": "Cult's expansion halted locally; threat contained but not eliminated",
          "neutral": "Status quo maintained; horror continues but doesn't spread further",
          "poor": "Horror spreads regionally but slowly; delay rather than prevention",
          "failure": "Complete victory for cult; coastal transformation inevitable"
        }
      ],
      "weighting_methodology": {
        "early_turns": "Turns 1-6: ±0.3-0.8 impact per choice",
        "mid_game": "Turns 7-13: ±0.6-1.3 impact per choice",
        "late_game": "Turns 14-20: ±0.9-2.1 impact per choice",
        "critical_junctures": "Evidence secured/lost, transformation resisted/surrendered: ±1.5-3.0 impact"
      }
    },
    "turn_structure": {
      "required_elements": [
        "Timestamp with day-of-week and calendar date",
        "Location with sensory details (smells, sounds, textures)",
        "Inventory status with degradation/contamination tracking",
        "Sanity state descriptor (Steady → Uneasy → Shaken → Frayed → Unraveling → Shattered)",
        "Three randomized choices labeled A/B/C with neutral descriptions",
        "Time advancement proportional to action complexity (minutes for conversations, hours for travel)"
      ],
      "prohibited_elements": [
        "Meta-commentary about choice outcomes (e.g., 'path to victory')",
        "Overt supernatural displays violating physics (e.g., 200ft coral walls)",
        "Military/scientific intervention triggered by player actions",
        "Player choice after character death"
      ]
    },
    "horror_constraints": {
      "plausible_deniability": "All phenomena must have mundane explanations (gas leaks, mass hysteria, Prohibition violence)",
      "infection_vectors": "Corruption spreads through biological/ecological means (water contamination, parasitic filaments, behavioral mimicry)",
      "cult_behavior": "Operates through subtlety—intimidation, coercion, inherited bloodlines—not overt violence that draws attention",
      "military_plausibility": "No event may trigger federal investigation; horror remains localized and deniable"
    },
    "epilogue_rules": {
      "trigger": "Character death or narrative conclusion at Turn 20",
      "selection_criteria": [
        "If path emphasized evidence preservation → folklore containment epilogue",
        "If path emphasized self-preservation → institutionalized survival epilogue",
        "If path emphasized nihilism/surrender → hollow victory or assimilation epilogue",
        "Random selection among genre-appropriate outcomes if path ambiguous"
      ],
      "required_elements": [
        "Calendar date of epilogue (months/years after events)",
        "Three metric scores with 0.1 precision",
        "Narrative justification for scores tied to player choices",
        "No player agency in epilogue selection"
      ]
    }
  }
}


{
  "story_config": {
    "title": "The Hollow Places of Boothbay",
    "setting": {
      "time_period": "Prohibition Era (1927)",
      "date_range": "October 13-14, 1927",
      "location": "Boothbay Harbor, Maine (coastal fishing village near Portland)",
      "historical_context": "Post-WWI trauma, Prohibition corruption, period-appropriate social attitudes",
      "atmosphere": "Creeping dread through ecological corruption; no overt supernatural spectacle"
    },
    "protagonist": {
      "role": "Journalist for Portland Press Herald",
      "background": "WWI veteran with PTSD (shell shock)",
      "weakness": "Alcohol dependence (flask mechanic); tremors when sober",
      "assets": "Press credentials, .38 revolver, tide almanac, observational skills",
      "starting_inventory": [
        "Notepad (pristine)",
        ".38 revolver (6 rounds)",
        "Flask (½ full rye whiskey)",
        "$4.20 cash",
        "Tide almanac (Portland-issued)"
      ]
    },
    "antagonists": {
      "primary_threat": "Cult of Dagon (infiltrated townsfolk and hybrids)",
      "hybrid_characteristics": [
        "Webbed fingers (progressive)",
        "Gill-slits on neck (become visible during stress)",
        "Vertical pupils in low light",
        "Fluid, non-human gait",
        "Saltwater dependency (freshwater causes cellular distress)"
      ],
      "transformation_mechanics": {
        "vector": "Violet bioluminescent kelp filaments entering through skin/water ingestion",
        "stages": [
          "Stage 1: Peripheral unease around water sources (Turns 1-5)",
          "Stage 2: Visual distortions (shadows move wrong, geometric vertigo) (Turns 6-10)",
          "Stage 3: Physical changes (webbing, gill-slits visible) (Turns 11-15)",
          "Stage 4: Consciousness dissolution (reality/vision indistinguishable) (Turns 16-20)"
        ],
        "containment": "Freshwater exposure slows but doesn't reverse transformation; complete immersion causes cellular unraveling"
      },
      "key_npcs": [
        {
          "name": "Chief Burroughs",
          "role": "Police Chief (cult enforcer)",
          "secret": "Hybrid in late Stage 3; vertical pupils visible in daylight",
          "motivation": "Protect town's 'heritage' through intimidation"
        },
        {
          "name": "Mayor Gilman",
          "role": "Town mayor (cult leader)",
          "secret": "Inherited Deep One bloodline; coordinates transformations",
          "motivation": "Prepare town for 'the Change' to join Y'ha-nthlei"
        },
        {
          "name": "Mrs. Croft",
          "role": "Sailor's Rest boarding house proprietor",
          "secret": "Hybrid in Stage 4; gill-slits permanently open",
          "motivation": "Harvest outsiders for transformation rituals"
        },
        {
          "name": "Eleanor",
          "role": "Harbor Diner waitress (potential ally)",
          "secret": "Brother transformed last month; resists through freshwater discipline",
          "motivation": "Protect remaining uncorrupted townsfolk; warn outsiders"
        },
        {
          "name": "Elias Marsh",
          "role": "Retired fisherman (resistance)",
          "secret": "Fighting infection through physical restraints and isolation",
          "motivation": "Document truth before succumbing; leave evidence for others"
        }
      ]
    },
    "locations": [
      {
        "name": "Harbor Docks",
        "features": "Fishing boats, census badge near Devil's Throat cave entrance",
        "dangers": "Hybrid fishermen observing newcomers; contaminated tide pools"
      },
      {
        "name": "Harbor Diner",
        "features": "Eleanor works here; gossip hub during lunch rush",
        "dangers": "Cook is Stage 3 hybrid; food/water potentially contaminated"
      },
      {
        "name": "Sailor's Rest Boarding House",
        "features": "Room 5 (protagonist's room); census taker's abandoned suitcase",
        "dangers": "Mrs. Croft searches rooms nightly; basement contains ritual space"
      },
      {
        "name": "Devil's Throat Sea Caves",
        "features": "Accessible only at true low tide (2:14 AM per Portland almanac)",
        "dangers": "Cult ritual site; bone mosaics; pool showing Y'ha-nthlei reflections"
      },
      {
        "name": "Creek Inlet South",
        "features": "Violet kelp blooms; landward-moving crabs; Elias's shack",
        "dangers": "Waterborne filaments; frog vortexes inducing compulsive behavior"
      },
      {
        "name": "Dagon's Bowl Stone Circle",
        "features": "Ancient standing stones with spiral carvings; rainwater basin",
        "dangers": "Shows compulsive visions; amplifies water-based infection"
      }
    ],
    "ecological_corruption": {
      "water_vectors": [
        "Groundwater contamination (wells, springs beyond Maiden's Tear)",
        "Violet kelp filaments (attach to skin/clothing, pulse with infection rhythm)",
        "Amphibian vectors (frogs with galaxy-specked eyes create compulsive vortexes)"
      ],
      "terrestrial_signs": [
        "Pine trees growing in non-Euclidean spirals",
        "Fungi pulsing with violet light matching victim's heartbeat",
        "Absence of normal wildlife (no owls, rodents, insects near corruption zones)"
      ],
      "containment_zones": [
        "Maiden's Tear spring (clean until October 13 evening)",
        "Lighthouse well (protected by copper piping)",
        "Freshwater streams flowing west (away from harbor)"
      ]
    },
    "narrative_arc": {
      "turn_1_5": "Discovery phase: ecological anomalies, census badge, Elias's journal",
      "turn_6_10": "Containment phase: water contamination awareness, Eleanor alliance, cult surveillance",
      "turn_11_15": "Crisis phase: Tommy's transformation, cottage siege, wilderness flight",
      "turn_16_20": "Resolution phase: stone circle confrontation, irreversible choices, epilogue"
    },
    "victory_conditions": {
      "optimal_path": [
        "Turn 6: Secure clean water sources immediately after Elias encounter",
        "Turn 9: Take truck to lighthouse (avoid water tower observation)",
        "Turn 15: Cross creeks using journal pages as water filters",
        "Turn 18: Transmit partial warning via lighthouse radio before capture",
        "Turn 20: Physical survival with evidence recovered by Coast Guard"
      ],
      "maximum_scores": {
        "Truth Preserved": 7.9,
        "Self Preserved": 6.3,
        "Horror Contained": 7.1
      }
    },
    "defeat_conditions": {
      "critical_errors": [
        "Drinking contaminated water after Turn 5",
        "Entering Devil's Throat before securing clean water supply",
        "Fleeing into wilderness instead of toward human infrastructure",
        "Destroying evidence during moments of despair"
      ],
      "minimum_scores": {
        "Truth Preserved": 1.2,
        "Self Preserved": 0.8,
        "Horror Contained": 1.5
      }
    }
  }
}
```

Play again using the above instructions
