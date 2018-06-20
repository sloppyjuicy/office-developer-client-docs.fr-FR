---
title: Meilleures pratiques pour le développement d’un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur 2013 Outlook Social Connector (OSC) :'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787573"
---
# <a name="best-practices-for-developing-a-provider"></a>Meilleures pratiques pour le développement d’un fournisseur

Vous devez respecter les pratiques suivantes lorsque vous développez un fournisseur 2013 Outlook Social Connector (OSC) :
  
- Pour des raisons de sécurité, les fournisseurs qui communiquent avec des serveurs via Internet doivent utiliser le protocole HTTPS (Hypertext Transfer Protocol (HTTP) avec Secure Socket Layer (SSL)). Dans le cas contraire, il existe un risque que les adresses de messagerie, les activités de réseaux sociaux et autres utilisateur données peuvent être interceptées ou exposées lors de leur transit.
    
- Si vous développez un fournisseur OSC pour un réseau social tiers, votre fournisseur doit respecter les conditions du réseau social de service.
    
- Pour réduire la taille du package de téléchargement du fournisseur, créez le fournisseur à l’aide d’un compilateur natif tel que C++ ou tout autre outil qui peut créer un composant COM.
    
- Dans votre fournisseur, créez un agent utilisateur unique qui est envoyé au réseau social pour effectuer le suivi des appels effectués par le fournisseur pour le réseaux sociaux.
    
- La méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) doit s’appuie pas sur le réseaux sociaux d’appel via Internet pour obtenir les fonctionnalités du fournisseur. Par exemple, les utilisateurs peuvent démarrer Outlook en mode hors connexion ; Si l’OSC appelle **GetCapabilities** et il n’existe pas de connexion réseau, l’appel **GetCapabilities** ne renvoie pas valide XML des **capacités** . La meilleure pratique consiste à stocker les **fonctionnalités** XML en tant que ressource dans votre fournisseur. 
    
- Votre fournisseur OSC peut générer un volume important d’appels à un réseau social. Selon les termes du contrat de service pour votre réseau social, tenez compte des amis dans un dossier Outlook afin de réduire le nombre d’appels à partir de l’OSC à votre fournisseur et, à son tour, à partir de votre fournisseur de réseau social de la mise en cache.
    
- Office 2013 est disponible dans les versions 32 bits et 64 bits. Les versions d’Office avant d’Office 2010 sont disponibles uniquement dans une version 32 bits. L’installation par défaut d’Office 2013 sur un ordinateur Windows 64 bits est de 32 bits. Si vous souhaitez prendre en charge la version 64 bits de l’OSC qui est installé avec Office 2013 de 64 bits, vous devez également libérer une version 64 bits de votre fournisseur. 
    
## <a name="see-also"></a>Voir aussi

- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Déploiement d'un fournisseur](deploying-a-provider.md)  
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

