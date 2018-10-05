---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399647"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="a13a1-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="a13a1-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="a13a1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a13a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a13a1-105">Met fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="a13a1-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="a13a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a13a1-106">Parameters</span></span>

 <span data-ttu-id="a13a1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a13a1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a13a1-108">[in] Handle vers la fenêtre parent de toutes les boîtes de dialogue ou fenêtre à afficher.</span><span class="sxs-lookup"><span data-stu-id="a13a1-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="a13a1-109">Ce paramètre est ignoré si l’indicateur MAPI_LOGOFF_UI n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="a13a1-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="a13a1-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a13a1-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a13a1-111">[in] Masque de bits d’indicateurs qui contrôlent l’opération de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="a13a1-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="a13a1-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="a13a1-112">The following flags can be set:</span></span>
    
<span data-ttu-id="a13a1-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="a13a1-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="a13a1-114">Si cette session est partagée, tous les clients qui a ouvert une session à l’aide de la session partagée doivent être informés de la fermeture de session en cours.</span><span class="sxs-lookup"><span data-stu-id="a13a1-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="a13a1-115">Les clients doivent se déconnectent.</span><span class="sxs-lookup"><span data-stu-id="a13a1-115">The clients should log off.</span></span> <span data-ttu-id="a13a1-116">Tout client qui est à l’aide de la session partagée peut définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="a13a1-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="a13a1-117">MAPI_LOGOFF_SHARED est ignorée si la session en cours n’est pas partagée.</span><span class="sxs-lookup"><span data-stu-id="a13a1-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="a13a1-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="a13a1-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="a13a1-119">**Fermeture de session** peut afficher une boîte de dialogue lors de l’opération, éventuellement inviter l’utilisateur à confirmer.</span><span class="sxs-lookup"><span data-stu-id="a13a1-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="a13a1-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="a13a1-120">_ulReserved_</span></span>
  
> <span data-ttu-id="a13a1-121">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="a13a1-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a13a1-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a13a1-122">Return value</span></span>

<span data-ttu-id="a13a1-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a13a1-123">S_OK</span></span> 
  
> <span data-ttu-id="a13a1-124">L’opération de fermeture de session a réussi.</span><span class="sxs-lookup"><span data-stu-id="a13a1-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a13a1-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="a13a1-125">Remarks</span></span>

<span data-ttu-id="a13a1-126">La méthode **IMAPISession::Logoff** termine une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="a13a1-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="a13a1-127">Lors de la **fermeture de session** renvoie, aucune des méthodes à l’exception de [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="a13a1-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a13a1-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="a13a1-128">Notes to callers</span></span>

<span data-ttu-id="a13a1-129">Lors de la **fermeture de session** renvoie, version de l’objet de la session en appelant la méthode **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="a13a1-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="a13a1-130">Pour plus d’informations sur la fin d’une session, voir [mettre fin à une Session MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="a13a1-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a13a1-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a13a1-131">MFCMAPI reference</span></span>

<span data-ttu-id="a13a1-132">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a13a1-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a13a1-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a13a1-133">**File**</span></span>|<span data-ttu-id="a13a1-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a13a1-134">**Function**</span></span>|<span data-ttu-id="a13a1-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a13a1-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a13a1-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="a13a1-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a13a1-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="a13a1-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="a13a1-138">MFCMAPI utilise la méthode **IMAPISession::Logoff** pour déconnecter la session avant de les mettre.</span><span class="sxs-lookup"><span data-stu-id="a13a1-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a13a1-139">En raison du comportement d’arrêt rapide introduit dans Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 et Microsoft Outlook 2013, les clients doivent jamais passer le paramètre **MAPI_LOGOFF_SHARED** à [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="a13a1-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="a13a1-140">Passage **MAPI_LOGOFF_SHARED** provoque tous les clients MAPI commencer l’arrêt et un comportement inattendu se produit.</span><span class="sxs-lookup"><span data-stu-id="a13a1-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a13a1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a13a1-141">See also</span></span>



[<span data-ttu-id="a13a1-142">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a13a1-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a13a1-143">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="a13a1-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a13a1-144">Fermeture d’une session MAPI</span><span class="sxs-lookup"><span data-stu-id="a13a1-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

