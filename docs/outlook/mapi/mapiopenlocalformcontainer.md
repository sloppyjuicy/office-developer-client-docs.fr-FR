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
ms.openlocfilehash: c00c2fa04ae7e89f8c23c085ba021a935748ad4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784769"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="dca19-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="dca19-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="dca19-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dca19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dca19-105">Renvoie un pointeur d’interface à la bibliothèque de formulaires local.</span><span class="sxs-lookup"><span data-stu-id="dca19-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dca19-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dca19-106">Header file:</span></span>  <br/> |<span data-ttu-id="dca19-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="dca19-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dca19-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="dca19-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dca19-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dca19-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dca19-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="dca19-110">Called by:</span></span>  <br/> |<span data-ttu-id="dca19-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="dca19-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="dca19-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dca19-112">Parameters</span></span>

 <span data-ttu-id="dca19-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="dca19-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="dca19-114">[out] Pointeur vers un pointeur vers l’interface de bibliothèque formulaire local.</span><span class="sxs-lookup"><span data-stu-id="dca19-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dca19-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dca19-115">Return value</span></span>

<span data-ttu-id="dca19-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dca19-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dca19-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="dca19-117">Remarks</span></span>

<span data-ttu-id="dca19-118">L’interface à laquelle un pointeur est retourné peut être utilisée par les programmes d’installation tiers pour installer des formulaires spécifiques à l’application dans la bibliothèque sans le programme avoir à se connecter à MAPI.</span><span class="sxs-lookup"><span data-stu-id="dca19-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dca19-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dca19-119">MFCMAPI reference</span></span>

<span data-ttu-id="dca19-120">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dca19-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dca19-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="dca19-121">**File**</span></span>|<span data-ttu-id="dca19-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="dca19-122">**Function**</span></span>|<span data-ttu-id="dca19-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="dca19-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dca19-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dca19-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="dca19-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="dca19-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="dca19-126">MFCMAPI utilise la méthode **MAPIOpenLocalFormContainer** pour ouvrir le conteneur de formulaire local pour l’afficher dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dca19-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dca19-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca19-127">See also</span></span>



[<span data-ttu-id="dca19-128">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="dca19-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

