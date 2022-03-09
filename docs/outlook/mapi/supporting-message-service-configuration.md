---
title: Prise en charge de la configuration du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
ms.openlocfilehash: 9f1b8e66e05b1a29f1490e6452558b3ce1461bac
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379030"
---
# <a name="supporting-message-service-configuration"></a>Prise en charge de la configuration du service de messagerie
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour prendre en charge la configuration du service de message, utilisez la procédure suivante :
  
1. Implémenter une fonction de point d’entrée conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . Les fonctions de point d’entrée de service de message gèrent l’accès aux données de configuration et sont appelées dans les circonstances suivantes : 
    
   - Lorsqu’un client se connecte pour récupérer des informations afin de configurer votre service de message.
    
   - Lorsqu’un client souhaite afficher ou modifier une propriété de configuration. 
    
   Bien que la plupart des services de message fournissent des fonctions de point d’entrée, comme ils le devraient, ces fonctions ne sont pas strictement requises. Les services de message peuvent fournir l’accès aux données de configuration d’autres manières. Toutefois, l’utilisation d’une fonction de point d’entrée standardise et simplifie le processus de configuration.
    
   MAPI s’attend à ce que toutes les fonctions de point d’entrée du service de message puissent stocker et récupérer des propriétés à partir des sections de profil associées à leur service de message. Vous pouvez prendre en charge cette fonctionnalité de manière interactive, par programme ou de manière interactive et par programme.
    
   Pour prendre en charge la configuration interactive, fournissez une feuille de propriétés qui affiche les propriétés impliquées dans la configuration de votre service de message. En tant qu’option, vous pouvez également fournir des feuilles de propriétés pour chaque fournisseur configurable. Certains services de message limitent les utilisateurs à une vue en lecture seule des propriétés de configuration . d’autres services de message permettent aux utilisateurs d’apporter des modifications.
    
   Pour prendre en charge la configuration par programme, votre fonction de point d’entrée de service de message doit pouvoir fonctionner sans intervention de l’utilisateur. Si votre service de message peut être appelé par l’Assistant Profil, vous devez prendre en charge la configuration par programme. Si votre service de message ne s’autorise pas à être configuré à l’aide de l’Assistant Profil, vous pouvez choisir de prendre en charge ou non la configuration par programme.
    
   Pour plus d’informations sur la prise en charge de la configuration dans une fonction de point d’entrée de service de message, voir [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publiez le nom de votre fonction de point d’entrée de service de message dans le fichier de configuration Mapisvc.inf en incluant l’entrée suivante dans la section service de message :
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Créez une ou plusieurs boîtes de dialogue de feuille de propriétés pour afficher les données de configuration.
    
4. Effectuez les tâches suivantes si vous souhaitez autoriser l’Assistant Profil à configurer votre service de message :
    
   - Implémenter une fonction de point d’entrée conforme au prototype [WIZARDENTRY](wizardentry.md) . 
    
   - Implémentez une Windows de dialogue standard conforme au prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md). 
    
   - Améliorez votre fonction de point d’entrée de service de message pour répondre à des événements supplémentaires.
    
## <a name="see-also"></a>Voir aussi

- [Implémentation du service de message](message-service-implementation.md)

