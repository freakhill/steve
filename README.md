![Alt text](https://g.gravizo.com/source/custom_mark10?https%3A%2F%2Fraw.githubusercontent.com%2freakhill%2Fsteve%2Fmaster%2FREADME.md)
<details> 
<summary></summary>
custom_mark10
digraph steve {
    rankdir=LR;
    size="8,5"
    node [shape = doublecircle]; Neutral PKB LWV RWV ALB SWY DCK FLK Down;
    node [shape = circle];
    Neutral -> PKB [ label = "f3+4" ];
    Neutral -> LWV [ label = "3" ];
    Neutral -> RWV [ label = "4" ];
    Neutral -> ALB [ label = "3+4" ];
    Neutral -> SWY [ label = "b3 or b4" ];
    Neutral -> DCK [ label = "f3 or f4" ];
    Neutral -> FLK [ label = "b3+4" ];
    Neutral -> b1;
    b1 -> FLK [ label = "b" ];
}
</details>
