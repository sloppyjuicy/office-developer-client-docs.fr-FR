---
title: Fonctionnalités non prises en charge par les gestionnaires de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419379"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Fonctionnalités non prises en charge par les gestionnaires de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fonctionnalités suivantes ne sont pas prises en charge par le gestionnaire de formulaire par défaut pour des raisons de performances, mais peuvent être prises en charge par les gestionnaires de formulaires personnalisés.
  
- Hiérarchie qui permet de regrouper ou de classer les formulaires dans une bibliothèque de formulaires. Une bibliothèque de formulaires est une base de données de formulaires à fichier plat.
    
- Contrôle d'accès pour les catégories de formulaires, correspondant aux classes de message ou aux superclasses.
    
- Prise en charge de plusieurs versions linguistiques du même formulaire dans une seule bibliothèque de formulaires.
    
Il s'agit des problèmes d'implémentation. Il n'y a rien à empêcher un gestionnaire de formulaires personnalisés d'implémenter ces fonctionnalités.
  
L'architecture des formulaires MAPI ne prend pas en charge plusieurs gestionnaires de formulaires exécutés simultanément. Bien que MAPI prenne en charge plusieurs fournisseurs de banques de messages simultanées, fournisseurs de transport et fournisseurs de carnet d'adresses, un seul gestionnaire de formulaires est pris en charge.
  
Étant donné qu'un seul gestionnaire de formulaires peut s'exécuter en même temps, si vous implémentez un gestionnaire de formulaires personnalisés, vous devrez réimplémenter toutes les fonctionnalités du gestionnaire de formulaires par défaut dont vous avez besoin. Étant donné que votre gestionnaire de formulaires personnalisés remplacera entièrement le gestionnaire de formulaires par défaut, les fonctionnalités du gestionnaire de formulaires par défaut ne seront pas disponibles, sauf s'ils sont dupliqués dans votre gestionnaire de formulaires personnalisés.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

