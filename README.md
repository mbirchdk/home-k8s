# home-k8s

# Get started (from raspberry to rancher UI)
1. Installer OS på SD-kort
    1. Hent raspberry imager til maskine med SD-kort læser (https://www.raspberrypi.org/software/)
    1. Vælg Ubuntu som OS
    1. Vælg SD-kortet
    1. Write
1. Configurer netværks-indstillinger.
    1. Kør `ipconfig` og find gateway ip
    2. Find `network-config` fil her i repositoriet
    3. Indsæt wifi navn og password samt den gateway du fandt fra forrige trin
    4. Kopier indholdet af den fil du har tilpasset, over i `network-config` på SD-kortet
1. Indsæt SD-kort i RaspberryPie

1. Log ind på servere med password `ubuntu` og bruger `ubuntu`
1. log ind på alle servere og installer:
    1. Kubectl
        1. sudo apt update
        1. sudo apt upgrade 
        1. sudo snap install kubectl --classic
        1. Reboot 
    4. docker (med https://www.docker.com/blog/getting-started-with-docker-for-arm-on-linux/ ) 
        1. ubuntu-bruger skal tilføjes til docker `usermod -aG docker <user_name>` ( https://rancher.com/docs/rke/latest/en/os/ )
    6. rke
        1. Find download link ved at gå ind på en release (f.eks. https://github.com/rancher/rke/releases/tag/v1.2.8 )
        1. Højre klik på den version der passer til maskinen, og kopier link
        1. wget i terminal på det downloadede
        1. Følg https://computingforgeeks.com/install-kubernetes-production-cluster-using-rancher-rke/
1. kør *ssh-keygen* for at lave et pub/private pair
l. Indsæt public key under /.ssh/authorized-keys)
l. kør rke -up
l. installér helm på master (https://helm.sh/docs/intro/install/)
l. installér rancher ui  (https://rancher.com/docs/rancher/v2.x/en/installation/install-rancher-on-k8s/)
1. Kør kommando `cp kube_config_cluster.yml ~/.kube/config`
