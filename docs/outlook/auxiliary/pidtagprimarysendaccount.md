---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Spécifie le principal accountsendstamp pour un message.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394083"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="a4f48-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="a4f48-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="a4f48-104">Indique le compte principal « envoyer » pour un message.</span><span class="sxs-lookup"><span data-stu-id="a4f48-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a4f48-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a4f48-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4f48-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a4f48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4f48-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="a4f48-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="a4f48-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a4f48-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4f48-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="a4f48-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="a4f48-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a4f48-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4f48-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a4f48-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a4f48-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a4f48-112">Area:</span></span>  <br/> |<span data-ttu-id="a4f48-113">Compte</span><span class="sxs-lookup"><span data-stu-id="a4f48-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4f48-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4f48-114">Remarks</span></span>

<span data-ttu-id="a4f48-115">Cette propriété s’applique à un objet de message MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4f48-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="a4f48-116">Pour un message reçu, l’horodatage « envoyer » de compte principal indique quel compte de transfert ou une réponse doit être envoyée avec.</span><span class="sxs-lookup"><span data-stu-id="a4f48-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="a4f48-117">Pour un message sortant, il détermine quel compte pour envoyer le message avec.</span><span class="sxs-lookup"><span data-stu-id="a4f48-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="a4f48-118">Sa valeur est la valeur [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) à partir de l’interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="a4f48-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4f48-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f48-119">See also</span></span>

- [<span data-ttu-id="a4f48-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a4f48-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="a4f48-121">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a4f48-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="a4f48-122">Propriété canonique PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="a4f48-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

