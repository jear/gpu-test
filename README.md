# gpu-test
    kubectl taint nodes worker19.bluedata nvidia.com/gpu=true:NoSchedule-
    kubectl label nodes worker19.bluedata  accelerator=nvidia-tesla-m6 
