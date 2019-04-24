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
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270097"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="05205-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="05205-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="05205-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05205-105">Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet fournisseur de bibliothèque de formulaires dans le contexte d'une session existante.</span><span class="sxs-lookup"><span data-stu-id="05205-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05205-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="05205-106">Header file:</span></span>  <br/> |<span data-ttu-id="05205-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="05205-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="05205-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="05205-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="05205-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="05205-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="05205-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="05205-110">Called by:</span></span>  <br/> |<span data-ttu-id="05205-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="05205-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="05205-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05205-112">Parameters</span></span>

 <span data-ttu-id="05205-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="05205-113">_pSession_</span></span>
  
> <span data-ttu-id="05205-114">dans Pointeur vers la session en cours d'utilisation par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="05205-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="05205-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="05205-115">_ppmgr_</span></span>
  
> <span data-ttu-id="05205-116">remarquer Pointeur vers l'interface **IMAPIFormMgr** renvoyée.</span><span class="sxs-lookup"><span data-stu-id="05205-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05205-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="05205-117">Return value</span></span>

<span data-ttu-id="05205-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="05205-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05205-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="05205-119">Remarks</span></span>

<span data-ttu-id="05205-120">Une fois qu'une application cliente appelle la fonction **MAPIOpenFormMgr** , la plupart des interactions liées aux formulaires ont lieu via le fournisseur de bibliothèque de formulaires ou une interface renvoyée par le fournisseur de la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="05205-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="05205-121">L'interface **IMAPIFormMgr** permet au client de travailler avec les gestionnaires de messages et d'effectuer des résolutions entre les classes de message et les bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="05205-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="05205-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="05205-122">MFCMAPI reference</span></span>

<span data-ttu-id="05205-123">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05205-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05205-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="05205-124">**File**</span></span>|<span data-ttu-id="05205-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="05205-125">**Function**</span></span>|<span data-ttu-id="05205-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="05205-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05205-127">MainDlg. cpp ouvre le gestionnaire de formulaires afin qu'un formulaire puisse être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="05205-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="05205-128">CMainDlg:: OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="05205-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="05205-129">MFCMAPI utilise la méthode **MAPIOpenFormMgr** pour ouvrir le gestionnaire de formulaires afin qu'un formulaire puisse être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="05205-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05205-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05205-130">See also</span></span>



[<span data-ttu-id="05205-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="05205-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

