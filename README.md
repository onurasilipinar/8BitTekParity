# 8BitTekParity
Library IEEE;
Use IEEE.std.logic_1164.all;


Entity tParity is
 Port( adata: in std_logic_vector (6 downto 0);
  bdata:out std_logic_vector (7 downto 0));
  end Entity;


Architecture Behv of tParity is 
signal temp: std_logic:='0' ;

Begin
  temp <= adata(0) xor adata(1) xor adata(2) xor adata(3) xor adata(4) xor adata(5) xor adata(6) ;
  bdata <= adata & not temp ; 

end Behv;
