---
title: Vue d’ensemble de la référence MAPI Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Derni�re modification�: vendredi 1 f�vrier 2013'
ms.openlocfilehash: bb7831ab79512eb8ca0018905e359654d7177cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564779"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="3ad38-103">Vue d’ensemble de la référence MAPI Outlook</span><span class="sxs-lookup"><span data-stu-id="3ad38-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="3ad38-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ad38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ad38-105">Cette rubrique fournit des informations générales sur la documentation de référence de MAPI pour Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="3ad38-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="3ad38-106">À propos de cette documentation</span><span class="sxs-lookup"><span data-stu-id="3ad38-106">About this documentation</span></span>

<span data-ttu-id="3ad38-107">Cette documentation s’applique à l’implémentation de la MAPI (Messaging API) dans Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="3ad38-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="3ad38-108">Antérieures à Microsoft Office Outlook 2007, référence du programmeur MAPI fait partie de la documentation de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ad38-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3ad38-109">Étant donné que Exchange a deemphasized l’utilisation de MAPI depuis Microsoft Exchange Server 2007, prise en charge pour l’implémentation Exchange est limitée.</span><span class="sxs-lookup"><span data-stu-id="3ad38-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="3ad38-110">L’implémentation Outlook de MAPI diffère de l’implémentation de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ad38-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="3ad38-111">L’implémentation d’Outlook est optimisée pour l’exécution sur les ordinateurs clients et met en évidence faible latence.</span><span class="sxs-lookup"><span data-stu-id="3ad38-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="3ad38-112">L’implémentation Exchange est conçue pour les serveurs où la haute disponibilité et mieux multithreading sont importantes.</span><span class="sxs-lookup"><span data-stu-id="3ad38-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="3ad38-113">Utilisez cette documentation pour les applications en cours d’exécution sur les systèmes de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3ad38-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="3ad38-114">Pour les applications serveur, utilisez l’implémentation Exchange de MAPI, le cas échéant, ou des API Exchange actuelles telles que les Services Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ad38-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="3ad38-115">Pour plus d’informations sur les Services Web Exchange, voir la [Référence de Services Web Exchange](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ad38-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="3ad38-116">Il peut être possible d’écrire des applications qui fonctionnent avec les implémentations Exchange ou Outlook de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ad38-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="3ad38-117">Par exemple, MFCMAPI fonctionne sur les deux plates-formes.</span><span class="sxs-lookup"><span data-stu-id="3ad38-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="3ad38-118">Les implémentations proposent de nombreuses fonctionnalités courantes, mais il existe des différences évidentes et discret.</span><span class="sxs-lookup"><span data-stu-id="3ad38-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="3ad38-119">Vous devez tester avec soin sur les deux plateformes si vous souhaitez que votre application fonctionne dans les environnements.</span><span class="sxs-lookup"><span data-stu-id="3ad38-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="3ad38-120">Ce test nécessite deux systèmes, car les deux implémentations en cours d’exécution sur la même installation de système d’exploitation n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3ad38-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="3ad38-121">Sachez que MAPI est appropriée pour l’accès aux données dans un emplacement de stockage MAPI de bas niveau ou à la création d’un transport, la banque de messages ou le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3ad38-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="3ad38-122">Étant donné que MAPI contourne la logique métier d’Outlook, vous devez également envisager l’utilisation du modèle objet Outlook lors de l’évaluation des API pour la création de votre solution.</span><span class="sxs-lookup"><span data-stu-id="3ad38-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="3ad38-123">Le modèle objet Outlook encapsule la logique métier Outlook mais n’est pas adapté aux applications de Service Windows, les fournisseurs de synchronisation ou code multithread.</span><span class="sxs-lookup"><span data-stu-id="3ad38-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="3ad38-124">Pour plus d’informations sur les nouveautés de cette édition, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ad38-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="3ad38-125">Nouveaut�s de cette �dition (en anglais)</span><span class="sxs-lookup"><span data-stu-id="3ad38-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="3ad38-126">�l�ments d'API d�conseill�es dans cette �dition</span><span class="sxs-lookup"><span data-stu-id="3ad38-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="3ad38-127">Si vous débutez au développement d’applications MAPI pour Outlook, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ad38-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="3ad38-128">Sélection d’une API ou d’une technologie pour développer des solutions pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="3ad38-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [<span data-ttu-id="3ad38-129">Utilis�e couramment des fichiers d'en-t�te</span><span class="sxs-lookup"><span data-stu-id="3ad38-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="3ad38-130">Propri�t�s couramment utilis�es</span><span class="sxs-lookup"><span data-stu-id="3ad38-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="3ad38-131">Objets couramment utilis�es</span><span class="sxs-lookup"><span data-stu-id="3ad38-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="3ad38-132">Le reste de cette référence est classé dans les trois types d’informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ad38-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="3ad38-133">[Exemples MAPI](mapi-samples.md) - permet d’accéder à nombreux exemples de code qui illustrent l’utilisation des différents éléments d’API et comment implémenter des fournisseurs de base MAPI et créer des éléments Outlook.</span><span class="sxs-lookup"><span data-stu-id="3ad38-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="3ad38-134">[Concepts MAPI](mapi-concepts.md) - explique les concepts et l’architecture de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ad38-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="3ad38-135">[Référence MAPI](mapi-reference.md) - fournit des informations détaillées sur les fonctions, les interfaces, les structures et les propriétés MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ad38-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3ad38-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ad38-136">See also</span></span>

- [<span data-ttu-id="3ad38-137">Mise en route avec la référence de MAPI pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="3ad38-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="3ad38-138">Exemples MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="3ad38-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="3ad38-139">Concepts MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="3ad38-139">MAPI Concepts</span></span>](mapi-concepts.md)

