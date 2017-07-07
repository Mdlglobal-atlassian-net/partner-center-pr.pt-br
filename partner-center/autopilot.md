---
title: "Simplificar a configuração do dispositivo com o Windows AutoPilot | Partner Center"
description: "Adicione um perfil de implantação do Windows AutoPilot no Partner Center para simplificar a configuração do dispositivo com o Windows AutoPilot"
author: KPacquer
keywords: "piloto automático, windows autopilot, piloto automático da microsoft, implantação zero touch, oobe, telas de logon"
robots: NOINDEX,NOFOLLOW
ms.openlocfilehash: aa650ee5f2848694fe44d4751d52f8014e0d22a8
ms.sourcegitcommit: e8b504fa98b3ec4c7c8fd954f63ea81299791906
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2017
---
# <a name="simplify-device-setup-with-windows-autopilot"></a>Simplificar a configuração do dispositivo com o Windows AutoPilot 

O Windows AutoPilot simplifica e protege a configuração de novos dispositivos Windows 10 Pro a partir da primeira inicialização em apenas algumas etapas. Para saber mais, consulte [Visão geral do Windows AutoPilot](https://docs.microsoft.com/windows/deployment/windows-10-auto-pilot).

## <a name="features"></a>Recursos

*  **Desativar as permissões de administrador local** para que os usuários finais configurem os dispositivos
*  **Mostra a página de logon de uma organização**. A organização pode predefinir uma página de logon que adiciona o dispositivo como um dispositivo de trabalho e o associa ao Azure Active Directory.
*  **Registre o dispositivo em um MDM (Gerenciador de Dispositivos Móveis)**, por exemplo, o Microsoft Intune, após a conclusão da OOBE (configuração inicial pelo usuário).
*  **Simplifique a OOBE** para usar apenas as etapas e decisões necessárias, usando um perfil de implantação do Windows AutoPilot. 

## <a name="requirements"></a>Requisitos

*  Dispositivos pré-instalados com a Atualização do Windows 10 Pro para Criadores (versão 1703 ou posterior)
*  O identificador de dispositivo conhecido como um hash de hardware (128 HWH ou 4K HWH), que normalmente é fornecido por um OEM. Você usará identificadores para atribuir perfis da organização no Partner Center. Depois de agosto de 2017, o hash de hardware não será mais necessário. 
*  Os dispositivos devem ter acesso à Internet. Quando o dispositivo não consegue se conectar, ele mostra que as telas padrão da experiência inicial do Windows (OOBE).
*  O registro do dispositivo em um MDM requer o Azure Active Directory Premium.

## <a name="add-organization-login-pages-to-oobe"></a>Adicionar páginas de login da organização à OOBE

Para adicionar páginas específicas da organização, adicione os dispositivos ao [diretório do Azure AD](https://go.microsoft.com/fwlink/?linkid=848958) da organização e crie páginas de logon.


## <a name="remove-windows-pages-from-oobe-with-a-windows-autopilot-deployment-profile"></a>Remover páginas do Windows da OOBE com um perfil de implantação do Windows AutoPilot

### <a name="examples-of-settings-in-a-windows-autopilot-deployment-profile"></a>Exemplos de configurações em um perfil de implantação do Windows AutoPilot
*  Ignorar as Configurações de privacidade na instalação
*  Desabilitar a conta de administrador local na instalação
*  Ignorar automaticamente as páginas na instalação
   *  Selecionar automaticamente a configuração para trabalho ou escola
   *  Ignorar a Cortana, o OneDrive e páginas de configuração de registro OEM

### <a name="add-devices-and-apply-a-profile"></a>Adicionar dispositivos e aplicar um perfil

No Partner Center, você pode criar um perfil de implantação do Windows AutoPilot e aplicá-lo a uma lista dos dispositivos.

Para configurar os dispositivos, envie uma lista dos dispositivos para o Partner Center, crie um perfil que seja aplicável aos dispositivos e aplique-o.

1.  Adicione a lista de dispositivos ao Partner Center. (agentes de vendas e agentes de administrador têm acesso para adicionar a lista de dispositivos ao Partner Center.)

    a.  Crie um arquivo .csv usando o script do PowerShell do tópico: [Visão geral do Windows AutoPilot](https://docs.microsoft.com/windows/deployment/windows-10-auto-pilot). Esse arquivo .csv contém informações do dispositivo, incluindo o número de série, o nome do OEM, o nome do modelo, a ID do produto e o identificador do dispositivo. 

    b.  No painel do Partner Center, vá para **Clientes** > selecione o cliente que está recebendo os dispositivos > **Dispositivos > Adicionar dispositivos**.

    c.  Nomeie o lote de dispositivos, por exemplo, "Computadores do departamento de vendas da Contoso – Pedido de abril de 2017". 

    d.  Clique em **Procurar** > selecione o arquivo de informações do dispositivo > **Validar**.

    **Observação:** se você receber uma mensagem de erro depois de tentar carregar o arquivo .csv, verifique o formato do arquivo. Depois de agosto, você poderá usar somente o hash de hardware ou o nome do OEM, o número de série e o modelo nessa ordem de colunas ou a ID do produto Windows. Você também pode usar o arquivo .csv de exemplo fornecido a partir do link próximo a **Adicionar dispositivos**.

2.  Crie um perfil que você possa aplicar aos dispositivos. (somente agentes de administrador têm acesso para criar e aplicar perfis no Partner Center.)

    a.  Em **Dispositivos**, clique em **Adicionar novo perfil**.

    b.  Nomeie o perfil, por exemplo, "Perfil de área de trabalho Contoso – Ignorar todo o OOBE".

    c.  Defina as configurações de OOBE. Por exemplo, marque **Ignorar as configurações expressas na instalação**.

    d.  Clique em **Enviar**.

3.  Aplique o perfil.

    a.  Em **Dispositivos**, no painel **Atribuir e excluir dispositivos**, selecione os dispositivos que você deseja configurar. Para selecionar um lote completo, clique na caixa de seleção ao lado do nome do lote (por exemplo, "Computadores do departamento de vendas da Contoso – Pedido de março de 2017").

    b.  Clique em **Aplicar perfil** e selecione o perfil (por exemplo, "Perfil de área de trabalho da Contoso – Ignorar todos os OOBE"). Os dispositivos mostrarão o perfil na coluna Perfil.

4.  Opcional: teste para verificar se o perfil funciona.

    a.  Conecte um dispositivo à rede e ative-o.

    b.  Verifique se aparecem as telas OOBE apropriadas (se existirem).

    c.  Para preparar o dispositivo para um novo usuário, conclua a experiência de OOBE e, em seguida, redefina o dispositivo com as configurações padrão de fábrica.


## <a name="to-update-or-delete-a-profile"></a>Para atualizar ou excluir um perfil 

Depois de atribuir um perfil a um dispositivo, você pode atualizá-lo, mesmo se você já deu o dispositivo para o cliente. Quando o dispositivo é conectado à Internet, ele baixa a versão mais recente do perfil durante o processo de OOBE. Se o cliente restaura o dispositivo com as configurações padrão de fábrica, o dispositivo baixará novamente as atualizações mais recentes para seu perfil. 

###<a name="you-can-remove-a-profile-from-a-device"></a>Você pode remover um perfil de um dispositivo
1. Selecione o dispositivo (ou lotes de dispositivos) para remover o perfil. 

2. No painel **Atribuir e excluir dispositivos**, selecione **Remover perfil**.

3. Vá para o perfil que você deseja remover e exclua-o. O perfil será excluído de todos os dispositivos.

Em **Dispositivos**, selecione o perfil. Aqui, você pode modificar as configurações atuais.