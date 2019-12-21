# gpu-test
    kubectl label nodes worker19.bluedata  accelerator=nvidia-tesla-m6 
    kubectl taint nodes worker19.bluedata nvidia.com/gpu=true:NoSchedule-

# describe pod Output
    Events:
      Type     Reason            Age                From               Message
      ----     ------            ----               ----               -------
      Warning  FailedScheduling  53s (x2 over 53s)  default-scheduler  0/3 nodes are available: 2 Insufficient nvidia.com/gpu, 3 node(s) didn't match node selector.
      Warning  FailedScheduling  24s (x2 over 24s)  default-scheduler  0/3 nodes are available: 1 node(s) had taints that the pod didn't tolerate, 2 Insufficient nvidia.com/gpu, 2 node(s) didn't match node selector.
      Normal   Scheduled         3s                 default-scheduler  Successfully assigned default/gpu-pod to worker19.bluedata

