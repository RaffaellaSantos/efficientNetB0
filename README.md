Configurações para rodar no conda

- Entrar no servidor

```bash
ssh -L port:localhost:port user@ip-do-servidor
```


- Inicializar Conda

```bash
/opt/conda/bin/conda --version
source /opt/conda/bin/activate
```

- Criar ambiente
```bash
conda env list #Verificar se o ambiente existe
conda create --name effiicient_env
```

- Ativar ambiente

```bash
conda env list #Verificar o nome do ambiente
conda activate efficient_env
```

- Testar GPU

```bash
python -c "import torch; print(f'PyTorch Version: {torch.__version__}'); print(f'CUDA Available: {torch.cuda.is_available()}'); print(f'Device Name: {torch.cuda.get_device_name(0) if torch.cuda.is_available() else \"N/A\"}')"
```

- Instalar dependências

```bash
conda install conda-forge::'lib'
```

- Abrir jupyter

```bash
jupyter lab
```