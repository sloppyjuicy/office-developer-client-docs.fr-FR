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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407136"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="67625-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="67625-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="67625-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67625-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67625-105">Fournit l'accès à la table d'État, un tableau qui contient des informations sur toutes les ressources MAPI de la session.</span><span class="sxs-lookup"><span data-stu-id="67625-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="67625-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67625-106">Parameters</span></span>

 <span data-ttu-id="67625-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67625-107">_ulFlags_</span></span>
  
> <span data-ttu-id="67625-108">dans Masque de réfixe des indicateurs qui déterminent le format des colonnes qui sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="67625-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="67625-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="67625-109">The following flag can be set:</span></span>
    
<span data-ttu-id="67625-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67625-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="67625-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="67625-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="67625-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="67625-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="67625-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="67625-113">_lppTable_</span></span>
  
> <span data-ttu-id="67625-114">remarquer Pointeur vers un pointeur vers la table d'État.</span><span class="sxs-lookup"><span data-stu-id="67625-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67625-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67625-115">Return value</span></span>

<span data-ttu-id="67625-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="67625-116">S_OK</span></span> 
  
> <span data-ttu-id="67625-117">La table a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="67625-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67625-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="67625-118">Remarks</span></span>

<span data-ttu-id="67625-119">La méthode **IMAPISession:: GetStatusTable** fournit l'accès à la table d'État qui contient des informations sur toutes les ressources MAPI de la session.</span><span class="sxs-lookup"><span data-stu-id="67625-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="67625-120">Il y a une ligne dans le tableau pour obtenir des informations sur le sous-système MAPI, une ligne pour le spouleur MAPI, une ligne pour le carnet d'adresses intégré et une ligne pour chaque fournisseur de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="67625-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="67625-121">Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table d'État, reportez-vous à la rubrique [Status tables](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="67625-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="67625-122">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="67625-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="67625-123">Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="67625-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="67625-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="67625-124">MFCMAPI reference</span></span>

<span data-ttu-id="67625-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="67625-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="67625-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="67625-126">**File**</span></span>|<span data-ttu-id="67625-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="67625-127">**Function**</span></span>|<span data-ttu-id="67625-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="67625-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="67625-129">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="67625-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="67625-130">CMainDlg:: OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="67625-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="67625-131">MFCMAPI utilise la méthode **IMAPISession:: GetStatusTable** pour obtenir la table d'État à afficher.</span><span class="sxs-lookup"><span data-stu-id="67625-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67625-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67625-132">See also</span></span>



[<span data-ttu-id="67625-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67625-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="67625-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="67625-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="67625-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="67625-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="67625-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="67625-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="67625-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="67625-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="67625-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="67625-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="67625-139">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67625-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="67625-140">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="67625-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="67625-141">Tables d'État</span><span class="sxs-lookup"><span data-stu-id="67625-141">Status Tables</span></span>](status-tables.md)

