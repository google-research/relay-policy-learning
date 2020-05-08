# Relay Policy Learning Environments

This is a set of environments and associated data for use with MuJoCo in a kitchen simulator.
The code instantiates a kitchen environment and parses associated demonstrations. 

## Getting Started (User)

1. Clone the repository
```
$ git clone https://github.com/google-research/relay-policy-learning
```

2. Use the environments in your code (After including in the PYTHONPATH)
```
#!/usr/bin/env python3

import adept_envs
import gym

env = gym.make('kitchen_relax-v1')
```

3. To use the demos, first clone the puppet VR repository and add PATH/TO/puppet/vive/source to the PYTHONPATH

```
$ git clone https://github.com/vikashplus/puppet
```

4. Use parse_demos to parse the data into pkl format. Unzip the kitchen_demos_multitask.zip and then run
```
$  MJPL python adept_envs/utils/parse_demos.py --env kitchen_relax-v1 --demo_dir <PATH TO DEMOS DIRECTORY>  --view playback --skip 40 --render offscreen                    
```

This is not an officially supported Google product
