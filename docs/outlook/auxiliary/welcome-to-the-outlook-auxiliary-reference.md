---
title: Bienvenue dans la référence auxiliaire Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: La référence auxiliaire Outlook contient un contenu conceptuel et une documentation de référence pour quatre jeux d'API, des exemples de code et un programme d'installation redistribuable qui permet aux développeurs d'étendre et d'intégrer Outlook. Les API de cette référence sont exposées par Outlook pour l'extensibilité, en dehors du modèle objet Outlook.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328979"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Bienvenue dans la référence auxiliaire Outlook

La référence auxiliaire Outlook contient un contenu conceptuel et une documentation de référence pour quatre jeux d'API, des exemples de code et un programme d'installation redistribuable qui permet aux développeurs d'étendre et d'intégrer Outlook. Les API de cette référence sont exposées par Outlook pour l'extensibilité, en dehors du modèle objet Outlook. 
  
Si vous débutez en tant que développeur de solutions pour Outlook, consultez [Sélection d'une API ou d'une technologie pour développer des solutions pour Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) pour identifier les API et technologies les plus adaptées à vos besoins. 

Pour obtenir des informations spécifiques sur le modèle objet Outlook, consultez la rubrique [référence VBA Outlook](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Pour obtenir des informations spécifiques sur l'API de messagerie (MAPI) prises en charge par Outlook, consultez la rubrique [référence MAPI pour Outlook](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Fond 

La discussion conceptuelle inclut les sujets suivants:
  
- [À propos des paramètres anti-spam](about-anti-spam-settings.md)
    
- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [À propos de la résolution de conflit pour les types d’éléments personnalisés](about-conflict-resolution-for-custom-item-types.md)
    
- [À propos de l'heure de la dernière mise à jour d'un carnet d'adresses en mode hors connexion](about-the-last-update-time-of-an-offline-address-book.md)
    
- [À propos de l’inscription d’un nouveau domaine pour la configuration automatique](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [À propos des demandes de réunion sous la forme d'informations mises à jour et mises à jour intégrales](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [À propos de la relocalisation des calendriers par programme pour l'heure d'été](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Il existe également un programme d'installation redistribuable pour les outils de relocalisation de calendrier tiers, qui fonctionne également pour les versions antérieures d'Outlook, depuis Outlook 2010. Pour télécharger le programme d'installation, consultez la rubrique [relative aux fichiers d'en-tête Outlook 2010: référence auxiliaire redistribuable et fichier d'en-tête pour les calendriers de](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)relocalisation.
    
- [À propos de persistance TZDEFINITION dans un flux de valider une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Référence

Le contenu de référence inclut les éléments suivants:
  
- Les [API exportées par Outlook](about-apis-exported-by-outlook.md) incluent des fonctions et des structures de données qui ont été implémentées à l'origine pour un usage interne et qui sont désormais exposées pour une utilisation publique. 
    
- L' [API de gestion des comptes](about-the-account-management-api.md) fournit l'accès aux informations de compte d'utilisateur et aux notifications des modifications de compte. 
    
- L' [API de couche](about-the-data-degradation-layer-api.md) de dégradation des données prend en charge les clients qui accèdent à un élément Outlook dans un format de caractères préféré plutôt que dans le format de caractères natif de l'objet. 
    
- L' [API](about-the-free-busy-api.md) de disponibilité fournit des informations de disponibilité sur des comptes d'utilisateurs spécifiques dans un intervalle de temps donné. 

## <a name="sample-tasks"></a>Exemples de tâches

Les exemples de tâches dans la référence auxiliaire Outlook sont les suivants:
    
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
    
La référence de chaque API répertorie les constantes, les définitions de types et les interfaces qu'un développeur doit implémenter pour utiliser les fonctionnalités supplémentaires.
  
> [!NOTE]
> Les développeurs doivent implémenter ces API uniquement comme indiqué dans cette référence. Certains paramètres des membres de l'interface et de la méthode sont nommés comme espaces réservés, car ils sont réservés à l'usage interne d'Outlook et peuvent faire l'objet de modifications sans préavis. 
  

