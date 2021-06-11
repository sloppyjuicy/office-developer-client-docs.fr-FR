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
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hébergement d’InfoPath en tant qu’éditeur XML dans une autre application

L'environnement d'édition de formulaire Microsoft InfoPath peut être hébergé dans une application Windows personnalisée. Cette fonctionnalité permet aux développeurs d'intégrer cet environnement dans des applications métiers. Les développeurs qui écrivent des applications traditionnelles basées sur COM peuvent utiliser l'objet **InfoPathEditorObject** qui est disponible en référençant le fichier IPEDITOR.DLL, et les développeurs écrivant des applications basées sur Microsoft .NET peuvent utiliser l'assembly **Microsoft.Office.InfoPath.FormControl**, qui fournit des types managés basés sur l'interface COM. Les IPEDITOR.DLL et **Microsoft.Office. L’assembly InfoPath.FormControl** est installé avec InfoPath dans le dossier C:\Program Files\Microsoft Office\Office15 ou C:\Program Files (x86)\Microsoft Office\Office15. 
  
L’article MSDN, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, se concentre sur l’objet **FormControl** et sur la façon de l’incorporer dans votre application personnalisée. Applications NET. Le téléchargement associé à l'article contient une application personnalisée qui fournit des fonctions .NET pour la réplication de l'environnement d'édition de formulaires InfoPath à travers l'utilisation de l'objet COM **IOleCommandTargets**.
  

