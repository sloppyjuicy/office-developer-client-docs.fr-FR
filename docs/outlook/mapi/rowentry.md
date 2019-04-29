---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436033"
---
# <a name="rowentry"></a><span data-ttu-id="74f8b-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="74f8b-103">ROWENTRY</span></span>

<span data-ttu-id="74f8b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74f8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74f8b-105">Contient une ligne et l'opération exécutée sur cette ligne dans un tableau via l'interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="74f8b-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="74f8b-106">Members</span><span class="sxs-lookup"><span data-stu-id="74f8b-106">Members</span></span>

<span data-ttu-id="74f8b-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="74f8b-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="74f8b-108">Une des opérations suivantes à effectuer sur les données:</span><span class="sxs-lookup"><span data-stu-id="74f8b-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="74f8b-109">ROW_ADD: ajouter les données à la table en tant que nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="74f8b-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="74f8b-110">ROW_MODIFY: modifiez cette ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="74f8b-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="74f8b-111">ROW_REMOVE: supprimez cette ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="74f8b-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="74f8b-112">ROW_EMPTY: n'ajoutez pas les données de ligne à la table.</span><span class="sxs-lookup"><span data-stu-id="74f8b-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="74f8b-113">(La ligne est vide.)</span><span class="sxs-lookup"><span data-stu-id="74f8b-113">(The row is empty.)</span></span>
    
<span data-ttu-id="74f8b-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="74f8b-114">**cValues**</span></span>
  
> <span data-ttu-id="74f8b-115">Nombre de valeurs de propriété dans **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="74f8b-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="74f8b-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="74f8b-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="74f8b-117">Tableau de structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="74f8b-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="74f8b-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="74f8b-118">MFCMAPI reference</span></span>

<span data-ttu-id="74f8b-119">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="74f8b-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74f8b-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="74f8b-120">**File**</span></span>|<span data-ttu-id="74f8b-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="74f8b-121">**Function**</span></span>|<span data-ttu-id="74f8b-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="74f8b-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74f8b-123">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="74f8b-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="74f8b-124">CRulesDlg:: GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="74f8b-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="74f8b-125">Permet de créer une liste de règles sélectionnées pour les actions **ModifyTable** suivantes.</span><span class="sxs-lookup"><span data-stu-id="74f8b-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74f8b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74f8b-126">See also</span></span>
  
- [<span data-ttu-id="74f8b-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74f8b-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="74f8b-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="74f8b-128">MAPI Structures</span></span>](mapi-structures.md)

