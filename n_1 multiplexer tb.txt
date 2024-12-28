module muxn_1TB();
parameter n=2;
parameter m=2**n;
reg [m-1:0]a;
reg [n-1 :0]s;
wire y;
muxn_1 k(a,s,y);
integer i;
initial
begin
for(i=0;i<64;i=i+1)
begin
{a[3],a[2],a[1],a[0],s[1],s[0]}=i;
#10;
end
end
endmodule