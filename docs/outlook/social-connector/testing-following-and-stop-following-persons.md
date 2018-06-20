---
title: Test des personnes suivantes et stop-suivant
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et pour arrêter le suivi d’un ami sur le réseaux sociaux.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787701"
---
# <a name="testing-following-and-stop-following-persons"></a>Test des personnes suivantes et stop-suivant

Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et pour arrêter le suivi d’un ami sur le réseaux sociaux.
  
## <a name="following-a-person"></a>Suivi d’une personne

Pour suivre une personne consiste à ajouter une personne comme un ami sur le réseaux sociaux, à l’aide de l’adresse SMTP fourni par l’élément Outlook sélectionné. Une personne suit généralement sur un réseau social implique la demande d’autorisation de cette personne par un message électronique à cette adresse SMTP. Pour accorder l’autorisation, cette personne doit avoir déjà incluse dans son compte de réseau social d’adresse SMTP, soit être prêt à ajouter à un compte de réseau social SMTP. Tester chacune des scénarios suivants pour vérifier que votre fournisseur OSC se comporte correctement.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Essayez de suivre une personne sur le réseau social qui existe sur le réseau social.  <br/> |Pour un réseau social qui ne nécessite pas l’autorisation de la personne, le réseaux sociaux ajoute immédiatement la personne comme un ami.  <br/> Pour un réseau qui requiert une autorisation de cette personne, le réseaux sociaux envoie une notification. Le volet personnes Outlook affiche une icône en attente pour cette personne.  <br/> |
|Essayez de suivre une personne sur le réseau social qui n’existe pas sur le réseaux sociaux.  <br/> |Le fournisseur OSC permet d’afficher l’erreur appropriée [ISocialSession::FollowPerson](isocialsession-followperson.md) ou [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Suivi d’un ami sur le réseaux sociaux.  <br/> |Pour l’ami sélectionné dans le volet personnes, badge du réseau social et l’image de profil d’un ami pour ce réseau social sont également affichés.  <br/> |
|Sélectionnez le lien vers la page de profil d’un ami.  <br/> |Page d’un ami sur le réseau social s’ouvre dans le navigateur par défaut de l’utilisateur connecté.  <br/> |
   
## <a name="stop-following-a-person"></a>Arrêter le suivi d’une personne

Pour arrêter le suivi d’une personne consiste à supprimer cette personne comme un ami sur le réseaux sociaux. Testez le scénario suivant pour vérifier votre cesse de fournisseur OSC correctement suivi d’une personne.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Tentative de suppression d’une personne comme un ami sur le réseaux sociaux.  <br/> |Le réseaux sociaux répertorie n’est plus cette personne comme un ami sur le compte de l’utilisateur connecté.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

