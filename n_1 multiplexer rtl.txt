module muxn_1(a,s,y);
parameter n=2;
input [n-1 :0]s;
parameter m=2**n;
input [m-1:0]a;
output reg y;
integer i;
always@(*)
for(i=0;i<m;i=i+1)
if(s==i)
begin
y=a[s];
end
endmodule
