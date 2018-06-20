---
title: Mise en œuvre de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784881"
---
# <a name="message-service-implementation"></a>Mise en œuvre de message

  
  
**S’applique à**: Outlook 
  
Un service de message est un ou plusieurs fournisseurs de services connexes regroupés en vue de simplifier l’installation et la configuration. Tous les fournisseurs de services doivent être inclus dans un service de message.
  
Pour implémenter un service de message avec un ou plusieurs fournisseurs, utilisez la procédure suivante :
  
1. Conception du service de message, déterminer le nombre et le type de fournisseurs de services à inclure. Pour plus d’informations sur la conception d’un service de message, consultez [conception d’un Service de Message](designing-a-message-service.md).
    
2. Créer un programme d’installation pour installer les fournisseurs de services dans le service de message. Pour plus d’informations sur l’écriture d’un programme d’installation du service message, consultez [Installation du Service de Message prise en charge](supporting-message-service-installation.md). 
    
3. Créez une fonction de point d’entrée pour effectuer une configuration. Pour plus d’informations sur l’écriture d’une entrée de service de message point fonction, voir [Configuration du Service de Message prise en charge](supporting-message-service-configuration.md) et [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Créez un fichier d’en-tête public qui contient des descriptions des valeurs valides pour les propriétés personnalisées que le service prend en charge les balises de propriété. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

