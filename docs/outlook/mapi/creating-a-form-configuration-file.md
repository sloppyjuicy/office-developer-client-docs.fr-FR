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
ms.openlocfilehash: d8159d93aef020d7c9c1b56be4cf6256f80b8aa3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584166"
---
# <a name="creating-a-form-configuration-file"></a>Création d’un fichier de configuration de formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un fichier de configuration de formulaire fournit des informations sur un formulaire à la fois dans le Gestionnaire de formulaire utilisée et pour les applications clientes. Un fichier de configuration de formulaire contient une spécification d’étendue pour un formulaire, y compris les propriétés publiées par le formulaire pour une utilisation par les clients, les verbes implémentées par le formulaire et les plateformes prises en charge par le formulaire de messagerie.
  
Un fichier de configuration de formulaire est un fichier avec l’extension .cfg et a un format similaire à un fichier d’initialisation de Windows. Il est un fichier texte brut avec un nombre de sections. Chaque section commence par un nom de section, placés entouré crochets. Chaque section contient une ou plusieurs lignes qui définissent les valeurs et les paramètres relatifs à la section. Valeurs de disposer d’un des types suivants :
  
- String
    
- Chaîne affichée
    
- Chaîne de plateforme
    
- Nom de chemin d’accès
    
- Entier
    
- GUID
    
Pour plus d’informations sur les sections d’un fichier .cfg, voir [Fichier fichiers au Format de formulaire Configuration](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

