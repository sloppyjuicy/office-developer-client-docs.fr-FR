---
title: Création d’un profil à l’aide de code personnalisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594732"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Création d’un profil à l’aide de code personnalisé

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Si vous choisissez d’écrire du code pour créer un profil, assurez-vous de bien comprendre l’ordre des entrées de profil et le type et la quantité d’informations sont nécessaire pour chaque entrée. Les implications de l’ordre des entrées dans un profil est expliquée dans [Les profils MAPI](mapi-profiles.md).
  
 **Pour créer un profil avec du code C ou C++**
  
1. Lisez le fichier d’en-tête pour chaque service de message. Comprendre les propriétés que vous devez configurer et que les valeurs que vous utilisez.
    
2. Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** . 
    
3. Appelez [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) pour créer votre profil. Si vous souhaitez créer un profil avec les services de message répertoriés dans la section **[Services par défaut]** du fichier MAPISVC.inf. Fichier, définir l’indicateur MAPI_DEFAULT_SERVICE. Si vous souhaitez permettre à l’utilisateur d’entrer les informations de configuration, définir l’indicateur MAPI_DIALOG. Assurez-vous que vous définissez cet indicateur si ce n’est pas toutes les informations nécessaires sont disponibles via le fichier MAPISVC.inf. Fichier. **CreateProfile** appelle la fonction de point d’entrée pour chaque service de message à ajouter au profil avec MSG_SERVICE_CREATE défini en tant que paramètre _ulContext_ . 
    
4. Appelez [IProfAdmin::AdminServices](iprofadmin-adminservices.md) pour obtenir un objet de l’administration de service de message. 
    
5. Utilisez l’objet de l’administration du service de message pour ajouter des services de messagerie au profil. Pour chaque service de message que vous souhaitez ajouter :
    
1. Appelez la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) pour créer le nouveau service de message. 
    
2. Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), en passant la structure **MAPIUID** du service que vous venez de créer et un tableau de valeurs de propriété avec ses propriétés de configuration. 
    
6. Pour récupérer l’identificateur d’un service nouvellement ajouté, qui est sa propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de message, puis recherchez la ligne qui représente le service de message. La dernière ligne de la table devant représenter le service de message dernièrement ajouté. 
    
Pour rendre un nouveau profil temporaire, appeler la méthode [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) immédiatement une fois que vous ouvrez une session. **DeleteProfile** marque le nouveau profil comme étant supprimée tout en les rendant utilisable pour la durée de la session. Car il ne sera pas inclus dans le tableau de profil de la session, les autres clients ne pourront pas l’utiliser. 
  

