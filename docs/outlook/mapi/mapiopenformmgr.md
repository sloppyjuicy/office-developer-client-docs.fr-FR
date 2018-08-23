---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586031"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="bcf02-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="bcf02-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="bcf02-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcf02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcf02-105">Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet de fournisseur de bibliothèque formulaire dans le contexte d’une session existante.</span><span class="sxs-lookup"><span data-stu-id="bcf02-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcf02-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bcf02-106">Header file:</span></span>  <br/> |<span data-ttu-id="bcf02-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="bcf02-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bcf02-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bcf02-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bcf02-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf02-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bcf02-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="bcf02-110">Called by:</span></span>  <br/> |<span data-ttu-id="bcf02-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="bcf02-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="bcf02-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf02-112">Parameters</span></span>

 <span data-ttu-id="bcf02-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="bcf02-113">_pSession_</span></span>
  
> <span data-ttu-id="bcf02-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="bcf02-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="bcf02-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="bcf02-115">_ppmgr_</span></span>
  
> <span data-ttu-id="bcf02-116">[out] Pointeur vers l’interface **IMAPIFormMgr** retournée.</span><span class="sxs-lookup"><span data-stu-id="bcf02-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bcf02-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bcf02-117">Return value</span></span>

<span data-ttu-id="bcf02-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bcf02-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bcf02-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="bcf02-119">Remarks</span></span>

<span data-ttu-id="bcf02-120">Une fois une application cliente effectue un appel à la fonction **MAPIOpenFormMgr** , la plupart des interactions de basés sur des formulaires suivants ont lieu via le fournisseur de bibliothèque de formulaire ou d’une interface renvoyée par le fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="bcf02-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="bcf02-121">L’interface **IMAPIFormMgr** autorise le client à travailler avec les gestionnaires de messages et effectuer des résolutions entre les classes de message et des bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="bcf02-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bcf02-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bcf02-122">MFCMAPI reference</span></span>

<span data-ttu-id="bcf02-123">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bcf02-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bcf02-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="bcf02-124">**File**</span></span>|<span data-ttu-id="bcf02-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="bcf02-125">**Function**</span></span>|<span data-ttu-id="bcf02-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="bcf02-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcf02-127">MainDlg.cpp ouvre le Gestionnaire de formulaire pour un formulaire peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bcf02-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="bcf02-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="bcf02-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="bcf02-129">MFCMAPI utilise la méthode **MAPIOpenFormMgr** pour ouvrir le Gestionnaire de formulaire pour un formulaire peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bcf02-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcf02-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf02-130">See also</span></span>



[<span data-ttu-id="bcf02-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="bcf02-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

