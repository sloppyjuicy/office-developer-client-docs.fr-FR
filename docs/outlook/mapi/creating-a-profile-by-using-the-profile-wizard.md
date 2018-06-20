---
title: Création d’un profil à l’aide de l’Assistant profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783103"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Création d’un profil à l’aide de l’Assistant profil

  
  
**S’applique à**: Outlook 
  
L’Assistant profil est une fonctionnalité MAPI qui permet à un utilisateur de créer un profil dans le plus simple possible. L’Assistant profil affiche une série de boîtes de dialogue qui invite l’utilisateur à sélectionner les services de messagerie et entrez des valeurs pour quelques-unes des propriétés essentielles de configuration. Pour la plupart des autres propriétés requises, l’Assistant profil utilise les valeurs par défaut fournies. Pour appeler l’Assistant profil, appelez **LaunchWizard**, une fonction basée sur le prototype [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
L’utilisateur peut ajouter uniquement les services de messagerie et les fournisseurs de services pour le nouveau profil qui prennent en charge de l’Assistant profil. Étant donné que chaque service de message peut nécessiter plus de propriétés à définir que l’Assistant profil peut gérer, sachez que si vous utilisez cette approche, il est possible pour une ou plusieurs des services sélectionnés ou des fournisseurs pour incomplète.
  

