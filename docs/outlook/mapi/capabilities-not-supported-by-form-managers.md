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
ms.openlocfilehash: a84c0a93f80080b71f6049e73f0a0094c38c28ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566872"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Fonctionnalités non prises en charge par les gestionnaires de formulaires

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les fonctionnalités suivantes ne sont pas pris en charge par le Gestionnaire de formulaire par défaut pour des raisons de performances, mais peuvent être pris en charge par les responsables de formulaire personnalisé.
  
- Une hiérarchie qui permet les formes groupées ou de catégorie au sein d’une bibliothèque de formulaires. Une bibliothèque de formulaires est une base de données de fichiers plats des formulaires.
    
- Contrôle d’accès pour les catégories de formulaires, correspondant à des classes de message ou surclasse.
    
- Prise en charge de plusieurs versions linguistiques du même formulaire dans une bibliothèque de formulaires unique.
    
Il s’agit des problèmes de mise en œuvre. Il n’a rien à empêcher un gestionnaire de formulaires personnalisés à partir de l’implémentation de ces fonctionnalités.
  
L’architecture de formulaire MAPI ne gère pas plusieurs responsables de formulaire qui s’exécutent simultanément. Bien que MAPI prend en charge plusieurs fournisseurs de magasins message simultanés, fournisseurs de transport et fournisseurs de carnet d’adresses, seul un gestionnaire de formulaire unique est pris en charge.
  
Étant donné que le gestionnaire qu’un seul formulaire peut être exécuté à la fois, si vous implémentez un gestionnaire de formulaire personnalisé, vous devrez réimplémenter toutes les fonctionnalités du Gestionnaire de formulaire par défaut dont vous avez besoin. Le Gestionnaire de votre formulaire personnalisé remplacera entièrement du Gestionnaire de formulaire par défaut, les fonctionnalités du Gestionnaire de formulaire par défaut ne seront pas disponibles, sauf si elles sont dupliqués dans le Gestionnaire de votre formulaire personnalisé.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

