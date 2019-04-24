---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Spécifie le accountsendstamp principal d'un message.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327705"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="33473-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="33473-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="33473-104">Spécifie le cachet «envoyer» du compte principal pour un message.</span><span class="sxs-lookup"><span data-stu-id="33473-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="33473-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="33473-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33473-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="33473-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33473-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="33473-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="33473-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="33473-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33473-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="33473-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="33473-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="33473-110">Data type:</span></span>  <br/> |<span data-ttu-id="33473-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="33473-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="33473-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="33473-112">Area:</span></span>  <br/> |<span data-ttu-id="33473-113">Compte</span><span class="sxs-lookup"><span data-stu-id="33473-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33473-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="33473-114">Remarks</span></span>

<span data-ttu-id="33473-115">Cette propriété s'applique à un objet message MAPI.</span><span class="sxs-lookup"><span data-stu-id="33473-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="33473-116">Pour un message reçu, le cachet «envoyer» du compte principal indique le compte vers lequel un envoi ou une réponse doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="33473-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="33473-117">Pour un message sortant, il détermine le compte avec lequel envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="33473-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="33473-118">Sa valeur est la valeur [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) de l'interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="33473-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33473-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33473-119">See also</span></span>

- [<span data-ttu-id="33473-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="33473-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="33473-121">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="33473-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="33473-122">Propriété canonique PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="33473-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

