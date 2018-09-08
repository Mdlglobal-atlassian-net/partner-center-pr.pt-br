---
title: Dimensionamento de VM do Microsoft Azure para uso máximo de reserva | Painel de parceiros
Description: Information on purchasing and managing Azure reservations
author: v-petand
keywords: azure, reservas, vm, gerenciar, uso, dimensionamento
ms.localizationpriority: medium
ms.openlocfilehash: bb7d022ba45462db313a9f4e16cc47e4550dbef6
ms.sourcegitcommit: 92629114d5081103bfe555081f69997af4ed56f2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2018
ms.locfileid: "2875776"
---
# <a name="microsoft-azure-vm-sizing-for-maximum-reservation-usage"></a><span data-ttu-id="8a396-103">Dimensionamento de VM do Microsoft Azure para uso máximo de reserva do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-103">Microsoft Azure VM sizing for maximum reservation usage</span></span> 

**<span data-ttu-id="8a396-104">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="8a396-104">Applies to</span></span>**

-  <span data-ttu-id="8a396-105">Painel de parceiros</span><span class="sxs-lookup"><span data-stu-id="8a396-105">Partner dashboard</span></span>
-  <span data-ttu-id="8a396-106">Portal do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-106">Azure portal</span></span>
-  <span data-ttu-id="8a396-107">Parceiros no CSP</span><span class="sxs-lookup"><span data-stu-id="8a396-107">Partners in CSP</span></span>

## <a name="determine-the-vm-size-for-a-customers-azure-reservation"></a><span data-ttu-id="8a396-108">Determinar o tamanho da VM para reserva do Azure do cliente</span><span class="sxs-lookup"><span data-stu-id="8a396-108">Determine the VM size for a customer’s Azure reservation</span></span> 

<span data-ttu-id="8a396-109">Ao comprar reservas do Microsoft Azure em nome dos seus clientes, você precisará escolher uma máquina virtual (VM) dimensionada para atender às necessidades de computação do cliente.</span><span class="sxs-lookup"><span data-stu-id="8a396-109">When buying Microsoft Azure reservations on behalf of your customers, you’ll need to choose a virtual machine (VM) sized to meet the customer’s computing needs.</span></span> <span data-ttu-id="8a396-110">Você pode encontrar essas informações usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="8a396-110">You can find this information using one of these methods:</span></span>

-   <span data-ttu-id="8a396-111">API de utilização do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-111">Azure utilization API</span></span>
-   <span data-ttu-id="8a396-112">O portal do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-112">The Azure portal</span></span>
-   <span data-ttu-id="8a396-113">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a396-113">Azure PowerShell</span></span>
-   <span data-ttu-id="8a396-114">A API do Azure Resource Manager (ARM)</span><span class="sxs-lookup"><span data-stu-id="8a396-114">The Azure Resource Manager (ARM) API</span></span>

<span data-ttu-id="8a396-115">As instruções para o uso de cada um desses métodos estão listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a396-115">Instructions for using each of these methods are below.</span></span> <span data-ttu-id="8a396-116">Depois que você comprar uma reserva, o desconto da reserva será aplicado automaticamente em máquinas virtuais que correspondam aos atributos e à quantidade da reserva.</span><span class="sxs-lookup"><span data-stu-id="8a396-116">After you buy a reservation, the reservation discount is applied automatically to virtual machines matching the attributes and quantity of the reservation.</span></span> <span data-ttu-id="8a396-117">Você não precisa atribuir a reserva a uma VM.</span><span class="sxs-lookup"><span data-stu-id="8a396-117">You don’t need to assign the reservation to a VM.</span></span>

>[!NOTE]
><span data-ttu-id="8a396-118">Os descontos da reserva não se aplicam a VMs clássicas ou promocionais.</span><span class="sxs-lookup"><span data-stu-id="8a396-118">Reservation discounts don’t apply to classic or promotional VMs.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8a396-119">Para identificar o tipo e o tamanho da VM a ser comprada em nome de seu cliente, você deverá usar um dos métodos descritos abaixo já que o tipo de série de VM não é exibido corretamente nos arquivos de reconciliação do Partner Center.</span><span class="sxs-lookup"><span data-stu-id="8a396-119">To correctly identify the type and size of VM to buy on behalf of your customer, you must use one of the methods described below as the VM series type is not correctly displayed in Partner Center reconciliation files.</span></span>


**<span data-ttu-id="8a396-120">Obter informações de dimensionamento de VM usando a API de utilização do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-120">Get VM sizing information using the Azure utilization API</span></span>**

1.  <span data-ttu-id="8a396-121">Use o valor do atributo ServiceType desde additionalInfo na resposta da API para identificar o tamanho da VM a ser comprada.</span><span class="sxs-lookup"><span data-stu-id="8a396-121">Use the value for ServiceType attribute from additionalInfo in the API response to identify the VM size to buy.</span></span> 

2.  <span data-ttu-id="8a396-122">Para obter mais informações, consulte [obter registros de utilização de um cliente do Azure](https://docs.microsoft.com/partner-center/develop/get-a-customer-s-utilization-record-for-azure) no [Painel de parceiros API](https://docs.microsoft.com/partner-center/develop/).</span><span class="sxs-lookup"><span data-stu-id="8a396-122">For more information, see [Get a customer’s utilization records for Azure](https://docs.microsoft.com/partner-center/develop/get-a-customer-s-utilization-record-for-azure) in the [Partner dashboard API](https://docs.microsoft.com/partner-center/develop/).</span></span> 

**<span data-ttu-id="8a396-123">Obter informações de dimensionamento de VM usando o portal do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-123">Get VM sizing information using the Microsoft Azure portal</span></span>**

1.  <span data-ttu-id="8a396-124">No painel de parceiros, vá para a página de **clientes** .</span><span class="sxs-lookup"><span data-stu-id="8a396-124">In your Partner dashboard, go to your **Customers** page.</span></span>

2.  <span data-ttu-id="8a396-125">Encontre o cliente que deseja comprar reservas de VM do Azure e então selecione a seta para baixo para expandir as informações do cliente.</span><span class="sxs-lookup"><span data-stu-id="8a396-125">Find the customer who wants to buy Azure VM reservations and then select the down arrow to expand the customer’s information.</span></span> <span data-ttu-id="8a396-126">Selecione **Portal de Gerenciamento do Microsoft Azure** para abrir o registro do cliente no portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a396-126">Select **Microsoft Azure Management Portal** to open the customer’s record in the Azure portal.</span></span> 

3.  <span data-ttu-id="8a396-127">Selecione **Máquinas virtuais** no menu do portal e então selecione a VM para a qual você deseja comprar uma reserva.</span><span class="sxs-lookup"><span data-stu-id="8a396-127">Select **Virtual machines** from the portal menu and then select the VM for which you want to buy a reservation.</span></span> 

4.  <span data-ttu-id="8a396-128">Na página de detalhes da VM, encontre as informações de tamanho e região, como ilustrado abaixo, e use essas informações para comprar a reserva no Partner Center.</span><span class="sxs-lookup"><span data-stu-id="8a396-128">On the VM’s detail page, find the size and region information, as illustrated below, and use this information to purchase the reservation in Partner Center.</span></span>  

    ![](images/usage1.png)

**<span data-ttu-id="8a396-129">Obter informações de dimensionamento de VM usando o Microsoft Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a396-129">Get VM sizing information using Microsoft Azure PowerShell</span></span>**

<span data-ttu-id="8a396-130">Use as informações na imagem abaixo para obter a localização e o tamanho da VM para a qual você deseja comprar uma reserva.</span><span class="sxs-lookup"><span data-stu-id="8a396-130">Use the information in the image below to get the location and size of the VM for which you want to buy a reservation.</span></span> 

![](images/usage2.png)

**<span data-ttu-id="8a396-131">Obter informações de dimensionamento de VM usando a API do Azure Resource Manager (ARM)</span><span class="sxs-lookup"><span data-stu-id="8a396-131">Get VM sizing information using the Azure Resource Manager (ARM) API</span></span>**

1.  <span data-ttu-id="8a396-132">Usando o ARMClient ou as APIs ARM, chame o cliente ARM para a VM para a qual você deseja comprar uma reserva.</span><span class="sxs-lookup"><span data-stu-id="8a396-132">Using the ARMClient or the ARM APIs, call the ARM client for the VM for which you want to buy a reservation.</span></span>

2.  <span data-ttu-id="8a396-133">/subscriptions/<Subscription ID>/resourceGroups/<Resource group name>/providers/Microsoft.Compute/virtualMachines/<VM Instance Name>?api-version=2017-12-01</span><span class="sxs-lookup"><span data-stu-id="8a396-133">/subscriptions/<Subscription ID>/resourceGroups/<Resource group name>/providers/Microsoft.Compute/virtualMachines/<VM Instance Name>?api-version=2017-12-01</span></span>

3.  <span data-ttu-id="8a396-134">A chamada retorna os valores de **vmSize** e **location**, como ilustrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="8a396-134">The call returns the values for **vmSize** and **location**, as illustrated below.</span></span>

    ![](images/usage3.png)
    ![](images/usage4.png)
 

## <a name="verify-azure-vm-usage-and-reservation-discount"></a><span data-ttu-id="8a396-135">Verificar o desconto de uso e de reserva de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-135">Verify Azure VM usage and reservation discount</span></span>

<span data-ttu-id="8a396-136">Depois de você comprar uma Instância de VM Reservada do Azure em nome de um cliente, o desconto para pagamento antecipado pelo espaço de VM será automaticamente aplicado às máquinas virtuais que correspondem aos atributos e à quantidade de reservas do cliente.</span><span class="sxs-lookup"><span data-stu-id="8a396-136">After you purchase an Azure Reserved VM Instance on behalf of a customer, the discount for paying for VM space in advance is automatically applied to the virtual machines that match the attributes and quantity of the customer’s reservation.</span></span> 

<span data-ttu-id="8a396-137">Você pode verificar o uso de reservas do cliente e ver para quais máquinas virtuais os descontos de reserva são aplicados usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="8a396-137">You can verify the customer’s reservation usage and see which virtual machines the reservation discounts are applied to by using one of the following methods:</span></span>   

-   <span data-ttu-id="8a396-138">O portal do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-138">The Azure portal</span></span>
-   <span data-ttu-id="8a396-139">API de utilização do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-139">Azure utilization API</span></span>

<span data-ttu-id="8a396-140">As instruções para o uso de cada um desses métodos estão listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a396-140">Instructions for using each of these methods are below.</span></span>

>[!NOTE]
><span data-ttu-id="8a396-141">Somente a API de utilização do Azure mostra a qual máquina virtual o desconto está sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="8a396-141">Only the Azure utilization API shows which virtual machine the discount is being applied to.</span></span>  

### <a name="verify-the-customers-reservation-usage-in-the-microsoft-azure-portal"></a><span data-ttu-id="8a396-142">Verificar o uso de reserva do cliente no portal do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-142">Verify the customer’s reservation usage in the Microsoft Azure portal</span></span>

1.  <span data-ttu-id="8a396-143">No painel de parceiros, vá para a página de **clientes** .</span><span class="sxs-lookup"><span data-stu-id="8a396-143">In your Partner dashboard, go to your **Customers** page.</span></span>

2.  <span data-ttu-id="8a396-144">Encontre o cliente cujo desconto e uso de reserva você deseja verificar e então selecione a seta para baixo para expandir as informações do cliente.</span><span class="sxs-lookup"><span data-stu-id="8a396-144">Find the customer whose reservation discount and usage you want to verify and then select the down arrow to expand the customer’s information.</span></span> <span data-ttu-id="8a396-145">Selecione **Portal de Gerenciamento do Microsoft Azure** para abrir o registro do cliente no portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a396-145">Select **Microsoft Azure Management Portal** to open the customer’s record in the Azure portal.</span></span> 

3.  <span data-ttu-id="8a396-146">Selecione **Reservas** no menu do portal e então selecione a reserva cujo uso você deseja verificar.</span><span class="sxs-lookup"><span data-stu-id="8a396-146">Select **Reservations** from the portal menu and then select the reservation you want to check usage for.</span></span> 

4.  <span data-ttu-id="8a396-147">Na página **Visão geral**, verifique o gráfico de utilização da reserva, que mostra o quanto da reserva foi aplicado às máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="8a396-147">On the **Overview** page check the reservation’s utilization graph, which shows how much of the reservation was applied to virtual machines.</span></span> 

    >[!NOTE]
    ><span data-ttu-id="8a396-148">Os dados de utilização podem ser atrasados em até 8 horas.</span><span class="sxs-lookup"><span data-stu-id="8a396-148">Utilization data may be delayed by up to 8 hours.</span></span>
    
    <span data-ttu-id="8a396-149">a.</span><span class="sxs-lookup"><span data-stu-id="8a396-149">a.</span></span>  <span data-ttu-id="8a396-150">Se a utilização da reserva for de 100%, o cliente estará recebendo toda a economia possível que a compra de reserva pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="8a396-150">If the reservation’s utilization is 100%, your customer is getting all the possible savings that the reservation purchase can provide.</span></span> 
    
    <span data-ttu-id="8a396-151">b.</span><span class="sxs-lookup"><span data-stu-id="8a396-151">b.</span></span>  <span data-ttu-id="8a396-152">Se o uso da reserva for 0%, o desconto não estará sendo aplicado a nenhuma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8a396-152">If the reservation’s usage is 0%, the discount is not being applied to any virtual machine.</span></span> 
    
    <span data-ttu-id="8a396-153">c.</span><span class="sxs-lookup"><span data-stu-id="8a396-153">c.</span></span>  <span data-ttu-id="8a396-154">Se o uso da reserva estiver entre 1% e 99%, há benefícios não utilizados.</span><span class="sxs-lookup"><span data-stu-id="8a396-154">If the reservation’s usage is between 1% and 99%, there are unused benefits.</span></span> 

5.  <span data-ttu-id="8a396-155">Para evitar essa situação, determine a VM de tamanho correto para dar suporte às necessidades de computação do cliente antes de fazer a compra.</span><span class="sxs-lookup"><span data-stu-id="8a396-155">To avoid this situation, determine the correct size VM to support the customer’s computing needs before making the purchase.</span></span>

### <a name="verify-the-customers-reservation-usage-with-the-azure-utilization-api"></a><span data-ttu-id="8a396-156">Verificar o uso de reserva do cliente com a API de utilização do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-156">Verify the customer’s reservation usage with the Azure utilization API</span></span>

>[!NOTE]
><span data-ttu-id="8a396-157">Somente a API de utilização do Azure mostra a qual máquina virtual o desconto está sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="8a396-157">Only the Azure utilization API shows which virtual machine the discount is being applied to.</span></span>  

<span data-ttu-id="8a396-158">Você pode obter dados de uso da reserva com a API de utilização do Azure para verificar se o cliente está recebendo o desconto da reserva e para ver a quais VMs (máquinas virtuais) o desconto é aplicado.</span><span class="sxs-lookup"><span data-stu-id="8a396-158">You can get reservation usage data with the Azure utilization API to verify that the customer is getting the reservation discount and to see which VMs (virtual machines) the discount is applied to.</span></span> <span data-ttu-id="8a396-159">Compare o Exemplo A ao Exemplo B para saber como verificar o uso da reserva de um cliente.</span><span class="sxs-lookup"><span data-stu-id="8a396-159">Compare Example A to Example B to see how to verify a customer’s reservation usage.</span></span> 

![](images\usage5.png)

-   <span data-ttu-id="8a396-160">A reservationId identifica a reserva do Azure que foi usada para aplicar o desconto à VM.</span><span class="sxs-lookup"><span data-stu-id="8a396-160">The reservationId identifies the Azure reservation that was used to apply the discount to the VM.</span></span>
-   <span data-ttu-id="8a396-161">consumptionMeter é a MeterId para a VM que tem o desconto da reserva aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="8a396-161">consumptionMeter is the MeterId for the VM that has the reservation discount applied to it.</span></span>
-   <span data-ttu-id="8a396-162">O ReservationMeter mostra o custo de US$ 0 desde que o desconto da reserva foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="8a396-162">The ReservationMeter shows $0 cost since the reservation discount was applied.</span></span> 

<span data-ttu-id="8a396-163">Para obter mais informações, consulte [Obter registros de utilização de um cliente do Azure](https://docs.microsoft.com/partner-center/develop/get-a-customer-s-utilization-record-for-azure) na [API do Partner Center](https://docs.microsoft.com/partner-center/develop/).</span><span class="sxs-lookup"><span data-stu-id="8a396-163">For more information, see [Get a customer’s utilization records for Azure](https://docs.microsoft.com/partner-center/develop/get-a-customer-s-utilization-record-for-azure) in the [Partner Center API](https://docs.microsoft.com/partner-center/develop/).</span></span>

>[!IMPORTANT]
><span data-ttu-id="8a396-164">Os custos de software, como o Microsoft Windows Server, não estão incluídos no preço de uma reserva de VM e aparecerão como itens de linha separados no registro do pedido e em sua fatura.</span><span class="sxs-lookup"><span data-stu-id="8a396-164">Software costs, such as Microsoft Windows Server, are not currently included in the price of a VM reservation and will appear as separate line items in the order record and on your invoice.</span></span> <span data-ttu-id="8a396-165">No entanto, se um cliente tiver o Benefício de Uso Híbrido do Azure, os custos de software não serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="8a396-165">However, if a customer has the Azure Hybrid Use Benefit, the software costs will not be applied.</span></span> <span data-ttu-id="8a396-166">Para obter mais informações, consulte [Custos de software do Windows não incluídos com Instâncias Reservadas](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs).</span><span class="sxs-lookup"><span data-stu-id="8a396-166">For more information, see [Windows software costs not included with Reserved Instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs).</span></span>  

## <a name="azure-reservations-resources"></a><span data-ttu-id="8a396-167">Recursos de reservas do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-167">Azure reservations resources</span></span>
|**<span data-ttu-id="8a396-168">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="8a396-168">For information about</span></span>**   |**<span data-ttu-id="8a396-169">Leia isto</span><span class="sxs-lookup"><span data-stu-id="8a396-169">Read this</span></span>**    |
|:-----------------------------|:-----------------|
|<span data-ttu-id="8a396-170">Reservas do Azure na visão geral do CSP</span><span class="sxs-lookup"><span data-stu-id="8a396-170">Azure reservations in CSP overview</span></span>  | [<span data-ttu-id="8a396-171">Vender Instâncias de VM Reservadas do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-171">Sell Microsoft Azure Reserved VM Instances</span></span>](azure-reservations.md)
|<span data-ttu-id="8a396-172">Como comprar reservas do Azure para seus clientes no painel de parceiros</span><span class="sxs-lookup"><span data-stu-id="8a396-172">Purchasing Azure reservations for your customers in your Partner dashboard</span></span>   |[<span data-ttu-id="8a396-173">Comprar reservas do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-173">Buy Azure reservations</span></span>](azure-reservations-buying.md)
| <span data-ttu-id="8a396-174">Gerenciar reservas do Azure no painel de parceiros</span><span class="sxs-lookup"><span data-stu-id="8a396-174">Managing Azure reservations in your Partner dashboard</span></span> | [<span data-ttu-id="8a396-175">Gerenciar reservas do Azure no painel de parceiros</span><span class="sxs-lookup"><span data-stu-id="8a396-175">Managing Azure reservations in your Partner dashboard</span></span>](azure-reservations-manage.md)
|<span data-ttu-id="8a396-176">Como comprar reservas do Azure no portal do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-176">Purchasing Azure reservations in the Azure portal</span></span> | <span data-ttu-id="8a396-177">[Pagar antecipadamente por máquinas virtuais com Instâncias de VM Reservadas do Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances) na Ajuda do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-177">[Prepay for virtual machines with Azure Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances) in the Azure Help</span></span> |
|<span data-ttu-id="8a396-178">Como gerenciar reservas do Azure no portal do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-178">Managing Azure reservations in the Azure portal</span></span>   |<span data-ttu-id="8a396-179">[Gerenciar instâncias de VM reservadas](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance) na Ajuda do Azure</span><span class="sxs-lookup"><span data-stu-id="8a396-179">[Manage reserved VM instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance) in the Azure Help</span></span>  |
|<span data-ttu-id="8a396-180">Como comprar reservas do Azure usando a API do Partner Center</span><span class="sxs-lookup"><span data-stu-id="8a396-180">Purchasing Azure reservations using the Partner Center API</span></span> | <span data-ttu-id="8a396-181">[Comprar Instâncias de VM Reservadas do Azure](https://docs.microsoft.com/partner-center/develop/purchase-azure-reservations) na documentação do desenvolvedor do Partner Center</span><span class="sxs-lookup"><span data-stu-id="8a396-181">[Purchase Azure Reserved VM Instances](https://docs.microsoft.com/partner-center/develop/purchase-azure-reservations) in the Partner Center developer documentation</span></span>


