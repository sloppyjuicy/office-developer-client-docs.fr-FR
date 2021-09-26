---
title: Création d’un profil à l’aide de l’Assistant Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: eed28b64effa080a604e1ea97ddf5911796e07ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631033"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Création d’un profil à l’aide de l’Assistant Profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’Assistant Profil est une fonctionnalité MAPI qui permet à un utilisateur de créer un profil de la manière la plus simple possible. L’Assistant Profil affiche une série de boîtes de dialogue qui invitent l’utilisateur à sélectionner les services de message et à entrer des valeurs pour quelques-unes des propriétés de configuration les plus essentielles. Pour la plupart des autres propriétés requises, l’Assistant Profil utilise les valeurs par défaut fournies. Pour appeler l’Assistant Profil, **appelez LaunchWizard**, une fonction basée sur le prototype [LAUNCHWIZARDENTRY.](launchwizardentry.md) 
  
L’utilisateur peut ajouter uniquement ces services de messagerie et fournisseurs de services au nouveau profil qui permet de prendre en charge l’Assistant Profil. Étant donné que chaque service de messagerie peut nécessiter plus de propriétés que ce que l’Assistant Profil peut gérer, sachez que si vous utilisez cette approche, un ou plusieurs des services ou fournisseurs sélectionnés peuvent être configurés de manière incomplète.
  

