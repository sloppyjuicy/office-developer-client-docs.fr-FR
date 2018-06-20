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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784751"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="6842d-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="6842d-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="6842d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6842d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6842d-105">Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet de fournisseur de bibliothèque formulaire dans le contexte d’une session existante.</span><span class="sxs-lookup"><span data-stu-id="6842d-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6842d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6842d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6842d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="6842d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6842d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6842d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6842d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6842d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6842d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6842d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6842d-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="6842d-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="6842d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6842d-112">Parameters</span></span>

 <span data-ttu-id="6842d-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="6842d-113">_pSession_</span></span>
  
> <span data-ttu-id="6842d-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6842d-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="6842d-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="6842d-115">_ppmgr_</span></span>
  
> <span data-ttu-id="6842d-116">[out] Pointeur vers l’interface **IMAPIFormMgr** retournée.</span><span class="sxs-lookup"><span data-stu-id="6842d-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6842d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6842d-117">Return value</span></span>

<span data-ttu-id="6842d-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6842d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6842d-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="6842d-119">Remarks</span></span>

<span data-ttu-id="6842d-120">Une fois une application cliente effectue un appel à la fonction **MAPIOpenFormMgr** , la plupart des interactions de basés sur des formulaires suivants ont lieu via le fournisseur de bibliothèque de formulaire ou d’une interface renvoyée par le fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="6842d-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="6842d-121">L’interface **IMAPIFormMgr** autorise le client à travailler avec les gestionnaires de messages et effectuer des résolutions entre les classes de message et des bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="6842d-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6842d-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6842d-122">MFCMAPI reference</span></span>

<span data-ttu-id="6842d-123">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6842d-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6842d-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6842d-124">**File**</span></span>|<span data-ttu-id="6842d-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6842d-125">**Function**</span></span>|<span data-ttu-id="6842d-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6842d-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6842d-127">MainDlg.cpp ouvre le Gestionnaire de formulaire pour un formulaire peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6842d-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="6842d-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="6842d-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="6842d-129">MFCMAPI utilise la méthode **MAPIOpenFormMgr** pour ouvrir le Gestionnaire de formulaire pour un formulaire peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6842d-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6842d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6842d-130">See also</span></span>



[<span data-ttu-id="6842d-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6842d-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

