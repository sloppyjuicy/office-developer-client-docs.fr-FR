---
title: Autorisation des interruptions utilisateur dans les opérations longues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
ms.openlocfilehash: fb50be79cad0c1a78bc299a145b1ef309678b522
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198326"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Autorisation des interruptions utilisateur dans les opérations longues

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Même si Windows utilise le multitâche préemptif, où l’exécution de vos fonctions ou commandes peut prendre beaucoup de temps, il est bon de donner un peu de temps au système d’exploitation de temps en temps pour l’aider à planifier des tâches simultanées. À l’aide Windows appels natifs, vous pouvez le faire à l’aide de la fonction de veille. À l’aide de l’API C, vous pouvez le faire à l’aide de la fonction [xlAbort](xlabort.md), qui produit non seulement le processeur pendant un instant, mais vérifie également si l’utilisateur a appuy sur la touche d’annulation, **ÉCHAP**.
  
La **fonction xlAbort** permet donc à votre code de vérifier si l’utilisateur souhaite mettre fin au processus, d’y faire le nettoyage nécessaire, puis de renvoyer le contrôle à Excel. La fonction vous permet également d’effacer la condition d’coupure. Cela permet à vos commandes d’afficher une boîte de dialogue pour vérifier si l’utilisateur souhaite mettre fin à la commande. Si l’utilisateur ne souhaite pas mettre fin à la commande, l’appel de la fonction **xlAbort** avec l’argument *FALSE* permet d’effacer la coupure. (L’argument par défaut est *TRUE,* qui vérifie simplement la condition, mais ne l’effacera pas.)
  
Vous pouvez appeler la **fonction xlAbort** à partir d’une fonction définie par l’utilisateur (UDF) ou d’une commande XLL. Dans une fonction UDF, lorsque la fonction **xlAbort** renvoie **true**, après avoir détecté un coupure utilisateur, vous avez généralement raccourci le calcul de la fonction et renvoyer une valeur pour indiquer que le calcul n’a pas été effectué, peut-être une erreur ou zéro. Vous ne souhaitez pas effacer la condition de rupture afin que d’autres instances de fonctions longues qui vérifient également cette condition se cassent également. Excel implicitement cette condition à la fin d’un recalcul.
  
Lorsque vous détectez une condition d’rupture dans une commande, vous l’effacerez généralement en appelant à nouveau la fonction **xlAbort** avec l’argument **FALSE,** bien que Excel ôte implicitement cette condition à la fin d’une commande.
  
## <a name="see-also"></a>Voir aussi

[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)  
[Développement de XLL de Excel 2013](developing-excel-xlls.md)  
[Accès à l’instance Excel et aux handles de fenêtre principaux](how-to-access-excel-instance-and-main-window-handles.md)
