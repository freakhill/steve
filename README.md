Data lifted from https://www.youtube.com/watch?v=hH8w3mLAFfw

Dot language tutorial http://www.graphviz.org/pdf/dotguide.pdf

![Alt text](https://g.gravizo.com/source/custom_mark10?https%3A%2F%2Fraw.githubusercontent.com%2Ffreakhill%2Fsteve%2Fmaster%2FREADME.md)
<details> 
<summary></summary>
custom_mark10
digraph steve {
    rankdir=LR;
    size="8,5"
    node [shape = doublecircle]; Neutral PKB LWV RWV ALB SWY DCK FLK DOWN;
    node [shape = circle];

    // stances
    //subgraph clusterFromNeutral {
    //    rank = same; Neutral; PKB; LWV; RWV; ALB; SWY; DCK; FLK;
    //}

    // switch to stances
    Neutral -> PKB [ label = "f3+4" ];
    Neutral -> LWV [ label = "3" ];
    Neutral -> RWV [ label = "4" ];
    Neutral -> ALB [ label = "3+4" ];
    Neutral -> SWY [ label = "b3 or b4" ];
    Neutral -> DCK [ label = "f3 or f4" ];
    Neutral -> FLK [ label = "b3+4" ];

    // from neutral stance!
    "b+1" [ label "b+1 (i13)" ];
    "qcf+1" [ label "qcf+1 (i16)" ];
    "df+1,2~1" [ label "df+1,2~1 (i13)" ];
    "1,2,1" [ label "1,2,1 (i10)" ];
    "1,d+1" [ label "1,d+1 (i10)" ];
    "1,1,d+1" [ label "1,1,d+1 (i10)" ];
    "2,1" [ label "2,1 (i12)" ];
    "f+2,1" [ label "f+2,1 (i21)" ];
    Neutral -> "b+1";
    Neutral -> "qcf+1";
    Neutral -> "df+1,2~1";
    Neutral -> "1,2,1";
    Neutral -> "1,d+1",
    Neutral -> "1,1,d+1";
    Neutral -> "2,1";
    Neutral -> "f+2,1";
    "b+1" -> FLK [ label = "b -1/+9/CS" ];
    "qcf+1" -> FLK [ label = "b -3/KND/KND" ];
    "df+1,2~1" -> FLK [ label = "b 0/+4/CS" ];
    "1,2,1" -> FLK [ label = "b -1/+5/+5" ];
    "1,d+1" -> FLK [ label = "b 0/+6/+11" ];
    "1,1,d+1" -> FLK [ label = "b 0/+6/+11" ];
    "2,1" -> FLK [ label = "b +3/+14GB/+14" ];
    "f+2,1" -> FLK [ label = "b +1/+5/+5" ];
    
    // from LWV
    "LWV 1,f+1,1" [ label = "1,f+1,1 (i23)";
    LWV -> "LWV 1,f+1,1";
    "LWV 1,f+1,1" -> FLK [ label = "b +4/+8/CS" ];
    
    // from PAB
    "PAB b+1,1,2,1" [ label = "b+1,1,2,1 (i18)" ];
    PAB -> "PAB b+1,1,2,1";
    "PAB b+1,1,2,1" -> FLK [ label = "b -3/KND/KND" ];
    
    // from FLK
    "FLK 1" [ label = "1 (i12)" ];
    "FLK 1,1" [ label = "1,1 (i12)" ];
    "FLK 1,1,1" [ label = "1,1,1 (i12)" ];
    "FLK 1,d+1" [ label = "1,d+1 (i12) high,(d)high 0/KND/CS" ];
    "FLK 1,f+1" [ label = "1,f+1 (i12) high,(d)mid -5/0/KND" ];
    "FLK b+2" [ label = "b+2 (i19) pc8~13 -10/KND/KND high, right-steppable" ];
    "FLK 2" [ label = "2 (i23) 0/KND/KND" ];
    "FLK 1+2" [ label = "1+2 (i12) Trhow" ];
    FLK -> "FLK 1";
    FLK -> "FLK 1,1";
    FLK -> "FLK 1,1,1";
    FLK -> "FLK 1,d+1";
    FLK -> "FLK 1,d+1";
    FLK -> "FLK 1,f+1";
    FLK -> "FLK b+2";
    FLK -> "FLK 2";
    FLK -> "FLK 1+2";
    "FLK 1,d+1" -> { "DMG db+2"; "DMG f,F+2"; };
    "FLK 1" -> FLK [ label = "b -1/+10/+10" ];
    "FLK 1,1" -> FLK [ label = "b -3/+5/+5" ];
    "FLK 1,1,1" -> FLK [ label = "b -4/+4/+4" ];
    "FLK 1" -> ALB [ label = "b+3+4" ];
    "FLK 1" -> "ALB 2" [ label = "b+3+4,2 CH combo" ];
    "FLK 1,1" -> ALB [ label = "b+3+4" ];
    "FLK 1,1,1" -> ALB [ label = "b+3+4" ];
    "FLK 1,f+1" -> "DMG f,F+2" [ label = "on 2nd hit CH" ];
    "FLK b+2" -> "DMG f,F+2" [ label = "on hit" ];
    "FLK b+2" -> "DMG FLK b+2";
    "FLK 2" -> "DMG db+2";
    "FLK 1+2" -> "OKI df+1+2" [ label = "meaty -12/KND/KND" ];
    "FLK 1+2" -> "OKI db+2" [ label = "avoid with left-roll right" ];
    "FLK 1+2" -> "OKI d+1+2" [ label "catch all" ];
    
    // from ALB
    "ALB 2" [ label = "2" ];
    
    // ==============================================
    // GUARANTEED DAMAGE!
    // ==============================================
    node [ shape = box ];
    "DMG db+2" [ label = "db+2" ];
    "DMG f,F+2" [ label = "f,F+2 (floor breaks)" ];
    
    // ==============================================
    // COMBOS!
    // ==============================================
    node [ shape = box3d ];
    "DMG FLK b+2" [ label = "FLK b+2, DCK1+2,2,b+3+4~db~n,1 (iWS1) f+1,1~b (FLK), DCKf+2 S! (<- extended duck and dash) df+1+2" ];
    
    
    // ==============================================
    // OKI!
    // ==============================================
    node [ shape = component ];
    "OKI df+1+2" [ label = "df+1+2" ];
    "OKI db+2" [ label = "db+2" ];
    "OKI d+1+2" [ label = "d+1+2" ];
    
}
custom_mark10
</details>
