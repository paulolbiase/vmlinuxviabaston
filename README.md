# 💻 Azure Lab – Criação de VM Linux com Bicep e Acesso via Bastion

## 🎯 Objetivo

Criar uma infraestrutura no Azure utilizando Bicep para provisionar:

- Rede Virtual (VNet)
- Sub-rede personalizada
- Grupo de Segurança de Rede (NSG)
- Interface de rede (NIC)
- Máquina virtual Linux (Ubuntu) com acesso via Bastion (sem IP público)

---

## 🧱 Infraestrutura Criada

| Recurso                  | Nome            | Região        |
|--------------------------|------------------|---------------|
| Resource Group           | `myResourceGroup`| East US  |
| Virtual Network (VNet)   | `myVnet`         | East US  |
| Subnet                  | `mySubnet`        | East US  |
| Network Security Group   | `myNsg`          | East US  |
| Interface de Rede (NIC)  | `myLinuxVM-nic`  | East US  |
| Máquina Virtual (VM)     | `myLinuxVM`      | East US  |
| Acesso via Bastion       | `Azure Bastion`  | East US  |

---

## ⚙️ Template Bicep

O arquivo `main.bicep` contém toda a definição da infraestrutura.

> **Parâmetros** utilizados:
- `adminUsername`: azureuser
- `adminPassword`: senha forte definida via CLI

---

## 🚀 Comandos Executados
az deployment group create \
  --resource-group myResourceGroup \
  --template-file main.bicep \
  --parameters adminPassword='definaseupasswordaqui'

 ## Prints
![image](https://github.com/user-attachments/assets/1389abcc-1a1a-4308-b51c-22d35a885164)
![image](https://github.com/user-attachments/assets/9c070c1c-b9de-4041-b904-39ba74e81261)
![image](https://github.com/user-attachments/assets/d2e63f57-1065-47fc-99b9-af8bd66b1e02)


