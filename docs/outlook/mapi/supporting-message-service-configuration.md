---
title: Prise en charge de la configuration du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418994"
---
# <a name="supporting-message-service-configuration"></a>Prise en charge de la configuration du service de messagerie
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour prendre en charge la configuration du service de messagerie, procédez comme suit:
  
1. Implémentez une fonction de point d'entrée conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . Les fonctions de point d'entrée de service de messagerie gèrent l'accès aux données de configuration et sont appelées dans les circonstances suivantes: 
    
   - Lorsqu'un client se connecte pour récupérer des informations afin de configurer votre service de messagerie.
    
   - Lorsqu'un client souhaite afficher ou modifier une propriété de configuration. 
    
   Bien que la plupart des services de message fournissent des fonctions de point d'entrée, comme c'est le cas, ces fonctions ne sont pas strictement obligatoires. Les services de messagerie peuvent fournir un accès aux données de configuration d'autres manières. Toutefois, l'utilisation d'une fonction de point d'entrée standardise et simplifie le processus de configuration.
    
   MAPI s'attend à ce que toutes les fonctions de point d'entrée du service de messagerie soient en mesure de stocker et de récupérer les propriétés des sections de profil associées à leur service de messagerie. Vous pouvez prendre en charge cette fonctionnalité de manière interactive, par programme ou à la fois de façon interactive et à la fois de manière interactive et par programme.
    
   Pour prendre en charge la configuration interactive, fournissez une feuille de propriétés qui affiche les propriétés impliquées dans la configuration de votre service de messagerie. Vous pouvez également fournir des feuilles de propriétés pour chaque fournisseur configurable. Certains services de message restreignent les utilisateurs à une vue en lecture seule des propriétés de configuration; d'autres services de messagerie permettent aux utilisateurs d'effectuer des modifications.
    
   Pour prendre en charge la configuration par programme, la fonction de point d'entrée de service de messagerie doit pouvoir fonctionner sans intervention de l'utilisateur. Si votre service de messagerie peut être appelé par l'Assistant Profil, vous devez prendre en charge la configuration par programme. Si votre service de messagerie ne s'autorise pas à être configuré à l'aide de l'Assistant Profil, vous pouvez choisir de prendre en charge la configuration par programme.
    
   Pour plus d'informations sur la prise en charge de la configuration dans une fonction de point d'entrée de service de messagerie, voir [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publiez le nom de votre fonction de point d'entrée de service de message dans le fichier de configuration MAPISVC. inf en incluant l'entrée suivante dans la section service de messagerie:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Créer une ou plusieurs boîtes de dialogue de feuille de propriétés pour afficher les données de configuration.
    
4. Effectuez les tâches suivantes si vous souhaitez autoriser l'Assistant Profil à configurer votre service de messagerie:
    
   - Implémentez une fonction de point d'entrée conforme au prototype [WIZARDENTRY](wizardentry.md) . 
    
   - Implémentez une procédure de boîte de dialogue Windows standard conforme au prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
    
   - Améliorez votre fonction de point d'entrée de service de messagerie pour répondre à des événements supplémentaires.
    
## <a name="see-also"></a>Voir aussi

- [Implémentation du service de messagerie](message-service-implementation.md)

