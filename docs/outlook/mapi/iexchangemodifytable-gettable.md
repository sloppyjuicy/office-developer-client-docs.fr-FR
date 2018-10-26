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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578989"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="3597a-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="3597a-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="3597a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3597a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3597a-105">Retourne un pointeur vers une interface pour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3597a-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="3597a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3597a-106">Parameters</span></span>

 <span data-ttu-id="3597a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3597a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3597a-108">[in] Réservé ; doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="3597a-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="3597a-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="3597a-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="3597a-110">Définit les nouveaux droits.</span><span class="sxs-lookup"><span data-stu-id="3597a-110">Sets new rights.</span></span>
    
<span data-ttu-id="3597a-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="3597a-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="3597a-112">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="3597a-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="3597a-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="3597a-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="3597a-114">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple de nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="3597a-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="3597a-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="3597a-115">_lppTable_</span></span>
  
> <span data-ttu-id="3597a-116">[out] Pointe vers une [IMAPITable : IUnknown](imapitableiunknown.md) interface contenant l’objet table.</span><span class="sxs-lookup"><span data-stu-id="3597a-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3597a-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3597a-117">MFCMAPI reference</span></span>

<span data-ttu-id="3597a-118">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3597a-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3597a-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3597a-119">**File**</span></span>|<span data-ttu-id="3597a-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3597a-120">**Function**</span></span>|<span data-ttu-id="3597a-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3597a-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3597a-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3597a-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="3597a-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="3597a-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="3597a-124">MFCMAPI utilise la méthode **IExchangeModifyTable::GetTable** pour obtenir une table des règles.</span><span class="sxs-lookup"><span data-stu-id="3597a-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3597a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3597a-125">See also</span></span>



[<span data-ttu-id="3597a-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3597a-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="3597a-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3597a-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

