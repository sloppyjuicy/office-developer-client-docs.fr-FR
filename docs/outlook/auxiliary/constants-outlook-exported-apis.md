---
title: Constantes (Outlook des API exportées)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Cette rubrique contient des définitions de constantes pour les API exportées par Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319872"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="b7525-103">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="b7525-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="b7525-104">Cette rubrique contient des définitions de constantes pour les API exportées par Outlook.</span><span class="sxs-lookup"><span data-stu-id="b7525-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="b7525-105">Définitions de la prise en charge des fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="b7525-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="b7525-106">Définitions de la prise en charge des catégories</span><span class="sxs-lookup"><span data-stu-id="b7525-106">Definitions for Category support</span></span>

|<span data-ttu-id="b7525-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="b7525-107">**Constant**</span></span>|<span data-ttu-id="b7525-108">**Définition**</span><span class="sxs-lookup"><span data-stu-id="b7525-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7525-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b7525-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="b7525-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7525-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="b7525-111">Identificateurs de dispatch divers</span><span class="sxs-lookup"><span data-stu-id="b7525-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="b7525-112">Outlook expose les identificateurs de dispatch suivants pour permettre aux développeurs d'utiliser [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) pour accéder à la propriété ou la méthode correspondante, ou écouter l'événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b7525-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="b7525-113">**Constante associée**</span><span class="sxs-lookup"><span data-stu-id="b7525-113">**Associated constant**</span></span>|<span data-ttu-id="b7525-114">**Valeur DISPID**</span><span class="sxs-lookup"><span data-stu-id="b7525-114">**Dispid value**</span></span>|<span data-ttu-id="b7525-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b7525-115">**Description**</span></span>|<span data-ttu-id="b7525-116">**Interface applicable**</span><span class="sxs-lookup"><span data-stu-id="b7525-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b7525-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="b7525-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="b7525-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="b7525-118">0xF024</span></span>  <br/> |<span data-ttu-id="b7525-119">Utilisé pour appeler la propriété correspondante sur un élément afin de vérifier si l'élément a été modifié mais n'a pas été enregistré.</span><span class="sxs-lookup"><span data-stu-id="b7525-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="b7525-120">Objets au niveau élément</span><span class="sxs-lookup"><span data-stu-id="b7525-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="b7525-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="b7525-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="b7525-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="b7525-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="b7525-123">Utilisé pour appeler la méthode correspondante dans l'Explorateur ou l'inspecteur afin de spécifier s'il faut afficher l'image d'un contact, en fonction d'un argument donné.</span><span class="sxs-lookup"><span data-stu-id="b7525-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="b7525-124">Explorateur ou inspecteur</span><span class="sxs-lookup"><span data-stu-id="b7525-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="b7525-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="b7525-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="b7525-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="b7525-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="b7525-127">Permet de gérer l'événement à partir de la fonction **IDispatch:: Invoke** qui se déclenche avant une opération d'impression.</span><span class="sxs-lookup"><span data-stu-id="b7525-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="b7525-128">Application</span><span class="sxs-lookup"><span data-stu-id="b7525-128">Application</span></span>  <br/> |
|<span data-ttu-id="b7525-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="b7525-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="b7525-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="b7525-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="b7525-131">Permet de gérer l'événement à partir de la fonction **IDispatch:: Invoke** qui se déclenche quand Outlook a terminé de lire les propriétés de l'élément.</span><span class="sxs-lookup"><span data-stu-id="b7525-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="b7525-132">Objets au niveau élément</span><span class="sxs-lookup"><span data-stu-id="b7525-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7525-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7525-133">See also</span></span>

- [<span data-ttu-id="b7525-134">API exportées Outlook</span><span class="sxs-lookup"><span data-stu-id="b7525-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="b7525-135">À propos des API exportées par Outlook</span><span class="sxs-lookup"><span data-stu-id="b7525-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="b7525-136">Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)</span><span class="sxs-lookup"><span data-stu-id="b7525-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="b7525-137">Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)</span><span class="sxs-lookup"><span data-stu-id="b7525-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="b7525-138">Événements disponibles et leur DISPID (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="b7525-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

