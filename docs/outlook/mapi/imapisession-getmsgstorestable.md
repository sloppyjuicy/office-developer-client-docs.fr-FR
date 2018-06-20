---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783922"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="46fdd-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="46fdd-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="46fdd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46fdd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46fdd-105">Permet d’accéder à la table de magasin de message qui contient des informations sur toutes les banques de messages dans le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="46fdd-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="46fdd-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="46fdd-106">Parameters</span></span>

 <span data-ttu-id="46fdd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="46fdd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="46fdd-108">[in] Masque de bits d’indicateurs qui détermine le format des colonnes sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="46fdd-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="46fdd-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="46fdd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="46fdd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46fdd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="46fdd-111">Les colonnes de type chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="46fdd-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="46fdd-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="46fdd-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="46fdd-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="46fdd-113">_lppTable_</span></span>
  
> <span data-ttu-id="46fdd-114">[out] Pointeur vers un pointeur vers la table.</span><span class="sxs-lookup"><span data-stu-id="46fdd-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46fdd-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="46fdd-115">Return value</span></span>

<span data-ttu-id="46fdd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="46fdd-116">S_OK</span></span> 
  
> <span data-ttu-id="46fdd-117">Le tableau a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="46fdd-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="46fdd-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="46fdd-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="46fdd-119">L’indicateur MAPI_UNICODE a été défini et que la session ne prend pas en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="46fdd-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46fdd-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="46fdd-120">Remarks</span></span>

<span data-ttu-id="46fdd-121">La méthode **IMAPISession::GetMsgStoresTable** récupère un pointeur vers la table, une table gérée par MAPI qui contient des informations sur chaque banque de messages ouverts dans le profil.</span><span class="sxs-lookup"><span data-stu-id="46fdd-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="46fdd-122">Pour obtenir la liste complète des colonnes obligatoires et facultatifs dans le message magasin table, voir les [Tables de stocker des messages](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="46fdd-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46fdd-123">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="46fdd-123">Notes to callers</span></span>

<span data-ttu-id="46fdd-124">Étant donné que MAPI met à jour la table de banque de messages pendant la session en cas de modification, appelez la méthode **Advise** de la table de magasin de message pour s’inscrire afin d’être averti de ces modifications.</span><span class="sxs-lookup"><span data-stu-id="46fdd-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="46fdd-125">Modifications possibles comprennent l’ajout de nouvelles banques de message, suppression existant stocke, remplace la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="46fdd-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="46fdd-126">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="46fdd-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="46fdd-127">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="46fdd-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="46fdd-128">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="46fdd-128">MFCMAPI reference</span></span>

<span data-ttu-id="46fdd-129">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46fdd-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="46fdd-130">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="46fdd-130">**File**</span></span>|<span data-ttu-id="46fdd-131">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="46fdd-131">**Function**</span></span>|<span data-ttu-id="46fdd-132">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="46fdd-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46fdd-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="46fdd-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="46fdd-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="46fdd-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="46fdd-135">MFCMAPI utilise la méthode **IMAPISession::GetMsgStoresTable** pour obtenir la table afin qu’il peut être affiché dans la boîte de dialogue de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="46fdd-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46fdd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46fdd-136">See also</span></span>



[<span data-ttu-id="46fdd-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="46fdd-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="46fdd-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46fdd-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="46fdd-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="46fdd-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="46fdd-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="46fdd-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="46fdd-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="46fdd-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="46fdd-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="46fdd-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="46fdd-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="46fdd-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="46fdd-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46fdd-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="46fdd-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="46fdd-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="46fdd-146">Tables de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="46fdd-146">Message Store Tables</span></span>](message-store-tables.md)

