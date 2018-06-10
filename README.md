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
    Neutral -> "b+1";
    Neutral -> "qcf+1";
    Neutral -> "df+1,2~1";
    Neutral -> "1,2,1";
    Neutral -> "1,d+1",
    Neutral -> "1,1,d+1";
    Neutral -> "2,1";
    "b+1" -> FLK [ label = "b -1/+9/CS" ];
    "qcf+1" -> FLK [ label = "b -3/KND/KND" ];
    "df+1,2~1" -> FLK [ label = "b 0/+4/CS" ];
    "1,2,1" -> FLK [ label = "b -1/+5/+5" ];
    "1,d+1" -> FLK [ label = "b 0/+6/+11" ];
    "1,1,d+1" -> FLK [ label = "b 0/+6/+11" ];
    "2,1" -> FLK [ label = "b +3/+14GB/+14" ];
    
}
custom_mark10
</details>
