---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570834"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="31208-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="31208-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="31208-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31208-105">Retourne un pointeur vers le tableau unique de MAPI (une liste des modèles que tous les du carnet d’adresses fournisseurs de prise en charge pour la création de nouveaux destinataires).</span><span class="sxs-lookup"><span data-stu-id="31208-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="31208-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="31208-106">Parameters</span></span>

 <span data-ttu-id="31208-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31208-107">_ulFlags_</span></span>
  
> <span data-ttu-id="31208-108">[in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne.</span><span class="sxs-lookup"><span data-stu-id="31208-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="31208-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="31208-109">The following flag can be set:</span></span>
    
<span data-ttu-id="31208-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31208-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="31208-111">Les colonnes de type chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="31208-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="31208-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="31208-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="31208-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="31208-113">_lppTable_</span></span>
  
> <span data-ttu-id="31208-114">[out] Pointeur vers un pointeur vers la table unique.</span><span class="sxs-lookup"><span data-stu-id="31208-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31208-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31208-115">Return value</span></span>

<span data-ttu-id="31208-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="31208-116">S_OK</span></span> 
  
> <span data-ttu-id="31208-117">Le tableau unique a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="31208-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31208-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="31208-118">Remarks</span></span>

<span data-ttu-id="31208-119">La méthode **IMAPISupport::GetOneOffTable** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="31208-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="31208-120">Fournisseurs de carnet d’adresses appellent **GetOneOffTable** pour récupérer la liste complète des modèles pour la création de nouveaux destinataires.</span><span class="sxs-lookup"><span data-stu-id="31208-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="31208-121">Ce tableau inclut les modèles qui prennent en charge des fournisseurs de carnet d’adresses qui sont actifs dans la session, ainsi que des modèles prenant en charge MAPI.</span><span class="sxs-lookup"><span data-stu-id="31208-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="31208-122">Les destinataires nouvellement créés peuvent être utilisés pour adresser un message ou peuvent être ajoutés à un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="31208-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="31208-123">Pour obtenir la liste des propriétés qui composent la colonne requise définie dans les tableaux uniques, voir [Tables uniques](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="31208-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="31208-124">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="31208-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="31208-125">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="31208-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="31208-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="31208-126">Notes to callers</span></span>

<span data-ttu-id="31208-127">Si vous êtes inscrit pour recevoir les notifications des modifications apportées à cette table unique, vous recevrez les notifications des modifications apportées aux tables uniques des autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="31208-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="31208-128">En fonction de ces notifications, vous pouvez bénéficier de nouveaux types d’adresses qui sont ajoutés lors de la session en cours.</span><span class="sxs-lookup"><span data-stu-id="31208-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31208-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31208-129">See also</span></span>



[<span data-ttu-id="31208-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="31208-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="31208-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="31208-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="31208-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31208-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="31208-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="31208-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="31208-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="31208-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="31208-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="31208-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="31208-136">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="31208-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="31208-137">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31208-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="31208-138">Tables uniques</span><span class="sxs-lookup"><span data-stu-id="31208-138">One-Off Tables</span></span>](one-off-tables.md)

