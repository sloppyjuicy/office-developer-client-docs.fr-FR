---
title: Vérification de la configuration de fournisseur de service
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 047a3b99b2d615984252071a1264521a4b2240f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787461"
---
# <a name="verifying-service-provider-configuration"></a>Vérification de la configuration de fournisseur de service
  
**S’applique à**: Outlook 
  
Votre méthode d’ouverture de session ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) doit vérifier la configuration de votre fournisseur. Cela consiste à vérifier que toutes les propriétés nécessaires pour l’opération complète sont correctement définies. Chaque fournisseur nécessite un nombre différent de propriétés. configuration dépend de votre fournisseur et le degré d’interaction utilisateur que vous autorisez. Certains fournisseurs de services conserver toutes les propriétés nécessaires dans le profil. 

Autres fournisseurs de services de conserver un jeu de propriétés partiel dans le profil et invite l’utilisateur pour les valeurs manquantes. Toujours autres fournisseurs ne stockent pas les propriétés dans le profil, tout dépend de l’utilisateur à fournir toutes les informations nécessaires pour la configuration.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Pour récupérer les propriétés stockées dans le profil
  
1. Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), en passant le [MAPIUID](mapiuid.md) de votre fournisseur comme un paramètre d’entrée. 
    
2. Appeler des méthodes de la section profil [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) pour récupérer les propriétés individuelles ou une liste de propriétés. 
    
### <a name="to-set-properties-from-user-information"></a>Pour définir les propriétés à partir des informations utilisateur
  
Afficher une feuille de propriétés, si MAPI n’a pas défini un indicateur interdisant l’affichage. Les indicateurs suivants indiquent qu’une interface utilisateur ne peut pas être présentée.
  
|**Flag**|**Fournisseur de services**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Fournisseur de carnet d’adresses  <br/> |
|LOGON_NO_DIALOG  <br/> |Fournisseur de transport  <br/> |
|MDB_NO_DIALOG  <br/> |Fournisseur de banque de messages  <br/> |
   
Si votre fournisseur ne stocke pas toutes ses propriétés de configuration dans le profil, solliciter l’utilisateur et MAPI un des indicateurs de suppression boîte dialogue passe à votre méthode d’ouverture de session, retourne MAPI_E_UNCONFIGURED. Renvoie également cette erreur lors de l’indicateur de suppression de boîte de dialogue n’est pas défini, mais l’utilisateur ne fournit pas toutes les informations requises.
  
En cas de votre fournisseur de services de la méthode d’ouverture de session avec MAPI_E_UNCONFIGURED, MAPI appelle de nouveau la fonction de point d’entrée. Si les informations ne peut pas être localisées avec le deuxième appel, la session peut arrêter, selon l’importance de votre fournisseur de services. 
  
L’illustration suivante montre la logique requise pour la configuration de votre méthode d’ouverture de session service fournisseur. 
  
**Organigramme de vérification de configuration**
  
![Organigramme de vérification de configuration] (media/amapi_62.gif "Organigramme de vérification de configuration")
  
## <a name="see-also"></a>Voir aussi

- [L’implémentation du fournisseur de Service d’ouverture de session](implementing-service-provider-logon.md)

