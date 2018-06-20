---
title: Autorisation utilisateur sauts dans les opérations de longue durée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonction xlAbort [excel 2007], tâches simultanées [Excel 2007], sauts utilisateur [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782181"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Autorisation utilisateur sauts dans les opérations de longue durée

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Même si Windows utilise multitâche préventif, où vos fonctions ou des commandes peuvent prendre beaucoup de temps d’exécution, il est conseillé de rendement peu de temps pour le système d’exploitation autre afin de planifier des tâches simultanées. À l’aide des appels Windows natives, procéder à l’aide de la fonction de mise en veille. À l’aide de l’API C, vous pouvez le faire à l’aide de la [fonction xlAbort](xlabort.md), non seulement génère le processeur pour une conversation instantanée, mais également vérifie si l’utilisateur a appuyé sur la touche Annuler, **ÉCHAP**.
  
La fonction **xlAbort** permet donc de votre code pour vérifier si l’utilisateur souhaite mettre fin au processus, de nettoyage nécessaires et rendre ensuite le contrôle vers Excel. La fonction permet d’effacer la condition d’arrêt. Cela permet à vos commandes afficher une boîte de dialogue pour vérifier si l’utilisateur souhaite mettre fin à la commande. Si l’utilisateur ne souhaite pas mettre fin à la commande, l’appel de la fonction **xlAbort** avec l’argument *FALSE* efface l’arrêt. (L’argument par défaut est *TRUE* , ce qui vérifie la condition simplement, mais ne la supprime pas). 
  
Vous pouvez appeler la fonction **xlAbort** à partir d’une fonction définie par l’utilisateur (UDF) ou d’une commande XLL. Dans un fichier UDF, lorsque la fonction **xlAbort** renvoie **la valeur TRUE**, avoir détecté un saut de l’utilisateur, vous généralement coupés le calcul de la fonction et renvoyer une valeur pour indiquer que le calcul n’a pas terminé, par exemple une erreur ou zéro. Vous ne devez pas désactiver la condition d’arrêt afin que d’autres instances de fonctions longues qui également vérifient cette condition d’arrêt également. Excel efface implicitement cette condition lorsque le recalcul se termine.
  
Lorsque vous détectez une condition d’arrêt dans une commande, vous désactivez généralement la condition en appelant la fonction **xlAbort** à l’aide de l’argument **FALSE**, bien qu’Excel efface implicitement cette condition issue d’une commande.
  
## <a name="see-also"></a>Voir aussi



[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Instance d’Excel Access et les poignées de la fenêtre principale](how-to-access-excel-instance-and-main-window-handles.md)

