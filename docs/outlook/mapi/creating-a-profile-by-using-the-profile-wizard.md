---
title: Création d'un profil à l'aide de l'Assistant Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411735"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Création d'un profil à l'aide de l'Assistant Profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'Assistant Profil est une fonctionnalité MAPI qui permet à un utilisateur de créer un profil de la manière la plus simple possible. L'Assistant Profil affiche une série de boîtes de dialogue qui demandent à l'utilisateur de sélectionner les services de messagerie et d'entrer des valeurs pour certaines des propriétés de configuration les plus importantes. Pour la plupart des autres propriétés requises, l'Assistant Profil utilise les valeurs par défaut fournies. Pour appeler l'Assistant Profil, appelez **LaunchWizard**, une fonction basée sur le prototype [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
L'utilisateur peut ajouter uniquement les services de messagerie et les fournisseurs de services au nouveau profil qui prend en charge l'Assistant Profil. Étant donné que chaque service de messagerie peut nécessiter plus de propriétés que l'Assistant Profil ne peut gérer, sachez que si vous utilisez cette approche, il est possible qu'un ou plusieurs des services ou fournisseurs sélectionnés ne soient pas configurés de manière incomplète.
  

