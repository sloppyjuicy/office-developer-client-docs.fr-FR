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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418049"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="f4979-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="f4979-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="f4979-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4979-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4979-105">Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet fournisseur de bibliothèque de formulaires dans le contexte d’une session existante.</span><span class="sxs-lookup"><span data-stu-id="f4979-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4979-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f4979-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4979-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="f4979-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f4979-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f4979-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4979-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4979-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4979-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f4979-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4979-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="f4979-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="f4979-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4979-112">Parameters</span></span>

 <span data-ttu-id="f4979-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="f4979-113">_pSession_</span></span>
  
> <span data-ttu-id="f4979-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="f4979-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="f4979-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="f4979-115">_ppmgr_</span></span>
  
> <span data-ttu-id="f4979-116">[out] Pointeur vers l’interface **IMAPIFormMgr** renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f4979-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4979-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4979-117">Return value</span></span>

<span data-ttu-id="f4979-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f4979-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4979-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4979-119">Remarks</span></span>

<span data-ttu-id="f4979-120">Après qu’une application cliente a appelé la fonction **MAPIOpenFormMgr,** la plupart des interactions ultérieures liées aux formulaires ont lieu via le fournisseur de bibliothèque de formulaires ou une interface renvoyée par le fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="f4979-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="f4979-121">**L’interface IMAPIFormMgr** permet au client d’utiliser des handlers de messages et d’effectuer des résolutions entre les classes de messages et les bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="f4979-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4979-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f4979-122">MFCMAPI reference</span></span>

<span data-ttu-id="f4979-123">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f4979-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4979-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f4979-124">**File**</span></span>|<span data-ttu-id="f4979-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f4979-125">**Function**</span></span>|<span data-ttu-id="f4979-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f4979-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4979-127">MainDlg.cpp ouvre le gestionnaire de formulaires afin qu’un formulaire puisse être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f4979-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="f4979-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="f4979-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="f4979-129">MFCMAPI utilise la **méthode MAPIOpenFormMgr** pour ouvrir le gestionnaire de formulaire afin qu’un formulaire puisse être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f4979-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4979-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4979-130">See also</span></span>



[<span data-ttu-id="f4979-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f4979-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

