---
title: Test du suivi et de l’arrêt de suivi de personnes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter le suivi d’un ami sur le réseau social.
ms.openlocfilehash: 8f599214b8b8bc42f7aad38c06db3c9a5a7b9888
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773032"
---
# <a name="testing-following-and-stop-following-persons"></a>Test du suivi et de l’arrêt de suivi de personnes

Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter le suivi d’un ami sur le réseau social.
  
## <a name="following-a-person"></a>Suivi d’une personne

Suivre une personne consiste à ajouter une personne en tant qu’ami sur le réseau social, à l’aide de l’adresse SMTP fournie par l’élément Outlook sélectionné. Le suivi d’une personne sur un réseau social implique généralement de demander l’autorisation à cette personne par courrier électronique à cette adresse SMTP. Pour accorder l’autorisation, cette personne doit avoir cette adresse SMTP déjà incluse dans son compte de réseau social ou être prête à ajouter ce SMTP à un compte de réseau social. Testez chacun des scénarios suivants pour vérifier que votre fournisseur OSC se comporte correctement.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Tentative de suivi d’une personne sur le réseau social qui existe sur le réseau social. |Pour un réseau social qui ne nécessite pas d’autorisation de la personne, le réseau social l’ajoute immédiatement en tant qu’ami. Pour un réseau qui requiert l’autorisation de cette personne, le réseau social envoie une notification. Le Outlook Personnes affiche une icône en attente pour cette personne. |
|Tentative de suivi d’une personne sur le réseau social qui n’existe pas sur le réseau social. |Le fournisseur OSC affiche l’erreur appropriée dans [ISocialSession::FollowPerson](isocialsession-followperson.md) ou [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md). |
|Suivi d’un ami sur le réseau social. |Pour l’ami sélectionné dans le volet Personnes, le badge du réseau social et l’image de profil de l’ami pour ce réseau social sont affichés. |
|Sélection du lien vers la page de profil d’un ami. |La page de l’ami sur le réseau social s’ouvre dans le navigateur par défaut de l’utilisateur connecté. |
   
## <a name="stop-following-a-person"></a>Arrêter le suivi d’une personne

Arrêter le suivi d’une personne consiste à supprimer cette personne en tant qu’ami sur le réseau social. Testez le scénario suivant pour vérifier que votre fournisseur OSC cesse de suivre une personne correctement.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Tentative de suppression d’une personne en tant qu’ami sur le réseau social. |Le réseau social ne répertorie plus cette personne en tant qu’ami sur le compte de l’utilisateur connecté. |
   
## <a name="see-also"></a>Voir aussi

- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

