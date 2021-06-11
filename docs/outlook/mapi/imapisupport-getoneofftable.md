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
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412757"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="eab94-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="eab94-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="eab94-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eab94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eab94-105">Renvoie un pointeur vers le tableau unique MAPI (liste de modèles que tous les fournisseurs de carnet d’adresses peuvent prendre en charge pour la création de destinataires).</span><span class="sxs-lookup"><span data-stu-id="eab94-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="eab94-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="eab94-106">Parameters</span></span>

 <span data-ttu-id="eab94-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eab94-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eab94-108">[in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne.</span><span class="sxs-lookup"><span data-stu-id="eab94-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="eab94-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="eab94-109">The following flag can be set:</span></span>
    
<span data-ttu-id="eab94-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eab94-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eab94-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="eab94-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="eab94-112">Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="eab94-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="eab94-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="eab94-113">_lppTable_</span></span>
  
> <span data-ttu-id="eab94-114">[out] Pointeur vers un pointeur vers le tableau one-off.</span><span class="sxs-lookup"><span data-stu-id="eab94-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eab94-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eab94-115">Return value</span></span>

<span data-ttu-id="eab94-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="eab94-116">S_OK</span></span> 
  
> <span data-ttu-id="eab94-117">La table a été récupérée avec succès.</span><span class="sxs-lookup"><span data-stu-id="eab94-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eab94-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="eab94-118">Remarks</span></span>

<span data-ttu-id="eab94-119">La **méthode IMAPISupport::GetOneOffTable** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="eab94-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="eab94-120">Les fournisseurs de carnet d’adresses **appellent GetOneOffTable** pour récupérer la liste complète des modèles de création de destinataires.</span><span class="sxs-lookup"><span data-stu-id="eab94-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="eab94-121">Ce tableau inclut des modèles qui sont des fournisseurs de carnet d’adresses qui sont actifs dans la prise en charge de session, ainsi que des modèles que MAPI prend en charge.</span><span class="sxs-lookup"><span data-stu-id="eab94-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="eab94-122">Les destinataires nouvellement créés peuvent être utilisés pour adresser un message ou peuvent être ajoutés à un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="eab94-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="eab94-123">Pour obtenir la liste des propriétés qui font partie de la colonne requise définie dans des tables uniques, voir [Tables uniques.](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="eab94-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="eab94-124">La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="eab94-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="eab94-125">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="eab94-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eab94-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="eab94-126">Notes to callers</span></span>

<span data-ttu-id="eab94-127">Si vous êtes inscrit pour recevoir des notifications de modifications apportées à ce tableau one-off, vous recevrez également des notifications de modifications apportées aux tables one-off d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="eab94-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="eab94-128">En fonction de ces notifications, vous pouvez prendre en charge les nouveaux types d’adresses ajoutés au cours de la session en cours.</span><span class="sxs-lookup"><span data-stu-id="eab94-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eab94-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eab94-129">See also</span></span>



[<span data-ttu-id="eab94-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="eab94-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="eab94-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="eab94-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="eab94-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eab94-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="eab94-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="eab94-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="eab94-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="eab94-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="eab94-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="eab94-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="eab94-136">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="eab94-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="eab94-137">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eab94-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="eab94-138">One-Off Tables</span><span class="sxs-lookup"><span data-stu-id="eab94-138">One-Off Tables</span></span>](one-off-tables.md)

