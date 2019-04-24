---
title: Autorisation des interruptions utilisateur dans les opérations longues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonction xlAbort [Excel 2007], tâches simultanées [Excel 2007], arrêts utilisateur [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310380"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Autorisation des interruptions utilisateur dans les opérations longues

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Bien que Windows utilise le multitâche préemptif, dans lequel les fonctions ou les commandes peuvent prendre beaucoup de temps à s'exécuter, il est recommandé de prévoir un certain temps pour le système d'exploitation maintenant et à nouveau afin de l'aider à planifier des tâches simultanées. À l'aide des appels Windows natifs, vous pouvez effectuer cette opération à l'aide de la fonction Sleep. À l'aide de l'API C, vous pouvez le faire à l'aide de la [fonction xlAbort](xlabort.md), qui permet non seulement le processeur pour un instant, mais également de vérifier si l'utilisateur a appuyé sur la touche annuler, puis sur **Échap**.
  
La fonction **xlAbort** permet donc à votre code de vérifier si l'utilisateur souhaite terminer le processus, effectuer le nettoyage nécessaire, puis renvoyer le contrôle à Excel. La fonction vous permet également de désactiver la condition d'arrêt. Cela permet à vos commandes d'afficher une boîte de dialogue pour vérifier si l'utilisateur souhaite terminer la commande. Si l'utilisateur ne souhaite pas terminer la commande, l'appel de la fonction **xlAbort** avec l' ** argument false efface le saut. (L'argument par défaut est *true* , qui vérifie simplement la condition, sans la désactiver.) 
  
Vous pouvez appeler la fonction **xlAbort** à partir d'une fonction définie par l'utilisateur (UDF) ou d'une commande XLL. Dans un fichier UDF, lorsque la fonction **xlAbort** renvoie la **valeur true**, après avoir détecté une interruption de l'utilisateur, vous pouvez généralement réduire le calcul de la fonction et renvoyer une valeur pour indiquer que le calcul n'a pas été terminé, peut-être une erreur ou un zéro. Vous ne devez pas effacer la condition d'arrêt afin que les autres instances des fonctions longues qui vérifient également cette condition s'arrêtent également. Excel efface implicitement cette condition lorsqu'un recalcul se termine.
  
Lorsque vous détectez une condition d'arrêt dans une commande, vous effacez généralement la condition en appelant à nouveau la fonction **xlAbort** avec l'argument **false**, même si Excel efface implicitement cette condition lorsqu'une commande se termine.
  
## <a name="see-also"></a>Voir aussi



[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Accès à l’instance Excel et aux handles de fenêtre principaux](how-to-access-excel-instance-and-main-window-handles.md)

