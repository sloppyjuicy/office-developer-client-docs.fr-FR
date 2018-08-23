---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565906"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="15c82-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="15c82-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="15c82-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15c82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15c82-105">Met à jour un objet de table MAPI.</span><span class="sxs-lookup"><span data-stu-id="15c82-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="15c82-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="15c82-106">Parameters</span></span>

 <span data-ttu-id="15c82-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15c82-107">_ulFlags_</span></span>
  
> <span data-ttu-id="15c82-108">[in] Utilisez une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="15c82-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="15c82-109">0 (zéro)</span><span class="sxs-lookup"><span data-stu-id="15c82-109">0 (zero)</span></span>
  
> <span data-ttu-id="15c82-110">Utilisez la valeur du membre de la structure [ROWENTRY](rowentry.md) **ulRowFlags** .</span><span class="sxs-lookup"><span data-stu-id="15c82-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="15c82-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="15c82-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="15c82-112">Définit les nouveaux droits.</span><span class="sxs-lookup"><span data-stu-id="15c82-112">Sets new rights.</span></span>
    
<span data-ttu-id="15c82-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="15c82-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="15c82-114">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="15c82-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="15c82-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="15c82-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="15c82-116">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple de nouveaux droits et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="15c82-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="15c82-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="15c82-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="15c82-118">Remplacer toutes les lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="15c82-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="15c82-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="15c82-119">_lpMods_</span></span>
  
> <span data-ttu-id="15c82-120">[in] Pointe vers une structure [ROWLIST](rowlist.md) contenant les propriétés de l’objet table.</span><span class="sxs-lookup"><span data-stu-id="15c82-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="15c82-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="15c82-121">MFCMAPI reference</span></span>

<span data-ttu-id="15c82-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15c82-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="15c82-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="15c82-123">**File**</span></span>|<span data-ttu-id="15c82-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="15c82-124">**Function**</span></span>|<span data-ttu-id="15c82-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="15c82-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="15c82-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="15c82-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="15c82-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="15c82-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="15c82-128">MFCMAPI utilise la méthode **IExchangeModifyTable::ModifyTable** pour écrire une règle modifiée dans la table des règles.</span><span class="sxs-lookup"><span data-stu-id="15c82-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15c82-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15c82-129">See also</span></span>



[<span data-ttu-id="15c82-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15c82-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="15c82-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="15c82-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="15c82-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="15c82-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="15c82-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="15c82-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

