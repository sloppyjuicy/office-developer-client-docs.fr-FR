---
title: Référence de l’assembly PIA (Primary Interop Assembly) Outlook
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
localization_priority: Normal
ms.openlocfilehash: 53c50c447c6f132c562a1a22934df646347a51bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335746"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="f73f3-102">Référence de l’assembly PIA (Primary Interop Assembly) Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="f73f3-103">La documentation Référence de l’assembly PIA (Primary Interop Assembly) Outlook 2013 fournit une aide au développement d’applications managées pour Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="f73f3-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="f73f3-104">Elle étend la [Référence pour développeurs Outlook 2013](https://docs.microsoft.com/office/vba/api/overview/outlook) de l’environnement COM à l’environnement managé et explique en détail comment utiliser l’assembly PIA.</span><span class="sxs-lookup"><span data-stu-id="f73f3-104">It extends the [Outlook 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="f73f3-105">Elle inclut tous les ajouts et les changements apportés au modèle objet dans Outlook 2013 et fournit de nombreux exemples de code en C\# et Visual Basic qui montrent comment exécuter des tâches courantes dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="f73f3-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="f73f3-106">Si vous débutez en tant que développeur de solutions pour Outlook, consultez [Sélection d'une API ou d'une technologie pour développer des solutions pour Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) pour identifier les API et technologies les plus adaptées à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f73f3-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="f73f3-107">Objectif de la Référence PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-107">Purpose of the Outlook PIA reference</span></span>

<span data-ttu-id="f73f3-108">Si vous débutez dans l’écriture de compléments pour Outlook, consultez d’abord le contenu conceptuel dans la Référence pour développeurs Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="f73f3-108">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference.</span></span> <span data-ttu-id="f73f3-109">Bien que l'environnement de programmation, l'accès à certaines méthodes et la connexion aux événements diffèrent dans COM et dans le développement managé, les fonctionnalités du modèle objet Outlook se comportent de manière identique dans COM et dans le développement managé.</span><span class="sxs-lookup"><span data-stu-id="f73f3-109">Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development.</span></span> <span data-ttu-id="f73f3-110">Vous pouvez vous référer au contenu conceptuel de la Référence pour développeurs Outlook 2013 pour mieux comprendre comment utiliser les différentes fonctionnalités du modèle objet.</span><span class="sxs-lookup"><span data-stu-id="f73f3-110">You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="f73f3-111">Si vous avez une connaissance de base du modèle objet Outlook et que vous apprenez à développer des compléments Outlook managés, consultez l’article relatif à la [configuration requise pour utiliser l’assembly PIA Outlook](setting-up-to-use-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="f73f3-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="f73f3-112">Pour en savoir plus sur le développement de solutions Office managées à l’aide des Outils de développement Office pour Visual Studio 2013, consultez l’article [Développement Office dans Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="f73f3-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="f73f3-113">Pour apprendre à programmer des tâches Outlook de base en Visual Basic et en C\#, reportez-vous à l’article relatif aux [solutions Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="f73f3-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="f73f3-114">Pour obtenir des exemples de code plus sophistiqués, consultez l’article [Comment... (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md) dans cette référence.</span><span class="sxs-lookup"><span data-stu-id="f73f3-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="f73f3-115">Si vous connaissez déjà le modèle objet Outlook, que vous savez écrire des applications managées et que vous utilisez l’assembly PIA Outlook pour la première fois, commencez par lire les articles sur [l’installation et le référencement de l’assembly PIA Outlook](installing-and-referencing-the-outlook-pia.md) et l’[architecture de l’assembly PIA Outlook](architecture-of-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="f73f3-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="f73f3-116">Accès à la Référence de l’assembly PIA Outlook au moment de la conception</span><span class="sxs-lookup"><span data-stu-id="f73f3-116">Accessing the Outlook PIA reference in design time</span></span>

<span data-ttu-id="f73f3-117">Si vous utilisez les Outils de développement Office pour Visual Studio 2013 et que vous êtes connecté à Internet, vous pouvez accéder à une aide contextuelle en appuyant sur la touche F1 dans l’environnement de développement intégré (IDE) Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f73f3-117">If you use Office Developer Tools for Visual Studio 2013 and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="f73f3-118">Ce contenu d’aide correspond à la référence de l’assembly PIA Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="f73f3-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f73f3-119">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f73f3-119">In this section</span></span>

- [<span data-ttu-id="f73f3-120">Nouveautés de la référence PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-120">What's new in the Outlook PIA reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="f73f3-121">Configuration pour utiliser l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-121">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="f73f3-122">Architecture de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="f73f3-123">Développement de compléments managés Outlook à l’aide de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-123">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="f73f3-124">Procédure (Référence PIA Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="f73f3-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="f73f3-125">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="f73f3-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="f73f3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f73f3-126">See also</span></span>

- [<span data-ttu-id="f73f3-127">Centre pour développeurs Outlook</span><span class="sxs-lookup"><span data-stu-id="f73f3-127">Outlook Developer Center</span></span>](../outlook-home.md)
- [<span data-ttu-id="f73f3-128">Interopérabilité entre COM et .NET</span><span class="sxs-lookup"><span data-stu-id="f73f3-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="f73f3-129">Développement Office dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f73f3-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="f73f3-130">Accessibilité des produits Microsoft</span><span class="sxs-lookup"><span data-stu-id="f73f3-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

