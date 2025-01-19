
```Lua
local function FlipFlop(S,R,P,Q)
    Q = not(S and P)
    P = not(R and Q)
    return S,R,P,Q
end

local BoolToBinary = {
    [true] = "1";
    [false]= "0";
}

local function BoolsToBinary(S,R,P,Q)
    return BoolToBinary[S] .. BoolToBinary[R] .. BoolToBinary[P] .. BoolToBinary[Q]
end

local B = {false, true}

for _,x in ipairs(B) do
    for _,y in ipairs(B) do
        for _,z in ipairs(B) do
            for _,a in ipairs(B) do
                local S,R,P,Q = x,y,z,a
                print("INIT:", BoolsToBinary(S,R,P,Q))
                local S,R,P,Q = FlipFlop(S,R,P,Q)
                print(1, BoolsToBinary(S,R,P,Q))
                
                for i = 2,5 do
                    S,R,P,Q = FlipFlop(S,R,P,Q)
                    print(i, BoolsToBinary(S,R,P,Q))
                end
            end
        end
    end
end
```