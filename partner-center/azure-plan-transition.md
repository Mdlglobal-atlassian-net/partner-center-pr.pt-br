---
title: Migrar clientes das ofertas atuais do Azure para o plano do Azure
ms.topic: article
ms.date: 05/04/2020
ms.service: partner-dashboard
ms.subservice: partnercenter-csp
description: Saiba como os parceiros CSP podem usar o Partner Center para migrar os clientes das ofertas do Azure no CSP existentes para os serviços do Azure no plano do Azure.
author: LauraBrenner
ms.author: labrenne
Keywords: ''
robots: ''
ms.localizationpriority: high
ms.custom: SEOMAY.20
ms.openlocfilehash: 05c28b852935dbce88d9f64c86b7c87fcbdc05cc
ms.sourcegitcommit: e9b627159745bcce53a8c2b1676f63f5249bba76
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2020
ms.locfileid: "82908328"
---
# <a name="transition-customers-to-azure-plan-from-existing-csp-azure-offers"></a>Fazer a transição de clientes para o plano do Azure de ofertas do Azure no CSP existentes

**Funções apropriadas**

- Agente administrativo
- Administrador de cobrança
- Administrador global
- Agente de suporte técnico
- Agente de vendas
- Administrador de gerenciamento de usuário

Provedores indiretos e parceiros de cobrança diretos podem fazer a transição para a nova experiência de comércio disponível no Programa CSP (Provedor de Serviços de Nuvem) para o Azure. (Revendedores indiretos precisarão trabalhar por meio dos respectivos provedores indiretos.) Os clientes terão uma maneira simplificada de comprar serviços de nuvem, seja de parceiros, de vendedores da Microsoft ou diretamente na Web.

A funcionalidade de transição é destinada apenas a clientes que estão fazendo a transição para a nova experiência de comércio para o Azure e que assinaram o Contrato de Cliente da Microsoft e não para outras ofertas do CSP, como o Office 365 ou o Dynamics 365.

## <a name="transition-existing-csp-offers-to-an-azure-plan"></a>Fazer a transição de ofertas do CSP existentes para um plano do Azure

Você pode fazer a transição de um cliente de suas ofertas do CSP do Azure existentes para os serviços do Azure no âmbito do plano do Azure na nova experiência de comércio no programa CSP de dentro do Partner Center. Para fazer isso, o parceiro e o cliente precisam ter uma relação de revendedor estabelecida por meio do Partner Center, e o cliente deve ter assinado o Contrato de Cliente da Microsoft.

### <a name="select-transition-to-azure-plan"></a>Selecione fazer a transição para o plano do Azure

1. Selecione o plano do Azure para o seu cliente.

2. Selecione **Fazer a transição de cobrança para o plano do Azure**.

![transição](images/azure/transition1.png)

3. Selecionar **Continuar**

![transição](images/azure/transition2.png)

Seu cliente será transferido para o plano do Azure.

**O fluxo de trabalho de transição automatiza as etapas de pré-requisito**:

- Compra de plano(s) do Azure
- Um plano por cliente em cenários de CSP direto  
- Um plano por revendedor  

Por exemplo, um parceiro comprou duas ofertas do Microsoft Azure e incluiu duas POR distintas na compra. Nesse caso, o fluxo de trabalho de transição comprará dois planos do Azure (um por revendedor) e mapeará as respectivas assinaturas do Azure nos planos do Azure automaticamente.  

**Como mapear a assinatura do Azure para o plano do Azure**

Após a compra do plano do Azure, nosso sistema mapeará as assinaturas do Azure existentes para os planos do Azure. O progresso pode ser exibido no portal do Azure, bem como no Partner Center. 

4. Volte para a página de **Assinaturas** do Partner Center do cliente a fim de atualizar o limite de orçamento usando a moeda local do cliente. 

![Transição](images/azure/transition3.png)

>[!NOTE]
>O orçamento definido no Partner Center não é transportado para o portal do Azure. Você também deve definir o orçamento e o alerta no portal do Azure.

Ao passar para o plano do Azure, não será mais possível comprar assinaturas do Azure para esse cliente. Você cria as assinaturas no âmbito do plano do Azure, no portal do Azure.

>[!NOTE]
> Todas as assinaturas do Azure adquiridas por meio do RBAC no plano do Azure terão preços na moeda local e serão cobradas nessa mesma moeda. As taxas de câmbio não serão usadas.

### <a name="track-your-transition-details"></a>Acompanhar os detalhes da transição

Siga o progresso da transição no portal do Azure, bem como no Partner Center.

![Mostrar detalhes](images/azure/details1.png)

**Impacto de cobrança para os parceiros**

Se você fizer a transição de um cliente de uma oferta do CSP do Azure existente, você terá os seguintes impactos de cobrança:

- Você será cobrado em sua fatura do CSP existente por todo o uso, até o ponto de saída da assinatura original do CSP do Azure.

- Se você tiver direitos de acesso de administrador à assinatura CSP existente, você continuará a ter tal acesso quando essa assinatura for migrada.

Para fazer a transição de Contratos Corporativos diretos para o CSP e o Servidor e os Registros de nuvem para os Serviços do Azure, leia [Obter a propriedade de cobrança das assinaturas do Azure para o Contrato de Parceiro da Microsoft](https://docs.microsoft.com/azure/billing/mpa-request-ownership)

**Log de auditoria**:

Para reconciliar a cobrança, veja seu histórico de assinaturas do “Microsoft Azure” (0145P) na página **Assinaturas**. 

A assinatura do “Microsoft Azure” (0145P) é composta por duas partes:
1. Assinatura do Commerce 
2. Assinatura do Azure (direito)

Quando a transição for concluída, a assinatura do Azure será movida no novo plano do Azure e a assinatura do Commerce será suspensa para que nenhum uso adicional seja relatado.  

>[Observação]\: Quando a assinatura do Microsoft Azure (0145P) é adquirida no CSP, tanto a assinatura do Commerce quanto a assinatura do Azure (direito) têm o mesmo valor. Somente no caso de alterações ou transferências na propriedade de cobrança é que os valores diferem. 

**Problemas de transição**

Não prevemos nenhum problema durante as transições. Caso ocorra alguma, nós o atualizaremos ao longo do próprio fluxo de trabalho de transição. Não deverá haver distúrbios para o uso do Azure.  

## <a name="next-steps"></a>Próximas etapas

- [Gerenciar assinaturas e recursos no âmbito do plano do Azure](azure-plan-manage.md)

- [Crédito ganho pelo parceiro – visão geral](partner-earned-credit.md)



