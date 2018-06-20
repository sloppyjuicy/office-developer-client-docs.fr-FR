---
title: Référence de la fonction API SDK XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- référence des fonctions d’API [excel 2007], fonctions [Excel 2007], référence [Excel 2007], du Kit de développement logiciel Excel 2007 XLL, référence
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782120"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Référence de la fonction API SDK XLL Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le SDK XLL Microsoft Excel 2013 contient des fichiers sources pour une bibliothèque Framework qui est conçu pour accélérer l’écriture de XLL et deux exemples de projets, exemple et générique. 
  
Cette section fournit une référence de fonction pour les éléments suivants :
  
- Rappels Excel la XLL peut appeler.
    
- Rappels XLL Microsoft Excel recherche.
    
- Fonctions clés dans les projets exemple et framework.
    
## <a name="sample-projects"></a>Exemples de projets

Le Kit de développement logiciel XLL Excel 2013 fournit des fichiers source et fichiers de projet Microsoft Visual Studio pour les exemples de projet suivants :
  
- Le projet **Framework** (`SAMPLES\FRAMEWRK\`) contient un projet qui peut être créé dans une bibliothèque, FRAMEWRK.lib, qui peut ensuite être lié dans d’autres projets XLL. La bibliothèque contient plusieurs fonctions et les outils qui facilitent l’écriture de XLL plus faciles. Cette bibliothèque est utilisée dans les deux autres projets en association avec le fichier d’en-tête FRAMEWRK.h.
    
- **L’exemple** de projet (`SAMPLES\EXAMPLE\`) contient un projet pouvant être créées pour un XLL, EXAMPLE.xll. La ressource XLL contient de nombreux exemples de l’utilisation de la bibliothèque Framework et exemples d’implémentation des fonctions telles que **xlAutoOpen**interface complément XLL.
    
- Le projet **générique** (`SAMPLES\GENERIC\`) contient un projet pouvant être créées pour un XLL, GENERIC.xll. La ressource XLL illustre plusieurs exemples de fonctions et commandes et est un bon point de départ pour l’écriture de votre propre XLL.
    
## <a name="in-this-section"></a>Dans cette section

- [Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)
  
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)
  
- [Fonctions de la DLL générique](functions-in-the-generic-dll.md)
  
- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Voir aussi

- [Programmation avec l�API�C dans Excel](programming-with-the-c-api-in-excel.md)
  
- [D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

