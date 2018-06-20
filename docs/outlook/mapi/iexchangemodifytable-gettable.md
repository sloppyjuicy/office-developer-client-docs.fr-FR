---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783688"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="879a3-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="879a3-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="879a3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="879a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="879a3-105">Retourne un pointeur vers une interface pour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="879a3-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="879a3-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="879a3-106">Parameters</span></span>

 <span data-ttu-id="879a3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="879a3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="879a3-108">[in] Réservé ; doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="879a3-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="879a3-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="879a3-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="879a3-110">Définit les nouveaux droits.</span><span class="sxs-lookup"><span data-stu-id="879a3-110">Sets new rights.</span></span>
    
<span data-ttu-id="879a3-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="879a3-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="879a3-112">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="879a3-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="879a3-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="879a3-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="879a3-114">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple de nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="879a3-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="879a3-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="879a3-115">_lppTable_</span></span>
  
> <span data-ttu-id="879a3-116">[out] Pointe vers une [IMAPITable : IUnknown](imapitableiunknown.md) interface contenant l’objet table.</span><span class="sxs-lookup"><span data-stu-id="879a3-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="879a3-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="879a3-117">MFCMAPI reference</span></span>

<span data-ttu-id="879a3-118">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="879a3-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="879a3-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="879a3-119">**File**</span></span>|<span data-ttu-id="879a3-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="879a3-120">**Function**</span></span>|<span data-ttu-id="879a3-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="879a3-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="879a3-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="879a3-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="879a3-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="879a3-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="879a3-124">MFCMAPI utilise la méthode **IExchangeModifyTable::GetTable** pour obtenir une table des règles.</span><span class="sxs-lookup"><span data-stu-id="879a3-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="879a3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879a3-125">See also</span></span>



[<span data-ttu-id="879a3-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="879a3-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="879a3-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="879a3-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

