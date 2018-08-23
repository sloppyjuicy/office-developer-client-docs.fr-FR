---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584807"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="efbb0-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="efbb0-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="efbb0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efbb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efbb0-105">La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface suivie d’une table qui contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="efbb0-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efbb0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="efbb0-106">Header file:</span></span>  <br/> |<span data-ttu-id="efbb0-107">Le fichier d’en-tête dans laquelle l’interface est définie et qui doit être inclus lorsque vous compilez votre code source.</span><span class="sxs-lookup"><span data-stu-id="efbb0-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="efbb0-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="efbb0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="efbb0-109">L’objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="efbb0-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="efbb0-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="efbb0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="efbb0-111">Une liste des composants qui fournissent une implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="efbb0-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="efbb0-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="efbb0-112">Called by:</span></span>  <br/> |<span data-ttu-id="efbb0-113">Une liste des composants qui appellent généralement les méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="efbb0-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="efbb0-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="efbb0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="efbb0-115">L’identificateur GUID d’interface.</span><span class="sxs-lookup"><span data-stu-id="efbb0-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="efbb0-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="efbb0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="efbb0-117">Le type de pointeur de l’objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="efbb0-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="efbb0-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="efbb0-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="efbb0-119">Pour les interfaces dérivées de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="efbb0-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="efbb0-120">Si nontransacted, les modifications prennent effet immédiatement. Si le traitement modifications ne prendront effet qu’après [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="efbb0-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="efbb0-121">La première table est un autre tableau qui répertorie toutes les méthodes de cette interface dans l’ordre vtable.</span><span class="sxs-lookup"><span data-stu-id="efbb0-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="efbb0-122">Une vtable est un tableau de pointeurs fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="efbb0-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="efbb0-123">Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="efbb0-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="efbb0-124">Méthodes héritées d’autres interfaces ne sont pas affichées dans le tableau de l’ordre Vtable, mais peuvent être utilisées de la même manière comme indiqué dans l’interface qui définit les.</span><span class="sxs-lookup"><span data-stu-id="efbb0-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="efbb0-125">Après chaque rubrique interface, les méthodes de l’interface sont documentées puis par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="efbb0-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="efbb0-126">Pour chaque méthode, la documentation inclut une instruction brève objectif, un bloc de syntaxe et les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="efbb0-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="efbb0-127">**Titre**</span><span class="sxs-lookup"><span data-stu-id="efbb0-127">**Heading**</span></span>|<span data-ttu-id="efbb0-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="efbb0-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efbb0-129">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efbb0-129">Parameters</span></span>  <br/> |<span data-ttu-id="efbb0-130">Une description de chaque paramètre de la méthode.</span><span class="sxs-lookup"><span data-stu-id="efbb0-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="efbb0-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="efbb0-131">Return Value</span></span>  <br/> |<span data-ttu-id="efbb0-132">Description de la méthode peut renvoyer les valeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="efbb0-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="efbb0-133">Voici les valeurs que les appelants doivent vérifier dans leur code.</span><span class="sxs-lookup"><span data-stu-id="efbb0-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="efbb0-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="efbb0-134">Remarks</span></span>  <br/> |<span data-ttu-id="efbb0-135">Description de pourquoi et comment la méthode est utilisée.</span><span class="sxs-lookup"><span data-stu-id="efbb0-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="efbb0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efbb0-136">See Also</span></span>  <br/> |<span data-ttu-id="efbb0-137">Références croisées à d’autres rubriques dans cette référence.</span><span class="sxs-lookup"><span data-stu-id="efbb0-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efbb0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efbb0-138">See also</span></span>



[<span data-ttu-id="efbb0-139">R�f�rence MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="efbb0-139">MAPI Reference</span></span>](mapi-reference.md)

