# reproducibility-tutorial
Test Repository as part of CyVerse FOSS2020 training

Instructions and context for this repository, process and related data is at https://learning.cyverse.org/projects/cyverse-cyverse-reproducbility-tutorial/en/latest/index.html
    1  pwd
    2  ls
    3  cd /scratch
    4  df -h
## Clone github repo
    5  git clone https://github.com/maliaca/reproducibility-tutorial.git
    6  ls
    7  clear

## Install conda
    8  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    9  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
   10  ln -s /opt/conda/pkgs/*/bin/* /bin
   11  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   12  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   13  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   14  /opt/conda/bin/pip install bash_kernel
   15  /opt/conda/bin/pip install ipykernel
   16  /opt/conda/bin/python3 -m bash_kernel.install
   17  clear
   18  /opt/conda/bin/conda search htseq
   19  /opt/conda/bin/conda search -c bioconda htseq
   20  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   21  /opt/conda/bin/conda search -c bioconda snakemake
   22  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   23  ln -s /opt/conda/bin/* /bin
   24  ln -s /opt/conda/lib/* /usr/lib
   25  snakemake --version
   26  sudo apt-get update
   27  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   28  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   29  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   30  sudo apt-get update
   31  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   32  docker run hello-world
   33  ls
   34  cd /scratch/reproducibility-tutorial/
   35  history >>README.md
