; DESIGN "INVERTER"
; DATE "Tue Oct 30 01:19:13 2018"
; VENDOR "Mentor Graphics Corp."
; PROGRAM "Calibre xRC v2014.1_17.12"
; CIRCUIT TEMPERATURE 27C
; NOMINAL TEMPERATURE 27C
;


mgc_rve_device_template "NM" "D" "G" "S" "B"
mgc_rve_device_template "N33" "D" "G" "S" "B"
mgc_rve_device_template "C1" "D" "G" "S" "B"
mgc_rve_device_template "C2" "D" "G" "S" "B"
mgc_rve_device_template "PM" "D" "G" "S" "B"
mgc_rve_device_template "P33" "D" "G" "S" "B"
mgc_rve_device_template "PNP" "c" "b" "e"
mgc_rve_device_template "PDIO18" "pos" "neg"
mgc_rve_device_template "PDIO33" "pos" "neg"
mgc_rve_device_template "NDIO18" "pos" "neg"
mgc_rve_device_template "NDIO33" "pos" "neg"
mgc_rve_device_template "NWDIO" "pos" "neg"
mgc_rve_device_template "RNWAA" "pos" "neg"
mgc_rve_device_template "RNWSTI" "pos" "neg"
mgc_rve_device_template "RPDIF" "pos" "neg"
mgc_rve_device_template "RPDIFSAB" "pos" "neg"
mgc_rve_device_template "RNDIF" "pos" "neg"
mgc_rve_device_template "RNDIFSAB" "pos" "neg"
mgc_rve_device_template "RPPO" "pos" "neg"
mgc_rve_device_template "RPPOSAB" "pos" "neg"
mgc_rve_device_template "RNPO" "pos" "neg"
mgc_rve_device_template "RNPOSAB" "pos" "neg"
mgc_rve_device_template "v" "P" "M"
mgc_rve_device_template "f" "P" "M"
mgc_rve_parasitic_template "c" "r" "l" "k" "h"

mgc_rve_cell_start "inverter" "VIN" "GND" "VDD" "VOUT"
mr_pi "NM" "MNM0" '( "MNM0_d" "MNM0_g" "MNM0_s" "MNM0_b") '( ("l" 1.8e-07) ("w" 2.2e-07) ("lpe" 3) ) '(-10.779 4.641)
mr_pi "PM" "MPM0" '( "MPM0_d" "MPM0_g" "MPM0_s" "MPM0_b") '( ("l" 1.8e-07) ("w" 2.2e-07) ("lpe" 3) ) '(-10.779 6.012)

mr_ni "VIN" 79.8558 3.42577e-16 7.78003e-17 '( "MNM0_g" "MPM0_g" )
mr_pp 'c "ciVIN_19" '("c_6_p" "0") 0.0593895f
mr_pp 'c "ciVIN_20" '("VIN" "0") 0.0554625f
mr_pp 'c "ciVIN_21" '("c_16_p" "0") 0.011671f
mr_pp 'c "ciVIN_22" '("c_4_p" "0") 0.0573426f
mr_pp 'c "ciVIN_23" '("c_3_p" "0") 0.0362796f
mr_pp 'c "ciVIN_24" '("MPM0_g" "0") 0.0866032f
mr_pp 'c "ciVIN_25" '("MNM0_g" "0") 0.035829f
mr_pp 'r "rVIN_26" '("VIN_18" "c_6_p") 6.61346
mr_pp 'r "rVIN_27" '("VIN" "VIN_18") 6.5
mr_pp 'r "rVIN_28" '("VIN_11" "c_16_p") 3.37062
mr_pp 'r "rVIN_29" '("c_4_p" "c_16_p") 3.37062
mr_pp 'r "rVIN_30" '("c_3_p" "c_16_p") 0.875966
mr_pp 'r "rVIN_31" '("c_3_p" "c_6_p") 16.1853
mr_pp 'r "rVIN_32" '("MPM0_g" "VIN_11") 20.0327
mr_pp 'r "rVIN_33" '("MNM0_g" "c_4_p") 22.9071


mr_ni "GND" 14.1022 1.43159e-16 6.11543e-17 '( "MNM0_b" "MNM0_s" )
mr_pp 'c "ciGND_12" '("c_26_n" "0") 0.0240113f
mr_pp 'c "ciGND_13" '("c_21_n" "0") 0.046795f
mr_pp 'c "ciGND_14" '("MNM0_b" "0") 0.0723532f
mr_pp 'r "rGND_15" '("GND_13" "MNM0_s") 6.99568
mr_pp 'r "rGND_16" '("GND_12" "GND_13") 6.6
mr_pp 'r "rGND_17" '("c_26_n" "GND") 0.0220435
mr_pp 'r "rGND_18" '("c_21_n" "GND_12") 0.0576522
mr_pp 'r "rGND_19" '("GND_3" "c_26_n") 0.0435808
mr_pp 'r "rGND_20" '("GND_3" "c_21_n") 0.195
mr_pp 'r "rGND_21" '("MNM0_b" "GND") 0.188217


mr_ni "VDD" 17.1432 1.43108e-16 6.29739e-17 '( "MPM0_b" "MPM0_s" )
mr_pp 'c "ciVDD_12" '("c_38_n" "0") 0.0239164f
mr_pp 'c "ciVDD_13" '("VDD_9" "0") 0.046795f
mr_pp 'c "ciVDD_14" '("c_33_n" "0") 8.45598e-20
mr_pp 'c "ciVDD_15" '("MPM0_b" "0") 0.0723117f
mr_pp 'r "rVDD_16" '("c_38_n" "VDD") 0.0352696
mr_pp 'r "rVDD_17" '("VDD_9" "c_38_n") 0.0435808
mr_pp 'r "rVDD_18" '("c_37_n" "VDD_16") 0.0155325
mr_pp 'r "rVDD_19" '("c_37_n" "VDD_9") 0.195
mr_pp 'r "rVDD_20" '("VDD_6" "MPM0_s") 7.73675
mr_pp 'r "rVDD_21" '("c_33_n" "VDD_16") 0.0420522
mr_pp 'r "rVDD_22" '("c_33_n" "VDD_6") 8.9
mr_pp 'r "rVDD_23" '("MPM0_b" "VDD") 0.174991


mr_ni "VOUT" 30.7756 7.20398e-17 9.23356e-17 '( "MNM0_d" "MPM0_d" )
mr_pp 'c "ciVOUT_11" '("c_47_n" "0") 1.59724e-19
mr_pp 'c "ciVOUT_12" '("VOUT" "0") 0.07188f
mr_pp 'r "rVOUT_13" '("VOUT_13" "MPM0_d") 7.77785
mr_pp 'r "rVOUT_14" '("VOUT_12" "VOUT_13") 8.9
mr_pp 'r "rVOUT_15" '("VOUT_8" "MNM0_d") 7.03285
mr_pp 'r "rVOUT_16" '("c_47_n" "VOUT_8") 6.6
mr_pp 'r "rVOUT_17" '("VOUT_5" "c_48_n") 0.0114805
mr_pp 'r "rVOUT_18" '("VOUT_5" "c_47_n") 0.0461217
mr_pp 'r "rVOUT_19" '("VOUT" "c_48_n") 0.158374
mr_pp 'r "rVOUT_20" '("c_44_n" "VOUT_12") 0.0576522
mr_pp 'r "rVOUT_21" '("c_44_n" "VOUT") 0.19127

mr_pp 'c "cc_1" '("MNM0_g" "MNM0_b") 4.63762e-19
mr_pp 'c "cc_2" '("MNM0_g" "c_21_n") 0.00138045f
mr_pp 'c "cc_3" '("c_3_p" "c_21_n") 3.83704e-19
mr_pp 'c "cc_4" '("c_4_p" "c_21_n") 4.27658e-19
mr_pp 'c "cc_5" '("VIN" "c_21_n") 0.0184524f
mr_pp 'c "cc_6" '("c_6_p" "c_21_n") 2.237e-19
mr_pp 'c "cc_7" '("VIN" "c_26_n") 0.00157519f
mr_pp 'c "cc_8" '("MPM0_g" "MPM0_b") 4.63762e-19
mr_pp 'c "cc_9" '("MPM0_g" "c_33_n") 3.75821e-19
mr_pp 'c "cc_10" '("c_3_p" "c_33_n") 4.80043e-19
mr_pp 'c "cc_11" '("VIN" "c_33_n") 0.0196843f
mr_pp 'c "cc_12" '("c_6_p" "c_33_n") 2.53765e-19
mr_pp 'c "cc_13" '("MPM0_g" "c_37_n") 0.00129241f
mr_pp 'c "cc_14" '("VIN" "c_38_n") 0.00159777f
mr_pp 'c "cc_15" '("MPM0_g" "c_44_n") 0.00281961f
mr_pp 'c "cc_16" '("c_16_p" "VOUT") 0.00235421f
mr_pp 'c "cc_17" '("VIN" "VOUT") 0.0228417f
mr_pp 'c "cc_18" '("MNM0_g" "c_47_n") 3.75821e-19
mr_pp 'c "cc_19" '("c_4_p" "c_48_n") 0.00235421f
mr_pp 'c "cc_20" '("MNM0_b" "MPM0_b") 0.00631368f
mr_pp 'c "cc_21" '("c_21_n" "c_33_n") 0.00142807f
mr_pp 'c "cc_22" '("MNM0_b" "c_47_n") 0.0130879f
mr_pp 'c "cc_23" '("c_21_n" "c_47_n") 0.0153316f
mr_pp 'c "cc_24" '("c_21_n" "c_48_n") 0.00208619f
mr_pp 'c "cc_25" '("MPM0_b" "c_44_n") 0.013364f
mr_pp 'c "cc_26" '("c_33_n" "c_44_n") 0.0147293f
mr_pp 'c "cc_27" '("c_37_n" "c_44_n") 0.00299098f
mgc_rve_cell_end

