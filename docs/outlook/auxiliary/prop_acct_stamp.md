---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Renvoie les informations de compte.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: c55eec212ae794592c83bbf06b01eab5ca6bff6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "19782822"
---
# <a name="propacctstamp"></a><span data-ttu-id="7538a-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="7538a-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="7538a-104">Renvoie les informations de compte.</span><span class="sxs-lookup"><span data-stu-id="7538a-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7538a-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7538a-105">Quick info</span></span>

<span data-ttu-id="7538a-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="7538a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7538a-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7538a-107">Identifier:</span></span>  <br/> |<span data-ttu-id="7538a-108">0x000d</span><span class="sxs-lookup"><span data-stu-id="7538a-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="7538a-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="7538a-109">Property type:</span></span>  <br/> |<span data-ttu-id="7538a-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7538a-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7538a-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="7538a-111">Property tag:</span></span>  <br/> |<span data-ttu-id="7538a-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="7538a-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="7538a-113">Access :</span><span class="sxs-lookup"><span data-stu-id="7538a-113">Access:</span></span>  <br/> |<span data-ttu-id="7538a-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7538a-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7538a-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7538a-115">Remarks</span></span>

<span data-ttu-id="7538a-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="7538a-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="7538a-117">Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="7538a-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7538a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7538a-118">See also</span></span>

- [<span data-ttu-id="7538a-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="7538a-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="7538a-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="7538a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

