---
title: Implémentation du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356916"
---
# <a name="message-service-implementation"></a>Implémentation du service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un service de messagerie est un ou plusieurs fournisseurs de services associés pour simplifier l'installation et la configuration. Tous les fournisseurs de services doivent être inclus dans un service de messagerie.
  
Pour implémenter un service de messagerie avec un ou plusieurs fournisseurs, procédez comme suit:
  
1. Concevez le service de messagerie en déterminant le nombre et le type de fournisseurs de services à inclure. Pour plus d'informations sur la création d'un service de messagerie, consultez la rubrique [conception d'un service de messagerie](designing-a-message-service.md).
    
2. Créez un programme d'installation pour installer les fournisseurs de services dans le service de messagerie. Pour plus d'informations sur l'écriture d'un programme d'installation du service de messagerie, consultez la rubrique [supportIng message service installation](supporting-message-service-installation.md). 
    
3. Créez une fonction de point d'entrée pour effectuer la configuration. Pour plus d'informations sur l'écriture d'une fonction de point d'entrée de service de messagerie, voir [supportIng Configuration service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Créez un fichier d'en-tête public contenant les balises de propriété et des descriptions des valeurs valides pour toutes les propriétés personnalisées prises en charge par le service de messagerie. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

