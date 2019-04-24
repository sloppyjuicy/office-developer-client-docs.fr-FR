---
title: Test du suivi et de l’arrêt de suivi de personnes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Cette rubrique décrit les scénarios permettant de tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter de suivre un ami sur le réseau social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316015"
---
# <a name="testing-following-and-stop-following-persons"></a>Test du suivi et de l’arrêt de suivi de personnes

Cette rubrique décrit les scénarios permettant de tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter de suivre un ami sur le réseau social.
  
## <a name="following-a-person"></a>Suivi d'une personne

Pour suivre une personne, il faut ajouter une personne en tant qu'ami sur le réseau social, à l'aide de l'adresse SMTP fournie par l'élément Outlook sélectionné. Le suivi d'une personne sur un réseau social implique généralement de demander l'autorisation de cette personne par un message électronique à cette adresse SMTP. Pour accorder l'autorisation, cette personne doit avoir cette adresse SMTP déjà incluse dans son compte de réseau social ou être disposé à ajouter ce protocole SMTP à un compte de réseau social. Testez chacun des scénarios suivants pour vérifier que votre fournisseur OSC se comporte correctement.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Tentative de suivi d'une personne sur le réseau social qui existe sur le réseau social.  <br/> |Pour un réseau social qui n'a pas besoin d'autorisation de la part de la personne, le réseau social ajoute immédiatement la personne en tant qu'ami.  <br/> Pour un réseau qui requiert une autorisation de la part de cette personne, le réseau social envoie une notification. Le volet contacts Outlook affiche une icône en attente pour cette personne.  <br/> |
|Tentative de suivi d'une personne sur le réseau social qui n'existe pas sur le réseau social.  <br/> |Le fournisseur OSC affiche l'erreur appropriée dans [ISocialSession:: followPerson](isocialsession-followperson.md) ou [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Suivi d'un ami sur le réseau social.  <br/> |Pour l'ami sélectionné dans le volet personnes, le badge du réseau social et l'image de profil de l'ami pour ce réseau social sont affichés.  <br/> |
|Sélection du lien vers la page de profil d'un ami.  <br/> |La page de l'ami sur le réseau social s'ouvre dans le navigateur par défaut de l'utilisateur connecté.  <br/> |
   
## <a name="stop-following-a-person"></a>Arrêter le suivi d'une personne

Pour arrêter le suivi d'une personne, vous pouvez la supprimer en tant qu'ami sur le réseau social. Testez le scénario suivant pour vérifier que votre fournisseur OSC cesse de suivre correctement une personne.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Tentative de suppression d'une personne en tant qu'ami sur le réseau social.  <br/> |Le réseau social ne répertorie plus cette personne en tant qu'ami sur le compte de l'utilisateur connecté.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

