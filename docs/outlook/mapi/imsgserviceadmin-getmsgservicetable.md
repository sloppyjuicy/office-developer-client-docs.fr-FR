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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309974"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="1ebb1-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="1ebb1-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="1ebb1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ebb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ebb1-105">Fournit l'accès à la table de service de messagerie, une liste des services de messagerie dans le profil.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1ebb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ebb1-106">Parameters</span></span>

 <span data-ttu-id="1ebb1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ebb1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1ebb1-108">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="1ebb1-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1ebb1-109">_lppTable_</span></span>
  
> <span data-ttu-id="1ebb1-110">remarquer Pointeur vers un pointeur vers la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ebb1-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ebb1-111">Return value</span></span>

<span data-ttu-id="1ebb1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ebb1-112">S_OK</span></span> 
  
> <span data-ttu-id="1ebb1-113">La table de service de message a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ebb1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ebb1-114">Remarks</span></span>

<span data-ttu-id="1ebb1-115">La méthode **IMsgServiceAdmin:: GetMsgServiceTable** donne accès à la table des services de messagerie, une table gérée par MAPI, qui répertorie les services de messagerie actuellement installés dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="1ebb1-116">Pour obtenir la liste complète des colonnes de la table des services de messagerie, consultez la rubrique [message service table](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1ebb1-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="1ebb1-117">La table des services de messagerie est statique.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-117">The message service table is static.</span></span> <span data-ttu-id="1ebb1-118">Une fois qu'un client a reçu l'accès à celui-ci, les ajouts ou suppressions de service de message suivants ne l'affectent pas.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="1ebb1-119">S'il n'y a pas de services de messagerie dans le profil actif, **GetMsgServiceTable** renvoie un tableau sans aucune ligne.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ebb1-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ebb1-120">MFCMAPI reference</span></span>

<span data-ttu-id="1ebb1-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ebb1-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1ebb1-122">**File**</span></span>|<span data-ttu-id="1ebb1-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1ebb1-123">**Function**</span></span>|<span data-ttu-id="1ebb1-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1ebb1-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ebb1-125">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="1ebb1-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="1ebb1-126">CMsgServiceTableDlg:: OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="1ebb1-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="1ebb1-127">MFCMAPI utilise la méthode **IMsgServiceAdmin:: GetMsgServiceTable** pour charger la table des services dans un profil à afficher dans la vue.</span><span class="sxs-lookup"><span data-stu-id="1ebb1-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ebb1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ebb1-128">See also</span></span>



[<span data-ttu-id="1ebb1-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="1ebb1-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="1ebb1-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="1ebb1-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="1ebb1-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ebb1-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="1ebb1-132">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1ebb1-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

