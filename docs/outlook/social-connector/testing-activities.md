---
title: Test des activités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Cette rubrique décrit des tests et des scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation à la demande pour retourner correctement les activités des amis et des non-amis.
ms.openlocfilehash: 63ddee94e28e7b8dfcb5d616069df2c275d41587
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582987"
---
# <a name="testing-activities"></a>Test des activités

Cette rubrique décrit des tests et des scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation à la demande pour retourner correctement les activités des amis et des non-amis.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Un fournisseur OSC implémente **ISocialProvider::GetCapabilities**, que l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation à la demande des activités des amis et des non-amis. Pour les personnes affichées dans le volet Personnes de Outlook, l’OSC obtient et hait ses adresses SMTP, appelle [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)et stocke (en mémoire) les données d’activités renvoyées pour ces personnes. 
  
### <a name="determining-activities-to-get"></a>Détermination des activités à obtenir

Les adresses SMTP hachées transmises à **GetActivitiesEx** sont essentielles pour déterminer si l’OSC aura des activités pour un ami ou un non-ami. L’OSC obtient les activités d’une personne si celle-ci spécifie cette adresse SMTP dans son compte de réseau social. Si la personne n’inclut pas cette adresse SMTP dans son compte de réseau social, ou si cette personne est un ami mais par une adresse de messagerie différente sur le réseau social, **GetActivitiesEx** n’a pas d’activités pour cette personne. En outre, pour une personne qui n’est pas un ami mais qui spécifie les adresses SMTP dans son compte de réseau social, les données renvoyées incluent uniquement ce qui est disponible pour un non-ami comme autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test pour des amis et des non-amis

Pour créer un sujet de test pour un ami, identifiez l’adresse SMTP d’une personne qui inclut cette adresse dans son compte de réseau social et qui a un statut d’ami avec l’utilisateur connecté sur ce réseau. Créez un message électronique qui inclut cette adresse SMTP. De même, pour créer un sujet de test pour un non-ami, identifiez l’adresse SMTP d’une personne qui n’est pas un ami de l’utilisateur connecté par cette adresse et qui a spécifié dans ses paramètres de confidentialité pour permettre aux non-amis d’afficher leur profil sur le réseau social. Créez un message électronique qui inclut cette adresse SMTP. 
  
Dans l Outlook’explorateur, lorsque vous sélectionnez le message électronique qui inclut un ami (ou un non-ami), le volet Personnes affiche les destinataires. La sélection de l’ami (ou non- ami) dans le volet Personnes vous permet de tester que le fournisseur fournit des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que vous êtes en train d’obtenir les activités appropriées pour les amis et les non-amis, testez les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|La personne sélectionnée dans le volet Personnes est un ami de l’utilisateur connecté sur le réseau social.  <br/> |Le volet Personnes affiche le profil et l’image de profil de cette personne tel qu’il est publié sur le réseau social.  <br/> |
|La personne sélectionnée dans le volet Personnes est un non-ami de l’utilisateur connecté sur le réseau social, mais a autorisé son profil à être consultable par des non-amis.  <br/> |Le volet Personnes affiche le profil et l’image de profil de cette personne tel qu’il est publié sur le réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)  
- [XML pour les activités](xml-for-activities.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

