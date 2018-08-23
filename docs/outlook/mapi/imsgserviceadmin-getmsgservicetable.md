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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5d8e91490cc39c3f259d35a923bb3bcbb2bf6011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568167"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="b4210-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="b4210-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="b4210-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4210-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4210-105">Permet d’accéder à la table de service de message, une liste des services dans le profil de message.</span><span class="sxs-lookup"><span data-stu-id="b4210-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="b4210-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="b4210-106">Parameters</span></span>

 <span data-ttu-id="b4210-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4210-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b4210-108">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="b4210-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="b4210-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b4210-109">_lppTable_</span></span>
  
> <span data-ttu-id="b4210-110">[out] Pointeur vers un pointeur vers le tableau de service de message.</span><span class="sxs-lookup"><span data-stu-id="b4210-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4210-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b4210-111">Return value</span></span>

<span data-ttu-id="b4210-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4210-112">S_OK</span></span> 
  
> <span data-ttu-id="b4210-113">Le tableau de service de message a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="b4210-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4210-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4210-114">Remarks</span></span>

<span data-ttu-id="b4210-115">La méthode **IMsgServiceAdmin::GetMsgServiceTable** permet d’accéder à la table de service de message, une table qui gère MAPI qui répertorie les services de message actuellement installées dans le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="b4210-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="b4210-116">Pour obtenir une liste complète des colonnes de la table de service de message, voir le [Tableau de Service de Message](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b4210-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="b4210-117">Le tableau de service de message est statique.</span><span class="sxs-lookup"><span data-stu-id="b4210-117">The message service table is static.</span></span> <span data-ttu-id="b4210-118">Une fois un client est autorisé à accéder à celui-ci, ajouts de service de message qui s’affiche et les suppressions n’affectent pas son.</span><span class="sxs-lookup"><span data-stu-id="b4210-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="b4210-119">S’il n’y a aucun message les services dans le profil actuel, **GetMsgServiceTable** renvoie un tableau avec des lignes de zéro.</span><span class="sxs-lookup"><span data-stu-id="b4210-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b4210-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b4210-120">MFCMAPI reference</span></span>

<span data-ttu-id="b4210-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b4210-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b4210-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b4210-122">**File**</span></span>|<span data-ttu-id="b4210-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b4210-123">**Function**</span></span>|<span data-ttu-id="b4210-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b4210-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4210-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b4210-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="b4210-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="b4210-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="b4210-127">MFCMAPI utilise la méthode **IMsgServiceAdmin::GetMsgServiceTable** pour charger le tableau des services dans un profil à afficher dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b4210-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4210-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4210-128">See also</span></span>



[<span data-ttu-id="b4210-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="b4210-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="b4210-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="b4210-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="b4210-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4210-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="b4210-132">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b4210-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

