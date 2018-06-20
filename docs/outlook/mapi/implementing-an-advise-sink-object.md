---
title: L’implémentation d’un objet de réception de notifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a95222f8ec75c519558636cf54111f28cbe14066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784174"
---
# <a name="implementing-an-advise-sink-object"></a>L’implémentation d’un objet de réception de notifications

  
  
**S’applique à**: Outlook 
  
Un client peut implémenter ses propres objets du récepteur advise ou utiliser une fonction utilitaire, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crée un objet de récepteur advise avec une implémentation **OnNotify** qui appelle une fonction de rappel. 
  
Il existe des avantages et inconvénients **HrAllocAdviseSink**. Il peut enregistrer le travail, mais il ne permet de contrôler aucun décompte de l’objet récepteur advise qu’il crée. Par conséquent, les clients qui ont besoin de contrôler avec soin version du récepteur de leurs notifications ou qui ont des interdépendances entre leur récepteur de notifications et un autre objet client doivent créer leur propre implémentation **IMAPIAdviseSink** et éviter d’utiliser ** HrAllocAdviseSink** complètement. 
  
Un client de mise en œuvre son propre récepteur de notifications doit rendre un objet indépendant non liés aux ou dépendent d’autres objets afin d’éliminer les problèmes potentiels de version de comptage et l’objet de référence. Toutefois, si vous devez implémenter votre récepteur de notifications dans le cadre d’un autre objet ou inclure un pointeur vers un autre objet en tant que membre de données arrière, il est recommandé que deux le nombre de référence séparée est mis à jour : un pour l’objet référencé par le récepteur de notifications et un pour le récepteur de notification. 
  
Lorsque le décompte de références de l’objet référencé tombe à zéro, tous ses méthodes peuvent échouer et ses vtable peut être détruit, mais la mémoire pour le récepteur de notifications doit conservés jusqu'à après que son décompte de références également descend à zéro. Cela signifie que méthode de **publication** du récepteur advise doit décrémente le décompte de références et terminer la destruction de l’objet lorsque ce décompte atteint zéro. Si les deux comptes de référence distincts ne sont pas conservées, il est facile de détruire accidentellement le récepteur de notifications dans le cadre du processus de **publication** de l’objet de niveau supérieur. 
  
Clients à l’aide de **HrAllocAdviseSink** pour implémenter un récepteur de notifications doivent être également veiller à ne pas inclure de leur fonction de rappel en tant que méthode dans un autre objet récepteur de notifications. Pour les clients C++, il est tentant de faire passer le pointeur _this_ comme paramètre. Il s’agit d’une stratégie dangereuse parce que les clients libèrent généralement un objet lorsque son décompte de références atteint zéro. Libérer de la mémoire pour l’objet de récepteur advise se rendre le pointeur _this_ non valide. 
  
Selon le type d’événement et la source de notifications, votre méthode **OnNotify** peut gérer les événements de différentes manières. Le tableau suivant propose des suggestions sur la façon de gérer certains événements standards. 
  
|**Type d’événement**|**Gestion de OnNotify**|
|:-----|:-----|
|Objet déplacé  <br/> |Si le parent d’origine de l’objet déplacé est lié au nouveau parent, mettre à jour le début de l’affichage du dossier ou du conteneur de carnet d’adresses la plus élevée dans la hiérarchie. Si les conteneurs deux parents ne sont pas liés, mettre à jour de leur point de vue.  <br/> |
|Nouveau message  <br/> |Modifier l’interface utilisateur pour informer l’utilisateur de l’arrivée d’un ou plusieurs nouveaux messages. Placez le dossier de réception dans l’affichage actuel.  <br/> |
|Erreur  <br/> |Pour tous les objets à l’exception de la session, ouvrez une session l’erreur si nécessaire et de retour. Pour l’objet session, fermez la session, si possible.  <br/> |
|Recherche terminée  <br/> |Aucun traitement n’est nécessaire.  <br/> |
   
> [!NOTE]
> Gestionnaires de notification doivent être réentrants. 
  

