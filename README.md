For updating policy :
                 # PYTHONPATH=. python interface/train_icrl.py \config/mujoco_WGW-discrete-v0/train_ICRL_discrete_WGW-v0-setting1.yaml \-n 5 -s 0

                 Final: cd ~/Desktop/ICRL_benchmarks_Original/interface
python train_policy.py ../config/mujoco_WGW-discrete-v0/train_policy_discrete_WGW-v0-setting1.yaml -n 1 -s 0
or PYTHONPATH=. python interface/train_policy.py config/mujoco_WGW-discrete-v0/train_policy_discrete_WGW-v0-setting1.yaml -n 1 -s 0

and for generating new expert data: (run inisde interface) PYTHONPATH=.. python generate_data_for_constraint_inference.py \
  -mn (name of trained policy) train_policy_discrete_WGW-v0-setting1-Oct-29-2025-12:19-seed_0 \
  -tn PI-Lag-WallGrid-Discrete(task) \
  -ct constraint \
  -rn 0
  final: PYTHONPATH=. python generate_data_for_constraint_inference.py   -mn train_policy_discrete_WGW-v0-setting1-Oct-29-2025-12:53-seed_0   -tn PI-Lag-WallGrid-Discrete   -ct constraint   -rn 0

