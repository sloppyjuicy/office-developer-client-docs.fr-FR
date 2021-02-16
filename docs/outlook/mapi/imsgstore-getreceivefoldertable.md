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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421353"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="784cf-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="784cf-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="784cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="784cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="784cf-105">Permet d’accéder à la table des dossiers de réception, une table qui inclut des informations sur tous les dossiers de réception de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="784cf-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="784cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="784cf-106">Parameters</span></span>

 <span data-ttu-id="784cf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="784cf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="784cf-108">[in] Masque de bits d’indicateurs qui contrôle l’accès à la table.</span><span class="sxs-lookup"><span data-stu-id="784cf-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="784cf-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="784cf-109">The following flags can be set:</span></span>
    
<span data-ttu-id="784cf-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="784cf-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="784cf-111">Permet à **GetReceiveFolderTable** de renvoyer correctement, éventuellement avant que la table soit entièrement disponible pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="784cf-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="784cf-112">Si la table n’est pas entièrement disponible, la réalisation d’un appel de table ultérieur peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="784cf-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="784cf-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="784cf-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="784cf-114">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="784cf-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="784cf-115">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="784cf-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="784cf-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="784cf-116">_lppTable_</span></span>
  
> <span data-ttu-id="784cf-117">[out] Pointeur vers un pointeur vers le tableau du dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="784cf-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="784cf-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="784cf-118">Return value</span></span>

<span data-ttu-id="784cf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="784cf-119">S_OK</span></span> 
  
> <span data-ttu-id="784cf-120">La table des dossiers de réception a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="784cf-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="784cf-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="784cf-121">Remarks</span></span>

<span data-ttu-id="784cf-122">La **méthode IMsgStore::GetReceiveFolderTable** permet d’accéder à une table qui indique les paramètres de propriété pour tous les dossiers de réception de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="784cf-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="784cf-123">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="784cf-123">Notes to implementers</span></span>

<span data-ttu-id="784cf-124">Pour obtenir la liste des colonnes requises dans une table de dossiers de réception, voir [Tables des dossiers de réception.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="784cf-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="784cf-125">Implémentez vos tables de dossiers de réception pour prendre en charge la définition de restrictions de propriété sur **la PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="784cf-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="784cf-126">Cela permet d’accéder facilement à des dossiers de réception particuliers.</span><span class="sxs-lookup"><span data-stu-id="784cf-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="784cf-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="784cf-127">Notes to callers</span></span>

<span data-ttu-id="784cf-128">La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="784cf-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="784cf-129">Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="784cf-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="784cf-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="784cf-130">MFCMAPI reference</span></span>

<span data-ttu-id="784cf-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="784cf-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="784cf-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="784cf-132">**File**</span></span>|<span data-ttu-id="784cf-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="784cf-133">**Function**</span></span>|<span data-ttu-id="784cf-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="784cf-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="784cf-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="784cf-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="784cf-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="784cf-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="784cf-137">MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolderTable** pour obtenir la table des dossiers de réception à afficher.</span><span class="sxs-lookup"><span data-stu-id="784cf-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="784cf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="784cf-138">See also</span></span>



[<span data-ttu-id="784cf-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="784cf-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="784cf-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="784cf-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="784cf-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="784cf-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="784cf-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="784cf-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="784cf-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="784cf-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="784cf-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="784cf-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

