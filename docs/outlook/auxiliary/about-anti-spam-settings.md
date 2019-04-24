---
title: À propos des paramètres anti-courrier indésirable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permet aux utilisateurs de spécifier des paramètres pour chaque compte afin de protéger le compte du courrier indésirable. Ces paramètres de blocage du courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil de l'utilisateur.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316960"
---
# <a name="about-anti-spam-settings"></a>À propos des paramètres anti-courrier indésirable

Outlook permet aux utilisateurs de spécifier des paramètres pour chaque compte afin de protéger le compte du courrier indésirable. Ces paramètres de blocage du courrier indésirable sont stockés dans une section désignée pour ce compte dans le profil de l'utilisateur. Utilisez la propriété [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) pour obtenir l'ID unique (UID) de la section dans le profil qui stocke les préférences de l'utilisateur pour ce compte, y compris les paramètres anti-courrier indésirable. 
  
Utilisez les propriétés suivantes pour obtenir les paramètres de blocage du courrier indésirable pour le compte:
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx): spécifie une liste d'adresses de messagerie et de domaines séparés par des points-virgules que l'utilisateur a spécifié en tant qu'expéditeurs bloqués pour le compte.
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— spécifie le niveau de filtrage du courrier indésirable spécifié par l'utilisateur pour le compte. Le tableau suivant indique les valeurs prises en charge.
    
|Valeur prise en charge |Définition |
|:-----|:-----|
|Aucun  <br/> |Égale  <br/> |
|Faible  <br/> |0x00000006  <br/> |
|Moyenne  <br/> |0x00000005  <br/> |
|Importante  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx): spécifie une liste délimitée par des points-virgules d'adresses de messagerie et de domaines que l'utilisateur a spécifiés comme destinataires approuvés pour le compte.
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx): spécifie une liste délimitée par des points-virgules d'adresses de messagerie et de domaines que l'utilisateur a spécifiés comme expéditeurs approuvés pour le compte.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Ajouter des noms aux listes de filtres de courrier inDésirable](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

