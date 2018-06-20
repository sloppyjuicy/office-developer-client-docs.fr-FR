---
title: Développement d’un fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783154"
---
# <a name="developing-a-mapi-address-book-provider"></a>Développement d’un fournisseur de carnet d’adresses MAPI

  
  
**S’applique à**: Outlook 
  
Un fournisseur de carnet d’adresses fournit des informations de destinataires pour les applications clientes, à la banque de messages et fournisseurs, de transport et MAPI. Informations sur le destinataires sont organisées hiérarchiquement en compartiments de stockage appelés conteneurs. Chaque carnet d’adresses dans le profil contribue à un ou plus niveau supérieur, ou parent, conteneurs MAPI carnet d’adresses, un affichage intégré d’informations sur le destinataires à partir de toutes les adresses du livre fournisseurs dans une session. Il est par le biais du carnet d’adresses MAPI que les clients et autres fournisseurs de services accéder aux données d’un fournisseur de carnet d’adresses.
  
MAPI génère le carnet d’adresses intégré par :
  
1. Récupérer les conteneurs de niveau supérieur à partir de chaque fournisseur de carnet d’adresses.
    
2. Extraction de table de hiérarchie de chaque conteneur. 
    
3. Copie de chaque table de hiérarchie dans une table de hiérarchie intégré. Il est la table de hiérarchie intégré qui est exposée au client. 
    
MAPI impose certains éléments requis sur les auteurs de fournisseur adresse téléchargeable. La gamme de fonctionnalités possibles que vous pouvez implémenter un enregistreur de carnet d’adresse est variés et flexibles. Par exemple, votre fournisseur peut être limité à fournir une vue en lecture seule d’un type particulier d’informations sur le destinataires ou implémenter un ensemble complet de fonctionnalités, permettant ainsi peut-être des clients ou fournisseurs de faire des ajouts ou modifications aux données destinataires et d’imposer les critères de recherche pour définir des vues personnalisées. 
  
Les données de votre fournisseur peuvent résider localement dans un fichier de base de données ou sur un serveur distant. Certains fournisseurs de carnet d’adresses sont conçus pour fonctionner avec un système de messagerie particulier, fortement couplé à un fournisseur de transport, tandis que d’autres personnes peuvent fonctionner avec tout système de messagerie.
  
MAPI définit un type particulier de fournisseur de carnet d’adresses appelée un carnet d’adresses personnel ou le carnet d’adresses personnel, qui implémente un seul conteneur modifiable et peut contenir des informations sur les destinataires copiées à partir d’autres conteneurs, ainsi que les informations créées directement. Bien que n’importe quel fournisseur de carnet d’adresses peut mettre en œuvre un carnet d’adresses personnel et plusieurs carnets d’adresses personnels peuvent être ajoutés à un profil, un seul de ces fournisseurs peut être désigné pour fonctionner en tant que le carnet d’adresses personnel pendant toute une session. 
  

