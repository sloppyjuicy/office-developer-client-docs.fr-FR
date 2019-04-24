---
title: Création d'un profil à l'aide d'un code personnalisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335789"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Création d'un profil à l'aide d'un code personnalisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous choisissez d'écrire du code pour créer un profil, assurez-vous que vous comprenez comment commander des entrées de profil, ainsi que le type et la quantité d'informations nécessaires pour chaque entrée. Les implications de la commande d'entrées dans un profil sont expliquées dans les [profils MAPI](mapi-profiles.md).
  
 **Pour créer un profil avec du code C ou C++**
  
1. Lisez le fichier d'en-tête pour chaque service de messagerie. Comprenez les propriétés que vous devrez configurer et les valeurs que vous utiliserez.
    
2. Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d'interface **IProfAdmin** . 
    
3. Appelez [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) pour créer votre profil. Si vous souhaitez créer un profil avec les services de messagerie figurant dans la section **[default services]** du MAPISVC. INF, définissez l'indicateur MAPI_DEFAULT_SERVICE. Si vous souhaitez permettre à l'utilisateur d'entrer des informations de configuration, définissez l'indicateur MAPI_DIALOG. Veillez à définir cet indicateur si toutes les informations nécessaires ne sont pas disponibles via le MAPISVC. Fichier INF. **CreateProfile** appelle la fonction de point d'entrée pour chaque service de messagerie à ajouter au profil avec MSG_SERVICE_CREATE défini en tant que paramètre _ulContext_ . 
    
4. Appelez [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) pour obtenir un objet d'administration de service de messagerie. 
    
5. Utilisez l'objet d'administration du service de messagerie pour ajouter des services de messagerie au profil. Pour chaque service de messagerie que vous souhaitez ajouter:
    
1. Appelez la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) pour créer le nouveau service de messagerie. 
    
2. Appelez [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), en transmettant la structure **MAPIUID** du service que vous venez de créer et un tableau de valeurs de propriété avec ses propriétés de configuration. 
    
6. Pour récupérer l'identificateur d'un service nouvellement ajouté, qui est sa propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), appelez [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de messages et rechercher la ligne qui représente service de messagerie. La dernière ligne du tableau représente le dernier service de messagerie ajouté. 
    
Pour créer un nouveau profil temporaire, appelez la méthode [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) immédiatement après avoir connecté. **DeleteProfile** marquera le nouveau profil comme supprimé tout en le rendant utilisable pendant la durée de la session. Étant donné qu'elle ne sera pas incluse dans la table de profils de la session, les autres clients ne pourront pas l'utiliser. 
  

