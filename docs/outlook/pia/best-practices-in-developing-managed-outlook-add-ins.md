---
title: Méthodes conseillées pour le développement de compléments Outlook managés
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 474a43c17360979b4b25ccb55c0ed48b2c9d2ef7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723095"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="661bf-102">Méthodes conseillées pour le développement de compléments Outlook managés</span><span class="sxs-lookup"><span data-stu-id="661bf-102">Best practices in developing managed Outlook add-ins</span></span>

<span data-ttu-id="661bf-p101">Même si les assemblys d'interopérabilité Outlook vous permettent d'écrire des solutions managées qui fonctionnent avec Outlook, Outlook est antérieur au .NET Framework et est conçu pour prendre en charge la programmabilité via des langages non managés comme Visual Basic pour Applications (VBA) et Visual Basic. Cette rubrique répertorie les principaux points à prendre en considération lors du développement d'un complément managé pour Outlook.</span><span class="sxs-lookup"><span data-stu-id="661bf-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="661bf-105">Libération systématique des objets</span><span class="sxs-lookup"><span data-stu-id="661bf-105">Systematically releasing objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="661bf-106">Utilisation d’un domaine d’application distinct pour éviter les blocages</span><span class="sxs-lookup"><span data-stu-id="661bf-106">Using a separate application domain to avoid crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="661bf-107">Utilisation d’un objet d’application approuvée fourni par les outils de développement Office pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="661bf-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="661bf-108">Définir convenablement la portée des variables dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="661bf-108">Scoping variables appropriately in event handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="661bf-109">Éviter les technologies non prises en charge dans les compléments Outlook managés</span><span class="sxs-lookup"><span data-stu-id="661bf-109">Avoiding unsupported technologies in managed Outlook add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="661bf-110">Utilisation de la liaison tardive en cas de dépendance envers plusieurs versions d’Outlook</span><span class="sxs-lookup"><span data-stu-id="661bf-110">Using late binding if depending on multiple versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

