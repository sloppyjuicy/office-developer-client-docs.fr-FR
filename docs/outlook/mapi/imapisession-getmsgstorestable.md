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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428136"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="eb940-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="eb940-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="eb940-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb940-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb940-105">Fournit l'accès à la table de banque de messages qui contient des informations sur toutes les banques de messages dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="eb940-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="eb940-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb940-106">Parameters</span></span>

 <span data-ttu-id="eb940-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb940-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eb940-108">dans Masque de réfixe des indicateurs qui déterminent le format des colonnes qui sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="eb940-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="eb940-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="eb940-109">The following flag can be set:</span></span>
    
<span data-ttu-id="eb940-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb940-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eb940-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb940-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="eb940-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="eb940-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="eb940-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="eb940-113">_lppTable_</span></span>
  
> <span data-ttu-id="eb940-114">remarquer Pointeur vers un pointeur vers la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="eb940-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb940-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb940-115">Return value</span></span>

<span data-ttu-id="eb940-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb940-116">S_OK</span></span> 
  
> <span data-ttu-id="eb940-117">La table a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="eb940-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="eb940-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="eb940-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="eb940-119">L'indicateur MAPI_UNICODE a été défini et la session ne prend pas en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb940-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb940-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb940-120">Remarks</span></span>

<span data-ttu-id="eb940-121">La méthode **IMAPISession:: GetMsgStoresTable** extrait un pointeur vers la table de banque de messages, une table gérée par MAPI qui contient des informations sur chaque banque de messages ouverte dans le profil.</span><span class="sxs-lookup"><span data-stu-id="eb940-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="eb940-122">Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table de banque de messages, consultez la rubrique [tables des banques de messages](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="eb940-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb940-123">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="eb940-123">Notes to callers</span></span>

<span data-ttu-id="eb940-124">Dans la mesure où MAPI met à jour la table de banque de messages pendant la session lorsque \*\*\*\* des modifications ont lieu, appelez la méthode Advise de la table de banque de messages pour vous inscrire afin d'être informé de ces modifications.</span><span class="sxs-lookup"><span data-stu-id="eb940-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="eb940-125">Les modifications possibles incluent l'ajout de nouvelles banques de messages, la suppression de magasins existants et les modifications apportées à la Banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="eb940-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="eb940-126">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="eb940-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="eb940-127">Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="eb940-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eb940-128">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="eb940-128">MFCMAPI reference</span></span>

<span data-ttu-id="eb940-129">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="eb940-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eb940-130">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="eb940-130">**File**</span></span>|<span data-ttu-id="eb940-131">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="eb940-131">**Function**</span></span>|<span data-ttu-id="eb940-132">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="eb940-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb940-133">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="eb940-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="eb940-134">CMainDlg:: OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="eb940-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="eb940-135">MFCMAPI utilise la méthode **IMAPISession:: GetMsgStoresTable** pour obtenir la table de banque de messages afin qu'elle puisse être affichée dans la boîte de dialogue principale de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="eb940-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb940-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb940-136">See also</span></span>



[<span data-ttu-id="eb940-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="eb940-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="eb940-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb940-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="eb940-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="eb940-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="eb940-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="eb940-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="eb940-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="eb940-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="eb940-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="eb940-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="eb940-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="eb940-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="eb940-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb940-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="eb940-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="eb940-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="eb940-146">Tables de banque de messages</span><span class="sxs-lookup"><span data-stu-id="eb940-146">Message Store Tables</span></span>](message-store-tables.md)

