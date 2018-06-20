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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783928"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="3d42b-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="3d42b-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="3d42b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d42b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d42b-105">Met fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d42b-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="3d42b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d42b-106">Parameters</span></span>

 <span data-ttu-id="3d42b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3d42b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3d42b-108">[in] Handle vers la fenêtre parent de toutes les boîtes de dialogue ou fenêtre à afficher.</span><span class="sxs-lookup"><span data-stu-id="3d42b-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="3d42b-109">Ce paramètre est ignoré si l’indicateur MAPI_LOGOFF_UI n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="3d42b-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="3d42b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d42b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3d42b-111">[in] Masque de bits d’indicateurs qui contrôlent l’opération de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="3d42b-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="3d42b-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="3d42b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="3d42b-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="3d42b-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="3d42b-114">Si cette session est partagée, tous les clients qui a ouvert une session à l’aide de la session partagée doivent être informés de la fermeture de session en cours.</span><span class="sxs-lookup"><span data-stu-id="3d42b-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="3d42b-115">Les clients doivent se déconnectent.</span><span class="sxs-lookup"><span data-stu-id="3d42b-115">The clients should log off.</span></span> <span data-ttu-id="3d42b-116">Tout client qui est à l’aide de la session partagée peut définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="3d42b-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="3d42b-117">MAPI_LOGOFF_SHARED est ignorée si la session en cours n’est pas partagée.</span><span class="sxs-lookup"><span data-stu-id="3d42b-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="3d42b-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="3d42b-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="3d42b-119">**Fermeture de session** peut afficher une boîte de dialogue lors de l’opération, éventuellement inviter l’utilisateur à confirmer.</span><span class="sxs-lookup"><span data-stu-id="3d42b-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="3d42b-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="3d42b-120">_ulReserved_</span></span>
  
> <span data-ttu-id="3d42b-121">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="3d42b-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d42b-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3d42b-122">Return value</span></span>

<span data-ttu-id="3d42b-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d42b-123">S_OK</span></span> 
  
> <span data-ttu-id="3d42b-124">L’opération de fermeture de session a réussi.</span><span class="sxs-lookup"><span data-stu-id="3d42b-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d42b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d42b-125">Remarks</span></span>

<span data-ttu-id="3d42b-126">La méthode **IMAPISession::Logoff** termine une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d42b-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="3d42b-127">Lors de la **fermeture de session** renvoie, aucune des méthodes à l’exception de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="3d42b-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d42b-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="3d42b-128">Notes to callers</span></span>

<span data-ttu-id="3d42b-129">Lors de la **fermeture de session** renvoie, version de l’objet de la session en appelant la méthode **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="3d42b-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="3d42b-130">Pour plus d’informations sur la fin d’une session, voir [mettre fin à une Session MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="3d42b-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3d42b-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3d42b-131">MFCMAPI reference</span></span>

<span data-ttu-id="3d42b-132">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3d42b-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3d42b-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3d42b-133">**File**</span></span>|<span data-ttu-id="3d42b-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3d42b-134">**Function**</span></span>|<span data-ttu-id="3d42b-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3d42b-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d42b-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="3d42b-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="3d42b-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="3d42b-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="3d42b-138">MFCMAPI utilise la méthode **IMAPISession::Logoff** pour déconnecter la session avant de les mettre.</span><span class="sxs-lookup"><span data-stu-id="3d42b-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3d42b-139">En raison du comportement d’arrêt rapide introduit dans Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 et Microsoft Outlook 2013, les clients doivent jamais passer le paramètre **MAPI_LOGOFF_SHARED** à [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="3d42b-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="3d42b-140">Passage **MAPI_LOGOFF_SHARED** provoque tous les clients MAPI commencer l’arrêt et un comportement inattendu se produit.</span><span class="sxs-lookup"><span data-stu-id="3d42b-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d42b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d42b-141">See also</span></span>



[<span data-ttu-id="3d42b-142">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d42b-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="3d42b-143">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3d42b-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3d42b-144">Mettre fin à une Session MAPI</span><span class="sxs-lookup"><span data-stu-id="3d42b-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

