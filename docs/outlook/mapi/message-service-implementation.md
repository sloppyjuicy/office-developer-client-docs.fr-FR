---
title: Implémentation du service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434031"
---
# <a name="message-service-implementation"></a>Implémentation du service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un service de messagerie est un ou plusieurs fournisseurs de services associés regroupés dans le but de simplifier l’installation et la configuration. Tous les fournisseurs de services doivent être inclus dans un service de messagerie.
  
Pour implémenter un service de messagerie avec un ou plusieurs fournisseurs, utilisez la procédure suivante :
  
1. Concevez le service de messagerie, en déterminant le nombre et le type de fournisseurs de services à inclure. Pour plus d’informations sur la conception d’un service de message, voir [Conception d’un service de message.](designing-a-message-service.md)
    
2. Créez un programme d’installation pour installer les fournisseurs de services dans le service de messagerie. Pour plus d’informations sur l’écriture d’un programme d’installation de service de message, voir [Prise en charge de l’installation du service de message.](supporting-message-service-installation.md) 
    
3. Créez une fonction de point d’entrée pour effectuer la configuration. Pour plus d’informations sur l’écriture d’une fonction de point d’entrée de service de message, voir [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Créez un fichier d’en-tête public qui contient les balises de propriété et les descriptions des valeurs valides pour toutes les propriétés personnalisées que le service de message prend en charge. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

