---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Renvoie l’accountsendstamp.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782803"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="d6555-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="d6555-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="d6555-104">Renvoie le tampon de « envoyer » de compte.</span><span class="sxs-lookup"><span data-stu-id="d6555-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d6555-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d6555-105">Quick info</span></span>

<span data-ttu-id="d6555-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d6555-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6555-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d6555-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d6555-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="d6555-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="d6555-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d6555-109">Property type:</span></span>  <br/> |<span data-ttu-id="d6555-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6555-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6555-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="d6555-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d6555-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="d6555-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="d6555-113">Access :</span><span class="sxs-lookup"><span data-stu-id="d6555-113">Access:</span></span>  <br/> |<span data-ttu-id="d6555-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6555-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6555-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6555-115">Remarks</span></span>

<span data-ttu-id="d6555-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="d6555-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d6555-117">Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="d6555-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6555-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6555-118">See also</span></span>

- [<span data-ttu-id="d6555-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="d6555-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="d6555-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d6555-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

