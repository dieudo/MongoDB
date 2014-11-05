607week10assignment
===================
Dieudonne Ouedraogo 


C:\mongodb\bin>mongo
MongoDB shell version: 2.4.12
connecting to: test
> db
test
> show dbs
WeekMongo       0.203125GB
employment      0.203125GB
local   0.078125GB
unitedstates    0.203125GB
> use WeekMongo
switched to db WeekMongo
> var mapf = function(){  emit(this.state, this.pop)  }
> var reducef = function(keySt, valPop){  return Array.sum(valPop);  }
> db.zips.mapReduce( mapf, reducef, { out: "PopulationInState" } )
{
        "result" : "PopulationInState",
        "timeMillis" : 5912,
        "counts" : {
                "input" : 29353,
                "emit" : 29353,
                "reduce" : 346,
                "output" : 51
        },
        "ok" : 1,
}
> db.PopulationInState.find()
{ "_id" : "AK", "value" : 544698 }
{ "_id" : "AL", "value" : 4040587 }
{ "_id" : "AR", "value" : 2350725 }
{ "_id" : "AZ", "value" : 3665228 }
{ "_id" : "CA", "value" : 29754890 }
{ "_id" : "CO", "value" : 3293755 }
{ "_id" : "CT", "value" : 3287116 }
{ "_id" : "DC", "value" : 606900 }
{ "_id" : "DE", "value" : 666168 }
{ "_id" : "FL", "value" : 12686644 }
{ "_id" : "GA", "value" : 6478216 }
{ "_id" : "HI", "value" : 1108229 }
{ "_id" : "IA", "value" : 2776420 }
{ "_id" : "ID", "value" : 1006749 }
{ "_id" : "IL", "value" : 11427576 }
{ "_id" : "IN", "value" : 5544136 }
{ "_id" : "KS", "value" : 2475285 }
{ "_id" : "KY", "value" : 3675484 }
{ "_id" : "LA", "value" : 4217595 }
{ "_id" : "MA", "value" : 6016425 }
Type "it" for more
> it
{ "_id" : "MD", "value" : 4781379 }
{ "_id" : "ME", "value" : 1226648 }
{ "_id" : "MI", "value" : 9295297 }
{ "_id" : "MN", "value" : 4372982 }
{ "_id" : "MO", "value" : 5110648 }
{ "_id" : "MS", "value" : 2573216 }
{ "_id" : "MT", "value" : 798948 }
{ "_id" : "NC", "value" : 6628637 }
{ "_id" : "ND", "value" : 638272 }
{ "_id" : "NE", "value" : 1578139 }
{ "_id" : "NH", "value" : 1109252 }
{ "_id" : "NJ", "value" : 7730188 }
{ "_id" : "NM", "value" : 1515069 }
{ "_id" : "NV", "value" : 1201833 }
{ "_id" : "NY", "value" : 17990402 }
{ "_id" : "OH", "value" : 10846517 }
{ "_id" : "OK", "value" : 3145585 }
{ "_id" : "OR", "value" : 2842321 }
{ "_id" : "PA", "value" : 11881643 }
{ "_id" : "RI", "value" : 1003218 }
Type "it" for more
> it
{ "_id" : "SC", "value" : 3486703 }
{ "_id" : "SD", "value" : 695397 }
{ "_id" : "TN", "value" : 4876457 }
{ "_id" : "TX", "value" : 16984601 }
{ "_id" : "UT", "value" : 1722850 }
{ "_id" : "VA", "value" : 6181479 }
{ "_id" : "VT", "value" : 562758 }
{ "_id" : "WA", "value" : 4866692 }
{ "_id" : "WI", "value" : 4891769 }
{ "_id" : "WV", "value" : 1793146 }
{ "_id" : "WY", "value" : 453528 }
> it
no cursor
>
