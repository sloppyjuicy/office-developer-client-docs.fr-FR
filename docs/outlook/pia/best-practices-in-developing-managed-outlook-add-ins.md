---
title: Méthodes conseillées pour le développement de compléments Outlook managés
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87573980836d63d751302b0efcec0952331b7fc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406861"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="74511-102">Méthodes conseillées pour le développement de compléments Outlook managés</span><span class="sxs-lookup"><span data-stu-id="74511-102">Best Practices in Developing Managed Outlook Add-ins</span></span>

<span data-ttu-id="74511-p101">Même si les assemblys d'interopérabilité Outlook vous permettent d'écrire des solutions managées qui fonctionnent avec Outlook, Outlook est antérieur au .NET Framework et est conçu pour prendre en charge la programmabilité via des langages non managés comme Visual Basic pour Applications (VBA) et Visual Basic. Cette rubrique répertorie les principaux points à prendre en considération lors du développement d'un complément managé pour Outlook.</span><span class="sxs-lookup"><span data-stu-id="74511-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="74511-105">Libération systématique des objets</span><span class="sxs-lookup"><span data-stu-id="74511-105">Systematically Releasing Objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="74511-106">Utilisation d’un domaine d’application distinct pour éviter les blocages</span><span class="sxs-lookup"><span data-stu-id="74511-106">Using a Separate Application Domain to Avoid Crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="74511-107">Utilisation d’un objet d’application approuvée fourni par les outils de développement Office pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74511-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="74511-108">Définir convenablement la portée des variables dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="74511-108">Scoping Variables Appropriately in Event Handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="74511-109">Éviter les technologies non prises en charge dans les compléments Outlook managés</span><span class="sxs-lookup"><span data-stu-id="74511-109">Avoiding Unsupported Technologies in Managed Outlook Add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="74511-110">Utilisation de la liaison tardive en cas de dépendance envers plusieurs versions d’Outlook</span><span class="sxs-lookup"><span data-stu-id="74511-110">Using Late Binding If Depending on Multiple Versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

