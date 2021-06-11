---
title: Création d’un fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425217"
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
    
Pour plus d’informations sur les sections d’un fichier .cfg, voir Format de fichier des fichiers [de configuration de formulaire.](file-format-of-form-configuration-files.md)
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

