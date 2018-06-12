---
title: Hébergement d’InfoPath en tant qu’éditeur XML dans une autre application
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Le formulaire Microsoft InfoPath environnement d’édition peut être hébergé dans une application Windows personnalisée, qui permet aux développeurs d’intégrer le dans des applications métier de l’environnement d’édition de formulaires InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782349"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="f87b9-103">Hébergement d'InfoPath en tant qu'éditeur XML dans une autre application</span><span class="sxs-lookup"><span data-stu-id="f87b9-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="f87b9-104">L'environnement d'édition de formulaire Microsoft InfoPath peut être hébergé dans une application Windows personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f87b9-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="f87b9-105">Cette fonctionnalité permet aux développeurs d'intégrer cet environnement dans des applications métiers.</span><span class="sxs-lookup"><span data-stu-id="f87b9-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="f87b9-106">Les développeurs qui écrivent des applications traditionnelles basées sur COM peuvent utiliser l'objet **InfoPathEditorObject** qui est disponible en référençant le fichier IPEDITOR.DLL, et les développeurs écrivant des applications basées sur Microsoft .NET peuvent utiliser l'assembly **Microsoft.Office.InfoPath.FormControl**, qui fournit des types managés basés sur l'interface COM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="f87b9-107">La IPEDITOR. DLL et assembly **Microsoft.Office.InfoPath.FormControl** sont installés avec InfoPath dans le C:\Program Files\Microsoft Office\Office15 ou C:\Program Files (x86) \Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="f87b9-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="f87b9-108">L’article MSDN d’hébergement de l’environnement d’édition de formulaires InfoPath 2007 dans une Application de formulaire Windows personnalisée, se concentre sur l’objet **FormControl** et comment incorporer dans votre personnalisé. Des applications .NET.</span><span class="sxs-lookup"><span data-stu-id="f87b9-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="f87b9-109">Le téléchargement associé à l'article contient une application personnalisée qui fournit des fonctions .NET pour la réplication de l'environnement d'édition de formulaires InfoPath à travers l'utilisation de l'objet COM **IOleCommandTargets**.</span><span class="sxs-lookup"><span data-stu-id="f87b9-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

