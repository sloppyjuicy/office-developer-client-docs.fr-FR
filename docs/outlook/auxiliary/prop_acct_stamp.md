---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Renvoie le cachet du compte.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408249"
---
# <a name="prop_acct_stamp"></a><span data-ttu-id="ff95b-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="ff95b-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="ff95b-104">Renvoie le cachet du compte.</span><span class="sxs-lookup"><span data-stu-id="ff95b-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff95b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ff95b-105">Quick info</span></span>

<span data-ttu-id="ff95b-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ff95b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff95b-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ff95b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ff95b-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="ff95b-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="ff95b-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="ff95b-109">Property type:</span></span>  <br/> |<span data-ttu-id="ff95b-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff95b-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ff95b-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="ff95b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ff95b-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="ff95b-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="ff95b-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="ff95b-113">Access:</span></span>  <br/> |<span data-ttu-id="ff95b-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ff95b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff95b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff95b-115">Remarks</span></span>

<span data-ttu-id="ff95b-116">Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ff95b-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ff95b-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ff95b-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff95b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff95b-118">See also</span></span>

- [<span data-ttu-id="ff95b-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="ff95b-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="ff95b-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="ff95b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

