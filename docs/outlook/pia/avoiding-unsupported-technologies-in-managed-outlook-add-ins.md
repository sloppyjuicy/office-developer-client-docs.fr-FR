---
title: Éviter les technologies non prises en charge dans les compléments Outlook managés
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705420"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a><span data-ttu-id="f5064-102">Éviter les technologies non prises en charge dans les compléments Outlook managés</span><span class="sxs-lookup"><span data-stu-id="f5064-102">Avoiding unsupported technologies in managed Outlook add-ins</span></span>

<span data-ttu-id="f5064-103">Certaines technologies qui sont antérieures à .NET Framework ne sont pas prises en charge dans la programmation du code managé.</span><span class="sxs-lookup"><span data-stu-id="f5064-103">Certain technologies that predate the .NET Framework are not supported in managed code programming.</span></span> <span data-ttu-id="f5064-104">Il s'agit notamment des technologies CDO (Collaboration Data Objects), MAPI (Messaging Application Programming Interface, souvent appelé Extended MAPI), et Simple MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5064-104">These technologies include Collaboration Data Objects (CDO), Messaging Application Programming Interface (MAPI, often known as Extended MAPI), and Simple MAPI.</span></span> <span data-ttu-id="f5064-105">Ces technologies ont été conçues et développées avec du code non managé et Microsoft ne fournit aucun wrapper managé officiel pour prendre en charge leur utilisation dans des applications managées.</span><span class="sxs-lookup"><span data-stu-id="f5064-105">These technologies were designed and developed with unmanaged code, and Microsoft does not provide official managed wrappers to support their use in managed applications.</span></span> 

<span data-ttu-id="f5064-106">Pour plus d’informations, reportez-vous à la section relative aux API prises en charge dans le code managé de l’article de la [base de connaissances 266353 : Instructions de prise en charge pour le développement de messagerie côté client](https://go.microsoft.com/fwlink/?linkid=89209).</span><span class="sxs-lookup"><span data-stu-id="f5064-106">For more information, see the section "APIs that are supported in managed code" in the article [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span></span>

<span data-ttu-id="f5064-107">Néanmoins, Microsoft Outlook propose de nombreuses fonctionnalités de modèle objet qui effectuent ce que seuls CDO et les extensions client Exchange (ECE) permettaient précédemment d’effectuer pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="f5064-107">Nonetheless, Microsoft Outlook offers many object model features that achieve what previously only CDO and Exchange Client Extensions (ECE) solved for developers.</span></span> <span data-ttu-id="f5064-108">Si vous utilisez CDO dans une application Outlook non managée existante et que l'absence de prise en charge de CDO dans les solutions managées vous a empêché d'effectuer une migration de l'application vers le code managé, vous pouvez désormais mettre à jour votre solution vers le code managé, uniquement en faisant appel au modèle objet Outlook et à l'assembly PIA (Primary Interop Assembly), sans avoir à recourir à CDO.</span><span class="sxs-lookup"><span data-stu-id="f5064-108">If you use CDO in an existing unmanaged Outlook application and the lack of support for CDO in managed solutions has hindered you from migrating the application to managed code, you can now consider updating your solution to managed code, using only the Outlook object model and the Primary Interop Assembly (PIA), without having to resort to CDO.</span></span> 

<span data-ttu-id="f5064-109">Pour plus d'informations sur une plateforme Outlook plus complète introduite dans Outlook 2007 afin de réduire la dépendance envers CDO et les Extensions de client Exchange, voir [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f5064-109">For more information about a more comprehensive Outlook platform introduced in Outlook 2007 to reduce reliance on CDO and ECE, see [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span></span>

