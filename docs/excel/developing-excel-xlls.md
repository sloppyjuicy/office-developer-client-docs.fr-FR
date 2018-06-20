---
title: Développement de XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compléments - [excel 2007], développement de XLL XLL - [Excel 2007,] - [Excel 2007], développement
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782026"
---
# <a name="developing-excel-xlls"></a>Développement de XLL Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
La raison principale pour l’écriture de Microsoft Excel XLL et à l’aide de l’API C consiste à créer des fonctions de feuille de calcul hautes performances. Les applications des fonctions de hautes performances et, à compter d’Excel 2007, la possibilité d’écrire des interfaces multithreads aux ressources du serveur puissant : rendre un composant essentiel de l’extensibilité Excel. Les performances des XLL a été davantage améliorée dans Excel 2007 à l’ajout de nouveaux types de données et le plus important, la prise en charge multithread.
  
L’API C a aucune des fonctionnalités de développement rapide plus haut niveau de Microsoft Visual Basic pour Applications (VBA), COM ou Microsoft .NET Framework. Gestion de la mémoire est faible niveau et par conséquent place une plus grande responsabilité sur le développeur. Nombreuses fonctionnalités d’Excel qui sont exposées par le biais de COM, en les rendant disponibles par le biais de VBA et le .NET Framework, ne sont pas exposées à l’API C.


- [Concepts de programmation Excel](excel-programming-concepts.md)
  
- [Utilisation des DLL](working-with-dlls.md)
  
- [Acc�s au code XLL dans Excel (en anglais)](accessing-xll-code-in-excel.md)
  
- [Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Cr�ation de XLL](creating-xlls.md)
  
- [�valuer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Multithread et gestion de la mémoire](multithreading-and-memory-management.md)
  
- [Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)
  
- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
  
- [Autorisation utilisateur sauts dans les opérations de longue durée](permitting-user-breaks-in-lengthy-operations.md)
  
- [Affichage des boîtes de dialogue à partir d’une DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Instance d’Excel Access et les poignées de la fenêtre principale](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilité descendante](backward-compatibility.md)
  

