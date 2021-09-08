--Codigo creado para codificar el resultado de la suma de 4 a 8 bits  

LIBRARY IEEE;
USE ieee.std_logic_1164.all;
-------------------------------------------------
ENTITY bcd_2 IS
 PORT(  resa: IN  STD_LOGIC_VECTOR(3 DOWNTO 0);--Resultado de la suma de 4 bits
        Cout : IN STD_LOGIC;--Carry final de la suma de 4 bits
		  resat: OUT STD_LOGIC_VECTOR(7 DOWNTO 0));--Resultado de la suma codificada de 4 a 8 bits
END ENTITY	bcd_2;
-------------------------------------------------
ARCHITECTURE bin_to_bcd OF bcd_2 IS 
BEGIN 

		resat(0) <= resa(0);--A los primeros 4 bits se les asigna el valor de cada posicion del resa
		resat(1) <= resa(1);
		resat(2) <= resa(2);
		resat(3) <= resa(3);
		resat(4) <= Cout;--Se coloca tambien el Cout o el carry final
		resat(5) <= '0';--Las siguientes tres posiciones se le asignan ceros
		resat(6) <= '0';
		resat(7) <= '0';
		
END ARCHITECTURE bin_to_bcd; 
