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
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436243"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="284c0-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="284c0-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="284c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="284c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="284c0-105">Renvoie un pointeur vers une interface pour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="284c0-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="284c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="284c0-106">Parameters</span></span>

 <span data-ttu-id="284c0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="284c0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="284c0-108">[in] Réservé ; doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="284c0-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="284c0-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="284c0-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="284c0-110">Définit de nouveaux droits.</span><span class="sxs-lookup"><span data-stu-id="284c0-110">Sets new rights.</span></span>
    
<span data-ttu-id="284c0-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="284c0-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="284c0-112">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="284c0-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="284c0-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="284c0-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="284c0-114">Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple des nouveaux droits de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="284c0-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="284c0-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="284c0-115">_lppTable_</span></span>
  
> <span data-ttu-id="284c0-116">[out] Pointe vers une [interface IMAPITable : IUnknown](imapitableiunknown.md) contenant l’objet table.</span><span class="sxs-lookup"><span data-stu-id="284c0-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="284c0-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="284c0-117">MFCMAPI reference</span></span>

<span data-ttu-id="284c0-118">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="284c0-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="284c0-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="284c0-119">**File**</span></span>|<span data-ttu-id="284c0-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="284c0-120">**Function**</span></span>|<span data-ttu-id="284c0-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="284c0-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="284c0-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="284c0-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="284c0-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="284c0-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="284c0-124">MFCMAPI utilise la **méthode IExchangeModifyTable::GetTable** pour obtenir une table de règles.</span><span class="sxs-lookup"><span data-stu-id="284c0-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="284c0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="284c0-125">See also</span></span>



[<span data-ttu-id="284c0-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="284c0-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="284c0-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="284c0-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

