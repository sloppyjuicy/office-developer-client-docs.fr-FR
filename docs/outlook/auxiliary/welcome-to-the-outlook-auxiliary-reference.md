---
title: Bienvenue dans la référence auxiliaire Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: L’autre référence Outlook contient contenu conceptuel et la documentation de référence pour les quatre ensembles d’API, les exemples de code et un programme d’installation redistribuable qui permettent aux développeurs d’étendre et d’intégration avec Outlook. API de cette référence est exposés par Outlook pour l’extensibilité, à l’extérieur du modèle objet Outlook.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384555"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Bienvenue dans la référence auxiliaire Outlook

L’autre référence Outlook contient contenu conceptuel et la documentation de référence pour les quatre ensembles d’API, les exemples de code et un programme d’installation redistribuable qui permettent aux développeurs d’étendre et d’intégration avec Outlook. API de cette référence est exposés par Outlook pour l’extensibilité, à l’extérieur du modèle objet Outlook. 
  
Si vous débutez en tant que développeur de solutions pour Outlook, consultez [Sélection d'une API ou d'une technologie pour développer des solutions pour Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) pour identifier les API et technologies les plus adaptées à vos besoins. 

Pour obtenir des informations spécifiques sur le modèle objet Outlook, voir la [référence VBA pour Outlook](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Pour plus d’informations sur MAPI (Messaging API) pris en charge par Outlook, voir la [Référence MAPI Outlook](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Conceptuelles 

La discussion conceptuelle inclut les sujets suivants :
  
- [À propos des paramètres anti-spam](about-anti-spam-settings.md)
    
- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [À propos de la résolution de conflit pour les types d’éléments personnalisés](about-conflict-resolution-for-custom-item-types.md)
    
- [À propos de l’heure de la dernière mise à jour d’un carnet d’adresse en mode hors connexion](about-the-last-update-time-of-an-offline-address-book.md)
    
- [À propos de l’inscription d’un nouveau domaine pour la configuration automatique](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [À propos des demandes de réunion sous la forme d'informations mises à jour et mises à jour intégrales](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [À propos des calendriers de redéfinition par programme à l’heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Il existe également un programme d’installation redistribuable pour les outils de redéfinition de calendrier tiers, qui fonctionne pour les versions antérieures d’Outlook, depuis Outlook 2010. Pour télécharger le programme d’installation, voir [Outlook 2010 : programme d’installation redistribuable auxiliaire référence et fichier d’en-tête pour redéfinir des calendriers](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Référence

Le contenu de référence inclut les éléments suivants :
  
- L' [API exportée par Outlook](about-apis-exported-by-outlook.md) incluent les fonctions et les structures de données qui ont été implémentées à l’origine pour un usage interne et sont maintenant exposés au public. 
    
- L' [API de gestion de compte](about-the-account-management-api.md) permet d’accéder aux informations de compte d’utilisateur et des notifications des modifications de compte. 
    
- L' [API de couche données dégradation](about-the-data-degradation-layer-api.md) prend en charge les clients qui accèdent à un élément Outlook dans un format de caractère par défaut au lieu du format natif de l’objet. 
    
- L' [API de disponibilité](about-the-free-busy-api.md) fournit des informations de disponibilité sur les comptes d’utilisateur spécifiques dans une plage de temps spécifique. 

## <a name="sample-tasks"></a>Exemples de tâches

Exemples de tâches de procédures dans l’autre référence Outlook sont les suivantes :
    
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
    
La référence pour chaque API répertorie les définitions de type, constantes et interfaces qu’un développeur doit implémenter pour utiliser les fonctionnalités supplémentaires.
  
> [!NOTE]
> Les développeurs doivent implémenter ces API uniquement comme indiqué dans cette référence. Certains membres de l’interface et les paramètres de méthode sont nommés comme espaces réservés, car ils sont réservés à un usage interne d’Outlook et peuvent être modifiés sans préavis. 
  

