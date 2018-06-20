---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True si le compte est un compte Exchange.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782799"
---
# <a name="propacctisexch"></a><span data-ttu-id="a960f-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="a960f-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="a960f-104">True si le compte est un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="a960f-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a960f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a960f-105">Quick info</span></span>

<span data-ttu-id="a960f-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a960f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a960f-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a960f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a960f-108">0 x 0014</span><span class="sxs-lookup"><span data-stu-id="a960f-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="a960f-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="a960f-109">Property type:</span></span>  <br/> |<span data-ttu-id="a960f-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a960f-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a960f-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="a960f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a960f-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="a960f-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="a960f-113">Access :</span><span class="sxs-lookup"><span data-stu-id="a960f-113">Access:</span></span>  <br/> |<span data-ttu-id="a960f-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a960f-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a960f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a960f-115">Remarks</span></span>

<span data-ttu-id="a960f-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a960f-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="a960f-117">Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="a960f-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a960f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a960f-118">See also</span></span>

- [<span data-ttu-id="a960f-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="a960f-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="a960f-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a960f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

