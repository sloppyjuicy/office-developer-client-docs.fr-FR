---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419183"
---
# <a name="rowlist"></a><span data-ttu-id="aa2f9-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="aa2f9-103">ROWLIST</span></span>

  
  
<span data-ttu-id="aa2f9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa2f9-105">Contient un tableau de structures [ROWENTRY](rowentry.md) représentant des lignes et les opérations effectuées sur ces lignes dans un tableau via l’interface [IExchangeModifyTable.](iexchangemodifytableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="aa2f9-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="aa2f9-106">Members</span><span class="sxs-lookup"><span data-stu-id="aa2f9-106">Members</span></span>

 <span data-ttu-id="aa2f9-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-107">**cEntries**</span></span>
  
> <span data-ttu-id="aa2f9-108">Nombre d’entrées dans le tableau spécifié par **le membre aEntries.**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="aa2f9-109">**aEntries[MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="aa2f9-110">Tableau de structures **ROWENTRY** qui contient les lignes et les opérations effectuées sur ces lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="aa2f9-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa2f9-111">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aa2f9-111">MFCMAPI reference</span></span>

<span data-ttu-id="aa2f9-112">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aa2f9-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa2f9-113">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-113">**File**</span></span>|<span data-ttu-id="aa2f9-114">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-114">**Function**</span></span>|<span data-ttu-id="aa2f9-115">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa2f9-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aa2f9-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="aa2f9-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="aa2f9-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="aa2f9-118">Utilisé pour créer une liste de règles sélectionnées pour les actions **ModifyTable suivantes.**</span><span class="sxs-lookup"><span data-stu-id="aa2f9-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa2f9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa2f9-119">See also</span></span>



[<span data-ttu-id="aa2f9-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="aa2f9-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="aa2f9-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa2f9-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="aa2f9-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="aa2f9-122">MAPI Structures</span></span>](mapi-structures.md)

