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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787033"
---
# <a name="rowlist"></a><span data-ttu-id="9a73c-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="9a73c-103">ROWLIST</span></span>

  
  
<span data-ttu-id="9a73c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a73c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a73c-105">Contient un tableau de structures [ROWENTRY](rowentry.md) représentant les lignes et les opérations sont effectuées sur les lignes d’une table par le biais de l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="9a73c-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="9a73c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9a73c-106">Members</span></span>

 <span data-ttu-id="9a73c-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="9a73c-107">**cEntries**</span></span>
  
> <span data-ttu-id="9a73c-108">Nombre d’entrées dans le tableau spécifié par le membre **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="9a73c-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="9a73c-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="9a73c-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="9a73c-110">Tableau de structures **ROWENTRY** qui contient les lignes et les opérations sont effectuées sur les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="9a73c-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9a73c-111">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9a73c-111">MFCMAPI reference</span></span>

<span data-ttu-id="9a73c-112">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9a73c-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9a73c-113">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9a73c-113">**File**</span></span>|<span data-ttu-id="9a73c-114">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9a73c-114">**Function**</span></span>|<span data-ttu-id="9a73c-115">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9a73c-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a73c-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9a73c-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="9a73c-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="9a73c-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="9a73c-118">Permet de créer une liste de règles sélectionnées pour les actions suivantes **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="9a73c-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a73c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a73c-119">See also</span></span>



[<span data-ttu-id="9a73c-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="9a73c-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="9a73c-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a73c-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="9a73c-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9a73c-122">MAPI Structures</span></span>](mapi-structures.md)

