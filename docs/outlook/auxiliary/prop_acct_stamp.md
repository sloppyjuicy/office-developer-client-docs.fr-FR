---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Renvoie le cachet de compte.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327593"
---
# <a name="propacctstamp"></a><span data-ttu-id="69b1e-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="69b1e-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="69b1e-104">Renvoie le cachet de compte.</span><span class="sxs-lookup"><span data-stu-id="69b1e-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="69b1e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="69b1e-105">Quick info</span></span>

<span data-ttu-id="69b1e-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="69b1e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69b1e-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="69b1e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="69b1e-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="69b1e-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="69b1e-109">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="69b1e-109">Property type:</span></span>  <br/> |<span data-ttu-id="69b1e-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69b1e-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="69b1e-111">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="69b1e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="69b1e-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="69b1e-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="69b1e-113">Access</span><span class="sxs-lookup"><span data-stu-id="69b1e-113">Access:</span></span>  <br/> |<span data-ttu-id="69b1e-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69b1e-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69b1e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="69b1e-115">Remarks</span></span>

<span data-ttu-id="69b1e-116">Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="69b1e-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="69b1e-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="69b1e-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69b1e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69b1e-118">See also</span></span>

- [<span data-ttu-id="69b1e-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="69b1e-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="69b1e-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="69b1e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

