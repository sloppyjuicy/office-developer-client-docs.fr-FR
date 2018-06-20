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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787035"
---
# <a name="rowentry"></a><span data-ttu-id="7d630-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="7d630-103">ROWENTRY</span></span>

<span data-ttu-id="7d630-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d630-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d630-105">Contient une ligne et l’opération est effectuée sur la ligne dans une table par le biais de l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7d630-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="7d630-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7d630-106">Members</span></span>

<span data-ttu-id="7d630-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="7d630-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="7d630-108">Une des opérations à effectuer sur les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d630-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="7d630-109">ROW_ADD : Ajoutez les données dans le tableau en tant qu’une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="7d630-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="7d630-110">ROW_MODIFY : Modifiez cette ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7d630-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="7d630-111">ROW_REMOVE : Supprimer cette ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="7d630-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="7d630-112">ROW_EMPTY : N’ajoutez pas les données de ligne à la table.</span><span class="sxs-lookup"><span data-stu-id="7d630-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="7d630-113">(La ligne est vide).</span><span class="sxs-lookup"><span data-stu-id="7d630-113">(The row is empty.)</span></span>
    
<span data-ttu-id="7d630-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7d630-114">**cValues**</span></span>
  
> <span data-ttu-id="7d630-115">Le nombre de valeurs de propriété dans **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="7d630-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="7d630-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="7d630-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="7d630-117">Tableau des structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7d630-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d630-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7d630-118">MFCMAPI reference</span></span>

<span data-ttu-id="7d630-119">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7d630-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d630-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="7d630-120">**File**</span></span>|<span data-ttu-id="7d630-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="7d630-121">**Function**</span></span>|<span data-ttu-id="7d630-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="7d630-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d630-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7d630-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="7d630-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="7d630-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="7d630-125">Permet de créer une liste de règles sélectionnées pour les actions suivantes **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="7d630-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d630-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d630-126">See also</span></span>
  
- [<span data-ttu-id="7d630-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d630-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="7d630-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="7d630-128">MAPI Structures</span></span>](mapi-structures.md)

