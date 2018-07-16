# gym-duckietown-agent

Clone this repo:

    git clone https://github.com/duckietown/gym-duckietown-agent.git
    
Change into that directory

    cd gym-duckietown-agent
    
Start containers (make sure to always have the latest simulator). During the first start this will download the ~2GB `duckietown/gym-duckietown-server` container. This might take a while depending on your internet speed. Afterwards this will build the `gym-duckietown-agent` container, which also might take a few minuts the first time. Successive starts should be ignificantly faster.

    docker-compose up --build

This should give you a reward output like 
    
    gym-duckietown-agent_1   | sent action: 0 12416 172.20.0.3 0.3899666666984558,-0.6107861995697021
    gym-duckietown-agent_1   | sent action: 0 12416 172.20.0.3 -0.7719264626502991,-0.47576847672462463
    gym-duckietown-agent_1   | sent action: 0 12416 172.20.0.3 0.471004456281662,0.10089363902807236
    gym-duckietown-agent_1   | sent action: 0 12416 172.20.0.3 -0.20569732785224915,0.5168590545654297
    gym-duckietown-agent_1   | sent action: 0 12416 172.20.0.3 -0.9524251222610474,0.6271501779556274
    gym-duckietown-agent_1   | sent reset
    gym-duckietown-agent_1   | The average reward of 10 episodes was -64.5558. Best episode: 0.0, worst episode: -190.8287
    gym-duckietown-agent_gym-duckietown-agent_1 exited with code 0

(The important bit is the second last line here)

Now edit the file `agent.py`, run the command `docker-compose pull && docker-compose up` again and try to improve your score.

Good luck :)
