---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270146"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="9d601-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="9d601-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="9d601-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d601-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d601-105">Renvoie un pointeur d'interface vers la bibliothèque de formulaires locale.</span><span class="sxs-lookup"><span data-stu-id="9d601-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d601-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9d601-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d601-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="9d601-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9d601-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="9d601-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d601-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d601-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d601-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="9d601-110">Called by:</span></span>  <br/> |<span data-ttu-id="9d601-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="9d601-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="9d601-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d601-112">Parameters</span></span>

 <span data-ttu-id="9d601-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="9d601-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="9d601-114">remarquer Pointeur vers un pointeur vers l'interface de la bibliothèque de formulaires locale.</span><span class="sxs-lookup"><span data-stu-id="9d601-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d601-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d601-115">Return value</span></span>

<span data-ttu-id="9d601-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9d601-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d601-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d601-117">Remarks</span></span>

<span data-ttu-id="9d601-118">L'interface à laquelle un pointeur est renvoyé peut être utilisée par des programmes d'installation tiers pour installer des formulaires spécifiques aux applications dans la bibliothèque sans que le programme doive d'abord se connecter à MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d601-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9d601-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9d601-119">MFCMAPI reference</span></span>

<span data-ttu-id="9d601-120">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9d601-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9d601-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9d601-121">**File**</span></span>|<span data-ttu-id="9d601-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9d601-122">**Function**</span></span>|<span data-ttu-id="9d601-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9d601-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d601-124">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="9d601-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="9d601-125">CMainDlg:: OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="9d601-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="9d601-126">MFCMAPI utilise la méthode **MAPIOpenLocalFormContainer** pour ouvrir le conteneur de formulaire local afin de le rendre dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9d601-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d601-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d601-127">See also</span></span>



[<span data-ttu-id="9d601-128">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9d601-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

