---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7de404f421a405d80dd7f98beba5168969222fc9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783937"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="73c82-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="73c82-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="73c82-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73c82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73c82-105">Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI dans la session.</span><span class="sxs-lookup"><span data-stu-id="73c82-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="73c82-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="73c82-106">Parameters</span></span>

 <span data-ttu-id="73c82-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73c82-107">_ulFlags_</span></span>
  
> <span data-ttu-id="73c82-108">[in] Masque de bits d’indicateurs qui détermine le format des colonnes sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="73c82-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="73c82-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="73c82-109">The following flag can be set:</span></span>
    
<span data-ttu-id="73c82-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="73c82-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="73c82-111">Les colonnes de type chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="73c82-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="73c82-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="73c82-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="73c82-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="73c82-113">_lppTable_</span></span>
  
> <span data-ttu-id="73c82-114">[out] Pointeur vers un pointeur vers la table d’état.</span><span class="sxs-lookup"><span data-stu-id="73c82-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73c82-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="73c82-115">Return value</span></span>

<span data-ttu-id="73c82-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="73c82-116">S_OK</span></span> 
  
> <span data-ttu-id="73c82-117">Le tableau a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="73c82-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73c82-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="73c82-118">Remarks</span></span>

<span data-ttu-id="73c82-119">La méthode **IMAPISession::GetStatusTable** permet d’accéder à la table d’état qui contient des informations sur toutes les ressources MAPI dans la session.</span><span class="sxs-lookup"><span data-stu-id="73c82-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="73c82-120">Il y a une ligne dans le tableau pour plus d’informations sur le sous-système MAPI, une ligne pour le spouleur MAPI, une ligne pour le carnet d’adresses intégré et une ligne pour chaque fournisseur de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="73c82-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="73c82-121">Pour obtenir une liste complète des colonnes obligatoires et facultatifs dans la table d’état, voir [Tableaux d’état](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="73c82-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="73c82-122">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="73c82-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="73c82-123">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="73c82-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73c82-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="73c82-124">MFCMAPI reference</span></span>

<span data-ttu-id="73c82-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="73c82-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73c82-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="73c82-126">**File**</span></span>|<span data-ttu-id="73c82-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="73c82-127">**Function**</span></span>|<span data-ttu-id="73c82-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="73c82-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73c82-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="73c82-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="73c82-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="73c82-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="73c82-131">MFCMAPI utilise la méthode **IMAPISession::GetStatusTable** pour obtenir la table d’état à afficher.</span><span class="sxs-lookup"><span data-stu-id="73c82-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73c82-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c82-132">See also</span></span>



[<span data-ttu-id="73c82-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73c82-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="73c82-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="73c82-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="73c82-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="73c82-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="73c82-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="73c82-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="73c82-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="73c82-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="73c82-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="73c82-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="73c82-139">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73c82-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="73c82-140">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="73c82-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="73c82-141">Tableaux d’état</span><span class="sxs-lookup"><span data-stu-id="73c82-141">Status Tables</span></span>](status-tables.md)

