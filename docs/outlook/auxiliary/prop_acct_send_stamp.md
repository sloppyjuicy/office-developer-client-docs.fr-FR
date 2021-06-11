---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Renvoie le accountsendstamp.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423005"
---
# <a name="prop_acct_send_stamp"></a><span data-ttu-id="b9b1e-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="b9b1e-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="b9b1e-104">Renvoie le cachet « envoyer » du compte.</span><span class="sxs-lookup"><span data-stu-id="b9b1e-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b9b1e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="b9b1e-105">Quick info</span></span>

<span data-ttu-id="b9b1e-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b9b1e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9b1e-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b9b1e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b9b1e-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="b9b1e-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="b9b1e-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="b9b1e-109">Property type:</span></span>  <br/> |<span data-ttu-id="b9b1e-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9b1e-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b9b1e-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="b9b1e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b9b1e-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="b9b1e-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="b9b1e-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="b9b1e-113">Access:</span></span>  <br/> |<span data-ttu-id="b9b1e-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9b1e-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9b1e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9b1e-115">Remarks</span></span>

<span data-ttu-id="b9b1e-116">Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="b9b1e-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="b9b1e-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="b9b1e-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9b1e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9b1e-118">See also</span></span>

- [<span data-ttu-id="b9b1e-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="b9b1e-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="b9b1e-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="b9b1e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

