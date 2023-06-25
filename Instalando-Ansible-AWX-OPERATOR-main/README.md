<img src="https://github.com/smctighevcp/Packer/blob/main/packer-icon.svg" style="width:150px;height:150px;">

# Packer

## Introdução

Este repositório contém compilações de empacotador para vários sistemas operacionais usando o construtor vSphere-ISO. Estas são minhas configurações atualizadas usando HCL em vez de JSON após o lançamento do Packer 1.7.

  Existem compilações individuais que são referenciadas na minha série de blogs [Link](https://virtualizandoaju.academy/2022/07/13/criando-um-template-vmware-oracle-linux-com-packer-usando-hcl2/) e usar algumas técnicas mais antigas. Eles estão localizados nas pastas específicas do sistema operacional.

A pasta vm-templates contém uma configuração combinada que usa algumas técnicas mais recentes com várias melhorias, bem como uma melhor reutilização do código, facilitando a manutenção. Atualmente, possui uma configuração de modelo para Windows Server 2022 (Core & Desktop), Photon e RHEL.

## Available Builds
* Windows Server 2022 | Standard & Datacenter | GUI
* Windows Server 2019 | Standard & Datacenter | GUI
* Centos 8
* Oracle Linux 7.9 (usando http)
* Oracle Linux 8.8
* Oracle Linux 9.2

## Files
- `variables.pkr.hcl` - Arquivo de declaração de variável
- `'OS-Name'.pkr.hcl` - Construir arquivo em cada configuração específica do sistema operacional
- `build.pkr.hcl` - Arquivo de compilação combinado em nova configuração
- `'OS-Name'.pkrvar.hcl` - Arquivo de variáveis ​​definidas pelo usuário
- `packer-build-menu.ps1` - Menu interativo do PowerShell para criar seus modelos a partir da compilação combinada.
- `get-application-media.ps1` - Usado para criar um arquivo ZIP de mídia de instalação a ser instalado por meio do script package-installations.ps1` durante a compilação.

## Change Log

### 24/06/2023
* Atualização de todos os arquivos.
* ovf desabilitado para import no content library devido a inconsistências.
* Oracle Linux 7.9 adicionado.
* Oracle Linux 8.8 adicionado.
* Oracle Linux 9.2 adicionado.
* Arquivo README.md adicionado.

### xx/xx/202x

