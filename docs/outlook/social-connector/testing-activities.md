---
title: Activités de test
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Cette rubrique décrit les scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation de la demande pour retourner correctement les activités des amis et non amis et les tests.
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787712"
---
# <a name="testing-activities"></a>Activités de test

Cette rubrique décrit les scénarios pour vérifier que le fournisseur Outlook Social Connector (OSC) utilise la synchronisation de la demande pour retourner correctement les activités des amis et non amis et les tests.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Synchronisation de la demande

Un fournisseur OSC implémente **ISocialProvider::GetCapabilities**, qui l’OSC appelle pour déterminer si le fournisseur prend en charge la synchronisation des activités des amis et non amis sur demande. Pour les personnes affichées dans le volet personnes Outlook, obtient l’OSC et hachages leur SMTP résout, appelle [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)et stocke les données activités (en mémoire) renvoyées à ces personnes. 
  
### <a name="determining-activities-to-get"></a>Détermination des activités à obtenir

Les adresses SMTP hachage passés à **GetActivitiesEx** sont les clés pour déterminer si l’OSC obtiendrez des activités pour un ami ou un autre ami. L’OSC Obtient des activités d’une personne si la personne Spécifie l’adresse SMTP dans son compte de réseau social. Si la personne n’inclut pas d’adresse SMTP dans son compte de réseau social, ou si cette personne est un ami, mais par une autre adresse e-mail sur le réseaux sociaux, **GetActivitiesEx** n’obtient pas les activités de cette personne. Également, pour une personne qui n’est pas un ami, mais spécifie les adresses SMTP dans son compte de réseaux sociaux, les données renvoyées incluent uniquement ce qui est disponible à un non-ami autorisé par les paramètres de confidentialité de cette personne. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Création de sujets de test d’amis ou non amis

Pour créer un objet de test pour un ami, identifier l’adresse SMTP d’une personne qui inclut cette adresse dans son compte de réseau social et qui a le statut ami avec l’utilisateur connecté à ce réseau. Créer un message électronique qui contient l’adresse SMTP. De même, pour créer un objet de test pour un ami-non, identifier l’adresse SMTP d’une personne qui n’est pas un ami de l’utilisateur connecté à cette adresse, et qui a spécifié dans ses paramètres de confidentialité pour autoriser non amis afficher leur profil sur le réseaux sociaux. Créer un message électronique qui contient l’adresse SMTP. 
  
Dans l’Explorateur Outlook, lorsque vous sélectionnez le message électronique qui inclut un ami (ou non ami), le volet personnes affiche les destinataires. Sélection l’ami (ou non ami) dans le volet personnes permet à tester que le fournisseur est fournissant des informations sur la personne.
  
### <a name="test-scenarios"></a>Scénarios de test

Pour vérifier que vous obtenez les activités appropriées d’amis ou non amis, de test pour les scénarios suivants.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Personne sélectionnée dans le volet personnes est un ami avec l’utilisateur connecté sur le réseau social.  <br/> |Le volet personnes affiche le profil de cette personne et de l’image de profil comme publiés sur le réseau social.  <br/> |
|Personne sélectionnée dans le volet personnes n’est un ami de l’utilisateur connecté sur le réseau social, mais a permis à son profil par non amis.  <br/> |Le volet personnes affiche le profil de cette personne et de l’image de profil comme publiés sur le réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)  
- [XML pour les activités](xml-for-activities.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

