---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410475"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="38a32-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="38a32-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="38a32-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38a32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38a32-105">Permet d’accéder à la table des services de message, une liste des services de message dans le profil.</span><span class="sxs-lookup"><span data-stu-id="38a32-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="38a32-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="38a32-106">Parameters</span></span>

 <span data-ttu-id="38a32-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38a32-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38a32-108">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="38a32-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="38a32-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="38a32-109">_lppTable_</span></span>
  
> <span data-ttu-id="38a32-110">[out] Pointeur vers un pointeur vers le tableau du service de message.</span><span class="sxs-lookup"><span data-stu-id="38a32-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38a32-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38a32-111">Return value</span></span>

<span data-ttu-id="38a32-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="38a32-112">S_OK</span></span> 
  
> <span data-ttu-id="38a32-113">La table de service de message a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="38a32-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38a32-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="38a32-114">Remarks</span></span>

<span data-ttu-id="38a32-115">La méthode **IMsgServiceAdmin::GetMsgServiceTable** permet d’accéder à la table de service de message, une table que MAPI tient à jour et qui répertorie les services de message actuellement installés dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="38a32-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="38a32-116">Pour obtenir la liste complète des colonnes dans le tableau des services de messages, consultez la [table Service de messages.](message-service-tables.md)</span><span class="sxs-lookup"><span data-stu-id="38a32-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="38a32-117">La table de service de message est statique.</span><span class="sxs-lookup"><span data-stu-id="38a32-117">The message service table is static.</span></span> <span data-ttu-id="38a32-118">Une fois qu’un client a été autorisé à y accéder, les ajouts ou suppressions de service de message suivants ne l’affecteront pas.</span><span class="sxs-lookup"><span data-stu-id="38a32-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="38a32-119">S’il n’existe aucun service de message dans le profil actuel, **GetMsgServiceTable renvoie** un tableau avec zéro ligne.</span><span class="sxs-lookup"><span data-stu-id="38a32-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38a32-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38a32-120">MFCMAPI reference</span></span>

<span data-ttu-id="38a32-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38a32-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38a32-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="38a32-122">**File**</span></span>|<span data-ttu-id="38a32-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="38a32-123">**Function**</span></span>|<span data-ttu-id="38a32-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="38a32-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38a32-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="38a32-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="38a32-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="38a32-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="38a32-127">MFCMAPI utilise la méthode **IMsgServiceAdmin::GetMsgServiceTable** pour charger la table des services dans un profil à afficher dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="38a32-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38a32-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38a32-128">See also</span></span>



[<span data-ttu-id="38a32-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="38a32-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="38a32-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="38a32-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="38a32-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38a32-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="38a32-132">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="38a32-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

