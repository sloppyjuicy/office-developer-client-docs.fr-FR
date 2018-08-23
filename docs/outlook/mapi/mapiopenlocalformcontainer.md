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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582559"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="6b81e-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b81e-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="6b81e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b81e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b81e-105">Renvoie un pointeur d’interface à la bibliothèque de formulaires local.</span><span class="sxs-lookup"><span data-stu-id="6b81e-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b81e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6b81e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b81e-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="6b81e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6b81e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6b81e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b81e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b81e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b81e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6b81e-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b81e-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="6b81e-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="6b81e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b81e-112">Parameters</span></span>

 <span data-ttu-id="6b81e-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="6b81e-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="6b81e-114">[out] Pointeur vers un pointeur vers l’interface de bibliothèque formulaire local.</span><span class="sxs-lookup"><span data-stu-id="6b81e-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b81e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6b81e-115">Return value</span></span>

<span data-ttu-id="6b81e-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6b81e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b81e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b81e-117">Remarks</span></span>

<span data-ttu-id="6b81e-118">L’interface à laquelle un pointeur est retourné peut être utilisée par les programmes d’installation tiers pour installer des formulaires spécifiques à l’application dans la bibliothèque sans le programme avoir à se connecter à MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b81e-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b81e-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6b81e-119">MFCMAPI reference</span></span>

<span data-ttu-id="6b81e-120">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6b81e-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b81e-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6b81e-121">**File**</span></span>|<span data-ttu-id="6b81e-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6b81e-122">**Function**</span></span>|<span data-ttu-id="6b81e-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6b81e-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b81e-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6b81e-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6b81e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b81e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="6b81e-126">MFCMAPI utilise la méthode **MAPIOpenLocalFormContainer** pour ouvrir le conteneur de formulaire local pour l’afficher dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6b81e-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b81e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b81e-127">See also</span></span>



[<span data-ttu-id="6b81e-128">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6b81e-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

