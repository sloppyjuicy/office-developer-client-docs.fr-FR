---
title: Bienvenue dans la Outlook auxiliaire
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: La référence auxiliaire Outlook contient du contenu conceptuel et de la documentation de référence pour quatre ensembles d’API, des exemples de code et un programme d’installation redistribuable qui permettent aux développeurs d’étendre et d’intégrer les Outlook. Les API de cette référence sont exposées Outlook pour l’extensibilité, en dehors Outlook modèle objet.
ms.openlocfilehash: 478dbf3057972b01a453d2dda105135c25517607
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564489"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Bienvenue dans la Outlook auxiliaire

La référence auxiliaire Outlook contient du contenu conceptuel et de la documentation de référence pour quatre ensembles d’API, des exemples de code et un programme d’installation redistribuable qui permettent aux développeurs d’étendre et d’intégrer les Outlook. Les API de cette référence sont exposées Outlook pour l’extensibilité, en dehors Outlook modèle objet. 
  
Si vous débutez en tant que développeur de solutions pour Outlook, consultez [Sélection d'une API ou d'une technologie pour développer des solutions pour Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) pour identifier les API et technologies les plus adaptées à vos besoins. 

Pour obtenir des informations spécifiques sur Outlook modèle objet, voir la [Outlook VBA.](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) 

Pour plus d’informations sur l’API de messagerie (MAPI) prise en charge par Outlook, voir la Outlook [référence MAPI .](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)

## <a name="conceptual"></a>Conceptuel 

La discussion conceptuelle comprend les sujets suivants :
  
- [À propos des paramètres anti-spam](about-anti-spam-settings.md)
    
- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [À propos de la résolution de conflit pour les types d’éléments personnalisés](about-conflict-resolution-for-custom-item-types.md)
    
- [À propos de l’heure de la dernière mise à jour d’un carnet d’adresses en mode hors connexion](about-the-last-update-time-of-an-offline-address-book.md)
    
- [À propos de l’inscription d’un nouveau domaine pour la configuration automatique](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [À propos des demandes de réunion sous la forme d'informations mises à jour et mises à jour intégrales](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- À propos de la [rebasing](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) de calendriers par programme pour l’heure d’été (il existe également un programme d’installation redistribuable pour les outils de rebasing de calendrier tiers, qui fonctionne également pour les versions précédentes de Outlook, depuis Outlook 2010. Pour télécharger le programme d’installation, [voir Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Référence

Le contenu de référence inclut les suivants :
  
- Les [API exportées](about-apis-exported-by-outlook.md) par Outlook incluent des fonctions et des structures de données qui ont été initialement implémentées pour une utilisation interne et sont désormais exposées pour une utilisation publique. 
    
- [L’API de gestion des](about-the-account-management-api.md) comptes permet d’accéder aux informations de compte d’utilisateur et aux notifications de modifications de compte. 
    
- [L’API de couche](about-the-data-degradation-layer-api.md) de dégradation des données prend en charge les clients qui accèdent à un Outlook dans un format de caractère préféré plutôt que dans le format de caractère natif de l’objet. 
    
- [L’API de libre/occupé](about-the-free-busy-api.md) fournit des informations d’état de libre/occupé sur des comptes d’utilisateurs spécifiques dans un délai spécifique. 

## <a name="sample-tasks"></a>Exemples de tâches

Les exemples de tâches de la Outlook auxiliaire sont les suivants :
    
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
    
La référence pour chaque API répertorie les constantes, définitions de types et interfaces qu’un développeur doit implémenter pour utiliser les fonctionnalités supplémentaires.
  
> [!NOTE]
> Les développeurs doivent implémenter ces API uniquement comme documenté dans cette référence. Certains membres d’interface et paramètres de méthode sont nommés comme espaces réservés, car ils sont réservés à l’utilisation interne de Outlook et peuvent être changés sans préavis. 
  

