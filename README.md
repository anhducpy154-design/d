firstly, we start with generating Pulse by 
% md.type = 'RRC';
% md.Tp   = 0.5e-9;
% md.beta = 0.6;
% tau = (0 : 4.6414e-12 : (28747-1)*4.6414e-12)';
% tau_0 = 1e-8;
% [s, ds, dds] = generatePulse(md, tau_0, tau, 0);
After that, we 
Ts = 4.641400000000000e-12;
and 
[Ruu, tau_axis] = generateRuu(s, Ts);
Lastly, open IR_map
Z = IR_map;
[tau_detect, gain_detect, h_mean, h_rvm, Ruu_short] = RVM_Multipath_IV_A2(Z, Ruu, 80, 6);
the final answer should be ran.
