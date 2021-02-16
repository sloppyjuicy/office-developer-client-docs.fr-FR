---
title: Hébergement d’InfoPath en tant qu’éditeur XML dans une autre application
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: L’environnement d’édition de formulaires Microsoft InfoPath peut être hébergé dans une application Windows personnalisée, ce qui permet aux développeurs d’intégrer l’environnement d’édition de formulaires InfoPath aux applications métier.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422578"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="83fb8-103">Hébergement d’InfoPath en tant qu’éditeur XML dans une autre application</span><span class="sxs-lookup"><span data-stu-id="83fb8-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="83fb8-104">L'environnement d'édition de formulaire Microsoft InfoPath peut être hébergé dans une application Windows personnalisée.</span><span class="sxs-lookup"><span data-stu-id="83fb8-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="83fb8-105">Cette fonctionnalité permet aux développeurs d'intégrer cet environnement dans des applications métiers.</span><span class="sxs-lookup"><span data-stu-id="83fb8-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="83fb8-106">Les développeurs qui écrivent des applications traditionnelles basées sur COM peuvent utiliser l'objet **InfoPathEditorObject** qui est disponible en référençant le fichier IPEDITOR.DLL, et les développeurs écrivant des applications basées sur Microsoft .NET peuvent utiliser l'assembly **Microsoft.Office.InfoPath.FormControl**, qui fournit des types managés basés sur l'interface COM.</span><span class="sxs-lookup"><span data-stu-id="83fb8-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="83fb8-107">L’assembly IPEDITOR.DLL et **Microsoft.Office.InfoPath.FormControl** sont installés avec InfoPath dans le dossier C:\Program Files\Microsoft Office\Office15 ou C:\Program Files (x86)\Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="83fb8-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="83fb8-108">L’article MSDN, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, se concentre sur l’objet **FormControl** et sur la façon de l’incorporer dans votre application personnalisée. Applications NET.</span><span class="sxs-lookup"><span data-stu-id="83fb8-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="83fb8-109">Le téléchargement associé à l'article contient une application personnalisée qui fournit des fonctions .NET pour la réplication de l'environnement d'édition de formulaires InfoPath à travers l'utilisation de l'objet COM **IOleCommandTargets**.</span><span class="sxs-lookup"><span data-stu-id="83fb8-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

