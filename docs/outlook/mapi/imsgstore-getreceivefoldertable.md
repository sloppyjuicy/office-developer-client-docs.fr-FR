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
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784264"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="9c41a-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="9c41a-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="9c41a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c41a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c41a-105">Permet d’accéder à la table de dossier de réception, une table qui consacrée des informations sur tous les dossiers de réception de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="9c41a-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="9c41a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="9c41a-106">Parameters</span></span>

 <span data-ttu-id="9c41a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c41a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9c41a-108">[in] Masque de bits d’indicateurs que les contrôles de table access.</span><span class="sxs-lookup"><span data-stu-id="9c41a-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="9c41a-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="9c41a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9c41a-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9c41a-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9c41a-111">Permet de **GetReceiveFolderTable** renvoyer avec succès, éventuellement avant le tableau est entièrement disponible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9c41a-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="9c41a-112">Si le tableau n’est pas disponible, un appel de la table suivante peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="9c41a-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="9c41a-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c41a-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9c41a-114">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="9c41a-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9c41a-115">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="9c41a-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9c41a-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9c41a-116">_lppTable_</span></span>
  
> <span data-ttu-id="9c41a-117">[out] Pointeur vers un pointeur vers le tableau de dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="9c41a-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c41a-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9c41a-118">Return value</span></span>

<span data-ttu-id="9c41a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c41a-119">S_OK</span></span> 
  
> <span data-ttu-id="9c41a-120">Le tableau de dossier de réception a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="9c41a-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c41a-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c41a-121">Remarks</span></span>

<span data-ttu-id="9c41a-122">La méthode **IMsgStore::GetReceiveFolderTable** permet d’accéder à un tableau qui affiche que les paramètres de propriété pour tous les messages recevoir des dossiers.</span><span class="sxs-lookup"><span data-stu-id="9c41a-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9c41a-123">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="9c41a-123">Notes to implementers</span></span>

<span data-ttu-id="9c41a-124">Pour une liste de colonnes dans une table de dossier de réception, voir [S’afficher les Tables de dossier](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9c41a-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="9c41a-125">Mettre en œuvre votre recevoir des tables de dossier pour prendre en charge des restrictions de propriété de paramètre de la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9c41a-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="9c41a-126">Cette permet d’accéder facilement aux notamment recevoir des dossiers.</span><span class="sxs-lookup"><span data-stu-id="9c41a-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c41a-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9c41a-127">Notes to callers</span></span>

<span data-ttu-id="9c41a-128">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="9c41a-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="9c41a-129">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="9c41a-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c41a-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9c41a-130">MFCMAPI reference</span></span>

<span data-ttu-id="9c41a-131">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9c41a-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c41a-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9c41a-132">**File**</span></span>|<span data-ttu-id="9c41a-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9c41a-133">**Function**</span></span>|<span data-ttu-id="9c41a-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9c41a-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c41a-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9c41a-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9c41a-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="9c41a-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="9c41a-137">MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolderTable** pour obtenir la table de dossier de réception à afficher.</span><span class="sxs-lookup"><span data-stu-id="9c41a-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c41a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c41a-138">See also</span></span>



[<span data-ttu-id="9c41a-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="9c41a-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="9c41a-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="9c41a-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="9c41a-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="9c41a-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="9c41a-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="9c41a-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="9c41a-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9c41a-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="9c41a-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9c41a-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

