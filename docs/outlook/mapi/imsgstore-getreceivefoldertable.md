---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317352"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="8e2ca-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="8e2ca-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="8e2ca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e2ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e2ca-105">Fournit l'accès à la table de dossiers de réception, un tableau qui contient des informations sur tous les dossiers de réception pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="8e2ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e2ca-106">Parameters</span></span>

 <span data-ttu-id="8e2ca-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e2ca-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8e2ca-108">dans Masque de des indicateurs qui contrôle l'accès aux tableaux.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="8e2ca-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="8e2ca-109">The following flags can be set:</span></span>
    
<span data-ttu-id="8e2ca-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8e2ca-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8e2ca-111">Permet à **GetReceiveFolderTable** de renvoyer correctement, éventuellement avant que la table soit entièrement disponible pour l'appelant.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="8e2ca-112">Si la table n'est pas entièrement disponible, un appel de tableau ultérieur peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="8e2ca-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e2ca-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8e2ca-114">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="8e2ca-115">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8e2ca-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8e2ca-116">_lppTable_</span></span>
  
> <span data-ttu-id="8e2ca-117">remarquer Pointeur vers un pointeur vers le tableau de dossiers de réception.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e2ca-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e2ca-118">Return value</span></span>

<span data-ttu-id="8e2ca-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e2ca-119">S_OK</span></span> 
  
> <span data-ttu-id="8e2ca-120">La table de dossiers de réception a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e2ca-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e2ca-121">Remarks</span></span>

<span data-ttu-id="8e2ca-122">La méthode **IMsgStore:: GetReceiveFolderTable** fournit l'accès à un tableau qui présente les paramètres de propriété de tous les dossiers de réception de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8e2ca-123">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8e2ca-123">Notes to implementers</span></span>

<span data-ttu-id="8e2ca-124">Pour obtenir la liste des colonnes requises dans une table de dossiers de réception, consultez la rubrique [Receive Folder tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ca-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="8e2ca-125">Implémentez vos tables de dossiers de réception pour prendre en charge la définition de restrictions de propriété sur la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e2ca-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="8e2ca-126">Cela permet d'accéder facilement à des dossiers de réception spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e2ca-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8e2ca-127">Notes to callers</span></span>

<span data-ttu-id="8e2ca-128">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ca-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="8e2ca-129">Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ca-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e2ca-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8e2ca-130">MFCMAPI reference</span></span>

<span data-ttu-id="8e2ca-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e2ca-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8e2ca-132">**File**</span></span>|<span data-ttu-id="8e2ca-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8e2ca-133">**Function**</span></span>|<span data-ttu-id="8e2ca-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8e2ca-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e2ca-135">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8e2ca-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="8e2ca-136">CMsgStoreDlg:: OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="8e2ca-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="8e2ca-137">MFCMAPI utilise la méthode **IMsgStore:: GetReceiveFolderTable** pour obtenir la table de dossiers de réception à afficher.</span><span class="sxs-lookup"><span data-stu-id="8e2ca-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e2ca-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e2ca-138">See also</span></span>



[<span data-ttu-id="8e2ca-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="8e2ca-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="8e2ca-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8e2ca-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="8e2ca-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="8e2ca-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="8e2ca-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8e2ca-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8e2ca-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e2ca-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8e2ca-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8e2ca-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

