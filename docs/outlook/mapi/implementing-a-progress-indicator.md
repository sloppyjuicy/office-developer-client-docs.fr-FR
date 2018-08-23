---
title: Implémentation d’un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1a359ec413da91b3e2819978e80ea0a921f6b245
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587123"
---
# <a name="implementing-a-progress-indicator"></a>Implémentation d’un indicateur de progression

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
De nombreuses opérations initiées par des clients prennent beaucoup de temps. Un des paramètres d’entrée à ces opérations potentiellement longues est un pointeur vers un objet de l’avancement, un objet qui implémente le [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface. Objets de progression contrôlent l’apparence et l’affichage des indicateurs de progression et sont implémentées par les clients et par MAPI. Vous pouvez choisir d’implémenter un objet de l’avancement ou non. L’implémentation de MAPI est disponible pour les fournisseurs de services à utiliser si vous décidez de ne pas fournir une implémentation. 
  
Objets de progression fonctionnent avec les éléments de données suivants :
  
- Valeur minimale globale qui, lorsque la méthode [IMAPIProgress::Progress](imapiprogress-progress.md) est appelée, doit être inférieure ou égale à la valeur du paramètre _ulValue_ . Au début de l’opération, _ulValue_ est égale à cette valeur minimale. 
    
- Valeur maximale globale qui, lorsque la méthode **IMAPIProgress::Progress** est appelée, doit être supérieure ou égale au paramètre _ulValue_ . À la fin de l’opération, _ulValue_ est égale à cette valeur maximale. 
    
- Indicateurs d’une valeur qui indique si la progression correspond à un haut ou bas niveau élément.
    
- Une valeur qui indique le niveau de progression de l’opération en cours.
    
- Le nombre d’éléments actuellement traités par rapport au total.
    
- Nombre total d’éléments à être traités au cours de l’opération.
    
Les valeurs minimales et maximales représentent le début et la fin de l’opération sous forme numérique. Utilisez 1 pour la valeur minimale initiale et 1000 pour définir la valeur maximale initiale, en transmettant ces valeurs aux fournisseurs de services dans les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax](imapiprogress-getmax.md) . Fournisseurs de services de réinitialiser ces valeurs quand ils appellent [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
La valeur flags est utilisée par les fournisseurs de service afin de déterminer comment ils doivent définir les autres valeurs. Initialiser la valeur flags à MAPI_TOP_LEVEL et renvoyer cette valeur dans votre implémentation de **GetFlags** jusqu'à ce que le fournisseur de services rétablit en appelant **SetLimits**. 
  
Dans votre implémentation de la méthode **SetLimits** , enregistrer une copie locale de chacun des paramètres : _lpulMin_, _lpulMax_et _lpulFlags_. Lorsqu’un fournisseur de services appelle vos méthodes **GetMin**, **GetMax**ou **GetFlags** , ces valeurs doivent être disponibles. 
  
Pour mettre à jour l’affichage de l’indicateur de progression, les fournisseurs de services appeler votre méthode **IMAPIProgress::Progress** . Il existe trois paramètres à cette méthode : un total, un nombre et une valeur. Utilisez le premier paramètre, _ulValue_, pour afficher l’indicateur de progression. Le paramètre _ulValue_ est l’indicateur de progression et sera égale à global _ulMin_ uniquement au début de l’opération et égale à global _ulMax_ uniquement à la fin de l’opération. 
  
Utilisation des paramètres de deuxième et troisième, _ulCount_ et _ulTotal_, le cas échéant afficher un message facultatif, tel que « 5 éléments terminé sur 10 ». Si les deuxième et troisième paramètres sont définies à 0, vous pouvez choisir s’il faut modifier visuellement l’indicateur de progression. Certains fournisseurs de services de définissent ces paramètres en zéros pour indiquer qu’ils sont traitement un sous-objet dont la progression est surveillée par rapport à un objet parent. Dans ce cas, il est logique de modifier l’affichage uniquement lorsque l’objet parent signale la progression. Certains fournisseurs de services transmet les zéros de ces paramètres chaque fois. 
  

