
Updating the Expert Policy

1. Verify ICRL setup with updated constraints:
   PYTHONPATH=. python interface/train_icrl.py \
   config/mujoco_WGW-discrete-v0/train_ICRL_discrete_WGW-v0-setting1.yaml -n 5 -s 0
2. Train the new expert policy
   from inside interface/
   cd ~/Desktop/ICRL_benchmarks_Original/interface
   python train_policy.py ../config/mujoco_WGW-discrete-v0/train_policy_discrete_WGW-v0-setting1.yaml -n 1 -s 0

3.Generating New Expert Data
   Run from inside the interface/ folder
   cd ~/Desktop/ICRL_benchmarks_Original/interface
   PYTHONPATH=.. python generate_data_for_constraint_inference.py \
    -mn train_policy_discrete_WGW-v0-setting1-Oct-29-2025-12:53-seed_0 \
    -tn PI-Lag-WallGrid-Discrete \
    -ct constraint \
    -rn 0


