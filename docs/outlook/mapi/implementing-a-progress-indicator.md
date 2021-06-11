---
title: Mise en œuvre d’un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435095"
---
# <a name="implementing-a-progress-indicator"></a>Mise en œuvre d’un indicateur de progression

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des opérations initiées par les clients prennent beaucoup de temps. L’un des paramètres d’entrée de ces opérations potentiellement longues est un pointeur vers un objet de progression , un objet qui implémente l’interface [IMAPIProgress : IUnknown.](imapiprogressiunknown.md) Les objets de progression contrôlent l’apparence et l’affichage des indicateurs de progression et sont implémentés par les clients et par MAPI. Vous pouvez choisir d’implémenter ou non un objet de progression. L’implémentation MAPI est disponible pour les fournisseurs de services à utiliser si vous ne souhaitez pas fournir d’implémentation. 
  
Les objets de progression fonctionnent avec les éléments de données suivants :
  
- Valeur minimale globale qui, lorsque votre méthode [IMAPIProgress::P rogress](imapiprogress-progress.md) est appelée, doit être inférieure ou égale à la valeur du paramètre _ulValue._ Au début de l’opération,  _ulValue_ sera égal à cette valeur minimale. 
    
- Valeur maximale globale qui, lorsque votre méthode **IMAPIProgress::P rogress** est appelée, doit être supérieure ou égale au paramètre _ulValue._ À la fin de l’opération,  _ulValue_ sera égal à cette valeur maximale. 
    
- Valeur d’indicateur qui indique si la progression correspond à un élément de niveau supérieur ou inférieur.
    
- Valeur qui indique le niveau de progression actuel de l’opération.
    
- Nombre d’éléments actuellement traitées par rapport au total.
    
- Nombre total d’éléments à traiter pendant l’opération.
    
Les valeurs minimale et maximale représentent le début et la fin de l’opération sous forme numérique. Utilisez 1 pour la valeur minimale initiale et 1 000 pour la valeur maximale initiale, en passant ces valeurs aux fournisseurs de services dans les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax.](imapiprogress-getmax.md) Les fournisseurs de services réinitialiseront ces valeurs lorsqu’ils appellent [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
La valeur des indicateurs est utilisée par les fournisseurs de services pour déterminer comment ils doivent définir les autres valeurs. Initialisez la valeur des indicateurs MAPI_TOP_LEVEL et renvoyez cette valeur dans votre implémentation de **GetFlags** jusqu’à ce que le fournisseur de services la réinitialise en appelant **SetLimits**. 
  
Dans votre implémentation de la méthode **SetLimits,** enregistrez les copies locales de chacun des paramètres :  _lpulMin_,  _lpulMax_ et  _lpulFlags_. Ces valeurs doivent être facilement disponibles lorsqu’un fournisseur de services appelle vos méthodes **GetMin,** **GetMax** ou **GetFlags.** 
  
Pour mettre à jour l’affichage de l’indicateur de progression, les fournisseurs de services appellent votre **méthode IMAPIProgress::P rogress.** Il existe trois paramètres pour cette méthode : une valeur, un nombre et un total. Utilisez le premier paramètre,  _ulValue,_ pour afficher l’indicateur de progression. Le  _paramètre ulValue_ est l’indicateur de progression et n’est égal à  _ulMin_ global qu’au tout début de l’opération et n’est égal à  _ulMax_ global qu’à la fin de l’opération. 
  
Utilisez les deuxième et troisième paramètres,  _ulCount_ et  _ulTotal,_ si disponibles, pour afficher un message facultatif tel que « 5 éléments terminés sur 10 ». Si les deuxième et troisième paramètres sont définies sur 0, vous pouvez choisir de modifier visuellement ou non l’indicateur de progression. Certains fournisseurs de services définissent ces paramètres sur zéros pour indiquer qu’ils traitent un sous-objet dont la progression est surveillée par rapport à un objet parent. Dans ce cas, il est logique de modifier l’affichage uniquement lorsque l’objet parent signale la progression. Certains fournisseurs de services passent des zéros pour ces paramètres à chaque fois. 
  

