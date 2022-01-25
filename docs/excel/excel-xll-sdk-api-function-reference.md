---
title: Référence des fonctions XLL SDK API Excel 2013
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Référence des fonctions API [Excel 2007], fonctions [Excel 2007], référence [Excel 2007] Kit de développement logiciel Excel 2007 XLL, référence
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
ms.localizationpriority: high
ms.openlocfilehash: 308119a8cb10324f314786166fdbfc3a8c56f8e5
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198855"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Référence des fonctions XLL SDK API Excel 2013

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le kit de développement XLL Microsoft Excel 2013 contient les fichiers sources d’une bibliothèque Framework conçue pour accélérer la rédaction de fichiers XLL, ainsi que deux exemples de projets : Example et Generic. 
  
Cette section fournit une référence des fonctions pour les éléments suivants :
  
- Rappels Excel que XLL peut appeler.
    
- Rappels XLL que Microsoft Excel peut rechercher.
    
- Fonctions principales dans les projets d’exemple et de cadre.
    
## <a name="sample-projects"></a>Exemples de projets

Le kit de développement XLL Excel 2013 fournit des fichiers sources et des fichiers de projet Microsoft Visual Studio pour les projets d’exemple suivants :
  
- Le projet **Framework** (`SAMPLES\FRAMEWRK\`) contient un projet qui peut être intégré dans une bibliothèque, FRAMEWRK.lib, qui peut ensuite être lié à d’autres projets XLL. La bibliothèque contient de nombreuses fonctions et outils qui simplifient la rédaction de fichiers XLL. Cette bibliothèque est utilisée dans les deux autres projets conjointement avec le fichier d’en-tête FRAMEWRK.h.
    
- Le projet **Example** (`SAMPLES\EXAMPLE\`) contient un projet qui peut être intégré à un fichier XLL, EXAMPLE.xll. Le fichier XLL contient de nombreux exemples d’utilisation de la bibliothèque Framework, ainsi que des exemples d’implémentation des fonctions d’interface du complément XLL telles que **xlAutoOpen**.
    
- Le projet **Generic** (`SAMPLES\GENERIC\`) contient un projet qui peut être intégré à un fichier XLL, GENERIC.xll. Le fichier XLL illustre plusieurs exemples de fonction et de commande, et constitue un bon point de départ pour la rédaction de vos propres fichiers XLL.
    
## <a name="in-this-section"></a>Dans cette section

- [Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Fonctions de rappel de l’API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)
  
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)
  
- [Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)
  
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Voir aussi

- [Programmation avec l�API C dans Excel](programming-with-the-c-api-in-excel.md)
  
- [Développement de XLL de Excel 2013](developing-excel-xlls.md)

