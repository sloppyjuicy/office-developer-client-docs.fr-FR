---
title: Création d’un fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
ms.openlocfilehash: 09a4af36468a076ba548947ca4fd0ae10200052f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380843"
---
# <a name="creating-a-form-configuration-file"></a>Création d’un fichier de configuration de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fichier de configuration de formulaire fournit des informations sur un formulaire à la fois au gestionnaire de formulaires utilisé et aux applications clientes. Un fichier de configuration de formulaire contient une spécification complète pour un formulaire, y compris les propriétés publiées par le formulaire pour une utilisation par les clients de messagerie, les verbes implémentés par le formulaire et les plateformes pris en charge par le formulaire.
  
Un fichier de configuration de formulaire est un fichier avec une extension .cfg et a un format similaire à celui d’un Windows d’initialisation. Il s’agit d’un fichier en texte simple avec un certain nombre de sections. Chaque section commence par un nom de section, entre crochets. Chaque section contient une ou plusieurs lignes qui définissent des valeurs et des paramètres pertinents pour cette section. Les valeurs ont l’un des types suivants :
  
- String
    
- Chaîne affichée
    
- Chaîne de plateforme
    
- Nom de chemin d'accès
    
- Entier
    
- GUID
    
Pour plus d’informations sur les sections d’un fichier .cfg, voir Format de fichier [des fichiers de configuration de formulaire](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

