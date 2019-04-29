---
title: Implémentation d'un indicateur de progression
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
# <a name="implementing-a-progress-indicator"></a>Implémentation d'un indicateur de progression

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreuses opérations lancées par les clients prennent beaucoup de temps. L'un des paramètres d'entrée de ces opérations potentiellement longues est un pointeur vers un objet de progression, un objet qui implémente l'interface [méthode imapiprogress: IUnknown](imapiprogressiunknown.md) . Les objets Progress contrôlent l'apparence et l'affichage des indicateurs de progression et sont implémentés par les clients et MAPI. Vous pouvez choisir d'implémenter ou non un objet de progression. L'implémentation MAPI est disponible pour les fournisseurs de services à utiliser si vous décidez de ne pas fournir une implémentation. 
  
Les objets Progress fonctionnent avec les éléments de données suivants:
  
- Valeur minimale globale qui, lorsque votre [méthode imapiprogress::P méthode rogress](imapiprogress-progress.md) est appelée, doit être inférieure ou égale à la valeur du paramètre _ulValue_ . Au début de l'opération, _ulValue_ est égal à cette valeur minimale. 
    
- Valeur maximale globale qui, lorsque votre **méthode imapiprogress::P méthode rogress** est appelée, doit être supérieure ou égale au paramètre _ulValue_ . À la fin de l'opération, _ulValue_ est égal à cette valeur maximale. 
    
- Valeur d'indicateur qui indique si la progression correspond à un élément de niveau supérieur ou inférieur.
    
- Valeur qui indique le niveau actuel de progression de l'opération.
    
- Nombre d'éléments actuellement traités par rapport au total.
    
- Nombre total d'éléments à traiter au cours de l'opération.
    
Les valeurs minimale et maximale représentent le début et la fin de l'opération sous forme numérique. Utilisez 1 pour la valeur minimale initiale et 1000 pour la valeur maximale initiale, en transmettant ces valeurs aux fournisseurs de services dans les méthodes [méthode imapiprogress:: GetMin](imapiprogress-getmin.md) et [méthode imapiprogress:: GetMax](imapiprogress-getmax.md) . Les fournisseurs de services réinitialisent ces valeurs lorsqu'ils appellent [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md). 
  
La valeur flags est utilisée par les fournisseurs de services pour déterminer la manière dont ils doivent définir les autres valeurs. Initialisez la valeur flags sur MAPI_TOP_LEVEL et renvoyez cette valeur dans votre implémentation de **GetFlags** jusqu'à ce que le fournisseur de services la réinitialise en appelant **SetLimits**. 
  
Dans votre implémentation de la méthode **SetLimits** , enregistrez des copies locales de chacun des paramètres suivants: _lpulMin_, _lpulMax_et _lpulFlags_. Ces valeurs doivent être immédiatement disponibles lorsqu'un fournisseur de services appelle vos méthodes **GetMin**, **GetMax**ou **GetFlags** . 
  
Pour mettre à jour l'affichage de l'indicateur de progression, les fournisseurs de services appellent votre **méthode imapiprogress::P méthode rogress** . Il existe trois paramètres pour cette méthode: une valeur, un nombre et un total. Utilisez le premier paramètre, _ulValue_, pour afficher l'indicateur de progression. Le paramètre _ulValue_ est l'indicateur de progression et est égal à _ulMin_ globales uniquement au tout début de l'opération et égal à global _ulMax_ uniquement à la fin de l'opération. 
  
Utilisez les deuxième et troisième paramètres, _ulCount_ et _ulTotal_, le cas échéant, pour afficher un message facultatif tel que «5 éléments terminés sur 10». Si les deuxième et troisième paramètres sont définis sur 0, vous pouvez choisir de modifier visuellement ou non l'indicateur de progression. Certains fournisseurs de services définissent ces paramètres à zéros pour indiquer qu'ils traitent un sous-objet dont la progression est contrôlée par rapport à un objet parent. Dans ce cas, il est logique de modifier l'affichage uniquement lorsque l'objet parent indique la progression. Certains fournisseurs de services transmettent les zéros de ces paramètres à chaque fois. 
  

