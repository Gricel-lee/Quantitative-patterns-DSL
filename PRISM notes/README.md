# Reward at most/ at least / equals to
Example:
```
module r1
x:bool init false;

[] x=false -> 1:(x'=true);

endmodule

rewards "channel_quality"
true : Y;
endrewards
```
Example of PRCTL Translation:

If Y=1, ```R>=10 [ F x ]``` = False

If Y=11, ```R>=10 [ F x ]``` = True
