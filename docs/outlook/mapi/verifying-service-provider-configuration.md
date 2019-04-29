---
title: Vérification de la configuration du fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418847"
---
# <a name="verifying-service-provider-configuration"></a>Vérification de la configuration du fournisseur de services
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre méthode d'ouverture de session ([IABProvider:: Logon](iabprovider-logon.md), [IMSProvider:: Logon](imsprovider-logon.md), ou [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md)) doit vérifier la configuration de votre fournisseur. Cela implique de vérifier que toutes les propriétés nécessaires pour une opération complète sont correctement définies. Chaque fournisseur requiert un nombre de propriétés différent; la configuration dépend de votre fournisseur et du degré d'interaction des utilisateurs que vous autorisez. Certains fournisseurs de services conservent toutes les propriétés nécessaires dans le profil. 

Les autres fournisseurs de services conservent un ensemble partiel de propriétés dans le profil et invitent l'utilisateur à indiquer les valeurs manquantes. D'autres fournisseurs ne stockent pas les propriétés dans le profil, en s'appuyant sur l'utilisateur pour fournir toutes les informations nécessaires à la configuration.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Pour récupérer les propriétés stockées dans le profil
  
1. Appelez [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), en transmettant l' [MAPIUID](mapiuid.md) de votre fournisseur en tant que paramètre d'entrée. 
    
2. Appelez les méthodes [IMAPIProp:: GetProps](imapiprop-getprops.md) ou IMAPIProp:: [GetPropList](imapiprop-getproplist.md) de la section Profil pour récupérer des propriétés individuelles ou une liste de propriétés. 
    
### <a name="to-set-properties-from-user-information"></a>Pour définir des propriétés à partir des informations utilisateur
  
Afficher une feuille de propriétés, si MAPI n'a pas défini un indicateur qui interdit l'affichage. Les indicateurs suivants indiquent qu'une interface utilisateur ne peut pas être présentée.
  
|**Indicateur**|**Fournisseur de services**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Fournisseur de carnets d'adresses  <br/> |
|LOGON_NO_DIALOG  <br/> |Fournisseur de transport  <br/> |
|MDB_NO_DIALOG  <br/> |Fournisseur de banque de messages  <br/> |
   
Si votre fournisseur ne stocke pas toutes ses propriétés de configuration dans le profil, nécessite une intervention de l'utilisateur et MAPI transmet l'un des indicateurs de suppression de la boîte de dialogue à votre méthode d'ouverture de session, renvoie MAPI_E_UNCONFIGURED. Renvoie également cette erreur lorsque l'indicateur de suppression de boîte de dialogue n'est pas défini, mais que l'utilisateur ne fournit pas toutes les informations requises.
  
Lorsque votre fournisseur de services échoue à sa méthode d'ouverture de session avec MAPI_E_UNCONFIGURED, MAPI appelle à nouveau votre fonction de point d'entrée. Si les informations ne peuvent pas être localisées avec le deuxième appel, la session peut se terminer, en fonction de l'importance de votre fournisseur de services. 
  
L'illustration suivante montre la logique requise pour la configuration dans votre méthode de connexion au fournisseur de services. 
  
**Diagramme de flux de vérification de la configuration**
  
![Organigramme de vérification] de la configuration (media/amapi_62.gif "Organigramme de vérification") de la configuration
  
## <a name="see-also"></a>Voir aussi

- [Implémentation de la connexion au fournisseur de services](implementing-service-provider-logon.md)

