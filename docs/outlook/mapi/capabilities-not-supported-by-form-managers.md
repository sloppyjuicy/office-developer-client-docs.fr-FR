---
title: Fonctionnalités non pris en charge par les gestionnaires de formulaires
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
# <a name="capabilities-not-supported-by-form-managers"></a>Fonctionnalités non pris en charge par les gestionnaires de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fonctionnalités suivantes ne sont pas pris en charge par le gestionnaire de formulaires par défaut pour des raisons de performances, mais peuvent être pris en charge par les gestionnaires de formulaires personnalisés.
  
- Hiérarchie qui permet de grouper ou de classer les formulaires dans une bibliothèque de formulaires. Une bibliothèque de formulaires est une base de données de formulaires à fichier plat.
    
- Contrôle d’accès pour les catégories de formulaires, correspondant aux classes de messages ou aux superclasses.
    
- Prise en charge de plusieurs versions linguistiques du même formulaire dans une seule bibliothèque de formulaires.
    
Il s’est question de problèmes d’implémentation. Rien n’empêche un gestionnaire de formulaires personnalisé d’implémenter ces fonctionnalités.
  
L’architecture de formulaire MAPI ne prend pas en charge plusieurs gestionnaires de formulaires qui s’exécutent simultanément. Bien que MAPI prend en charge plusieurs fournisseurs de magasins de messages, fournisseurs de transport et fournisseurs de carnets d’adresses simultanés, un seul gestionnaire de formulaires est pris en charge.
  
Étant donné qu’un seul gestionnaire de formulaire peut être en cours d’exécution en même temps, si vous implémentez un gestionnaire de formulaires personnalisé, vous devrez ré-implémenter les fonctionnalités du gestionnaire de formulaires par défaut dont vous avez besoin. Étant donné que votre gestionnaire de formulaires personnalisé remplacera entièrement le gestionnaire de formulaires par défaut, les fonctionnalités du gestionnaire de formulaires par défaut ne seront pas disponibles, sauf si elles sont dupliquées dans votre gestionnaire de formulaires personnalisé.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

