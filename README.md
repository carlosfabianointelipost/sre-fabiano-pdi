# sre-fabiano-pdi
Repositório para o PDI 2024
Milestone 01 - Subir VPC e Cluster

Criar VPC

- 2 subnets (pública e privada)
- nat gateway
- internet gateway

Criação de cluster EKS com Spotinst na VPC criada

- v1.31
- 2 node groups 
-- 1 100% spot
-- 1 50% spot

Milestone 02 - ArgoCD, GitOps e Networking

- Criar repositório github (sre-fabiano-pdi)
- Instalar ArgoCD 
-- Pattern Apps of Apps
-- Conectado ao repositório
-- Plugin Vault
-- AWS Load Balancer Controller
-- Criar certificado (argocd.pdi.intelipost.com.br)
-- Criar ingress ALB externo (acesso argocd)

Milestone 03 - Subir aplicação no cluster comunicando com recursos AWS

- Criar Bucket S3 privado
-- Adicionar arquivo .txt com qualquer conteúdo
- Criar aplicação para baixar os arquivos do bucket e printar o conteúdo.
-- Iniciar aplicação de 10 em 10 minutos
- Criar aplicação que monta secret do aws secrets manager e joga o conteúdo para o log do pod.

Milestone 04 - Permissionamento


- Criar 2 usuários AWS
-- Role full-access
--- acesso total
-- Role dev
--- acesso leitura

- Criar 2 roles de acesso ao cluster EKS
-- Role full-access
--- Acesso a todos os namespaces
--- permissão escrita.
-- Role dev-acess
--- Acesso a todos os namespaces
--- permissão leitura

- Simular acesso com os dois usuários
-- S3
-- EKS
-- Secrets Manager
- Capturar nos logs de auditoria e os eventos dos acessos.

