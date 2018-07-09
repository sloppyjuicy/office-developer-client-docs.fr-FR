---
title: Constantes (Outlook exportée API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Cette rubrique contient des définitions de constantes pour les API qui exporte Outlook.
ms.openlocfilehash: 54b491e436b7b9275a227de40439ddb66d8d0c5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782550"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="53ae0-103">Constantes (Outlook exportée API)</span><span class="sxs-lookup"><span data-stu-id="53ae0-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="53ae0-104">Cette rubrique contient des définitions de constantes pour les API qui exporte Outlook.</span><span class="sxs-lookup"><span data-stu-id="53ae0-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="53ae0-105">Prise en charge des définitions de fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="53ae0-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="53ae0-106">Prise en charge des définitions de catégorie</span><span class="sxs-lookup"><span data-stu-id="53ae0-106">Definitions for Category support</span></span>

|<span data-ttu-id="53ae0-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="53ae0-107">**Constant**</span></span>|<span data-ttu-id="53ae0-108">**Définition**</span><span class="sxs-lookup"><span data-stu-id="53ae0-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53ae0-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="53ae0-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="53ae0-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53ae0-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="53ae0-111">Identificateurs de répartition divers</span><span class="sxs-lookup"><span data-stu-id="53ae0-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="53ae0-112">Outlook expose les identificateurs de répartition suivants (DISPID) afin que les développeurs peuvent utiliser [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) pour accéder à la propriété correspondante ou la méthode, ou écouter l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="53ae0-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="53ae0-113">**Constante associée**</span><span class="sxs-lookup"><span data-stu-id="53ae0-113">**Associated constant**</span></span>|<span data-ttu-id="53ae0-114">**Valeur DISPID**</span><span class="sxs-lookup"><span data-stu-id="53ae0-114">**Dispid value**</span></span>|<span data-ttu-id="53ae0-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="53ae0-115">**Description**</span></span>|<span data-ttu-id="53ae0-116">**Interface applicable**</span><span class="sxs-lookup"><span data-stu-id="53ae0-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53ae0-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="53ae0-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="53ae0-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="53ae0-118">0xF024</span></span>  <br/> |<span data-ttu-id="53ae0-119">Utilisé pour appeler la propriété correspondante sur un élément pour vérifier si l’élément a été modifié mais n’a pas été enregistré.</span><span class="sxs-lookup"><span data-stu-id="53ae0-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="53ae0-120">Objets de niveau élément</span><span class="sxs-lookup"><span data-stu-id="53ae0-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="53ae0-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="53ae0-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="53ae0-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="53ae0-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="53ae0-123">Utilisé pour appeler la méthode correspondante dans l’Explorateur de solutions ou l’inspecteur pour spécifier s’il faut afficher l’image d’un contact, basé sur un argument donné.</span><span class="sxs-lookup"><span data-stu-id="53ae0-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="53ae0-124">Objet Explorer ou inspector</span><span class="sxs-lookup"><span data-stu-id="53ae0-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="53ae0-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="53ae0-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="53ae0-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="53ae0-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="53ae0-127">Permet de gérer l’événement à partir de la fonction **IDispatch::Invoke** qui se déclenche avant une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="53ae0-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="53ae0-128">Application</span><span class="sxs-lookup"><span data-stu-id="53ae0-128">Application</span></span>  <br/> |
|<span data-ttu-id="53ae0-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="53ae0-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="53ae0-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="53ae0-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="53ae0-131">Permet de gérer l’événement à partir de la fonction **IDispatch::Invoke** qui se déclenche quand Outlook est terminée, les propriétés de l’élément de lecture.</span><span class="sxs-lookup"><span data-stu-id="53ae0-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="53ae0-132">Objets de niveau élément</span><span class="sxs-lookup"><span data-stu-id="53ae0-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53ae0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53ae0-133">See also</span></span>

- [<span data-ttu-id="53ae0-134">Outlook des API exportées</span><span class="sxs-lookup"><span data-stu-id="53ae0-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="53ae0-135">À propos de l’API exporté par Outlook</span><span class="sxs-lookup"><span data-stu-id="53ae0-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="53ae0-136">Déterminer si un élément Outlook a été modifié mais ne pas enregistré (autre référence Outlook)</span><span class="sxs-lookup"><span data-stu-id="53ae0-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="53ae0-137">Spécifier s’il faut afficher l’image d’un contact dans Outlook (autre référence Outlook)</span><span class="sxs-lookup"><span data-stu-id="53ae0-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/fr-fr/library/office/gg262879.aspx)
- [<span data-ttu-id="53ae0-138">Événements disponibles et leur DISPID (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="53ae0-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

