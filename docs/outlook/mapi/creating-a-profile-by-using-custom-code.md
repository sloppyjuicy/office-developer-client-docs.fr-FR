---
title: Créer un profil à l’aide de code personnalisé
manager: lindalu
ms.date: 03/01/2022
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
ms.openlocfilehash: 5a2e1711af91fab22e7881223d7325c774024739
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370077"
---
# <a name="create-a-profile-by-using-custom-code"></a>Créer un profil à l’aide de code personnalisé
  
**S’applique à** : Outlook 2013 | Outlook 2016
  
Si vous choisissez d’écrire du code pour créer un profil, assurez-vous de comprendre comment commander les entrées de profil, ainsi que le type et la quantité d’informations nécessaires pour chaque entrée. Les implications de l’ordre des entrées dans un profil sont expliquées dans les [profils MAPI](mapi-profiles.md).
  
## <a name="to-create-a-profile-with-c-or-c-code"></a>Pour créer un profil avec du code C ou C++
  
1. Lisez le fichier d’en-tête de chaque service de message. Comprenez les propriétés que vous devrez configurer et les valeurs que vous utiliserez.

1. Appelez la [fonction MAPIAdminProfiles pour](mapiadminprofiles.md) récupérer un pointeur d’interface **IProfAdmin** .

1. [Appelez IProfAdmin::CreateProfile](iprofadmin-createprofile.md) pour créer votre profil. Si vous souhaitez créer un profil avec les services de message répertoriés dans la section **[Services** par défaut] de MAPISVC. Fichier INF, définissez l’MAPI_DEFAULT_SERVICE’indicateur. Si vous souhaitez permettre à l’utilisateur d’entrer des informations de configuration, définissez l MAPI_DIALOG de configuration. Assurez-vous de définir cet indicateur si toutes les informations nécessaires ne sont pas disponibles via MAPISVC. Fichier INF. **CreateProfile appelle** la fonction de point d’entrée pour chaque service de message à ajouter au profil avec MSG_SERVICE_CREATE définie en tant que _paramètre ulContext_ .

1. [Appelez IProfAdmin::AdminServices pour](iprofadmin-adminservices.md) obtenir un objet d’administration de service de message.

1. Utilisez l’objet d’administration du service de message pour ajouter des services de message au profil. Pour chaque service de message que vous souhaitez ajouter :

1. Appelez [la méthode IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) pour créer le service de message.

1. Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), en passant la structure **MAPIUID** du service que vous avez créé et un tableau de valeurs de propriétés avec ses propriétés de configuration.

1. Pour récupérer l’identificateur d’un service nouvellement ajouté, qui est sa propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de message et rechercher la ligne qui représente le service de message. La dernière ligne du tableau représente le service de message le plus récemment ajouté.

Pour rendre un nouveau profil temporaire, appelez la méthode [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) immédiatement après votre connexion. **DeleteProfile marque** le nouveau profil comme étant supprimé tout en le rendant utilisable pendant toute la durée de la session. Comme il ne sera pas inclus dans la table de profils de la session, les autres clients ne pourront pas l’utiliser.
  