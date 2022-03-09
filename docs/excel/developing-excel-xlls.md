---
title: Développement de fichiers XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compléments - [Excel 2007], développer des fichiers XLL - [Excel 2007], fichiers XLL - [Excel 2007], développer
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
ms.localizationpriority: high
ms.openlocfilehash: 0bd4db26c711d8eb2fbe23cc97dc6b63f9b7681c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372408"
---
# <a name="developing-excel-xlls"></a>Développement de fichiers XLL Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
La principale raison d’écrire des fichiers XLL Microsoft Excel et d’utiliser l’API C est de créer des fonctions de feuille de calcul hautes performances. Les applications des fonctions hautes performances (et dans Excel 2007, la possibilité d’écrire des interfaces multithreads vers des ressources serveur puissantes) en font un axe essentiel de l’extensibilité d’Excel. Les performances des fichiers XLL ont été davantage améliorées dans Excel 2007 grâce à l’ajout de nouveaux types de données et, surtout, à la prise en charge du multithreading.
  
L’API C ne possède aucune des fonctionnalités de développement rapide de niveau supérieur de Microsoft Visual Basic pour Applications (VBA), COM ou Microsoft .NET Framework. La gestion de la mémoire opère à faible niveau et, par conséquent, fait peser plus de responsabilités sur le développeur. La plupart des fonctionnalités d’Excel exposées par le biais de COM, ce qui les rend accessibles par le biais de .NET Framework et de VBA, ne sont pas exposées à l’API C.

- [Concepts de programmation Excel](excel-programming-concepts.md)
  
- [Utilisation des fichiers DLL](working-with-dlls.md)
  
- [Accés au code XLL dans Excel](accessing-xll-code-in-excel.md)
  
- [Appel des fonctions XLL à partir de l’Assistant Fonction ou des boîtes de dialogue Remplacer](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Création de XLL](creating-xlls.md)
  
- [Évaluer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Multithreading et gestion de la mémoire](multithreading-and-memory-management.md)
  
- [Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)
  
- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
  
- [Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)
  
- [Affichage des boîtes de dialogue dans un fichier DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Accès à l’instance Excel et aux handles de fenêtre principaux](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilité descendante](backward-compatibility.md)
  