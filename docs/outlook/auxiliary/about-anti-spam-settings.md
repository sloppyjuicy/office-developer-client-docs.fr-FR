---
title: À propos des paramètres anti-courrier indésirable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permet aux utilisateurs de spécifier les paramètres pour chaque compte pour vous aider à protéger le compte du courrier indésirable. Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil utilisateur.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390379"
---
# <a name="about-anti-spam-settings"></a>À propos des paramètres anti-courrier indésirable

Outlook permet aux utilisateurs de spécifier les paramètres pour chaque compte pour vous aider à protéger le compte du courrier indésirable. Ces paramètres anti-courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil utilisateur. Utilisez la propriété [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) pour obtenir l’ID unique (UID) de la section dans le profil qui stocke les préférences de l’utilisateur pour ce compte, y compris les paramètres de blocage du courrier indésirable. 
  
Pour obtenir les paramètres de blocage du courrier indésirable pour le compte, utilisez les propriétés suivantes :
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié en tant que des expéditeurs bloqués pour le compte.
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— Spécifie le niveau de filtrage que l’utilisateur a spécifié pour le compte. Le tableau suivant présente les valeurs prises en charge.
    
|Valeur prise en charge |Définition |
|:-----|:-----|
|Aucune  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Moyenne  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié comme destinataires approuvés pour le compte.
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— spécifie une liste délimitée par des points-virgules d’adresses de messagerie et les domaines qui l’utilisateur a spécifié comme des expéditeurs approuvés pour le compte.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Ajouter des noms aux listes de filtre de courrier indésirable](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

