---
title: Vue d’ensemble de la référence MAPI Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: Dernière modification le 1er février 2013
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348495"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="4fadb-103">Vue d’ensemble de la référence MAPI Outlook</span><span class="sxs-lookup"><span data-stu-id="4fadb-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="4fadb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fadb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fadb-105">Cette rubrique fournit des informations générales sur la documentation Référence MAPI Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="4fadb-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="4fadb-106">À propos de la documentation</span><span class="sxs-lookup"><span data-stu-id="4fadb-106">About this documentation</span></span>

<span data-ttu-id="4fadb-107">Cette documentation s’applique à l’implémentation de Messaging API (MAPI) dans Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="4fadb-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="4fadb-108">Avant Microsoft Office Outlook 2007, la référence du programmeur MAPI faisait partie de la documentation de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fadb-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4fadb-109">Étant donné qu’Exchange a minimisé l’utilisation de MAPI depuis Microsoft Exchange Server 2007, la prise en charge de l’implémentation Exchange est limitée.</span><span class="sxs-lookup"><span data-stu-id="4fadb-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="4fadb-110">L’implémentation Outlook de MAPI diffère de l’implémentation Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fadb-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="4fadb-111">L’implémentation Outlook est optimisée pour l’exécution sur les ordinateurs client et met en évidence la faible latence.</span><span class="sxs-lookup"><span data-stu-id="4fadb-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="4fadb-112">L’implémentation Exchange est destinée aux serveurs où la haute disponibilité et un meilleur multithreading sont d’une grande importance.</span><span class="sxs-lookup"><span data-stu-id="4fadb-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="4fadb-113">Utilisez cette documentation pour les applications en cours d’exécution sur les systèmes de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="4fadb-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="4fadb-114">Pour les applications serveur, utilisez l’implémentation Exchange de MAPI le cas échéant, ou utilisez les API Exchange actuelles telles que les Services Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fadb-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="4fadb-115">Pour plus d’informations sur les Services Web Exchange, consultez l’article [Référence des Services Web Exchange](https://msdn.microsoft.com/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="4fadb-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="4fadb-116">Il est possible de créer des applications qui fonctionnent avec des implémentations Outlook ou Exchange de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fadb-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="4fadb-117">Par exemple, MFCMAPI fonctionne parfaitement sur les deux plateformes.</span><span class="sxs-lookup"><span data-stu-id="4fadb-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="4fadb-118">Les implémentations proposent de nombreuses fonctionnalités courantes, mais il existe des différences évidentes et subtiles.</span><span class="sxs-lookup"><span data-stu-id="4fadb-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="4fadb-119">Vous devez faire un essai sur les deux plateformes si vous souhaitez que votre application fonctionne dans tous les environnements.</span><span class="sxs-lookup"><span data-stu-id="4fadb-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="4fadb-120">Ce test nécessitera deux systèmes, car l’exécution des deux implémentations sur l’installation du même système d’exploitation n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4fadb-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="4fadb-121">Sachez que MAPI convient pour un accès de bas niveau aux données d’une banque MAPI ou pour créer un transport, une banque de messages ou un fournisseur de carnets d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4fadb-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="4fadb-122">Étant donné que MAPI contourne la logique métier d’Outlook, vous pensez également à utiliser un modèle objet Outlook lorsque vous évaluez les API pour créer votre solution.</span><span class="sxs-lookup"><span data-stu-id="4fadb-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="4fadb-123">Le modèle objet Outlook encapsule la logique métier d’Outlook, mais n’est pas utilisable pour le code multithread, la synchronisation des fournisseurs ou les applications de service Windows.</span><span class="sxs-lookup"><span data-stu-id="4fadb-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="4fadb-124">Pour connaître les nouveautés de cette édition, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fadb-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="4fadb-125">Nouveautés de cette édition</span><span class="sxs-lookup"><span data-stu-id="4fadb-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="4fadb-126">Éléments d’API obsolètes dans cette édition</span><span class="sxs-lookup"><span data-stu-id="4fadb-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="4fadb-127">Si vous êtes nouveau dans le développement d’applications MAPI pour Outlook, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fadb-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="4fadb-128">Sélection d’une API ou d’une technologie pour le développement de solutions pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="4fadb-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="4fadb-129">Fichiers d’en-tête couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="4fadb-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="4fadb-130">Propriétés couramment utilisées</span><span class="sxs-lookup"><span data-stu-id="4fadb-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="4fadb-131">Objets couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="4fadb-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="4fadb-132">Le reste de cette référence est classé dans les trois types d’informations suivants :</span><span class="sxs-lookup"><span data-stu-id="4fadb-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="4fadb-133">[Exemples MAPI](mapi-samples.md) : vous dirige vers plusieurs exemples de code qui montrent l’utilisation de différents éléments d’API, et expliquent comment implémenter des fournisseurs MAPI de base et créer des éléments Outlook.</span><span class="sxs-lookup"><span data-stu-id="4fadb-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="4fadb-134">[Concepts MAPI](mapi-concepts.md) : explique les concepts et l’architecture de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fadb-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="4fadb-135">[Référence MAPI](mapi-reference.md) : fournit des informations détaillées sur les fonctions, les interfaces, les structures et les propriétés dans MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fadb-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4fadb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fadb-136">See also</span></span>

- [<span data-ttu-id="4fadb-137">Mise en route avec la référence de MAPI pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="4fadb-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="4fadb-138">Exemples MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="4fadb-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="4fadb-139">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="4fadb-139">MAPI Concepts</span></span>](mapi-concepts.md)

