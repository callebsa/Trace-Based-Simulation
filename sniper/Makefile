all:	
	cd .. && make -j
	../run-sniper -n 8 -cgainestown -crob -gperf_model/dram/num_controllers=1 -gperf_model/l3_cache/shared_cores=8 -gperf_model/l2_cache/perfect=true -gperf_model/l3_cache/perfect=true -gperf_model/l1_icache/perfect=true  -gperf_model/dram/direct_access=true -ggeneral/enable_icache_modeling=false -gperf_model/branch_predictor/type=none -gperf_model/l1_dcache/perfect=true -gclock_skew_minimization/barrier/quantum=2147483647 -gperf_model/dtlb/size=0 -gperf_model/core/interval_timer/window_size=256 -gperf_model/core/rob_timer/rs_entries=256 -gperf_model/core/rob_timer/outstanding_loads=256 -gperf_model/core/rob_timer/outstanding_stores=256 -gperf_model/core/rob_timer/commit_width=4 -gperf_model/core/rob_timer/deptrace=true -gperf_model/core/rob_timer/store_to_load_forwarding=false -gperf_model/core/rob_timer/deptrace_microops=true -gperf_model/core/rob_timer/deptrace_start_active=true --insert-clear-stat-by-icount=7 --no-cache-warming --save-output -- ../test/fft-deptrace/FFT -p 8 -m 16
	rm -f sim.deptrace.0
	gunzip sim.deptrace.0.gz 
	head sim.deptrace.0 --line=20
