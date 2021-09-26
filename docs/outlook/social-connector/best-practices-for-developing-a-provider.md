---
title: Meilleures pratiques en matière de développement de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur Outlook Social Connector 2013 (OSC) :'
ms.openlocfilehash: 97405b70b225e7e5c961e07f31bdd5eeb3247bb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608962"
---
# <a name="best-practices-for-developing-a-provider"></a>Meilleures pratiques en matière de développement de fournisseur

Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur Outlook Social Connector 2013 (OSC) :
  
- Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs sur Internet doivent utiliser le protocole HTTPS (Hypertext Transfer Protocol) avec SSL (Secure Socket Layer). Dans le cas contraire, il existe un risque que des adresses de messagerie, des activités de réseau social et d’autres données utilisateur soient interceptées ou exposées en transit.
    
- Si vous développez un fournisseur OSC pour un réseau social tiers, votre fournisseur doit respecter les conditions d’utilisation du réseau social.
    
- Pour réduire la taille du package de téléchargement du fournisseur, créez-le à l’aide d’un compilateur natif tel que C++ ou tout autre outil qui peut créer un composant COM.
    
- Dans votre fournisseur, créez un agent utilisateur unique qui est envoyé au réseau social pour suivre les appels effectués par le fournisseur vers le réseau social.
    
- La [méthode ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) ne doit pas compter sur l’appel du réseau social sur Internet pour obtenir les fonctionnalités du fournisseur. Par exemple, les utilisateurs peuvent démarrer Outlook hors connexion ; Si l’OSC appelle **GetCapabilities** et qu’il n’y a pas de connexion réseau, l’appel **GetCapabilities** ne retournera pas de **fonctionnalités** XML valides. La meilleure pratique consiste à stocker les **fonctionnalités** XML en tant que ressource dans votre fournisseur. 
    
- Votre fournisseur OSC peut générer un volume important d’appels vers un réseau social. Selon les conditions d’utilisation de votre réseau social, envisagez de mettre en cache des amis dans un dossier Outlook pour réduire le nombre d’appels de l’OSC à votre fournisseur et, à son tour, de votre fournisseur vers le réseau social.
    
- Office 2013 est disponible dans les versions 32 bits et 64 bits. Les versions Office antérieures Office 2010 sont disponibles uniquement dans une version 32 bits. L’installation par Office 2013 sur les Windows 64 bits est 32 bits. Si vous envisagez de prendre en charge la version 64 bits d’OSC installée avec Office 2013 64 bits, vous devez également publier une version 64 bits de votre fournisseur. 
    
## <a name="see-also"></a>Voir aussi

- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Déploiement d'un fournisseur](deploying-a-provider.md)  
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

