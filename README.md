# 🌐 Guia Completo Microsoft Azure – Experiência e Laboratórios

Este repositório documenta minha experiência e aprendizado com **Microsoft Azure**, abordando conceitos, serviços, boas práticas, governança, segurança, alta disponibilidade, escalabilidade e aplicação prática. Serve como material de estudo, referência e documentação para laboratórios e preparação para o exame **AZ-900 – Microsoft Azure Fundamentals**.

---

## 💡 1. Introdução ao Azure

O **Microsoft Azure** é uma plataforma de **computação em nuvem** que permite criar, gerenciar e hospedar aplicativos e serviços sem depender de infraestrutura física própria.  
Benefícios principais:

- **Escalabilidade:** Ajuste automático de recursos conforme demanda.  
- **Alta disponibilidade:** Garantia de funcionamento contínuo, minimizando downtime.  
- **Confiabilidade:** Redundância, replicação de dados e backup automático.  
- **Segurança:** Criptografia avançada, autenticação e monitoramento.  
- **Eficiência de custos:** Modelo pay-as-you-go (paga apenas pelo que usar).  
- **Flexibilidade:** Suporta **IaaS, PaaS e SaaS**, além de integração com múltiplas plataformas.

---

## ☁️ 2. Modelos de Nuvem

| Tipo | Descrição | Vantagens | Desvantagens | Exemplos |
|------|-----------|-----------|--------------|----------|
| Pública | Recursos compartilhados gerenciados pelo provedor | Escalabilidade, baixo custo inicial | Menor controle | Azure, AWS, Google Cloud |
| Privada | Infraestrutura exclusiva de uma organização | Maior segurança e controle | Alto custo, pouca flexibilidade | Azure Stack, datacenter próprio |
| Híbrida | Combinação de pública e privada | Flexibilidade e segurança | Complexidade maior | Azure Arc, Azure Hybrid Benefit |

### Modelo de Consumo
- **Pay-as-you-go:** Paga-se apenas pelo que for usado.  
- **CapEx vs OpEx:** Reduz investimento inicial (CapEx) com custos distribuídos e flexíveis (OpEx).

---

## 🖥️ 3. Modelos de Serviço em Nuvem

| Modelo | O que é | Controle do Cliente | Gerenciamento pelo Provedor | Exemplos Azure |
|--------|---------|------------------|----------------------------|----------------|
| **IaaS** | Infraestrutura como serviço | Alto (SO, apps, dados) | Hardware, data center | Virtual Machines, Virtual Networks |
| **PaaS** | Plataforma como serviço | Médio (apps e dados) | Infraestrutura e plataforma | Azure App Service, Azure SQL Database |
| **SaaS** | Software como serviço | Baixo (uso do software) | Tudo (infra + software) | Microsoft 365, Teams, Dynamics 365 |

> **Diagrama simplificado de responsabilidade:**
>
> ```
> IaaS  -> Cliente: SO, apps, dados | Provedor: infra, hardware
> PaaS  -> Cliente: apps e dados    | Provedor: infra + plataforma
> SaaS  -> Cliente: usa o software  | Provedor: tudo
> ```

---

## 🔧 4. Principais Serviços do Azure

### 4.1 Computação
- **Virtual Machines (VMs):** Servidores virtuais sob demanda.  
- **Azure App Service:** Hospedagem de apps web e APIs.  
- **Azure Functions:** Funções serverless executadas sob demanda.  
- **Azure Kubernetes Service (AKS):** Orquestração de contêineres.

### 4.2 Armazenamento
- **Blob Storage:** Armazenamento de arquivos não estruturados.  
- **File Storage:** Compartilhamento de arquivos.  
- **Queue Storage:** Fila para mensagens entre apps.  
- **Table Storage:** Banco NoSQL simples.

### 4.3 Banco de Dados
- **Azure SQL Database:** Banco relacional gerenciado.  
- **Cosmos DB:** Banco NoSQL globalmente distribuído.  
- **Azure Database for PostgreSQL/MySQL/MariaDB:** Bancos gerenciados com alta disponibilidade.  
- **Azure Cache for Redis:** Cache para acelerar aplicações.

### 4.4 Rede
- **Virtual Network (VNet):** Rede privada em nuvem.  
- **Load Balancer:** Distribuição de tráfego.  
- **Application Gateway:** Balanceamento HTTP/HTTPS e firewall.  
- **VPN Gateway:** Conexão segura com redes locais.  
- **Azure Front Door:** Distribuição global e aceleração de apps.

### 4.5 Segurança
- **Azure Active Directory (AAD):** Gerenciamento de identidade e autenticação.  
- **Azure Key Vault:** Armazenamento seguro de segredos e chaves.  
- **Azure Security Center / Defender:** Monitoramento e proteção de recursos.  
- **Role-Based Access Control (RBAC):** Controle de permissões granular.

### 4.6 Inteligência Artificial e Machine Learning
- **Cognitive Services:** APIs de visão, fala, linguagem e decisão.  
- **Azure Machine Learning:** Criação e treino de modelos de IA.  
- **Bot Service:** Desenvolvimento de chatbots inteligentes.

### 4.7 Análise e Big Data
- **Azure Synapse Analytics:** Integração de dados e data warehouse.  
- **Azure Data Lake Storage:** Armazenamento massivo de dados.  
- **Azure Databricks:** Processamento em larga escala de big data.

### 4.8 DevOps e Monitoramento
- **Azure DevOps:** CI/CD, controle de versão e gestão de projetos.  
- **Azure Monitor:** Monitoramento de aplicações e infraestrutura.  
- **Log Analytics:** Análise de logs centralizada.  
- **Application Insights:** Monitoramento de performance de apps.

### 4.9 Integração e Automação
- **Logic Apps:** Automação de fluxos de trabalho.  
- **Event Grid:** Distribuição de eventos em larga escala.  
- **Service Bus:** Comunicação entre aplicativos e microserviços.

---

## ⚡ 5. Alta Disponibilidade e Recuperação

- **Zonas de Disponibilidade:** Redundância física e geográfica.  
- **Backup e Restore:** Proteção de dados críticos.  
- **Azure Site Recovery:** Plano de Disaster Recovery automatizado.  

> **Exemplo de arquitetura de alta disponibilidade em ASCII:**
>
> ```
> Região 1: VM1 --+       
>                  +--> Load Balancer --> Usuários
> Região 2: VM2 --+
> ```

---

## 🛠️ 6. Monitoramento e Governança

- **Azure Policy:** Define regras de conformidade.  
- **Cost Management:** Monitoramento e otimização de custos.  
- **Tagging:** Organização de recursos por projeto, departamento ou custo.  
- **Blueprints:** Modelos de arquitetura para implementação consistente.  

---

## 📊 7. Boas Práticas

1. Planejar arquitetura com **regiões e zonas de disponibilidade**.  
2. Aplicar **RBAC** para controle de acesso seguro.  
3. Usar **tags** para facilitar gerenciamento e relatórios.  
4. Automatizar deploys com **ARM Templates** ou **Bicep**.  
5. Monitorar recursos com **Azure Monitor** e **Application Insights**.  
6. Configurar **backup e disaster recovery** desde o início.  
7. Avaliar o **modelo de custo** e otimizar recursos continuamente.

---

## 🧪 8. Laboratórios e Experimentos Práticos

Exemplos de exercícios práticos:

- Criar **Azure SQL Database**.  
- Configurar **firewall e regras de acesso**.  
- Monitorar performance com **Azure Monitor**.  
- Implementar **backup e restore automático**.  
- Testar escalabilidade e alta disponibilidade usando **Zonas de Disponibilidade**.  

---

## 📚 9. Recursos Úteis

- [Documentação Oficial Azure](https://learn.microsoft.com/azure/)  
- [Microsoft Learn - AZ-900](https://learn.microsoft.com/training/certifications/azure-fundamentals/)  
- [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/)  
- [Artigos e Tutoriais DIO](https://web.dio.me/articles)

---

✅ **Conclusão**

O Azure oferece uma ampla gama de serviços para computação, armazenamento, rede, banco de dados, segurança e análise. Conhecer esses conceitos permite planejar, implementar e gerenciar soluções modernas, seguras e escaláveis na nuvem. Este repositório serve como registro de aprendizado, referência prática e preparação para exames como **AZ-900**.
