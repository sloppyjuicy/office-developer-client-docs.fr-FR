---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Spécifie l’accountsendstamp secondaire pour le message.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782806"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="6f10f-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="6f10f-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="6f10f-104">Indique le compte secondaire « Envoyer » pour le message.</span><span class="sxs-lookup"><span data-stu-id="6f10f-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6f10f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="6f10f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f10f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f10f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f10f-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="6f10f-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="6f10f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f10f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f10f-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="6f10f-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="6f10f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f10f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f10f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f10f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f10f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6f10f-112">Area:</span></span>  <br/> |<span data-ttu-id="6f10f-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="6f10f-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f10f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f10f-114">Remarks</span></span>

<span data-ttu-id="6f10f-115">Cette propriété s’applique à un objet de message MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f10f-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="6f10f-116">Pour un message reçu, l’horodatage « envoyer » de compte secondaire indique quel compte de transfert ou une réponse doit être envoyée, si le transfert et réponse ne peut pas être envoyé avec le compte principal.</span><span class="sxs-lookup"><span data-stu-id="6f10f-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="6f10f-117">Pour un message sortant, le compte secondaire « Envoyer » horodatage détermine avec le compte à envoyer le message, si le message ne peut pas être envoyé avec le compte principal.</span><span class="sxs-lookup"><span data-stu-id="6f10f-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="6f10f-118">Sa valeur est la valeur [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) à partir de l’interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="6f10f-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f10f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f10f-119">See also</span></span>

- [<span data-ttu-id="6f10f-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="6f10f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="6f10f-121">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f10f-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="6f10f-122">Propriété canonique PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="6f10f-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

