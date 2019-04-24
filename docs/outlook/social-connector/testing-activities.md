---
title: Test des activités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Cette rubrique décrit les tests et les scénarios permettant de vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation à la demande pour retourner correctement les activités des amis et des non-amis.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329182"
---
# <a name="testing-activities"></a>Test des activités

Cette rubrique décrit les tests et les scénarios permettant de vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation à la demande pour retourner correctement les activités des amis et des non-amis.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Un fournisseur OSC implémente **ISocialProvider:: GetCapabilities**, que l'OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation à la demande des activités des amis et des non-amis. Pour les personnes affichées dans le volet Outlook, le OSC Obtient et hache leurs adresses SMTP, appelle [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)et stocke (en mémoire) les données d'activités renvoyées pour ces personnes. 
  
### <a name="determining-activities-to-get"></a>Détermination des activités à obtenir

Les adresses SMTP hachées transmises à **GetActivitiesEx** sont la clé permettant de déterminer si OSC obtiendra des activités pour un ami ou un non-ami. Le OSC obtient des activités pour une personne si la personne spécifie que l'adresse SMTP est dans son compte de réseau social. Si la personne n'inclut pas l'adresse SMTP dans son compte de réseau social, ou si cette personne est un ami, mais par une adresse de messagerie différente sur le réseau social, **GetActivitiesEx** n'obtient pas d'activités pour cette personne. Par ailleurs, pour une personne qui n'est pas un ami mais qui spécifie les adresses SMTP dans son compte de réseau social, les données renvoyées incluent uniquement ce qui est disponible pour un non-Friend, comme autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test pour des amis et des non-amis

Pour créer un objet de test pour un ami, identifiez l'adresse SMTP d'une personne qui inclut cette adresse dans son compte de réseau social et qui a un État Friend avec l'utilisateur connecté sur ce réseau. Créez un message électronique qui inclut cette adresse SMTP. De la même manière, pour créer un objet de test pour un non-ami, identifiez l'adresse SMTP d'une personne qui n'est pas un ami de l'utilisateur connecté par cette adresse, et qui a spécifié dans ses paramètres de confidentialité pour autoriser les personnes non friendes à afficher son profil sur le réseau social. Créez un message électronique qui inclut cette adresse SMTP. 
  
Dans l'explorateur Outlook, lorsque vous sélectionnez le message électronique qui comprend un ami (ou non un ami), le volet contacts affiche les destinataires. La sélection de l'option Friend (ou non-Friend) dans le volet contacts vous permet de vérifier que le fournisseur fournit des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que vous obtenez des activités appropriées pour des amis et des non-amis, testez les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Personne sélectionnée dans le volet de personnes est un ami avec l'utilisateur connecté sur le réseau social.  <br/> |Le volet de contacts affiche l'image de profil et de profil de cette personne sous la forme publiée sur le réseau social.  <br/> |
|Personne sélectionnée dans le volet de personnes est un non-ami de l'utilisateur connecté au réseau social, mais a autorisé son profil à être visualisé par des non-Friends.  <br/> |Le volet de contacts affiche l'image de profil et de profil de cette personne sous la forme publiée sur le réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)  
- [XML pour les activités](xml-for-activities.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

