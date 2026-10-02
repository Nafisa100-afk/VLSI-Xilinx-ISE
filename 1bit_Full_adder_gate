library IEEE;

use IEEE.STD_LOGIC_1164.ALL;



entity Full_adder_gate is

    Port (

        A    : in STD_LOGIC;

        B    : in STD_LOGIC;

        Cin  : in STD_LOGIC;

        SUM  : out STD_LOGIC;

        COUT : out STD_LOGIC

    );

end Full_adder_gate;



architecture Structural of Full_adder_gate is



    component Half_adder_gate

        Port (

            A     : in STD_LOGIC;

            B     : in STD_LOGIC;

            SUM   : out STD_LOGIC;

            CARRY : out STD_LOGIC

        );

    end component;



    component OR_gate

        Port (

            A : in STD_LOGIC;

            B : in STD_LOGIC;

            Y : out STD_LOGIC

        );

    end component;



    signal S1 : STD_LOGIC;

    signal C1 : STD_LOGIC;

    signal C2 : STD_LOGIC;



begin



    HA1 : Half_adder_gate

        port map (

            A     => A,

            B     => B,

            SUM   => S1,

            CARRY => C1

        );



    HA2 : Half_adder_gate

        port map (

            A     => S1,

            B     => Cin,

            SUM   => SUM,

            CARRY => C2

        );



    OR1 : OR_gate

        port map (

            A => C1,

            B => C2,

            Y => COUT

        );



end Structural;
