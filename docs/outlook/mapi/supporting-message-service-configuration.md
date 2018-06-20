---
title: Prise en charge de la configuration du service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787276"
---
# <a name="supporting-message-service-configuration"></a>Prise en charge de la configuration du service de message
  
**S’applique à**: Outlook 
  
Pour prendre en charge la configuration du service de message, utilisez la procédure suivante :
  
1. Implémenter une fonction de point d’entrée est conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . Fonctions de point d’entrée message service gérer l’accès aux données de configuration et sont appelées dans les circonstances suivantes : 
    
   - Lorsqu’un client se connecte pour récupérer des informations pour configurer votre service de message.
    
   - Lorsqu’un client souhaite afficher ou modifier une propriété de configuration. 
    
   Bien que la plupart des services de messagerie fournissent des fonctions de point d’entrée, comme il faut, ces fonctions ne sont pas obligatoires. Services de messagerie peuvent fournir l’accès aux données de configuration par d’autres moyens. Toutefois, à l’aide d’une fonction de point d’entrée normalise et simplifie le processus de configuration.
    
   MAPI attend tous les messages service entrée point les fonctions pour être en mesure de stocker et récupérer les propriétés des sections qui sont associées au service de message de leur profil. Prendre en charge cette fonctionnalité interactive, par programmation, ou les deux interactive et par programme.
    
   Pour prendre en charge la configuration interactive, fournir une feuille de propriétés qui affiche les propriétés nécessaires à la configuration de votre service de message. En tant qu’option, vous pouvez également fournir des feuilles de propriétés pour chaque fournisseur configurable. Certains services message restreindre les utilisateurs à un affichage en lecture seule des propriétés de configuration ; autres services de messagerie permettent aux utilisateurs d’apporter des modifications.
    
   Pour prendre en charge la configuration par programme, votre fonction de point d’entrée message service doit être en mesure de fonctionner sans intervention de l’utilisateur. Si votre service de message peut être appelé par l’Assistant profil, à prendre en charge une configuration par programme. Si votre service de message n’autorise pas elle-même être configurés à l’aide de l’Assistant profil, vous pouvez choisir s’il faut prendre en charge la configuration par programme.
    
   Pour plus d’informations sur la prise en charge de configuration dans une entrée de service de message point fonction, voir [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publier le nom de la fonction de point de message service entrée dans le fichier de configuration Mapisvc.inf en incluant l’entrée suivante dans la section service de message :
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Créer une ou plusieurs propriétés feuille boîtes de dialogue pour afficher les données de configuration.
    
4. Effectuer les tâches suivantes si vous souhaitez permettre à l’Assistant profil configurer votre service de message :
    
   - Implémenter une fonction de point d’entrée est conforme au prototype [WIZARDENTRY](wizardentry.md) . 
    
   - Implémenter une procédure de boîte de dialogue Windows standard qui est conforme au prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
    
   - Améliorez votre fonction point d’entrée message service pour répondre aux événements supplémentaires.
    
## <a name="see-also"></a>Voir aussi

- [Mise en œuvre de message](message-service-implementation.md)

