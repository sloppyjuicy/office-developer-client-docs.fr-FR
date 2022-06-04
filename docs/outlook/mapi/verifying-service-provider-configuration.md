---
title: Vérification de la configuration du fournisseur de services
description: Décrit comment vérifier la configuration du fournisseur de services dans Outlook 2013 et Outlook 2016, avec des documents de référence supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
ms.openlocfilehash: 35aa17f42c8128af893e9154d99d8c36293e94f1
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894144"
---
# <a name="verifying-service-provider-configuration"></a>Vérification de la configuration du fournisseur de services
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre méthode d’ouverture de session ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md) ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) doit vérifier la configuration de votre fournisseur. Cela implique de vérifier que toutes les propriétés nécessaires pour une opération complète sont définies correctement. Chaque fournisseur requiert un nombre différent de propriétés ; la configuration dépend de votre fournisseur et du degré d’interaction utilisateur que vous autorisez. Certains fournisseurs de services conservent toutes les propriétés nécessaires dans le profil. 

D’autres fournisseurs de services conservent un ensemble partiel de propriétés dans le profil et invitent l’utilisateur à rechercher des valeurs manquantes. D’autres fournisseurs ne stockent pas du tout les propriétés dans le profil, en s’appuyant sur l’utilisateur pour fournir toutes les informations nécessaires à la configuration.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Pour récupérer les propriétés stockées dans le profil
  
1. Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), en passant le [MAPIUID](mapiuid.md) de votre fournisseur en tant que paramètre d’entrée. 
    
2. Appelez les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la section de profil pour récupérer des propriétés individuelles ou une liste de propriétés. 
    
### <a name="to-set-properties-from-user-information"></a>Pour définir des propriétés à partir d’informations utilisateur
  
Afficher une feuille de propriétés, si MAPI n’a pas défini d’indicateur interdisant l’affichage. Les indicateurs suivants indiquent qu’une interface utilisateur ne peut pas être présentée.
  
|**Indicateur**|**Fournisseur**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Fournisseur de carnet d’adresses  <br/> |
|LOGON_NO_DIALOG  <br/> |Fournisseur de transport  <br/> |
|MDB_NO_DIALOG  <br/> |Fournisseur de magasin de messages  <br/> |
   
Si votre fournisseur ne stocke pas toutes ses propriétés de configuration dans le profil, nécessitant une interaction de l’utilisateur et que MAPI transmet l’un des indicateurs de suppression de boîte de dialogue à votre méthode d’ouverture de session, retournez MAPI_E_UNCONFIGURED. Retournez également cette erreur lorsque l’indicateur de suppression de boîte de dialogue n’est pas défini, mais que l’utilisateur ne fournit pas toutes les informations requises.
  
Lorsque votre fournisseur de services échoue à sa méthode d’ouverture de session avec MAPI_E_UNCONFIGURED, MAPI appelle à nouveau votre fonction de point d’entrée. Si les informations ne peuvent pas être localisées avec le deuxième appel, la session peut s’arrêter, en fonction de l’importance de votre fournisseur de services. 
  
L’illustration suivante montre la logique requise pour la configuration dans la méthode d’ouverture de session de votre fournisseur de services. 
  
**Diagramme de flux de vérification de la configuration**
  
![Diagramme de flux de vérification de la configuration](media/amapi_62.gif "Diagramme de flux de vérification de la configuration")
  
## <a name="see-also"></a>Voir aussi

- [Implémentation de l’ouverture de session du fournisseur de services](implementing-service-provider-logon.md)

