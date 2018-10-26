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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584807"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="2d30e-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2d30e-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="2d30e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d30e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d30e-105">La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface suivie d’une table qui contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d30e-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d30e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2d30e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d30e-107">Le fichier d’en-tête dans laquelle l’interface est définie et qui doit être inclus lorsque vous compilez votre code source.</span><span class="sxs-lookup"><span data-stu-id="2d30e-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="2d30e-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="2d30e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2d30e-109">L’objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="2d30e-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2d30e-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2d30e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d30e-111">Une liste des composants qui fournissent une implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="2d30e-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="2d30e-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2d30e-112">Called by:</span></span>  <br/> |<span data-ttu-id="2d30e-113">Une liste des composants qui appellent généralement les méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="2d30e-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="2d30e-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="2d30e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2d30e-115">L’identificateur GUID d’interface.</span><span class="sxs-lookup"><span data-stu-id="2d30e-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="2d30e-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="2d30e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2d30e-117">Le type de pointeur de l’objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="2d30e-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2d30e-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="2d30e-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2d30e-119">Pour les interfaces dérivées de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2d30e-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="2d30e-120">Si nontransacted, les modifications prennent effet immédiatement. Si le traitement modifications ne prendront effet qu’après [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="2d30e-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="2d30e-121">La première table est un autre tableau qui répertorie toutes les méthodes de cette interface dans l’ordre vtable.</span><span class="sxs-lookup"><span data-stu-id="2d30e-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="2d30e-122">Une vtable est un tableau de pointeurs fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d30e-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="2d30e-123">Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="2d30e-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="2d30e-124">Méthodes héritées d’autres interfaces ne sont pas affichées dans le tableau de l’ordre Vtable, mais peuvent être utilisées de la même manière comme indiqué dans l’interface qui définit les.</span><span class="sxs-lookup"><span data-stu-id="2d30e-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="2d30e-125">Après chaque rubrique interface, les méthodes de l’interface sont documentées puis par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="2d30e-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="2d30e-126">Pour chaque méthode, la documentation inclut une instruction brève objectif, un bloc de syntaxe et les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d30e-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="2d30e-127">**Titre**</span><span class="sxs-lookup"><span data-stu-id="2d30e-127">**Heading**</span></span>|<span data-ttu-id="2d30e-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="2d30e-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d30e-129">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d30e-129">Parameters</span></span>  <br/> |<span data-ttu-id="2d30e-130">Une description de chaque paramètre de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2d30e-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="2d30e-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d30e-131">Return Value</span></span>  <br/> |<span data-ttu-id="2d30e-132">Description de la méthode peut renvoyer les valeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="2d30e-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="2d30e-133">Voici les valeurs que les appelants doivent vérifier dans leur code.</span><span class="sxs-lookup"><span data-stu-id="2d30e-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="2d30e-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d30e-134">Remarks</span></span>  <br/> |<span data-ttu-id="2d30e-135">Description de pourquoi et comment la méthode est utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d30e-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="2d30e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d30e-136">See Also</span></span>  <br/> |<span data-ttu-id="2d30e-137">Références croisées à d’autres rubriques dans cette référence.</span><span class="sxs-lookup"><span data-stu-id="2d30e-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d30e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d30e-138">See also</span></span>



[<span data-ttu-id="2d30e-139">R�f�rence MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="2d30e-139">MAPI Reference</span></span>](mapi-reference.md)

