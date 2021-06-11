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
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422662"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="3a77b-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3a77b-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="3a77b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a77b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a77b-105">La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface, suivie d’un tableau contenant les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a77b-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a77b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3a77b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a77b-107">Fichier d’en-tête dans lequel l’interface est définie et qui doit être inclus lorsque vous compilez votre code source.</span><span class="sxs-lookup"><span data-stu-id="3a77b-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="3a77b-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="3a77b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a77b-109">Objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a77b-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="3a77b-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3a77b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a77b-111">Liste des composants qui fournissent une implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a77b-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="3a77b-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3a77b-112">Called by:</span></span>  <br/> |<span data-ttu-id="3a77b-113">Liste des composants qui appellent généralement les méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a77b-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="3a77b-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="3a77b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a77b-115">GUID de l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="3a77b-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="3a77b-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3a77b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a77b-117">Type de pointeur pour l’objet qui expose l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a77b-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="3a77b-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="3a77b-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="3a77b-119">Pour les interfaces dérivées [d’IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3a77b-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="3a77b-120">Si ce n’est pas le cas, les modifications prennent effet immédiatement ; si elles sont transposées, les modifications ne prennent effet [qu’une fois IMAPIProp::SaveChanges](imapiprop-savechanges.md) appelé.</span><span class="sxs-lookup"><span data-stu-id="3a77b-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="3a77b-121">Le premier tableau suivant est un autre tableau qui répertorie toutes les méthodes de cette interface dans l’ordre vtable.</span><span class="sxs-lookup"><span data-stu-id="3a77b-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="3a77b-122">Un tableau vtable est un tableau de pointeurs de fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="3a77b-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="3a77b-123">Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="3a77b-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="3a77b-124">Les méthodes héritées d’autres interfaces ne sont pas affichées dans la table Order Vtable, mais peuvent être utilisées de la même manière que dans l’interface qui les définit.</span><span class="sxs-lookup"><span data-stu-id="3a77b-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="3a77b-125">Après chaque rubrique d’interface, les méthodes de l’interface sont ensuite documentées par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="3a77b-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="3a77b-126">Pour chaque méthode, la documentation inclut une brève instruction à usage, un bloc de syntaxe et les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a77b-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="3a77b-127">**Titre**</span><span class="sxs-lookup"><span data-stu-id="3a77b-127">**Heading**</span></span>|<span data-ttu-id="3a77b-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="3a77b-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a77b-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="3a77b-129">Parameters</span></span>  <br/> |<span data-ttu-id="3a77b-130">Description de chaque paramètre de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3a77b-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="3a77b-131">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3a77b-131">Return Value</span></span>  <br/> |<span data-ttu-id="3a77b-132">Description des valeurs uniques que la méthode peut renvoyer.</span><span class="sxs-lookup"><span data-stu-id="3a77b-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="3a77b-133">Voici les valeurs que les appelants doivent vérifier dans leur code.</span><span class="sxs-lookup"><span data-stu-id="3a77b-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="3a77b-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a77b-134">Remarks</span></span>  <br/> |<span data-ttu-id="3a77b-135">Description du pourquoi et de la façon dont la méthode est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3a77b-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="3a77b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a77b-136">See Also</span></span>  <br/> |<span data-ttu-id="3a77b-137">Renvois à d’autres rubriques de cette référence.</span><span class="sxs-lookup"><span data-stu-id="3a77b-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a77b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a77b-138">See also</span></span>



[<span data-ttu-id="3a77b-139">Référence MAPI</span><span class="sxs-lookup"><span data-stu-id="3a77b-139">MAPI Reference</span></span>](mapi-reference.md)

