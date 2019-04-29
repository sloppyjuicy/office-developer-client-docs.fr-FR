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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418175"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="92bd5-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="92bd5-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="92bd5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92bd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92bd5-105">Met à jour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="92bd5-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="92bd5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92bd5-106">Parameters</span></span>

 <span data-ttu-id="92bd5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92bd5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="92bd5-108">dans Utilisez l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="92bd5-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="92bd5-109">0 (zéro)</span><span class="sxs-lookup"><span data-stu-id="92bd5-109">0 (zero)</span></span>
  
> <span data-ttu-id="92bd5-110">Utilisez la valeur du membre **ulRowFlags** de la structure [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="92bd5-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="92bd5-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="92bd5-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="92bd5-112">Définit de nouveaux droits.</span><span class="sxs-lookup"><span data-stu-id="92bd5-112">Sets new rights.</span></span>
    
<span data-ttu-id="92bd5-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="92bd5-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="92bd5-114">Lorsque ACLTABLE_FREEBUSY est transmis, fournit un affichage détaillé des nouveaux droits de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="92bd5-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="92bd5-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="92bd5-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="92bd5-116">Lorsque ACLTABLE_FREEBUSY est transmis, fournit un affichage simple des nouveaux droits de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="92bd5-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="92bd5-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="92bd5-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="92bd5-118">Remplacez toutes les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="92bd5-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="92bd5-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="92bd5-119">_lpMods_</span></span>
  
> <span data-ttu-id="92bd5-120">dans Pointe vers une structure [ROWLIST](rowlist.md) contenant les propriétés de l'objet table.</span><span class="sxs-lookup"><span data-stu-id="92bd5-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="92bd5-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="92bd5-121">MFCMAPI reference</span></span>

<span data-ttu-id="92bd5-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="92bd5-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="92bd5-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="92bd5-123">**File**</span></span>|<span data-ttu-id="92bd5-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="92bd5-124">**Function**</span></span>|<span data-ttu-id="92bd5-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="92bd5-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92bd5-126">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="92bd5-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="92bd5-127">CRulesDlg:: OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="92bd5-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="92bd5-128">MFCMAPI utilise la méthode **IExchangeModifyTable:: ModifyTable** pour réécrire une règle modifiée dans la table de règles.</span><span class="sxs-lookup"><span data-stu-id="92bd5-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92bd5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92bd5-129">See also</span></span>



[<span data-ttu-id="92bd5-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92bd5-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="92bd5-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="92bd5-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="92bd5-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="92bd5-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="92bd5-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="92bd5-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

