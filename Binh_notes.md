# Binh's notes


- ROCm 6.4.2: https://rocm.docs.amd.com/projects/radeon/en/latest/docs/install/native_linux/install-radeon.html
- Python 3.12
```
conda create -n forge python=3.12
conda activate forge
```
- torch
```
pip install --upgrade pip wheel
wget https://repo.radeon.com/rocm/manylinux/rocm-rel-6.4.2/torch-2.6.0%2Brocm6.4.2.git76481f7c-cp312-cp312-linux_x86_64.whl
wget https://repo.radeon.com/rocm/manylinux/rocm-rel-6.4.2/torchvision-0.21.0%2Brocm6.4.2.git4040d51f-cp312-cp312-linux_x86_64.whl
wget https://repo.radeon.com/rocm/manylinux/rocm-rel-6.4.2/pytorch_triton_rocm-3.2.0%2Brocm6.4.2.git7e948ebf-cp312-cp312-linux_x86_64.whl
wget https://repo.radeon.com/rocm/manylinux/rocm-rel-6.4.2/torchaudio-2.6.0%2Brocm6.4.2.gitd8831425-cp312-cp312-linux_x86_64.whl
pip uninstall torch torchvision pytorch-triton-rocm
pip install torch-2.6.0+rocm6.4.2.git76481f7c-cp312-cp312-linux_x86_64.whl torchvision-0.21.0+rocm6.4.2.git4040d51f-cp312-cp312-linux_x86_64.whl torchaudio-2.6.0+rocm6.4.2.gitd8831425-cp312-cp312-linux_x86_64.whl pytorch_triton_rocm-3.2.0+rocm6.4.2.git7e948ebf-cp312-cp312-linux_x86_64.whl
```
- pytorch3d:
```
pip install "git+https://github.com/facebookresearch/pytorch3d.git@stable"
```
- Check:
```
python -c 'import torch; print(torch.cuda.is_available())'
```
- Clean up:
```
rm -f *torch*.whl
```
-Others
```
pip install -r requirements.txt
```
